---
title: Prehľad priznania výnosov
description: Táto téma poskytuje informácie o priznaní výnosov v aplikácii Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278887"
---
# <a name="revenue-recognition-overview"></a>Prehľad priznania výnosov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

V Dynamics 365 Project Operations sa princípy priznania výnosov líšia v závislosti od zvolenej metódy fakturácie pre projekt alebo časť projektu. Táto téma poskytuje informácie o priznaní výnosov v aplikácii Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transakcie účtované použitím spôsobu fakturácie času a materiálu

- Priznanie nákladov a výnosov je prepojené. Transakčné náklady a nefakturované predaje sa zaúčtujú pomocou [Denník integrácie Project Operations](../project-accounting/project-operations-integration-journal.md).
- Profil nákladov a výnosov projektu určuje, či sa nevyfakturované predajné transakcie zaúčtujú do hlavnej účtovnej knihy. Ak je vybraná možnosť **Prírastok príjmu**, systém používa pri zaúčtovaní účty **Hodnota predaja WIP** a **Hodnota prírastkov predajných výnosov**. Nasleduje príklad tejto metódy.  

  | Typ transakcie | Debet/Kredit | Množstvo |
  | --- | --- | --- |
  | Hodnota predaja WIP | Debet | 100 |
  | Hodnota prírastkov predajných výnosov | Kredit | 100 |

- Výnos sa rozpoznáva počas fakturácie. Systém používa účet **Fakturovaný výnos** počas zaúčtovania. Nasleduje príklad tejto metódy.  

  | Typ transakcie | Debet/Kredit | Množstvo |
  | --- | --- | --- |
  | Zostatok zákazníka | Debet | 120 |
  | Splatná daň z predaja | Kredit | 20 |
  | Fakturovaný výnos | Kredit | 100 |

- Ak bol výnos zhromaždený pri zaúčtovaní nevyfakturovaných predajov, systém tieto zhromaždené výnosy pri fakturácii vráti späť.

  | Typ transakcie | Debet/Kredit | Množstvo |
  | --- | --- | --- |
  | Hodnota predaja WIP | Kredit | 100 |
  | Hodnota prírastkov predajných výnosov | Debet | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transakcie účtované použitím spôsobu fakturácie pevnej ceny

- Priznanie nákladov a výnosov je oddelené. Transakčné náklady sa zaúčtujú pomocou [Denníka integrácie Project Operations](../project-accounting/project-operations-integration-journal.md). Nevyfakturované predajné transakcie sa nevytvárajú.
- Výnosy môžu byť uznané počas fakturácie, ak majú projektové náklady a profil výnosov **Zásadu použitú pri výpočtoch dokončenia projektu** nastavenú na **Žiadne WIP**. Túto metódu používajte iba na krátkodobé jednoduché projekty.
- Výnosy možno vykázať pomocou odhadov výnosov s pevnou cenou, buď metódou **Dokončená zmluva** alebo **Vykázanie percentuálneho vykázania výnosov**.

## <a name="additional-resources"></a>Ďalšie zdroje
[Článok Konfigurácia účtovníctva pre fakturovateľné projekty](../project-accounting/configure-accounting-billable-projects.md)

[Projekty odhadov výnosov s pevnou cenou](rev-rec-percentage-completion-method.md)

[Správa odhadov výnosov](rev-rec-completed-contract-method.md)

[Náklady na dokončenie metód](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]