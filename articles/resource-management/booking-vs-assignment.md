---
title: Rezervácie verzus priradenia
description: Táto téma poskytuje informácie o rozdieloch medzi rezerváciami zdrojov a priradeniami zdrojov.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1906ebd76f5fc66215aa5963242de13206a81668cb4973cccaf5b153514672d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008470"
---
# <a name="bookings-vs-assignments"></a>Rezervácie verzus priradenia

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Rezervácie sú pevné alebo predbežné alokácie zdrojov k projektu. Pevné rezervácie spotrebúvajú kapacitu zdroja. Rezervácie predstavujú organizačné koncepty pre tímy, aby mohli pochopiť, ako sa budú využívať zdroje v rôznych projektoch. Dynamics 365 Project Operations považuje rezervácie za koncept na úrovni projektu. 

Na rozdiel od rezervácií sú priradenia sú priraďovaním zdrojov k projektovým úlohám v pláne projektu. Zdroje môžu byť pomenované alebo všeobecné.  Keď sa požiadavka na zdroj odvodí z priradenia projektovej úlohy, aplikácia Project Operations použije kontúry úsilia priradenia zdrojov na vytvorenie kontúr detailov požiadavky na zdroje. Odkaz na priradenie zdrojov sa však neudržiava. Aktualizácie rezervácií odvodené z požiadavky na zdroje neaktualizujú žiadne priradenia zdrojov.

Súčet rezervácií zdroja sa zvyčajne bude rovnať súčtu priradení zdroja k jednej alebo viacerým úlohám. Project Operations však nepresadzuje túto zmluvu. V zobrazení **Vyrovnanie** zobrazuje Projektový manažér miesta, kde nesúhlasia rezervácie a priradenia.




[!INCLUDE[footer-include](../includes/footer-banner.md)]