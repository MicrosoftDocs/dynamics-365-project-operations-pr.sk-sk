---
title: Integrácia faktúry dodávateľa
description: Táto téma poskytuje informácie o integrácií faktúr dodávateľa v Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8650eed2230b99b821c1635fdc88252bb65c5583
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591194"
---
# <a name="vendor-invoice-integration"></a>Integrácia faktúry dodávateľa

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Obstarávanie súvisiace s projektom v Dynamics 365 Project Operations možno zaznamenať prechodom na **Záväzky** > **Faktúry** > **Čakajúce faktúry dodávateľa** a pomocou dokumentu faktúry čakajúceho dodávateľa. Viac informácií nájdete v časti [Nákup neskladových materiálov pomocou nespracovanej faktúry dodávateľa](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Pred použitím funkcií popísaných v tejto téme si prečítajte a vykonajte požadované konfigurácie. Viac informácií nájdete v časti [Povoliť neskladované materiály a čakajúce faktúry dodávateľa](../procurement/configure-materials-nonstocked.md).

V Project Operations sa faktúry dodávateľov súvisiace s projektom účtujú pomocou špeciálnych pravidiel účtovania:

- Náklady súvisiace s projektom (vrátane nevratnej dane) sa okamžite neúčtujú na účet nákladov na projekt v hlavnej knihe. Namiesto toho sa náklady zaúčtujú v časti **Účet integrácie obstarávania**. Tento účet je konfigurovaný v časti **Projektový manažment a účtovníctvo** > **Nastavenie** > **Parametre projektového manažmentu a účtovníctva** na karte **Project Operations v Dynamics 365 Customer engagement**.
- Duálny zápis synchronizuje podrobnosti faktúry dodávateľa s Microsoft Dataverse pomocou nasledujúcich tabuľkových máp:

     - **Entita exportu faktúr dodávateľa integrácie Project Operations (msdyn_projectvendorinvoices)**: Táto tabuľková mapa synchronizuje informácie v hlavičke faktúry dodávateľa. Synchronizujú sa iba faktúry dodávateľa s najmenej jedným riadkom, ktorý obsahuje ID projektu Dataverse.
     - **Riadok entity exportu faktúr projektu dodávateľa projektu Project Operations (msdyn_projectvendorinvoices)**: Táto tabuľková mapa synchronizuje informácie v riadku faktúry dodávateľa. Synchronizujú sa iba riadky, ktoré obsahujú ID projektu Dataverse.

     > [!NOTE]
     > Fakturačné údaje dodávateľa v Dataverse nie sú editovateľné.

Vedľajšia kniha daní, vedľajšia kniha dodávateľa a iné finančné účtovania sa pri účtovaní faktúry dodávateľa zaznamenávajú podľa potreby v Dynamics 365 Finance.

![Integrácia faktúr dodávateľov.](media/DW7VendorInvoice.png)

Keď sa záznamy zapisujú do entity **Faktúra dodávateľa** v Dataverse, začína automatizovaný proces schvaľovania záznamov. V prípade potreby je možné stav automatizovaného schvaľovacieho procesu skontrolovať v Dataverse tým, že pôjdete do **Pokročilé nastavenia** > **Systém** > **Systémové úlohy**. Po dokončení schválenia systém vytvorí dôležité záznamy tried transakcií v entite **Skutočné hodnoty**.

Skutočnosti týkajúce sa materiálu sa potom spracujú pomocou mapy tabuľky s dvojitým zápisom **Skutočné hodnoty integrácie Project Operations (msdyn_actuals)**. Ďalšie informácie nájdete v časti [Odhady a skutočné hodnoty projektu](resource-dual-write-estimates-actuals.md).

Periodický proces, **Import z prípravy** vytvára riadky denníka integrácie Project Operations týkajúce sa faktúry dodávateľa. Ofsetový účet je predvolene nastavený na účet integrácie obstarávania. Po zaúčtovaní denníka integrácie sa zostatok na účte vyrovná pre transakciu s faktúrou dodávateľa a čiastka riadku sa presunie na účet nákladov na projekt. Transakcie vedľajšej knihy projektu sa vytvárajú aj na účely následnej fakturácie a vykazovania výnosov.
