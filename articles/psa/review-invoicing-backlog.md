---
title: Skontrolujte fakturačné oneskorenie projektov a projektových zmlúv
description: Táto téma poskytuje informácie o tom, ako skontrolovať čas, výdavky a backlogy produktu a ako ich označiť ako pripravené na fakturáciu.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150507"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Skontrolujte fakturačné oneskorenie projektov a projektových zmlúv

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ak je transakcia pripravená na vytvorenie a spracovanie faktúry, transakcia by mala byť označená ako **Pripravené na faktúru**. Táto téma popisuje typy transakcií, ktoré je možné vytvoriť.

## <a name="review-the-time-and-material-billing-backlog"></a>Prezrite si backlog fakturácie času a materiálu

Keď je položka času alebo výdavkov predložená a schválená pre projekt, PSA vytvorí skutočný projekt. Ak kombinácia projektu a transakcie triedy sú priradené k riadku zmluvy pre čas a materiály projektu, dve skutočné hodnoty sa vytvoria po schválení položky:

- Skutočné údaje nákladov 
- Nevyfakturované skutočné hodnoty predajov

Neúčtované predajné skutočné hodnoty predstavujú fakturačný backlog a stav fakturácie musí byť nastavený na **Pripravené na faktúru**. Po vytvorení faktúry projektu sa nevyfakturované skutočné hodnoty predajov s označením **Pripravené na fakturáciu** skopírujú ako podrobnosti riadka faktúry.

Ak chcete skontrolovať fakturačné oneskorenie pre čas a materiály, prejdite na **Predaj** \> **Fakturácia** \> **Backlog pre fakturáciu času a materiálu**. Vyberte všetky neúčtované predajné skutočné hodnoty, ktoré sú pripravené na fakturáciu, a potom vyberte položku **Pripravené na faktúru**. Stav fakturácie týchto skutočných hodnôt sa zmení na možnosť **Pripravené na faktúru**.

![Backlog pre fakturáciu času a materiálu](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Backlog pre fakturáciu produktov

V prípade, že projektová zmluva má riadky zmluvy založené na produkte, tieto riadky sa považujú za fakturáciu pri každom vytvorení faktúry pre zmluvu o projekte. Každý produkt, ktorý má riadky zmluvy, ktoré sú označené ako **Pripravené na faktúru**, sa skopíruje do faktúry projektu ako riadky projektových faktúr.

Ak chcete skontrolovať backlog fakturácie pre produkty, prejdite na **Predaj** \> **Fakturácia** \> **Backlog pre fakturáciu produktov**. Zvoľte všetky riadky zmluvy produktovej faktúry, ktoré sú pripravené na fakturáciu a potom stlačte možnosť **Pripravené na faktúru**. Stav fakturácie týchto riadkov sa zmení na možnosť **Pripravené na faktúru**.

![Backlog pre fakturáciu produktov](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Skontrolujte medzníky fakturácie na zmluvách s pevnou cenou

Každý riadok projektovej zmluvy, ktorý má fakturačnú metódu s pevnou cenou, musí definovať čiastkové ciele zmluvy. Tieto míľniky zmluvy možno fakturovať iba vtedy, ak sú označené príznakom **Pripravené na faktúru**. 

Ak chcete skontrolovať fakturačné míľniky, prejdite na ponuku **Predaj** \> **Faktúra** \> **Medzníky pevných cien**. Zvoľte si medzníky, ktoré sú pripravené na fakturáciu a následne stlačte možnosť **Pripravené na faktúru**. Stav fakturácie týchto medzných hodnôt sa zmení na možnosť **Pripravené na faktúru**.

![Medzníky pevných cien](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]