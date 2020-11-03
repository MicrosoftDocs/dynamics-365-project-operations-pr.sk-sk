---
title: Nastavenie nákladových a predajných sadzieb pre katalógové produkty
description: Táto téma poskytuje informácie o tom, ako nastaviť cenu a sadzby predaja pre položky v katalógu produktov.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084431"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Nastavenie nákladových a predajných sadzieb pre katalógové produkty

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_


Nastavenie cien pre položky katalógu produktov v Dynamics 365 Project Operations je rovnaké ako v Dynamics 365 Sales.

Pretože produkty nie je možné odhadnúť alebo použiť na projektoch v rámci Project Operations, nie je potrebné nastavovať ceny katalógov produktov v cenníkoch projektov pre ponuky a kontrakty.

Ceny katalógov výrobkov by mali byť stanovené v poli **Cena produktu** cenovej ponuky, zmluvy alebo účtu. Nenastavujte ceny katalógov výrobkov v cenníkoch projektov pre tieto entity. Projektové cenníky sú vyhradené pre Project Operations. Existuje obchodná logika pre konkrétnu aplikáciu, ktorá kopíruje cenníky z ponuky do zmluvy. Výsledkom je projektový cenník špecifický pre zmluvu. Operácia kopírovania môže oneskoriť proces vyhrávania cenovej ponuky, ak je cenový zoznam projektu v cenovej ponuke príliš veľký. Cenníky výrobkov sa nekopírujú, aby sa vytvorili vlastné cenníky na zmluvách. To znamená, že cenníky produktov nemajú vplyv na výkonnosť procesu využívania cenovej ponuky.
