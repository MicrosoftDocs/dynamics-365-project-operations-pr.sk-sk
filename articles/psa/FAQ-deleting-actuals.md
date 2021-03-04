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
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148977"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Prečo nemôžem odstrániť záznamy z entity Skutočných hodnôt?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) neumožňuje odstrániť skutočné hodnoty, pretože slúžia ako zdroj pravdy pre transakcie, ktoré majú finančné dôsledky na nadväzujúce systémy, napríklad financie. Ak by sa mohli odstrániť skutočné hodnoty, môže sa spochybniť integrita transakcií finančného výkazníctva. Ak chcete vytvoriť auditový záznam, zákazníci by mali používať účtovné denníky na vytvorenie náhradných transakcií.

