---
title: Nastavenie udržania dodávateľov
description: Táto téma vysvetľuje, ako nastaviť udržanie dodávateľa.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583723"
---
# <a name="set-up-vendor-retention"></a>Nastavenie udržania dodávateľov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma poskytuje informácie, ako nastaviť udržanie dodávateľa.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Nastavte si účet udržania dodávateľa v hlavnej knihe

1. V Dynamics 365 Finance prejdite na **Hlavná kniha** > **Nastavenie odosielania** > **Účty pre automatické transakcie**.
2. Pridajte nový riadok.
3. V poli **Typ účtovania** vyberte **Udržanie dodávateľa**.
4. Vyberte hlavný účet pre účtovanie udržania dodávateľa.

## <a name="create-vendor-retention-terms"></a>Vytvorte podmienky udržania dodávateľov

Použite stránku **Podmienky uchovávania dodávateľa** na nastavenie a zachovanie podmienok uchovávania platieb dodávateľom. Zadajte percentuálny podiel platby dodávateľa, ktorý sa má ponechať, a percento predtým udržaných súm, ktoré sa majú uvoľniť. Čiastky sa automaticky uchovávajú na faktúrach dodávateľov, kým zmluva nedosiahne určený stav dokončenia. Keď sú pre dodávateľa stanovené podmienky uchovávania, môžete ich použiť na akýkoľvek projekt, na ktorom predajca pracuje.

1. V časti Finance prejdite na **Projektový manažment a účtovníctvo** > **Nastaviť** > **Uchovávanie** > **Podmienky uchovávania platieb dodávateľom**.
2. Vyberte **Nový** na pridanie nových podmienok uchovania pre dodávateľa. Hodnota v poli **ID pravidla** pre nový výraz sa zadá automaticky. 
3. V poli **Opis** zadajte popisný názov pre nové pravidlo.
4. Na karte **Podmienky** vyberte **Pridať riadok** a zadajte pravidlo uchovania dodávateľa.
5. V poli **Percento dodaných jednotiek** zadajte percento dokončenia pravidla. Čiastky sa automaticky uchovávajú na faktúrach dodávateľov, kým sa fáza dokončenia projektu nerovná percentuálnemu podielu, ktorý zadáte. Napríklad, ak zadáte 50,00, sumy sa uchovajú, kým nebude projekt dokončený na 50 percent.
6. V poli **Percento na uchovanie** zadajte percento z čiastky faktúry dodávateľa, ktorá sa má zachovať. Ak napríklad do tohto poľa zadáte 10,00, 10 percent zo sumy na faktúrach dodávateľa sa zachová, kým projekt nedosiahne percento dokončenia, ktoré vyberiete v poli **Percento dodaných jednotiek**.
7. V poli **Percento uvoľnenia** zadajte percentuálny podiel všetkých predtým zadržaných súm, ktoré sa majú uvoľniť na zvolenej úrovni dokončenia projektu.

> [!NOTE]
> Ak máte viac ako jeden míľnik pre rôzne úrovne dokončenia projektu, zadajte pre každé pravidlo uchovávania údajov samostatný riadok termínu uchovania dodávateľa. Každý riadok môže určiť iné percento, ktoré sa má zachovať, a iné percento, ktoré sa má uvoľniť pre každú určenú úroveň dokončenia projektu.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Nastavenie dodávateľskej zmluvy pre projekt

Nastavte podmienky uchovávania dodávateľa, ktoré sa vzťahujú na projekt. Podmienky uchovania dodávateľa sa zobrazia aj na objednávkach, ktoré vytvoríte pre dodávateľa.

1. Vo časti Finance prejdite na **Projektový manažment a účtovníctvo** > **Projekty** > **Všetky projekty**. 
2. Vyberte projekt a na table akcií vyberte **Skupina projektu** > **Dodávateľské zmluvy**.
3. Na st ránke **Dodávateľské zmluvy** pridajte nový riadok.
4. V poli **Kód účtu** vyberte jednu z nasledujúcich možností:
   - **Tabuľka**: Podmienky uchovania dodávateľa sa vzťahujú na jedného dodávateľa.
   - **Skupina**: Podmienky uchovania dodávateľa sa vzťahujú na všetkých dodávateľov v skupine dodávateľov.
   - **Všetky**: Podmienky uchovania dodávateľa sa vzťahujú na všetkých dodávateľov.
5. V poli **Dodávateľ/skupina dodávateľov** vyberte dodávateľa alebo skupinu dodávateľov, na ktorých sa vzťahujú podmienky uchovania dodávateľa. Ak ste vybrali **Všetky** v predchádzajúcom kroku nie je toto pole k dispozícii.
6. V poli **Podmienky uchovávania dodávateľa** vyberte ID pravidla pre podmienky uchovávania, ktoré sa majú vzťahovať na tohto dodávateľa.

