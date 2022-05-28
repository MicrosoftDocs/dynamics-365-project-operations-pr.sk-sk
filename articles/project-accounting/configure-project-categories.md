---
title: Konfigurácia kategórií projektov
description: Táto téma poskytuje informácie o nastavovaní kategórií projektov.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 94b66feef4164f3cd52d5fe917071647f731b047
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591561"
---
# <a name="configure-project-categories"></a>Konfigurácia kategórií projektov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Project Operations ponúka rozsiahle možnosti kategorizácie výnosov a výdavkov na projekty. Kategórie poskytujú schopnosť reportovať a analyzovať projektové transakcie a riadiť účtovanie do všeobecnej hlavnej knihy.

Nasledujúci diagram ilustruje koreláciu medzi kategóriami transakcií, zdieľanými kategóriami a kategóriami projektu. 

Kategórie transakcií sú základným zoskupením pre projektové transakcie. V rámci tohto zoskupenia existuje skupina zdieľaných kategórií, ktoré je možné zdieľať medzi aplikáciami a modulmi. Keď sa pozrieme ešte ďalej na špecifiká, kategórie projektov sú najpodrobnejšou úrovňou kategórií. Kategórie projektov sú špecifické pre právnické osoby, moduly a aplikácie.

![Korelácia medzi kategóriami transakcií, zdieľanými kategóriami a kategóriami projektu.](media/project-categories.png)

## <a name="transaction-categories"></a>Kategórie transakcií

Kategórie transakcií predstavujú základné zoskupenie pre projektové transakcie a nie sú špecifické pre spoločnosť alebo typ transakcie. Spoločnosť Contoso Robotics napríklad používa na zoskupenie transakcií projektu kategórie Dizajn, Cestovanie, Inštalácia a Transakcie služieb.

Kategórie transakcií sú definované v module Project Operations. 
1. Prejdite do **Nastavenia** \> **Kategórie transakcií** na otvorenie formulára. 
2. Vytvorte novú kategóriu transakcií výberom možnosti **Nová** alebo výberom možnosti **Import z programu Excel**.

## <a name="shared-categories"></a>Zdieľané kategórie

Dynamics 365 používa koncept zdieľaných kategórií na kategorizáciu výdavkov v rôznych aplikáciách, ako sú Dynamics 365 Finance, Dynamics 365 Supply Chain a Dynamics 365 Project Operations. Pre každú vytvorenú kategóriu transakcií Project Operations automaticky vytvorí štyri súvisiace zdieľané kategórie: Hodiny, Výdavok, Poplatky a Položka. Zdieľané kategórie môžete skontrolovať a upraviť v časti **Riadenie projektu a účtovníctvo** \> **Nastaviť** \> **Kategórie** \> **Zdieľané kategórie**.

## <a name="project-categories"></a>Kategórie projektov

Kategórie projektu predstavujú najpodrobnejšiu úroveň konfigurácie kategórií a musia byť nakonfigurované osobitne a pre každú spoločnosť účtovníkom projektu.

1. Prejdite do **Riadenie projektu a účtovníctvo** \> **Nastaviť** \> **Kategórie** \> **Kategórie projektov**.
2. Vyberte **Nové**.
3. Vyberte možnosť **ID kategórie** zdieľanej kategórie, ktorú ste vytvorili v predchádzajúcej časti. Project Operations umožňuje používať iba tie zdieľané kategórie, ktoré sú spojené s kategóriami transakcií.
4. Vyberte skupinu kategórií.

## <a name="category-groups"></a>Skupiny kategórií

Skupiny kategórií sa používajú na zdieľanie vlastností, predovšetkým odosielanie profilov medzi súvisiacimi kategóriami projektu. Pre každý typ transakcie musí existovať najmenej jedna skupina kategórií a každej kategórii projektu je priradená skupina.

Špecifikácie účtovania v Project Operations sú definované pravidlami profilu nákladov a výnosov projektu, kategóriami projektov a skupinami kategórií. Skupiny kategórií môžete nastaviť tak, že prejdete na **Riadenie projektu a účtovníctvo** \> **Nastaviť** \> **Kategórie** \> **Skupiny kategórií**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]