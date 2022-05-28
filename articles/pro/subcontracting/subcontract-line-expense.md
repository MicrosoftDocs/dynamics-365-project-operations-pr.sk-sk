---
title: Riadky subdodávateľskej zmluvy pre kategórie výdavkov
description: Táto téma vysvetľuje, ako zaznamenávať riadky subdodávateľskej zmluvy pre výdavky a používať polia na nákup času od dodávateľov.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9eba8b70aeb98389515ee679e4bfb1426736ee2c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591699"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Riadky subdodávateľskej zmluvy pre kategórie výdavkov

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Subdodávateľská zmluva v Dynamics 365 Project Operations môže mať riadok pre kategórie výdavkov. Riadky subdodávateľských zmlúv pre kategórie výdavkov umožňujú projektovému manažérovi nakupovať kategórie služieb alebo produktov od dodávateľov, ktoré môžu účtovať projektu.

Ak chcete vytvoriť riadok subdodávateľskej zmluvy pre kategórie výdavkov v Project Operations, postupujte podľa nasledujúcich pokynov.

1. Na navigačnej table vyberte položku **Subdodávateľské zmluvy** a otvorte subdodávateľskú zmluvu, s ktorou chcete pracovať.
2. Na karte **Riadky subdodávateľskej zmluvy** vyberte **Nový** a vytvorte nový riadok.
3. Na stránke **Rýchle vytvorenie** v poli **Trieda transakcie** vyberte **Výdavok** a zadajte alebo vyberte akékoľvek iné požadované informácie o poli.

Nasledujúca tabuľka poskytuje informácie o poliach na stránke s podrobnosťami **Riadok subdodávateľskej zmluvy** a stránke **Rýchle vytvorenie**.

| **Pole** | **Opis** | **Funkčný vplyv** |
| --- | --- | --- |
| Meno | Názov riadka subdodávateľskej zmluvy, ktorý má pomôcť s identifikáciou. | Toto sa zobrazí ako prvý stĺpec vo všetkých vyhľadávaniach na základe riadkov subdodávateľských zmlúv. |
| Popis | Stručný popis kategórií nákladov, ktoré sa nakupujú na riadku subdodávateľských zmlúv. | Nie je |
|Typ riadka | Toto pole má predvolenú hodnotu **Založené na množstve**. |Nie je |
| Spôsob fakturácie | Toto je množina možností, ktorý predstavuje dva hlavné zmluvné modely podporované zo strany Project Operations: **Pevná cena** a **Čas a materiál**. | Na základe zvoleného spôsobu fakturácie je pre riadky subdodávateľov s metódou fakturácie s pevnou cenou k dispozícii míľnik založený na faktúre. |
| Trieda transakcie | Toto pole má predvolenú hodnotu **Čas**. Ak chcete vytvoriť riadky subdodávateľských zmlúv na nákup produktov, nastavte pole **Trieda transakcie** na **Výdavok**.  | To naznačuje, že riadok zmluvy subdodávateľa sa používa na zaznamenávanie nákupu kategórie nákladov, ktoré sa majú použiť na projektoch. |
| Kategória transakcie | Zobrazuje zoznam aktívnych kategórií transakcií v systéme. |Nie je |
| Požadovaný štart | Zadajte dátum, kedy musia byť kategórie nákupu k dispozícii u predajcu. | Požadovaný začiatok sa používa na výber cenníka projektu z cenníkov projektu pripojených k subdodávke. Náklady na kategóriu na riadku subdodávateľskej zmluvy pochádzajú z tohto cenníka. |
| Požadovaný koniec | Zadajte dátum, kedy už kategórie nákupu nebudú potrebné. | Toto sa použije na zobrazenie upozornení, keď projektový manažér priraďuje tento riadok subdodávateľskej zmluvy k odhadom konkrétnych nákladov na projekt, ktoré sú požadované po tomto dátume. |
| Objednané množstvo | Množstvo kategórie, ktoré sa nakupuje u dodávateľa. | Toto sa použije na zobrazenie upozornení, keď projektový manažér prečerpá z tohto množstva.|
| Skupina jednotiek | Predvolená hodnota je založená na predvolenej skupine jednotiek, ktorá je nastavená pre vybratú kategóriu. |Nie je |
| Jednotka | Predvolená hodnota je nastavená pre vybratú kategóriu.  | Kombinácia **Kategória** a **Jednotka** budú použité ako predvolené alebo vypočítané pre jednotkovú cenu pre riadok subdodávateľskej zmluvy.  |
| Jednotková cena | Predvolená hodnota používa kombináciu **Kategória** a **Jednotka** z kategórie cien súvisiacej s cenníkom projektu, ktorý sa vzťahuje na požadovaný začiatok riadka subdodávateľskej zmluvy. |Nie je |
| Medzisúčet | Toto je pole iba na čítanie, ktoré sa počíta ako množstvo X jednotková cena, ak sú zadané hodnoty množstva aj jednotkovej ceny. Ak sú jedno alebo obe polia prázdne, môžete do tohto poľa zadať hodnotu. |Nie je |
| Daň z predaja | Zadajte sumu dane z predaja. |Nie je |
| Celková čiastka | Celková suma riadka subdodávateľskej zmluvy vrátane daní. Toto pole sa počíta ako medzisúčet + daň z predaja. |Nie je |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
