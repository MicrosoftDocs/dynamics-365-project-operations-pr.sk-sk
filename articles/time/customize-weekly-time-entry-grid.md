---
title: Rozšírenie zadaní času
description: Táto téma poskytuje informácie o tom, ako môžu vývojári rozšíriť riadenie zadaní času.
author: stsporen
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d9c14f0550d4429ac794607a3fb61717566207e4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124657"
---
# <a name="extending-time-entries"></a>Rozšírenie zadaní času

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations obsahuje rozšíriteľné vlastné riadenie zadaní času. Toto riadenie obsahuje nasledujúce funkcie:

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
Každé zadanie času je spojené so záznamom zdroja času. Tento záznam určuje, ako a ktoré aplikácie majú spracovať zadanie času.

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

1. Pridajte vlastné pole do dialógového okna rýchleho vytvorenia.
2. Nakonfigurujte mriežku na zobrazenie vlastného poľa.
3. Pridanie vlastného poľa do riadka úpravy toku úloh alebo bunky úpravy toku úloh.

Uistite sa, že nové pole má požadované overenia v riadku alebo bunke úpravy toku úloh. V rámci tohto kroku zamknite pole na základe stavu zadania času.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Pridajte vlastné pole do dialógového okna rýchleho vytvorenia
Vlastné pole pridajte do dialógového okna **Rýchle vytvorenie zadania času**. Potom, keď sa pridajú zadania času, je možné zadať hodnotu výberom možnosti **Nová**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Nakonfigurujte mriežku na zobrazenie vlastného poľa
Existujú dva spôsoby na pridanie vlastného poľa do mriežky týždenného zadania času:

  - Prispôsobenie zobrazenia a pridávanie vlastného poľa
  - Vytvorenie nového predvoleného vlastného zadania času 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Prispôsobenie zobrazenia a pridávanie vlastného poľa

Prispôsobte zobrazenie **Moje týždenné zadania času** a pridajte do neho vlastné pole. Úpravou vlastností v zobrazení môžete vybrať umiestnenie a veľkosť vlastného poľa v mriežke.

#### <a name="create-a-new-default-custom-time-entry"></a>Vytvorenie nového predvoleného vlastného zadania času

Toto zobrazenie by malo obsahovať polia **Popis** a **Externé komentáre** okrem stĺpcov, ktoré chcete mať v mriežke. 

1. Úpravou týchto vlastností v zobrazení vyberte umiestnenie, veľkosť a predvolené poradie zoradenia vlastného poľa v mriežke. 
2. Nakonfigurujte vlastný ovládací prvok pre toto zobrazenie, aby bol ovládacím prvkom **Mriežka so zadaniami času**. 
3. Pridajte tento ovládací prvok do zobrazenia a vyberte ho pre web, telefón a tablet. 
4. Nakonfigurujte parametre pre týždennú mriežku zadania času. 
5. Nastavte pole **Dátum začatia** na **msdyn_date**, nastavte pole **Trvanie** na **msdyn_duration** a nastavte pole **Stav** na **msdyn_entrystatus**. 
6. Pre predvolené zobrazenie je pole **Zoznam stavov iba na čítanie** nastavené na **192350002,192350003,192350004**. Pole **Tok úloh úpravy riadkov** je nastavené na **msdyn_timeentryrowedit**. Pole **Tok úloh úpravy buniek** je nastavené na **msdyn_timeentryedit**. 
7. Tieto polia môžete prispôsobiť, ak chcete pridať alebo odstrániť stav iba na čítanie, alebo použiť inú pracovnú skúsenosť (TBX) na úpravu riadkov alebo buniek. Tieto polia sú teraz viazané na statickú hodnotu.


> [!NOTE] 
> Obe možnosti odstránia niektoré predpripravené filtrovanie v entitách **Projekt** a **Projektová úloha**, takže všetky zobrazenia vyhľadávania pre entity budú viditeľné. Predpripravene sú viditeľné iba relevantné zobrazenia vyhľadávania.

Určite príslušný tok úloh pre vlastné pole. Ak ste do mriežky pridali pole, mal by ísť v riadku upraviť tok úloh, ktorý sa používa pre polia, ktoré sa vzťahujú na celý riadok časových položiek. Ak vlastné pole má jedinečnú hodnotu každý deň, napríklad vlastné pole pre **Čas ukončenia**, mal by ísť v bunke upraviť tok úloh.

Ak chcete pridať vlastné pole do toku úloh, presuňte prvok **Pole** do príslušnej pozície na strane a potom nastavte vlastnosti poľa. Nastavte vlastnosť **Zdroj** na **Zadanie času** a nastavte vlastnosť poľa **Údajové pole** na vlastné pole. Vlastnosť **Pole** určuje zobrazovaný názov na stránke TBX. Vyberte možnosť **Použiť** na uloženie zmien do poľa a potom vyberte **Aktualizovať** na uloženie zmien na stránku.

Ak chcete namiesto toho použiť novú vlastnú stránku TBX, vytvorte nový proces. Nastavte kategóriu na **Tok obchodného procesu**, nastavte entitu na **Zadanie času** a nastavte typ obchodného procesu na **Spustiť proces ako postup úloh**. V časti **Vlastnosti** sa vlastnosť **Názov stránky** musí nastaviť na zobrazovací názov pre stránku. Pridajte všetky príslušné polia na stránku TBX. Uloženie a aktivovanie procesu. Aktualizujte vlastnosť vlastného ovládacieho prvku pre príslušný tok úloh na hodnotu **Názov** v procese.

### <a name="add-new-option-set-values"></a>Pridanie nových hodnôt množiny možností
Ak chcete pridať hodnoty množiny možností do predpripraveného poľa, otvorte stránku úprav pre pole a v časti **Typ** vyberte položku **Upraviť** vedľa množiny možností. Pridajte novú možnosť, ktorá má vlastný štítok a farbu. Ak chcete pridať nový stav položky času, predpripravené pole má názov **Stav zadania**, nie **Stav**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Označenie nového stavu položky času ako iba na čítanie
Ak chcete určiť stav nového zadania času iba na čítanie, pridajte novú hodnotu zadania času do vlastnosti **Zoznam stavov iba na čítanie**. Upraviteľná časť mriežky časového vstupu bude zamknutá pre riadky, ktoré majú nový stav.
V ďalšom kroku pridajte obchodné pravidlá na uzamknutie všetkých polí na stránkach TBX **Úprava riadka so zadaním času** a **Úprava zadania času**. K obchodným pravidlám pre tieto stránky môžete pristupovať otvorením editora toku obchodného procesu pre stránku a následným výberom položky **Obchodné pravidlá**. Nový stav môžete pridať k podmienke v existujúcich obchodných pravidlách, alebo môžete pridať nové obchodné pravidlo pre nový stav.

### <a name="add-custom-validation-rules"></a>Pridávanie vlastných overovacích pravidiel
Existujú dva typy overovacích pravidiel, ktoré môžete pridať pre skúsenosti s týždennou mriežkou zadávania času:

- Obchodné pravidlá na strane klienta, ktoré fungujú v rýchlych dialógových oknách na vytváranie a na stránkach TBX.
- Overenie doplnku na strane servera, ktoré sa vzťahuje na všetky aktualizácie zadávania času.

#### <a name="business-rules"></a>Podnikové pravidlá
Použite obchodné pravidlá na uzamykanie a odomykanie polí, zadajte predvolené hodnoty do polí a definujte overenia, ktoré vyžadujú informácie len z aktuálneho záznamu o čase. K obchodným pravidlám pre stránku TBX môžete pristupovať otvorením editora toku obchodného procesu pre stránku a následným výberom položky **Obchodné pravidlá**. Potom môžete upraviť existujúce obchodné pravidlá alebo pridať nové obchodné pravidlo. Pre ešte viac prispôsobené overenia, môžete použiť obchodné pravidlo na spustenie JavaScript.

#### <a name="plug-in-validations"></a>Overovanie doplnkov
Overenia doplnku použite pre akékoľvek overenia vyžadujúce si viac kontextu než je dostupný v samostatnom zázname zadania času alebo pri akýchkoľvek overeniach, ktoré chcete spúšťať na riadkových aktualizáciách v mriežke. Ak chcete dokončiť overenie, vytvorte vlastný doplnok v entite **Zadanie času**.

### <a name="copying-time-entries"></a>Kopírovanie zadaní času
Pomocou zobrazenia **Kopírovať stĺpce zadaní času** definujte zoznam polí, ktoré sa majú kopírovať počas zadávania času. **Dátum** a **Trvanie** sú povinné polia a nemali by byť odstránené zo zobrazenia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]