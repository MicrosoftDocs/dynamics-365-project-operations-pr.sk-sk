---
title: Poznámky vývojára týkajúce sa schválení
description: Táto téma poskytuje ďalšie informácie vývojárov o práci so schváleniami.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483967"
---
# <a name="developer-notes-for-approvals"></a>Poznámky vývojára týkajúce sa schválení

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations obsahuje logiku overovania, ktorá zaisťuje správny prechod záznamu cez fázy schvaľovania. Správne prechody záznamov zabezpečujú: 

  - Všetky podporné riadky sa vytvárajú v súvisiacich tabuľkách, ako sú napríklad denníky a skutočné údaje.
  - Schvaľovateľ je označený ako **Schvaľovateľ projektu** pred pokračovaním v projekte.
