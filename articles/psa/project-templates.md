---
title: Projektové šablóny
description: Táto téma poskytuje informácie o používaní šablón projektov na rýchle nastavenie projektu.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: aff6fc5bb855fe1e9007933fdc1a88eb020da0ad
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586041"
---
# <a name="project-templates"></a>Projektové šablóny 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Šablóna projektu je preddefinovaný rámec, ktorý vám pomôže rýchlo a ľahko spustiť projekt. Preddefinované šablóny môžete použiť na vytvorenie nového projektu jediným kliknutím. Čo sa týka projektov, musíte definovať predpoklady pre šablóny projektu. Musíte definovať kalendár projektu pre každú šablónu projektu a roly a cenníky musia byť preddefinované v organizácii tak, aby súčasti šablóny mali užitočné údaje.

Šablóna projektu pozostáva z troch súčastí: plánu, odhadov projektu a členov projektového tímu.

## <a name="schedule"></a>Plánovanie

Plán v šablóne projektu má rovnaký súbor prvkov ako plán v projekte. Môžete si vytvoriť hierarchiu úloh, priradiť role k úlohám, zadefinovať atribúty plánov, a nastaviť závislosti. Plán v šablóne projektu tiež podporuje režimy úloh pre každú úlohu. Preto podporuje plánovací engine. Musíte priradiť projektový kalendár k projektu. Pri vytváraní pracovného plánu neexistuje žiadny rozdiel medzi šablónou projektu a projektom.

## <a name="project-estimates"></a>Odhady projektu

Odhady projektu v šablóne projektu fungujú rovnakým spôsobom ako odhady projektov v projekte. Však náklady a predajné ceny sú stiahnuté z predvolených nákladov a predajných cenníkov , ktoré sú definované v parametroch.

## <a name="creating-a-project-from-a-template"></a>Vytvorenie projektu zo šablóny
 
Existuje niekoľko spôsobov, ako vytvoriť projekt zo šablóny projektu:

- Pri vytváraní projektu z cenovej ponuky si môžete vybrať šablónu projektu v dialógovom okne **rýchle vytvorenie projektu**.

> ![Dialógové okno Rýchle vytvorenie: Projekt.](media/project-11.png)

- Keď vytvoríte projekt výbraním **nový projekt**, stránka **projekt** sa zobrazí pred tým ako sa záznam uloží. V poli **vybrať šablónu** vyberte jednu z preddefinovaných šablón projektu v organizácii.
- Použite **vytvoriť projekt zo šablóny** na stránke **entity šablóny**.

## <a name="copying-components-of-template-to-project"></a>Kopírovanie komponentov šablóny do projektu

Pri kopírovaní súčastí šablóny projektu do projektu, sa môže vyskytnúť niekoľko prepisov v závislosti od nastavení v projekte.

### <a name="copying-the-schedule"></a>Kopírovanie plánu

Ak má projekt rozdielny projektový kalendár ako šablóna, pri kopírovaní plánu zo šablóny projektu, použije sa v pláne úlohy pracovný čas z projektového kalendára. Týmto spôsobom sa upraví plán tak, aby zodpovedal záložnému kalendáru projektu. Podobne si začiatočný dátum projektu prevezme aj prvá úloha v pláne a plán ostatných hierarchií je aktualizovaný na základe trvania a závislostí, ktoré sú stanovené v šablóne. 

### <a name="copying-project-estimates"></a>Kopírovanie odhadov projektu 

Pri kopírovaní naprieč riadkami odhadu projektu, sú cenníky aktualizované. Pre cenník nákladov, sú tieto aktualizácie založené na vlastniacej jednotke projektu. Predajné cenníky sú založené na zákazníkovi. Pre projekty, ktoré sú priradené k predajným entitám, sú jednotkové ceny nákladov a predajov stanovené na základe týchto cenníkov.

### <a name="copying-a-project-team"></a>Kopírovanie projektového tímu

Keď je projektový tím kopírovaný z projektovej šablóny, sú skopírované všeobecné zdroje spolu so zručnosťami a schopnosťami, ktoré sú definované v šablóne. Priradenie všeobecných zdrojov sa zachová rovnaké ako bolo pri šablóne projektu. Pomenované zdroje nie sú podporované v šablónach projektov.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
