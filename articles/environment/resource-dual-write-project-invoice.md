---
title: Integrácia projektovej faktúry
description: Tento článok poskytuje informácie o integrácii duálneho zápisu Project Operations pre fakturáciu zákazníkom.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029043"
---
# <a name="project-invoice-integration"></a>Integrácia projektovej faktúry

Tento článok poskytuje informácie o integrácii duálneho zápisu Project Operations pre fakturáciu zákazníkom.

V rámci Project Operations manažér projektu spravuje nevybavené fakturácie projektu a vytvára proforma faktúru pre zákazníka v Microsoft Dataverse. Na základe tejto proforma faktúry účtovník pohľadávky alebo účtovník projektu vytvorí faktúru obrátenú na zákazníka. Integrácia duálneho zápisu zaručuje, že sa synchronizujú podrobnosti proforma faktúry s aplikáciami na riadenie financií a prevádzok. Po zaúčtovaní faktúry orientovanej na zákazníka systém aktualizuje príslušné skutočnosti projektu v Dataverse s účtovnými podrobnosťami. Nasledujúca grafika poskytuje koncepčný prehľad na vysokej úrovni o tejto integrácii.

   ![Integrácia projektovej faktúry.](./media/DW5Invoicing.png)

Potom, čo projektový manažér potvrdí proforma faktúru v Dataverse, informácie v hlavičke proforma faktúry sa synchronizujú s aplikáciami na riadenie financií a prevádzok využívajúce mapu tabuľky duálneho zápisu, **Návrh faktúry projektu V2 (faktúry)**. Toto je jednosmerná integrácia z Dataverse do aplikácií na riadenie financií a prevádzok. Vytváranie alebo mazanie návrhov faktúr projektu priamo v aplikáciách na riadenie financií a prevádzok nie sú podporované.

Potvrdenie faktúry v Dataverse tiež spúšťa obchodnú logiku na vytváranie záznamov týkajúcich sa fakturácie v entite **Skutočné hodnoty**. Tieto záznamy sa synchronizujú s financiami a operáciami pomocou mapy tabuľky s duálnym zápisom, **Skutočné hodnoty integrácie Project Operations (msdyn\_actuals).** Ďalšie informácie nájdete v časti [Odhady a skutočné hodnoty projektu](resource-dual-write-estimates-actuals.md). 

Riadky návrhov faktúr za projekt sú vytvárané periodickým procesom **Postupné importovanie formulára**. Tento proces je založený na podrobných údajoch o fakturovaných predajoch v tabuľke **Skutočné štádiá**. Viac informácií nájdete v časti [Správa návrhov faktúr projektu](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
