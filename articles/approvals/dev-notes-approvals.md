---
title: Poznámky vývojára týkajúce sa schválení
description: Tento článok poskytuje ďalšie informácie pre vývojárov o práci so schváleniami.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924771"
---
# <a name="developer-notes-for-approvals"></a>Poznámky vývojára týkajúce sa schválení

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations obsahuje logiku overovania, ktorá zaisťuje správny prechod záznamu cez fázy schvaľovania. Správne prechody záznamov zabezpečujú: 

  - Všetky podporné riadky sa vytvárajú v súvisiacich tabuľkách, ako sú napríklad denníky a skutočné údaje.
  - Schvaľovateľ je označený ako **Schvaľovateľ projektu** pred pokračovaním v projekte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]