---
title: Integrácia projektovej faktúry
description: Táto téma poskytuje informácie o integrácii duálneho zápisu Project Operations pre fakturáciu zákazníkom.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955831"
---
# <a name="project-invoice-integration"></a>Integrácia projektovej faktúry

Táto téma poskytuje informácie o integrácii duálneho zápisu Project Operations pre fakturáciu zákazníkom.

V rámci Project Operations manažér projektu spravuje nevybavené fakturácie projektu a vytvára proforma faktúru pre zákazníka v Microsoft Dataverse. Na základe tejto proforma faktúry účtovník pohľadávky alebo účtovník projektu vytvorí faktúru obrátenú na zákazníka. Integrácia duálneho zápisu zaručuje, že sa synchronizujú podrobnosti proforma faktúry s aplikáciami Finance and Operations. Po zaúčtovaní faktúry orientovanej na zákazníka systém aktualizuje príslušné skutočnosti projektu v Dataverse s účtovnými podrobnosťami. Nasledujúca grafika poskytuje koncepčný prehľad na vysokej úrovni o tejto integrácii.

   ![Integrácia projektovej faktúry](./media/DW5Invoicing.png)

Potom, čo projektový manažér potvrdí proforma faktúru v Dataverse, informácie v hlavičke proforma faktúry sa synchronizujú s aplikáciami Finance and Operations využívajúce mapu tabuľky dvojitého zápisu, **Návrh faktúry projektu V2 (faktúry)**. Toto je jednosmerná integrácia z Dataverse do aplikácií Finance and Operations. Vytváranie alebo mazanie návrhov faktúr projektu priamo v aplikáciách Finance and Operations nie sú podporované.

Potvrdenie faktúry v Dataverse tiež spúšťa obchodnú logiku na vytváranie záznamov týkajúcich sa fakturácie v entite **Skutočné hodnoty**. Tieto záznamy sa synchronizujú s Finance and Operations pomocou mapy tabuľky s dvojitým zápisom, **Skutočné hodnoty integrácie Project Operations (msdyn\_actuals).** Ďalšie informácie nájdete v časti [Odhady a skutočné hodnoty projektu](resource-dual-write-estimates-actuals.md). 

Riadky návrhov faktúr za projekt sú vytvárané periodickým procesom **Postupné importovanie formulára**. Tento proces je založený na podrobných údajoch o fakturovaných predajoch v tabuľke **Skutočné štádiá**. Viac informácií nájdete v časti [Správa návrhov faktúr projektu](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
