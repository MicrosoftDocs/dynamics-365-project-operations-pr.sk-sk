---
title: Implementujte vlastné polia pre mobilnú aplikáciu Microsoft Dynamics 365 Project Timesheet pre iOS a Android
description: Táto téma poskytuje bežné vzory používania rozšírení na implementáciu vlastných polí.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084418"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="6698b-103">Implementujte vlastné polia pre mobilnú aplikáciu Microsoft Dynamics 365 Project Timesheet pre iOS a Android</span><span class="sxs-lookup"><span data-stu-id="6698b-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6698b-104">Táto téma poskytuje bežné vzory používania rozšírení na implementáciu vlastných polí.</span><span class="sxs-lookup"><span data-stu-id="6698b-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="6698b-105">Pokrývajú sa tieto témy:</span><span class="sxs-lookup"><span data-stu-id="6698b-105">The following topics are covered:</span></span>

- <span data-ttu-id="6698b-106">Rôzne typy údajov, ktoré podporuje rámec vlastného poľa</span><span class="sxs-lookup"><span data-stu-id="6698b-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="6698b-107">Ako zobraziť polia iba na čítanie alebo upraviteľné polia v záznamoch časových výkazov a ukladať hodnoty poskytnuté používateľom späť do databázy</span><span class="sxs-lookup"><span data-stu-id="6698b-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="6698b-108">Ako zobraziť polia iba na čítanie v hlavičke časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="6698b-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="6698b-109">Ako integrovať inú vlastnú obchodnú logiku, aby ste do polí zadali predvolené hodnoty a vykonali ďalšie overenie</span><span class="sxs-lookup"><span data-stu-id="6698b-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="6698b-110">Publikum</span><span class="sxs-lookup"><span data-stu-id="6698b-110">Audience</span></span>

<span data-ttu-id="6698b-111">Táto téma je určená pre vývojárov, ktorí integrujú svoje vlastné polia do mobilnej aplikácie Microsoft Dynamics 365 Project Timesheet, ktorá je k dispozícii pre Apple iOS a Google Android.</span><span class="sxs-lookup"><span data-stu-id="6698b-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="6698b-112">Predpokladom je, že čitatelia sú oboznámení s vývojom X++ a funkciou časových výkazov projektu.</span><span class="sxs-lookup"><span data-stu-id="6698b-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="6698b-113">Zmluva o údajoch - trieda TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="6698b-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="6698b-114">Trieda **TSTimesheetCustomField** je trieda kontraktu údajov X++, ktorá predstavuje informácie o vlastnom poli pre funkčnosť časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="6698b-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="6698b-115">Zoznamy objektov vlastných polí sa odovzdávajú v dátovej zmluve TSTimesheetDetails aj v dátovej zmluve TSTimesheetEntry, aby sa v mobilnej aplikácii zobrazili vlastné polia.</span><span class="sxs-lookup"><span data-stu-id="6698b-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="6698b-116">**TSTimesheetDetails** - Zmluva o hlavičke časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="6698b-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="6698b-117">**TSTimesheetEntry** - Zmluva o transakcii s časovým rozvrhom.</span><span class="sxs-lookup"><span data-stu-id="6698b-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="6698b-118">Skupiny týchto objektov, ktoré majú rovnaké informácie o projekte a **timesheetLineRecId** hodnota predstavuje riadok.</span><span class="sxs-lookup"><span data-stu-id="6698b-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="6698b-119">fieldBaseType (typy)</span><span class="sxs-lookup"><span data-stu-id="6698b-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="6698b-120">Vlastnosť **FieldBaseType** na objekt **TsTimesheetCustom** určuje typ poľa, ktoré sa zobrazí v aplikácii.</span><span class="sxs-lookup"><span data-stu-id="6698b-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="6698b-121">Nasledujúce hodnoty **typov** , ktoré sú podporované.</span><span class="sxs-lookup"><span data-stu-id="6698b-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="6698b-122">Typ hodnoty</span><span class="sxs-lookup"><span data-stu-id="6698b-122">Types value</span></span> | <span data-ttu-id="6698b-123">Typ</span><span class="sxs-lookup"><span data-stu-id="6698b-123">Type</span></span>              | <span data-ttu-id="6698b-124">Poznámky</span><span class="sxs-lookup"><span data-stu-id="6698b-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="6698b-125">0</span><span class="sxs-lookup"><span data-stu-id="6698b-125">0</span></span>           | <span data-ttu-id="6698b-126">Reťazec (a Enum)</span><span class="sxs-lookup"><span data-stu-id="6698b-126">String (and Enum)</span></span> | <span data-ttu-id="6698b-127">Pole sa zobrazuje ako textové pole.</span><span class="sxs-lookup"><span data-stu-id="6698b-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="6698b-128">1</span><span class="sxs-lookup"><span data-stu-id="6698b-128">1</span></span>           | <span data-ttu-id="6698b-129">Integer</span><span class="sxs-lookup"><span data-stu-id="6698b-129">Integer</span></span>           | <span data-ttu-id="6698b-130">Hodnota sa zobrazuje ako číslo bez desatinných miest.</span><span class="sxs-lookup"><span data-stu-id="6698b-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="6698b-131">2</span><span class="sxs-lookup"><span data-stu-id="6698b-131">2</span></span>           | <span data-ttu-id="6698b-132">Reálne číslo</span><span class="sxs-lookup"><span data-stu-id="6698b-132">Real</span></span>              | <span data-ttu-id="6698b-133">Hodnota sa zobrazuje ako číslo s desatinnými miestami.</span><span class="sxs-lookup"><span data-stu-id="6698b-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="6698b-134">Skutočnú hodnotu meny v aplikácii zobrazíte pomocou vlastnosti **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="6698b-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="6698b-135">Môžete použiť vlastnosť **numberOfDecimals** a nastaviť počet desatinných miest, ktoré sa zobrazia.</span><span class="sxs-lookup"><span data-stu-id="6698b-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="6698b-136">3</span><span class="sxs-lookup"><span data-stu-id="6698b-136">3</span></span>           | <span data-ttu-id="6698b-137">Dátum</span><span class="sxs-lookup"><span data-stu-id="6698b-137">Date</span></span>              | <span data-ttu-id="6698b-138">Formáty dátumu sú určené používateľom nastavením **Formát dátumu, času a čísla** , ktoré je uvedené v **Preferencie jazyka a krajiny/regiónu** v časti **Možnosti používateľa**.</span><span class="sxs-lookup"><span data-stu-id="6698b-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="6698b-139">4</span><span class="sxs-lookup"><span data-stu-id="6698b-139">4</span></span>           | <span data-ttu-id="6698b-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="6698b-140">Boolean</span></span>           | |
| <span data-ttu-id="6698b-141">15</span><span class="sxs-lookup"><span data-stu-id="6698b-141">15</span></span>          | <span data-ttu-id="6698b-142">GUID</span><span class="sxs-lookup"><span data-stu-id="6698b-142">GUID</span></span>              | |
| <span data-ttu-id="6698b-143">16</span><span class="sxs-lookup"><span data-stu-id="6698b-143">16</span></span>          | <span data-ttu-id="6698b-144">Int64</span><span class="sxs-lookup"><span data-stu-id="6698b-144">Int64</span></span>             | |

- <span data-ttu-id="6698b-145">Ak vlastnosť **stringOptions** nie je poskytovaná v objekte **TSTimesheetCustomField** je používateľovi poskytnuté pole s voľným textom.</span><span class="sxs-lookup"><span data-stu-id="6698b-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="6698b-146">Vlastnosť **stringLength** sa dá použiť na nastavenie maximálnej dĺžky reťazca, ktorú môžu používatelia zadať.</span><span class="sxs-lookup"><span data-stu-id="6698b-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="6698b-147">Ak vlastnosť **stringOptions** sa poskytuje v objekte **TSTimesheetCustomField** , tieto prvky zoznamu sú jediné hodnoty, ktoré môžu používatelia vybrať pomocou prepínačov (prepínačov).</span><span class="sxs-lookup"><span data-stu-id="6698b-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="6698b-148">V takom prípade môže pole reťazca slúžiť ako hodnota vymenovania na účely zadania používateľom.</span><span class="sxs-lookup"><span data-stu-id="6698b-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="6698b-149">Ak chcete uložiť hodnotu do databázy ako vymenovanie, ručne namapujte hodnotu reťazca späť na hodnotu vymenovania pred uložením do databázy pomocou reťazca príkazov (pozrite si časť „Použiť reťazec príkazov v triede TSTimesheetEntryService na uloženie záznamu časového výkazu z aplikácie späť do databázy“ ďalej v tejto téme).</span><span class="sxs-lookup"><span data-stu-id="6698b-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="6698b-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="6698b-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="6698b-151">Túto vlastnosť môžete použiť na formátovanie skutočných hodnôt ako meny.</span><span class="sxs-lookup"><span data-stu-id="6698b-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="6698b-152">Tento prístup je použiteľný, iba ak hodnota **fieldBaseType** je **Reálne**.</span><span class="sxs-lookup"><span data-stu-id="6698b-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="6698b-153">**TSCustomFieldExtendedType:None** – Neaplikuje sa žiadne formátovanie.</span><span class="sxs-lookup"><span data-stu-id="6698b-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="6698b-154">**TSCustomFieldExtendedType::Currency** – Formátovanie hodnoty ako meny.</span><span class="sxs-lookup"><span data-stu-id="6698b-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="6698b-155">Keď je aktívne formátovanie meny, pole **stringValue** možno použiť na odovzdanie kódu meny, ktorý by sa mal zobraziť v aplikácii.</span><span class="sxs-lookup"><span data-stu-id="6698b-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="6698b-156">Hodnota je hodnotou iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="6698b-156">The value is a read-only value.</span></span>

    <span data-ttu-id="6698b-157">Pole **realValue** obsahuje čiastku peňazí, ktorá by sa mali uložiť do databázy.</span><span class="sxs-lookup"><span data-stu-id="6698b-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="6698b-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="6698b-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="6698b-159">Túto vlastnosť môžete použiť na určenie miesta, kde sa má vlastné pole v aplikácii zobraziť.</span><span class="sxs-lookup"><span data-stu-id="6698b-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="6698b-160">**TSCustomFieldSection::Header** – Pole sa zobrazí v sekcii aplikácie **Zobraziť ďalšie podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="6698b-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="6698b-161">Tieto polia sú vždy iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="6698b-161">These fields are always read-only.</span></span>
- <span data-ttu-id="6698b-162">**TSCustomFieldSection::Line** – Toto pole sa zobrazí po všetkých predpripravených riadkových poliach v záznamoch časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="6698b-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="6698b-163">Tieto polia môžu byť upraviteľné alebo iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="6698b-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="6698b-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="6698b-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="6698b-165">Táto vlastnosť identifikuje pole, keď sa hodnoty, ktoré poskytuje aplikácia, uložia späť do databázy.</span><span class="sxs-lookup"><span data-stu-id="6698b-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="6698b-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="6698b-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="6698b-167">Táto vlastnosť identifikuje pole, keď sa hodnoty, ktoré poskytuje aplikácia, uložia späť do databázy.</span><span class="sxs-lookup"><span data-stu-id="6698b-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="6698b-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="6698b-168">isEditable (NoYes)</span></span>

<span data-ttu-id="6698b-169">Nastaviť túto vlastnosť na **Áno** , čím stanovíte, že pole v časti zadania časového rozvrhu by mali používatelia upravovať.</span><span class="sxs-lookup"><span data-stu-id="6698b-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="6698b-170">Nastavte vlastnosť na **Nie** , aby bolo pole iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="6698b-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="6698b-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="6698b-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="6698b-172">Nastavte túto vlastnosť na **Áno** , čím stanovíte, že pole v časti zadania časového rozvrhu musí byť povinné.</span><span class="sxs-lookup"><span data-stu-id="6698b-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="6698b-173">označenie (str)</span><span class="sxs-lookup"><span data-stu-id="6698b-173">label (str)</span></span>

<span data-ttu-id="6698b-174">Táto vlastnosť určuje označenie, ktoré sa zobrazuje vedľa poľa v aplikácii.</span><span class="sxs-lookup"><span data-stu-id="6698b-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="6698b-175">stringOptions (Zoznam reťazcov)</span><span class="sxs-lookup"><span data-stu-id="6698b-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="6698b-176">Táto vlastnosť je použiteľná iba ak je **fieldBaseType** nastavené na **Reťazec**.</span><span class="sxs-lookup"><span data-stu-id="6698b-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="6698b-177">Ak je možnosť **stringOptions** nastavená, hodnoty reťazcov, ktoré sú k dispozícii na výber pomocou prepínačov, sú určené reťazcami v zozname.</span><span class="sxs-lookup"><span data-stu-id="6698b-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="6698b-178">Ak nie sú zadané žiadne reťazce, je povolené zadávanie voľného textu do poľa reťazca (príklad nájdete ďalej v časti „Použite reťazec príkazov v triede TSTimesheetEntryService na uloženie záznamu časového výkazu z aplikácie späť do databázy“.)</span><span class="sxs-lookup"><span data-stu-id="6698b-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="6698b-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="6698b-179">stringLength (int)</span></span>

<span data-ttu-id="6698b-180">Táto vlastnosť určuje maximálnu dĺžku poľa reťazca.</span><span class="sxs-lookup"><span data-stu-id="6698b-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="6698b-181">Je použiteľná iba ak je **fieldBaseType** nastavené na **Reťazec**.</span><span class="sxs-lookup"><span data-stu-id="6698b-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="6698b-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="6698b-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="6698b-183">Táto vlastnosť určuje počet desatinných miest, ktoré sa zobrazujú pre skutočné pole.</span><span class="sxs-lookup"><span data-stu-id="6698b-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="6698b-184">Je použiteľná iba ak je **fieldBaseType** nastavené na **Real**.</span><span class="sxs-lookup"><span data-stu-id="6698b-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="6698b-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="6698b-185">orderSequence (int)</span></span>

<span data-ttu-id="6698b-186">Táto vlastnosť riadi poradie, v ktorom sa vlastné polia zobrazia v aplikácii, keď je zadaných viac ako jedno vlastné pole.</span><span class="sxs-lookup"><span data-stu-id="6698b-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="6698b-187">Najskôr sa zobrazia polia s nižšími číslami.</span><span class="sxs-lookup"><span data-stu-id="6698b-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="6698b-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="6698b-188">booleanValue (boolean)</span></span>

<span data-ttu-id="6698b-189">Pre polia typu **Booleovské** , táto vlastnosť odovzdá boolovskú hodnotu poľa medzi serverom a aplikáciou.</span><span class="sxs-lookup"><span data-stu-id="6698b-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="6698b-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="6698b-190">guidValue (guid)</span></span>

<span data-ttu-id="6698b-191">Pre polia typu **GUID** , táto vlastnosť odovzdá hodnotu GUID poľa medzi serverom a aplikáciou.</span><span class="sxs-lookup"><span data-stu-id="6698b-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="6698b-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="6698b-192">int64Value (int64)</span></span>

<span data-ttu-id="6698b-193">Pre polia typu **Int64** , táto vlastnosť odovzdá Int64 hodnotu poľa medzi serverom a aplikáciou.</span><span class="sxs-lookup"><span data-stu-id="6698b-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="6698b-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="6698b-194">intValue (int)</span></span>

<span data-ttu-id="6698b-195">Pre polia typu **Int** , táto vlastnosť odovzdá Int hodnotu poľa medzi serverom a aplikáciou.</span><span class="sxs-lookup"><span data-stu-id="6698b-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="6698b-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="6698b-196">realValue (real)</span></span>

<span data-ttu-id="6698b-197">Pre polia typu **Real** , táto vlastnosť odovzdá real hodnotu poľa medzi serverom a aplikáciou.</span><span class="sxs-lookup"><span data-stu-id="6698b-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="6698b-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="6698b-198">stringValue (str)</span></span>

<span data-ttu-id="6698b-199">Pre polia typu **Reťazec** , táto vlastnosť odovzdá hodnotu reťazca poľa medzi serverom a aplikáciou.</span><span class="sxs-lookup"><span data-stu-id="6698b-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="6698b-200">Používa sa tiež na polia typu **Real** , ktoré sú naformátované ako mena.</span><span class="sxs-lookup"><span data-stu-id="6698b-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="6698b-201">V prípade týchto polí sa vlastnosť používa na odovzdanie kódu meny do aplikácie.</span><span class="sxs-lookup"><span data-stu-id="6698b-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="6698b-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="6698b-202">dateValue (date)</span></span>

<span data-ttu-id="6698b-203">Pre polia typu **Dátum** , táto vlastnosť odovzdá hodnotu dátumu poľa medzi serverom a aplikáciou.</span><span class="sxs-lookup"><span data-stu-id="6698b-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="6698b-204">Zobraziť a uložiť vlastné pole v časti zadania časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="6698b-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="6698b-205">Nižšie je snímka obrazovky z mobilnej aplikácie vytvorenia záznamu časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="6698b-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="6698b-206">Zobrazuje vopred pripravené polia a vlastné pole v sekcii „Zadávanie času“ s názvom „Testovací reťazec“ s hodnotou enum už nastavenej „Druhej možnosti”.</span><span class="sxs-lookup"><span data-stu-id="6698b-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Vyskúšajte vlastné pole reťazca v aplikácii](media/timesheet-entry.jpg)



<span data-ttu-id="6698b-208">Nižšie je uvedený obrázok obrazovky z mobilnej aplikácie používateľa, ktorý si vybral jednu z možností výčtu dostupných pre vlastné pole „Testovací reťazec“.</span><span class="sxs-lookup"><span data-stu-id="6698b-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="6698b-209">Dve možnosti sú „Prvá možnosť“ a „Druhá možnosť“ zobrazené ako prepínače.</span><span class="sxs-lookup"><span data-stu-id="6698b-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="6698b-210">Druhá možnosť je momentálne vybraná.</span><span class="sxs-lookup"><span data-stu-id="6698b-210">The second option is currently selected.</span></span>

![Prepínače pre vlastné pole Testovací reťazec](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="6698b-212">Rozšírte tabuľku TSTimesheetLine tak, aby mala vlastné pole</span><span class="sxs-lookup"><span data-stu-id="6698b-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="6698b-213">V typických scenároch je pravdepodobné, že údaje pre vlastné pole v časti zadania časového rozvrhu sa uložia do tabuľky TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="6698b-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="6698b-214">Iné tabuľky však možno použiť, ak je možné údaje načítať na základe poskytnutého záznamu TSTimesheetTrans alebo ak nemá konkrétny kontext záznamu (napríklad ak je pole v parametroch projektu nastavené ako iba na čítanie),</span><span class="sxs-lookup"><span data-stu-id="6698b-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="6698b-215">Upozorňujeme, že vlastné polia nemusia mať žiadne sprievodné záznamy databázy.</span><span class="sxs-lookup"><span data-stu-id="6698b-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="6698b-216">Môžu byť dynamicky generované na základe logiky X++.</span><span class="sxs-lookup"><span data-stu-id="6698b-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="6698b-217">Tento prístup môže byť užitočný v scenároch iba na čítanie (príklad dynamicky generovaných vlastných hodnôt polí nájdete v časti „Použiť reťazec príkazov na triede TSTimesheetDetails, metóda buildCustomFieldListForHeader na vyplnenie podrobností časového rozvrhu“.)</span><span class="sxs-lookup"><span data-stu-id="6698b-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="6698b-218">Nižšie je snímka obrazovky z Visual Studio stromu aplikačných objektov.</span><span class="sxs-lookup"><span data-stu-id="6698b-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="6698b-219">Zobrazuje rozšírenie tabuľky TSTimesheetLine s poľom TestLineString pridaným ako vlastné pole.</span><span class="sxs-lookup"><span data-stu-id="6698b-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Riadkový reťazec](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="6698b-221">Použite príkazový riadok v metóde buildCustomFieldList triedy TSTimesheetSettings na zobrazenie poľa v časti zadania časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="6698b-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="6698b-222">Tento kód riadi nastavenia zobrazenia poľa v aplikácii.</span><span class="sxs-lookup"><span data-stu-id="6698b-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="6698b-223">Napríklad ovláda typ poľa, štítok, či je pole povinné a v ktorej časti sa pole zobrazuje.</span><span class="sxs-lookup"><span data-stu-id="6698b-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="6698b-224">Nasledujúci príklad ukazuje pole reťazca pre časové údaje.</span><span class="sxs-lookup"><span data-stu-id="6698b-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="6698b-225">Toto pole má dve možnosti, **Prvá možnosť** a **Druhá možnosť** , ktoré sú k dispozícii prostredníctvom prepínačov.</span><span class="sxs-lookup"><span data-stu-id="6698b-225">This field has two options, **First option** and **Second option** , that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="6698b-226">Pole v aplikácii je spojené s poľom **TestLineString** , ktoré sa pridá do tabuľky TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="6698b-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="6698b-227">Všimnite si použitie metódy **TSTimesheetCustomField::newFromMetatdata()** na zjednodušenie inicializácie vlastností vlastného poľa: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** a **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="6698b-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** , and **numberOfDecimals**.</span></span> <span data-ttu-id="6698b-228">Tieto parametre môžete podľa potreby nastaviť aj manuálne.</span><span class="sxs-lookup"><span data-stu-id="6698b-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="6698b-229">Použite príkazový riadok v metóde buildCustomFieldListForEntry triedy TSTimesheetEntry na zadanie hodnôt v časti zadania časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="6698b-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="6698b-230">Metóda **buildCustomFieldListForEntry** sa používa na zadávanie hodnôt do uložených riadkov časového rozvrhu v mobilnej aplikácii.</span><span class="sxs-lookup"><span data-stu-id="6698b-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="6698b-231">Ako parameter trvá záznam TSTimesheetTrans.</span><span class="sxs-lookup"><span data-stu-id="6698b-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="6698b-232">Polia z tohto záznamu možno použiť na vyplnenie hodnoty vlastného poľa v aplikácii.</span><span class="sxs-lookup"><span data-stu-id="6698b-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="6698b-233">Pomocou reťazca príkazov v triede TSTimesheetEntryService uložíte záznam časového rozvrhu z aplikácie späť do databázy</span><span class="sxs-lookup"><span data-stu-id="6698b-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="6698b-234">Ak chcete uložiť vlastné pole späť do databázy pri bežnom používaní, musíte rozšíriť viac metód:</span><span class="sxs-lookup"><span data-stu-id="6698b-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="6698b-235">Metóda **timesheetLineNeedsUpdating** sa používa na zistenie, či bol záznam linky zmenený používateľom v aplikácii a musí byť uložený do databázy.</span><span class="sxs-lookup"><span data-stu-id="6698b-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="6698b-236">Ak výkon nie je problémom, je možné túto metódu zjednodušiť, aby sa vždy vrátila hodnota **true**.</span><span class="sxs-lookup"><span data-stu-id="6698b-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="6698b-237">Metódy **populateTimesheetLineFromEntryDuringCreate** a **populateTimesheetLineFromEntryDuringUpdate** je možné rozšíriť tak, aby zadávali hodnoty do záznamu databázy TSTimesheetLine z poskytnutého záznamu zmluvy údajov TSTimesheetEntry.</span><span class="sxs-lookup"><span data-stu-id="6698b-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="6698b-238">V nasledujúcom príklade si všimnite, ako sa mapovanie medzi databázovým poľom a vstupným poľom vykonáva ručne pomocou kódu X++.</span><span class="sxs-lookup"><span data-stu-id="6698b-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="6698b-239">Metóda **populateTimesheetWeekFromEntry** môže byť tiež rozšírená, ak vlastné pole, ktoré je namapované na objekt **TSTimesheetEntry** sa musí zapísať späť do databázovej tabuľky TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="6698b-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="6698b-240">Nasledujúci príklad uloží hodnotu **firstOption** alebo **secondOption** , ktorú si používateľ vyberie, do databázy ako nespracovanú hodnotu reťazca.</span><span class="sxs-lookup"><span data-stu-id="6698b-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="6698b-241">Ak je databázové pole poľom typu **enum** , tieto hodnoty je možné manuálne namapovať na hodnotu enum a potom uložiť do poľa enum v databázovej tabuľke.</span><span class="sxs-lookup"><span data-stu-id="6698b-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="6698b-242">Zobraziť a uložiť vlastné pole v časti hlavičky časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="6698b-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="6698b-243">Nižšie je snímka obrazovky z mobilnej aplikácie používateľa prezerajúceho si časový rozvrh.</span><span class="sxs-lookup"><span data-stu-id="6698b-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="6698b-244">V pravom hornom rohu bolo vybrané tlačidlo „Viac informácií“, aby sa zobrazila možnosť „Zobraziť ďalšie podrobnosti“.</span><span class="sxs-lookup"><span data-stu-id="6698b-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Príkaz zobrazenia ďalších podrobností](media/show-more.png)

<span data-ttu-id="6698b-246">Nižšie je snímka obrazovky z mobilnej aplikácie zobrazujúca časť „Viac” časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="6698b-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="6698b-247">Do sekcie hlavičky časového výkazu bolo pridané vlastné pole s názvom „Miera využitia tohto časového rozvrhu (vypočítané vlastné pole)“.</span><span class="sxs-lookup"><span data-stu-id="6698b-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="6698b-248">Vo vlastnom poli je nastavená hodnota iba na čítanie „0,667“.</span><span class="sxs-lookup"><span data-stu-id="6698b-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Časť Viac](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="6698b-250">Rozšírte tabuľku TSTimesheetTable tak, aby mala vlastné pole</span><span class="sxs-lookup"><span data-stu-id="6698b-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="6698b-251">V typických scenároch je pravdepodobné, že údaje pre vlastné pole v časti hlavičky časového rozvrhu sa vytiahnu z tabuľky TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="6698b-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="6698b-252">Iné tabuľky však možno použiť, ak je možné údaje načítať na základe poskytnutého záznamu TSTimesheetTable alebo ak nemá konkrétny kontext záznamu (napríklad ak je pole v parametroch projektu nastavené ako iba na čítanie),</span><span class="sxs-lookup"><span data-stu-id="6698b-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="6698b-253">Upozorňujeme, že vlastné polia nemusia mať žiadne sprievodné záznamy databázy.</span><span class="sxs-lookup"><span data-stu-id="6698b-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="6698b-254">Môžu byť dynamicky generované na základe logiky X++.</span><span class="sxs-lookup"><span data-stu-id="6698b-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="6698b-255">Nasledujúci príklad ukazuje tento prístup.</span><span class="sxs-lookup"><span data-stu-id="6698b-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="6698b-256">Polia v sekcii hlavičky sú v aplikácii vždy iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="6698b-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="6698b-257">Použite príkazový riadok v metóde buildCustomFieldList triedy TSTimesheetSettings na zobrazenie poľa v časti hlavičky</span><span class="sxs-lookup"><span data-stu-id="6698b-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="6698b-258">Tento kód riadi nastavenia zobrazenia poľa v aplikácii.</span><span class="sxs-lookup"><span data-stu-id="6698b-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="6698b-259">Napríklad ovláda typ poľa, štítok, či je pole povinné a v ktorej časti sa pole zobrazuje.</span><span class="sxs-lookup"><span data-stu-id="6698b-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="6698b-260">Nasledujúci príklad ukazuje vypočítanú hodnotu v časti hlavičky v aplikácii.</span><span class="sxs-lookup"><span data-stu-id="6698b-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="6698b-261">Použite príkazový riadok v metóde buildCustomFieldListForHeader triedy TSTimesheetDetails na vyplnenie podrobností v časovom rozvrhu</span><span class="sxs-lookup"><span data-stu-id="6698b-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="6698b-262">Metóda **buildCustomFieldListForHeader** sa používa na vyplnenie podrobností hlavičky časového rozvrhu v mobilnej aplikácii.</span><span class="sxs-lookup"><span data-stu-id="6698b-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="6698b-263">Ako parameter vezme záznam TSTimesheetTable.</span><span class="sxs-lookup"><span data-stu-id="6698b-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="6698b-264">Polia z tohto záznamu možno použiť na vyplnenie hodnoty vlastného poľa v aplikácii.</span><span class="sxs-lookup"><span data-stu-id="6698b-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="6698b-265">Nasledujúci príklad nečíta z databázy žiadne hodnoty.</span><span class="sxs-lookup"><span data-stu-id="6698b-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="6698b-266">Namiesto toho používa logiku X++ na vygenerovanie vypočítanej hodnoty, ktorá sa potom zobrazí v aplikácii.</span><span class="sxs-lookup"><span data-stu-id="6698b-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="6698b-267">Ďalšie možnosti konfigurovateľnosti/rozšíriteľnosti</span><span class="sxs-lookup"><span data-stu-id="6698b-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="6698b-268">Pridáva sa ďalšie overenie aplikácie</span><span class="sxs-lookup"><span data-stu-id="6698b-268">Adding additional validation for the app</span></span>

<span data-ttu-id="6698b-269">Existujúca logika pre funkčnosť časového rozvrhu na úrovni databázy bude stále fungovať podľa očakávaní.</span><span class="sxs-lookup"><span data-stu-id="6698b-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="6698b-270">Môžete prerušiť dokončenie operácií ukladania alebo odosielania a zobraziť konkrétnu chybovú správu **throw error("message to user")** do kódu prostredníctvom reťazca rozšírenia príkazov.</span><span class="sxs-lookup"><span data-stu-id="6698b-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="6698b-271">Tu sú tri príklady užitočných rozšíriteľných metód:</span><span class="sxs-lookup"><span data-stu-id="6698b-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="6698b-272">Ak **validateWrite** v tabuľke TSTimesheetLine vráti hodnotu **false** počas operácie uloženia riadku časového rozvrhu sa v mobilnej aplikácii zobrazí chybové hlásenie.</span><span class="sxs-lookup"><span data-stu-id="6698b-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="6698b-273">Ak **validateSubmit** v tabuľke TSTimesheetTable vráti hodnotu **false** počas operácie odoslania časového rozvrhu sa v aplikácii používateľovi zobrazí chybové hlásenie.</span><span class="sxs-lookup"><span data-stu-id="6698b-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="6698b-274">Logika, ktorá vypĺňa polia (napríklad **Vlastnosť riadku** ) počas metódy **vložiť** v tabuľke TSTimesheetLine bude stále bežať.</span><span class="sxs-lookup"><span data-stu-id="6698b-274">Logic that fills in fields (for example, **Line Property** ) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="6698b-275">Skrytie a označenie vopred pripravených polí ako konfigurácie iba na čítanie</span><span class="sxs-lookup"><span data-stu-id="6698b-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="6698b-276">Z parametrov projektu môžete v mobilnej aplikácii urobiť hotové polia iba na čítanie alebo skryté.</span><span class="sxs-lookup"><span data-stu-id="6698b-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="6698b-277">Nastavte možnosti v časti **Mobilné časové rozvrhy** na karte **Časový rozvrh** stránky **Parametre projektového riadenia a účtovníctva**.</span><span class="sxs-lookup"><span data-stu-id="6698b-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parametre projektu](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="6698b-279">Zmena aktivít, ktoré sú k dispozícii na výber prostredníctvom rozšírení</span><span class="sxs-lookup"><span data-stu-id="6698b-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="6698b-280">Aktivity, ktoré sú k dispozícii na výber pre projekt, sa vypĺňajú cez metódy **getActivitiesForProject()** a **getActivityQuery()** v triede **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="6698b-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="6698b-281">Na zmenu tohto správania môžete použiť reťazec príkazov tak, aby zodpovedal vášmu obchodnému scenáru pre aktivity, ktoré sú k dispozícii na výber pre konkrétny projekt.</span><span class="sxs-lookup"><span data-stu-id="6698b-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="6698b-282">Zadanie predvolenej kategórie projektu do záznamov časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="6698b-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="6698b-283">Zadanie predvolenej kategórie projektu do položiek časového rozvrhu sa vyskytuje na troch úrovniach.</span><span class="sxs-lookup"><span data-stu-id="6698b-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="6698b-284">Pomocou reťazca príkazov môžete rozšíriť správanie na ktorejkoľvek alebo všetkých týchto úrovniach, aby ste dosiahli požadované správanie.</span><span class="sxs-lookup"><span data-stu-id="6698b-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="6698b-285">Používa sa táto hierarchia:</span><span class="sxs-lookup"><span data-stu-id="6698b-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="6698b-286">Aplikácia sa pokúsi vložiť predvolenú kategóriu z prostriedku projektu.</span><span class="sxs-lookup"><span data-stu-id="6698b-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="6698b-287">Táto predvolená kategória je nastavená v metóde **getCurrentUserResource** a **getDelegatedResourcesForCurrentUser** v triede **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="6698b-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="6698b-288">Ak predvolená kategória nie je poskytnutá na úrovni prostriedkov projektu, aplikácia sa ju pokúsi stiahnuť z aktivity projektu.</span><span class="sxs-lookup"><span data-stu-id="6698b-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="6698b-289">Táto predvolená kategória je nastavená v metóde **getActivitiesForProject** v triede **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="6698b-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="6698b-290">Ak predvolená kategória nie je poskytnutá na úrovni aktivity, predvolená kategória sa vezme z parametrov projektu.</span><span class="sxs-lookup"><span data-stu-id="6698b-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="6698b-291">Táto predvolená kategória je nastavená v metóde **getProjectDetailsbyRule** v triede **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="6698b-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
