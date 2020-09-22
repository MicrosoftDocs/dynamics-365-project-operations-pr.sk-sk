---
title: Vytvoriť šablónu projektu
description: Ako vytvoriť projektovú šablónu v Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755545"
---
# <a name="create-a-project-template-project-service"></a>Vytvorenie projektovej šablóny (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Šablóny projektu šetria čas v prípade, ak má vaša spoločnosť pravidelné ponuky alebo podobné typy projektov. Poskytujú štandardné nastavenie rolí a odhadovaných hodín pre daný typ projektu. Správcovia účtu a projektoví manažéri môžu vytvárať projekty na základe projektovej šablóny, prípadne si môžu šablónu skopírovať a vytvoriť si tak vlastnú.  
  
## <a name="components-of-project-template"></a>Súčasti šablóny projektu
 Šablóna projektu pozostáva z troch zložiek:  
  
- **Štruktúra rozdelenia práce**: Štruktúra rozdelenia práce je šablóna projektu s rovnakými prvkami, ktoré sú aj v projekte. Môžete si vytvoriť hierarchiu úloh, priradiť role k úlohám, zadefinovať atribúty plánov, nastaviť závislosti a pozrieť si všetky údaje v Gantt. Štruktúra rozdelenia práce predstavuje šablónu projektu, ktorá podporuje aj režime úloh pre jednotlivé úlohy. Pri vytváraní pracovného harmonogramu neexistuje žiadny rozdiel medzi šablónou projektu a projektom.  
  
- **Projektové odhady**: projektové odhady v šablónach fungujú rovnako, ako v projektoch. Jediným rozdielom je cenník pre predvolené určenie nákladov a predajných cien, ktorý predstavuje predvolené cenníky nákladov a predajných cien zadefinovaných v parametre [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Zvyšok funkcií je rovnaký ako v projekte.  
  
- **Vytvorenie tímu projektu**: Pri vytváraní projektového tímu šablóny projektu si v nej nemôžete zarezervovať pomenovaný zdroj. V štruktúre rozdelenia prác môžete použiť funkciu **Generovať projektový tím**, čím vytvoríte súbor všeobecných zdrojov. Môžete tiež zadať požadovaných schopnosti a zručností všeobecných zdrojov. Všeobecný zdroj nemôžete nahradiť rezervovateľným zdrojom v šablónach projektu.  
  
## <a name="create-a-project-from-a-template"></a>Vytvorenie projektu zo šablóny  
 Projekt zo šablóny môžete vytvoriť nasledovne:  
  
-   Pri vytváraní projektu z cenovej ponuky si môžete vybrať šablónu projektu vo formulári rýchleho vytvárania projektu.  
  
-   Pri vytváraní projektu kliknutím na možnosť **nový projekt** sa pred uložením záznamu zobrazí formulár projektu. Tu môžete kliknúť na pole **vybrať šablónu**, čím si vyberiete zo zoznamu preddefinovaných projektových šablón svojej organizácie.  
  
-   Kliknite na tlačidlo **Vytvoriť projekt pomocou šablóny** na stránke **Šablóna projektu**, čím vytvoríte projekt zo šablóny.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Kopírovanie komponentov šablóny do projektu  
 Pri kopírovaní súčasti šablóny do projektu, existuje niekoľko vecí, ktoré by ste mali vedieť.  
  
 **Kopírovanie štruktúry rozdelenia práce**: pri kopírovaní štruktúry rozdelenia prác zo šablóny projektu, ak má projekt iný kalendár, než má šablóna, pracovné hodiny kalendára projektu sa použijú na plánovanie úloh. Týmto sa upraví plán záložného kalendára projektu. Podobne si začiatočný dátum prevezme aj prvá úloha na štruktúre rozdelenia práce. Ďalšie úlohy v pláne hierarchie sa teda budú aktualizovať na základe trvania a závislostí stanovených v štruktúre rozdelenia prác šablóny.  
  
 **Kopírovanie odhadov projektu**: pri kopírovaní medziprojektových odhadov sa cenníky aktualizujú na základe vlastníctva jednotiek projektu pre cenník obstarávacej ceny a zákazníka pre cenník predajnej ceny. Jednotkové náklady a predajné ceny sa odvíjajú z cenníkov v projekte, ktoré sú priradené k predajnej entite.  
  
 **Kopírovanie projektového tímu**: Pri kopírovaní projektového tímu zo šablóny do projektu sa skopírujú všeobecné zdroje spolu so zručnosťami a schopnosťami stanovenými v šablóne. Priradenie všeobecných zdrojov sa zachová rovnaké ako pri šablóne projektu.  
  
### <a name="see-also"></a>Pozrite si tiež:  
 [Príručka projektového manažéra](../project-service/project-manager-guide.md)
