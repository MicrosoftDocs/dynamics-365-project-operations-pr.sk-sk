---
title: Import a udržiavanie transakcií kreditnou kartou
description: Táto téma vysvetľuje, ako importovať a udržiavať transakcie kreditnými kartami súvisiace s výdavkami. Tieto transakcie je možné nastaviť tak, aby sa automaticky importovali podľa opakujúceho sa plánu, alebo podľa potreby je možné ich manuálne importovať.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: edeab157aa2fa6cf518ad086b4c1f22c5b45fa04
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005180"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="8a916-104">Import a udržiavanie transakcií kreditnou kartou</span><span class="sxs-lookup"><span data-stu-id="8a916-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="8a916-105">Transakcie s kreditnými kartami súvisiace s výdavkami je možné nastaviť tak, aby sa automaticky importovali podľa opakujúceho sa harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="8a916-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="8a916-106">Alternatívne je možné transakcie importovať manuálne podľa potreby.</span><span class="sxs-lookup"><span data-stu-id="8a916-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="8a916-107">Transakcie kreditnými kartami sa importujú prostredníctvom dátovej entity Transakcie kreditnou kartou.</span><span class="sxs-lookup"><span data-stu-id="8a916-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="8a916-108">Ďalšie informácie o entitách údajov nájdete v časti [Entity údajov](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="8a916-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="8a916-109">Import transakcií kreditnou kartou</span><span class="sxs-lookup"><span data-stu-id="8a916-109">Import credit card transactions</span></span>

1. <span data-ttu-id="8a916-110">Na stránke **Transakcie kreditnou kartou** vyberte **Importovať transakcie**.</span><span class="sxs-lookup"><span data-stu-id="8a916-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="8a916-111">Ak správu údajov otvárate prvýkrát, systém musí najskôr aktualizovať zoznam dátových entít.</span><span class="sxs-lookup"><span data-stu-id="8a916-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="8a916-112">Do poľa **Názov** zadajte jedinečný popis úlohy importu.</span><span class="sxs-lookup"><span data-stu-id="8a916-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="8a916-113">V poli **Formát zdrojových údajov** vyberte formát súboru, ktorý obsahuje transakcie kreditnej karty na import.</span><span class="sxs-lookup"><span data-stu-id="8a916-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="8a916-114">Vyberte **Nahrať** a potom vyhľadajte a vyberte súbor, ktorý chcete importovať.</span><span class="sxs-lookup"><span data-stu-id="8a916-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="8a916-115">Po nahraní súboru overte spárovanie súboru transakcií s kreditnými kartami a stĺpcov dátovej entity Transakcie s kreditnými kartami výberom prepojenia **Zobraziť mapu** na dlaždici.</span><span class="sxs-lookup"><span data-stu-id="8a916-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="8a916-116">Ak sa vyskytujú chyby spárovania, alebo ak musíte zmeniť spárovanie, vykonajte zmeny spárovania buď z karty **Vizualizácia spárovania** alebo karty **Podrobnosti spárovania**.</span><span class="sxs-lookup"><span data-stu-id="8a916-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="8a916-117">Ak chcete automatizovať transakcie kreditnou kartou, vyberte **Vytvoriť opakujúcu sa dátovú úlohu**.</span><span class="sxs-lookup"><span data-stu-id="8a916-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="8a916-118">Potom môžete nastaviť opakovanie, ktoré definuje, ako často sa majú transakcie kreditnou kartou importovať.</span><span class="sxs-lookup"><span data-stu-id="8a916-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="8a916-119">Po dokončení vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a916-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="8a916-120">Ak chcete vybratý súbor importovať teraz, vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="8a916-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="8a916-121">Ak sa počas importu vyskytnú chyby, môžete si prezrieť protokol vykonávania alebo údaje o postupe, aby ste videli chyby, ktoré musíte opraviť, aby ste zaručili úspešný import.</span><span class="sxs-lookup"><span data-stu-id="8a916-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="8a916-122">Ak musíte importovať viac ako jeden formát súboru, musíte vytvoriť samostatné úlohy importu pre každý typ formátu.</span><span class="sxs-lookup"><span data-stu-id="8a916-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="8a916-123">Zmena priradenia transakcií kreditnou kartou pre ukončených zamestnancov</span><span class="sxs-lookup"><span data-stu-id="8a916-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="8a916-124">Po ukončení záznamu zamestnanca je účet zamestnanca služby Active Directory Domain Services (AD DS) deaktivovaný.</span><span class="sxs-lookup"><span data-stu-id="8a916-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="8a916-125">Môžu však existovať aktívne transakcie s kreditnými kartami, ktoré sa musia stále zaúčtovať a uhradiť.</span><span class="sxs-lookup"><span data-stu-id="8a916-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="8a916-126">Zo stránky **Transakcie kreditnou kartou** môžete zamestnanca znova priradiť k akejkoľvek transakcii kreditnou kartou, kde bol ukončený pridružený zamestnanec.</span><span class="sxs-lookup"><span data-stu-id="8a916-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="8a916-127">Vyberte jednu alebo viac transakcií kreditnou kartou a potom vyberte **Opätovné pridelenie transakcií**.</span><span class="sxs-lookup"><span data-stu-id="8a916-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="8a916-128">Potom môžete vybrať iného zamestnanca, ktorému chcete priradiť transakcie kreditnou kartou.</span><span class="sxs-lookup"><span data-stu-id="8a916-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="8a916-129">Po opätovnom priradení transakcií kreditnou kartou ich možno vybrať pre výkaz výdavkov a zaplatiť obvyklým spôsobom na úhradu výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="8a916-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]