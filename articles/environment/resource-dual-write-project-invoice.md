---
title: Integrácia projektovej faktúry
description: Tento článok poskytuje informácie o integrácii duálneho zápisu Project Operations pre zákaznícku fakturáciu.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912121"
---
# <a name="project-invoice-integration"></a>Integrácia projektovej faktúry

Tento článok poskytuje informácie o integrácii duálneho zápisu Project Operations pre zákaznícku fakturáciu.

V rámci Project Operations manažér projektu spravuje nevybavené fakturácie projektu a vytvára proforma faktúru pre zákazníka v Microsoft Dataverse. Na základe tejto proforma faktúry účtovník pohľadávky alebo účtovník projektu vytvorí faktúru obrátenú na zákazníka. Integrácia duálneho zápisu zaisťuje, že podrobnosti o proforma faktúre sú synchronizované s aplikáciami Finance and Operations. Po zaúčtovaní faktúry orientovanej na zákazníka systém aktualizuje príslušné skutočnosti projektu v Dataverse s účtovnými podrobnosťami. Nasledujúca grafika poskytuje koncepčný prehľad na vysokej úrovni o tejto integrácii.

   ![Integrácia projektovej faktúry.](./media/DW5Invoicing.png)

Potom, čo projektový manažér potvrdí zálohovú faktúru v Dataverse sa informácie hlavičky proforma faktúry synchronizujú s aplikáciami Finance and Operations pomocou mapy s dvojitým zápisom, **Návrh projektovej faktúry V2 (faktúry)**. Toto je jednosmerná integrácia z Dataverse do aplikácií pre financie a prevádzku. Vytváranie alebo odstraňovanie návrhov faktúr projektu priamo v aplikáciách Finance and Operations nie je podporované.

Potvrdenie faktúry v Dataverse tiež spúšťa obchodnú logiku na vytváranie záznamov týkajúcich sa fakturácie v entite **Skutočné hodnoty**. Tieto záznamy sa synchronizujú s financiami a prevádzkou pomocou mapy s dvojitým zápisom, **Aktuálne informácie o integrácii projektových operácií (msdyn\_ skutočné).** Ďalšie informácie nájdete v časti [Odhady a skutočné hodnoty projektu](resource-dual-write-estimates-actuals.md). 

Riadky návrhov faktúr za projekt sú vytvárané periodickým procesom **Postupné importovanie formulára**. Tento proces je založený na podrobných údajoch o fakturovaných predajoch v tabuľke **Skutočné štádiá**. Viac informácií nájdete v časti [Správa návrhov faktúr projektu](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
