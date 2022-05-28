---
title: Nasadenie aplikácie Project Operations – čiastočné
description: Táto téma poskytuje informácie o tom, ako nainštalovať jednoduché nasadenie Project Operations – dohoda o fakturácii pro forma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580751"
---
# <a name="deploy-project-operations---lite"></a>Nasadenie aplikácie Project Operations – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_



Project Operations podporuje viac modelov nasadenia. Najlepší model nasadenia nájdete v časti [Typy nasadenia](determine-deployment-type.md).


> [!IMPORTANT]
> Toto nasadenie, jednoduché nasadenie – dohoda o fakturácii pro forma, má za následok **Dataverse – iba nasadenie Project Operations**.

- [Nainštalujte Project Operations do nového Dataverse životné prostredie](#new)
- [Nainštalujte do existujúceho Dataverse životné prostredie](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Nainštalujte Project Operations do nového Dataverse životné prostredie

1. Ako [Globálne resp Power Platform správca](/power-platform/admin/global-service-administrators-can-administer-without-license) s licenciou Project Operations vytvorte novú Dataverse prostredie v [Centrum spravovania PowerPlatform](https://admin.powerplatform.com). Uistite sa, že **Vytvorte databázu pre toto prostredie** a **Aplikácie Dynamics 365** sú povolené. Ďalšie informácie nájdete v časti [Vytváranie a správa prostredí v centre spravovania Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Vyberte **Microsoft Dynamics 365 Project Operations** zo zoznamu nasadenia aplikácií Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Nainštalujte operácie projektu do existujúceho Dataverse životné prostredie
1. Uistite sa, že prostredie nebolo nakonfigurované s [duálny zápis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) ako inštalácia potom nainštaluje [Projektové operácie pre scenáre založené na zdrojoch/nezásobe](project-operations-integrated-deployment-overview.md) schopnosti.
2. Ako [Globálny správca alebo správca Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licenciou Project Operations vyhľadajte prostredie v [Centre spravovania PowerPlatform](https://admin.powerplatform.com), kde chcete nainštalovať Project Operations.
3. Nainštalujte **Microsoft Dynamics 365 Project Operations** zo zoznamu nasadenia aplikácií Dynamics 365. Ďalšie informácie nájdete v časti [Správa aplikácií Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
