---
title: Pridanie nových vlastných formulárov entít (Project Service Automation 2.x)
description: Táto téma poskytuje informácie o pridávaní vlastných formulárov entít pre príležitosti, cenové ponuky, objednávky alebo faktúry v Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 57d4b9aad433af6d3e73369c76f2793f349c6965
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084558"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="7299f-103">Pridanie nových vlastných formulárov entít (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="7299f-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="7299f-104">Typ poľa</span><span class="sxs-lookup"><span data-stu-id="7299f-104">Type field</span></span> 

<span data-ttu-id="7299f-105">Dynamics 365 Project Service Automation spolieha na pole **Typ** ( **msdyn\_ordertype** ) príležitosti, ponuky, objednávky a faktúry entity na rozlišovanie **založené na práci** verzie týchto entít z **založené na položke** a **založené na službách** verzie.</span><span class="sxs-lookup"><span data-stu-id="7299f-105">Dynamics 365 Project Service Automation relies on the **Type** ( **msdyn\_ordertype** ) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="7299f-106">Verzie založené na práci týchto entít spracúva PSA.</span><span class="sxs-lookup"><span data-stu-id="7299f-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="7299f-107">Veľa obchodnej logiky na strane klienta a na strane servera riešenia závisí od **Typ** poľa.</span><span class="sxs-lookup"><span data-stu-id="7299f-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="7299f-108">Preto je dôležité, aby sa pole inicializoval správnou hodnotou pri vytvorení entít.</span><span class="sxs-lookup"><span data-stu-id="7299f-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="7299f-109">Nesprávna hodnota môže spôsobiť nesprávne správanie a určitá obchodná logika nemusí fungovať správne.</span><span class="sxs-lookup"><span data-stu-id="7299f-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="7299f-110">Automatické prepínanie formulárov</span><span class="sxs-lookup"><span data-stu-id="7299f-110">Automatic form switching</span></span>

<span data-ttu-id="7299f-111">Aby sa predišlo možnému poškodeniu údajov a neočakávanému správaniu, ktoré sú spôsobené nesprávnou inicializáciou a úpravou záznamov entity predaja, PSA teraz obsahuje logiku automatického prepínania formulárov v out-of-box formulárov.</span><span class="sxs-lookup"><span data-stu-id="7299f-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="7299f-112">Táto logika posúva používateľov na správny formulár pre prácu s verziou na práci založená alebo akýkoľvek iný typ Príležitosti, Ponuky, Objednávky alebo Faktúry entity.</span><span class="sxs-lookup"><span data-stu-id="7299f-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="7299f-113">Keď používateľ otvorí verziu založenú na práci pre Príležitosti, Ponuky, Objednávky alebo Faktúry entity, formulár sa prepne na **Projektové Informácie**.</span><span class="sxs-lookup"><span data-stu-id="7299f-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="7299f-114">Logika automatického prepínania formulára spolieha na mapovanie medzi **formId** hodnotou a **msdyn\_OrderType** poľom.</span><span class="sxs-lookup"><span data-stu-id="7299f-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="7299f-115">Všetky out-of-box formuláre boli pridané do tohto mapovania.</span><span class="sxs-lookup"><span data-stu-id="7299f-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="7299f-116">Vlastné formuláre však musia byť manuálne pridané, aby uviedli, ktorá verzia entity je určená na spracovanie.</span><span class="sxs-lookup"><span data-stu-id="7299f-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="7299f-117">Toto je založené na **msdyn\_OrderType** poli.</span><span class="sxs-lookup"><span data-stu-id="7299f-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="7299f-118">Ak prepínaniu formulára chýba mapovanie, logika sa prepne na out-of-box formulár, na základe hodnoty, ktorá je uložená v **msdyn\_OrderType** poli entity.</span><span class="sxs-lookup"><span data-stu-id="7299f-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="7299f-119">Pridanie vlastných formulárov a zapnutie logiky prepínania formulárov</span><span class="sxs-lookup"><span data-stu-id="7299f-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="7299f-120">Nasledujúci príklad ukazuje, ako pridať vlastný formulár, **Moje projektové informácie** , takže pracuje s príležitosťami založenými na práci.</span><span class="sxs-lookup"><span data-stu-id="7299f-120">The following example shows how to add a custom form, **My Project Information** , so that it works with work-based opportunities.</span></span> <span data-ttu-id="7299f-121">Rovnaký proces sa používa na pridávanie vlastných formulárov tak, aby pracovali s ponukami, objednávkami a faktúrami.</span><span class="sxs-lookup"><span data-stu-id="7299f-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="7299f-122">Ak chcete vytvoriť vlastnú verziu informačného formulára **Projektové Informácie** , postupujte podľa týchto krokov.</span><span class="sxs-lookup"><span data-stu-id="7299f-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="7299f-123">V entite príležitosť otvorte formulár **Projektové informácie** a uložte kópiu pod názvom **Moje projektové informácie**.</span><span class="sxs-lookup"><span data-stu-id="7299f-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="7299f-124">Otvorte nový formulár a potom vo vlastnostiach, sa uistite, že formulár inicializačné skripty z formulára **Projektové Informácie** sú prítomné.</span><span class="sxs-lookup"><span data-stu-id="7299f-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="7299f-125">Neodstraňujte skripty.</span><span class="sxs-lookup"><span data-stu-id="7299f-125">Don't remove the scripts.</span></span> <span data-ttu-id="7299f-126">V opačnom prípade niektoré údaje môžu byť inicializované nesprávne.</span><span class="sxs-lookup"><span data-stu-id="7299f-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="7299f-127">Skontrolujte, či pole **Typ** ( **msdyn\_OrderType** ) je prítomný vo formulári.</span><span class="sxs-lookup"><span data-stu-id="7299f-127">Verify that the **Type** ( **msdyn\_ordertype** ) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="7299f-128">Neodstraňujte toto pole.</span><span class="sxs-lookup"><span data-stu-id="7299f-128">Don't remove this field.</span></span> <span data-ttu-id="7299f-129">V opačnom prípade inicializácia skriptov zlyhá.</span><span class="sxs-lookup"><span data-stu-id="7299f-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="7299f-130">Vyhľadajte hodnotu **formId** nového formulára.</span><span class="sxs-lookup"><span data-stu-id="7299f-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="7299f-131">Tento krok môžete urobiť dvoma rôznymi spôsobmi:</span><span class="sxs-lookup"><span data-stu-id="7299f-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="7299f-132">Exportujte formulár **Moje informácie o projekte** ako súčasť nespravovaného riešenia a potom vyhľadajte hodnotu **formId** v súbore customization.XML exportovaného riešenia.</span><span class="sxs-lookup"><span data-stu-id="7299f-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="7299f-133">Otvorte formulár **Moje informácie o projekte** v editore formulárov, a potom vyhľadajte globálne jednoznačný identifikátor (GUID) vedľa parametra **fromId** v URL, ako je znázornené na nasledujúcom obrázku.</span><span class="sxs-lookup"><span data-stu-id="7299f-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Hodnota formId nového formulára v URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="7299f-135">Vytvorenie mapovania **msdyn\_ordertype** pre hodnotu **formId** úpravou msdyn\_/salesdocument/PSSalesdocumentcustomFormIds.js webový zdroj.</span><span class="sxs-lookup"><span data-stu-id="7299f-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="7299f-136">Odstráňte kód zo zdroja a nahraďte ho nasledujúcim kódom.</span><span class="sxs-lookup"><span data-stu-id="7299f-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="7299f-137">Uložte a potom zverejnite prispôsobenia.</span><span class="sxs-lookup"><span data-stu-id="7299f-137">Save and then publish the customizations.</span></span>
