---
title: Vytvorenie zálohy ad hoc v zmluve
description: Táto téma poskytuje informácie o vytvorení zálohy v zmluve podľa potreby.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 51e3b0ac8e111be70fe6ad0f9c162dfaec3339ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003515"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Vytvorenie zálohy ad hoc v zmluve

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Microsoft Dynamics 365 Project Operations podporuje fakturačné scenáre, ktoré zahŕňajú preddavky a zálohy. Proces používania **Záloh** v **Project Operations** je podobný zmluvám založeným na **Preddavkoch**. 

Podľa nasledujúcich pokynov môžete zákazníkovi fakturovať zálohu.

1. Choďte na stránku **Projektová zmluva** a potom vyberte kartu **Zálohy a preddavky**.
2. Vo vedľajšej mriežke, ktorá obsahuje zoznam všetkých predtým zaznamenaných záloh a preddavkov, vyberte **+ Nový preddavok projektovej zmluvy**. 

    Otvorí sa formulár **Rýchle vytvorenie** na zaznamenanie zálohy alebo preddavku.
    
3. V nasledujúcej tabuľke sú uvedené polia na zaznamenanie zálohy a úvahy, na ktoré treba pamätať pri vytváraní nových:

    | Pole | Popis | Nadväzujúci vplyv |
    | --- | --- | --- |
    | **Zákazník projektovej zmluvy** | Toto pole označuje, ktorému zákazníkovi v zmluve bude fakturovaná táto záloha. | Ak máte v zmluve viac zákazníkov a chcete každému z nich fakturovať konkrétnu zálohu alebo preddavok, vytvorte zálohu pre každého zákazníka osobitne. |
    | **Opis** | Opis účelu alebo načasovania zálohy, ktorý pomáha pri identifikácii tejto zálohy. | Tento opis sa zobrazuje na riadku faktúry pre túto zálohu. |
    | **Suma** | Suma zálohy alebo preddavku. | Táto suma sa zobrazuje na riadku faktúry pre túto zálohu. |
    | **Dátum fakturácie** | Dátum, kedy je tento preddavok fakturovaný zákazníkovi. | Toto je dátum automatizovaného procesu vytvárania faktúry na vytvorenie riadku faktúry pre tento preddavok. |
    | **Stav faktúry** | Toto je nastavenie možnosti, ktoré označuje, či je tento preddavok pridaný do konceptu faktúry pre tohto zákazníka. Možné hodnoty sú:</br>- **Nepripravené na fakturáciu**</br>- **Pripravené na faktúru** | Keď sú záloha alebo preddavok označené ako **Pripravené na fakturáciu**, sú pridané ako čas riadku na koncepte faktúry. Na vyrovnanie s nákladmi na projekt na ďalšie fakturačné obdobie je možné použiť iba plne fakturovaný preddavok. |

4. Vyberte **Uložiť a zavrieť** v dialógovom okne rýchleho vytvorenia na zaznamenanie zálohy alebo preddavku.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]