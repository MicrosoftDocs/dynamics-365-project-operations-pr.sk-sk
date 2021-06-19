---
title: Definovanie kalendárov zdrojov
description: Táto téma poskytuje informácie o tom, ako definovať kalendáre pracovnej doby pre zdroje v Project Operations.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5ac834e16afc2f559bee6e10434f7015e8a8e51f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012200"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="6c463-103">Definovanie kalendárov zdrojov</span><span class="sxs-lookup"><span data-stu-id="6c463-103">Define resource calendars</span></span>

<span data-ttu-id="6c463-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="6c463-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6c463-105">Každý rezervovateľný zdroj pracujúci na projekte musí mať kalendár pracovnej doby na definovanie jeho dostupnosti.</span><span class="sxs-lookup"><span data-stu-id="6c463-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="6c463-106">Pracovnú dobu zdroja je možné definovať dvoma spôsobmi:</span><span class="sxs-lookup"><span data-stu-id="6c463-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="6c463-107">Definovanie individuálnych pravidiel kalendára pre zdroj</span><span class="sxs-lookup"><span data-stu-id="6c463-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="6c463-108">Použitie existujúcej šablóny kalendára pre zdroj</span><span class="sxs-lookup"><span data-stu-id="6c463-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="6c463-109">Definovanie pracovnej doby zdroja</span><span class="sxs-lookup"><span data-stu-id="6c463-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="6c463-110">V ponuke **Zdroje** vyberte možnosť **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="6c463-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="6c463-111">V zobrazení mriežky vyberte príslušný **Rezervovateľný zdroj**.</span><span class="sxs-lookup"><span data-stu-id="6c463-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="6c463-112">Na stránke **Podrobnosti o zdroji** vyberte kartu **Pracovná doba**. V predvolenom nastavení je v kalendári rezervovateľných zdrojov predvolená pracovná doba predvolenej šablóny pracovnej doby, ktorá je definovaná pre organizáciu.</span><span class="sxs-lookup"><span data-stu-id="6c463-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="6c463-113">Ak chcete aktualizovať pracovnú dobu, kliknite pravým tlačidlom myši na dátum začiatku navrhovaného pravidla kalendára, ktoré sa má definovať.</span><span class="sxs-lookup"><span data-stu-id="6c463-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="6c463-114">Pomocou ponuky pravidiel kalendára môžete definovať pravidlo kalendára pre konkrétny deň, zvyšok radu alebo celý kalendár.</span><span class="sxs-lookup"><span data-stu-id="6c463-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="6c463-115">Po výbere možnosti môžete definovať:</span><span class="sxs-lookup"><span data-stu-id="6c463-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="6c463-116">Deň v týždni, v ktorom bude platiť pracovná doba.</span><span class="sxs-lookup"><span data-stu-id="6c463-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="6c463-117">Pracovný čas v rámci každého dňa.</span><span class="sxs-lookup"><span data-stu-id="6c463-117">The working times within each day.</span></span>
    - <span data-ttu-id="6c463-118">Časové pásmo pre pravidlo kalendára.</span><span class="sxs-lookup"><span data-stu-id="6c463-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="6c463-119">Ak je to relevantné, pre pravidlo možno určiť aj mimopracovný čas.</span><span class="sxs-lookup"><span data-stu-id="6c463-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="6c463-120">Použitie šablóny kalendára na zdroj</span><span class="sxs-lookup"><span data-stu-id="6c463-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="6c463-121">V ponuke **Zdroje** vyberte možnosť **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="6c463-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="6c463-122">V zobrazení mriežky vyberte až 25 **Rezervovateľných zdrojov**, ktoré sa majú aktualizovať.</span><span class="sxs-lookup"><span data-stu-id="6c463-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="6c463-123">Vyberte možnosť **Nastaviť kalendár** a zobrazí sa dialógové okno so zoznamom dostupných šablón pracovnej doby.</span><span class="sxs-lookup"><span data-stu-id="6c463-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="6c463-124">Vyberte šablónu, ktorú chcete použiť, a potom vyberte **Použiť**.</span><span class="sxs-lookup"><span data-stu-id="6c463-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]