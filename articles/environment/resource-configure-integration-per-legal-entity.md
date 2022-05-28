---
title: Konfigurácia integrácie Project Operations pre každú právnickú osobu
description: Táto téma poskytuje informácie o nastavení a integrácie podľa právnickej osoby v Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64606a20a49fd8e9602b6ac3c1ab1880796eb128
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585857"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurácia integrácie Project Operations pre každú právnickú osobu 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma vás prevedie krokmi potrebnými na konfiguráciu aplikácie Dynamics 365 Project Operations pre právnickú osobu.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Povoľte funkčné kľúče v Dynamics 365 Finance

Vykonaním nasledujúcich krokov povolíte požadované funkcie.

1. V Dynamics 365 Finance prejdite na **Správa funkcií** pracovnom priestore.
2. V časti **Zoznam funkcií**, vyhľadajte a povoľte nasledujúce funkcie:
  
    - **Povoliť pre projekt viac riadkov zmluvy**
    - **Povoliť operácie projektu na Dynamics 365 Customer Engagement**

> [!NOTE]
> Ak nevidíte uvedené **Funkčné klávesy**, overte, či vaša verzia Finance spĺňa požiadavku na minimálnu verziu (verzia aplikácie 10.0.13 s použitými všetkými aktualizáciami kvality alebo vyššími verziami). Stlačte možnosť **Skontrolovať aktualizácie** na obnovenie zoznamu funkcií.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definujte scenár nasadenia Project Operations pre právnickú osobu

Operáciu projektu môžete povoliť na Dynamics 365 Customer Engagement na úrovni právnickej osoby. Môžete mať jednu právnickú osobu, ktorá používa projektové operácie na Dynamics 365 Customer Engagement pre scenáre založené na zdrojoch/nezásobách. V rovnakom prostredí môžete mať inú právnickú osobu, ktorá používa Project Operations pre scenáre skladovaných/výrobných zákaziek.

1. V Dynamics 365 Finance prejdite na **Projektový manažment a účtovníctvo** > **Nastaviť** > **Globálny projektový manažment a účtovné parametre**.
2. V zozname dostupných právnických osôb vyberte subjekty, pre ktoré budú povolené viaceré zmluvné línie a projektové operácie na Dynamics 365 Customer Engagement. Právnické osoby, ktoré budú používať operácie projektu pre scenáre skladovania/výrobnej objednávky, nechajte nevybrané.

> [!NOTE]
> Právnickú osobu je možné vybrať, iba ak nemá žiadne existujúce projekty.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurácia parametrov riadenia projektu a účtovníctva

Každá právnická osoba, ktorá používa Project Operations na Dynamics 365 Customer Engagement, potrebuje sadu predvolených parametrov. Tieto parametre sú konfigurované na karte **Project Operations** na stránke **Parametre projektového riadenia a účtovníctva**. Uvedené parametre sú:

  - **Predvolené typy fakturácie**: Project Operations používa pevnú množinu predvolených typov fakturácie, ktorú je potrebné namapovať na vlastnosti riadkov Finance. Vytvorte záznam pre každý typ fakturácie: **Nešpecifikované**, **Spoplatnené**, **Nedá sa spoplatniť**, **Bezplatné** a **Nie je k dispozícií**.
  - **Predvolené hodnoty kategórie projektu**: Vyberte predvolené kategórie projektu, ktoré sa majú použiť pre každý typ transakcie. Tieto predvolené hodnoty sa použijú v **Denníku integrácie Project Operations** a v odhadoch, kde nie je špecifikovaná žiadna kategória transakcií pre skutočný projekt.
  - **Prognózy**: Vyberte predpovedný model, ktorý sa použije pre odhady času a výdavkov.


[!INCLUDE[footer-include](../includes/footer-banner.md)]