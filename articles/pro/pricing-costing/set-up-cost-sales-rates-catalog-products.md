---
title: Nastavenie nákladových a predajných sadzieb pre katalógové produkty – čiastočné
description: Táto téma poskytuje informácie o tom, ako nastaviť cenu a sadzby predaja pre položky v katalógu produktov.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764580"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="ef996-103">Nastavenie nákladových a predajných sadzieb pre katalógové produkty – čiastočné</span><span class="sxs-lookup"><span data-stu-id="ef996-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="ef996-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="ef996-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="ef996-105">Nastavenie cien pre položky katalógov produktov v aplikácii Dynamics 365 Project Operations je rovnaké ako v aplikácii Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="ef996-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="ef996-106">V Project Operations nemožno produkty odhadnúť ani použiť na projektoch, takže ceny katalógov produktov pre ponuky a zmluvy nie je potrebné nastavovať v cenníkoch projektov.</span><span class="sxs-lookup"><span data-stu-id="ef996-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="ef996-107">Použite pole **Cena produktu** pre ponuky, zmluvy alebo účet na nastavenie cien katalógu produktov.</span><span class="sxs-lookup"><span data-stu-id="ef996-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="ef996-108">Nenastavujte ceny katalógu produktov v cenníkoch projektov.</span><span class="sxs-lookup"><span data-stu-id="ef996-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="ef996-109">Projektové cenníky sú vyhradené pre Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ef996-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="ef996-110">Obchodná logika pre konkrétnu aplikáciu kopíruje cenníky z cenovej ponuky do zmluvy.</span><span class="sxs-lookup"><span data-stu-id="ef996-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="ef996-111">Výsledkom je projektový cenník špecifický pre zmluvu.</span><span class="sxs-lookup"><span data-stu-id="ef996-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="ef996-112">Operácia kopírovania môže oneskoriť proces vyhrávania cenovej ponuky, ak je cenový zoznam projektu v cenovej ponuke príliš veľký.</span><span class="sxs-lookup"><span data-stu-id="ef996-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="ef996-113">Cenníky výrobkov sa nekopírujú, aby sa vytvorili vlastné cenníky na zmluvách.</span><span class="sxs-lookup"><span data-stu-id="ef996-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="ef996-114">Keďže nejde o žiadne kopírovanie, nie je ovplyvnená výkonnosť procesu cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="ef996-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
