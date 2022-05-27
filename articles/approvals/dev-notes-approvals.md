---
title: Poznámky vývojára týkajúce sa schválení
description: Táto téma poskytuje ďalšie informácie vývojárov o práci so schváleniami.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579739"
---
# <a name="developer-notes-for-approvals"></a>Poznámky vývojára týkajúce sa schválení

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations obsahuje logiku overovania, ktorá zaisťuje správny prechod záznamu cez fázy schvaľovania. Správne prechody záznamov zabezpečujú: 

  - Všetky podporné riadky sa vytvárajú v súvisiacich tabuľkách, ako sú napríklad denníky a skutočné údaje.
  - Schvaľovateľ je označený ako **Schvaľovateľ projektu** pred pokračovaním v projekte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]