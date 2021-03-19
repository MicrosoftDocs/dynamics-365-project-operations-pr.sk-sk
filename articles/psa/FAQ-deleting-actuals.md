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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286087"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Prečo nemôžem odstrániť záznamy z entity Skutočných hodnôt?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) neumožňuje odstrániť skutočné hodnoty, pretože slúžia ako zdroj pravdy pre transakcie, ktoré majú finančné dôsledky na nadväzujúce systémy, napríklad financie. Ak by sa mohli odstrániť skutočné hodnoty, môže sa spochybniť integrita transakcií finančného výkazníctva. Ak chcete vytvoriť auditový záznam, zákazníci by mali používať účtovné denníky na vytvorenie náhradných transakcií.



[!INCLUDE[footer-include](../includes/footer-banner.md)]