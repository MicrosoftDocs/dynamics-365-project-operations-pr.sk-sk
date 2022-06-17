---
title: Nasadenie aplikácie Project Operations – čiastočné
description: Tento článok poskytuje informácie o tom, ako nainštalovať nasadenie Project Operations lite – dohoda o proforma fakturácii.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930337"
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
1. Uistite sa, že prostredie nebolo nakonfigurované s [duálny zápis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) ako inštalácia potom nainštaluje [Projektové operácie pre scenáre založené na zdrojoch/nezásobách](project-operations-integrated-deployment-overview.md) schopnosti.
2. Ako [Globálny správca alebo správca Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licenciou Project Operations vyhľadajte prostredie v [Centre spravovania PowerPlatform](https://admin.powerplatform.com), kde chcete nainštalovať Project Operations.
3. Nainštalujte **Microsoft Dynamics 365 Project Operations** zo zoznamu nasadenia aplikácií Dynamics 365. Ďalšie informácie nájdete v časti [Správa aplikácií Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
