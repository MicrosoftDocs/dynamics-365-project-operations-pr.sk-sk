---
title: Správne účtovanie na základe konceptných návrhov projektových faktúr
description: Táto téma vysvetľuje, ako upraviť informácie týkajúce sa účtovníctva v návrhu koncepcie faktúry.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251273"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Správne účtovanie na základe konceptných návrhov projektových faktúr

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

*Prevádzkové podrobnosti* pre projektové faktúry vedie projektový manažér na proforma faktúre. Medzi tieto podrobnosti patrí rozhodnutie o hodinách, výdavkoch, materiáloch alebo míľnikoch, ktoré musia byť fakturované, sadzby a uplatnenie záloh a zadržaných súm. Po potvrdení pôvodnej proforma faktúry môžete upraviť prevádzkové podrobnosti vytvorením a potvrdením [opravnej proforma faktúry](../proforma-invoicing/corrective-invoices.md).

*Účtovné údaje* faktúry za projekt sa uchovávajú v dokumente faktúry orientovanej na zákazníka. Tieto podrobnosti zahŕňajú výpočet dane z obratu a finančné dimenzie, ktoré sa vzťahujú na faktúru. Táto téma poskytuje podrobnosti o tom, ako je možné tieto účtovné podrobnosti upraviť v koncepte návrhu faktúry projektu.

## <a name="adjust-sales-tax"></a>Úprava dane z predaja

Predvolené skupiny fakturácie dane z predaja a skupiny dane z predaja položiek je možné upraviť priamo v dokumente návrhu faktúry. Ak chcete upraviť tieto skupiny, stlačte možnosť **Upraviť**, a potom na každom riadku návrhu faktúry za projekt zadajte novú hodnotu do poľa **Skupina dane z predaja** alebo do poľa **Skupina dane z predaja položiek**.

## <a name="adjust-financial-dimensions"></a>Úprava finančných dimenzií

Finančné dimenzie nemožno upravovať priamo na riadku ponuky faktúry za projekt. Namiesto toho postupujte podľa týchto krokov a upravte finančné dimenzie v návrhu projektovej faktúry.

1. Na návrhu faktúry projektu stlačte možnosť **Vymazať všetko** a odstráňte riadky konceptu faktúry projektu.

    > [!NOTE]
    > Tlačidlo **Vymazať všetko** je k dispozícii až po povolení možnosti **Vymazať riadky návrhu faktúry pri používaní Project Operations na scenára na základe zdrojov/nenaskladnenia** v pracovnom priestore **Správa funkcií**.

2. Úprava finančných dimenzií:

    - **Transakcie na účet (míľniky fakturácie):** Prejdite do **Všetky projekty** \> **Spravovať** \> **Transakcie na účet** a vyberte míľnik, ktorý je potrebné upraviť. Potom na karte **Finančné dimenzie** podľa potreby aktualizujte hodnoty.
    - **Časové, nákladové a materiálne transakcie:** Na stránke **Zaúčtované projektové transakcie** stačte možnosť **Upraviť účtovníctvo** a aktualizujte finančné dimenzie.

3. Po dokončení úprav hodnôt finančnej dimenzie prejdite na **Projektový manažment a účtovníctvo** \> **Periodické** \> **Integrácia Project Operations** a stlačte možnosť **Import z pracovnej tabuľky** , čím sa spustí pravidelný proces. Tento proces používa aktualizované hodnoty finančných dimenzií na opätovné vytvorenie riadkov návrhu faktúry projektu. Aktualizované hodnoty sa potom použijú v sekundárnej knihe projektu a hlavnej knihe pri zaúčtovaní faktúry projektu.
