---
title: Integrácia projektovej faktúry
description: Táto téma poskytuje informácie o integrácii duálneho zápisu Project Operations pre fakturáciu zákazníkom.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581257"
---
# <a name="project-invoice-integration"></a>Integrácia projektovej faktúry

Táto téma poskytuje informácie o integrácii duálneho zápisu Project Operations pre fakturáciu zákazníkom.

V rámci Project Operations manažér projektu spravuje nevybavené fakturácie projektu a vytvára proforma faktúru pre zákazníka v Microsoft Dataverse. Na základe tejto proforma faktúry účtovník pohľadávky alebo účtovník projektu vytvorí faktúru obrátenú na zákazníka. Integrácia duálneho zápisu zaisťuje, že podrobnosti o proforma faktúre sú synchronizované s aplikáciami Finance and Operations. Po zaúčtovaní faktúry orientovanej na zákazníka systém aktualizuje príslušné skutočnosti projektu v Dataverse s účtovnými podrobnosťami. Nasledujúca grafika poskytuje koncepčný prehľad na vysokej úrovni o tejto integrácii.

   ![Integrácia projektovej faktúry.](./media/DW5Invoicing.png)

Potom, čo projektový manažér potvrdí zálohovú faktúru v Dataverse sa informácie hlavičky proforma faktúry synchronizujú s aplikáciami Finance and Operations pomocou mapy s dvojitým zápisom, **Návrh projektovej faktúry V2 (faktúry)**. Toto je jednosmerná integrácia z Dataverse do aplikácií pre financie a prevádzku. Vytváranie alebo odstraňovanie návrhov faktúr projektu priamo v aplikáciách Finance and Operations nie je podporované.

Potvrdenie faktúry v Dataverse tiež spúšťa obchodnú logiku na vytváranie záznamov týkajúcich sa fakturácie v entite **Skutočné hodnoty**. Tieto záznamy sa synchronizujú s financiami a prevádzkou pomocou mapy s dvojitým zápisom, **Aktuálne informácie o integrácii projektových operácií (msdyn\_ skutočné).** Ďalšie informácie nájdete v časti [Odhady a skutočné hodnoty projektu](resource-dual-write-estimates-actuals.md). 

Riadky návrhov faktúr za projekt sú vytvárané periodickým procesom **Postupné importovanie formulára**. Tento proces je založený na podrobných údajoch o fakturovaných predajoch v tabuľke **Skutočné štádiá**. Viac informácií nájdete v časti [Správa návrhov faktúr projektu](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
