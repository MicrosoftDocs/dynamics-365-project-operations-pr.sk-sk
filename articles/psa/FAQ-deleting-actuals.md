---
title: Prečo nemôžem odstrániť záznamy z entity skutočných hodnôt?
description: Táto téma poskytuje informácie o tom, prečo nie je možné odstrániť záznamy z entity skutočných hodnôt.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127177"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="2c67f-103">Prečo nemôžem odstrániť záznamy z entity Skutočných hodnôt?</span><span class="sxs-lookup"><span data-stu-id="2c67f-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2c67f-104">Project Service Automation (PSA) neumožňuje odstrániť skutočné hodnoty, pretože slúžia ako zdroj pravdy pre transakcie, ktoré majú finančné dôsledky na nadväzujúce systémy, napríklad financie.</span><span class="sxs-lookup"><span data-stu-id="2c67f-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="2c67f-105">Ak by sa mohli odstrániť skutočné hodnoty, môže sa spochybniť integrita transakcií finančného výkazníctva.</span><span class="sxs-lookup"><span data-stu-id="2c67f-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="2c67f-106">Ak chcete vytvoriť auditový záznam, zákazníci by mali používať účtovné denníky na vytvorenie náhradných transakcií.</span><span class="sxs-lookup"><span data-stu-id="2c67f-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

