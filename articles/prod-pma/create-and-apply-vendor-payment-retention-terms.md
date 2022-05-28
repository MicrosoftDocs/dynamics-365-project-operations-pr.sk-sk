---
title: Vytvorenie a aplikovanie podmienok uchovania platieb dodávateľa
description: Táto téma poskytuje informácie o tom, ako nastaviť a udržiavať podmienky uchovania platieb dodávateľa.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3961d18fcd53381ad43a1d3e598ac61652ba9843
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685121"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Vytvorenie a aplikovanie podmienok uchovania platieb dodávateľa

[!include [banner](../includes/banner.md)] 

Nastavenie podmienok uchovania platieb dodávateľa pre projekt je užitočné, keď chce vaša organizácia ponechať časť uskutočnených platieb dodávateľovi. Napríklad, keď chcete zadržať platbu pre dodávateľa, kým dodané produkty nesplnia vaše očakávania. Podmienky uchovania platby dodávateľa je možné určiť pri rokovaniach o dodávateľskej zmluve.

## <a name="create-vendor-payment-retention-terms"></a>Vytvorenie podmienok uchovania platieb dodávateľa

Môžete zadať percento platby dodávateľa na uchovanie a percento predtým uchovaných súm, ktoré sa majú uvoľniť. Čiastky sa automaticky uchovávajú na faktúrach dodávateľov, kým zmluva nedosiahne určený stav dokončenia. Po nastavení podmienok uchovania ich môžete použiť na akýkoľvek projekt pre daného dodávateľa.

Pomocou nasledujúcich krokov môžete nastaviť a udržiavať podmienky uchovania pre platby dodávateľov. 

1. Prejdite do časti **Projektové riadenie a účtovníctvo** > **Uchovanie** > **Podmienky uchovania platby dodávateľa**.
2. Vyberte **Nový** na pridanie nových podmienok uchovania pre dodávateľa. Automaticky sa zadá hodnota **ID pravidla** pre nové podmienky. 
3. Zadajte stručný popis do poľa **Popis** a na rýchlej karte **Podmienky** vyberte možnosť **Pridať riadok** na zadanie hodnoty podmienok pre nasledujúce položky:

   - **Percento dodaných jednotiek** : Zadajte percento dokončenia pre podmienku. Čiastky sa automaticky uchovávajú na faktúrach dodávateľov, kým sa fáza dokončenia projektu nebude rovnať stanovenému percentu. Napríklad, ak zadáte 50,00, sumy sa uchovajú, kým nebude projekt dokončený na 50 percent.
   - **Percento na uchovanie**: Zadajte percento z čiastky faktúry dodávateľa, ktoré sa má uchovať. Napríklad, ak zadáte 10,00, tak sa 10 percent zo sumy na faktúre dodávateľa ponechá, kým projekt nedosiahne percentuálny podiel dokončenia stanovený v poli **Percento dodaných jednotiek**.
   - **Percento na uvoľnenie** : Vyberte **Pridať riadok** na zadanie percenta zo všetkých predtým uchovaných súm, ktoré sa majú uvoľniť pre zvolenú úroveň dokončenia projektu.

> [!NOTE]
> Ak máte viac ako jeden medzník pre rôzne úrovne dokončenia projektu, zadajte samostatný riadok podmienky uchovania pre dodávateľa pre každé pravidlo uchovania. Každý riadok môže určiť iné percento uchovania a iné percento uvoľnenia pre každú určenú úroveň dokončenia projektu.

Po vytvorení podmienok uchovania pre dodávateľa môžete použiť tieto podmienky pre projekt.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Použitie dodávateľských podmienok uchovania pre projekt

1. Prejdite na položku **Projektové riadenie a účtovníctvo** > **Projekty** > **Všetky projekty** a otvorte projekt na stránke so zoznamom projektov.
2. Na karte FastTab **Zmluvy s predajcom** stlačte možnosť **Pridať riadok**.
3. V poli **Kód účtu** vyberte jednu z nasledujúcich možností: 

   - **Tabuľka**: Podmienky uchovania dodávateľa sa vzťahujú na jedného dodávateľa.
   - **Skupina**: Podmienky uchovania dodávateľa sa vzťahujú na všetkých dodávateľov v skupine dodávateľov.
   - **Všetky**: Podmienky uchovania dodávateľa sa vzťahujú na všetkých dodávateľov.

4. V poli **Dodávateľ/skupina dodávateľov** vyberte dodávateľa alebo skupinu dodávateľov, na ktorých sa vzťahujú podmienky uchovania dodávateľa. Ak ste vybrali **Všetky** v predchádzajúcom kroku nie je toto pole k dispozícii.
5. V poli **Podmienky uchovania dodávateľa** vyberte retenčné podmienky, ktoré ste vytvorili v predchádzajúcom postupe.
6. Ak má projekt pre dodávateľa nastavené aj podmienky typu „zaplatiť po zaplatení“ (PWP), zadajte limitnú hodnotu pre projekt do poľa **Percentuálna hodnota prahovej hodnoty PWP**.

Podmienky uchovania dodávateľa sa zobrazia aj na objednávkach, ktoré vytvoríte pre dodávateľa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]