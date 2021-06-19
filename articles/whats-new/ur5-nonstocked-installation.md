---
title: Aktualizujte Project Operations vo svojom prostredí Finance
description: Táto téma poskytuje informácie o tom, ako aktualizovať Project Operations vo vašom prostredí Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011075"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Aktualizujte Project Operations vo svojom prostredí Finance

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_


Táto téma poskytuje informácie o tom, ako aktualizovať Dynamics 365 Project Operations vo vašom prostredí Dynamics 365 Finance. Existujú tri postupy, ktoré sú potrebné na aktualizáciu Project Operations na verziu 5 (UR5):

- [Importujte balík do vašej ukážky projektu](#import)
- [Použite aktualizáciu](#apply)
- [Aktualizujte svoje prostredie Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importujte balík do vášho projektu LCS

1. Prihláste sa do [Lifecycle Services (LCS)](https://lcs.dynamics.com/) ako vlastník projektu alebo manažér prostredia.
2. Zo zoznamu projektov vyberte svoj projekt LCS.
3. Na stránke **Projekt** v skupine **Prostredia** otvorte prostredie, ktoré chcete aktualizovať.
4. Skontrolujte, či je prostredie spustené. Ak nie je spustené, spustite prostredie.
5. V časti **Nové vydanie** pod **Dostupné aktualizácie** vyberte **Zobraziť aktualizáciu** pre 10.0.15.

![Tlačidlo Zobraziť aktualizácie](media/view-update.png)

6. Na stránke **Binárne aktualizácie** vyberte **Uložiť balík**.
7. Na stránke **Skontrolovať a uložiť aktualizácie** vyberte **Uložiť balík**.
8. Na table **Uložiť balík do knižnice aktív**, ktorá sa otvorí, zadajte názov balíka a potom vyberte **Uložiť balík**.
9. Keď LCS dokončí ukladanie balíka, povolí sa tlačidlo **Hotovo**. Vyberte položku **Hotovo**. LCS overí balík. Overenie môže trvať niekoľko minút alebo až hodinu.


## <a name="apply-the-package-update"></a><a name="apply"></a>Použite aktualizáciu balíka

1. V LCS na stránke **Podrobnosti o prostredí** vyberte **Udržiavať** > **Použiť aktualizácie**.
2. V zozname vyberte balík, ktorý ste uložili skôr, a potom vyberte **Použiť**.
3. Vyberte **Áno** na potvrdenie, že chcete nasadiť balík.

![Potvrďte dialógové okno nasadenia balíka](media/confirm-package-deployment.png)

4. Vyberte **Áno** na potvrdenie, že chcete aktualizovať aplikáciu.

![Potvrďte dialógové okno aktualizácie aplikácie](media/confirm-application-update.png)

Spustí sa nasadenie a aktualizácia aplikácie. 

Na stránke **Podrobnosti o prostredí** v pravom hornom rohu sa aktualizuje stav prostredia na **Poskytuje sa služba**. Aktualizácia bude dokončená približne o dve hodiny. Informácie o vydaní aplikácie sa aktualizujú na **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** a stav prostredia sa aktualizuje na **Nasadené**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Aktualizujte svoje prostredie Dataverse

1. Prihláste sa do [centra spravovania Power Platform](https://admin.powerplatform.com/).
2. V zozname vyhľadajte a otvorte prostredie, ktoré ste použili na inštaláciu Project Operations.
3. Na stránke **Prostredia** vyberte **Zdroj** > **Aplikácie Dynamics 365**.
4. V zozname vyhľadajte **Microsoft Dynamics 365 Project Operations** a v stĺpci **Stav** vyberte **Aktualizácia k dispozícii**.
5. Začiarknite políčko **Súhlasím s podmienkami služby** a potom vyberte **Aktualizovať**. Nainštaluje sa najnovšia verzia riešenia.

Po dokončení inštalácie budete mať nainštalovanú verziu 4.5.0.134.

## <a name="configure-new-features"></a>Konfigurácia nových funkcií

### <a name="enable-dual-write-mapping"></a>Povolenie mapovania s duálnym zápisom

Po dokončení aktualizácie prostredí Finance a Dataverse môžete povoliť požadované mapovania s duálnym zápisom. Dokončením nasledujúcich postupov povolíte mapovania s duálnym zápisom.

- [Aktualizujte nastavenia zabezpečenia v prostredí Customer Engagement](#security)
- [Obnovte údaje o entitách](#refresh)
- [Aktualizujte a spustite mapovania s duálnym zápisom](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Aktualizujte nastavenia zabezpečenia v prostredí Dataverse

Nasledujúce aktualizácie bezpečnostných oprávnení pre entity sú vyžadované ako súčasť aktualizácie UR5.

1. V prostredí Dataverse prejdite na **Nastavenia** a v skupine **Systém** vyberte **Zabezpečenie**.

![Nastavenia prostredia Dataverse](media/Picture21.png)

2. Vyberte **Roly zabezpečenia**.
3. V zozname rolí vyberte **používateľ aplikácie s duálnym zápisom** a vyberte kartu **Vlastné entity**. 
4. Overte, či má rola povolenia **Čítať** a **Pripojiť k** pre:

      - **Typ výmenného kurzu meny**
      - **Účtovná osnova** 
      - **Rozpočtový kalendár** 
      - **Hlavná kniha**

5. Po aktualizácii roly zabezpečenia prejdite na **Nastavenia** > **Zabezpečenie** > **Tímy**. Overte, či bola tímu pridelená rola **používateľ aplikácie s duálnym zápisom**. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Obnovte dátové entity z aktualizácie

1. Vo svojom prostredí Finance otvorte pracovný priestor **Správa údajov** a potom otvorte stránku **Parametre rámca**.
2. Na karte **Nastavenia entity** vyberte **Obnoviť zoznam entít**.
3. Vyberte **Zavrieť** na potvrdenie obnovenia entity.

 > [!NOTE]
 > Dokončenie tohto procesu bude trvať približne 20 minút. Po dokončení obnovenia budete informovaní.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Aktualizujte mapovania s duálnym zápisom

1. V pracovnom priestore **Správa údajov** vyberte **Duálny zápis**.
2. Vyberte **Použiť riešenia**, vyberte obe riešenia v zozname a potom vyberte **Použiť**.
3. Na stránke **Duálny zápis** vyberte nasledujúce mapy tabuliek a potom vyberte **Zastaviť**.

    - **Skutočné hodnoty integrácie Project Operations (msdyn_actuals)**
    - **Kategórie výdavkov projektu na integráciu Project Operations (msdyn_expensecategories)**
    - **Integrácia Project Operations predstavuje skutočnú entitu exportu výdavkov projektu (msdyn_expenses)**

4. Na stránke **Verzia mapy tabuľky** použite novú verziu mapy na každú z troch entít.
5. Na stránke **Duálny zápis** výberom spustenia reštartujte mapy.
6. V zozname máp vyberte mapu **Ledger (msdyn_ledgers)** so všetkými predpokladmi a začiarknite políčko **Počiatočná synchronizácia**. 
7. V poli **Predloha pre počiatočnú synchronizáciu** vyberte **aplikácie Finance and Operations** a potom vyberte **Spustiť**.
 
 ![Synchronizácia máp účtovnej knihy](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]