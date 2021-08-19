---
title: Konfigurácia integrácie Project Operations pre každú právnickú osobu
description: Táto téma poskytuje informácie o nastavení a integrácie podľa právnickej osoby v Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fc3f5be1318d482ece9a6e9e4fadc3cf628ff79577776e679f32cef7c0b2fc8f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999425"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurácia integrácie Project Operations pre každú právnickú osobu 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma vás prevedie krokmi potrebnými na konfiguráciu aplikácie Dynamics 365 Project Operations pre právnickú osobu.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Aktivácia funkčných klávesov v Dynamics 365 Finance

Vykonaním nasledujúcich krokov povolíte požadované funkcie.

1. V Dynamics 365 Finance prejdite na pracovný priestor **Správa funkcií**.
2. V časti **Zoznam funkcií**, vyhľadajte a povoľte nasledujúce funkcie:
  
    - **Povoliť pre projekt viac riadkov zmluvy**
    - **Aktivácia Project Operations v Dynamics 365 Customer Engagement**

> [!NOTE]
> Ak nevidíte uvedené **Funkčné klávesy**, overte, či vaša verzia Finance spĺňa požiadavku na minimálnu verziu (verzia aplikácie 10.0.13 s použitými všetkými aktualizáciami kvality alebo vyššími verziami). Stlačte možnosť **Skontrolovať aktualizácie** na obnovenie zoznamu funkcií.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definujte scenár nasadenia Project Operations pre právnickú osobu

Môžete povoliť Project Operations v Dynamics 365 Customer Engagement na úrovni právnickej osoby. Môžete mať jeden právny subjekt, ktorý používa Project Operations v Dynamics 365 Customer Engagement pre scenáre založené na zdrojoch/neinventárne scenáre. V rovnakom prostredí môžete mať inú právnickú osobu, ktorá používa Project Operations pre scenáre skladovaných/výrobných zákaziek.

1. V Dynamics 365 Finance prejdite na **Projektové riadenie a účtovníctvo** > **Nastaviť** > **Globálne parametre projektového riadenia a účtovníctva**.
2. V zozname dostupných právnych osôb vyberte subjekty, na ktorých je zapnutých viac riadkov zmlúv a dôjde k aktivácii funkcií Project Operations v Dynamics 365 Customer Engagement. Právnické osoby, ktoré budú používať operácie projektu pre scenáre skladovania/výrobnej objednávky, nechajte nevybrané.

> [!NOTE]
> Právnickú osobu je možné vybrať, iba ak nemá žiadne existujúce projekty.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurácia parametrov riadenia projektu a účtovníctva

Každá právnická osoba využívajúca Project Operations v Dynamics 365 Customer Engagement potrebuje množinu predvolených parametrov. Tieto parametre sú konfigurované na karte **Project Operations** na stránke **Parametre projektového riadenia a účtovníctva**. Uvedené parametre sú:

  - **Predvolené typy fakturácie**: Project Operations používa pevnú množinu predvolených typov fakturácie, ktorú je potrebné namapovať na vlastnosti riadkov Finance. Vytvorte záznam pre každý typ fakturácie: **Nešpecifikované**, **Spoplatnené**, **Nedá sa spoplatniť**, **Bezplatné** a **Nie je k dispozícií**.
  - **Predvolené hodnoty kategórie projektu**: Vyberte predvolené kategórie projektu, ktoré sa majú použiť pre každý typ transakcie. Tieto predvolené hodnoty sa použijú v **Denníku integrácie Project Operations** a v odhadoch, kde nie je špecifikovaná žiadna kategória transakcií pre skutočný projekt.
  - **Prognózy**: Vyberte predpovedný model, ktorý sa použije pre odhady času a výdavkov.


[!INCLUDE[footer-include](../includes/footer-banner.md)]