---
title: Rozšírenie zadaní času
description: Tento článok poskytuje informácie o tom, ako môžu vývojári rozšíriť ovládací prvok zadávania času.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914789"
---
# <a name="extending-time-entries"></a>Rozšírenie zadaní času

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations obsahuje rozšíriteľný vlastný prvok na zadávanie času. Toto riadenie obsahuje nasledujúce funkcie:

- Horizontálne zadávanie času počas týždňa
- Súčty za deň, riadok alebo týždeň
- Kopírovanie riadkov alebo týždňov
- Zadávanie času ako HH:mm alebo HH.hh (automaticky sa prevedie na HH.hh)
- Importovanie z priradení rezervácií alebo plánovaných činností

Predĺženie zadaní času je možné v dvoch oblastiach:
- [Pridávanie vlastných zadaní času na vlastné použitie](#add)
- [Prispôsobenie riadenia týždenných zadaní času](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Pridávanie vlastných zadaní času na vlastné použitie

Zadania času sú základnou entitou používanou vo viacerých scenároch. V aprílovom pláne Wave 1 2020 bolo predstavené základné riešenie TESA. TESA poskytuje entitu **Nastavenia** a novú rolu zabezpečenia **Používateľ zadania času**. Boli zahrnuté aj nové polia, **msdyn_start** a **msdyn_end**, ktoré majú priamy vzťah s **msdyn_duration**. Nová entita, rola zabezpečenia a polia umožňujú jednotnejší prístup k času vo viacerých produktoch.


### <a name="time-source-entity"></a>Zdrojová entita času
| Pole | Popis | 
|-------|------------|
| Meno  | Názov zdrojovej entity času použitý ako hodnota výberu pri vytváraní zadaní času. |
| Predvolený zdroj času [Zdroj času: isdefault] | Predvolene môže byť označený iba jeden zdroj času. To umožňuje, aby sa položky predvolene nastavili na zdroj času, ak nie je zadaný. |
|Typ zdroja času [Zdroj času: sourcetype] | Typ zdroja je voliteľná možnosť (Typ zdroja zadania času), ktorá umožňuje priradenie zdroja času k aplikácii. Spoločnosť Microsoft si vyhradzuje hodnoty väčšie ako 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Zadania času a entita zdroja času
Každé zadanie času je spojené so záznamom zdroja času. Tento záznam určuje, ktoré aplikácie majú spracovať zadanie času a ako.

Zadania času sú vždy jedným súvislým časovým blokom s prepojeným začiatkom, koncom a časom trvania.

Logika automaticky aktualizuje záznam zadania času v nasledujúcich situáciách:

- Ak sú k dispozícii dve z troch nasledujúcich polí, tretie sa počíta automaticky: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Polia **msdyn_start** a **msdyn_end** zohľadňujú časové pásmo.
- Zadania času vytvorené iba s uvedenými **msdyn_date** a **msdyn_duration** začnú o polnoci. Polia **msdyn_start** a **msdyn_end** sa príslušným spôsobom aktualizujú.

#### <a name="time-entry-types"></a>Typy zadania času

Záznamy o zadaní času majú pridružený typ, ktorý definuje správanie v toku príspevkov pre priradenú aplikáciu.

|Označenie | Hodnota|
|-----|-----|
|Zastavené   |192,355,000|
|Cesta | 192,355,001|
|Nadčas   | 192,354,320|
|Práca   | 192,350,000|
|Neprítomnosť    | 192,350,001|
|Dovolenka   | 192,350,002|


## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Prispôsobenie riadenia týždenných zadaní času
Vývojári môžu pridať ďalšie polia a vyhľadávania k ďalším entitám a implementovať vlastné obchodné pravidlá na podporu svojich obchodných scenárov.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Pridanie vlastných polí s hľadaním iných entít
Existujú tri hlavné kroky na pridanie vlastného poľa do mriežky týždenného vstupného času.

1. Pridajte vlastné pole do dialógového okna **Rýchle vytvorenie**.
2. Nakonfigurujte mriežku na zobrazenie vlastného poľa.
3. Pridajte vlastné pole na stránku **Úprava riadka** alebo **Úprava zadania času** podľa potreby.

Uistite sa, že nové pole má požadované overenia na stránke **Úprava riadka** alebo **Úprava zadania času**. V rámci tejto úlohy zamknite pole na základe stavu zadania času.

Keď pridáte vlastné pole do mriežky **Zadanie času** a potom vytvoríte časové položky priamo v mriežke, vlastné pole pre tieto položky sa automaticky nastaví tak, aby sa zhodovalo s riadkom. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Pridanie vlastného poľa do dialógového okna Rýchle vytvorenie
Vlastné pole pridajte do dialógového okna **Rýchle vytvorenie: Vytvorenie zadania času**. Používatelia potom môžu zadať hodnotu, keď pridajú zadania času výberom možnosti **Nová**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Nakonfigurujte mriežku na zobrazenie vlastného poľa
Existujú dva spôsoby na pridanie vlastného poľa do mriežky **Týždenné zadanie času**.

- Prispôsobte zobrazenie **Moje týždenné zadania času** a pridajte do neho vlastné pole. Úpravou vlastností v zobrazení môžete určiť umiestnenie a veľkosť vlastného poľa v mriežke.
- Vytvorte nové vlastné zobrazenie časového vstupu a nastavte ho ako predvolené zobrazenie. Toto zobrazenie by malo obsahovať polia **Popis** a **Externé komentáre** okrem stĺpcov, ktoré chcete zahrnúť do mriežky. Úpravou vlastností v zobrazení môžete určiť umiestnenie, veľkosť a predvolené poradie zoradenia vlastného poľa v mriežke. Potom nakonfigurujte vlastný ovládací prvok pre toto zobrazenie, aby bol išlo o ovládací prvok **Mriežka so zadaniami času**. Pridajte tento ovládací prvok do zobrazenia a vyberte ho pre **Web**, **Telefón** a **Tablet**. Potom nakonfigurujte parametre pre mriežku **Týždenné zadanie času**. Nastavte pole **Počiatočný dátum** na **msdyn\_date**, pole **Trvanie** na **msdyn\_duration** a pole **Status** na **msdyn\_entrystatus**. Pole **Zoznam stavov iba na čítanie** je nastavené na **192350002 (Schválené)**, **192350003 (Odoslané)** alebo **192350004 (Bola podaná žiadosť o odvolanie)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Pridanie vlastného poľa do na príslušnú stránky úprav
Stránky, ktoré sa používajú na úpravu časových záznamov alebo riadkov časových záznamov, nájdete pod položkou **Formuláre**. Tlačidlo **Upraviť zadanie** v mriežke otvorí stránku **Úprava zadania** a tlačidlo **Upraviť riadok** otvorí stránku **Úprava riadka**. Tieto stránky môžete upraviť tak, aby obsahovali vlastné polia.

Obe možnosti odstránia niektoré predpripravené filtrovanie v entitách **Projekt** a **Projektová úloha**, takže všetky zobrazenia vyhľadávania pre entity sú viditeľné. Predpripravene sú viditeľné iba relevantné zobrazenia vyhľadávania.

Musíte určiť príslušnú stránku pre vlastné pole. S najväčšou pravdepodobnosťou, ak ste do mriežky pridali pole, malo by sa dostať na stránku **Úprava riadka**, ktorá sa používa pre polia, ktoré sa vzťahujú na celý riadok časových položiek. Ak má vlastné pole v riadku každý deň jedinečnú hodnotu (napríklad ak ide o vlastné pole pre čas ukončenia), malo by sa nachádzať na stránke **Úprava zadania času**.

Ak chcete pridať vlastné pole na stránku, presuňte prvok **Pole** do príslušnej pozície na stránke a potom nastavte jeho vlastnosti.

### <a name="add-new-option-set-values"></a>Pridanie nových hodnôt množiny možností
Ak chcete pridať hodnoty množiny možností do vopred pripraveného poľa, postupujte podľa týchto krokov.

1. Otvorte stránku úprav pre pole a potom v časti **Typ** vyberte položku **Upraviť** vedľa množiny možností.
2. Pridajte novú možnosť, ktorá má vlastný štítok a farbu. Ak chcete pridať nový stav položky času, predpripravené pole má názov **Stav zadania**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Označenie nového stavu položky času ako iba na čítanie
Ak chcete určiť stav nového zadania času iba na čítanie, pridajte novú hodnotu zadania času do vlastnosti **Zoznam stavov iba na čítanie**. Nezabudnite pridať číslo, nie označenie. Upraviteľná časť mriežky zadania času bude zamknutá pre riadky, ktoré majú nový stav. Ak chcete nastaviť vlastnosť **Zoznam stavov iba na čítanie** inak pre rôzne zobrazenia **Zadanie času**, pridajte mriežku **Zadanie času** v sekcii **Vlastné ovládacie prvky** a nakonfigurujte parametre podľa potreby.

V ďalšom kroku pridajte obchodné pravidlá na uzamknutie všetkých polí na stránkach **Úprava riadka** a **Úprava zadania času**. Ak chcete získať prístup k obchodným pravidlám pre tieto stránky, otvorte editor formulárov pre každú stránku a potom vyberte položku **Obchodné pravidlá**. Nový stav môžete pridať k podmienke v existujúcich obchodných pravidlách, alebo môžete pridať nové obchodné pravidlo pre nový stav.

### <a name="add-custom-validation-rules"></a>Pridávanie vlastných overovacích pravidiel
Pre prostredie s mriežkou **Týždenné zadanie času** môžete pridať dva typy pravidiel overovania:

- Obchodné pravidlá na strane klienta, ktoré fungujú na stránkach
- Overenie doplnku na strane servera, ktoré sa vzťahuje na všetky aktualizácie zadávania času

#### <a name="client-side-business-rules"></a>Obchodné pravidlá na strane klienta
Použite obchodné pravidlá na uzamykanie a odomykanie polí, zadajte predvolené hodnoty do polí a definujte overenia, ktoré vyžadujú informácie len z aktuálneho záznamu o čase. Ak chcete získať prístup k obchodným pravidlám pre stránku, otvorte editor formulárov a potom vyberte položku **Obchodné pravidlá**. Potom môžete upraviť existujúce obchodné pravidlá alebo pridať nové obchodné pravidlo.

#### <a name="server-side-plug-in-validations"></a>Overenie doplnkov na strane servera
Overenia doplnku by ste mali použiť pre akékoľvek overenia vyžadujúce si viac kontextu než je dostupný v samostatnom zázname zadania času. Mali by ste ich použiť aj na akékoľvek overenia, ktoré chcete spustiť pri inline aktualizáciách v mriežke. Ak chcete dokončiť overenia, vytvorte vlastný doplnok v entite **Zadanie času**.

### <a name="limits"></a>Limity
V súčasnosti má mriežka **Zadanie času** limit veľkosti 500 riadkov. Ak existuje viac ako 500 riadkov, prebytočné riadky sa nezobrazia. Neexistuje spôsob, ako tento limit veľkosti zvýšiť.

### <a name="copying-time-entries"></a>Kopírovanie zadaní času
Pomocou zobrazenia **Kopírovať stĺpce zadaní času** definujte zoznam polí, ktoré sa majú kopírovať počas zadávania času. **Dátum** a **Trvanie** sú povinné polia a nemali by byť odstránené zo zobrazenia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
