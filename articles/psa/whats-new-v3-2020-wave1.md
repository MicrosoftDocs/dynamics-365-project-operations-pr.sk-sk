---
title: Čo je nové alebo zmenené v Project Service Automation verzia 3.x, vlna 1 2020
description: Táto téma poskytuje informácie o tom, čo je nové a zmenené v Project Service Automation verzia 3, vlna 1 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
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
ms.openlocfilehash: 073b70b4ae02d943eb0794b51e888815ee16f438
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577899"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Čo je nové alebo zmenené v Project Service Automation verzia 3, vlna 1 2020

[!include [banner](../includes/psa-now-project-operations.md)]

Táto téma zdôrazňuje kľúčové aspekty modernizácie pri prechode na najnovšie vydanie Project Service Automation (PSA), verzia 3.x, vlna 1 2020.

## <a name="time-entry"></a>Zadanie času
Rozhranie zadávania času bolo rozšírené, aby poskytovalo možnosti na vloženie časového vstupu do viacerých scenárov zákazníkov. Zahŕňa to možnosť pridávať typy položiek, ktoré teraz riadia špecifické správanie na základe názvu schémy poľa **Nastavenia zadania času**, zobrazené ako **Zdroj času**. Na podporu tejto funkcie bolo pridané nové riešenie s názvom Čas, výdavky, štatúty a schválenia (TESA).

### <a name="upgrade-consideration"></a>Informácie o inovácii
Na podporu tejto funkcie boli roly v rámci PSA aktualizované tak, aby obsahovali nové oprávnenia. Tieto oprávnenia poskytujú prístup na čítanie novej entity, **Nastavenia zadania času**.

Používatelia, ktorí požadujú možnosť zaznamenávania času, by mali mať pridelenú rolu používateľa **Používateľ zadania času** okrem existujúcich rol. Táto rola zahŕňa novú funkčnosť a zaisťuje, aby zadávanie času naďalej fungovalo.

Ak máte okrem toho ešte vlastné moduly aplikácií, ktoré zahŕňajú všetky formuláre pre entitu zadania času, budete musieť z modulu odstrániť **Formulár rýchleho vytvorenia zadaní času TESA**.

### <a name="currently-extended-time-entry-changes"></a>Aktuálne rozšírené zmeny zadávania času
Aby sa minimalizoval vplyv zadávania času na súčasných používateľov, je táto zmena roly jedinou základnou požiadavkou potrebnou na pokračovanie vo využívaní zadávania času. Ak ste vytvorili vlastné zobrazenia alebo oddelené rozhrania so zadávaním času, musíte nastaviť polia **Nastavenie zadania času** na správnu hodnotu PSA.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
