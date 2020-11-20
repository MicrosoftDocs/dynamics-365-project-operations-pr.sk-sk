---
title: Nastavenie integrácie kreditnej karty
description: Táto téma vysvetľuje, ako importovať a udržiavať transakcie kreditnými kartami súvisiace s výdavkami.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120877"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="76152-103">Nastavenie integrácie kreditnej karty</span><span class="sxs-lookup"><span data-stu-id="76152-103">Set up credit card integration</span></span>

<span data-ttu-id="76152-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="76152-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="76152-105">Transakcie s kreditnými kartami súvisiace s výdavkami je možné nastaviť tak, aby sa automaticky importovali podľa opakujúceho sa harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="76152-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="76152-106">Alternatívne je možné transakcie importovať manuálne podľa potreby.</span><span class="sxs-lookup"><span data-stu-id="76152-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="76152-107">Transakcie kreditnými kartami sa importujú prostredníctvom dátovej entity Transakcie kreditnou kartou.</span><span class="sxs-lookup"><span data-stu-id="76152-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="76152-108">Import transakcií kreditnou kartou</span><span class="sxs-lookup"><span data-stu-id="76152-108">Import credit card transactions</span></span>

1. <span data-ttu-id="76152-109">Na stránke **Transakcie kreditnou kartou** vyberte **Importovať transakcie**.</span><span class="sxs-lookup"><span data-stu-id="76152-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="76152-110">Ak správu údajov otvárate prvýkrát, systém musí najskôr aktualizovať zoznam dátových entít.</span><span class="sxs-lookup"><span data-stu-id="76152-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="76152-111">Do poľa **Názov** zadajte jedinečný popis úlohy importu.</span><span class="sxs-lookup"><span data-stu-id="76152-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="76152-112">V poli **Formát zdrojových údajov** vyberte formát súboru, ktorý obsahuje transakcie kreditnej karty na import.</span><span class="sxs-lookup"><span data-stu-id="76152-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="76152-113">Vyberte **Nahrať** a potom vyhľadajte a vyberte súbor, ktorý chcete importovať.</span><span class="sxs-lookup"><span data-stu-id="76152-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="76152-114">Po nahraní súboru overte spárovanie súboru transakcií s kreditnými kartami a stĺpcov dátovej entity Transakcie s kreditnými kartami výberom prepojenia **Zobraziť mapu** na dlaždici.</span><span class="sxs-lookup"><span data-stu-id="76152-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="76152-115">Ak sa vyskytujú chyby spárovania, alebo ak musíte zmeniť spárovanie, vykonajte zmeny spárovania buď z karty **Vizualizácia spárovania** alebo karty **Podrobnosti spárovania**.</span><span class="sxs-lookup"><span data-stu-id="76152-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="76152-116">Ak chcete automatizovať transakcie kreditnou kartou, vyberte **Vytvoriť opakujúcu sa dátovú úlohu**.</span><span class="sxs-lookup"><span data-stu-id="76152-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="76152-117">Potom môžete nastaviť opakovanie, ktoré definuje, ako často sa majú transakcie kreditnou kartou importovať.</span><span class="sxs-lookup"><span data-stu-id="76152-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="76152-118">Po dokončení vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="76152-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="76152-119">Ak chcete vybratý súbor importovať teraz, vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="76152-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="76152-120">Ak sa počas importu vyskytnú chyby, môžete si prezrieť protokol vykonávania alebo údaje o postupe, aby ste videli chyby, ktoré musíte opraviť, aby ste zaručili úspešný import.</span><span class="sxs-lookup"><span data-stu-id="76152-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="76152-121">Ak musíte importovať viac ako jeden formát súboru, musíte vytvoriť samostatné úlohy importu pre každý typ formátu.</span><span class="sxs-lookup"><span data-stu-id="76152-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="76152-122">Zmena priradenia transakcií kreditnou kartou pre ukončených zamestnancov</span><span class="sxs-lookup"><span data-stu-id="76152-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="76152-123">Po ukončení záznamu zamestnanca je účet zamestnanca služby Active Directory Domain Services (AD DS) deaktivovaný.</span><span class="sxs-lookup"><span data-stu-id="76152-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="76152-124">Môžu však existovať aktívne transakcie s kreditnými kartami, ktoré sa musia stále zaúčtovať a uhradiť.</span><span class="sxs-lookup"><span data-stu-id="76152-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="76152-125">Zo stránky **Transakcie kreditnou kartou** môžete zamestnanca znova priradiť k akejkoľvek transakcii kreditnou kartou, kde bol ukončený pridružený zamestnanec.</span><span class="sxs-lookup"><span data-stu-id="76152-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="76152-126">Vyberte jednu alebo viac transakcií kreditnou kartou a potom vyberte **Opätovné pridelenie transakcií**.</span><span class="sxs-lookup"><span data-stu-id="76152-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="76152-127">Potom môžete vybrať iného zamestnanca, ktorému chcete priradiť transakcie kreditnou kartou.</span><span class="sxs-lookup"><span data-stu-id="76152-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="76152-128">Po opätovnom priradení transakcií kreditnou kartou ich možno vybrať pre výkaz výdavkov a zaplatiť obvyklým spôsobom na úhradu výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="76152-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
