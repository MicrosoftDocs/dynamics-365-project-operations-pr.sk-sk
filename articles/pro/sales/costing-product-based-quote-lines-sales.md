---
title: Náklady v riadkoch cenových ponúk založených na produkte
description: Táto téma poskytuje informácie o uplatnení obstarávacej ceny na riadok cenovej ponuky založený na produkte.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d21ab159294cac66ffeb8abcf0943b4babd7b360
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118946"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="5c1cd-103">Náklady v riadkoch cenových ponúk založených na produkte</span><span class="sxs-lookup"><span data-stu-id="5c1cd-103">Costing product-based quote lines</span></span>

<span data-ttu-id="5c1cd-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="5c1cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="5c1cd-105">Riadky cenových ponúk založené na produkte v Dynamics 365 Project Operations obsahujú aj pole **Obstarávacia cena**.</span><span class="sxs-lookup"><span data-stu-id="5c1cd-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="5c1cd-106">Toto pole sa používa na sledovanie obstarávacej ceny produktu v riadku cenovej ponuky a na následné výpočty ziskovosti.</span><span class="sxs-lookup"><span data-stu-id="5c1cd-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="5c1cd-107">Keď sa pre katalógový produkt vytvorí riadok cenovej ponuky založenej na produkte, náklad v riadku cenovej ponuky založenej na produkte sa predvolene nastaví podľa poľa **Štandardné náklady** v katalógu produktov.</span><span class="sxs-lookup"><span data-stu-id="5c1cd-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="5c1cd-108">Pole štandardných nákladov v katalógu produktov je nastavené v základnej mene organizácie.</span><span class="sxs-lookup"><span data-stu-id="5c1cd-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="5c1cd-109">Predvolené jednotkové náklady v riadku cenovej ponuky založenej na produkte sa prevedú na predajnú menu v cenovej ponuke.</span><span class="sxs-lookup"><span data-stu-id="5c1cd-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="5c1cd-110">Jednotkový náklad v riadku cenovej ponuky založenej na produkte</span><span class="sxs-lookup"><span data-stu-id="5c1cd-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="5c1cd-111">Účelom jednotkových nákladov v riadku cenovej ponuky založenej na produkte je umožniť rozdielne náklady na produkt pri každom predaji.</span><span class="sxs-lookup"><span data-stu-id="5c1cd-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="5c1cd-112">Toto nie je typický scenár, ale niekedy môže dodávateľ znížiť cenu produktu v závislosti od zákazníka konečného predaja.</span><span class="sxs-lookup"><span data-stu-id="5c1cd-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="5c1cd-113">Napríklad:</span><span class="sxs-lookup"><span data-stu-id="5c1cd-113">For example:</span></span>

<span data-ttu-id="5c1cd-114">Spoločnosť Fabrikam Robotics inštaluje robotické ramená na montážnych linkách spoločnosti A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="5c1cd-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="5c1cd-115">Fabrikam poskytuje inštalačné služby, ale robotické ramená sú získavané od spoločnosti Trey robotics.</span><span class="sxs-lookup"><span data-stu-id="5c1cd-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="5c1cd-116">Ak inštalácia robotických ramien v spoločnosti A Datum Corporation otvorí novú priemyselnú vertikálu pre robotické ramená od spoločnosti Trey, spoločnosť Trey môže poskytnúť spoločnosti Fabrikam špeciálnu zľavu za tento obchod.</span><span class="sxs-lookup"><span data-stu-id="5c1cd-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="5c1cd-117">V takom prípade spoločnosť Fabrikam vytvorí riadok cenovej ponuky založenej na produkte pre spoločnosť Robotic Arms a pre túto cenovú ponuku zadá špeciálne jednotkové náklady.</span><span class="sxs-lookup"><span data-stu-id="5c1cd-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="5c1cd-118">Tieto náklady sa líšia od štandardných nákladov spoločnosti Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="5c1cd-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
