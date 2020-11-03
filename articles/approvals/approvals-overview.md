---
title: Prehľad schválení
description: Táto téma poskytuje informácie o práci so schválením v Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084224"
---
# <a name="approvals-overview"></a><span data-ttu-id="c2781-103">Prehľad schválení</span><span class="sxs-lookup"><span data-stu-id="c2781-103">Approvals overview</span></span>

<span data-ttu-id="c2781-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="c2781-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c2781-105">Predloženia času a výdavkov prechádzajú pracovným postupom schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="c2781-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="c2781-106">Po schválení záznamov sa transakcie zaznamenajú do skutočných hodnôt alebo sa čas zarezervuje do harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="c2781-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="c2781-107">Pracovný postup schválenia</span><span class="sxs-lookup"><span data-stu-id="c2781-107">Approvals workflow</span></span>
<span data-ttu-id="c2781-108">Keď vytvoríte a odošlete záznam o čase alebo výdavkoch, vytvorí sa záznam schválenia.</span><span class="sxs-lookup"><span data-stu-id="c2781-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="c2781-109">Schvaľovateľ projektov alebo váš manažér záznam skontroluje a schváli.</span><span class="sxs-lookup"><span data-stu-id="c2781-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="c2781-110">Ak sa záznam týka projektu, po jeho schválení sa vytvoria skutočné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="c2781-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="c2781-111">Vďaka tomu je možné sledovať náklady a fakturácie.</span><span class="sxs-lookup"><span data-stu-id="c2781-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="c2781-112">Schválenie záznamu</span><span class="sxs-lookup"><span data-stu-id="c2781-112">Approve an entry</span></span>
<span data-ttu-id="c2781-113">Formulár **Schválenia** umožňuje prepínať medzi rôznymi zobrazeniami, aby ste si mohli pozrieť rôzne typy schválení.</span><span class="sxs-lookup"><span data-stu-id="c2781-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="c2781-114">Prejdite na formulár **Schválenia** a vyberte **Výdavky** , **Čas** alebo **Odvolania**.</span><span class="sxs-lookup"><span data-stu-id="c2781-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="c2781-115">Skontrolujte každé schválenie a vyberte tie, ktoré chcete schváliť.</span><span class="sxs-lookup"><span data-stu-id="c2781-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="c2781-116">Vyberte **Schváliť** na schválenie vybraných záznamov.</span><span class="sxs-lookup"><span data-stu-id="c2781-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="c2781-117">Systém tieto záznamy spracuje a vytvorí skutočné hodnoty alebo rezerváciu.</span><span class="sxs-lookup"><span data-stu-id="c2781-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="c2781-118">Odmietnutie záznamu</span><span class="sxs-lookup"><span data-stu-id="c2781-118">Reject an entry</span></span>
<span data-ttu-id="c2781-119">Ako schvaľovateľ projektu možno budete musieť poslať záznam späť používateľovi, ktorý ho opraví.</span><span class="sxs-lookup"><span data-stu-id="c2781-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="c2781-120">Prejdite do formulára **Schválenia** a vyberte záznam, ktorý chcete odmietnuť.</span><span class="sxs-lookup"><span data-stu-id="c2781-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="c2781-121">Vyberte **Odmietnuť**.</span><span class="sxs-lookup"><span data-stu-id="c2781-121">Select **Reject**.</span></span>
3. <span data-ttu-id="c2781-122">Voliteľné – pridajte komentár do dialógového okna **Komentáre k odmietnutiu** na informovanie používateľa, prečo je záznam odmietnutý.</span><span class="sxs-lookup"><span data-stu-id="c2781-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="c2781-123">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2781-123">Select **OK**.</span></span> <span data-ttu-id="c2781-124">Položka sa vráti používateľovi.</span><span class="sxs-lookup"><span data-stu-id="c2781-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="c2781-125">Odvolanie záznamov</span><span class="sxs-lookup"><span data-stu-id="c2781-125">Recall entries</span></span>
<span data-ttu-id="c2781-126">V určitom okamihu bude pravdepodobne potrebné odvolať podaný záznam.</span><span class="sxs-lookup"><span data-stu-id="c2781-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="c2781-127">Ak záznam nebol schválený, bude okamžite vrátený.</span><span class="sxs-lookup"><span data-stu-id="c2781-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="c2781-128">Schválený záznam však môže mať podstatný vplyv.</span><span class="sxs-lookup"><span data-stu-id="c2781-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="c2781-129">Schvaľovateľ projektu je povinný schváliť odvolanie, aby sa transakcia stornovala v skutočných hodnotách.</span><span class="sxs-lookup"><span data-stu-id="c2781-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="c2781-130">Špecifikovanie schvaľovateľov projektov</span><span class="sxs-lookup"><span data-stu-id="c2781-130">Specify Project approvers</span></span>
<span data-ttu-id="c2781-131">Každý projekt má niekoľko členov projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="c2781-131">Each project has a number of project team members.</span></span> <span data-ttu-id="c2781-132">Môžete určiť, ktorí členovia tímu sú tiež schvaľovateľmi projektu.</span><span class="sxs-lookup"><span data-stu-id="c2781-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="c2781-133">Prejdite do formulára **Projekty** a otvorte projekt zo zoznamu.</span><span class="sxs-lookup"><span data-stu-id="c2781-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="c2781-134">Na karte **Tím** vyberte člena tímu, ktorý bude schvaľovateľom projektu, a potom vyberte **Upraviť**.</span><span class="sxs-lookup"><span data-stu-id="c2781-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="c2781-135">Nastavte pole **Schvaľovateľ projektu** na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="c2781-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="c2781-136">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="c2781-136">Select **Save**.</span></span>
5. <span data-ttu-id="c2781-137">Ak chcete pridať ďalších schvaľovateľov projektu, zopakujte kroky 2 až 4.</span><span class="sxs-lookup"><span data-stu-id="c2781-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="c2781-138">Konfigurácia manažéra používateľa</span><span class="sxs-lookup"><span data-stu-id="c2781-138">Configure the user's manager</span></span>

1. <span data-ttu-id="c2781-139">Prejdite do položky **Nastavenie** > **Zabezpečenie** > **Používatelia**.</span><span class="sxs-lookup"><span data-stu-id="c2781-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="c2781-140">V zozname vyberte používateľa, ktorému priraďujete manažéra a v oblasti **Informácie o organizácii** vyberte manažéra zo zoznamu.</span><span class="sxs-lookup"><span data-stu-id="c2781-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="c2781-141">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="c2781-141">Select **Save**.</span></span>


