---
title: Naplánovať projekt so štruktúrou rozdelenia práce
description: Ako naplánovať projekt so štruktúrou rozdelenia práce v Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d77d9f8427f06015d4f4cb9438d7f59ac840b061
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084546"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Naplánovať projekt so štruktúrou rozdelenia práce (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Plán projektu komunikuje, akú prácu treba vykonať, ktoré zdroje budú vykonávať prácu, a časový rámec v ktorom práca musí byť dokončená. Plán projektu odráža všetky práce spojené s realizáciu projektu na čas. Jedným z prvých krokov vo fáze začatia projektu je prísť s plánom projektu. Ak chcete vytvoriť plán projektu, musíte vytvoriť štruktúru pracovných rozpisov.  
  
 Vytvorte štruktúru projektu so štruktúrou rozdelenia prác, ktorá vám pomôže:  
  
- Rozobrať práce do konkrétnych úloh  
  
- Odhad času potrebného na dokončenie úlohy  
  
- Určenie závislostí medzi úlohami a trvanie úloh  
  
- Určenie úloh na dokončenie každej úlohy  
  
  Plán projektu v štruktúre rozdelenia práce má známy vzhľad a jeho súčasťou je interaktívny Ganttov graf.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Vytvárať štruktúru rozdelenia práce pre projekt  
 Vytvárať štruktúru rozdelenia práce na zastúpenie postupnosti úloh v projekte. Štruktúra rozdelenia práce zahŕňa úlohy, požiadavky každej úlohy a informácie o výnosoch a nákladoch. V štruktúre rozdelenie práce môžete pridať:  
  
-   Poradie úloh v hierarchii  
  
-   Ostatné úlohy, ktoré musia byť dokončené pred spustením úlohy  
  
-   Počiatočný dátum, koncový dátum a trvanie úlohy  
  
-   Počet hodín, ktoré sú potrebné pre úlohy  
  
-   Požadované zručnosti a vzdelanie každého pracovníka  
  
-   Pracovníci, ktorí sú priradení k úlohe  
  
-   Odhadované výnosy a náklady  
  
## <a name="task-types"></a>Typ úloh  
Pri vytváraní vašej štruktúry rozdelenia práce budete používať tieto druhy úloh:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Koreňový uzol projektu** | Súhrn úloh najvyššej úrovne pre projekt. Všetky ostatné úlohy projektu sú vytvorené pod ním. Názov koreňovej úlohy je názov projektu. Úsilie, dátumy a trvanie koreňového uzla vychádzajú z hodnôt v hierarchii pod ním. Nemôžete upraviť vlastnosti koreňového uzla, ani koreňový uzol odstrániť. | 
| **Súhrn alebo zásobník úloh** | Súhrnná úloha je úloha, ktorá má priradené čiastkové úlohy. Súhrnná úloha nemá žiadne pracovné úsilie, ani vlastné náklady. Jeho pracovného úsilia a náklady sú súhrnom jeho čiastkových úloh. Môžete zmeniť názov súhrnnej úlohy, ale nie je možné zmeniť úsilie, dátumy alebo čas, pretože tie sa vypočítajú automaticky. Odstránenie súhrnnej úlohy odstráni úlohu a všetkých jej čiastkové úlohy.|  
| **Úlohy listového uzla** | Úloha listového uzla predstavuje najpodrobnejšie práce na projekte. Má odhadnuté úsilie, plánovaný počet zdrojov, plánovaný dátum začatia a ukončenia a celkové trvanie.|

  
## <a name="task-hierarchy"></a>Hierarchia úlohy  
 Pri vytváraní hierarchia úloh máte nasledujúce možnosti:  
  
- **Pridať úlohu**.   Úlohy môžete pridať na pozícii, ktorú si v hierarchii úlohy vyberiete. Ak nevyberiete pozíciu, objaví sa na konci vašej novej úlohy.  
  
- **Zväčšiť odsadenie úlohy**.   Odsaďte úlohu, aby sa stala podriadenou úlohe, ktorá je priamo nad ňou.  
  
- **Zmenšiť odsadenie úlohy**.   Zmenšiť odsadenie úlohy, aby už nebolo podriadenou úlohou svojej pôvodne nadradenej úlohy.  
  
- **Posunúť nahor a posunúť nadol**.   Posúvajte úlohy nahor a nadol v hierarchii nadradenej úlohy. Presúvanie úloh nahor alebo nadol, nemá vplyv na jeho úsilie, náklady, termíny, alebo trvanie.  
  
## <a name="task-attributes"></a>Atribúty úlohy  
 Názov úlohy popisuje prácu, ktorú treba dokončiť. Použite rôzne atribúty úloh na popísanie plánu a personálnych požiadaviek na úlohu.  
  
### <a name="schedule-attributes"></a>Naplánovať atribúty

 - Priraďte hodnoty do **hodín úsilie** , **počet zdrojov** , **dátum začatia** , **dátum skončenia** a **trvanie** na stanovenie plánu úlohy. 
 - **Úsilie** je odhad hodín, ktoré sú potrebné na dokončenie úlohy.
 - **Počet zdrojov** je odhad, ktorý projektový manažér použije v úlohe na čo najlepší plán. 
 - **Trvanie** (v dňoch) udáva počet pracovných dní, koľko bude trvať dokončenie úlohy.  
  
### <a name="staffing-attributes"></a>Personálne atribúty

 - **Úloha** , **Organizačná jednotka zdroja** , **Počet zdrojov** a **Zdroje** popisujú personálne požiadavky úlohy. 
 - **Úloha** popisuje typ zdroja, ktorý je potrebný na vykonanie úlohy. 
 - **Organizačná jednotka zdroj** označuje organizačnú jednotku, z ktorej by mal byť personálom obsadený zdroj úlohy. Ovplyvňuje to tiež odhad nákladov a predajov úlohy, pretože sa na to odkazuje pri odhadovaní jednotkovej predajnej ceny zdroja. 
 - **Zdroje** má všeobecný prostriedok alebo prostriedok s názvom keď sa nájde.  
  
## <a name="task-dependencies"></a>Závislosti úloh  
 Môžete vytvoriť predchodcu vzťah jednej alebo viacerých úloh štruktúry rozdelenia práce. Môžete nastaviť jednu alebo viacero hodnôt v poli predchodcu úlohy na označenie úloh, ktoré sú závislé. Keď priradíte hodnotu predchodcu úlohy, úloha môže začať iba ak sa dokončili všetky predchádzajúce úlohy. Nastavenie tejto závislosti na úlohe bude mať za následok prepočet plánovaného dátum začatia úlohy ako najneskoršieho konca všetkých svojich predchodcov. Predchodcov vplyv na plán nie sú obmedzované stanoveným režimom úlohy.  
  
## <a name="task-mode"></a>Režim úlohy  
 Režim úlohy je jedným z dôležitých faktorov, ktoré určujú plánovanie úloh listového uzla. Existujú dva režimy pre každú úlohu: režim automatického plánovania a režim manuálneho plánovania.  
  
-   **Automatické plánovanie**.   Keď nastavíte režim úlohy na automatické plánovanie, systém plánovania úloh použije pravidlá plánovania na nasledovné atribúty úloh, čím sa určí plán úlohy:  
  
    -   Predchodcovia  
  
    -   Úsilie  
  
    -   Počet zdrojov  
  
    -   počiatočný a koncový dátum,  
  
-   **Moje pravidlá plánovania**.   Dátum začiatku listového uzla úlohy nemá prednastavených predchodcov plánovaného počiatočného dátumu plánovania projektu. Trvanie úlohy listového uzla sa vždy vypočítava ako počet pracovných dní medzi dátumom začatia a skončenia. Po automatickom naplánovaní úlohy bude systém plánovania sledovať nižšie uvedené pravidlá:  
  
    -   Počiatočný a koncový dátum úlohy musí vždy byť pracovný deň v súlade s plánovacím kalendárom projektu  
  
    -   Dátum začatia úlohy, ktorá má predvolených predchodcov poslednému dátumu ukončenia svojich predchodcov  
  
    -   Úsilie = počet ľudí * trvanie * hodín v štandardný pracovný deň kalendára projektu  
  
-   **Ručné plánovanie**.   V niektorých prípadoch sa budete chcieť od týchto pravidiel odchýliť. V týchto prípadoch môžete nastaviť režim úloh na manuálne naplánované úlohy. Tým plánovací systém prestane vypočítavať hodnoty pre ostatné atribúty plánovania. Nastavenie predchodcov úloh vždy ovplyvní dátum začatia závislej úlohy.  
  
## <a name="create-a-work-breakdown-structure"></a>Vytvorenie štruktúry rozdelenia práce  
  
1.  Prejdite na **Project Service > Projekty**.  
  
2.  Kliknite na projekt, na ktorom chcete pracovať.  
  
3.  Na paneli v hornej časti obrazovky zvoľte šípku ukazujúcu nadol vedľa názvu projektu a potom kliknite na Štruktúra rozdelenia práce.  
  
4.  Ak chcete pridať úlohu, kliknite na **Pridať úlohu**. Vyplňte polia pre úlohu a potom kliknite na položku **Uložiť**.  
  
5.  Pokračujte v pridávaní úloh, kým nebude štruktúra rozdelenia práce úplná. Pri vytváraní vašej štruktúry rozdelenia práce, môžete vykonať nasledovné činnosti pri organizácii svojich úloh:  
  
    -   Vyberte úlohu a kliknite na tlačidlo **Zarážka** ju presuniete pod inú úlohu, alebo kliknite na zmenšenie odsadenia ju presuniete mimo úrovne.  
  
    -   Vyberte úlohu a kliknite na tlačidlo **Posunúť nahor** alebo **Posunúť nadol** , čím ju presuniete v zozname nadol alebo nahor.  
  
    -   Kliknite na tlačidlo **Skryť ganttov graf** skryjete ganttov graf. Kliknutím na **Zobraziť ganttov graf** ho znova zobrazíte.  
  
    -   Zvoľte rôzne obdobie času pre ganttov graf v časti **Časový rozsah**.  
  
6.  Na pridanie rol, ktoré ste zadali do vašej štruktúry rozdelenia práce pre členov tímu projektu, kliknite na tlačidlo **Generovať projektový tím**.  
  
7.  Po skončení so zmenami kliknite na možnosť **Uložiť** v pravom spodnom rohu obrazovky.  
  
### <a name="see-also"></a>Pozrite si tiež  
 [Príručka projektového manažéra](../psa/project-manager-guide.md)
