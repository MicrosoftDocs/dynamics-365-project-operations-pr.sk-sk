---
title: Nastavenie nákladových a predajných sadzieb pre katalógové produkty – čiastočné
description: Táto téma poskytuje informácie o tom, ako nastaviť cenu a sadzby predaja pre položky v katalógu produktov.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996050"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Nastavenie nákladových a predajných sadzieb pre katalógové produkty – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_


Nastavenie cien pre položky katalógov produktov v aplikácii Dynamics 365 Project Operations je rovnaké ako v aplikácii Dynamics 365 Sales.

V Project Operations nemožno produkty odhadnúť ani použiť na projektoch, takže ceny katalógov produktov pre ponuky a zmluvy nie je potrebné nastavovať v cenníkoch projektov.

Použite pole **Cena produktu** pre ponuky, zmluvy alebo účet na nastavenie cien katalógu produktov. Nenastavujte ceny katalógu produktov v cenníkoch projektov. Projektové cenníky sú vyhradené pre Project Operations. Obchodná logika pre konkrétnu aplikáciu kopíruje cenníky z cenovej ponuky do zmluvy. Výsledkom je projektový cenník špecifický pre zmluvu. Operácia kopírovania môže oneskoriť proces vyhrávania cenovej ponuky, ak je cenový zoznam projektu v cenovej ponuke príliš veľký. Cenníky výrobkov sa nekopírujú, aby sa vytvorili vlastné cenníky na zmluvách. Keďže nejde o žiadne kopírovanie, nie je ovplyvnená výkonnosť procesu cenovej ponuky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]