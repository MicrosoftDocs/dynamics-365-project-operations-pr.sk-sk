---
title: Mobilná aplikácia Project Timesheet
description: Tento článok poskytuje informácie o mobilnej aplikácii Microsoft Dynamics 365 Project Timesheet. Mobilná aplikácia Project Timesheet umožňuje používateľom zadávať a schvaľovať časové rozvrhy projektov na svojom mobilnom zariadení.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110994"
---
# <a name="project-timesheet-mobile-application"></a>Mobilná aplikácia Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Prehľad

Mobilná aplikácia Microsoft Dynamics 365 Project Timesheet umožní používateľom zadávať a schvaľovať časové rozvrhy projektov na svojom mobilnom zariadení (iPhone alebo Android). Táto mobilná aplikácia zobrazuje funkcie časového rozvrhu, ktoré sa nachádzajú v oblasti Projektové riadenie a účtovníctvo v Dynamics 365 Finance. Pomáha zvyšovať produktivitu a efektivitu používateľov a tiež umožňuje včasne zadávať a schvaľovať časové rozvrhy projektu.

## <a name="download-and-install-the-mobile-app"></a>Stiahnite a nainštalujte mobilnú aplikáciu

Stiahnite a nainštalujte si mobilnú aplikáciu Microsoft Dynamics 365 Project Timesheet pre Android alebo iPhone z mobilného obchodu pre vaše zariadenie.

## <a name="enable-the-app"></a>Povolenie aplikácie 

V službe Finance musí byť povolená mobilná aplikácia Project Timesheet. Ak chcete povoliť túto funkciu, prejdite do **Parametre riadenia projektu a účtovníctva \> Časový rozvrh** a vyberte parameter **Povoliť Microsoft Dynamics 365 Project Timesheet**.

### <a name="resolve-sign-in-issues"></a>Riešenie problémov s prihlásením

**Problém:** Počas prihlasovania do aplikácie Project Timesheet Mobile sa používateľom zobrazí chybové hlásenie, že „nemajú prístup k aplikácii 2bc50526-cdc3-4e36-a970-c284c34cbd6e v tom nájomníkovi.“

**Problém:** Počas prihlasovania do mobilnej aplikácie Project Timesheet sa používateľom zobrazí chyba, ktorá sa podobá jednému z nasledujúcich príkladov:

- „AADSTS50020: Používateľský účet ‚[meno používateľa]‘ od poskytovateľa identity ‚https://sts.windows.net/[app id]‘ neexistuje v nájomníkovi ‚[tenant id]‘ a nemá prístup k aplikácii ‚[app id]‘ v tomto nájomníkovi.“
- „Vybraté konto používateľa v nájomníkovi ‚[tenant id]‘ neexistuje a nemôže získať prístup k aplikácii ‚[app id]‘ v danom nájomníkovi.“

**Vysvetlenie:** Tieto problémy sú spôsobené zmenou, ktorá bola vykonaná v Azure Active Directory (Azure AD) z máji 2022 a týka sa to externých používateľov. Keďže táto zmena nebola vykonaná pre aplikácie na riadenie financií a prevádzok, môže ovplyvniť zákazníkov na akejkoľvek verzii platformy alebo aplikácie.

**Oprava:** Všetci externí používatelia musia byť pozvaní do nájomníka cez Azure AD. Ďalšie informácie nájdete v časti [Pozvite používateľov pomocou B2B spolupráce Azure Active Directory](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Prihlásenie sa do aplikácie

1.  Spustite aplikáciu na mobilnom zariadení.

2.  Zadajte adresu URL služby Finance.

3.  Pri prvom prihlásení sa zobrazí výzva na zadanie používateľského mena a hesla. Zadajte svoje prihlasovacie údaje.

4. Prihlásite sa do svojej predvolenej spoločnosti.

## <a name="submit-a-project-timesheet"></a>Odoslanie časového rozvrhu projektu

V aplikácii môžete vytvoriť a odoslať časový rozvrh projektu. Nový časový rozvrh môžete založiť na informáciách z predchádzajúceho časového rozvrhu, uložených riadkoch alebo priradeniach projektu. Ak máte úlohu delegáta, môžete tiež zadať časový rozvrh iného pracovníka. Ak chcete vytvoriť časový rozvrh ako delegát, vyberte tlačidlo **Ponuka** a potom vyberte názov zdroja.

Stránka časového rozvrhu vytvorí nový časový rozvrh pre časové obdobie na základe aktuálneho dátumu. Zobrazí sa pracovný týždeň. Ak časový rozvrh pokrýva viac týždňov, môžete si na kartách pracovného týždňa zvoliť iný pracovný týždeň.
Ak existuje časový rozvrh pre aktuálny dátum, zobrazí sa. Ak potrebujete vytvoriť nový časový rozvrh v inom časovom období, vyberte tlačidlo **Ponuka** a potom vyberte **Nový časový rozvrh**.

Informácie o projekte môžete zadať kliknutím na akciu **Pridať čas** alebo na akciu **Kopírovať čas z**. Akcia **Kopírovať čas z** skopíruje informácie o riadku projektu, ale nie hodiny. Ponuka **Kopírovať čas z** obsahuje nasledujúce možnosti:

- **Kopírovať z existujúceho časového rozvrhu** – Skopírovanie riadkov časového rozvrhu z existujúceho časového rozvrhu.

- **Kopírovať z obľúbených** – Vytvorenie nových riadkov časového rozvrhu pomocou nastavení časového rozvrhu, ktoré ste vybrali ako obľúbené.

- **Kopírovať z priradenia** – Vytvorenie nových riadkov časového rozvrhu z priradených projektov.

Zobrazené informácie o projekte závisia od mobilných parametrov, ktoré ste definovali na stránke **Parametre riadenia projektu a účtovníctva**.

V poli **Právnická osoba** vyberte právnickú osobu, pre ktorú ste vykonali projektovú prácu. Pole **Právnická osoba** je k dispozícii, iba ak je pre vašu právnickú osobu povolená podpora medzipodnikového časového rozvrhu.

Vyberte zákazníka, ktorý je spojený s projektom pre časový rozvrh. Pre prvé vydanie v systéme Android nie je zadanie zákazníkom podporované, pretože najskôr musíte zvoliť projekt. Ak ste najprv vybrali projekt, pole **Zákazník** sa vyplní automaticky.

V poli **Projekt** vyberte projekt, pre ktorý zadávate čas. Pole **Zákazník** sa vyplní automaticky.

Vyhľadanie zákazníka a projektu umožňuje vyhľadávanie medzi zákazníkmi aj projektmi.

Podľa potreby vyberte informácie v poliach **Kategória**, **Aktivita**, **Vlastnosť riadku**, **Skupina dane z obratu** a **Skupina dane z obratu tovaru**. Tieto polia je možné prepísať.

Pole **Vlastnosť riadku** sa nastaví na predvolenú hodnotu na základe parametrov riadenia projektu a účtovníctva. Keď sú povolené parametre projekt/kategória a kategória/zdroj, hodnota **Vlastnosť riadku** bude nastavená na predvolenú hodnotu, ktorú ste definovali pre toto overenie. Ak parametre projekt/kategória a kategória/zdroj nie sú povolené, hodnota **Vlastnosť riadku** bude predvolená podľa poľa **Povoliť vlastnosť predvoleného riadku** na stránke **Parametre riadenia projektu a účtovníctva**. Hodnota **Vlastnosť riadku** môže byť prepísaná.

Ak chcete pridať čas, vyberte deň. Zadajte počet hodín, ktoré ste každý deň odpracovali.

Ak chcete pridať komentár k zadaným hodinám, kliknite na **Pridať komentáre** a potom zadajte komentáre pre interné publikum, publikum zákazníkov alebo pre obidve.
Interné komentáre si môžu prezerať manažéri projektu. Komentáre zákazníkov sú súčasťou faktúr.

Ak chcete riadok uložiť ako obľúbený, začiarknite políčko a potom kliknite na **Uložiť ako obľúbené**.

Finančná dimenzia a podpora príloh nie sú v mobilnej aplikácii poskytované.

Podľa potreby pokračujte v pridávaní riadkov projektu, aby ste vyplnili časový rozvrh.

Kliknutím na **Odoslať** odošlete časový rozvrh do pracovného postupu schválenia.

## <a name="review-timesheets"></a>Kontrola časových rozvrhov

Zoznam časových výkazov, ktoré je potrebné skontrolovať, je k dispozícii v ponuke. Táto možnosť je k dispozícii, iba ak ste boli označený za schvaľovateľa pracovného postupu. Podporované je schválenie hlavičky aj riadku. Schválenie na úrovni riadkov ponúka možnosť označiť jeden alebo viac riadkov na schválenie. Po skontrolovaní informácií časového rozvrhu kliknite na **Schváliť**, **Delegovať** alebo **Vrátiť** a pokračujte v pracovnom postupe.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
