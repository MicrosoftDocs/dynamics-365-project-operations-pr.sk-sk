---
title: Čo je nové alebo zmenené v Project Service Automation verzia 3.x, vlna 1 2020
description: Táto téma poskytuje informácie o tom, čo je nové a zmenené v Project Service Automation verzia 3, vlna 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755581"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Čo je nové alebo zmenené v Project Service Automation verzia 3, vlna 1 2020
Táto téma zdôrazňuje kľúčové aspekty modernizácie pri prechode na najnovšie vydanie Project Service Automation (PSA), verzia 3.x, vlna 1 2020.

## <a name="time-entry"></a>Zadanie času
Rozhranie zadávania času bolo rozšírené, aby poskytovalo možnosti na vloženie časového vstupu do viacerých scenárov zákazníkov. Zahŕňa to možnosť pridávať typy položiek, ktoré teraz riadia špecifické správanie na základe názvu schémy poľa **Nastavenia zadania času**, zobrazené ako **Zdroj času**.

### <a name="upgrade-consideration"></a>Informácie o inovácii
Na podporu tejto funkcie boli roly v rámci PSA aktualizované tak, aby obsahovali nové oprávnenia. Tieto oprávnenia poskytujú prístup na čítanie novej entity, **Nastavenia zadania času**.

Používatelia, ktorí požadujú možnosť zaznamenávania času, by mali mať pridelenú rolu používateľa **Používateľ zadania času** okrem existujúcich rol. Táto rola zahŕňa novú funkčnosť a zaisťuje, aby zadávanie času naďalej fungovalo.

### <a name="currently-extended-time-entry-changes"></a>Aktuálne rozšírené zmeny zadávania času
Aby sa minimalizoval vplyv zadávania času na súčasných používateľov, je táto zmena roly jedinou základnou požiadavkou potrebnou na pokračovanie vo využívaní zadávania času. Ak ste vytvorili vlastné zobrazenia alebo oddelené rozhrania so zadávaním času, musíte nastaviť polia **Nastavenie zadania času** na správnu hodnotu PSA.
