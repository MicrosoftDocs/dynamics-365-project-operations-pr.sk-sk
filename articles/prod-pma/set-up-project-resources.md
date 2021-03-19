---
title: Nastavenie zdrojov pre projekty
description: Táto téma poskytuje informácie o nastavení alebo požadovaní zdrojov projektu.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288758"
---
# <a name="set-up-project-resources"></a>Nastavenie zdrojov pre projekty

[!include [banner](../includes/banner.md)]

Musíte si pripraviť kalendár a priradiť ho k zamestnancovi alebo pracovníkovi. Kalendár sa používa na plánovanie projektu a pracovného času zdrojov, ktoré sú rezervované pre projekt. Počas nastavovania kalendára môžu projektoví manažéri v rámci optimalizácie zdrojov vykonať optimalizáciu zdrojov. Na základe harmonogramu kalendára je možné uvaliť obmedzenia na zdroje. Kalendár si môžete nastaviť na stránke **Kalendáre**.

Keď nastavujete pracovníka ako zdroj projektu, môžete si vybrať z pracovníkov, ktorí pracujú v spoločnosti, pre ktorú nastavujete zdroje. Prípadne si môžete vybrať pracovníkov z iných spoločností vo vašej organizácii. Títo pracovníci sú známi ako medzipodnikové zdroje.

Nasledujúce postupy vysvetľujú, ako nastaviť pracovníka ako zdroj projektu vo vašej spoločnosti a ako nastaviť medzipodnikový zdroj projektu.

## <a name="set-up-a-worker-as-a-project-resource"></a>Nastavenie pracovníka ako zdroja projektu

1. Na stránke **Pracovníci** v zozname **Pracovníci** vyberte pracovníka, ktorého pridávate ako zdroje projektu, a otvorte záznam pracovníka.
2. Na table Akcia vyberte možnosť **Projekt** &gt; **Nastaviť** &gt; **Nastavenie projektu**.
3. Vyberte kalendár a potom stránku zavrite.

Môžete tiež určiť predvolené projekty pre zdroj ako typ predbežného priradenia. Predbežné priradenia je možné použiť, keď manažér zdrojov alebo projektový manažér vopred vedia, na ktorých projektoch bude zdroj pracovať. Predbežné priradenia môžu byť tiež založené na žiadosti sponzora projektu alebo zákazníka. Na predbežné priradenie projektu vyberte na stránke **Priradiť projekty** na karte **Projekty** v zozname **Zostávajúce projekty** príslušný projekt.

## <a name="set-up-an-intercompany-resource"></a>Nastavenie medzipodnikového zdroja

Keď nastavíte pracovníka ako medzipodnikový zdroj, musíte dokončiť nastavenie v spoločnosti, ktorá ho prenajíma, ale aj ktorá si ho prenajíma.

### <a name="in-the-lending-company"></a>V spoločnosti, ktorá prenajíma

1. V službe Financie skontrolujte, či je vybratá spoločnosť, ktorá prenajíma, a potom dokončite postup v predchádzajúcej časti „Nastavenie pracovníka ako zdroja projektu“.
2. Na stránke **Účtovanie medzi spoločnosťami** vyberte možnosť **Nové**.
3. V poli **ID právnickej osoby** vyberte spoločnosť, ktorá prenajíma. Vyplňte príslušné polia zodpovedajúcim spôsobom a potom vyberte položku **Uložiť a Zavrieť**.
4. Na stránke **Cena transferu** vyberte možnosť **Nové**.
5. V poli **Právnická osoba, ktorá si prenajíma** vyberte príslušnú spoločnosť.
6. Ak chcete prenajať spoločnosti, ktorá si prenajíma, iba ten zdroj, ktorý ste vytvorili na začiatku tejto časti v poli **Zdroj**, vyberte názov zdroja, ktorý ste vytvorili. Ak chcete v spoločnosti, ktorá prenajíma, sprístupniť všetky zdroje pre spoločnosť, ktorá si prenajíma, nechajte pole **Zdroje** prázdne.
7. Na stránke **Parametre projektového riadenia a účtovníctva**, na karte **Medzipodnikové**, nastavte možnosť **Povoliť medzipodnikové plánovanie zdrojov a časové rozvrhy** na **Áno**.

### <a name="in-the-borrowing-company"></a>V spoločnosti, ktorá si prenajíma

- Na stránke **Zoznam zdrojov** vo filtri vyhľadávania zadajte názov zdroja, ktorý ste vytvorili pre spoločnosť, ktorá prenajíma, aby ste overili, či je uvedený v zozname zdrojov spoločnosti, ktorá si prenajíma.

## <a name="request-project-resources"></a>Žiadosť o zdroje pre projekty
Funkcie pre plánovanie zdrojov projektu slúži iba na to, aby správcovia zdrojov distribuovali personálne zdroje na zákazky alebo projekty. Ak chcete povoliť túto funkciu, dokončite nasledujúce úlohy alebo skontrolujte, či boli dokončené:

- Nastaviť číselné sekvencie.
- Nastavte pracovné postupy riadenia projektu a účtovníctva.
- Povoliť pracovné postupy týkajúce sa požiadaviek na zdroje.

Po dokončení predchádzajúcich úloh môžete podľa potreby dokončiť nasledujúce úlohy:

- Vytvoriť požiadavku na zdroj z personálne obsadeného zdroja s predbežnou rezerváciou.
- Monitorovať požiadavky na zdroje.
- Splniť požiadavky na zdroje.
- Vyžiadajte si personálny zdroj zo štruktúry WBS.
- Zarezervujte si zdroje pre projekt bez toho, aby ste museli vyžadovať personálny zdroj.


[!INCLUDE[footer-include](../includes/footer-banner.md)]