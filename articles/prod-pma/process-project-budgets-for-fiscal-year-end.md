---
title: Prenos rozpočtov projektu na konci fiškálneho roka
description: Tento článok poskytuje informácie o tom, ako previesť zostávajúce sumy rozpočtu do budúcich rokov a ako vytvoriť podrobnosti rozpočtového registra.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
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
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084497"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Prenos rozpočtov projektu na konci fiškálneho roka

[!include [banner](../includes/banner.md)]

Pri práci na viacročnom projekte vám môže zostať zvyšný rozpočet na konci fiškálny rok. Môžete previesť zostávajúce sumy rozpočtu do budúceho roka a vytvoriť podrobnosti registra rozpočtu pre sumy v priradených účtoch hlavnej knihy. Než prenesiete zostávajúce sumy, skontrolujte a analyzujte zostávajúce sumy rozpočtu.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Skontrolujte a analyzujte zostávajúce sumy rozpočtu

Vykonajte nasledujúce kroky, aby ste skontrolovali koncoročné rozpočtové sumy pre projekty, ale sumy nepreniesli ďalej.

1. Prejdite do **Projektové riadenie a účtovníctvo** > **Periodické** > **Rozpočty** > **Prenos rozpočtov**. 
2. Na stránke **Proces prenosu rozpočtu projektu** na karte **Koncoročné možnosti** overte, že možnosť **Preniesť zostávajúce sumy rozpočtu projektu** nie je povolená.
3. Na karte **Parametre** v poli **Rozpočtový rok projektu** vyberte fiškálny rok, pre ktorý chcete zobraziť zostávajúcu sumu rozpočtu. 
4. V poli **Otvárací fiškálny rok** projektu vyberte fiškálny rok, pre ktorý chcete zobraziť zostávajúcu sumu rozpočtu. 
5. V poli **Model z predpovede** stlačte možnosť **Zostávajúci rozpočet**. 
6. Ak chcete zahrnúť projekty, ktoré vyhovujú vybraným kritériám a nemajú zostávajúci rozpočet, vyberte **Zobraziť nulový zostatok**.  
7. Na karte **Vybrať rozpočty**, stlačte možnosť **Načítať všetky rozpočty** na načítanie všetkých rozpočtov, ktoré zodpovedajú vybraným kritériám, a potom vyberte možnosť **Spracovať**. 
8. Ak chcete navrhnúť databázový dotaz, ktorý načíta konkrétnu skupinu rozpočtov do panela, vyberte možnosť **Načítať vybrané rozpočty**.

Ak chcete získať ďalšie informácie o konkrétnom riadku na table, vyberte riadok a potom stlačte **Zobraziť podrobnosti rozpočtu** alebo **Zobraziť účty**.

## <a name="carry-forward-remaining-budget-amounts"></a>Preniesť zostávajúce sumy rozpočtu 

Keď spracujete zostávajúce sumy rozpočtu, môžete v hlavnej knihe vytvoriť transakcie pre sumy, ktoré prenášate ďalej. Ak chcete vytvoriť transakcie hlavnej knihy, vykonajte kroky v časti [Preneste sumy rozpočtu a vytvárajte transakcie hlavnej knihy](#carry-forward). 

> [!NOTE]
> Sumy rozpočtu, ktoré sa prenášajú ďalej, sa prevedú do predpovedného modelu, ktorý je vybratý na stránke **Predpovedné modely** ako model predpovede prenosu.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Preneste sumy rozpočtu a vytvárajte transakcie hlavnej knihy

1.  Prejdite do **Projektové riadenie a účtovníctvo** > **Periodické** > **Rozpočty** > **Prenos rozpočtov**. 
2. Na stránke **Proces prenosu rozpočtu projektu** stlačte možnosť **Koniec roka**, a potom povoľte **Preniesť zostávajúce sumy rozpočtu projektu** a **Vytvorte položky registra rozpočtu v hlavnej knihe**. 
3. Na karte **Parametre** v skupine poľa **Parametre projektu** vyberte nasledovné:

   - **Projektový rozpočtový rok**: Zvoľte začiatok fiškálneho roka, pre ktorý chcete zobraziť zostávajúcu sumu rozpočtu. 
   - **Zisk a strata**: Vytvorte transakcie ziskov a strát v hlavnej knihe. 
   -  **WIP**: Vytvorenie transakcií Work in Progress (WIP) v hlavnej knihe.
   -  **Mzda**: Vytvorte transakcie alokácie miezd v hlavnej knihe. 

5. V skupine poľa **Hlavná účtovná kniha** uveďte nasledujúce informácie: 

   - V poli **Otvárací fiškálny rok** vyberte fiškálny rok, pre ktorý chcete zobraziť prenosnú sumu rozpočtu pre projekty. Predvolená hodnota je jeden rok po hodnote v poli **Rozpočtový rok projektu**.
   -  V poli **Prenosové obdobie**, vyberte obdobie, pre ktoré chcete vytvoriť podrobnosti registra rozpočtu v hlavnej knihe. Toto je zvyčajne prvé obdobie v úvodnom fiškálnom roku.

6. V skupine poľa **Skopírovať od/do** uveďte nasledujúce informácie:

   - V poli **Z predpovedného modelu** vyberte model prognózy rozpočtu projektu spojený so zostávajúcimi čiastkami rozpočtu, ktoré chcete previesť na projekty. 
   - V poli **Z modelu hlavnej účtovnej knihy** vyberte model prognózy rozpočtu hlavnej účtovnej knihy spojený so zostávajúcimi čiastkami rozpočtu, ktoré chcete previesť do hlavnej účtovnej knihy. 
   -  Stlačte možnosť **Mena prevodu predaja** a použite ponuku predaja projektu na transakcie hlavnej knihy, ktoré sa vytvoria pri prenose súm rozpočtu pre projekty. Ak táto možnosť nie je vybratá, transakcie používajú účtovnú menu. 
   -  Stlačte možnosť **Zobraziť nulový zostatok** na zahrnutie projektov, ktoré nemajú zostávajúce sumy rozpočtu, ale spĺňajú ďalšie kritériá, ktoré vyberiete v projektoch zobrazených v dolnom paneli.

7. Na karte **Vybrať rozpočty**, stlačte možnosť **Načítať všetky rozpočty** na načítanie všetkých rozpočtov, ktoré zodpovedajú vybraným kritériám. Ak chcete navrhnúť databázový dotaz, ktorý načíta konkrétnu skupinu projektových rozpočtov do panela, vyberte možnosť **Načítať vybrané rozpočty**.
8. Pre každý projekt, ktorý chcete spracovať, vyberte možnosť na začiatku riadku pre projekt.

    > [!TIP]
    > Ak chcete vybrať všetky alebo väčšinu projektov, začiarknite políčko v ľavom hornom rohu. Ak chcete vylúčiť spracovanie ľubovoľného projektu, zrušte jeho začiarknutie.

9. Ak chcete previesť zostávajúce sumy rozpočtu pre vybrané projekty do vybranej fiškálny rok a vytvoriť podrobnosti registra rozpočtu v hlavnej knihe, vyberte možnosť **Spracovať**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Preneste sumy rozpočtu bez vytvorenia transakcie hlavnej knihy

1. Prejdite do **Projektové riadenie a účtovníctvo** > **Periodické** > **Rozpočty** > **Prenos rozpočtov**.
2. Na stránke **Proces prenosu rozpočtu projektu** v poli **Koncoročné možnosti** overte, že možnosť **Preniesť zostávajúce sumy rozpočtu projektu** nie je povolená.
3. V skupine **Parametre** v poli **Rozpočtový rok projektu** vyberte fiškálny rok, pre ktorý chcete zobraziť zostávajúcu sumu rozpočtu.
4. V skupine poľa **Skopírovať od/do** uveďte nasledujúce informácie:

   - V poli **Z predpovedného modelu** vyberte model prognózy rozpočtu projektu spojený so zostávajúcimi čiastkami rozpočtu, ktoré chcete previesť na projekty. 
   - Ak chcete zahrnúť projekty, ktoré vyhovujú vybraným kritériám a nemajú zostávajúci rozpočet, vyberte **Zobraziť nulový zostatok**.
   - V skupine **Vybrať rozpočty**, stlačte možnosť **Načítať všetky rozpočty** na načítanie všetkých rozpočtov, ktoré zodpovedajú vybraným kritériám. Ak chcete navrhnúť databázový dotaz, ktorý načíta konkrétnu skupinu projektových rozpočtov do panela, vyberte možnosť **Načítať vybrané rozpočty**.

5. Pre každý projekt, ktorý chcete spracovať, vyberte možnosť na začiatku riadku pre projekt. 
6. Vyberte možnosť **Spracovať** a preneste zostávajúce sumy rozpočtu pre vybrané projekty do vybratého fiškálneho roka.

