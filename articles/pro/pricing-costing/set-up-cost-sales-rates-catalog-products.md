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
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="e6320-103">Nastavenie nákladových a predajných sadzieb pre katalógové produkty – čiastočné</span><span class="sxs-lookup"><span data-stu-id="e6320-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="e6320-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="e6320-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e6320-105">Nastavenie cien pre položky katalógu produktov v Dynamics 365 Project Operations je rovnaké ako v Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e6320-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="e6320-106">Pretože produkty nie je možné odhadnúť alebo použiť na projektoch v rámci Project Operations, nie je potrebné nastavovať ceny katalógov produktov v cenníkoch projektov pre ponuky a kontrakty.</span><span class="sxs-lookup"><span data-stu-id="e6320-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="e6320-107">Ceny katalógov výrobkov by mali byť stanovené v poli **Cena produktu** cenovej ponuky, zmluvy alebo účtu.</span><span class="sxs-lookup"><span data-stu-id="e6320-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="e6320-108">Nenastavujte ceny katalógov výrobkov v cenníkoch projektov pre tieto entity.</span><span class="sxs-lookup"><span data-stu-id="e6320-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="e6320-109">Projektové cenníky sú vyhradené pre Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e6320-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="e6320-110">Existuje obchodná logika pre konkrétnu aplikáciu, ktorá kopíruje cenníky z ponuky do zmluvy.</span><span class="sxs-lookup"><span data-stu-id="e6320-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="e6320-111">Výsledkom je projektový cenník špecifický pre zmluvu.</span><span class="sxs-lookup"><span data-stu-id="e6320-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="e6320-112">Operácia kopírovania môže oneskoriť proces vyhrávania cenovej ponuky, ak je cenový zoznam projektu v cenovej ponuke príliš veľký.</span><span class="sxs-lookup"><span data-stu-id="e6320-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="e6320-113">Cenníky výrobkov sa nekopírujú, aby sa vytvorili vlastné cenníky na zmluvách.</span><span class="sxs-lookup"><span data-stu-id="e6320-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="e6320-114">To znamená, že cenníky produktov nemajú vplyv na výkonnosť procesu využívania cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e6320-114">This means that product price lists don't impact the performance of the quote win process.</span></span>