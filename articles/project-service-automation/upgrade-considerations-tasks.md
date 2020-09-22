---
title: Informácie o inovácii o štruktúre rozdelenia práce
description: Táto téma poskytuje informácie o inovácii štruktúry rozdelenia práce z programu Project Service Automation 2.x na 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755622"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Informácie o inovácii o štruktúre rozdelenia práce
Táto téma poskytuje informácie o inovácii štruktúry rozdelenia práce z programu Project Service Automation 2.x na 3.x. Táto téma definuje dobrý stav projektu v Project Service Automation (PSA), ktorý je potrebný pre úspešnú inováciu. Je tam tiež informácia o bežných podmienkach blokovania, ktoré budú po inovácii neúspešné. Ďalšie informácie o definovaní projektových úloh a ich funkcií v rámci plánu projektu nájdete v časti [Projektové plány](project-creating.md).

## <a name="key-entities"></a>Kľúčové entity
Pre presnú štruktúru rozdelenia práce, ktorá je už načítaná so zdrojmi, sa požadujú nasledujúce entity:

- [Projekt](../developer/entities/msdyn_project.md)
- [Projektový tím](../developer/entities/msdyn_projectteam.md)
- [Projektová úloha](../developer/entities/msdyn_projecttask.md)
- [Priradenia zdrojov](../developer/entities/msdyn_resourceassignment.md)
- [Závislosť projektovej úlohy](../developer/entities/msdyn_projecttaskdependency.md)
- [Rezervovateľné zdroje](../developer/entities/bookableresource.md)

Ak chcete definovať prostriedok načítaný štruktúrou rozdelenia práce, musíte vykonať nasledujúce kroky:

1. Vytvorte nový projekt. Ďalšie informácie o vytváraní nového projektu nájdete v časti [msdyn_project](../developer/entities/msdyn_project.md).
2. Vytvorte jednu alebo viac úloh. Ďalšie informácie o vytváraní úlohy si prečítajte v časti [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).
3. Definovanie závislostí úloh. Viac informácií nájdete v časti [Závislosť projektovej úlohy](../developer/entities/msdyn_projecttaskdependency.md).
4. Priraďte členom projektového tímu projekt. Ďalšie informácie nájdete v dokumente [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).
5. Priraďte členov projektového tímu k úlohám. Ďalšie informácie nájdete v dokumente [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).

## <a name="project-team-relationships"></a>Vzťahy projektového tímu

Ak chcete zabezpečiť úspešnú inováciu, musia byť správne udržiavané nasledujúce vzťahy:
- Všetci členovia projektového tímu musia byť spájaní s rezervovateľnými zdrojmi.
- Všetci členovia projektového tímu musia byť spájaní s rovnakým projektom. 

## <a name="project-task-relationships"></a>Vzťahy projektovej úlohy
Ak chcete zabezpečiť úspešnú inováciu, musia byť správne udržiavané nasledujúce vzťahy:

- Všetky súvisiace úlohy musia byť priradené k rovnakému projektu.
- Každá riadna úloha musí mať nadradenú úlohu.
- Každá riadna úloha musí mať nadradený projekt.

### <a name="valid-conditions"></a>Platné podmienky

- Všetky trvania úloh musí byť väčšie alebo rovné (>=) jednej hodiny a menej ako 1 800 000 minút (1 250 dní).*
- Všetky úlohy musia mať počiatočný dátum nie skôr ako 2000/01/01.*
- Všetky úlohy musia mať počiatočný dátum najneskôr 17 rokov od dnešného dňa.*
- Všetky úlohy musia mať počiatočný dátum skorší alebo rovný dátumu dokončenia.
- Všetky typy klasifikácie (náklady, materiál, daň a čas) musia mať hodnoty pre **predvolenú jednotku** a **jednotkovú skupinu**.
- Malo by sa vyhýbať formátom dátumov s písmenami.

### <a name="potential-mitigation-steps"></a>Potenciálny postup zmiernenia
- Pomocou rozšíreného vyhľadávania môžete identifikovať úlohy projektu, ktoré neobsahujú ID projektu.
- Pomocou rozšíreného vyhľadávania môžete identifikovať úlohy projektu, pri ktorých je plánované trvanie väčšie ako 1 800 000.
- Pred vykonaním akýchkoľvek zmien údajov by ste mali preskúmať všetky prispôsobenia spojené s entitou, ktoré mohli viesť k uvedeniu údajov do nesprávneho stavu. Tieto prispôsobenia by sa mali vyriešiť pred pokračovaním akýchkoľvek aktualizácií týkajúcich sa údajov.
- V prípade identifikovaných úloh, ktoré boli osamotené, zvážte odstránenie týchto úloh, ak nie sú potrebné alebo ak by sa mali spojiť so správnym nadradeným projektom.
- V prípade akýchkoľvek úloh, ktorých trvanie je dlhšie ako 1 250 dní, zvážte pridanie viacerých úloh, ktoré predstavujú celkové trvanie, ak je to možné.

> [!NOTE]
> Položky označené hviezdičkou (\*) majú limity, ktoré sú spôsobené tým, že riadenie vzťahov so zákazníkmi (CRM) podporuje iba 7 320 rozšírení opakovania. Musíte zostať pod týmto limitom.

## <a name="resource-assignment-relationships"></a>Vzťahy priradenia zdrojov
Ak chcete zabezpečiť úspešnú inováciu, musia byť správne udržiavané nasledujúce vzťahy:

- Všetky priradenia zdrojov v štruktúre rozdelenia práce musia súvisieť s tým istým projektom.
- Všetky priradenia zdrojov v štruktúre rozdelenia práce musia byť priradené k členom projektového tímu v rovnakom projekte.

### <a name="potential-mitigation-steps"></a>Potenciálny postup zmiernenia
- Identifikujte všetky úlohy, ktoré nespĺňajú vyššie uvedené podmienky.  
- Všetky priradenia zdrojov, ktoré už nie sú platné, by sa mali odstrániť.

## <a name="project-task-dependency-relationships"></a>Vzťahy závislosti projektovej úlohy
Ak chcete zabezpečiť úspešnú inováciu, musia byť správne udržiavané nasledujúce vzťahy:

- Všetky závislosti projektových úloh musia súvisieť s rovnakým projektom.
- Úloha nemôže mať rovnakú závislosť odkazovanú viackrát.
