---
title: Konfigurácia účtovníctva pre interné projekty
description: Táto téma poskytuje informácie o tom, ako nastaviť účtovné postupy pre interné projekty v aplikácii Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084298"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="ae667-103">Konfigurácia účtovníctva pre interné projekty</span><span class="sxs-lookup"><span data-stu-id="ae667-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="ae667-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="ae667-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ae667-105">Interné projekty umožňujú spoločnostiam sledovať náklady spojené s činnosťami, ktoré sa zákazníkom neúčtujú.</span><span class="sxs-lookup"><span data-stu-id="ae667-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="ae667-106">Príklady interných projektov zahŕňajú:</span><span class="sxs-lookup"><span data-stu-id="ae667-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="ae667-107">Vývoj produktu, napríklad mobilnej aplikácie, a sledovanie nákladov spojených s vývojom.</span><span class="sxs-lookup"><span data-stu-id="ae667-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="ae667-108">Správa času a výdavkov pred predajom.</span><span class="sxs-lookup"><span data-stu-id="ae667-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="ae667-109">Tento interný projekt pred predajom je možné neskôr previesť na fakturovateľný projekt v prípade získania cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="ae667-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="ae667-110">S akýmkoľvek projektom, ktorý nie je spojený so zmluvou v Dynamics 365 Project Operations, sa zaobchádza ako s interným.</span><span class="sxs-lookup"><span data-stu-id="ae667-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="ae667-111">Profily nákladov a výnosov projektu sa nepoužívajú na určenie účtovných pravidiel projektu.</span><span class="sxs-lookup"><span data-stu-id="ae667-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="ae667-112">Náklady na interné projekty sa vždy účtujú pomocou zásad ziskov a strát.</span><span class="sxs-lookup"><span data-stu-id="ae667-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="ae667-113">Účty hlavnej knihy pre zverejňovania sú definované na stránke **Nastavenia zverejňovania v hlavnej knihe**.</span><span class="sxs-lookup"><span data-stu-id="ae667-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="ae667-114">Časové transakcie sa zverejňujú zaúčtovaním účtu **Náklady** a pripísaním na účet **Alokácia miezd**.</span><span class="sxs-lookup"><span data-stu-id="ae667-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="ae667-115">Výdavkové transakcie sa zverejňujú zaúčtovaním účtu **Náklady** a pripísaním na **Účet s odchýlkami pre výdavky**.</span><span class="sxs-lookup"><span data-stu-id="ae667-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="ae667-116">Po pridaní transakcií do projektu, ak je projekt spojený so zmluvou o projekte, systém vráti všetky akumulované transakcie a vytvorí nové fakturovateľné transakcie.</span><span class="sxs-lookup"><span data-stu-id="ae667-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="ae667-117">Fakturovateľné transakcie sa riadia účtovnými pravidlami definovanými v príslušnom profile nákladov a výnosov projektu.</span><span class="sxs-lookup"><span data-stu-id="ae667-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


