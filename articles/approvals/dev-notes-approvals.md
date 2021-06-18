---
title: Poznámky vývojára týkajúce sa schválení
description: Táto téma poskytuje ďalšie informácie vývojárov o práci so schváleniami.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996810"
---
# <a name="developer-notes-for-approvals"></a>Poznámky vývojára týkajúce sa schválení

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations obsahuje logiku overovania, ktorá zaisťuje správny prechod záznamu cez fázy schvaľovania. Správne prechody záznamov zabezpečujú: 

  - Všetky podporné riadky sa vytvárajú v súvisiacich tabuľkách, ako sú napríklad denníky a skutočné údaje.
  - Schvaľovateľ je označený ako **Schvaľovateľ projektu** pred pokračovaním v projekte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]