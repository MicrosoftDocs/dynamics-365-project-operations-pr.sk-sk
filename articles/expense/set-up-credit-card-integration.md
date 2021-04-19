---
title: Nastavenie integrácie kreditnej karty
description: Táto téma vysvetľuje, ako pracovať s transakciami kreditnej karty spojenými s výdavkami.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
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
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866702"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="98bb4-103">Nastavenie integrácie kreditnej karty</span><span class="sxs-lookup"><span data-stu-id="98bb4-103">Set up credit card integration</span></span>

<span data-ttu-id="98bb4-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="98bb4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="98bb4-105">Transakcie s kreditnými kartami súvisiace s výdavkami je možné nastaviť tak, aby sa automaticky importovali podľa opakujúceho sa harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="98bb4-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="98bb4-106">Alternatívne je možné transakcie importovať manuálne podľa potreby.</span><span class="sxs-lookup"><span data-stu-id="98bb4-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="98bb4-107">Transakcie kreditnou kartou sa importujú prostredníctvom dátovej entity transakcie kreditnou kartou.</span><span class="sxs-lookup"><span data-stu-id="98bb4-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="98bb4-108">Import transakcií kreditnou kartou</span><span class="sxs-lookup"><span data-stu-id="98bb4-108">Import credit card transactions</span></span>

<span data-ttu-id="98bb4-109">Pri importovaní transakcií kreditnou kartou postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="98bb4-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="98bb4-110">Na stránke **Transakcie kreditnou kartou** vyberte **Importovať transakcie**.</span><span class="sxs-lookup"><span data-stu-id="98bb4-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="98bb4-111">Ak správu údajov otvárate prvýkrát, systém musí najskôr aktualizovať zoznam dátových entít.</span><span class="sxs-lookup"><span data-stu-id="98bb4-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="98bb4-112">V poli **Názov** zadajte jedinečný popis úlohy importu.</span><span class="sxs-lookup"><span data-stu-id="98bb4-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="98bb4-113">V poli **Formát zdrojových údajov** vyberte formát súboru, ktorý obsahuje transakcie kreditnej karty na import.</span><span class="sxs-lookup"><span data-stu-id="98bb4-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="98bb4-114">Vyberte **Nahrať** a potom vyhľadajte a vyberte súbor, ktorý chcete importovať.</span><span class="sxs-lookup"><span data-stu-id="98bb4-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="98bb4-115">Po nahraní súboru overte mapovanie súboru transakcií kreditnou kartou a stĺpcov dátovej entity transakcií kreditnou kartou výberom prepojenia **Zobraziť mapu** na dlaždici.</span><span class="sxs-lookup"><span data-stu-id="98bb4-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="98bb4-116">Ak sa vyskytujú chyby spárovania, alebo ak musíte zmeniť spárovanie, vykonajte zmeny spárovania buď z karty **Vizualizácia spárovania** alebo karty **Podrobnosti spárovania**.</span><span class="sxs-lookup"><span data-stu-id="98bb4-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="98bb4-117">Ak chcete automatizovať transakcie kreditnou kartou, vyberte **Vytvoriť opakujúcu sa dátovú úlohu**.</span><span class="sxs-lookup"><span data-stu-id="98bb4-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="98bb4-118">Potom môžete nastaviť opakovanie, ktoré definuje, ako často sa majú transakcie kreditnou kartou importovať.</span><span class="sxs-lookup"><span data-stu-id="98bb4-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="98bb4-119">Po dokončení vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="98bb4-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="98bb4-120">Ak chcete vybratý súbor importovať teraz, vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="98bb4-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="98bb4-121">Ak sa počas importu vyskytnú chyby, môžete si prezrieť protokol vykonávania alebo údaje o postupe, aby ste videli chyby, ktoré musíte opraviť, aby ste zabezpečili úspešný import.</span><span class="sxs-lookup"><span data-stu-id="98bb4-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="98bb4-122">Ak potrebujete importovať viac ako jeden formát súboru, musíte vytvoriť samostatné úlohy importu pre každý typ formátu.</span><span class="sxs-lookup"><span data-stu-id="98bb4-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="98bb4-123">Zmena priradenia transakcií kreditnou kartou pre ukončených zamestnancov</span><span class="sxs-lookup"><span data-stu-id="98bb4-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="98bb4-124">Po ukončení záznamu zamestnanca je účet zamestnanca služby Active Directory Domain Services (AD DS) deaktivovaný.</span><span class="sxs-lookup"><span data-stu-id="98bb4-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="98bb4-125">Môžu však existovať aktívne transakcie s kreditnými kartami, ktoré sa musia stále zaúčtovať a uhradiť.</span><span class="sxs-lookup"><span data-stu-id="98bb4-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="98bb4-126">Na stránke **Transakcie kreditnou kartou** môžete zamestnanca znova priradiť k akejkoľvek transakcii kreditnou kartou, kde bol priradený zamestnanec prepustený.</span><span class="sxs-lookup"><span data-stu-id="98bb4-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="98bb4-127">Vyberte jednu alebo viac transakcií kreditnou kartou a potom vyberte **Opätovné pridelenie transakcií**.</span><span class="sxs-lookup"><span data-stu-id="98bb4-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="98bb4-128">Potom môžete vybrať iného zamestnanca, ktorému chcete priradiť transakcie kreditnou kartou.</span><span class="sxs-lookup"><span data-stu-id="98bb4-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="98bb4-129">Po opätovnom priradení transakcií kreditnou kartou ich možno vybrať pre výkaz výdavkov a zaplatiť obvyklým spôsobom na úhradu výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="98bb4-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="98bb4-130">Odstránenie transakcií kreditnou kartou</span><span class="sxs-lookup"><span data-stu-id="98bb4-130">Delete credit card transactions</span></span> 

<span data-ttu-id="98bb4-131">Niekedy po importovaní transakcií kreditnou kartou môže byť potrebné niektoré transakcie vymazať.</span><span class="sxs-lookup"><span data-stu-id="98bb4-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="98bb4-132">Môže to byť preto, že transakcie sú duplikáty, alebo preto, že údaje nemusia byť presné.</span><span class="sxs-lookup"><span data-stu-id="98bb4-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="98bb4-133">Správcovia môžu používať funkciu **„Odstrániť transakcie kreditnou kartou“** na výber a odstránenie transakcií kreditnou kartou, ktoré **nie sú pripojené** k výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="98bb4-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="98bb4-134">Prejdite na **Periodické úlohy** > **Odstránenie transakcií kreditnou kartou**.</span><span class="sxs-lookup"><span data-stu-id="98bb4-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="98bb4-135">Vyberte **Filtrovať** a poskytnite informácie na identifikáciu záznamov, ktoré sa majú zahrnúť.</span><span class="sxs-lookup"><span data-stu-id="98bb4-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="98bb4-136">Stlačením možnosti **OK** vymažte záznamy.</span><span class="sxs-lookup"><span data-stu-id="98bb4-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
