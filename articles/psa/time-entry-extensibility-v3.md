---
title: Prispôsobenie týždenného vstupného času
description: Táto téma poskytuje informácie o tom, ako implementovať vlastné obchodné pravidlá, ktoré podporujú postupy organizácie.
author: stsporen
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cc395e77e987dac062251ef87fcf8295305178e2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084451"
---
# <a name="customize-weekly-time-entry"></a>Prispôsobenie týždenného vstupného času 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V Microsoft Dynamics 365 Project Service Automation verzia 3.3 Microsoft predstavil moderné mriežky, ktoré umožňujú projektovým prostriedkom rýchlo zadávať čas súčasne až do jedného týždňa. Nová mriežka týždenného časového vstupu môže zobraziť súčty pre položky podľa dátumu, riadka alebo týždňa. Zdroje môžu robiť kópie časových zápisov v rámci týždňa a tiež hromadne kopírovať z predchádzajúcich týždňov. Prispôsobovače systému môžu prispôsobiť zobrazenie pridaním polí, pridaním vyhľadávania do iných entít a implementáciou vlastných obchodných pravidiel na podporu postupov ich organizácie.

Čas vstupu a nové týždenné časovej mriežky sú prístupné prostredníctvom mapy lokality. Nerozšíriteľný zážitok z vlastného času vstupu, ktorý bol súčasťou predchádzajúcich verzií PSA, bol nahradený mriežkou rozšíriteľnej týždennej časovej položky a tiež alternatívnym zážitkom v mriežke a kalendári iba na čítanie. Z dôvodu tejto zmeny môžu používatelia zadávať čas v týždenných čiastkach.

## <a name="page-layout"></a>Rozloženie stránky
Nová mriežka týždenného časového vstupu je vlastný ovládací prvok, ktorý má panel s nástrojmi a dve hlavné **Časti** a **Trvanie**. Panel s nástrojmi obsahuje tlačidlo, ktoré sa vzťahuje len na tento vlastný ovládací prvok pre mriežku časovej položky. Naopak, tlačidlá na table akcií v hornej časti stránky sa vzťahujú na tri typy ovládacích prvkov, ktoré sú podporované pre zadávanie času: ovládací prvok týždenného vstupu, ovládací prvok iba na čítanie a ovládací prvok kalendár.

### <a name="dimensions"></a>Rozmery
Časti **Dimenzie** zobrazujú ako hlavičky stĺpca všetky dimenzie, proti ktorým možno zadávať čas. Nasledujúce dimenzie sú predpripravené:

- Projekt
- Projektová úloha
- Rola
- Typ
- Stav zadania

Sekcia **Dimenzia** neumožňuje riadkové úpravy. Táto časť je podporovaná zobrazením, ktoré umožňuje pridať vlastné polia do mriežky týždennej časovej položky. Informácie o pridávaní vlastných polí nájdete v časti „Rozšíriteľnosť” neskôr v tejto téme.

### <a name="duration"></a>Trvanie
V časti trvanie sa zobrazujú dni v týždni ako hlavičky stĺpcov. Táto časť umožňuje úpravy v riadku. Po vytvorení riadka časového vstupu, ktorý má príslušné dimenzie, môžu používatelia rýchlo zadávať, v riadku, množstvo času, ktoré strávili v týchto dimenziách.

## <a name="create-a-new-time-entry"></a>Vytvorenie nového časového záznamu
Ak chcete vytvoriť novú časovú položku v mriežke časového vstupu, vyberte položku **Nové**. Zobrazí sa dialógové okno **Rýchle vytvorenie zadania času**. V tomto dialógovom okne môžu používatelia vybrať dátum vstupu a potom zadať údaje pre dimenzie **Projekt** , **Projektová úloha** , **Rola** a **Trvanie** v minútach, hodinách alebo dňoch zadaním **h** , **m** alebo **d** spolu s číslom. Používatelia môžu tiež zadať popis a komentáre, ktoré môžu byť zdieľané externe pre čas vstupu. Keď používatelia uložia zmeny, hodnoty, ktoré zadali proti dimenziám, zobrazia sa v časti **Dimenzie**. Informácie o trvaní, ktoré zadali v **Trvanie** , sa zobrazia v dátum, pre ktorý bol vytvorený záznam času.

Vyhľadávacie polia sú podporované systémovými zobrazeniami. Ak napríklad používateľ prejde do projektu, pole **Projektová úloha** sa predvolene nastaví na zobrazenie **Kopírovať**. Ak chcete vytvoriť časové položky pre úlohy, ktoré nie sú priradené používateľovi, kliknite v dialógovom okne na možnosť **Zmeniť zobrazenie** na vyhľadávanie a stlačte možnosť **Všetky aktívne projektové úlohy**.

## <a name="edit-a-time-entry"></a>Úprava zadania času
Podrobnosti z niektorých polí na stránke časovej položky, ako napríklad **Popis** a **Externé poznámky** sa nezobrazujú v mriežke týždenného vstupu. Namiesto toho malý trojuholníkový indikátor sa objaví v bunkách trvania, ktoré majú tieto ďalšie podrobnosti. Vyberte bunku a potom stlačte možnosť **Upraviť podrobnosti** , ak chcete zobraziť údaje na table **Rýchle úpravy**. Ak chcú upraviť alebo aktualizovať Podrobnosti pre konkrétnu časovú položku, ktorá nie je súčasťou mriežky týždenných časových položiek, používatelia musia otvoriť tablu **Rýchle úpravy**.

## <a name="copy-a-time-entry-row"></a>Kopírovanie riadku zadania času
Po vytvorení prvého riadka vstupu môžu používatelia zvoliť možnosť **Kopírovať riadok** a skopírovať celý riadok do nového riadka. Po skopírovaní riadka týmto spôsobom sa skopírujú aj dimenzie a trvania. Používatelia môžu tiež vybrať možnosť **Upraviť riadok** a aktualizovať hodnoty dimenzie a trvania v riadku v sekcii **Trvanie**.

## <a name="open-a-time-entry"></a>Otvorenie časovej položky
Na podporu optimálneho a rýchleho zadávania v najvýraznejších poliach sa v mriežke týždenného vstupu zobrazí podmnožina vybratých dimenzií a časových trvaní. Ak chcete zobraziť všetky podrobnosti o jedinom časovom zápise, v časti **Upraviť zadanie** stlačte položku **Otvoriť**.

## <a name="submit-a-time-entry"></a>Odoslať zadanie času
Používatelia môžu odoslať jednorazovú položku alebo skupinu časových položiek výberom bloku buniek alebo celým časovým riadkom a následným výberom možnosti **Odoslať**. Odoslané časové položky sa zobrazia ako položky, ktoré čakajú na schválenie na stránke **Schválenie** schvaľovateľov. Po úspešnom odovzdaní záznamov ich nemožno upravovať.

## <a name="recall-a-time-entry"></a>Odvolať zadanie času
Môžete si pripomenúť položky, ktoré ste odoslali. Môžete si pripomenúť, jediný čas vstupu, blok času položky, alebo celý rad časových položiek. Pripomenuté časové zápisy sú k dispozícii pre zdroje na úpravu.

## <a name="time-entry-status"></a>Stav zadania času
Nové položky času sa automaticky priradia k stavu **Koncept**. Keď je odoslaná časová položka, stav sa aktualizuje na **Odoslané**. Keď je odoslaná časová položka schválená, stav sa aktualizuje na **Schválené**. Ak je položka času zamietnutá, stav sa aktualizuje na **Vrátené** a položka bude k dispozícii na opravu a opätovné odoslanie. Odstránia sa len časové položky, ktoré majú stav **Koncept**.

## <a name="view-rejection-comments"></a>Zobraziť komentáre k zamietnutiu
Ak schvaľovateľ zamietne časovú položku, môže pridať poznámky k zamietnutiu, ktoré pomôžu prostriedku pochopiť dôvod zamietnutia. Ak chcete zobraziť komentáre odmietnutia pre časovú položku, vyberte položku **Otvoriť položku**. Pripomienky k zamietnutiu sa zobrazia na časovej osi. Na časovej osi môže zdroj reagovať na komentáre zamietnutia skôr, než znova odošle položku.

## <a name="copy-week"></a>Kopírovať týždeň
Po vytvorení niekoľkých časových položiek môžu používatelia použiť možnosť **Kopírovať týždeň** na hromadné vytvorenie ďalších časových položiek. Otvorí sa dialógové okno **Kopírovať**. V časti **Obdobie od** použite polia **Počiatočný dátum** a **Koncový dátum** na definovanie rozsahu dátumov, z ktorého sa majú kopírovať časové položky. V časti **Obdobie do** v poli **Počiatočný dátum** zadajte dátum vytvorenia položiek času. Potom vyberte položku **Kopírovať**. Pre zadaný dátum v období „do” sa vytvorí kópia časových položiek pre zodpovedajúci deň v týždni v období „od”. Napríklad, pondelkový čas vstup z minulého týždňa bude skopírovaný do pondelka pre týždeň uvedený v období „do”.

## <a name="import"></a>Import
Rovnaký základný proces sa používa na import z rezervácií, úloh a výmen. Používatelia môžu určiť rozsah dátumov, z ktorých sa importujú rezervácie. Musia explicitne vybrať rezervácie, ktoré by mali byť skopírované do časových položiek konceptu. V predchádzajúcom vydaní navrhované časové údaje sa objavili v mriežke a v kalendári a boli stratené pri obnovení relácie.

## <a name="extensibility"></a>Rozšíriteľnosť
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Pridanie vlastných polí, ktoré majú dotazy na iné entity
Existujú tri hlavné kroky na pridanie vlastného poľa do mriežky týždenného vstupného času.

1.  Pridajte vlastné pole do dialógového okna rýchleho vytvorenia.
2.  Nakonfigurujte mriežku na zobrazenie vlastného poľa.
3.  Pridajte vlastné pole buď do riadka úpravy toku úloh alebo bunky úpravy toku úloh.

Musíte sa tiež uistiť, že nové pole má požadované overenia v riadku alebo bunke úpravy toku úloh. V rámci tohto kroku musíte zamknúť pole na základe stavu položky času.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Pridajte vlastné pole do dialógového okna rýchleho vytvorenia
Vlastné pole musíte pridať do dialógového Rýchle vytvorenie zadania času. aby používatelia mohli zadať hodnotu pre to, keď pridajú časové položky pomocou tlačidla **Nové**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Nakonfigurujte mriežku na zobrazenie vlastného poľa
Existujú dva spôsoby na pridanie vlastné pole do mriežky týždenný čas vstupu. Prvou možnosťou je prispôsobiť zobrazenie **Moje týždenné zadania času** a pridať do neho vlastné pole. Úpravou týchto vlastností v zobrazení môžete vybrať umiestnenie a veľkosť vlastného poľa v mriežke.

Druhou možnosťou je vytvoriť nové vlastné zobrazenie časového vstupu a nastaviť ho ako predvolené zobrazenie. Toto zobrazenie by malo obsahovať polia **Popis** a **Externé komentáre** okrem stĺpcov, ktoré chcete mať v mriežke. Úpravou týchto vlastností v zobrazení môžete vybrať umiestnenie, veľkosť a predvolené poradie zoradenia vlastného poľa v mriežke. Potom nakonfigurujte vlastný ovládací prvok pre toto zobrazenie, aby bol išlo o ovládací prvok **Mriežka so zadaniami času**. Pridajte tento ovládací prvok do zobrazenia a vyberte ho pre web, telefón a tablet. Potom nakonfigurujte parametre pre týždennú mriežku časového vstupu. Nastavte pole **Dátum začatia** na **msdyn_date** , nastavte pole **Trvanie** na **msdyn_duration** a nastavte pole **Stav** na **msdyn_entrystatus**. Pre predvolené zobrazenie je pole **Zoznam stavov iba na čítanie** nastavené na **192350002,192350003,192350004** , pole **Tok úloh úpravy riadkov** na hodnotu **msdyn_timeentryrowedit** a pole **Tok úloh úpravy buniek** nastavená na **msdyn_timeentryedit**. Tieto polia môžete prispôsobiť, ak chcete pridať alebo odstrániť stav iba na čítanie, alebo použiť inú pracovnú skúsenosť (TBX) na úpravu riadkov alebo buniek. Tieto polia by mali byť viazané na statickú hodnotu.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Pridanie vlastného poľa do príslušnej úpravy toku úloh
Stránky TBX, ktoré sa používajú na úpravu, nájdete v časti **Procesy**. Predvolenými stránkami sú **Project Service – úprava riadka so zadaním času** a **Project Service – úprava zadania času**. Môžete buď upraviť tieto predvolené stránky, alebo vytvoriť nové vlastné stránky TBX.

> [!NOTE] 
> Obe možnosti odstránia niektoré predpripravené filtrovanie v entitách **Projekt** a **Projektová úloha** , takže všetky zobrazenia vyhľadávania pre entity budú viditeľné. Predpripravene sú viditeľné iba relevantné zobrazenia vyhľadávania.

Musíte určiť príslušný tok úloh pre vlastné pole. S najväčšou pravdepodobnosťou, ak ste do mriežky pridali pole, mal by ísť v riadku upraviť tok úloh, ktorý sa používa pre polia, ktoré sa vzťahujú na celý riadok časových položiek. Ak vlastné pole má jedinečnú hodnotu každý deň, napríklad vlastné pole pre **Čas ukončenia** , mal by ísť v bunke upraviť tok úloh.

Ak chcete pridať vlastné pole do toku úloh, presuňte prvok **Pole** do príslušnej pozície na strane a potom nastavte jeho vlastnosti. Nastavte vlastnosť **Zdroj** na **Zadanie času** a nastavte vlastnosť poľa **Údajové pole** na vlastné pole. Vlastnosť **Pole** určuje zobrazovaný názov na stránke TBX. Stlačením možnosti **Použiť** uložte svoje zmeny do poľa. Potom stlačte možnosť **Aktualizovať** a uložte svoje zmeny stránky.

Ak chcete namiesto toho použiť novú vlastnú stránku TBX, vytvorte nový proces. Nastavte kategóriu na **Tok obchodného procesu** , nastavte entitu na **Zadanie času** a nastavte typ obchodného procesu na **Spustiť proces ako postup úloh**. V časti **Vlastnosti** sa vlastnosť **Názov stránky** musí nastaviť na zobrazovací názov pre stránku. Pridajte všetky príslušné polia na stránku TBX. Uložte a aktivujte proces a potom aktualizujte vlastnosť vlastného ovládacieho prvku pre príslušný tok úloh na hodnotu **Názov** v procese.

### <a name="add-new-option-set-values"></a>Pridanie nových hodnôt množiny možností
Ak chcete pridať hodnoty množiny možností do predpripraveného poľa, otvorte stránku úprav pre pole a potom v často **Typ** vyberte položku **Upraviť** vedľa množiny možností. Potom pridajte novú možnosť, ktorá má vlastný štítok a farbu. Ak chcete pridať nový stav položky času, predpripravené pole má názov **Stav zadania** , nie **Stav**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Označenie nového stavu položky času ako iba na čítanie
Ak chcete určiť stav nového časového vstupu iba na čítanie, pridajte novú hodnotu časového vstupu (číslo, nie štítok) do vlastnosti **Zoznam stavov iba na čítanie**. Upraviteľná časť mriežky časového vstupu bude zamknutá pre riadky, ktoré majú nový stav.
V ďalšom kroku pridajte obchodné pravidlá na uzamknutie všetkých polí na stránkach TBX **Úprava riadka so zadaním času** a **Úprava zadania času**. K obchodným pravidlám pre tieto stránky môžete pristupovať otvorením editora toku obchodného procesu pre stránku a následným výberom položky **Obchodné pravidlá**. Nový stav môžete pridať k podmienke v existujúcich obchodných pravidlách, alebo môžete pridať nové obchodné pravidlo pre nový stav.

### <a name="add-custom-validation-rules"></a>Pridávanie vlastných overovacích pravidiel
Existujú dva typy pravidiel overenia, ktoré môžete pridať pre týždenný čas vstupu mriežky skúsenosti: • Klientske obchodné pravidlá, ktoré pracujú v dialógových oknách rýchleho vytvorenia a na stránkach TBX • Overenia na strane servera, ktoré sa vzťahujú na všetky aktualizácie časových položiek

#### <a name="business-rules"></a>Obchodné pravidlá
Použite obchodné pravidlá na uzamykanie a odomykanie polí, zadajte predvolené hodnoty do polí a definujte overenia, ktoré vyžadujú informácie len z aktuálneho záznamu o čase. K obchodným pravidlám pre stránku TBX môžete pristupovať otvorením editora toku obchodného procesu pre stránku a následným výberom položky **Obchodné pravidlá**. Potom môžete upraviť existujúce obchodné pravidlá alebo pridať nové obchodné pravidlo. Pre ešte viac prispôsobené overenia, môžete použiť obchodné pravidlo na spustenie JavaScript.

#### <a name="plug-in-validations"></a>Overovanie doplnkov
Overenia doplnku by ste mali použiť pre akékoľvek overenia vyžadujúce si viac kontextu než je dostupný v samostatnom zázname zadania času alebo pri akýchkoľvek overeniach, ktoré chcete spúšťať na riadkových aktualizáciách v mriežke. Ak chcete dokončiť overenie, vytvorte vlastný doplnok v entite **Zadanie času**.

> [!IMPORTANT] 
> V súčasnosti známy problém na stránkach TBX zabraňuje používateľom opraviť informácie a opätovné voľby vykonať, keď zlyhá overovanie doplnku. Ako riešenie nastavte overovanie obchodného pravidla na čo najväčšie zabránenie tejto situácii.
