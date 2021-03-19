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
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290288"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="48ca4-103">Poznámky vývojára týkajúce sa schválení</span><span class="sxs-lookup"><span data-stu-id="48ca4-103">Developer notes for Approvals</span></span>

<span data-ttu-id="48ca4-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="48ca4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="48ca4-105">Dynamics 365 Project Operations obsahuje logiku overovania, ktorá zaisťuje správny prechod záznamu cez fázy schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="48ca4-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="48ca4-106">Správne prechody záznamov zabezpečujú:</span><span class="sxs-lookup"><span data-stu-id="48ca4-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="48ca4-107">Všetky podporné riadky sa vytvárajú v súvisiacich tabuľkách, ako sú napríklad denníky a skutočné údaje.</span><span class="sxs-lookup"><span data-stu-id="48ca4-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="48ca4-108">Schvaľovateľ je označený ako **Schvaľovateľ projektu** pred pokračovaním v projekte.</span><span class="sxs-lookup"><span data-stu-id="48ca4-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]