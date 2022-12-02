---
title: Čo je nové alebo zmenené v Project Service Automation verzia 3
description: Tento článok poskytuje informácie o tom, čo je nové a zmenené v Project Service Automation verzia 3.
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8d076e270f426131119eab097e7f359c228edb51
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926611"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Čo je nové alebo zmenené v Project Service Automation verzia 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]



Tento článok poskytuje informácie o zmenách používateľského rozhrania (UI), funkčnosti a terminológii v Project Service Automation medzi verziou 2 alebo verziou 1 a verziou 3.

## <a name="project-scheduling"></a>Plánovanie projektov
Plán projektu, ktorý bol známy ako štruktúra rozdelenia práce (WBS) v predchádzajúcich verziách, bol premenovaný na program a je prístupný kliknutím na kartu **Plán**. 

![Plánovanie projektov.](media/psa-schedule-01.png)

Rozvrh má teraz nový rozhranie pre interakciu, ktoré je moderné aj prístupné. Základný plánovací modul Project Service Automation sa však nezmenil. Ovládacie tlačidlá v páse s nástrojmi mriežky plánovania umožňujú interakciu s plánom podobným predchádzajúcej verzii Project Service Automation. Medzi ďalšie zmeny v pláne patria:

- **Ganttov graf** – Ganttov graf už nie je prítomný. Nová vizualizácia gannta sa vráti v budúcej aktualizácii.
- **Hlavičky stĺpcov** – môžete skryť hlavičky stĺpcov v mriežke kliknutím na indikátor nadol vedľa názvu stĺpca. 
- **Stĺpce** – kliknutím na tlačidlo **Pridať stĺpec** môžete zobraziť skryté stĺpce. 
- **Kategória transakcie** – Vyhľadávanie **kategórie transakcie** bolo pridané do mriežky plánu a predvolene sa zobrazuje. 
 
## <a name="project-templates"></a>Projektové šablóny
Pri funkčnosti šablóny projektu boli vykonané nasledujúce zmeny.

### <a name="create-a-project-template"></a>Vytvoriť šablónu projektu 
Šablónu projektu môžete vytvoriť vo verzii 3, ktorá je podobná predchádzajúcim verziám Project Service Automation. Šablóna môže obsahovať iba plán a plán môže obsahovať nasadenia, ale nie sú potrebné. Ak plán má úlohy, môžu byť len pre všeobecné zdroje. Môžete generovať požiadavky na zdroje pre všeobecné zdroje, ale nemôžu byť rezervované so skutočnými zdrojmi v šablóne. Nemôžete rezervovať skutočný zdroj tímu v šablóne. 

### <a name="create-a-template-from-an-existing-template"></a>Vytvorenie novej šablóny z existujúcej šablóny
Keď vytvoríte novú šablónu projektu z existujúcej šablóny v Project Service Automation verzia 3, nastane nasledovné: 

- Plán zdrojového projektu sa skopíruje do šablóny. 
- Všeobecné prostriedky sa skopírujú do tímu a všetky všeobecné priradenia prostriedkov sa skopírujú. Požiadavky na všeobecné zdroje sa neskopírujú. 

### <a name="create-a-template-from-an-existing-project"></a>Vytvorenie novej šablóny z existujúceho projektu
Keď vytvoríte novú šablónu projektu z existujúcej existujúceho projektu, nastane nasledovné: 

- Plán zdrojového projektu sa skopíruje do šablóny. 
- Všeobecné prostriedky sa skopírujú do tímu a všetky všeobecné priradenia prostriedkov sa zachovajú. Požiadavky na všeobecné zdroje sa neskopírujú.    
- Pomenované prostriedky, priradené alebo nepriradené, sa z tímu odstránia a nahradia sa všeobecnými zdrojmi.
- V prípade prítomnosti sa informácie odstránia. 
- Ak je prítomný, odkazy na citácie a zmluvy sú odstránené. 

### <a name="create-a-project-from-a-template"></a>Vytvorenie projektu zo šablóny
Keď vytvoríte nový projekt zo šablóny v Project Service Automation verzia 3, nastane nasledovné:

- Plán, tím a priradenia sa skopírujú do nového projektu.   
- Počiatočný dátum je buď kópia dátumu, alebo dátumu vybratý používateľom.   
- Pre všetkých všeobecných členov tímu s požiadavkami na zdroje v šablóne, požiadavky nie sú skopírované ani generované automaticky. Budete ich musieť generovať. 

## <a name="copy-a-project"></a>Kopírovať projekt
Keď skopírujete projekt v Project Service Automation verzia 3, nastane nasledovné: 

- Odhadovaný počiatočný dátum sa skopíruje, ale môže sa zmeniť.  
- Plán projektu a úlohy sa skopírujú. 
- Všeobecné zdroje a ich priradenia sa skopírujú. Požiadavky na zdroje pre všeobecné zdroje sa neskopírujú. Budete ich musieť znova generovať. 
- Skutočné zdroje a ich priradenia sa neskopírujú. Namiesto toho sa nahrádzajú všeobecnými zdrojmi. 
- Skutočné hodnoty sa neskopírujú do nového projektu. 

## <a name="move-a-scheduled-project"></a>Premiestnenie plánovaného projektu
Keď presuniete plán existujúceho projektu dopredu, stane sa toto: 

- Dátumy úloh sa automaticky premiestnia tak, aby zodpovedali obdobiu presunu. 
- Priradené všeobecné prostriedky zostávajú priradené.   
- Ak sa vygenerujú ešte pred presunutím projektu, požiadavky na všeobecný prostriedok zostávajú rovnaké a nie sú automaticky znovu generované. Budete ich musieť generovať znova, aby odrážali nové úlohy v dôsledku presunutia úlohy. 
- Priradenie skutočných zdrojov sa zmení tak, aby zodpovedalo presunu dátumu úlohy. Rezervácie na reálne zdroje sa nemenia. Rezerváciu budete musieť upraviť pomocou zobrazenia odsúhlasenia. 
- Tímové zdroje s rezerváciami, ale žiadne úlohy sa nezmenili. 
- Skutočné hodnoty sa nepresúvajú. 

## <a name="estimates"></a>Odhady
Odhady boli rozdelené na dve karty **Priradenie zdroja** a **Odhady**. Karta **Priradenie zdroja** obsahuje odhady intenzity a zobrazuje priradenia prostriedkov pre úlohy v zobrazení s časovým rozvrhnutom. Odhady môžete upraviť na základe toho, čo bolo vytvorené plánovacím systémom.

![Karta Priradenie zdroja zobrazuje odhady intenzity a priradenia zdrojov pre úlohy.](media/resource-assignments-tab-02.png)

Na karte **Odhady** sa zobrazujú čiastky nákladov a predaja pre priradenia prostriedkov. Čiastky sú iba na čítanie. Náklady a predajné ceny sú teraz riadené od členov tímu úlohy v rozvrhu. To znamená, že ak máte úlohu bez priradenia, úloha sa zobrazí pod nepriradený kontajner. To tiež znamená, že bez **roly**, čo je predvolený cenový rozmer, tam nebudú žiadne odhadované náklady alebo predaje, ak máte zákazníka alebo zmluvu/cenovú ponuku spojenú s projektom. 

![Karta Odhady zobrazujúca čiastky nákladov a predaja.](media/estimates-tab-03.png)
  
Kategória je podporovaná aj na úlohách v zobrazení plánu. Zoskupenie podľa kategórie na časovo fázovom zobrazení odhadov poskytne lepšie skúsenosti, najmä ak máte v projekte aj odhady výdavkov. Odhady výdavkov sa zadajú pomocou mriežky na samostatnej karte. 

Odhady výdavkov možno zadať v mriežke na karte **Odhady nákladov**. 

![Karta Odhady výdavkov zobrazuje mriežku s odhadmi výdavkov.](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Správa zdrojov
V Project Service Automation verzia 3, s novým používateľským rozhraním zjednoteného klienta a zmenami vo vzťahu medzi rezerváciami a priradeniami, sa dramaticky zmenilo personálne obsadenie projektu generickými alebo reálnymi zdrojmi medzi verziou 2 a 1. Avšak, pojmy rezervovateľné zdroje, a to ako **skutočné** a **generické** zostávajú rovnaké, rovnako ako členovia tímu, požiadavky, úlohy a rezervácie.   

![Používanie výberu zdroja.](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Priradenie skutočného rezervovateľného prostriedku 
V Project Service Automation verzie 3, rezervácie a priradenie úloh nie sú tak úzko prepojené ako v predchádzajúcich verziách Project Service Automation. Môžete použiť mriežku tímu na rezerváciu **skutočného** člena tímu, podobne ako v trhu.

Pomocou výberu zdrojov v pláne môžete vybrať člena tímu vytvoreného v zobrazení tímu a potom ich priradiť k úlohám. Môžete im aj naďalej priraďovať úlohy, dokonca aj po ich rezervácii. Na odsúhlasenie členov tímu, ktorí majú rozdiely v rezerváciách a úlohách, použite kartu **Vyrovnanie**.

Výber prostriedkov zobrazí členov tímu projektu. Môžete tiež použiť výber zdrojov na vyhľadanie vybraných rezervovateľných zdrojov, ktoré nie súčasťou projektového tímu. Môžete ich priradiť k úlohe a stanú sa súčasťou projektového tímu. Budete ich musieť rezervovať použitím karty **Tabula plánovania** alebo **Vyrovnanie**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Priraďte všeobecný rezervovateľný prostriedok k úlohe a projektovým tímom a potom splníme skutočným zdrojom prostredníctvom tabule plánovania 
V Project Service Automation verzie 3, funkcia generovania tímov nie je použitá pre všeobecné zdroje. Namiesto toho môžete vytvoriť a priamo priradiť všeobecný prostriedok z plánu zadaním názvu pozície všeobecného prostriedku v bunke zdroja plánu. Alebo kliknite na ikonu zdroj v bunke k otvoreniu výberu zdrojov a potom zadajte názov všeobecného prostriedku, ktorý chcete vytvoriť. Otvorí sa panel rýchleho vytvorenia, ktorý vám umožní nastaviť rolu a organizačnú jednotku člena tímu generických zdrojov. Po vytvorení prostriedku je priradený k úlohe a môžete aj naďalej priraďovať tento všeobecný prostriedok k iným úlohám v pláne.    
 
Ak ste zdroj priradili k všetkým príslušným úlohám, môžete vygenerovať požiadavku na zdroje a potom ju naplniť priamo rezerváciou s **Tabulou plánovania** alebo odoslaním žiadosti o prostriedky. Všeobecné zdroje môžete pridať aj priamo do mriežky člena tímu. 

Všeobecné zdroje sa pridajú do projektového tímu bez požiadaviek na zdroje a dátumov začiatku a ukončenia projektu, kým sa negeneruje požiadavka na zdroj. Ak chcete vygenerovať požiadavku, vyberte všeobecný zdroj a kliknite na **Generovať**. Požiadavka odkaz teraz zobrazí a požadované hodiny budú vyplnené s pridelenými hodinami. Môžete kliknúť na odkaz a otvoriť a aktualizovať požiadavku.
  
Keď je rezervácia úplná a úplne splnená pomenovaným prostriedkom, všeobecný prostriedok sa nahradí názvom prostriedku a priradenie v pláne sa aktualizuje s názvom prostriedku. 

Navrhované zdroje pre požiadavky sú teraz uložené na karte namiesto samostatnej sekcie.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Viaceré pomenované zdroje plniace generický zdroj
Ak je splnená požiadavka s viacerými zdrojmi, všeobecný prostriedok zostáva v tíme a priradí sa k úlohe. Pomenovaní členovia tímu, ktorí sú rezervovaní, nebudú priradení ako súčasť pozície. Projektový manažér môže priradiť prácu podľa zodpovedajúcich skutočných prostriedkov.  Zobrazenie **Vyrovnanie** ponúka rozpis rezervácií naprieč viacerými zdrojmi priradenia úlohy. To sa nerobí automaticky, pretože v komplikovanejších scenároch, ako je ten, kde máte zväzok úloh vytvárajúcich požiadavku, kde je úmyslom projektového manažéra priradenie, je potrebné predpokladať. Vzhľadom k tomu, že systém nemôže pochopiť zámer, je pravdepodobné, že predpoklady budú iné, než je určené, a stane sa nesprávny alebo nepredvídateľný výsledok. Predvídateľný výsledok je, že všeobecný zdroj zostáva priradený, kým projektový manažér zámerne vytvorí úlohy priraďujúce zdroje pomocou zobrazenia **Vyrovnanie**.

### <a name="reconciliation"></a>Vyrovnanie
Záložka **Vyrovnanie** zobrazuje rezervácie a všetky priradenia pre každého člena projektového tímu. Zobrazenie zobrazuje hodiny v bunkách, ktoré môžu reprezentovať časové body od mesiacov do dní. Zobrazenie umožňuje projektovým správcom porovnať rezervácie členov tímu a ich priradenia pre ich projektový tím. Je to užitočné, pretože rezervácie a úlohy nie sú tesne spojené, čo umožňuje väčšiu flexibilitu pri plánovaní projektu. 

![Záložka Vyrovnanie zobrazuje rezervácie a všetky priradenia pre členov projektového tímu.](media/resource-reconciliation-tab-06.png)

Pre každý prostriedok, zobrazenie má rozdiel medzi členom tímu rezervácie a súhrn ich úlohy priradenia a ukazuje nasledujúce dve rozdiely, ktoré môžu nastať s rezervácie a nasadenia v projekte: 

- **Nedostatok rezervácií** – Nedostatky rezervácie sa objavia, keď má zdroj viac priradení než rezervácie. Keďže táto kapacita nebola vyhradená, projektový manažér ho môže napraviť rozšírením rezervácií prostriedkov na krytie deficitu. 
- **Rozšírené rezervácie** – Nadmerná rezervácia nastane, keď sa zdroj zarezervuje do projektu, no nebude priradený k úlohám.  Môže to byť prijateľný výskyt, napríklad ak bol zdroj rezervovaný pred priradením úlohy. Avšak v iných prípadoch, zdroj nie je možné naplánovať, ktoré majú byť pridelené, a PM by mali zvážiť zrušenie rezervácie zdrojov, aby umožnili kapacitu použiť pre iný projekt. 

Ak máte priradenia úloh pre prostriedok bez rezervácií (nedostatok rezervácie), môžete vybrať súhrnný nedostatok rezervácií a kliknúť na položku **Rozšíriť rezerváciu**. Odtiaľ si môžete prezrieť rezerváciu, ktorá je potrebná na riešenie nedostatku zdrojov a ich dostupnosti. 
 
## <a name="time-and-expense"></a>Čas a výdavky
Táto časť obsahuje informácie o zmenách času, výdavkov a schvaľovania vo verzii 3 Project Service Automation. Ako súčasť Dynamics 365 Project Service Automation riešenia sa obnovila funkcia **Zadanie času** na využívanie rámci zjednoteného rozhrania. To umožňuje doručenie konzistentného, jednotného používateľského rozhrania, ktoré nasleduje responzívny dizajn pre optimálne prezeranie na ľubovoľnej veľkosti obrazovky alebo zariadení. 

### <a name="landing-page"></a>Vstupná stránka
Nerozšíriteľné vlastné časy boli vo verzii 3 zastarané. Namiesto toho je teraz rozšíriteľná a prístupná natívna mriežka skúsenosti. Môžete pristupovať k funkcii časového vstupu pomocou mapy lokality na ľavej strane. S touto zmenou už nebudete môcť zadávať čas na jeden týždeň súčasne. Namiesto toho budete musieť vytvoriť časový záznam pre každý deň v mriežke. Po niekoľkých vytvorených časových položkách môžu používatelia hromadne vytvárať časové položky s funkciou **Kopírovanie**, ktorá je vysvetlená ďalej v tomto článku. 

![Vstupná stránka zadávania času.](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Vytvorenie nových položiek času 
Kliknite tlačidlo **Nové** v páse s nástrojmi rýchleho vytvorenia stránky pre čas vstupu, kde zadáte trvanie v minútach, hodinách alebo dňoch. Ak to chcete urobiť, stačí začať písať h, m, alebo d spolu s množstvom.  

![Rýchle vytvorenie zadania času.](media/quick-create-time-entry-08.png)

Vyhľadávacie polia sú podporované systémovými zobrazeniami. Ak napríklad zadáte informácie o projekte, pole **Projektová úloha** sa automaticky nastaví na zobrazenie **Moje otvorené projektové úlohy**. Ak chcete vytvoriť časové položky pre úlohy, ktoré nie sú priradené používateľovi, kliknite na možnosť **Zmeniť zobrazenie** na vyhľadávanie a stlačte možnosť **Všetky aktívne projektové úlohy**. Po vytvorení a predstavení času v mriežke môžete upraviť ľubovoľné hodnoty riadkov priamo v mriežke.  

### <a name="bulk-createcopy"></a>Hromadné vytvorenie/kopírovanie 
Po vytvorení niekoľkých časových položiek môžete použiť funkciu kopírovania na hromadné vytvorenie dodatočných časových položiek. Kliknutím na možnosť **Skopírovať** otvorte dialógové okno **Kopírovať**. V časti **Obdobie od: Počiatočný dátum** nastavte rozsah dátumov, od ktorých sa musia kopírovať časové obdobia. V časti **Obdobie do: Počiatočný dátum** zadajte dátum, pre ktorý sa musia vytvoriť položky času. Kliknutím položku **Kopírovať** skopírujete položky času do zodpovedajúceho dňa v týždni, ktorý je uvedený v časti **Obdobie do**. Napríklad, pondelkový čas vstup z minulého týždňa bude skopírovaný do pondelka pre týždeň uvedený v **Obdobie Do**. 

![Skopírovať hromadné časové záznamy.](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importovať údaje 
Úlohy a výmeny sa riadia rovnakým vzorom používateľského rozhrania, ktoré umožňujú používateľovi určiť rozsah dátumov, kedy je potrebné importovať rezervácie. Potom musíte explicitne vybrať rezervácie, ktoré by mali byť skopírované do časových položiek **Koncept**. Vo verzii 3 už viac nemôžete vidieť **Navrhované** časové záznamy na mriežke a v kalendári.  

### <a name="change-in-calendar-control"></a>Zmena v ovládacom prvku kalendára
Vo verzii 3 sme sa vzdialili od vlastného ovládacieho prvku kalendára a teraz používate kalendár UC na zobrazenie položiek času v týždni. Pomocou tohto kalendára môžete zobraziť deň, týždeň a mesiac. 

> [!NOTE]
> Obmedzenie v kalendári je, že tento ovládací prvok nepodporuje akcie na jednotlivé položky kalendára. Nebudete môcť napríklad vybrať jeden alebo viac položiek kalendára a odoslať alebo odstrániť tieto položky. Kliknutím na položku kalendára sa otvorí stránka entity **Entita zadania času** pre ďalšie akcie. 

### <a name="extensibility"></a>Rozšíriteľnosť
**Zachytiť len údaje o vlastných poliach entitách záznamu času a nákladov** – Položka času využíva upraviteľnú mriežku, mriežku iba na čítanie a ovládacie prvky kalendára z platformy. Všetky tieto ovládacie prvky sú natívne, a preto budú podporovať prispôsobenia. V Project Service Automation verzie 3 môžete pridať ďalšie vlastné polia, nastaviť vyhľadávacie polia a zálohovať ich vlastnými pohľadmi. Vlastnú obchodnú logiku môžete nastaviť aj na základe vybratých hodnôt vo vlastných poliach.  

**Zachytiť údaje o vlastných poliach v čase a výdavky položky a propagovať ho prostredníctvom subjektov podporujúcich odoslania a schvaľovania** – Typické spracovanie časových záznamov sa zobrazuje v nasledovnom diagrame.

![Proces postupu zadania času.](media/process-time-entries-10.png)

Ak obchodné požiadavky stanovujú, že čas a náklady entity musia zachytiť vlastné cenové dimenzie a množiť hodnoty, ktoré sú nastavené čas a vstupný prostriedok vo vlastnej cenovej dimenzie prostredníctvom všetkých entít v predchádzajúcom obrázku, pozri [Nastavenie vlastných polí ako dimenzií cien](set-up-pricing-dimensions.md)

Na podporu obchodných požiadaviek, kde musia subjekty času a výdavkov zachytiť vlastné dimenzie neurčovania cien a propagovať hodnoty, môžete použiť nastavenie dimenzií cien a vyjadriť vlastné dimenzie ako dimenzie cien bez poplatkov alebo fakturačného kurzu. Ďalším scenárom by bolo pridanie vlastného poľa do každej entity pomocou rovnakého názvu poľa vo všetkých entitách. Vlastné doplnky môžu byť vytvorené tak, aby sa týkali záznamov v entitách, ktoré sa podieľajú na toku odosielania/schvaľovania pomocou transakcií pôvodu a transakcií pripojenia entity.  

### <a name="delegate-time-and-expense-entry"></a>Delegovanie času a vstupných nákladov
Platforma Common Data Service nepodporuje jedného používateľa napodobňujúceho iného, čo znamená vo verzii 3 Project Service Automation, že nie je žiadna podpora pre delegovaný čas a výdavky vstupu. Avšak, partneri a zákazníci využili riešenie na umožnenie podpory pre delegované zadávanie času vo verzii 3. Ide iba o vyriešenie problému, a nie kompletné riešenie, takže je dôležité pochopiť obmedzenia a používať tento prístup len v prípade, že obmedzenia sú prijateľné. 

> [!IMPORTANT]
> Tieto informácie by sa mali považovať za navrhované usmernenie pre vlastnú implementáciu partnera/zákazníka. Produktový tím neponúka formálnu podporu tejto funkcie prostredníctvom niektorého z našich podporných kanálov.

### <a name="customization-details"></a>Podrobnosti prispôsobenia 
Prispôsobenia umožňujú pridať **Rezervovateľný zdroj** na vytvorenie a úpravu skúseností úpravy, ktoré používateľovi umožňujú konať ako delegát zmenou poľa **Rezervovateľný zdroj** inému používateľovi, ktorého záznamy času a výdavkov je potrebné zaznamenať. Nasledujúce kroky pokrývajú delegáciu zadania času. Rovnaké informácie sa vzťahujú na delegovanie vstupných výdavkov. 
 
1.  Zabezpečiť, aby delegovaný používateľ mal globálny bezpečnostný prístup k projektom a projektovým úlohám. 
1.  Keďže **Rezervovateľný zdroj**, ktorý je poľom v entite **Zadanie času**, nie je vystavený na stránke **Rýchle vytvorenie**, musíte ho pridať.

    -alebo-

    Vytvorenie vlastného zobrazenia, ktoré obsahuje stĺpec **Rezervovateľný zdroj**, na zobrazenie iba položiek času vytvorených pre zdroj. Publikujte prispôsobenia v návrhárovi aplikácie modulu pre toto zobrazenie na zobrazenie v časti **Výber zobrazenia** na stránke **Zadania času**. Existujú dva doplnky, ktoré spracúvajú nastavenie pre manažéra neprojektových časových položiek:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Vytvorte nový doplnok na prepísanie poľa **Manažér** manažéra používateľa priradeného v poli **Rezervovateľný zdroj**. Použite rovnakú **Etapu vykonávania** ako je out-of-band (OOB) doplnok (predbežné overenie) a použite **Príkaz na vykonanie**, ktorý je vyššie než doplnky OOB (väčšie ako 1). Tým sa zabezpečí, že vlastný doplnok sa vykoná až po doplnkoch OOB.  
 
### <a name="end-user-experience"></a>Skúsenosť koncového používateľa
1.  Keď vytvoríte časovú položku na stránke rýchleho vytvorenia, zadajte podrobnosti projektu a projektu a potom vyberte používateľa v poli **Rezervovateľné zdroje**, pre ktoré je potrebné zaznamenať časové údaje. 
2.  V predvolenom nastavení toto pole predvolené prihláseného používateľa, avšak vzhľadom na to, že používateľ prepísal toto poľa, čas položka je teraz vytvorená pre vybraný **Rezervovateľný zdroj**.
3.  Keď odošlete položky času, ktoré ste vytvorili pre tieto záznamy, položky budú zaradené do frontu pre schvaľovateľa projektu podľa očakávania. 
4.  Keď si spomínate časové položky vytvorené pre iného používateľa, položky času sa vrátia do stavu **Koncept** s poľom **Rezervovateľný zdroj** nastaveným inému používateľovi. 
5.  Voliteľne môžete prepnúť na vlastné zobrazenie a filtrovať položky času vytvorené pre iného používateľa. 
 
### <a name="limitations"></a>Obmedzenia
Funkcie **Kopírovať** a **Import** fungujú len v kontexte prihláseného používateľa. To znamená, že nie je možné kopírovať alebo importovať čas položky, ktoré sú vytvorené pre používateľa, ktorý je prihlásený ako rezervovateľný prostriedok.

Časové položky, ktoré nie sú pre projekt, budú smerované na schválenie správcovi rezervovateľného prostriedku len vtedy, ak krok 4 v sekcii **Podrobnosti prispôsobenia** vyššie bude dokončený. V opačnom prípade neprojektové časové položky pre iného používateľa budú nesprávne smerované na manažéra prihláseného používateľa. 

### <a name="other-changes"></a>Iné zmeny 
Funkcia **Rezervácie a úlohy** bola odstránená. 

## <a name="multidimensional-pricing"></a>Viacrozmerné ceny
Ak chcete maximalizovať flexibilitu a splniť rôzne obchodné požiadavky, verzia 3 Project Service Automation podporuje diskrétne uplatňovanie súborov cenových dimenzií na cenu a vyúčtovanie sadzieb. Hodnoty dimenzie je možné nastaviť ako predvolené a potom ich kopírovať naprieč procesom ocenenia a oceňovania z profilovania prostriedkov na čas vstupu na skutočné hodnoty projektu. Konfigurácia a modifikácia alebo rozšírenie špecifické pre zákazníka využíva štandardnú infraštruktúru prispôsobiteľnosti.

Project Service Automation sa dodáva s predvolenou sadu cenových dimenzií a rolí a zdrojových jednotiek, a umožňuje nastavenie cien a nákladov pre každú kombináciu roly a organizačnej jednotky.

Pre zákazníkov Project Service Automation, ktorí chcú naďalej používať tieto predpripravené polia ako cenové dimenzie vo verzii 3, nebudú existovať žiadne pozorovateľné zmeny. Môžete naďalej používať Project Service Automation ako zvyčajne. Ak však potrebujete cenu alebo náklady na vaše zdroje pomocou iných dodatočných atribútov, verzia 3 umožňuje pridávať vlastné cenové dimenzie do Project Service Automation. Rozšírenie vlastných cenových dimenzií je komplikovaným konfiguračným zážitkom. 

## <a name="quotes-and-contracts"></a>Cenové ponuky a zmluvy
Vo verzii 3 Project Service Automation sa zmenili aspekty nastavenia a riadenia cenových ponúk a zmlúv. Nasledujúce časti poskytujú podrobnejšie informácie.

### <a name="set-up-chargeability-options"></a>Nastavenie možností účtovateľnosti
Vo verziách 1 a 2 sa nastavenie vznik daňovej povinnosti pre roly a kategórie pre konkrétne cenové ponuky a zmluvy vykonalo pomocou zobrazenia **Účtovateľnosť**, ktorá bola v hornej navigácii riadka cenovej ponuky alebo riadka zmluvy. To bolo tiež, kde by ste mohli nastaviť ceny pre tieto kategórie rol a výdavkov.

Verzia 3, nastavenie možnosti vznik daňovej povinnosti podľa rolí a výdavkov kategórie sa vykoná na úrovni cenovej ponuky alebo zmluvy. Nastavenie cien je oddelené od nastavenia účtovateľnosti. Možnosti **Účtovateľné roly** a **Fakturovateľné kategórie** ako karty nájdete na stránkach **Riadok cenovej ponuky** a **Riadok zmluvy** bez nutnosti používať navigačné prvky v hornej časti.

![Účtovateľné roly.](media/chargeable-12.png)
 
Nastavenie účtovateľných rolí a účtovateľných kategórií tiež využíva predpripravený upraviteľný ovládací prvok mriežky. Pre každú rolu a kategóriu, podporované možnosti pre typ fakturácie počas fázy cenovej ponuky a zmluvy zostávajú nezmenené z predchádzajúcej verzie ako **Účtovateľné** a **Neúčtovateľné**. Možnosť **Bezplatný** nie je podporovaný typ počas fázy cenovej ponuky alebo uzatvárania zmluvy. Možnosť **Bezplatný** je podporovaná iba počas schvaľovania času alebo výdavkov.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Vytvorenie a úprava vlastných cien pre cenovú ponuku Project Service Automation a zmluvu o projekte
Vo verziách 1 a 2, pomocou vlastného cenníka pre konkrétne cenové ponuky a zmluvy bola vykonaná možnosti **Upraviť ceny** na zobrazení **Účtovateľnosť**. Zobrazenie **Účtovateľnosť** sa nachádzalo v hornej navigácii riadka cenovej ponuky alebo riadka zmluvy. Bolo to tiež miesto, kde ste mohli nastavovať možnosť účtovateľnosti pre roly alebo kategórie výdavkov.

Od verzie 3, vytváranie a používanie vlastného projektového cenníka pri cenovej ponuke Project Service Automation a projektovej zmluve Project Service Automation boli oddelené od nastavenia účtovateľnosti. Cenová ponuka Project Service Automation a projektové zmluvy Project Service Automation majú novú kartu s názvom **Cenníky projektov**. Táto karta zobrazuje priradené zobrazenie všetkých cenníkov projektu, ktoré sú pripojené k cenovej ponuke alebo projektovej zmluve Project Service Automation. Ak chcete vytvoriť vlastný cenník z existujúceho cenníka, ktorý je už priradený k projektovej ponuke alebo zmluve, kliknite na možnosť **Vytvorenie vlastných cien**. Tým sa vytvorí kópia všetkých priradených cenníkov a pripojí ich k cenovej ponuke alebo zmluve. Teraz môžete otvoriť cenník a upraviť rolu alebo cenu kategórie výdavkov tak, aby tieto zmeny cien sa vzťahujú len na túto cenovú ponuku alebo zmluvu. 
  
Nasledujúce grafika platí pred vytvorením vlastných cenníkov.

![Pred vlastnými cenníkmi.](media/before-custom-price-lists-13.png)

Nasledujúce grafika zobrazuje stav po vytvorení vlastných cenníkov.

![Po vlastných cenníkoch.](media/after-custom-price-lists-14.png)

> [!NOTE]
> Krátke oneskorenie môže nastať medzi po kliknutí na tlačidlo **Vytvorenie vlastných cien**, keď je vytvorený vlastný cenník. Odporúčame obnoviť mriežku namiesto kliknutia niekoľkokrát. Vlastný cenník bol vytvorený, ak priradený názov cenníka má názov cenovej ponuky alebo názov zmluvy o projekte, ktorý je k nemu priložený.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
