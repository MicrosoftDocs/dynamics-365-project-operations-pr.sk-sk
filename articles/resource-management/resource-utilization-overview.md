---
title: Prehľad využitia zdroja
description: Táto téma poskytuje informácie o zobrazení využitia zdrojov v aplikácii Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367955"
---
# <a name="resource-utilization-overview"></a>Prehľad využitia zdroja

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Zdroje môžu mať cieľové fakturovateľné využitie. Tento cieľ využitia je definovaný ako atribút v predvolenej role zdroja, alebo nastavenie v zázname jednotlivých rezervovateľných zdrojov. Výpočty využitia sú založené na skutočných hodinách, ktoré zdroje hlásili pomocou schválených časových položiek.

Na výpočet využitia sa používajú nasledujúce vzorce:

  - Fakturovateľné využitie = Spoplatnená skutočná kapacita hodín ÷ kapacita zdroja
  - Nefakturovateľné využitie = skutočný čas s fakturáciou typu ID = Nefakturovateľné, doplnkové alebo nie je k dispozícii ÷ zdroj kapacity
  - Interné = skutočný čas bez predajnej zmluvy ÷ kapacita zdrojov
  - Kapacita zdrojov = pracovné hodiny zdroja – mimo pracoviska – dni pracovného času

**Zobrazenie využitia** prostriedkov môžete nájsť na table **Zdroje**.

Každá bunka v mriežke predstavuje percento fakturovateľného využitia prostriedku v období, ako je napríklad deň, týždeň alebo mesiac. Na vyfarbenie buniek sa používajú nasledujúce vzorce:

  - **Zelená**: Fakturovateľné využitie > = Cieľ využívanie zdrojov
  - **Žltá**: Cieľové využitie – 20 < = Fakturovateľná využitie < Cieľové využitie
  - **Červená**: Fakturovateľná využitie < Cieľové využitie – 20

Keďže zobrazenie **Využitie zdroja** je založené na tabuli plánovania, môžete filtrovať výsledky pomocou možností filtrovania tabule plánovania.

Mriežka si vyžaduje, aby ste stanovili cieľové využitie buď roly, alebo individuálneho zdroja. Ak tak chcete urobiť, prejdite na **Zdroje** > **Zdrojové roly**.

Okrem toho musí byť priradená predvolená rola pre každý rezervovateľný prostriedok. Prejdite na **Zdroje** > **Zdroje**. Na karte **Project Service** skontrolujte, či je definovaná rola zdroja a či pole **Je predvolená** je nastavené na **Áno**. Môžete pridať ďalšie roly, kde **Je predvolená** = **Nie**. Rola, kde **Je predvolená** = **Áno** sa používa na vyhodnotenie využitia zdroja proti cieľu pre túto rolu.

Na karte **Project Service** môžete tiež nastaviť individuálne cieľové využitie prostriedku. Výpočet využitia potom použije cieľové využitie na vyhodnotenie cieľového prostriedku namiesto cieľa predvolenej roly prostriedku.

Využitie sa zobrazuje pre zdroj len vtedy, ak tento zdroj schválil účtovateľný čas počas obdobia, ktoré je zobrazené v mriežke.


[!INCLUDE[footer-include](../includes/footer-banner.md)]