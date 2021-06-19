---
title: Práca s osobnými výdavkami vo výkaze výdavkov
description: Táto téma poskytuje informácie o tom, ako pracovať s osobnými výdavkami, ktoré vzniknú zamestnancom pri cestovaní na služobné účely.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025703"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="5040c-103">Práca s osobnými výdavkami vo výkaze výdavkov</span><span class="sxs-lookup"><span data-stu-id="5040c-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="5040c-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="5040c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5040c-105">Počas služobnej cesty môže zamestnanec účtovať osobné náklady na svoju podnikovú kreditnú kartu.</span><span class="sxs-lookup"><span data-stu-id="5040c-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="5040c-106">Ak nebol definovaný proces vybavovania osobných výdavkov, proces schválenia výkazu výdavkov môže byť narušený, keď zamestnanec predloží svoj podrobný výkaz výdavkov.</span><span class="sxs-lookup"><span data-stu-id="5040c-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="5040c-107">Existujú dve metódy, ktoré môžete použiť na prácu s osobnými výdavkami zamestnanca:</span><span class="sxs-lookup"><span data-stu-id="5040c-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="5040c-108">**Platené zamestnancom**: Vaša organizácia neplatí osobné náklady, ktoré sú uvedené na účte za firemnú kreditnú kartu.</span><span class="sxs-lookup"><span data-stu-id="5040c-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="5040c-109">Zamestnanec namiesto toho platí výdavky priamo predajcovi kreditných kariet.</span><span class="sxs-lookup"><span data-stu-id="5040c-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="5040c-110">**Zaplatené spoločnosťou**: Vaša organizácia zaplatí celý účet za podnikovú kreditnú kartu a potom z účtu zamestnanca strhne osobné náklady.</span><span class="sxs-lookup"><span data-stu-id="5040c-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="5040c-111">Metódu využívanú vašou spoločnosťou môžete zmeniť na stránke **Parametre správy výdavkov**.</span><span class="sxs-lookup"><span data-stu-id="5040c-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="5040c-112">Povolenie funkcie rozdelených výdavkov, keď má pole s osobnou sumou definovanú hodnotu</span><span class="sxs-lookup"><span data-stu-id="5040c-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="5040c-113">Funkcia **Povoliť funkciu rozdelených výdavkov, keď má pole s osobnou sumou definovanú hodnotu** platí iba pre výkazy o výdavkoch, ktoré sa schvaľujú pomocou pracovného postupu na úrovni riadku.</span><span class="sxs-lookup"><span data-stu-id="5040c-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="5040c-114">Správy sa schvaľujú tak, že prejdete na **Spracovať výkazy o výdavkoch** > **Výkazy o výdavkoch pridelené mne** > **Otvoriť výkaz o výdavkoch**.</span><span class="sxs-lookup"><span data-stu-id="5040c-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="5040c-115">Ak chcete povoliť túto funkciu, prejdite na časť **Pracovné priestory** > **Správa funkcií**, vyberte možnosť **Povoliť funkciu rozdelených výdavkov, keď má pole s osobnou sumou definovanú hodnotu** a potom vyberte možnosť **Povoliť teraz**.</span><span class="sxs-lookup"><span data-stu-id="5040c-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="5040c-116">Keď je táto funkcia povolená, riadky výdavkov, ktoré využívajú túto funkciu, vygenerujú po odoslaní výkazu dva riadky.</span><span class="sxs-lookup"><span data-stu-id="5040c-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="5040c-117">Vygenerujú sa dva riadky, aby schvaľovateľ mohol schváliť každý riadok samostatne.</span><span class="sxs-lookup"><span data-stu-id="5040c-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
