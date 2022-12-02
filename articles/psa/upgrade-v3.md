---
title: Dôležité informácie týkajúce sa inovácie – Microsoft Dynamics 365 Project Service Automation z verzie 2.x alebo 1.x na verziu 3
description: Tento článok poskytuje informácie o úvahách, ktoré musíte vykonať pri inovácii zo systému Project Service Automation verzie 2. x alebo 1. x na verziu 3.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3f67b2fe39c9d0224207e7c655892318ec7e09b8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918929"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Informácie o inovácii – PSA verzie 2.x alebo 1.x na verziu 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation a Field Service
Dynamics 365 Project Service Automation a Dynamics 365 Field Service používajú riešenie Universal Resourcing Scheduling (URS) na plánovanie zdrojov. Ak máte vo svojej inštancii Project Service Automation a Field Service, inovujte obe riešenia na najnovšiu verziu. Pre Project Service Automation je to verzia 3.x. Pre službu Field Service je to verzia 8.x. Aktualizáciou Project Service Automation alebo Field Service sa nainštaluje najnovšia verzia URS. Ak riešenia Project Service Automation a Field Service v rovnakej inštancii nie sú inovované na najnovšiu verziu, môže dôjsť k nekonzistentnému správaniu.

## <a name="resource-assignments"></a>Priradenia zdrojov
V Project Service Automation verzia 2 a verzia 1, priradenia úloh boli uložené ako podradené úlohy (nazývané aj riadkové úlohy) **entita Úloha** a nepriamo súvisí s entitou **Priradenie zdroja**. Riadkové úlohy boli viditeľné v okne nasadenia na štruktúre rozdelenia práce (WBS).

![Riadkové úlohy na WBS v Project Service Automation, verzia 2 a verzia 1.](media/upgrade-line-task-01.png)

Vo verzii 3 Project Service Automation sa zmenila základná schéma priraďovania rezervovateľných zdrojov k úlohám. Riadkové úlohy boli zastarané a existuje priama 1:1 vzťah medzi úlohy v **entite Úloha** a členom tímu v entite priradenia **Priradenie zdroja**. Úlohy, ktoré sú priradené k členovi projektového tímu, sa teraz ukladajú priamo do entity priradenia prostriedkov.  

Tieto zmeny majú vplyv na inováciu všetkých existujúcich projektov, ktoré majú priradenia prostriedkov pre pomenované rezervovateľné zdroje a všeobecné zdroje v projektovom tíme. Tento článok poskytuje úvahy, ktoré budete musieť vziať do úvahy pre vaše projekty pri inovácii na verziu 3. 

### <a name="tasks-assigned-to-named-resources"></a>Úlohy priradené k pomenovaným zdrojom
Pomocou podkladovej entity úloh úlohy vo verzii 2 a verzii 1 umožnili členom tímu vykresliť inú rolu, než je predvolená definovaná rola. Napríklad Lucia Kováčová, ktorá je predvolene priradená k roli manažér programu, môže byť priradená k úlohe s rolou Vývojár. Vo verzii 3 je vždy predvolená úloha pomenovaného člena tímu, takže všetky úlohy, ku ktorým je Lucia Kováčová priradená používa Luciinu predvolenú rolu manažéra programu.

Ak ste priradili prostriedok k úlohe mimo ich predvolenú rolu vo verzii 2 a verzia 1, pri inovácii, pomenovaný prostriedok bude priradený k predvolenej role pre všetky priradenia úloh, bez ohľadu na priradenie rolí vo verzii 2. Výsledkom tohto pridelenia budú rozdiely vo vypočítaných odhadoch z verzie 2 alebo verzie 1 na verziu 3, pretože odhady sa vypočítajú na základe roly prostriedku a nie priradenia úlohy riadka. Napríklad vo verzii 2 boli priradené dve úlohy pre Jarmila Gajdošová. Úloha v riadku úloha pre úlohu 1 je Vývojár a pre úlohu 2 manažér programu. Jarmila Gajdošová má predvolenú úlohu manažéra programu.

![Viacero rolí priradených jednému zdroju.](media/upgrade-multiple-roles-02.png)

Pretože sa roly Vývojár a programový manažér líšia, odhady nákladov a predajov sú nasledovné:

![Odhady nákladov pre roly zdrojov.](media/upggrade-cost-estimates-03.png)

![Odhady predajov pre roly zdrojov.](media/upgrade-sales-estimates-04.png)

Pri inovácii na verziu 3, riadkové úlohy nahrádzajú priradenia prostriedkov na úlohu členom tímu rezervovateľného prostriedku. Nasadenie použije predvolenú úlohu rezervovateľného prostriedku. V nasledujúcom obrázku, Jarmila Gajdošová, ktorá má úlohu manažéra programu, je zdrojom.

![Priradenia zdrojov.](media/resource-assignment-v2-05.png)

Keďže odhady vychádzajú z predvolenej roly prostriedku, odhady predaja a nákladov sa môžu zmeniť. V nasledujúcom obrázku už nevidíte rolu **Vývojár**, pretože rola sa teraz vzala z predvolenej roly rezervovateľného zdroja.

![Odhady nákladov pre predvolené roly.](media/resource-assignment-cost-estimate-06.png)
![Odhad predaja pre predvolené roly.](media/resource-assignment-sales-estimate-07.png)

Po dokončení inovácie môžete upraviť rolu člena tímu tak, aby bola iná ako priradená predvolená hodnota. Ak však zmeníte rolu členov tímu, zmení sa na všetky pridelené úlohy, pretože členovia tímu nemôžu prideliť viaceré roly vo verzii 3.

![Aktualizácia roly zdroja.](media/resource-role-assignment-08.png)

To platí aj pre riadkové úlohy, ktoré boli priradené k pomenovaných prostriedkov, keď zmeníte jednotku organizácie prostriedku z predvoleného nastavenia na inú organizačnú jednotku. Po dokončení inovácie verzie 3 bude priradenie používať predvolenú organizačnú jednotku prostriedku namiesto jednej množiny na úlohu v riadku.

### <a name="tasks-assigned-to-generic-resources"></a>Úlohy priradené k všeobecným zdrojom
Vo verzii 2 a verzia 1, môžete nastaviť rolu a organizačnej jednotky na úlohu a potom použite funkciu **Generovať tím** na vygenerovanie všeobecných zdrojov založených na atribútoch stanovených v úlohe. Vo verzii 3 vytvoríte všeobecných členov tímu s rolou a organizačnou jednotkou a potom priraďte členom tímu úlohy.

Vo verzii 2 a verzii 1 môžu byť projekty so všeobecnými zdrojmi v dvoch stavoch alebo kombináciou oboch na úrovni úloh. Napríklad môžete mať nasledovné scenáre:

- Úlohy s rolami a súborom organizačných jednotiek, ale bez pridružených priradení prostriedkov boli vytvorené.
- Úlohy s generickými priradeniami prostriedkov člena tímu, ktoré boli priradené vytvorením všeobecného prostriedku použitím funkcie **Generovať tím**.

Pred začatím inovácie, odporúčame, aby ste opätovne vygenerovali tím pre každý projekt, ktorý má úlohy pridelené všeobecným zdrojom alebo ešte čaká na spustenie procesu generovania tímu.

Pre úlohy, ktoré sú priradené k všeobecným členom tímu, ktorí boli generovaní prostredníctvom možnosti **Generovať tím** ponechá inovácia všeobecné zdroje v tíme a ponechá priradenie k danému všeobecnému členovi tímu. Odporúčame, aby ste vygenerovali požiadavku na zdroj pre všeobecného člena tímu po inovácii, ale skôr, než si rezervujete alebo odošlete požiadavku na zdroj. Tým sa zachovajú všetky priradenia organizačnej jednotky na všeobecných členov tímu, ktoré sa líšia od zmluvnej organizačnej jednotky projektu.

Napríklad v projekte Project Z je zmluvnou jednotkou Contoso US. V projektovom pláne boli úlohy testovania v rámci fázy implementácie pridelené technickým konzultantom úlohy a priradenou organizačnou jednotkou Contoso India.

![Priradenie implementačnej fázy organizácie.](media/org-unit-assignment-09.png)

Po fáze implementácie je úloha integračného testu priradená role Technický konzultant, no organizácia je nastavená na Contoso US.  

![Úloha priradenia testovacej úlohy pre integráciu.](media/org-unit-generate-team-10.png)

Keď vytvoríte tím pre projekt, dvaja všeobecní členovia tímu sú vytvorené z dôvodu rôznych organizačnej jednotiek v úlohách. Technický konzultant 1 bude pridelený k úlohám Contoso India a technický konzultant 2 bude mať úlohy Contoso US.  

![Vygenerovaní všeobecní členovia tímu.](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> V Project Service Automation verzia 2 a verzia 1, člen tímu nedrží organizačnú jednotku, ktorá sa uvádza v riadku úlohy.

![Riadkové úlohy verzie 2 a verzie 1 v Project Service Automation.](media/line-tasks-12.png)

Organizačnú jednotku môžete zobraziť v zobrazení odhadov. 

![Odhady organizačnej jednotky.](media/org-unit-estimates-view-13.png)
 
Po dokončení inovácie sa k všeobecnému členovi tímu pridá organizačná jednotka, ktorá zodpovedá všeobecnému členovi tímu a odstráni sa riadok úlohy. Z tohto dôvodu odporúčame pred inováciou generovať alebo znova generovať tím na každý projekt, ktorý obsahuje všeobecné prostriedky.

Pre úlohy, ktoré sú priradené k úlohe s jednotkou organizácie, ktorá sa odlišuje od organizačnej jednotky zmluvného projektu a tím nebol vygenerovaný, inovácia vytvorí generický člen tímu pre rolu, ale použije zmluvnú jednotku projektu pre člena tímu organizačnej jednotky. S odvolaním sa na príklad s projektom Z, zmluvná jednotka organizácie Contoso a úlohy testovania projektových plánov v rámci fázy implementácie boli priradené k úlohe technického poradcu s organizačnou jednotkou Contoso India. Testovacia úloha integrácie dokončená po fáze implementácie bola priradená roly Technický konzultant. Jednotka organizácie je Contoso US a tím nebol vygenerovaný. Inovácia vytvorí jedného všeobecného člena tímu, technického poradcu, ktorý má pridelené hodiny všetkých troch úloh a organizačnej jednotky Contoso US, zmluvnej organizačnej jednotky projektu.   
 
Zmena predvolené rôznych zdrojov organizačnej jednotky na negenerovaných členov tímu je dôvod, prečo odporúčame generovať alebo opätovne generovať tím na každý projekt, ktorý obsahuje všeobecné prostriedky pred inováciou tak, aby nedošlo k strateniu priradení organizačných jednotiek.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
