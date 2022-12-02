---
title: Konfigurácia integrácie Project Operations pre každú právnickú osobu
description: Tento článok poskytuje informácie o nastavení a integrácie podľa právnickej osoby v Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914697"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurácia integrácie Project Operations pre každú právnickú osobu 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok vás prevedie krokmi potrebnými na konfiguráciu aplikácie Dynamics 365 Project Operations pre právnickú osobu.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Povoľte funkčné klávesy v Dynamics 365 Finance

Vykonaním nasledujúcich krokov povolíte požadované funkcie.

1. V nástroji Dynamics 365 Finance prejdite na pracovný priestor **Správa funkcie**.
2. V časti **Zoznam funkcií**, vyhľadajte a povoľte nasledujúce funkcie:
  
    - **Povoliť pre projekt viac riadkov zmluvy**
    - **Povolenie Project Operations v Dynamics 365 Customer Engagement**

> [!NOTE]
> Ak nevidíte uvedené **Funkčné klávesy**, overte, či vaša verzia Finance spĺňa požiadavku na minimálnu verziu (verzia aplikácie 10.0.13 s použitými všetkými aktualizáciami kvality alebo vyššími verziami). Stlačte možnosť **Skontrolovať aktualizácie** na obnovenie zoznamu funkcií.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definujte scenár nasadenia Project Operations pre právnickú osobu

Môžete povoliť Project Operations v Dynamics 365 Customer Engagement na úrovni právnickej osoby. Môžete mať jeden právny subjekt, ktorý používa Project Operations v Dynamics 365 Customer Engagement pre scenáre založené na zdrojoch/neskladovaných položiek. V rovnakom prostredí môžete mať inú právnickú osobu, ktorá používa Project Operations pre scenáre skladovaných/výrobných zákaziek.

1. V Dynamics 365 Finance prejdite na **Projektové riadenie a účtovníctvo** > **Nastaviť** > **Globálne parametre projektového riadenia a účtovníctva**.
2. V zozname dostupných právnických osôb vyberte subjekty, na ktorých je zapnutých viac riadkov zmlúv a dôjde k aktivácii funkcií Project Operations v Dynamics 365 Customer Engagement. Právnické osoby, ktoré budú používať operácie projektu pre scenáre skladovania/výrobnej objednávky, nechajte nevybrané.

> [!NOTE]
> Právnickú osobu je možné vybrať, iba ak nemá žiadne existujúce projekty.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurácia parametrov riadenia projektu a účtovníctva

Každá právnická osoba využívajúca Project Operations v Dynamics 365 Customer Engagement potrebuje množinu predvolených parametrov. Tieto parametre sú konfigurované na karte **Project Operations** na stránke **Parametre projektového riadenia a účtovníctva**. Uvedené parametre sú:

  - **Predvolené typy fakturácie**: Project Operations používa pevnú množinu predvolených typov fakturácie, ktorú je potrebné namapovať na vlastnosti riadkov Finance. Vytvorte záznam pre každý typ fakturácie: **Nešpecifikované**, **Spoplatnené**, **Nedá sa spoplatniť**, **Bezplatné** a **Nie je k dispozícií**.
  - **Predvolené hodnoty kategórie projektu**: Vyberte predvolené kategórie projektu, ktoré sa majú použiť pre každý typ transakcie. Tieto predvolené hodnoty sa použijú v **Denníku integrácie Project Operations** a v odhadoch, kde nie je špecifikovaná žiadna kategória transakcií pre skutočný projekt.
  - **Prognózy**: Vyberte predpovedný model, ktorý sa použije pre odhady času a výdavkov.


[!INCLUDE[footer-include](../includes/footer-banner.md)]