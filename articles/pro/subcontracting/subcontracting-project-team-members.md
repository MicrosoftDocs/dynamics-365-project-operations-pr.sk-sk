---
title: Členovia projektového tímu v rámci subdodávateľskej zmluvy
description: Tento článok vysvetľuje, ako uzatvárať subdodávateľské zmluvy s členmi projektového tímu v Microsoft Dynamics 365 Project Operations.
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

V Microsoft Dynamics 365 Project Operations si môžete si zvoliť uzatvorenie subdodávateľskej zmluvy s členmi projektového tímu bez personálneho obsadenia alebo s personálnym obsadením.

- Členovia projektového tímu bez personálneho obsadenia majú priradený všeobecný zdroj.
- Členovia tímu s personálnym obsadením majú priradený menovaný zdroj.

Keď prepojíte člena projektového tímu s riadkom subdodávateľskej zmluvy, všetky priradenia k úlohám, ktoré má člen tímu, budú preúčtované na základe nákupného cenníka priloženého k subdodávateľskej zmluve.  Na karte **Odhady** na stránke **Podrobnosti projektu** vyberte tlačidlo **Aktualizovať ceny** a zobrazíte aktualizované ceny a/alebo kalkulácie vyplývajúce z rozhodnutia uzavrieť subdodávateľskú zmluvu. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subdodávateľská zmluva člena projektového tímu bez personálneho obsadenia
Stránka **Podrobnosti o členovi tímu** obsahuje polia subdodávateľskej zmluvy a riadku subdodávateľskej zmluvy, ktoré umožňujú projektovému manažérovi vyjadriť, ako by chcel čerpať kapacitu požadovanú zo subdodávateľskej zmluvy. Ak chcete vytvoriť subdodávateľskú zmluvu s členom projektového tímu ako všeobecný zdrojom, postupujte takto:

1.  Vyberte si subdodávateľskú zmluvu na stránke **Podrobnosti o členovi tímu**.

2.  Môžete vybrať subdodávateľské zmluvy v stave **Koncept** alebo **Potvrdené**. **Zatvorené** alebo **Zrušené** subdodávateľské zmluvy nie je možné vybrať. 

3.  Pole **Riadok subdodávateľskej zmluvy** sa zobrazí po výbere subdodávateľskej zmluvy.

4.  V poli **Riadok subdodávateľskej zmluvy** môžete vybrať len riadky subdodávateľskej zmluvy, ktoré sú pre čas. Nemôžete vybrať riadky subdodávateľskej zmluvy pre náklady ani materiál.

5.  Rola pre záznam člena projektového tímu sa musí zhodovať s rolou v riadku subdodávateľskej zmluvy. To zaisťuje, že čas pre rolu, ktorá sa odhaduje na projekte, je tá istá rola, ktorá je zakúpená na riadku subdodávateľskej zmluvy. 

Keď je všeobecný člen tímu spojený so subdodávateľskou zmluvou a riadkom subdodávateľskej zmluvy, pole **Typ pracovníka** v riadku všeobecného člena tímu sa aktualizuje na **Zmluvný pracovník** a hodnota **Platnosť subdodávateľskej zmluvy** sa nastaví na **Platné**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subdodávka člena projektového tímu s personálnym obsadením
Rovnako ako všeobecní členovia tímu alebo členovia tímu bez personálneho obsadenia, aj kapacita členov tímu s personálnym obsadením potrebná pre projekt môže byť spojená so subdodávateľskou zmluvou. Ak chcete vytvoriť subdodávateľskú zmluvu s menovaným členom projektového tímu, postupujte takto:

1.  Uistite sa, že menovaný zdroj je nastavený ako typ rezervovateľného zdroja zmluvného pracovníka. Tiež sa uistite, že pole **Predajca** v rezervovateľnom zdroji sa zhoduje s dodávateľom v subdodávateľskej zmluve, ktorú si vyberáte. 

2.  Môžete vybrať subdodávateľské zmluvy v stave **Koncept** alebo **Potvrdené**. **Zatvorené** alebo **Zrušené** subdodávateľské zmluvy nie je možné vybrať. 

3.  Pole **Riadok subdodávateľskej zmluvy** sa zobrazí po výbere subdodávateľskej zmluvy.

4.  V poli **Riadok subdodávateľskej zmluvy** môžete vybrať len riadky subdodávateľskej zmluvy, ktoré sú pre čas. Nemôžete vybrať riadky subdodávateľskej zmluvy pre náklady ani materiál.

5.  Rola pre záznam člena projektového tímu sa musí zhodovať s rolou v riadku subdodávateľskej zmluvy. To zaisťuje, že čas pre rolu, ktorá sa odhaduje na projekte, je tá istá rola, ktorá je zakúpená na riadku subdodávateľskej zmluvy. 

Menovaní členovia projektového tímu, ktorí sú nastavení ako typ zmluvného pracovníka **Rezervovateľný zdroj**, sa zobrazia so stavom platnosti subdodávateľskej zmluvy **Neplatný**, ak nie sú spojení so subdodávateľskou zmluvou. Keď je menovaný člen projektového tímu spojený so subdodávateľskou zmluvou a riadkom subdodávateľskej zmluvy, pole **Typ pracovníka** v riadku člena tímu sa aktualizuje na **Zmluvný pracovník** a hodnota **Platnosť subdodávateľskej zmluvy** sa nastaví na **Platné**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
