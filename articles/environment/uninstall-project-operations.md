---
title: Odinštalovanie Dynamics 365 Project Operations
description: Táto téma poskytuje informácie o tom ako odinštalovať Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e2600c770477ad32cebb66f33a8ca31502a6da3d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575875"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Odinštalovanie Dynamics 365 Project Operations 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Ak chcete odinštalovať Dynamics 365 Project Operations, musíte mať pridelenú rolu správcu.

1. Prejdite do časti **Nastavenia** > **Riešenia**.

    ![Stránka nastavení.](./media/uninstall-proj-ops-solutions.png)
  
2. Odstráňte riešenia v presnom poradí, v akom sú uvedené v nasledujúcej tabuľke. 

    | Krok | Názov riešenia                                    | Poznámka                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 2 | ProjectOperations_Anchor                           | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 5 | ProjectService                                     | Žiadne ďalšie poznámky.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Žiadne ďalšie poznámky.                                                                         |
    | 7 | ProjectServiceCore                                 | Žiadne ďalšie poznámky.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 9 | FieldServiceCommon                                 | Vyžaduje sa pre duálny zápis pomocou Dynamics 365 Finance alebo Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Vyžaduje sa pre duálny zápis pomocou Dynamics 365 Finance alebo Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Vyžadované pre Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Vyžadované pre Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Vyžadované pre Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Vyžadované pre Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Vyžadované pre Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Vyžadované pre Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Vyžadované pre Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 19 | Dynamics365Notes                                   | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 21 | DualWriteCore                                      | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 23 | Dynamics365AssetManagement                         | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 26 | HCMCommon                                          | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 28 | Účastník                                              | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 29 | Dynamics365Company                                 | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 30 | CurrencyExchangeRates                              | Ak sa nenájde, toto riešenie preskočte.                                                            |
    | 31 | AssetCommon                                        | Ak sa nenájde, toto riešenie preskočte.                                                            |
