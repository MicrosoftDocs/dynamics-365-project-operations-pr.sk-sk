---
title: Nasadenie aplikácie Project Operations – čiastočné
description: Tento článok poskytuje informácie o tom, ako nainštalovať jednoduché nasadenie Project Operations – dohoda o fakturácii pro forma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930337"
---
# <a name="deploy-project-operations---lite"></a>Nasadenie aplikácie Project Operations – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_



Project Operations podporuje viac modelov nasadenia. Najlepší model nasadenia nájdete v časti [Typy nasadenia](determine-deployment-type.md).


> [!IMPORTANT]
> Toto nasadenie, jednoduché nasadenie – dohoda o fakturácii pro forma, má za následok **Dataverse – iba nasadenie Project Operations**.

- [Inštalácia Project Operations do nového prostredia Dataverse](#new)
- [Inštalácia do existujúceho prostredia Dataverse](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Inštalácia Project Operations do nového prostredia Dataverse

1. Ako [Globálny správca alebo správca Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licenciou na Project Operations vytvorte nové prostredie Dataverse v [centre spravovania PowerPlatform](https://admin.powerplatform.com). Uistite sa, že **Vytvoriť databázu pre toto prostredie** a **Aplikácie Dynamics 365** sú povolené. Ďalšie informácie nájdete v časti [Vytváranie a správa prostredí v centre spravovania Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Vyberte **Microsoft Dynamics 365 Project Operations** zo zoznamu nasadenia aplikácií Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Inštalácia Project Operations do existujúceho prostredia Dataverse
1. Uistite sa, že prostredie nebolo nakonfigurované pomocou [duálneho zápisu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), pretože inštalácia potom nainštaluje funkcie [Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách](project-operations-integrated-deployment-overview.md).
2. Ako [Globálny správca alebo správca Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licenciou Project Operations vyhľadajte prostredie v [Centre spravovania PowerPlatform](https://admin.powerplatform.com), kde chcete nainštalovať Project Operations.
3. Nainštalujte **Microsoft Dynamics 365 Project Operations** zo zoznamu nasadenia aplikácií Dynamics 365. Ďalšie informácie nájdete v časti [Správa aplikácií Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
