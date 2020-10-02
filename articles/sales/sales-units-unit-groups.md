---
title: Jednotky a jednotkové skupiny
description: Táto téma poskytuje informácie o tom, ako vytvoriť jednotky a skupiny jednotiek v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898775"
---
# <a name="units-and-unit-groups"></a>Jednotky a jednotkové skupiny

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Jednotky predstavujú množstvá alebo hodnoty, v ktorých sa produkty alebo služby predávajú. Napríklad ak predávate záhradkárske potreby, možno predať semená v jednotkách balíkoch, debnách alebo paletách. skupina jednotiek je zbierka týchto rôznych jednotiek.

Ak chcete vykonať kroky v tejto téme, uistite sa, že máte priradenú rolu Správca systému alebo Sales Professional Manager či ekvivalentné povolenia.

## <a name="create-a-unit-group"></a>Vytvorenie jednotkovej skupiny

1. Na mape lokality zvoľte možnosť **Jednotky**.
2. Vyberte **Nový** a v dialógovom okne **Vytvoriť skupinu jednotiek** zadajte názov jednotky.
3. V poli **Primárna jednotka** zadajte najnižšiu bežnú jednotku merania, ktorá sa bude využívať pri predaji produktu. Môžete napríklad zadať „kus“ alebo „unca“.
4. Vyberte položku **OK**.

## <a name="add-units-to-a-unit-group"></a>Pridanie jednotiek do jednotkovej skupiny

1. Otvorte jednotkovú skupinu a na karte **Súvisiace** vyberte **Jednotky**. Môžete vidieť, že primárna jednotka je už pridaná.
2. Vyberte **Pridať novú jednotku** a na stránke **Rýchle vytvorenie: Jednotka** v poli **Názov** zadajte názov jednotky.
3. Do poľa **Množstvo** zadajte množstvo, ktoré bude jednotka obsahovať. Ak napríklad krabica obsahuje dva kusy, zadajte hodnotu „2”. 
4. V poli **Základná jednotka** vyberte základnú jednotku, aby ste určili najnižšiu jednotku merania pre jednotku. Môžete napríklad zvoliť „Kus“.
5. Vyberte položku **Uložiť**:
