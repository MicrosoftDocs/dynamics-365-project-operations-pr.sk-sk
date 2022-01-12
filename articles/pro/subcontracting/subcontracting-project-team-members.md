---
title: Subdodávky členov projektového tímu
description: Táto téma vysvetľuje, ako zadať subdodávateľom členov projektového tímu v Microsofte Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: b98fc356d7de77fa7f05667acaa5569a7053e4d1
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903775"
---
# <a name="subcontracting-project-team-members"></a>Subdodávky členov projektového tímu

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

V Microsofte Dynamics 365 Project Operations, môžete si vybrať subdodávateľské zmluvy s členmi projektového tímu bez personálu alebo s personálom.

- Členovia projektového tímu bez zamestnancov majú priradený všeobecný zdroj.
- Členovia tímu s personálom majú priradený pomenovaný zdroj.

Keď prepojíte člena projektového tímu s riadkom subdodávok, všetky priradenia k úlohám, ktoré má člen tímu, budú preúčtované na základe nákupného cenníka priloženého k subdodávke.  Na **Odhady** kartu na **Podrobnosti projektu** vyberte stránku **Aktualizujte ceny** zobrazíte aktualizované ceny a/alebo kalkulácie vyplývajúce z rozhodnutia uzavrieť subdodávku. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subdodávky člena projektového tímu bez personálu
The **Podrobnosti o členovi tímu** stránka obsahuje polia subdodávok a subdodávok, ktoré umožňujú projektovému manažérovi vyjadriť, ako by chcel čerpať kapacitu požadovanú zo subdodávky. Ak chcete subdodávateľom člena projektového tímu ako všeobecný zdroj, postupujte takto:

1.  Vyberte si subdodávku na **Detail člena tímu** stránku.

2.  Môžete si vybrať iba subdodávky s **Návrh** alebo **Potvrdené** postavenie. **Zatvorené** alebo **Zrušené** subdodávky nie je možné vybrať. 

3.  The **Subdodávateľská linka** pole sa zobrazí po výbere subdodávky.

4.  V **Subdodávateľská linka** pole, môžete vybrať len linky subdodávok, ktoré sú na čas. Nemôžete vybrať riadky subdodávok pre náklady alebo materiál.

5.  Rola pre záznam člena projektového tímu sa musí zhodovať s rolou na riadku subdodávok. To zaisťuje, že čas pre rolu, ktorá sa odhaduje na projekte, je tá istá rola, ktorá je zakúpená na subdodávateľskej linke. 

Keď je generický člen tímu priradený k subdodávke a subdodávke, **Typ pracovníka** pole v riadku všeobecného člena tímu sa aktualizuje na **Pracovník na dohodu** a **Platnosť subdodávky** bude nastavená na **Platné**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subdodávky s personálne obsadeným členom projektového tímu
Rovnako ako všeobecní alebo nepersonalizovaní členovia tímu, aj kapacita členov tímu potrebná na projekte môže byť spojená so subdodávkou. Ak chcete zadať subdodávateľovi menovaného člena projektového tímu, postupujte takto:

1.  Uistite sa, že pomenovaný zdroj je nastavený ako typ rezervovateľného zdroja zmluvného pracovníka. Tiež sa uistite, že **Predajca** pole na rezervovateľnom zdroji sa zhoduje s dodávateľom v subdodávke, ktorú si vyberáte. 

2.  Môžete si vybrať len subdodávky v **Návrh** alebo **Potvrdené** postavenie. **Zatvorené** alebo **Zrušené** subdodávky nie je možné vybrať. 

3.  The **Subdodávateľská linka** pole sa zobrazí po výbere subdodávky.

4.  V **Subdodávateľská linka** pole, môžete vybrať len linky subdodávok, ktoré sú na čas. Nemôžete vybrať riadky subdodávok pre náklady alebo materiál.

5.  Rola pre záznam člena projektového tímu sa musí zhodovať s rolou na riadku subdodávok. To zaisťuje, že čas pre rolu, ktorá sa odhaduje na projekte, je tá istá rola, ktorá je zakúpená na subdodávateľskej linke. 

Pomenovaní členovia projektového tímu, ktorí sú nastavení typu zmluvného pracovníka **Rezervovateľný zdroj** sa zobrazí so stavom platnosti subdodávky **Neplatný** ak nie sú spojené so subdodávkou. Keď je pomenovaný člen projektového tímu priradený k subdodávke a subdodávke, **Typ pracovníka** pole v riadku člena tímu sa aktualizuje na **Pracovník na dohodu** a **Platnosť subdodávky** bude nastavená na **Platné**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
