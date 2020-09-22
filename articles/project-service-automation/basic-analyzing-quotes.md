---
title: Analýza projektových cenových ponúk
description: Táto téma poskytuje informácie o analýze projektových cenových ponúk.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755527"
---
# <a name="analysis-of-project-quotes"></a>Analýza projektových cenových ponúk

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analyzuje projektové cenové ponuky na odhad ziskovosti. Analyzuje tiež, ako dobre je cenová ponuka zarovnaná s očakávaniami zákazníkov o dátume doručenia alebo dátume dokončenia a o rozpočte.

## <a name="profitability-analysis"></a>Analýza ziskovosti

Project Service Automation analyzuje ziskovosť pomocou hrubého zisku a upraveného hrubého zisku.

- Hrubý zisk sa vypočítava pomocou nasledujúceho vzorca:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Upravený hrubý zisk sa vypočítava pomocou nasledujúceho vzorca:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Ak sa hodnoty pre hrubý zisk a upravený hrubý zisk líšia širokým rozpätím, veľká časť práce v cenovej ponuke je klasifikovaná ako neúčtovateľná.

## <a name="analysis-of-customer-expectations"></a>Analýza očakávaní zákazníka

Ak zadáte hodnoty pre nasledujúce polia, môžete analyzovať cenové ponuky a generovať grafy pre očakávania zákazníkov týkajúce sa plánu a rozpočtu:

- **Requested delivery date** pole v hlavičke cenovej ponuky.
- Pole **Customer budget** pre každý riadok cenovej ponuky (pre riadky založené na projekte a riadky založené na produkte).

Analýza očakávaní zákazníkov o harmonograme sa vykonáva porovnaním posledného koncového dátumu riadka cenovej ponuky s požadovaným dátumom doručenia vo všetkých riadkoch cenovej ponuky v cenovej ponuke.

Analýza očakávaní zákazníkov o rozpočte sa vykonáva porovnaním súčtu celkového rozpočtu zákazníka s ponúkanou sumou vo všetkých riadkoch cenových ponúk.
