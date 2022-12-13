---
title: Nasaďte Project Operations Lite
description: Tento článok poskytuje informácie o tom, ako nainštalovať jednoduché nasadenie Project Operations – dohoda o fakturácii pro forma.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810998"
---
# <a name="deploy-project-operations-lite"></a>Nasaďte Project Operations Lite

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_



Project Operations podporuje viac modelov nasadenia. Najlepší model nasadenia nájdete v časti [Typy nasadenia](determine-deployment-type.md).


> [!IMPORTANT]
> Toto nasadenie, jednoduché nasadenie – dohoda o fakturácii pro forma, má za následok **Dataverse – iba nasadenie Project Operations**.

- [Inštalácia Project Operations do nového prostredia Dataverse](#new)
- [Inštalácia do existujúceho prostredia Dataverse](#existing)
- [Nainštalujte do existujúceho Dataverse prostredia, ktoré obsahuje komponenty s duálnym zápisom](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Nainštalujte Project Operations Lite do nového Dataverse prostredia

1. Ako [Globálny správca alebo správca Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licenciou na Project Operations vytvorte nové prostredie Dataverse v [centre spravovania PowerPlatform](https://admin.powerplatform.com). Uistite sa, že **Vytvoriť databázu pre toto prostredie** a **Aplikácie Dynamics 365** sú povolené. Ďalšie informácie nájdete v časti [Vytváranie a správa prostredí v centre spravovania Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Vyberte **Microsoft Dynamics 365 Project Operations** zo zoznamu nasadenia aplikácií Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Nainštalujte Project Operations Lite do existujúceho Dataverse prostredia 
1. Ako [Globálny správca alebo správca Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licenciou Project Operations vyhľadajte prostredie v [Centre spravovania PowerPlatform](https://admin.powerplatform.com), kde chcete nainštalovať Project Operations.
1. Nainštalujte **Microsoft Dynamics 365 Project Operations** zo zoznamu nasadenia aplikácií Dynamics 365. Ďalšie informácie nájdete v časti [Správa aplikácií Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Nainštalujte Project Operations Lite do existujúceho Dataverse prostredia, kde už existujú riešenia duálneho zápisu

Ak chcete pokračovať v prevádzke Project Operations v režime Lite Deployment, mali by ste postupovať podľa týchto krokov:

1. Ako [Globálny správca alebo správca Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licenciou Project Operations vyhľadajte prostredie v [Centre spravovania PowerPlatform](https://admin.powerplatform.com), kde chcete nainštalovať Project Operations.
1. Nainštalujte **Microsoft Dynamics 365 Project Operations** zo zoznamu nasadenia aplikácií Dynamics 365. Ďalšie informácie nájdete v časti [Správa aplikácií Dynamics 365](/power-platform/admin/manage-apps).
1. Keďže vaše prostredie má nainštalované komponenty Dual write, ktoré pomáhajú s integráciou s finančnými a prevádzkovými aplikáciami, inštalácia Project Operations nainštaluje aj možnosti a rozšírenia potrebné na integráciu údajov súvisiacich s Projectom do finančných a prevádzkových aplikácií. Keďže chcete spustiť Project Operations v nasadení Lite, tieto integračné komponenty by sa mali odstrániť, pretože budú vytvárať obmedzenia a režijné náklady pre scenáre nasadenia Lite. Ručne odinštalujte riešenia **Dynamics 365 Project Operations Dual Write** a **Dynamics 365 Project Operations Dual Write Entity Maps** a odstráňte tieto komponenty.
1. Prejdite na **Operácie projektu -> Nastavenia -> Parametre**. Otvorte stránku **Parametre projektu** a nastavte pole **Správanie pri aktualizácii riešenia** na **Lite Iba**. To zaisťuje, že žiadne následné inovácie Project Operations nevrátia integračné komponenty späť do Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
