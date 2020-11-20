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
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="a80f8-103">Poznámky vývojára týkajúce sa schválení</span><span class="sxs-lookup"><span data-stu-id="a80f8-103">Developer notes for Approvals</span></span>

<span data-ttu-id="a80f8-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="a80f8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a80f8-105">Dynamics 365 Project Operations obsahuje logiku overovania, ktorá zaisťuje správny prechod záznamu cez fázy schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="a80f8-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="a80f8-106">Správne prechody záznamov zabezpečujú:</span><span class="sxs-lookup"><span data-stu-id="a80f8-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="a80f8-107">Všetky podporné riadky sa vytvárajú v súvisiacich tabuľkách, ako sú napríklad denníky a skutočné údaje.</span><span class="sxs-lookup"><span data-stu-id="a80f8-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="a80f8-108">Schvaľovateľ je označený ako **Schvaľovateľ projektu** pred pokračovaním v projekte.</span><span class="sxs-lookup"><span data-stu-id="a80f8-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
