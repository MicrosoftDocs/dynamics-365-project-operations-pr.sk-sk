---
title: Nastavenie cenníkov
description: Táto téma poskytuje informácie o tom, ako nastaviť cenníka nákladu a predaja.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 000c22944b187b6250f2e982d73020028093fde6
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180211"
---
# <a name="set-up-price-lists"></a><span data-ttu-id="96f3a-103">Nastavenie cenníkov</span><span class="sxs-lookup"><span data-stu-id="96f3a-103">Set up price lists</span></span>

<span data-ttu-id="96f3a-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="96f3a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="96f3a-105">Cenníky v Dynamics 365 Project Operations predstavujú katalóg sadzieb.</span><span class="sxs-lookup"><span data-stu-id="96f3a-105">Price lists in Dynamics 365 Project Operations represent a catalog of rates.</span></span> <span data-ttu-id="96f3a-106">Ceny vyjadrujú náklady, predaj a fakturačné sadzby.</span><span class="sxs-lookup"><span data-stu-id="96f3a-106">The rates express cost, sales, and bill rates.</span></span> <span data-ttu-id="96f3a-107">V závislosti od toho, či cenník vyjadruje nákladové sadzby alebo predajné a fakturačné sadzby, je kontext cenníka **Predaj** alebo **Náklady**.</span><span class="sxs-lookup"><span data-stu-id="96f3a-107">Depending on whether the price list expresses cost rates or sales and bill rates, the context of the price list is **Sales** or **Cost**.</span></span>

<span data-ttu-id="96f3a-108">Nasledujúce rozšírenia sú špecifické pre Project Operations a sú aplikované na cenníky z Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="96f3a-108">The following extensions are specific to Project Operations and are applied to price lists from Dynamics 365 Sales.</span></span>

- <span data-ttu-id="96f3a-109">**Kontext**: Toto pole má podporované hodnoty, **Náklady** a **Predaj**.</span><span class="sxs-lookup"><span data-stu-id="96f3a-109">**Context**: This field has the supported values, **Cost** and **Sales**.</span></span> <span data-ttu-id="96f3a-110">Hodnota **Nákup** nie je podporovaná.</span><span class="sxs-lookup"><span data-stu-id="96f3a-110">The value, **Purchase** is not supported.</span></span> <span data-ttu-id="96f3a-111">Nastavte kontext na **Náklady** a vytvorte cenník nákladov alebo nastavte kontext na **Predaj** pre predajný cenník.</span><span class="sxs-lookup"><span data-stu-id="96f3a-111">Set the context to **Cost** to make a cost price list or set the context to **Sales** for a sales price list.</span></span> <span data-ttu-id="96f3a-112">Cenníky nákladov určujú cenu pre typ nákladov v záznamoch o odhadoch a skutočných hodnotách.</span><span class="sxs-lookup"><span data-stu-id="96f3a-112">Cost price lists resolve the price for the cost type on estimate and actuals records.</span></span> <span data-ttu-id="96f3a-113">Cenníky predajných cien riešia cenu na základe odhadovaných a skutočných záznamov o fakturovaných a fakturovaných typoch predaja.</span><span class="sxs-lookup"><span data-stu-id="96f3a-113">Sales price lists resolve the price on estimated and actual records of unbilled and billed sales types.</span></span>
- <span data-ttu-id="96f3a-114">**Časová jednotka** : Toto je predvolená časová jednotka, pre ktorú je cena nastavená v príslušnej tabuľke **Cena roly** pre tento cenník.</span><span class="sxs-lookup"><span data-stu-id="96f3a-114">**Time Unit**: This is the default unit of time for which the price is set up in the related **Role Price** table for this price List.</span></span>
- <span data-ttu-id="96f3a-115">**Entita cenníka**: Toto skryté pole je v časti Project Operations určené na odlíšenie cenových ponúk, ktoré sú špecifické pre danú ponuku alebo zmluvu, od tých, ktoré sú štandardné a globálne použiteľné.</span><span class="sxs-lookup"><span data-stu-id="96f3a-115">**Price List Entity**: This  hidden field is by Project Operations to differentiate price lists that are quote or contract-specific from those that are standard and globally applicable.</span></span>

## <a name="price-list-header"></a><span data-ttu-id="96f3a-116">Hlavička cenníka</span><span class="sxs-lookup"><span data-stu-id="96f3a-116">Price list header</span></span>

<span data-ttu-id="96f3a-117">Nasledujúca tabuľka obsahuje polia na karte **Všeobecné**, ktorá je jedinečná pre Project Operations alebo má významné zmeny v správaní z cenníkov v Sales.</span><span class="sxs-lookup"><span data-stu-id="96f3a-117">The following table includes the fields on the **General** tab of a price list that are unique to Project Operations or have significant changes in behavior from price lists in Sales.</span></span>

| <span data-ttu-id="96f3a-118">Pole</span><span class="sxs-lookup"><span data-stu-id="96f3a-118">Field</span></span> | <span data-ttu-id="96f3a-119">Miesto</span><span class="sxs-lookup"><span data-stu-id="96f3a-119">Location</span></span> | <span data-ttu-id="96f3a-120">Popis</span><span class="sxs-lookup"><span data-stu-id="96f3a-120">Description</span></span> | <span data-ttu-id="96f3a-121">Nadväzujúci vplyv</span><span class="sxs-lookup"><span data-stu-id="96f3a-121">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="96f3a-122">Meno</span><span class="sxs-lookup"><span data-stu-id="96f3a-122">Name</span></span> | <span data-ttu-id="96f3a-123">Karta **Všeobecné** a formuláre **Rýchle vytvorenie**</span><span class="sxs-lookup"><span data-stu-id="96f3a-123">**General** tab and **Quick Create** forms</span></span> | <span data-ttu-id="96f3a-124">Identita cenníka.</span><span class="sxs-lookup"><span data-stu-id="96f3a-124">The identity of the price list.</span></span> | <span data-ttu-id="96f3a-125">Cenník zobrazuje túto hodnotu na všetkých stránkach so zoznamami a v rozbaľovacích možnostiach.</span><span class="sxs-lookup"><span data-stu-id="96f3a-125">The price list is shown with this value on all list pages and drop-down options.</span></span>|
| <span data-ttu-id="96f3a-126">Kontext</span><span class="sxs-lookup"><span data-stu-id="96f3a-126">Context</span></span> | <span data-ttu-id="96f3a-127">Karta **Všeobecné** a formuláre **Rýchle vytvorenie**</span><span class="sxs-lookup"><span data-stu-id="96f3a-127">**General** tab and **Quick Create** forms</span></span> | <span data-ttu-id="96f3a-128">Toto pole je možné nastaviť na **Náklady** alebo **Predaj**.</span><span class="sxs-lookup"><span data-stu-id="96f3a-128">This field can be set to **Cost** or **Sales**.</span></span> | <span data-ttu-id="96f3a-129">Cenník s kontextom nastaveným na **Náklady** sa používa na vyhľadanie ceny odhadov nákladov a skutočných nákladov.</span><span class="sxs-lookup"><span data-stu-id="96f3a-129">A price list set to **Cost** is used to look up the price for cost estimates and cost actuals.</span></span> <span data-ttu-id="96f3a-130">Cenník s kontextom nastaveným na **Predaj** sa používa na vyhľadanie ceny odhadov predaja a skutočných predajov.</span><span class="sxs-lookup"><span data-stu-id="96f3a-130">A price list set to **Sales** is used to look up the price for sales estimates and sales actuals.</span></span> <span data-ttu-id="96f3a-131">Iba cenníky, ktoré majú nastavený kontext na **Predaj** môžu byť pripojené k cenníkom pre zákazníkov, cenové ponuky projektu a projektové zmluvy.</span><span class="sxs-lookup"><span data-stu-id="96f3a-131">Only price lists that have the context set to **Sales** can be attached to project price lists for customers, project quotes, and project contracts.</span></span> |
| <span data-ttu-id="96f3a-132">Počiatočný dátum</span><span class="sxs-lookup"><span data-stu-id="96f3a-132">Start Date</span></span> | <span data-ttu-id="96f3a-133">Karta **Všeobecné** a formuláre **Rýchle vytvorenie**</span><span class="sxs-lookup"><span data-stu-id="96f3a-133">**General** tab and **Quick Create** forms</span></span> | <span data-ttu-id="96f3a-134">Počiatočný dátum obdobia, v ktorom je cenník platný.</span><span class="sxs-lookup"><span data-stu-id="96f3a-134">The start date of the period in which is price list is effective.</span></span> | <span data-ttu-id="96f3a-135">Toto pole sa spolu s poľom **Dátum ukončenia** používa na určenie, ktorý cenník je použiteľný pre určitý odhad alebo riadok skutočnej hodnoty.</span><span class="sxs-lookup"><span data-stu-id="96f3a-135">With the **End Date** field, this field is used to determine which price list is applicable for a certain estimate or actual line.</span></span> |
| <span data-ttu-id="96f3a-136">Konečný dátum</span><span class="sxs-lookup"><span data-stu-id="96f3a-136">End Date</span></span> | <span data-ttu-id="96f3a-137">Karta **Všeobecné** a formuláre **Rýchle vytvorenie**</span><span class="sxs-lookup"><span data-stu-id="96f3a-137">**General** tab and **Quick Create** forms</span></span> | <span data-ttu-id="96f3a-138">Konečný dátum obdobia, v ktorom je cenník platný.</span><span class="sxs-lookup"><span data-stu-id="96f3a-138">The end date of the period in which is price list is effective.</span></span> | <span data-ttu-id="96f3a-139">Toto pole sa spolu s poľom **Dátum začiatku** používa na určenie, ktorý cenník je použiteľný pre určitý odhad alebo riadok skutočnej hodnoty.</span><span class="sxs-lookup"><span data-stu-id="96f3a-139">With the **Start Date** field, this field is used to determine which price list is applicable for a certain estimate or actual line.</span></span> |
| <span data-ttu-id="96f3a-140">Mena</span><span class="sxs-lookup"><span data-stu-id="96f3a-140">Currency</span></span> | <span data-ttu-id="96f3a-141">Karta **Všeobecné** a formuláre **Rýchle vytvorenie**</span><span class="sxs-lookup"><span data-stu-id="96f3a-141">**General** tab and **Quick Create** forms</span></span> | <span data-ttu-id="96f3a-142">Toto pole sa používa na predvolenú menu v každom riadku položky, kategórie alebo cenníka súvisiaceho s týmto cenníkom.</span><span class="sxs-lookup"><span data-stu-id="96f3a-142">This field is used to default the currency on each role, category, or price list item line related to this price list.</span></span> | <span data-ttu-id="96f3a-143">V cenníkoch **Predaj**, roly, kategórie alebo riadky položiek cenníka nemožno vytvoriť v inej mene, ako je táto mena.</span><span class="sxs-lookup"><span data-stu-id="96f3a-143">On **Sales** price lists, roles, categories, or price list item lines can't be created in any currency other than this currency.</span></span> <span data-ttu-id="96f3a-144">V cenníkoch **Náklady**, môžete vytvoriť cenový riadok role v akejkoľvek mene.</span><span class="sxs-lookup"><span data-stu-id="96f3a-144">On **Cost** price lists, you can create a role price line in any currency.</span></span> <span data-ttu-id="96f3a-145">Tu definovaná mena sa používa ako predvolená.</span><span class="sxs-lookup"><span data-stu-id="96f3a-145">The currency defined here is used as a default.</span></span> <span data-ttu-id="96f3a-146">Používateľské nastavenie, ktoré súvisí s cenami rolí, môže túto hodnotu prepísať, aby umožnilo nastavenie sadzby nákladov práce v akejkoľvek mene.</span><span class="sxs-lookup"><span data-stu-id="96f3a-146">The user setup that is related role prices can override this value to enable labor cost rate setup in any currency.</span></span> <span data-ttu-id="96f3a-147">Sadzby ceny kategórie a náklady položky cenníka je možné nastaviť iba v tu definovanej mene.</span><span class="sxs-lookup"><span data-stu-id="96f3a-147">Category cost rates and price list item costs can be set up only in the currency defined here.</span></span> |
| <span data-ttu-id="96f3a-148">Jednotka času</span><span class="sxs-lookup"><span data-stu-id="96f3a-148">Time Unit</span></span> | <span data-ttu-id="96f3a-149">Karta **Všeobecné** a formuláre **Rýchle vytvorenie**</span><span class="sxs-lookup"><span data-stu-id="96f3a-149">**General** tab and **Quick Create** forms</span></span> | <span data-ttu-id="96f3a-150">Toto pole sa používa na predvolenie časovej jednotky v každom riadku položky súvisiacej s týmto cenníkom.</span><span class="sxs-lookup"><span data-stu-id="96f3a-150">This field is used to default the time unit on each role line related to this price list.</span></span> | <span data-ttu-id="96f3a-151">Hodnota tohto poľa sa používa iba pri nastavení ceny súvisiacej roly.</span><span class="sxs-lookup"><span data-stu-id="96f3a-151">This field value is only used on related role price setup.</span></span> <span data-ttu-id="96f3a-152">V cenníkoch **Náklady** a **Predaj**, môžete vytvoriť cenový riadok role v akejkoľvek časovej jednotke.</span><span class="sxs-lookup"><span data-stu-id="96f3a-152">On **Cost** and **Sales** price lists, you can create a role price line in any unit of time.</span></span> <span data-ttu-id="96f3a-153">Tu definovaná časová jednotka sa používa ako predvolená.</span><span class="sxs-lookup"><span data-stu-id="96f3a-153">The time unit defined here is used as a default.</span></span> <span data-ttu-id="96f3a-154">Používateľské nastavenie, ktoré súvisí s cenami rolí, môže túto hodnotu prepísať, aby umožnilo nastavenie sadzby nákladov práce a sadzby fakturácie v akejkoľvek časovej jednotke.</span><span class="sxs-lookup"><span data-stu-id="96f3a-154">The user setup related role prices can override this value to enable labor cost and bill rate setup in any unit of time.</span></span> |
| <span data-ttu-id="96f3a-155">Popis</span><span class="sxs-lookup"><span data-stu-id="96f3a-155">Description</span></span> | <span data-ttu-id="96f3a-156">Karta **Všeobecné** a formuláre **Rýchle vytvorenie**</span><span class="sxs-lookup"><span data-stu-id="96f3a-156">**General** tab and **Quick Create** forms</span></span> | <span data-ttu-id="96f3a-157">Toto je textové pole a umožňuje použiť viacriadkový popis cenníka.</span><span class="sxs-lookup"><span data-stu-id="96f3a-157">This text field allows you to provide a multi-line description of the price list.</span></span> | <span data-ttu-id="96f3a-158">Toto pole sa zobrazuje v zobrazeniach **Priradené** pre cenník v rôznych entitách, ktoré majú súvisiace cenníky.</span><span class="sxs-lookup"><span data-stu-id="96f3a-158">This field is shown in the **Associated** views on the price list in various entities that have related price lists.</span></span> |