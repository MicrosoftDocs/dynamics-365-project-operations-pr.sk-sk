---
title: Riešenie problémov s prácou v mriežke úloh
description: Táto téma poskytuje informácie o riešení problémov potrebných pri práci v mriežke úloh.
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213419"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="09ea8-103">Riešenie problémov s prácou v mriežke úloh</span><span class="sxs-lookup"><span data-stu-id="09ea8-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="09ea8-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="09ea8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="09ea8-105">Táto téma popisuje, ako opraviť problémy, s ktorými sa môžete stretnúť pri práci so správou nákladov.</span><span class="sxs-lookup"><span data-stu-id="09ea8-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="09ea8-106">Povoliť súbory cookie</span><span class="sxs-lookup"><span data-stu-id="09ea8-106">Enable cookies</span></span>

<span data-ttu-id="09ea8-107">Project Operations vyžaduje, aby boli povolené súbory cookie tretích strán, aby sa zobrazila štruktúra rozdelenia práce.</span><span class="sxs-lookup"><span data-stu-id="09ea8-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="09ea8-108">Ak súbory cookie tretích strán nie sú povolené, namiesto zobrazenia úloh sa po výbere karty **Úlohy** na stránke **Projekt** zobrazí prázdna stránka.</span><span class="sxs-lookup"><span data-stu-id="09ea8-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Prázdna karta, keď nie sú povolené súbory cookie tretích strán](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="09ea8-110">Riešenie</span><span class="sxs-lookup"><span data-stu-id="09ea8-110">Workaround</span></span>
<span data-ttu-id="09ea8-111">V prípade prehliadačov Microsoft Edge alebo Google Chrome nasledujúce postupy naznačujú, ako aktualizovať nastavenie prehliadača tak, aby boli povolené súbory cookie tretích strán.</span><span class="sxs-lookup"><span data-stu-id="09ea8-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="09ea8-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="09ea8-112">Microsoft Edge</span></span>

1. <span data-ttu-id="09ea8-113">Otvorte prehľadávač Edge.</span><span class="sxs-lookup"><span data-stu-id="09ea8-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="09ea8-114">V pravom hornom rohu vyberte **tri bodky** (...) a následne vyberte položku **Nastavenia**.</span><span class="sxs-lookup"><span data-stu-id="09ea8-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="09ea8-115">V časti **Súbory cookie a povolenia lokality** vyberte **Súbory cookie a údaje o lokalite**.</span><span class="sxs-lookup"><span data-stu-id="09ea8-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="09ea8-116">Vypnite **Blokovať súbory cookie tretích strán**.</span><span class="sxs-lookup"><span data-stu-id="09ea8-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="09ea8-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="09ea8-117">Google Chrome</span></span>

1. <span data-ttu-id="09ea8-118">Otvorte prehľadávač Chrome.</span><span class="sxs-lookup"><span data-stu-id="09ea8-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="09ea8-119">V pravom hornom rohu vyberte tri zvislé bodky a potom vyberte položku **Nastavenia**.</span><span class="sxs-lookup"><span data-stu-id="09ea8-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="09ea8-120">V časti **Ochrana osobných údajov a zabezpečenie** vyberte **Súbory cookie a iné údaje o lokalite**.</span><span class="sxs-lookup"><span data-stu-id="09ea8-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="09ea8-121">Vyberte **Povoliť všetky súbory cookie**.</span><span class="sxs-lookup"><span data-stu-id="09ea8-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09ea8-122">Ak zablokujete súbory cookie tretích strán, zablokujú sa všetky súbory cookie a údaje lokalít z iných webov, aj keď je tento web povolený vo vašom zozname výnimiek.</span><span class="sxs-lookup"><span data-stu-id="09ea8-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="09ea8-123">Koncový bod PEX</span><span class="sxs-lookup"><span data-stu-id="09ea8-123">PEX Endpoint</span></span>

<span data-ttu-id="09ea8-124">Project Operations vyžaduje, aby parameter projektu odkazoval na koncový bod PEX.</span><span class="sxs-lookup"><span data-stu-id="09ea8-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="09ea8-125">Tento koncový bod je potrebný na komunikáciu so službou použitou na vykreslenie štruktúry rozdelenia práce.</span><span class="sxs-lookup"><span data-stu-id="09ea8-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="09ea8-126">Ak parameter nie je povolený, zobrazí sa chyba „Parameter projektu nie je platný“.</span><span class="sxs-lookup"><span data-stu-id="09ea8-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="09ea8-127">Riešenie</span><span class="sxs-lookup"><span data-stu-id="09ea8-127">Workaround</span></span>
 ![Pole Koncový bod PEX v parametri projektu](media/projectparameter.png)

1. <span data-ttu-id="09ea8-129">Pridajte pole **Koncový bod PEX** na stránke **Parametre projektu**.</span><span class="sxs-lookup"><span data-stu-id="09ea8-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="09ea8-130">Aktualizujte pole o túto hodnotu: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="09ea8-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span></span>
3. <span data-ttu-id="09ea8-131">Odstráňte pole zo stránky **Parametre projektu**.</span><span class="sxs-lookup"><span data-stu-id="09ea8-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="09ea8-132">Oprávnenia pre Project for Web</span><span class="sxs-lookup"><span data-stu-id="09ea8-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="09ea8-133">Project Operations sa spolieha na externú plánovaciu službu.</span><span class="sxs-lookup"><span data-stu-id="09ea8-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="09ea8-134">Táto služba vyžaduje, aby mal používateľ priradených niekoľko rol na čítanie a zápis do entít týkajúcich sa štruktúry rozdelenia práce.</span><span class="sxs-lookup"><span data-stu-id="09ea8-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="09ea8-135">Medzi tieto entity patria projektové úlohy, priradenia zdrojov a závislosti úloh.</span><span class="sxs-lookup"><span data-stu-id="09ea8-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="09ea8-136">Ak používateľ nemôže pri prechode na kartu **Úlohy** vykresliť štruktúru rozdelenia práce, je to pravdepodobne preto, že nebol povolený projekt pre Project Operations.</span><span class="sxs-lookup"><span data-stu-id="09ea8-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="09ea8-137">Používateľ môže dostať buď chybu roly zabezpečenia, alebo chybu súvisiacu s odmietnutím prístupu.</span><span class="sxs-lookup"><span data-stu-id="09ea8-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="09ea8-138">Riešenie</span><span class="sxs-lookup"><span data-stu-id="09ea8-138">Workaround</span></span>

1. <span data-ttu-id="09ea8-139">Prejdite na **Nastavenie > Zabezpečenie > Používatelia > Používatelia aplikácie**.</span><span class="sxs-lookup"><span data-stu-id="09ea8-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Čítačka aplikácie](media/applicationuser.jpg)
   
2. <span data-ttu-id="09ea8-141">Dvakrát kliknite na záznam používateľa aplikácie a overte nasledovné:</span><span class="sxs-lookup"><span data-stu-id="09ea8-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="09ea8-142">Používateľ má prístup k projektu.</span><span class="sxs-lookup"><span data-stu-id="09ea8-142">The user has access to the project.</span></span> <span data-ttu-id="09ea8-143">Toto overenie sa zvyčajne vykonáva tak, že sa zabezpečí, že používateľ má rolu zabezpečenia **Projektový manažér**.</span><span class="sxs-lookup"><span data-stu-id="09ea8-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="09ea8-144">Používateľ aplikácie Microsoft Project existuje a je správne nakonfigurovaný.</span><span class="sxs-lookup"><span data-stu-id="09ea8-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="09ea8-145">Ak tento používateľ neexistuje, môžete vytvoriť nový záznam používateľa.</span><span class="sxs-lookup"><span data-stu-id="09ea8-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="09ea8-146">Vyberte **Noví používatelia**.</span><span class="sxs-lookup"><span data-stu-id="09ea8-146">Select **New Users**.</span></span> <span data-ttu-id="09ea8-147">Zmeňte formulár na zadávanie v časti **Používateľ aplikácie** a potom pridajte **ID aplikácie**.</span><span class="sxs-lookup"><span data-stu-id="09ea8-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Podrobnosti o používateľovi aplikácie](media/applicationuserdetails.jpg)

4. <span data-ttu-id="09ea8-149">Skontrolujte, či používateľovi bola pridelená správna licencia a či je služba povolená v podrobnostiach plánu služieb licencie.</span><span class="sxs-lookup"><span data-stu-id="09ea8-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="09ea8-150">Overte, či môže používateľ otvoriť project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="09ea8-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="09ea8-151">Prostredníctvom parametrov projektu overte, či systém ukazuje na správny koncový bod projektu.</span><span class="sxs-lookup"><span data-stu-id="09ea8-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="09ea8-152">Overte, či je vytvorený užívateľ projektovej aplikácie.</span><span class="sxs-lookup"><span data-stu-id="09ea8-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="09ea8-153">Aplikujte na používateľa nasledujúce roly zabezpečenia:</span><span class="sxs-lookup"><span data-stu-id="09ea8-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="09ea8-154">Používateľ služby Dataverse</span><span class="sxs-lookup"><span data-stu-id="09ea8-154">Dataverse User</span></span>
  - <span data-ttu-id="09ea8-155">Systém riešenia Project Operations</span><span class="sxs-lookup"><span data-stu-id="09ea8-155">Project Operations System</span></span>
  - <span data-ttu-id="09ea8-156">Systém projektu</span><span class="sxs-lookup"><span data-stu-id="09ea8-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="09ea8-157">Chyba pri aktualizácii štruktúry rozdelenia práce</span><span class="sxs-lookup"><span data-stu-id="09ea8-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="09ea8-158">Keď sa vykoná jedna alebo viac aktualizácií štruktúry rozdelenia práce, zmeny nakoniec zlyhajú a neuložia sa.</span><span class="sxs-lookup"><span data-stu-id="09ea8-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="09ea8-159">V mriežke rozvrhu sa vyskytla chyba a upozornila, že „Poslednú zmenu, ktorú ste vykonali, sa nepodarilo uložiť.“</span><span class="sxs-lookup"><span data-stu-id="09ea8-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="09ea8-160">Riešenie</span><span class="sxs-lookup"><span data-stu-id="09ea8-160">Workaround</span></span>

1. <span data-ttu-id="09ea8-161">Skontrolujte, či používateľovi bola pridelená správna licencia a či je služba povolená v podrobnostiach plánu služieb licencie.</span><span class="sxs-lookup"><span data-stu-id="09ea8-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="09ea8-162">Overte, či môže používateľ otvoriť project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="09ea8-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="09ea8-163">Overte, či systém ukazuje na správny koncový bod projektu.</span><span class="sxs-lookup"><span data-stu-id="09ea8-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="09ea8-164">Overte, či bol vytvorený užívateľ projektovej aplikácie.</span><span class="sxs-lookup"><span data-stu-id="09ea8-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="09ea8-165">Aplikujte na používateľa nasledujúce roly zabezpečenia:</span><span class="sxs-lookup"><span data-stu-id="09ea8-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="09ea8-166">Používateľ Dataverse alebo základný používateľ</span><span class="sxs-lookup"><span data-stu-id="09ea8-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="09ea8-167">Systém riešenia Project Operations</span><span class="sxs-lookup"><span data-stu-id="09ea8-167">Project Operations System</span></span>
  - <span data-ttu-id="09ea8-168">Systém projektu</span><span class="sxs-lookup"><span data-stu-id="09ea8-168">Project System</span></span>
  - <span data-ttu-id="09ea8-169">Systém dvojitého zápisu Project Operations (táto rola je vyžadovaná, ak v Project Operations nasadzujete scenár založený na zdrojoch/chýbajúcich zdrojoch.)</span><span class="sxs-lookup"><span data-stu-id="09ea8-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
