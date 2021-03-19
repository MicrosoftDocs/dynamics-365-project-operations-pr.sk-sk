---
title: Projekty odhadov výnosov s pevnou cenou
description: Táto téma poskytuje informácie o výnosoch s pevnou cenou v projektoch.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278932"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="38d83-103">Projekty odhadov výnosov s pevnou cenou</span><span class="sxs-lookup"><span data-stu-id="38d83-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="38d83-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="38d83-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="38d83-105">Keď vytvoríte riadok projektov zmluvy s nasledujúcimi atribútmi v Dynamics 365 Project Operations v rámci Microsoft Dataverse, systém automaticky vytvorí projekt odhadu výnosov s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="38d83-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="38d83-106">Informácie v tomto projekte vychádzajú z tohto:</span><span class="sxs-lookup"><span data-stu-id="38d83-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="38d83-107">Metóda fakturácie s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="38d83-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="38d83-108">Priradený projekt.</span><span class="sxs-lookup"><span data-stu-id="38d83-108">An associated project.</span></span>
  - <span data-ttu-id="38d83-109">Aspoň jeden míľnik definovaný na karte **Plán faktúry** na stránke **Riadok projektovej zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="38d83-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="38d83-110">Kontrola projektov odhadov výnosov s pevnou cenou</span><span class="sxs-lookup"><span data-stu-id="38d83-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="38d83-111">Ak chcete skontrolovať projekty odhadov výnosov s pevnou cenou, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="38d83-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="38d83-112">V prostredí Dynamics 365 Finance prejdite na **Projektový manažment a účtovníctvo** > **Projekty** > **Projekty odhadov výnosov s pevnou cenou**.</span><span class="sxs-lookup"><span data-stu-id="38d83-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="38d83-113">Vyberte projekt, ktorý chcete zobraziť, a dvojitým kliknutím na **Odhad ID projektu** otvorte záznam a skontrolujte podrobnosti o projekte.</span><span class="sxs-lookup"><span data-stu-id="38d83-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="38d83-114">Rozbaľte kartu **Projekt**. Jeden projekt uvidíte v mriežke **Vybrané projekty**.</span><span class="sxs-lookup"><span data-stu-id="38d83-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="38d83-115">Systém to používa ako predvolený projekt, pretože ide o projekt priradený k riadku projektovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="38d83-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="38d83-116">Ak chcete zmeniť pridruženie, vyberte ďalšie projekty a pridajte ich do mriežky **Vybrané projekty**.</span><span class="sxs-lookup"><span data-stu-id="38d83-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="38d83-117">Ak je v tejto mriežke vybratých viac projektov, vypočíta sa percento dokončenia projektu a odhady výnosov pre všetky vybrané projekty.</span><span class="sxs-lookup"><span data-stu-id="38d83-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="38d83-118">Náklady na projekt, profil výnosov, šablónu nákladov a kód obdobia je možné nastaviť ručne.</span><span class="sxs-lookup"><span data-stu-id="38d83-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="38d83-119">Ak nie sú nastavené ručne, hodnoty sa nastavia predvolene počas prvého výpočtu odhadu pre projekt pomocou pravidiel nakonfigurovaných pre profily nákladov a výnosov projektu.</span><span class="sxs-lookup"><span data-stu-id="38d83-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]