---
title: Rozšírenie zadaní času
description: Táto téma poskytuje informácie o tom, ako môžu vývojári rozšíriť riadenie zadaní času.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583005"
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

- The **msdyn_start** a **msdyn_end** polia poznajú časové pásmo.
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

1. Pridajte vlastné pole do **Rýchla tvorba** dialógové okno.
2. Nakonfigurujte mriežku na zobrazenie vlastného poľa.
3. Pridajte vlastné pole do **Úprava riadkov** alebo **Úprava zadania času** podľa potreby.

Uistite sa, že nové pole obsahuje požadované overenia **Úprava riadkov** alebo **Úprava zadania času** stránku. V rámci tejto úlohy zamknite pole na základe stavu zadania času.

Keď pridáte vlastné pole do **Zadanie času** mriežky a potom vytvorte časové položky priamo v mriežke, vlastné pole pre tieto položky sa automaticky nastaví tak, aby sa zhodovalo s riadkom. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Pridajte vlastné pole do dialógového okna Rýchle vytvorenie
Pridajte vlastné pole do **Rýchle vytvorenie: Vytvorenie záznamu času** dialógové okno. Používatelia potom môžu zadať hodnotu, keď pridajú zadania času výberom možnosti **Nová**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Nakonfigurujte mriežku na zobrazenie vlastného poľa
Existujú dva spôsoby pridania vlastného poľa do **Týždenný vstup času** mriežka.

- Prispôsobte si **Moje týždenné časové záznamy** a pridajte doň vlastné pole. Úpravou vlastností v zobrazení môžete určiť polohu a veľkosť vlastného poľa v mriežke.
- Vytvorte nové vlastné zobrazenie záznamu času a nastavte ho ako predvolené zobrazenie. Tento pohľad by mal obsahovať **Popis** a **Externé komentáre** polia okrem stĺpcov, ktoré má mriežka zahrnúť. Úpravou vlastností v zobrazení môžete určiť polohu, veľkosť a predvolené poradie zoradenia mriežky. Potom nakonfigurujte vlastný ovládací prvok pre toto zobrazenie, aby bol išlo o ovládací prvok **Mriežka so zadaniami času**. Pridajte ovládací prvok do zobrazenia a vyberte ho **Web**, **a** **Tablet**. Ďalej nakonfigurujte parametre pre **Týždenný vstup času** mriežka. Nastaviť **Dátum začiatku** pole do **msdyn\_ dátum**, nastaviť **Trvanie** pole do **msdyn\_ trvanie** a nastavte **Postavenie** pole do **msdyn\_ vstupný stav**. The **Zoznam stavov len na čítanie** pole je nastavené na **192350002 (Schválené)**, **(Odoslané)**, alebo **192350004 (vyžaduje sa stiahnutie)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Pridajte vlastné pole na príslušnú stránku úprav
Stránky, ktoré sa používajú na úpravu časových záznamov alebo riadkov časových záznamov, nájdete pod **Formuláre**. The **Upraviť záznam** tlačidlo v mriežke otvorí **Upraviť záznam** stránku a **Upraviť riadok** tlačidlo otvorí **Úprava riadkov** stránku. Tieto stránky môžete upraviť tak, aby obsahovali vlastné polia.

Obe možnosti odstraňujú niektoré filtrovanie pred spustením **Projekt** a **Projektová úloha** entity, aby boli viditeľné všetky pohľady na vyhľadávanie entít. Predpripravene sú viditeľné iba relevantné zobrazenia vyhľadávania.

Musíte určiť vhodnú stránku pre vlastné pole. S najväčšou pravdepodobnosťou, ak ste pridali pole do mriežky, malo by ísť na **Úprava riadkov** stránku, ktorá sa používa pre polia, ktoré sa vzťahujú na celý riadok časových záznamov. Ak má vlastné pole v riadku každý deň jedinečnú hodnotu (napríklad, ak ide o vlastné pole pre čas ukončenia), malo by ísť na **Úprava zadania času** stránku.

Ak chcete pridať vlastné pole na stránku, potiahnite a **Lúka** prvok na príslušné miesto na stránke a potom nastavte jeho vlastnosti.

### <a name="add-new-option-set-values"></a>Pridanie nových hodnôt množiny možností
Ak chcete pridať hodnoty množina možností do rozbaleného poľa, postupujte podľa týchto krokov.

1. Otvorte stránku úprav pre pole a potom pod **Typ**, vyberte **Upraviť** vedľa množina možností.
2. Pridajte novú možnosť, ktorá má vlastný štítok a farbu. Ak chcete pridať nový stav zadávania času, pole po rozbalení bude pomenované **Stav vstupu**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Označenie nového stavu položky času ako iba na čítanie
Ak chcete určiť stav nového zadania času iba na čítanie, pridajte novú hodnotu zadania času do vlastnosti **Zoznam stavov iba na čítanie**. Nezabudnite pridať číslo, nie štítok. Upraviteľná časť časovej mriežky bude teraz uzamknutá pre riadky, ktoré majú nový stav. Ak chcete nastaviť **Zoznam stavov len na čítanie** majetok inak pre rôzny **Vstup času** zobrazenia, pridajte **Zadanie času** mriežka v zobrazení **Vlastné ovládacie prvky** a nakonfigurujte parametre podľa potreby.

Ďalej pridajte obchodné pravidlá na uzamknutie všetkých polí na **Úprava riadkov** a **Úprava zadania času** stránky. Ak chcete získať prístup k obchodným pravidlám pre tieto stránky, otvorte editor formulárov pre každú stránku a potom vyberte **Obchodné pravidlá**. Nový stav môžete pridať k podmienke v existujúcich obchodných pravidlách, alebo môžete pridať nové obchodné pravidlo pre nový stav.

### <a name="add-custom-validation-rules"></a>Pridávanie vlastných overovacích pravidiel
Môžete pridať dva typy pravidiel overenia pre **Týždenný vstup času** skúsenosti s mriežkou:

- Obchodné pravidlá na strane klienta, ktoré fungujú na stránkach
- Overenia zásuvných modulov na strane servera, ktoré sa vzťahujú na všetky aktualizácie časových záznamov

#### <a name="client-side-business-rules"></a>Obchodné pravidlá na strane klienta
Použite obchodné pravidlá na uzamykanie a odomykanie polí, zadajte predvolené hodnoty do polí a definujte overenia, ktoré vyžadujú informácie len z aktuálneho záznamu o čase. Ak chcete získať prístup k obchodným pravidlám pre stránku, otvorte editor formulárov a potom vyberte **Obchodné pravidlá**. Potom môžete upraviť existujúce obchodné pravidlá alebo pridať nové obchodné pravidlo.

#### <a name="server-side-plug-in-validations"></a>Overenie zásuvných modulov na strane servera
Overenia doplnku by ste mali použiť pre všetky overenia, ktoré si vyžadujú viac kontextu, ako je k dispozícii v zázname jedného záznamu. Mali by ste ich použiť aj na akékoľvek overenia, ktoré chcete spustiť pri inline aktualizáciách v mriežke. Na dokončenie overení vytvorte vlastný doplnok na **Vstup času** subjekt.

### <a name="limits"></a>Limity
V súčasnosti je **Zadanie času** mriežka má limit veľkosti 500 riadkov. Ak existuje viac ako 500 riadkov, prebytočné riadky sa nezobrazia. Neexistuje spôsob, ako tento limit veľkosti zvýšiť.

### <a name="copying-time-entries"></a>Kopírovanie zadaní času
Pomocou zobrazenia **Kopírovať stĺpce zadaní času** definujte zoznam polí, ktoré sa majú kopírovať počas zadávania času. **Dátum** a **Trvanie** sú povinné polia a nemali by byť odstránené zo zobrazenia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
