---
title: Rezervácia pomenovaných rezervovateľných zdrojov pre projektový tímu a priradenie úloh
description: Táto téma poskytuje informácie o spôsobe rezervovania pomenovaných zdrojov pre projektové tímy a ich priradenia k úlohám.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cdbcd84d2277ba1c8e68270d5b1f8ca45c17f05e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575369"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Rezervácia pomenovaných rezervovateľných zdrojov pre projektový tímu a priradenie úloh 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Môžete pridať pomenovaný zdroj do projektového tímu jeho rezerváciou priamo do tímu. Ak to chcete urobiť, postupujte podľa nasledujúcich krokov.

1. V Project Service Automation, prejdite na **Projects**, a vyberte otvoriť projekt, pre ktorý robíte rezerváciu.
2. Na stránke **Project** na karte **Team** kliknite na **New**. 

![Pridanie člena tímu z karty tímu.](media/RM-how-to-1.png)

3. V dialógovom okne **Quick Create Project Team Member** vyberte rezervovateľný zdroj. Pole **Rola** sa vyplní predvolenou úlohou prostriedku, ak má jeden priradený. Môžete zmeniť rolu podľa potreby. 
4. Vyberte z a do dátumov, že zdroj bude potrebný a vyberte spôsob pridelenia kapacity zdroja. 
5. Ak chcete, aby bol člen tímu schvaľovateľ projektu, vyberte **Yes** v poli **Project Approver**. To bude znamenať, že člen tímu môže schváliť odoslané časové a výdavkové záznamy pre tento projekt. 
6. Kliknite na tlačidlo **Uložiť**.

![Pridanie člena tímu do formulára rýchleho vytvorenia.](media/RM-how-to-2.png)


Teraz môžete priradiť rezervovaný zdroj k úlohám v projekte. Na stránke **Project** kliknite na kartu **Schedule** na priradenie úloh k novému zdroju. Výber zdroja, ktorý sa spúšťa z poľa **Resources** v mriežke úloh, zobrazí členov tímu, ktorých môžete vybrať.

![Priradenie člena tímu k úlohe na tabuli plánovania.](media/RM-how-to-3.png)

Vo verzii 3 pre Project Service Automation (PSA), rezervované zdroje a priradenia úloh nie sú tesne spojené. To znamená, že keď použijete výber zdrojov v pláne, môžete priradiť úlohy členom tímu na viac hodín ako pokrývajú ich rezervácie projektu.
Rozdiely medzi rezerváciami členov tímu a priradeniami môžete vidieť na karte **Team** alebo na karte **Resource Reconciliation**. Môžete tiež zosúladiť rozdiely medzi rezerváciami a priradeniami pre zdroje na podrobnejšej úrovni.

![Tabuľka odsúhlasenia zdrojov.](media/RM-how-to-4.png)

Môžete tiež použiť výber zdrojov, na karte **Plán** k vyhľadaniu vybraných rezervovateľných zdrojov, ktoré nie súčasťou projektového tímu. Tieto sú uvedené vo výbere zdrojov ako **Other Resources**.

![Priradenie zdroja ktorý nie je členom tímu, k úlohe.](media/RM-how-to-5.png)

Keď to urobíte, zdroj je pridaný do projektového tímu a priradený k úlohe, ale nie sú generované žiadne rezervácie.

![Člen tímu s úlohami a bez rezervácií.](media/RM-how-to-6.png)

Môžete použiť **Reconciliation** na zväčšenie tabuľkovej rezervačnej schopnosti alebo **Schedule Board** na rezerváciu zdrojovej kapacity pre projekt.

![Rozšírenie rezervácií pre člena tímu na karte odsúhlasenie zdroja.](media/RM-how-to-7.png)

Po tom, ako sa člen tímu rezervuje na váš projekt, môžete použiť spravovanie rezervácií alebo nástenku plánovania priamo na spravovanie ich rezervácií.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
