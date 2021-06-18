---
title: Ako prispôsobiť projektové fázy toku obchodného procesu?
description: Prehľad ako môžte prispôsobiť tok obchodného procesu v rámci etáp projektu?
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2e6c60fe67aea908013077bde40c2faeabc2f39e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993165"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="7c397-103">Ako prispôsobiť projektové fázy toku obchodného procesu?</span><span class="sxs-lookup"><span data-stu-id="7c397-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="7c397-104">Je známe obmedzenia v starších verziách aplikácie Project Service že mená etapy projektu fázach pracovného procesu sa musia presne s očakávanými anglickými názvami (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="7c397-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="7c397-105">V opačnom prípade nebude obchodná logika, ktorá sa spolieha na názvy fáz v angličtine, pracovať podľa očakávaní.</span><span class="sxs-lookup"><span data-stu-id="7c397-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="7c397-106">To je dôvod, prečo nevidíte známe akcie, akými sú **Prepnúť proces** alebo **Upraviť proces** na formulári projektu a nie je podporovaná ani možnosť prispôsobenia toku obchodného procesu.</span><span class="sxs-lookup"><span data-stu-id="7c397-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="7c397-107">Toto obmedzenie bolo vyriešené vo verzii 2.4.5.48 a novšej.</span><span class="sxs-lookup"><span data-stu-id="7c397-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="7c397-108">Tento článok poskytuje navrhované riešenia pre staršie verzie, ak potrebujete prispôsobenie predvoleného toku obchodného procesu pre staršie verzie.</span><span class="sxs-lookup"><span data-stu-id="7c397-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="7c397-109">Obchodná logika si vyžaduje presnú zhodu s anglickými názvami fáz</span><span class="sxs-lookup"><span data-stu-id="7c397-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="7c397-110">Projektové fázy toku obchodných procesov zahŕňajú obchodnú logiku, ktorá poháňa nasledujúce správania v aplikácii:</span><span class="sxs-lookup"><span data-stu-id="7c397-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="7c397-111">Keď sa projekt priradí k cenovej ponuke, kód nastaví tok obchodného procesu na fázu **Quote**.</span><span class="sxs-lookup"><span data-stu-id="7c397-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="7c397-112">Keď sa projekt priradí ku zmluve, kód nastaví tok obchodného procesu na fázu **Plan**.</span><span class="sxs-lookup"><span data-stu-id="7c397-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="7c397-113">Keď tok obchodného procesu prejde do fázy **Close**, záznam projektu sa deaktivuje.</span><span class="sxs-lookup"><span data-stu-id="7c397-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="7c397-114">Ak je deaktivovaný projektu, projektový formulár a prácu štruktúru činností (WBS) sú nastavené iba na čítanie, pomenovaných zdrojov rezervácie sú uvoľnené a akékoľvek priradené Cenníky sú deaktivované.</span><span class="sxs-lookup"><span data-stu-id="7c397-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="7c397-115">Tento biznis logika sa opiera o anglické názvy pre fázy projektu.</span><span class="sxs-lookup"><span data-stu-id="7c397-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="7c397-116">Táto závislosti na anglických názvoch fáz predstavuje hlavný dôvod, prečo sa neodporúča upravovať fázy projektu toku obchodného procesu. Rovnako pre to tiež nevidíte spoločné akcie toku obchodných procesov, akými je **Prepnúť proces** alebo **Upraviť proces** v entite projektu.</span><span class="sxs-lookup"><span data-stu-id="7c397-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="7c397-117">Čo sa stane, ak sa názov fázy nebude hodovať s anglickými názvami?</span><span class="sxs-lookup"><span data-stu-id="7c397-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="7c397-118">V aplikácii Project Service verzie 1.x na platforme 8.2, keď sa názov etapy v toku obchodných procesov presne nezhodujú s anglickými názvami etapy, obchodná logika, ktorá nastavuje správnu etapu cenových ponúk alebo zmlúv, alebo tá, ktorá projektu uzatvára, bude preskočená.</span><span class="sxs-lookup"><span data-stu-id="7c397-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="7c397-119">Nezobrazia sa žiadne chybové hlásenia.</span><span class="sxs-lookup"><span data-stu-id="7c397-119">No error messages are displayed.</span></span> <span data-ttu-id="7c397-120">Z toho dôvodu sa zdá, že nemôžete upravovať tok obchodného procesu fáz projektu.</span><span class="sxs-lookup"><span data-stu-id="7c397-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="7c397-121">Nezobrazia sa vám však ani žiadne automatické procesy pracujúce na cenových ponukách, zmluvách a uzatváraní projektu.</span><span class="sxs-lookup"><span data-stu-id="7c397-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="7c397-122">V aplikácii Project Service verzie 2.4.4.30 alebo novšej na platforme 9.0 došlo k výraznej architektonickej zmene toku obchodných procesov, ktorá si vyžadovala prepísanie obchodnej logiky toku obchodného procesu.</span><span class="sxs-lookup"><span data-stu-id="7c397-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="7c397-123">Výsledkom je, že v prípade, ak sa názvy etapy procesu nezhodujú s očakávanými anglickými názvami, zobrazí sa vám chybové hlásenie.</span><span class="sxs-lookup"><span data-stu-id="7c397-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="7c397-124">Preto ak chcete prispôsobiť projektové fázy pracovného procesu pre projekt entitu, môžete len pridať zbrusu novej etapy do predvoleného pracovného procesu pre projekt subjektu, pričom ponecháte etapy **Cenová ponuka**, **Plán** a **Zavrieť** tak, ako sú.</span><span class="sxs-lookup"><span data-stu-id="7c397-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="7c397-125">Toto obmedzenie zaisťuje, že sa vám nebudú zobrazovať chyby z obchodnej logiky, ktorá očakáva v toku obchodných procesov anglické názvy etáp.</span><span class="sxs-lookup"><span data-stu-id="7c397-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="7c397-126">Vo verzii 2.4.5.48 alebo novšej bola obchodná logika popísaná v tomto článku odstránená z predvoleného toku obchodného procesu pre entitu projektu.</span><span class="sxs-lookup"><span data-stu-id="7c397-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="7c397-127">Inováciou na danú alebo novšiu verziu budete môcť upravovať alebo nahrádzať predvolený tok obchodného procesu tým vlastným.</span><span class="sxs-lookup"><span data-stu-id="7c397-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="7c397-128">Riešenia pre staršie verzie</span><span class="sxs-lookup"><span data-stu-id="7c397-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="7c397-129">Ak inovácia nie je možnosť, môžete prispôsobiť projektové fázy toku obchodného procesu pre projektovú entitu jedným z týchto dvoch spôsobov:</span><span class="sxs-lookup"><span data-stu-id="7c397-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="7c397-130">Pridať ďalšie etapy s predvolenou konfiguráciou, pri zachovaní anglicky fáze mená pre **Cenová ponuka**, **Plán**, a **Zavrieť**.</span><span class="sxs-lookup"><span data-stu-id="7c397-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Snímka obrazovky pridávania etáp k predvolenej konfigurácii](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="7c397-132">Vytvorte si vlastný tok obchodných procesov a nastavte ho ako hlavný tok obchodných procesov pre entitu projektu, čo vám umožní mať ľubovoľné názvy etáp.</span><span class="sxs-lookup"><span data-stu-id="7c397-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="7c397-133">Ak však chcete používať rovnaké štandardné projektové etapy **Cenová ponuka**, **Plán** a **Zatvoriť**, budete musieť vykonať niekoľko prispôsobení, ktoré sú odvodené od vlastných názvov etáp.</span><span class="sxs-lookup"><span data-stu-id="7c397-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="7c397-134">Komplexnejšia logika sa využíva pri zatváraní projektu, čo možno aj naďalej spustiť obyčajnou deaktiváciou záznamu projektu.</span><span class="sxs-lookup"><span data-stu-id="7c397-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Prispôsobenie BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="7c397-136">Ďalšie pokyny pre aplikáciu Project Service verzie 2.4.4.30 alebo staršej na platforme 9.0</span><span class="sxs-lookup"><span data-stu-id="7c397-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="7c397-137">V Project Service 2.4.4.30 alebo staršej na platforme 9.0 sa s vlastným tokom obchodného procesu pole **Názov etapy** v projektovej entite použitej v grafe **Projekt podľa etapy** v zobrazení zoznamov projektov neaktualizuje, pretože je spojené s predvoleným tokom obchodných procesov projektových etáp.</span><span class="sxs-lookup"><span data-stu-id="7c397-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="7c397-138">Tento problém možno riešiť nasledovným postupom:</span><span class="sxs-lookup"><span data-stu-id="7c397-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="7c397-139">Pridajte vlastné pole, ktoré zachytí aktuálnu etapu toku obchodného procesu, ktorá sa aktualizuje vtedy, keď používateľ pokračuje vo vlastnom toku obchodného procesu.</span><span class="sxs-lookup"><span data-stu-id="7c397-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="7c397-140">Upravte graf **Projekt podľa etapy** tak, aby vyhovoval vlastnému poľu a nie predvolenej konfigurácii.</span><span class="sxs-lookup"><span data-stu-id="7c397-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="7c397-141">Kroky na vytvorenie vlastného toku obchodného procesu pre entitu projektu</span><span class="sxs-lookup"><span data-stu-id="7c397-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="7c397-142">Na vytvorenie vlastného toku obchodného procesu pre entitu projektu postupujte nasledovne:</span><span class="sxs-lookup"><span data-stu-id="7c397-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="7c397-143">Prejdite do časti **Nastavenia** > **Centrum spracovania**.</span><span class="sxs-lookup"><span data-stu-id="7c397-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="7c397-144">Nekopírujte projektové fázy toku obchodného procesu, pretože sa tým skopíruje aj obchodná logika Project Service.</span><span class="sxs-lookup"><span data-stu-id="7c397-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Vytvoriť proces](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="7c397-146">Návrhár procesov použite na vytvorenie požadovaných názvov etapy.</span><span class="sxs-lookup"><span data-stu-id="7c397-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="7c397-147">Ak chcete rovnaké funkcie ako predvolené etapy pre **Cenová ponuka**, **Plán** a **Zavrieť**, budete to musieť vytvoriť na základe vlastných názvov fáz toku obchodného procesu.</span><span class="sxs-lookup"><span data-stu-id="7c397-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Snímka obrazovky návrhára procesov použitého pri prispôsobovaní BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="7c397-149">V návrhárovi procesu kliknite na možnosť **Tok procesu objednávky** a nastavte vlastný tok obchodných procesov ako hlavný tok obchodných procesov pre entitu projektu jeho presunutím nad etapy projektu toku obchodného procesu do hornej časti zoznamu.</span><span class="sxs-lookup"><span data-stu-id="7c397-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="7c397-150">Snímka obrazovky používania Toku procesu objednávky</span><span class="sxs-lookup"><span data-stu-id="7c397-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="7c397-151">Nasledujúce kroky platia pre aplikáciu Project Service 2.4.4.30 alebo staršiu na platforme 9.0</span><span class="sxs-lookup"><span data-stu-id="7c397-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="7c397-152">Pridajte nové vlastné pole k entite projektu tak, aby zachytilo vlastné etapy vo vlastnom toku obchodných procesov.</span><span class="sxs-lookup"><span data-stu-id="7c397-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="7c397-153">Budete musieť pridať obchodnú logiku (plugin/workflow) na aktualizáciu tohto poľa po aktualizácii etapy vo vlastnom toku obchodných procesov.</span><span class="sxs-lookup"><span data-stu-id="7c397-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Snímka obrazovky prispôsobenia projektovej entity](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="7c397-155">Upravte graf **Projekt podľa etapy** a použite nové vlastné pole pre etapy.</span><span class="sxs-lookup"><span data-stu-id="7c397-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Snímka obrazovky použitia grafu Projekt podľa etapy](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="7c397-157">Upravte akékoľvek zobrazenia pre entity projektu ,ktoré budú zahŕňať vaše nové vlastné pole pre etapy.</span><span class="sxs-lookup"><span data-stu-id="7c397-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Snímka obrazovky úpravy zobrazení projektovej entity](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]