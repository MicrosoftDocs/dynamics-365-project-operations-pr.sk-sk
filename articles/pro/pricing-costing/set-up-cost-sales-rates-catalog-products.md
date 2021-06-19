---
title: Nastavenie nákladových a predajných sadzieb pre katalógové produkty – čiastočné
description: Táto téma poskytuje informácie o tom, ako nastaviť cenu a sadzby predaja pre položky v katalógu produktov.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004358"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Nastavenie nákladových a predajných sadzieb pre katalógové produkty – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_


Nastavenie cien pre položky katalógov produktov v aplikácii Dynamics 365 Project Operations je rovnaké ako v aplikácii Dynamics 365 Sales.

V Project Operations nemožno produkty odhadnúť ani použiť na projektoch, takže ceny katalógov produktov pre ponuky a zmluvy nie je potrebné nastavovať v cenníkoch projektov.

Použite pole **Cena produktu** pre ponuky, zmluvy alebo účet na nastavenie cien katalógu produktov. Nenastavujte ceny katalógu produktov v cenníkoch projektov. Projektové cenníky sú vyhradené pre Project Operations. Obchodná logika pre konkrétnu aplikáciu kopíruje cenníky z cenovej ponuky do zmluvy. Výsledkom je projektový cenník špecifický pre zmluvu. Operácia kopírovania môže oneskoriť proces vyhrávania cenovej ponuky, ak je cenový zoznam projektu v cenovej ponuke príliš veľký. Cenníky výrobkov sa nekopírujú, aby sa vytvorili vlastné cenníky na zmluvách. Keďže nejde o žiadne kopírovanie, nie je ovplyvnená výkonnosť procesu cenovej ponuky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]