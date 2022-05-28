---
title: Prehľad spracovania fakturácie
description: Táto téma poskytuje prehľad procesov fakturácie v Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 0328d5321909bcc17754da4e19d7652b77a665d5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582729"
---
# <a name="invoicing-process-overview"></a>Prehľad spracovania fakturácie

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch ponúkajú komplexné možnosti prispôsobené tak, aby vyhovovali potrebám projektového manažéra aj referenta pohľadávok/účtovníka projektu. Pre proces fakturácie riadi projektový manažér nevybavené účty fakturácie projektu a referent pohľadávok/účtovník projektu vytvára vyhovujúci a presný fakturačný dokument orientovaný na zákazníka.

![Vývojový diagram fakturácie.](./media/invoicing-flow.png)

Riadok zmluvy projektu definuje spôsob účtovania pre súvisiace transakcie projektu. Keď projektový manažér schváli časové a nákladové transakcie, systém zaznamená transakcie do **Aktuálne informácie o projekte** subjektu a odošle informácie **Projektový manažment a účtovníctvo** modul v Dynamics 365 Finance. Účtovník projektu potom skontroluje a zaúčtuje záznamy pomocou [Denník integrácie Project Operations](../project-accounting/project-operations-integration-journal.md). Tento denník obsahuje dôležité účtovné podrobnosti o skutočných hodnotách projektu, ako sú fakturácia, skupina dane z obratu, skupina dane z obratu fakturovanej položky a finančné dimenzie.

Projektový manažér môže skontrolovať nevyfakturované predajné transakcie pomocou spôsobu fakturácie času a materiálu v dokumente [Backlog pre fakturáciu času a materiálu](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) a fakturácia pevnej ceny v [Míľniky pevnej ceny](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Tieto zobrazenia vám umožňujú filtrovať a vyberať transakcie, ktoré je potrebné zahrnúť do nasledujúceho fakturačného cyklu, a potom ich označiť ako **Pripravené na fakturáciu**.

Môžete [ručne vytvoriť pro forma faktúru](../proforma-invoicing/create-manual-proforma-invoice.md) alebo použiť [pravidelný proces](../proforma-invoicing/configure-automated-invoice-creation.md). Projektový manažér môže podľa potreby [upraviť návrh pro forma faktúry](../proforma-invoicing/manage-proforma-invoice.md) a potom ho potvrdiť.

Potvrdená pro forma faktúra sa odošle do modulu **Projektové riadenie a účtovníctvo** v aplikácii Finance. Účtovník projektu naformátuje a aktualizuje návrh projektovej faktúry a potom zaúčtuje a vytlačí dokument. Zaúčtované faktúry projektu sa zaznamenávajú v hlavnej knihe, ako aj vo vedľajších účtovných knihách Zákazník a Projekt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]