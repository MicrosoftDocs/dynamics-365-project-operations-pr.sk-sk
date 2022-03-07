---
title: Vytvorenie zmlúv založených na zálohách pre fakturácie na základe priebehu
description: Táto téma vysvetľuje, ako vytvoriť projektové zmluvy, aby ste zákazníkom mohli generovať faktúry na základe percenta z dokončenej práce.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289523"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Vytvorenie zmlúv založených na zálohách pre fakturácie na základe priebehu
[!include [banner](../includes/banner.md)]

Táto téma vysvetľuje, ako vytvoriť projektové zmluvy, aby ste zákazníkom mohli generovať faktúry na základe percenta z dokončenej práce. Čiastky faktúry sa automaticky počítajú pre rozpočtové kategórie práce, ktoré ste nastavili pre projekt. Načasovanie faktúry sa nastaví pri rokovaniach so zákazníkom o projektovej zmluve.

Postupy v tejto téme použite na nastavenie zmluvy, súvisiaceho projektu a fakturačných pravidiel, ktoré počítajú sumy faktúr pre rozpočtové kategórie prác, ktoré ste pre projekt nastavili.

Po vytvorení zmluvy a projektu môžete nastaviť podrobnosti projektu. Môžete napríklad definovať činnosti a priradiť pracovníkov k projektu.

## <a name="example"></a>Príklad

Vaša organizácia je firma na vývoj softvéru. Súhlasíte s vytvorením balíka mzdového účtovníctva pre zákazníka za celkový poplatok 20 000 amerických dolárov (USD). Vaša organizácia sa zaväzuje fakturovať zákazníkovi po dokončení konkrétnych percent projektu. Pre prácu ste nastavili nasledujúce kategórie projektu, aby ste ich mohli použiť v procese fakturácie:

- Consulting
- Dizajn
- Inštalácia

Nastavíte pravidlá fakturácie, ktoré automaticky počítajú čiastky faktúry za percento projektovej práce dokončenej pre každú kategóriu.

Rozpočtový manažér vytvorí rozpočet pre kategórie projektu. Množstvo dokončenej práce sa automaticky počíta ako percento skutočnej práce v porovnaní s rozpočtovanými sumami.

## <a name="prerequisites"></a>Predpoklady

Pred vytvorením projektu, ktorý používa fakturačné pravidlá, musíte nastaviť postupnosť čísel pre fakturačné pravidlá a denník poplatkov, ktorý sa používa na účtovanie postupových fakturácií.

1. Prejdite na **Projektové riadenie a účtovníctvo** \> **Nastaviť** \> **Parametre projektového riadenia a účtovníctva**.
2. Na stránke **Parametre projektového riadenia a účtovníctva** na karte **Číselné sekvencie** nastavte číselnú postupnosť, ktorú chcete použiť pri vytváraní fakturačných pravidiel.
3. Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Denníky** \> **Poplatky**.
4. Na stránke **Denník poplatkov** stlačte možnosť **Nový** a zadajte názov denníka.

## <a name="create-a-contract-for-progress-billings"></a>Vytvorte zmluvu o postupných fakturáciách

Týmto postupom sa vytvorí projektová zmluva pre projekt s pevnou cenou. Faktúru za projekt vytvoríte, keď práca dokončená na projekte dosiahne určené percento.

1. Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Projekty** \> **Projektové zmluvy**.
2. Na stránke **Projektové zmluvy** stlačte možnosť **Nová**.
3. V dialógovom okne **Nová projektová zmluva** nastavte nasledujúce polia:

    - **Názov**
    - **Typ financovania**
    - **Zdroj financovania**
    - **Mena predaja** - Štandardne sa táto mena používa pre faktúry zákazníkov, ktoré sú spojené so zmluvou o projekte. Menu predaja však môžete zmeniť na konkrétnej faktúre zákazníka.

4. Vyberte položku **OK**. Informácie sa skopírujú do hlavičky stránky **Projektové zmluvy**.
5. Na stránke **Projektové zmluvy** vyplňte zvyšné požadované informácie o projekte.

## <a name="create-a-project-for-progress-billings"></a>Vytvorte projekt o postupných fakturáciách

Podľa týchto pokynov vytvorte projekt a všetky podprojekty, ktoré sú spojené so zmluvou o projekte.

1. Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Projekty** \> **Všetky projekty**.
2. Na stránke **Všetky projekty** kliknite vyberte **Nový**.
3. V dialógovom okne **Nový projekt** v poli **Typ projektu** stlačte možnosť **Čas a materiál**.
4. Vyberte si projektovú skupinu. Skupina projektov definuje informácie o účtovaní pre projekty, ktoré sú skupine priradené.
5. Vyberte **Vytvoriť projekt**.
6. Po vytvorení projektu nastavte fázu projektu na **Prebieha**.

## <a name="create-a-budget-for-a-project"></a>Vytvorenie rozpočtu pre projekt

Kategórie rozpočtu sa používajú na automatický výpočet čiastky faktúry za percento práce dokončenej pre každú kategóriu. Podľa týchto pokynov vytvoríte rozpočtové kategórie pre odhadované náklady.

1. Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Projekty** \> **Všetky projekty**.
2. Na stránke **Všetky projekty** stlačte a otvorte požadovaný projekt.
3. Na stránke **Projekty**, na paneli akcií, na karte **Plán** v skupine **Rozpočet** stlačte možnosť **Rozpočet projektu**.
4. Na stránke **Rozpočet projektu** zadajte odhadované náklady pre každú kategóriu v projekte.

## <a name="create-billing-rules-for-progress-billings"></a>Vytvorte pravidlá fakturácie pre fakturácie priebehu

1. Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Projekty** \> **Projektové zmluvy**.
2. Na stránke zoznamu **Projektové zmluvy** vyberte a otvorte projektovú zmluvu.
3. Na stránke zmluvy o projekte na karte FastTab **Pravidlá fakturácie** stlačte možnosť **Pridať**.
4. Na stránke **Pravidlo fakturácie** v poli **Typ riadka** stlačte možnosť **Priebeh**.
5. Na karte FastTab **Podrobnosti riadka pravidla fakturácie** v poli **Hodnota zmluvy** do poľa zadajte celkovú hodnotu zmluvy.
6. V poli **Kategória** vyberte kategóriu, do ktorej sa má účtovať poplatková transakcia.
7. V poli **Projekt** vyberte projekt, ktorý používa toto pravidlo fakturácie.
8. Voliteľné: Priraďte pravidlo fakturácie ďalším projektom. Na karte FastTab **Projekt** v časti **Dostupné projekty** vyberte projekt a potom kliknutím na tlačidlo so šípkou doprava pridajte projekt do časti **Vybrané projekty**.
9. Voliteľné: Vypočítajte percentuálnu čiastku, ktorú zákazník zadržuje z platieb na faktúre. Na karte FastTab **Podmienky uchovania platby** vyberte zdroj financovania a potom do poľa **Percento zadržania** zadajte percento zadržania.
10. Opakovaním týchto krokov vytvoríte ďalšie pravidlá fakturácie pre projektovú zmluvu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]