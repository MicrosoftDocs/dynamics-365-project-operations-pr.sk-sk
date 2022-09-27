---
title: Členovia projektového tímu v rámci subdodávateľskej zmluvy
description: Tento článok vysvetľuje, ako zadať subdodávateľom členov projektového tímu v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522815"
---
# <a name="subcontracting-project-team-members"></a>Členovia projektového tímu v rámci subdodávateľskej zmluvy

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

V Microsofte Dynamics 365 Project Operations, môžete si zvoliť subdodávku nezamestnaných alebo personálne obsadených členov projektového tímu.

- Členovia projektového tímu bez zamestnancov majú priradený všeobecný zdroj.
- Členovia tímu s personálom majú priradený pomenovaný zdroj.

Keď prepojíte člena projektového tímu s riadkom subdodávok, všetky priradenia k úlohám, ktoré má člen tímu, budú preúčtované na základe nákupného cenníka priloženého k subdodávke.  Na **Odhady** kartu na **Podrobnosti projektu** vyberte stránku **Aktualizujte ceny** zobrazíte aktualizované ceny a/alebo kalkulácie vyplývajúce z rozhodnutia uzavrieť subdodávku. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subdodávky člena projektového tímu bez personálu
The **Podrobnosti o členovi tímu** stránka obsahuje polia subdodávok a subdodávok, ktoré umožňujú projektovému manažérovi vyjadriť, ako by chcel čerpať kapacitu požadovanú zo subdodávky. Ak chcete subdodávateľom člena projektového tímu ako všeobecný zdroj, postupujte takto:

1.  Vyberte si subdodávku na **Detail člena tímu** stránku.

2.  Môžete si vybrať iba subdodávky s **Návrh** alebo **Potvrdené** postavenie. **ZATVORENÉ** alebo **Zrušené** subdodávky nie je možné vybrať. 

3.  The **Subdodávateľská linka** pole sa zobrazí po výbere subdodávky.

4.  V **Subdodávateľská linka** pole, môžete vybrať len linky subdodávok, ktoré sú na čas. Nemôžete vybrať riadky subdodávok pre náklady alebo materiál.

5.  Rola pre záznam člena projektového tímu sa musí zhodovať s rolou v riadku subdodávok. To zaisťuje, že čas pre rolu, ktorá sa odhaduje na projekte, je tá istá rola, ktorá je zakúpená na subdodávateľskej linke. 

Keď je generický člen tímu spojený so subdodávkou a subdodávateľskou líniou, **Typ pracovníka** pole v riadku všeobecného člena tímu sa aktualizuje na **Pracovník na dohodu** a **Platnosť subdodávky** bude nastavená na **Platné**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subdodávky s personálne obsadeným členom projektového tímu
Rovnako ako všeobecní alebo nepersonalizovaní členovia tímu, aj kapacita členov tímu potrebná na projekte môže byť spojená so subdodávkou. Ak chcete zadať subdodávateľovi menovaného člena projektového tímu, postupujte takto:

1.  Uistite sa, že pomenovaný zdroj je nastavený ako typ rezervovateľného zdroja zmluvného pracovníka. Tiež sa uistite, že **Predajca** pole na rezervovateľnom zdroji sa zhoduje s dodávateľom v subdodávke, ktorú si vyberáte. 

2.  Môžete si vybrať len subdodávky v **Návrh** alebo **Potvrdené** postavenie. **ZATVORENÉ** alebo **Zrušené** subdodávky nie je možné vybrať. 

3.  The **Subdodávateľská linka** pole sa zobrazí po výbere subdodávky.

4.  V **Subdodávateľská linka** pole, môžete vybrať len linky subdodávok, ktoré sú na čas. Nemôžete vybrať riadky subdodávok pre náklady alebo materiál.

5.  Rola pre záznam člena projektového tímu sa musí zhodovať s rolou v riadku subdodávok. To zaisťuje, že čas pre rolu, ktorá sa odhaduje na projekte, je tá istá rola, ktorá je zakúpená na subdodávateľskej linke. 

Pomenovaní členovia projektového tímu, ktorí sú nastavení typu zmluvného pracovníka **Rezervovateľný zdroj** sa zobrazí so stavom platnosti subdodávky **Neplatný** ak nie sú spojené so subdodávkou. Keď je pomenovaný člen projektového tímu priradený k subdodávke a subdodávateľskej línii, **Typ pracovníka** pole v riadku člena tímu sa aktualizuje na **Pracovník na dohodu** a **Platnosť subdodávky** bude nastavená na **Platné**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
