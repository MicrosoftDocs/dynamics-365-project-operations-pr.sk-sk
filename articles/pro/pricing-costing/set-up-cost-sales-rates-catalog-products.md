---
title: Nastavenie nákladových a predajných sadzieb pre katalógové produkty – čiastočné
description: Táto téma poskytuje informácie o tom, ako nastaviť cenu a sadzby predaja pre položky v katalógu produktov.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176720"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Nastavenie nákladových a predajných sadzieb pre katalógové produkty – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_


Nastavenie cien pre položky katalógu produktov v Dynamics 365 Project Operations je rovnaké ako v Dynamics 365 Sales.

Pretože produkty nie je možné odhadnúť alebo použiť na projektoch v rámci Project Operations, nie je potrebné nastavovať ceny katalógov produktov v cenníkoch projektov pre ponuky a kontrakty.

Ceny katalógov výrobkov by mali byť stanovené v poli **Cena produktu** cenovej ponuky, zmluvy alebo účtu. Nenastavujte ceny katalógov výrobkov v cenníkoch projektov pre tieto entity. Projektové cenníky sú vyhradené pre Project Operations. Existuje obchodná logika pre konkrétnu aplikáciu, ktorá kopíruje cenníky z ponuky do zmluvy. Výsledkom je projektový cenník špecifický pre zmluvu. Operácia kopírovania môže oneskoriť proces vyhrávania cenovej ponuky, ak je cenový zoznam projektu v cenovej ponuke príliš veľký. Cenníky výrobkov sa nekopírujú, aby sa vytvorili vlastné cenníky na zmluvách. To znamená, že cenníky produktov nemajú vplyv na výkonnosť procesu využívania cenovej ponuky.
