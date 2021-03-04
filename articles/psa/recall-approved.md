---
title: Odvolanie schváleného času a položiek výdavkov
description: Táto téma poskytuje informácie o zrušení predtým schváleného času projektu alebo nákladov transakcie.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9bb25ac9ef7b400063c5f958311e475de6f6506
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147871"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="67e7e-103">Odvolanie schváleného času a položiek výdavkov</span><span class="sxs-lookup"><span data-stu-id="67e7e-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="67e7e-104">Člen projektového tímu alebo iná osoba, ktorá odošle čas alebo výdavok, môže pripomenúť, že čas alebo náklad po jeho schválení.</span><span class="sxs-lookup"><span data-stu-id="67e7e-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="67e7e-105">Proces na vyvolanie schváleného času alebo výdavku má dva kroky:</span><span class="sxs-lookup"><span data-stu-id="67e7e-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="67e7e-106">Odosielateľ požaduje stiahnutie.</span><span class="sxs-lookup"><span data-stu-id="67e7e-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="67e7e-107">Schvaľovateľ schvaľuje stiahnutie.</span><span class="sxs-lookup"><span data-stu-id="67e7e-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="67e7e-108">Požiadať o stiahnutie</span><span class="sxs-lookup"><span data-stu-id="67e7e-108">Request a recall</span></span>

<span data-ttu-id="67e7e-109">Tieto kroky použite na vyžiadanie stiahnutia schváleného zadania času alebo výdavkov.</span><span class="sxs-lookup"><span data-stu-id="67e7e-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="67e7e-110">Pre položky času, prejdite na **Projekty** \> **Moja práca** \> **Zadanie času**.</span><span class="sxs-lookup"><span data-stu-id="67e7e-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="67e7e-111">-alebo-</span><span class="sxs-lookup"><span data-stu-id="67e7e-111">–or–</span></span>

    <span data-ttu-id="67e7e-112">Pre položky výdavkov, prejdite na **Projekty** \> **Moja práca** \> **Výdavky**.</span><span class="sxs-lookup"><span data-stu-id="67e7e-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="67e7e-113">V prípade položiek času vyberte všetky položky času pre konkrétnu kombináciu projektu a úlohy.</span><span class="sxs-lookup"><span data-stu-id="67e7e-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="67e7e-114">Prípadne v mriežke vyberte jednotlivé bunky pre čas v určitom dátume konkrétneho projektu.</span><span class="sxs-lookup"><span data-stu-id="67e7e-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="67e7e-115">-alebo-</span><span class="sxs-lookup"><span data-stu-id="67e7e-115">–or–</span></span>

    <span data-ttu-id="67e7e-116">Pre položky výdavkov vyberte riadok pre položku výdavku na vyvolanie.</span><span class="sxs-lookup"><span data-stu-id="67e7e-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="67e7e-117">Vyberte položku **Odvolať**.</span><span class="sxs-lookup"><span data-stu-id="67e7e-117">Select **Recall**.</span></span> <span data-ttu-id="67e7e-118">Zobrazí sa dialógové okno s potvrdením.</span><span class="sxs-lookup"><span data-stu-id="67e7e-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="67e7e-119">Ak boli vybraté položky času a výdavkov už schválené, zobrazí sa výzva na zadanie dôvodu stiahnutia.</span><span class="sxs-lookup"><span data-stu-id="67e7e-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="67e7e-120">Zadajte dôvod stiahnutia a potom vyberte **OK**, čím potvrdíte operáciu.</span><span class="sxs-lookup"><span data-stu-id="67e7e-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="67e7e-121">Systém odošle osobe, ktorá schválila položky, žiadosť o schválenie odvolania.</span><span class="sxs-lookup"><span data-stu-id="67e7e-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="67e7e-122">Aj keď možno odvolať záznamy schváleného času a výdavkov, po vyfakturovaní schváleného času alebo výdavku zákazníkovi už nemožno požiadavku o stiahnutie vytvoriť.</span><span class="sxs-lookup"><span data-stu-id="67e7e-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="67e7e-123">Používateľ, ktorý sa pokúsi vytvoriť žiadosť o stiahnutie dostane správu, ktorá uvádza, že čas alebo výdavky nemožno stiahnuť, pretože už boli fakturované.</span><span class="sxs-lookup"><span data-stu-id="67e7e-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="67e7e-124">Schválenie alebo odmietnutie žiadosti o stiahnutie</span><span class="sxs-lookup"><span data-stu-id="67e7e-124">Approve or reject a recall request</span></span>

<span data-ttu-id="67e7e-125">Ak chcete schváliť alebo zamietnuť žiadosť o stiahnutie, postupujte podľa týchto krokov.</span><span class="sxs-lookup"><span data-stu-id="67e7e-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="67e7e-126">Prejdite na **projekty** \> **moja práca** \> **schválenia**.</span><span class="sxs-lookup"><span data-stu-id="67e7e-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="67e7e-127">Na stránke zoznamu **Schválenia** zmeňte zobrazenie na **Žiadosti o odvolanie na schválenie**.</span><span class="sxs-lookup"><span data-stu-id="67e7e-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="67e7e-128">Zobrazí sa zoznam predložených žiadostí o stiahnutie.</span><span class="sxs-lookup"><span data-stu-id="67e7e-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="67e7e-129">Vyberte jednu alebo viac položiek a potom vyberte položku **Schváliť** alebo **Odmietnuť**.</span><span class="sxs-lookup"><span data-stu-id="67e7e-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="67e7e-130">Ak ste vybrali možnosť **Schváliť**, zobrazí sa upozorňujúce hlásenie, ktoré vysvetľuje vplyv schválenia.</span><span class="sxs-lookup"><span data-stu-id="67e7e-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="67e7e-131">Stlačením možnosti **OK** potvrďte operáciu.</span><span class="sxs-lookup"><span data-stu-id="67e7e-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="67e7e-132">Žiadosť o odvolanie bola schválená.</span><span class="sxs-lookup"><span data-stu-id="67e7e-132">The recall request is approved.</span></span>

    <span data-ttu-id="67e7e-133">-alebo-</span><span class="sxs-lookup"><span data-stu-id="67e7e-133">–or–</span></span>

    <span data-ttu-id="67e7e-134">Ak ste vybrali **Odmietnuť**, žiadosť o odvolanie sa zamietne.</span><span class="sxs-lookup"><span data-stu-id="67e7e-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="67e7e-135">Ako pri požadovaní stiahnutia skontroluje po schválení stiahnutia systém akúkoľvek aktivitu fakturácie v záznamoch času či výdavkov.</span><span class="sxs-lookup"><span data-stu-id="67e7e-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="67e7e-136">Ak bola položka už fakturovaná, alebo ak je v návrhu faktúry, schvaľovateľovi sa zobrazí chybové hlásenie, ktoré uvádza, že čas alebo výdavky nemôžu byť schválené na stiahnutie, pretože to bolo už fakturované.</span><span class="sxs-lookup"><span data-stu-id="67e7e-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="67e7e-137">Vplyv žiadosti o stiahnutie</span><span class="sxs-lookup"><span data-stu-id="67e7e-137">Impact of a recall request</span></span>

<span data-ttu-id="67e7e-138">Ak sa schválenie odmietne, existuje prevádzkový dopad aj finančný dopad.</span><span class="sxs-lookup"><span data-stu-id="67e7e-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="67e7e-139">Prevádzkový vplyv</span><span class="sxs-lookup"><span data-stu-id="67e7e-139">Operational impact</span></span>

<span data-ttu-id="67e7e-140">Ak je žiadosť o odvolanie schválená, záznam o schválení je označený ako **Zamietnutý**.</span><span class="sxs-lookup"><span data-stu-id="67e7e-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="67e7e-141">Stav položky sa zmení na **Vrátený** alebo **Zamietnutý** v závislosti od toho, či ide o časovú položku alebo položku výdavkov.</span><span class="sxs-lookup"><span data-stu-id="67e7e-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="67e7e-142">Člen projektového tímu môže zobraziť položky, upraviť ich a potom znova odoslať alebo odstrániť položky úplne.</span><span class="sxs-lookup"><span data-stu-id="67e7e-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="67e7e-143">Ak sa žiadosť o odvolanie zamietne, stav položky zostane **Schválený** a položku nie je možné upraviť členom projektového tímu alebo schvaľovateľa projektu.</span><span class="sxs-lookup"><span data-stu-id="67e7e-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="67e7e-144">Finančný vplyv</span><span class="sxs-lookup"><span data-stu-id="67e7e-144">Financial impact</span></span>

<span data-ttu-id="67e7e-145">Ak dôjde k schváleniu žiadosti o odvolanie, zodpovedajúce skutočné hodnoty nákladov a predaja sa aktualizujú nasledujúcim spôsobom:</span><span class="sxs-lookup"><span data-stu-id="67e7e-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="67e7e-146">Pole **Stav úpravy** sa aktualizuje na **Upravené**.</span><span class="sxs-lookup"><span data-stu-id="67e7e-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="67e7e-147">Pole **Stav fakturácie** sa aktualizuje na **Zrušené**.</span><span class="sxs-lookup"><span data-stu-id="67e7e-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="67e7e-148">Ďalšie, storno položky sú vytvorené v tabuľke skutočné údaje.</span><span class="sxs-lookup"><span data-stu-id="67e7e-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="67e7e-149">Ak chcete vytvoriť storno položky, systém skopíruje hodnoty polí z pôvodných skutočných hodnôt.</span><span class="sxs-lookup"><span data-stu-id="67e7e-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="67e7e-150">Iba hodnoty, ktoré nie sú skopírované, sú hodnoty množstva.</span><span class="sxs-lookup"><span data-stu-id="67e7e-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="67e7e-151">Tieto hodnoty sa namiesto toho obrátili.</span><span class="sxs-lookup"><span data-stu-id="67e7e-151">These values are reversed instead.</span></span> <span data-ttu-id="67e7e-152">Obrátené skutočné hodnoty sú vytvorené pre skutočné hodnoty **nákladov**, aj pre **nefakturovaných predajov**.</span><span class="sxs-lookup"><span data-stu-id="67e7e-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="67e7e-153">Pole **Stav úpravy** na vrátených skutočných hodnotách je nastavené na **Neupraviteľné** a pole **Stav fakturácie** je nastavené na **Zrušené**.</span><span class="sxs-lookup"><span data-stu-id="67e7e-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="67e7e-154">V dôsledku týchto zmien sa zaznamenané výdavky a backlog príjmov na projekte nebudú viac vzťahovať na sumy, ktoré tieto skutočné hodnoty predstavujú.</span><span class="sxs-lookup"><span data-stu-id="67e7e-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="67e7e-155">Ak sa žiadosť o odvolanie zamietne, neexistuje žiadny finančný vplyv na projekt.</span><span class="sxs-lookup"><span data-stu-id="67e7e-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="67e7e-156">Zmeny záznamov zadania času</span><span class="sxs-lookup"><span data-stu-id="67e7e-156">Changes to time entry records</span></span>

<span data-ttu-id="67e7e-157">Nasledujúci obrázok zobrazuje zmeny, ktoré sa vyskytnú pri schválených časových položkách, keď sú stiahnuté.</span><span class="sxs-lookup"><span data-stu-id="67e7e-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Prechody stavu zadania času](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="67e7e-159">Zmeny záznamov zadania výdavkov</span><span class="sxs-lookup"><span data-stu-id="67e7e-159">Changes to expense entry records</span></span>

<span data-ttu-id="67e7e-160">Nasledujúci obrázok zobrazuje zmeny, ktoré sa vyskytnú pri schválených výdavkových položkách, keď sú stiahnuté.</span><span class="sxs-lookup"><span data-stu-id="67e7e-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Prechody stavu zadania výdavkov](media/ExpenseEntryStateTransitions.png)
