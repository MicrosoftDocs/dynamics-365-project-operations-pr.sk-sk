---
title: Správa návrhov projektových faktúr
description: Táto téma poskytuje podrobnosti o spracovaní faktúr orientovaných na zákazníka v Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 83e5af60d0a3baf0b59da2a97c6b156ef5b2b7ed
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089302"
---
# <a name="manage-project-invoice-proposals"></a><span data-ttu-id="2255b-103">Správa návrhov projektových faktúr</span><span class="sxs-lookup"><span data-stu-id="2255b-103">Manage project invoice proposals</span></span>

<span data-ttu-id="2255b-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="2255b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2255b-105">Vaše fakturačné oddelenie môže spracovať návrhy projektových faktúr, ak sú splnené tieto dve podmienky:</span><span class="sxs-lookup"><span data-stu-id="2255b-105">Project invoice proposals can be processed by your billing department when the following two conditions are met:</span></span>

  - <span data-ttu-id="2255b-106">Projektový manažér potvrdí pro forma faktúru v Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2255b-106">The Project manager confirms the proforma invoice in Microsoft Dataverse.</span></span>
  - <span data-ttu-id="2255b-107">Všetky časovo a vecne nevyfakturované predajné transakcie, ktoré sú zahrnuté v pro forma faktúre, sa účtujú pomocou účtovného denníka **integrácie Project Operations** Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2255b-107">All time and material unbilled sales transactions that are included in the proforma invoice are posted using the Dynamics 365 **Project Operations Integration** journal.</span></span>

<span data-ttu-id="2255b-108">Podľa týchto pokynov môžete dokončiť návrh faktúry projektu v Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="2255b-108">Use the following steps to complete a project invoice proposal in Dynamics 365 Finance.</span></span>

1. <span data-ttu-id="2255b-109">Skontrolujte fakturačné údaje týkajúce sa časových a vecných transakcií a zaúčtujte účtovný denník **Integrácia Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="2255b-109">Review billing information for time and material transactions and post the **Project Operations Integration** journal.</span></span>
2. <span data-ttu-id="2255b-110">Skontrolujte fakturačné informácie a nájdite medzníky fakturácie s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="2255b-110">Review billing information for fixed price billing milestones.</span></span>
3. <span data-ttu-id="2255b-111">Skontrolujte a naformátujte návrhy projektových faktúr.</span><span class="sxs-lookup"><span data-stu-id="2255b-111">Review and format a project invoice proposal.</span></span>
4. <span data-ttu-id="2255b-112">Zaúčtujte a vytlačte projektové faktúry.</span><span class="sxs-lookup"><span data-stu-id="2255b-112">Post and print project invoices.</span></span>

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a><span data-ttu-id="2255b-113">Spravujte fakturačné informácie v účtovnom denníku integrácie Project Operations</span><span class="sxs-lookup"><span data-stu-id="2255b-113">Manage billing information in the Project Operations Integration journal</span></span>

<span data-ttu-id="2255b-114">Skutočné hodnoty projektu vytvorené v Dataverse sú skontrolované a zaúčtované v aplikácii Finance účtovníkom projektu.</span><span class="sxs-lookup"><span data-stu-id="2255b-114">Project actuals created in Dataverse are reviewed and posted in Finance by the Project accountant.</span></span> <span data-ttu-id="2255b-115">Ďalšie informácie o práci s denníkom integrácie nájdete v časti [Denník integrácie v aplikácii Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="2255b-115">For more information about working with the Integration journal, see [Integration journal in Project Operations](../project-accounting/project-operations-integration-journal.md).</span></span>

<span data-ttu-id="2255b-116">Skutočné náklady a nefakturované skutočné predaje sa do denníka integrácie pridávajú ako samostatné riadky:</span><span class="sxs-lookup"><span data-stu-id="2255b-116">Cost actuals and unbilled sales actuals are added to the Integration journal as separate lines:</span></span>

  - <span data-ttu-id="2255b-117">Obstarávacia cena jednotky a suma nákladov pri predvolenom nastavení skutočných nákladov z transakcie skutočných nákladov projektu v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2255b-117">The unit cost price and cost amount on the Cost actual default from the project actual cost transaction in Dataverse.</span></span>
  - <span data-ttu-id="2255b-118">Jednotková predajná cena a suma predaja v nevyplatenej predajnej transakcii sú predvolené od skutočnej nevyfakturovanej predajnej transakcie v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2255b-118">The unit sales price and sales amount on the Unbilled sales transaction defaults from the project actual unbilled sales transaction in Dataverse.</span></span>

### <a name="billing-sales-tax"></a><span data-ttu-id="2255b-119">Fakturačná daň z predaja</span><span class="sxs-lookup"><span data-stu-id="2255b-119">Billing sales tax</span></span>

<span data-ttu-id="2255b-120">Výpočet dane z predaja pre fakturáciu je určený prostredníctvom kombinácie polí **Skupina fakturovanej dane z predaja** a **Skupina dane z predaja fakturovanej položky** na nevyfakturovanom zázname o predaji v zázname **Integrácia Project Operations** v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="2255b-120">Sales tax calculation for billing is determined by the **Billing sales tax group** and **Billing item sales tax group** field combination on an unbilled sales record on the **Project Operations Integration** journal line.</span></span> <span data-ttu-id="2255b-121">Systém predvolene nastavuje tieto hodnoty poľa na základe nastavení na karte **Financie** na stránke **Parametre projektového riadenia a účtovníctva**.</span><span class="sxs-lookup"><span data-stu-id="2255b-121">The system defaults these field values based on settings on the **Financials** tab on the **Project management and accounting parameters** page.</span></span>

- <span data-ttu-id="2255b-122">**Metóda skupiny dane z predaja** určuje predvolenú logiku skupiny dane z predaja:</span><span class="sxs-lookup"><span data-stu-id="2255b-122">**Sales tax group method** determines the billing sales tax group defaulting logic:</span></span>
  
  - <span data-ttu-id="2255b-123">**Projekt**: Vždy nastaví predvolenú skupinu fakturácie dane z predaja z projektu.</span><span class="sxs-lookup"><span data-stu-id="2255b-123">**Project**: Will always default the billing sales tax group from the project.</span></span> <span data-ttu-id="2255b-124">Výberom možnosti **Zobraziť predvolené účtovníctvo** na stránke **Všetky projekty** môžete skontrolovať alebo zmeniť predvolenú skupinu fakturácie dane z predaja v projekte.</span><span class="sxs-lookup"><span data-stu-id="2255b-124">You can review or change the default billing sales tax group on a project by selecting **Show default accounting** on the **All Projects** page.</span></span>
  - <span data-ttu-id="2255b-125">**Projektová zmluva**: Vždy nastaví predvolenú skupinu fakturácie dane z predaja z projektovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="2255b-125">**Project contract**: Will always default the billing sales tax group from the project contract.</span></span> <span data-ttu-id="2255b-126">Výberom možnosti **Zobraziť predvolené účtovníctvo** na stránke **Projektové zmluvy** môžete skontrolovať alebo zmeniť predvolenú skupinu dane z predaja v projektovej zmluve.</span><span class="sxs-lookup"><span data-stu-id="2255b-126">You can review or change the default sales tax group on a project contract by selecting **Show default accounting** on the **Project contracts** page.</span></span>
  - <span data-ttu-id="2255b-127">**Zákazník**: Vždy nastaví predvolenú skupinu fakturácie dane z predaja zo zákazníka.</span><span class="sxs-lookup"><span data-stu-id="2255b-127">**Customer**: Will always default the billing sales tax group from the customer.</span></span>
  - <span data-ttu-id="2255b-128">**Vyhľadávanie**: Bude prehľadávať všetky vyššie uvedené entity a vyberie prvú dostupnú hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2255b-128">**Search**: Will search across all the above entities and select the first value available.</span></span> <span data-ttu-id="2255b-129">Hľadanie sa začína entitou **Projekt**, potom entitou **Projektová zmluva** a nakoniec entitou **Zákazník**.</span><span class="sxs-lookup"><span data-stu-id="2255b-129">Search starts with the **Project** entity, then the **Project contract** entity, and finally the **Customer** entity.</span></span>

- <span data-ttu-id="2255b-130">**Metóda skupiny dane z predaja položky** určuje predvolenú logiku skupiny dane z predaja položky:</span><span class="sxs-lookup"><span data-stu-id="2255b-130">**Item sales tax group method** determines the billing item sales tax group defaulting logic:</span></span>
  
  - <span data-ttu-id="2255b-131">Pre typy časových, nákladových a poplatkových transakcií bude skupina dane z predaja fakturovanej položky vždy predvolená podľa entity **Kategória projektu**.</span><span class="sxs-lookup"><span data-stu-id="2255b-131">For time, expense, and fee transaction types, the billing item sales tax group will always default from the **Project category** entity.</span></span>
  - <span data-ttu-id="2255b-132">Pre materiálové typy transakcií je predvolená skupina dane z obratu fakturovanej položky na základe nastavenia **Metóda skupiny dane z predaja položky** v časti **Parametre projektového riadenia a účtovníctva**.</span><span class="sxs-lookup"><span data-stu-id="2255b-132">For material transaction types, the billing item sales tax group defaults based on the **Item sales tax group method** setting in **Project management and accounting parameters**.</span></span> <span data-ttu-id="2255b-133">Predvolené číslo položky je skupina DPH z položky z entity **Vydaný produkt**.</span><span class="sxs-lookup"><span data-stu-id="2255b-133">The item number defaults the item sales tax group from the **Released product** entity.</span></span> <span data-ttu-id="2255b-134">Predvolená kategória je skupina DPH z položky z entity **Kategória projektu**.</span><span class="sxs-lookup"><span data-stu-id="2255b-134">The category defaults the item sales tax group from the **Project category** entity.</span></span>

### <a name="financial-dimensions"></a><span data-ttu-id="2255b-135">Finančné dimenzie</span><span class="sxs-lookup"><span data-stu-id="2255b-135">Financial dimensions</span></span>

<span data-ttu-id="2255b-136">Finančné dimenzie pre nevyfakturované záznamy o predaji v denníku **Integrácia Project Operations** sú predvolene z entity **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="2255b-136">The financial dimensions for unbilled sales records in the **Project Operations Integration** journal default from the **Project** entity.</span></span> <span data-ttu-id="2255b-137">Finančné dimenzie možno skontrolovať a upraviť výberom možnosti **Rozdeliť sumy**.</span><span class="sxs-lookup"><span data-stu-id="2255b-137">Financial dimensions can be reviewed and adjusted by selecting **Distribute Amounts**.</span></span> <span data-ttu-id="2255b-138">Ak potrebujete zmeniť finančné dimenzie nevyfakturovaného záznamu o predaji po zaúčtovaní denníka integrácie, ale skôr ako sa potvrdí pro forma faktúra, prejdite na **Všetky projekty** > **Spravovať** > **Zaúčtované transakcie**, vyberte transakciu a potom vyberte **Proces** > **Upraviť účtovníctvo**.</span><span class="sxs-lookup"><span data-stu-id="2255b-138">If you need to change the financial dimensions of the unbilled sales record after the Integration journal is posted but before the Proforma invoice is confirmed, go to **All Projects** > **Manage** > **Posted transactions**, select the transaction, and then select **Process** > **Adjust accounting**.</span></span>

### <a name="exchange-rates"></a><span data-ttu-id="2255b-139">Výmenné kurzy</span><span class="sxs-lookup"><span data-stu-id="2255b-139">Exchange rates</span></span>

<span data-ttu-id="2255b-140">Nevyfakturovaná mena transakcie v Dataverse sa používa ako mena transakcie v aplikácii Finance a prevádza sa na účtovnú menu spoločnosti pomocou výmenných kurzov definovaných v aplikácii Finance.</span><span class="sxs-lookup"><span data-stu-id="2255b-140">Unbilled transaction currency in Dataverse is used as transaction currency in Finance and converted to company's accounting currency using exchange rates defined in Finance.</span></span>


## <a name="manage-the-financial-attributes-of-billing-milestones"></a><span data-ttu-id="2255b-141">Spravujte finančné atribúty medzníkov fakturácie</span><span class="sxs-lookup"><span data-stu-id="2255b-141">Manage the financial attributes of billing milestones</span></span> 

<span data-ttu-id="2255b-142">Riadky projektových zmlúv využívajúce fakturačný postup s pevnou cenou sa fakturujú prostredníctvom možnosti [Medzníky pevnej ceny](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line).</span><span class="sxs-lookup"><span data-stu-id="2255b-142">Project contract lines using the fixed price billing method are invoiced through [Fixed price milestones](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line).</span></span> <span data-ttu-id="2255b-143">Účtovník projektu môže skontrolovať medzníky fakturácie v aplikácii Finance, v časti **Projektové riadenie a účtovníctvo** > **Všetky projekty** > **Spravovať** > **Transakcie na účet**.</span><span class="sxs-lookup"><span data-stu-id="2255b-143">The Project accountant can review billing milestones in Finance by going to **Project management and accounting** > **All projects** > **Manage** > **On-account transactions**.</span></span>

### <a name="billing-sales-tax"></a><span data-ttu-id="2255b-144">Fakturačná daň z predaja</span><span class="sxs-lookup"><span data-stu-id="2255b-144">Billing sales tax</span></span>

<span data-ttu-id="2255b-145">Hodnoty **Skupina dane z predaja** a **Skupina dane z predaja položky** sú predvolene z nastavení, keď sa v Dataverse vytvorí nový medzník fakturácie.</span><span class="sxs-lookup"><span data-stu-id="2255b-145">The **Sales tax group** and **Item sales tax group**  values default from the settings when a new billing milestone is created in Dataverse.</span></span> <span data-ttu-id="2255b-146">Systém predvolene nastavuje hodnoty na tieto polia na základe nastavení na karte **Financie** na stránke **Parametre projektového riadenia a účtovníctva**.</span><span class="sxs-lookup"><span data-stu-id="2255b-146">The system defaults the values to these fields based on settings on the **Financial** tab on the **Project management and accounting parameters** page.</span></span>

- <span data-ttu-id="2255b-147">**Metóda skupiny dane z predaja** určuje predvolenú logiku položky **Skupina dane z fakturovaného predaja**:</span><span class="sxs-lookup"><span data-stu-id="2255b-147">**Sales tax group method** determines the defaulting logic of the **Billing sales tax group**:</span></span>

    - <span data-ttu-id="2255b-148">**Projekt** vždy nastaví predvolenú skupinu fakturácie dane z predaja z projektu.</span><span class="sxs-lookup"><span data-stu-id="2255b-148">**Project** will always default the billing sales tax group from the project.</span></span> <span data-ttu-id="2255b-149">Výberom možnosti **Zobraziť predvolené účtovníctvo** na stránke **Všetky projekty** môžete skontrolovať alebo zmeniť predvolenú skupinu dane z predaja v projekte.</span><span class="sxs-lookup"><span data-stu-id="2255b-149">You can review or change the default sales tax group on a project by selecting **Show default accounting** on the **All Projects** page.</span></span>
    - <span data-ttu-id="2255b-150">**Projektová zmluva** vždy nastaví predvolenú skupinu fakturácie dane z predaja z projektovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="2255b-150">**Project contract** will always default the billing sales tax group from the project contract.</span></span> <span data-ttu-id="2255b-151">Výberom možnosti **Zobraziť predvolené účtovníctvo** na stránke **Projektové zmluvy** môžete skontrolovať alebo zmeniť predvolenú skupinu dane z predaja v projektovej zmluve.</span><span class="sxs-lookup"><span data-stu-id="2255b-151">You can review or change default sales tax group on a project contract by selecting **Show default accounting** on the **Project contracts** page.</span></span>
    - <span data-ttu-id="2255b-152">**Zákazník** vždy nastaví predvolenú skupinu fakturácie dane z predaja zo zákazníka.</span><span class="sxs-lookup"><span data-stu-id="2255b-152">**Customer** will always default to the billing sales tax group from the customer.</span></span>
    - <span data-ttu-id="2255b-153">**Vyhľadávanie** bude prehľadávať všetky entity z tohto zoznamu a vyberie prvú dostupnú hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2255b-153">**Search** will search across all the entities in this list and select the first value available.</span></span> <span data-ttu-id="2255b-154">Hľadanie sa začína entitou **Projekt**, potom entitou **Projektová zmluva** a potom entitou **Zákazník**.</span><span class="sxs-lookup"><span data-stu-id="2255b-154">Search starts with the **Project** entity, then the **Project contract** entity, and then the **Customer** entity.</span></span>

- <span data-ttu-id="2255b-155">**Skupina s daňou z obratu položky s pevnou cenou** sa používa na predvolenú hodnotu pre pole **Skupina dane z predaja položky**.</span><span class="sxs-lookup"><span data-stu-id="2255b-155">**Fixed price milestone item sales tax group** is used to default the value to the **Item sales tax group** field.</span></span>

### <a name="financial-dimensions"></a><span data-ttu-id="2255b-156">Finančné dimenzie</span><span class="sxs-lookup"><span data-stu-id="2255b-156">Financial dimensions</span></span>

<span data-ttu-id="2255b-157">Predvolené finančné dimenzie pre medzník fakturácie s pevnou cenou sú stanovené v riadkoch zmlúv projektu.</span><span class="sxs-lookup"><span data-stu-id="2255b-157">Default financial dimensions for the fixed price billing milestone are set on Project contract lines.</span></span> <span data-ttu-id="2255b-158">Prejdite na **Zmluvy o projekte** > **Zobraziť predvolené účtovníctvo** a na karte **Riadky zmluvy** vyberte **cenu riadku zmluvy**, potom nastavte hodnoty finančnej dimenzie, ktoré chcete použiť ako predvolené.</span><span class="sxs-lookup"><span data-stu-id="2255b-158">Go to **Project contracts** > **Show default accounting** and on the **Contract lines** tab, select **price contract line**, then set the financial dimension values that you want to use as the default.</span></span>

<span data-ttu-id="2255b-159">Účtovník projektu môže upravovať informácie o dani z predaja a finančných dimenziách na medzníkoch faktúr, kým sa nevytvorí návrh faktúry projektu.</span><span class="sxs-lookup"><span data-stu-id="2255b-159">The Project accountant can edit the sales tax and financial dimensions information on invoice milestones up until the Project invoice proposal is created.</span></span>


## <a name="create-project-invoice-proposals"></a><span data-ttu-id="2255b-160">Vytvorenie návrhov projektových faktúr</span><span class="sxs-lookup"><span data-stu-id="2255b-160">Create project invoice proposals</span></span>

<span data-ttu-id="2255b-161">Návrhy projektových faktúr je možné skontrolovať v module **Projektové riadenie a účtovníctvo** v časti **Faktúry projektu** > **Návrhy faktúr projektu**.</span><span class="sxs-lookup"><span data-stu-id="2255b-161">Project invoice proposals can be reviewed in the **Project management and accounting** module by going to **Project invoices** > **Project invoice proposals**.</span></span>

<span data-ttu-id="2255b-162">Hlavička návrhu faktúry projektu sa vytvorí v aplikácii Finance, keď sa potvrdí pro forma faktúra v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2255b-162">The Project invoice proposal header is created in Finance when the Proforma invoice is confirmed in Dataverse.</span></span> <span data-ttu-id="2255b-163">Pre jednoduchšie zosúladenie systém nastaví číslo návrhu faktúry projektu v aplikácii Finance na rovnaké číslo ako ID pro forma faktúry v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2255b-163">For easier reconciliation, the system sets the Project invoice proposal number in Finance to the same number as the Proforma invoice ID in Dataverse.</span></span> <span data-ttu-id="2255b-164">Pretože pro forma faktúry nie sú nevyhnutne potvrdené v rovnakom poradí, v akom sú vytvorené, postupnosť čísiel návrhov faktúr projektu v službe Finance musí umožňovať zmeny na nižšie a vyššie čísla.</span><span class="sxs-lookup"><span data-stu-id="2255b-164">Because Proforma invoices are not necessarily confirmed in the same order they are created, the Project invoice proposal number sequence in Finance must allow for changes to lower and higher numbers.</span></span> <span data-ttu-id="2255b-165">Nakonfigurujte postupnosť čísel podľa nasledujúcich krokov:</span><span class="sxs-lookup"><span data-stu-id="2255b-165">Configure number sequences using the following steps:</span></span>

1. <span data-ttu-id="2255b-166">V aplikácii Finance prejdite na **Správa organizácie** > **Číselné sekvencie** > **Číselné sekvencie**.</span><span class="sxs-lookup"><span data-stu-id="2255b-166">In Finance, go to **Organization Administration** > **Number sequences** > **Number sequences**.</span></span>
2. <span data-ttu-id="2255b-167">Vo filtri **Oblasť** vyberte **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="2255b-167">In the **Area** filter, select **Projects**.</span></span>
3. <span data-ttu-id="2255b-168">Vo filtri **Odkaz** vyberte **Návrh faktúry**.</span><span class="sxs-lookup"><span data-stu-id="2255b-168">In the **Reference** filter, select **Invoice proposal**.</span></span>
4. <span data-ttu-id="2255b-169">Pole **Spoločnosť** použite na filtrovanie každej právnickej entity s povolenou integráciou Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2255b-169">Use the **Company** field to filter each legal entity with Project Operations Dataverse integration enabled.</span></span>
5. <span data-ttu-id="2255b-170">Otvorte **Podrobnosti o postupnosti čísel** a na karte **Všeobecné** nastavte:</span><span class="sxs-lookup"><span data-stu-id="2255b-170">Open **Number Sequence details** and on the **General** tab set:</span></span>

    - <span data-ttu-id="2255b-171">**Povoliť zmeny používateľa: na nižší počet** = **Áno**</span><span class="sxs-lookup"><span data-stu-id="2255b-171">**Allow user changes: To a lower number** = **Yes**</span></span>
    - <span data-ttu-id="2255b-172">**Povoliť zmeny používateľa: na vyšší počet** = **Áno**</span><span class="sxs-lookup"><span data-stu-id="2255b-172">**Allow user changes: To a higher number** = **Yes**</span></span>

<span data-ttu-id="2255b-173">Riadky s návrhmi faktúr pre projekt pridáva systém pomocou pravidelného procesu **Import z pracovnej tabuľky** (**Projektový manažment a účtovníctvo** > **Pravidelné** > **Integrácia Project Operations** > **Import z pracovnej tabuľky**).</span><span class="sxs-lookup"><span data-stu-id="2255b-173">Project invoice proposal lines are added by the system using the periodic process **Import from staging table** (**Project management and accounting** > **Periodic** > **Project Operations integration** > **Import from staging table**).</span></span> <span data-ttu-id="2255b-174">Tento proces je možné spustiť manuálne alebo pomocou pravidelného plánu.</span><span class="sxs-lookup"><span data-stu-id="2255b-174">This process can be run manually or by using a periodic schedule.</span></span> <span data-ttu-id="2255b-175">Systém nepridá riadky do dokumentu návrhu faktúry, kým nebudú všetky riadky pripravené na fakturáciu.</span><span class="sxs-lookup"><span data-stu-id="2255b-175">The system won't add lines to the invoice proposal document until all the lines are ready to be invoiced.</span></span> <span data-ttu-id="2255b-176">Časové a materiálové transakcie sú pripravené na fakturáciu, až keď sa zaúčtujú pomocou denníka **Integrácia Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="2255b-176">Time and material transactions are ready to be invoiced only when they are posted using the **Project Operations Integration** journal.</span></span>

## <a name="format-and-print-invoice-proposals"></a><span data-ttu-id="2255b-177">Formátovanie a tlač návrhov faktúr</span><span class="sxs-lookup"><span data-stu-id="2255b-177">Format and print invoice proposals</span></span>

<span data-ttu-id="2255b-178">Účtovník projektu môže prispôsobiť výtlačok projektovej faktúry pomocou stránky **Naformátovať návrh faktúry** možností správy tlače.</span><span class="sxs-lookup"><span data-stu-id="2255b-178">The Project accountant can customize a project invoice printout by using the **Format invoice proposal** page and print management capabilities.</span></span>

### <a name="format-invoice-proposals"></a><span data-ttu-id="2255b-179">Formátovanie návrhov faktúr</span><span class="sxs-lookup"><span data-stu-id="2255b-179">Format invoice proposals</span></span>

<span data-ttu-id="2255b-180">Stránka **Naformátovať návrhy faktúr** umožňuje zobrazenie vlastných zoskupovacích transakcií vo faktúre projektu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="2255b-180">The **Format invoice proposals** page allows custom grouping transactions to display in the customer project invoice.</span></span>

1. <span data-ttu-id="2255b-181">Na stránke **Návrh projektovej faktúry** vyberte **Tlač** > **Naformátovať návrh faktúry**.</span><span class="sxs-lookup"><span data-stu-id="2255b-181">On the **Project invoice proposal** page, select **Print** > **Format invoice proposal**.</span></span>
2. <span data-ttu-id="2255b-182">Výberom možnosti **Nové** vytvoríte nové zoskupenie pre výtlačok faktúry projektu.</span><span class="sxs-lookup"><span data-stu-id="2255b-182">Select **New** to create a new grouping for the Project invoice printout.</span></span>
3. <span data-ttu-id="2255b-183">V poli **Podrobnosti/zhrnutie** vyberte možnosti pre toto zoskupenie:</span><span class="sxs-lookup"><span data-stu-id="2255b-183">In the **Detail/Summary** field, select options for this grouping:</span></span>

    - <span data-ttu-id="2255b-184">Vyberte **Podrobnosti** na vytlačenie podrobností transakcie zákazníckej faktúry.</span><span class="sxs-lookup"><span data-stu-id="2255b-184">Select **Detail** to print the transaction details of the customer invoice.</span></span>
    - <span data-ttu-id="2255b-185">Vyberte **Súhrn** na vytlačenie súhrnu transakcie zákazníckej faktúry.</span><span class="sxs-lookup"><span data-stu-id="2255b-185">Select **Summary** to print the transaction summary of the customer invoice.</span></span>

> [!NOTE]
> <span data-ttu-id="2255b-186">Výber v poli **Podrobnosti/zhrnutie** na stránke **Naformátovať návrh faktúry** prepíše možnosť vybranú v poli **Formát faktúry** na stránke **Návrhy faktúr** na vytlačenie podrobnej faktúry alebo súhrnnej faktúry.</span><span class="sxs-lookup"><span data-stu-id="2255b-186">The selection in the **Detail/Summary** field on the **Format invoice proposal** page overrides the option selected in the **Invoice format** field on the **Invoice proposals** page to print a detailed invoice or a summarized invoice.</span></span>

- <span data-ttu-id="2255b-187">Vyberte riadky transakcií, ktoré chcete zahrnúť do tejto časti na karte **Dostupné transakcie** a vyberte **Zahrnúť transakcie** na ich presun na kartu **Vybrané transakcie**.</span><span class="sxs-lookup"><span data-stu-id="2255b-187">Select the transaction lines to include in this section on the **Available transactions** tab and select **Include transactions** to move them to the **Selected transactions** tab.</span></span>
- <span data-ttu-id="2255b-188">Vyberte **Posunúť nahor** a **Posunúť nadol** na zmenu poradia sekcií.</span><span class="sxs-lookup"><span data-stu-id="2255b-188">Select **Move up** and **Move down** to change the order of the sections.</span></span>
- <span data-ttu-id="2255b-189">Vyberte **Ukážka pred tlačou** na náhľad naformátovanej faktúry.</span><span class="sxs-lookup"><span data-stu-id="2255b-189">Select **Print preview** to preview formatted invoice.</span></span>

### <a name="print-management"></a><span data-ttu-id="2255b-190">Správa tlače</span><span class="sxs-lookup"><span data-stu-id="2255b-190">Print management</span></span>

<span data-ttu-id="2255b-191">Správa tlače používa na tlač rôzne súbory správ, špecifikáciu cieľov a prispôsobenie textu päty pre faktúru.</span><span class="sxs-lookup"><span data-stu-id="2255b-191">Print management uses different report files to print, specify destinations, and customize footer text for the invoice.</span></span> <span data-ttu-id="2255b-192">Správu tlače je možné nastaviť na úrovni modulu, tieto nastavenia však možno prepísať pre konkrétneho zákazníka, zmluvu alebo návrh faktúry.</span><span class="sxs-lookup"><span data-stu-id="2255b-192">Print management can be set up at the module level, however these settings can be overridden for a specific customer, contract, or invoice proposal.</span></span> <span data-ttu-id="2255b-193">Pre prístup k tejto funkcii na stránke **Návrh projektovej faktúry** vyberte možnosť **Tlačiť** > **Správa tlače**.</span><span class="sxs-lookup"><span data-stu-id="2255b-193">To access this function on the **Project invoice proposal** page, select **Print** > **Print management**.</span></span>

<span data-ttu-id="2255b-194">Nastavenie správy tlače sa zobrazuje ako stromové zobrazenie, kde každá úroveň uzla zobrazuje dostupné dokumenty, ktoré je potrebné upraviť.</span><span class="sxs-lookup"><span data-stu-id="2255b-194">Print management setup is displayed as a tree view, where each node level displays the available documents to adjust.</span></span> <span data-ttu-id="2255b-195">Môžete priradiť vlastné výtlačky na úrovni modulu, zákazníka, zmluvy alebo návrhu faktúry.</span><span class="sxs-lookup"><span data-stu-id="2255b-195">You can assign custom printouts at the module, customer, contract, or invoice proposal document level.</span></span> <span data-ttu-id="2255b-196">Ak chcete upraviť výtlačok pôvodného dokumentu, rozbaľte požadovaný uzol a vyberte **Pôvodná položka**.</span><span class="sxs-lookup"><span data-stu-id="2255b-196">To modify the original document printout, expand the desired node and select **Original item**.</span></span> <span data-ttu-id="2255b-197">V poli **Formát zostavy** vyberte formát zostavy, ktorý sa má použiť na tlač.</span><span class="sxs-lookup"><span data-stu-id="2255b-197">In the **Report format** field, select the report format to be used for printing.</span></span> <span data-ttu-id="2255b-198">Môžete použiť vlastné formáty zostáv pomocou možnosti [Rámec riadenia obchodných dokumentov](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).</span><span class="sxs-lookup"><span data-stu-id="2255b-198">You can use custom report formats by using [Business Document Management framework](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).</span></span>

## <a name="post-invoice-proposals"></a><span data-ttu-id="2255b-199">Zaúčtovanie návrhov faktúr</span><span class="sxs-lookup"><span data-stu-id="2255b-199">Post invoice proposals</span></span>

<span data-ttu-id="2255b-200">Po skontrolovaní a úprave faktúry a uspokojivom riadku návrhu faktúry skontrolujte súčty faktúry a daň z predaja.</span><span class="sxs-lookup"><span data-stu-id="2255b-200">After the invoice has been reviewed and edited, and the invoice proposal lines are satisfactory, check the invoice totals and sales tax.</span></span> <span data-ttu-id="2255b-201">V skupine **Podrobnosti** vyberte **Súčty** a potom vyberte **Zaúčtovať** na zaúčtovanie faktúry.</span><span class="sxs-lookup"><span data-stu-id="2255b-201">In the **Details** group, select **Totals** and then select **Post** to post the invoice.</span></span>

<span data-ttu-id="2255b-202">Ak chcete zobraziť faktúru pred zaúčtovaním, zrušte začiarknutie políčka **Zaúčtovanie**.</span><span class="sxs-lookup"><span data-stu-id="2255b-202">To view the invoice before posting, clear the **Posting** check box.</span></span> <span data-ttu-id="2255b-203">**Pro forma** sa vytlačí na faktúre na znak toho, že ide o vzor faktúry.</span><span class="sxs-lookup"><span data-stu-id="2255b-203">**Pro forma** will be printed on the invoice to signify it is a sample invoice.</span></span> <span data-ttu-id="2255b-204">Ak chcete vytlačiť faktúru, začiarknite políčko **Vytlačiť faktúru**.</span><span class="sxs-lookup"><span data-stu-id="2255b-204">To print the invoice, select the **Print invoice** check box.</span></span>

<span data-ttu-id="2255b-205">Okrem stránky **Návrh faktúry** je možné zaslať návrhy faktúr spustením pravidelnej úlohy **Zaúčtovať návrhy faktúr**.</span><span class="sxs-lookup"><span data-stu-id="2255b-205">In addition to the **Invoice proposal** page, invoice proposals can also be posted by running the periodic job, **Post invoice proposals**.</span></span> <span data-ttu-id="2255b-206">Ak chcete nájsť túto úlohu, prejdite na **Projektové riadenie a účtovníctvo** > **Pravidelné** > **Faktúry projektu** > **Zaúčtovať návrhy faktúr**.</span><span class="sxs-lookup"><span data-stu-id="2255b-206">To find this job, go to **Project management and accounting** > **Periodic** > **Project invoices** > **Post invoice proposals**.</span></span>

<span data-ttu-id="2255b-207">Táto stránka zobrazuje všetky návrhy faktúr, ktoré sú pripravené na zaúčtovanie.</span><span class="sxs-lookup"><span data-stu-id="2255b-207">This page shows all the invoice proposals that are ready for posting.</span></span> <span data-ttu-id="2255b-208">Výberom možnosti **Dávka** môžete naplánovať účtovanie návrhov faktúr.</span><span class="sxs-lookup"><span data-stu-id="2255b-208">You can schedule posting invoice proposals by selecting **Batch**.</span></span> <span data-ttu-id="2255b-209">Nastavte **Parameter dávkového spracovania** na **Áno** a nastavte opakovanie dávkového spracovania výberom **Opakovanie**.</span><span class="sxs-lookup"><span data-stu-id="2255b-209">Set the **Batch processing parameter** to **Yes** and set the recurrence of batch processing by selecting **Recurrence**.</span></span>