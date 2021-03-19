---
title: Správa odhadov výnosov
description: Táto téma poskytuje informácie o tom, ako pracovať s odhadmi výnosov pre projekty.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b63346f56db8b906e5aa45940465bdb18e3df480
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279022"
---
# <a name="manage-revenue-estimates"></a>Správa odhadov výnosov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Môžete vytvárať, počítať, zaúčtovať, vracať späť alebo eliminovať odhady výnosov. Môžete to urobiť ručne alebo periodicky. Táto téma poskytuje informácie o tom, ako pracovať s odhadmi výnosov pre projekty.

### <a name="manage-revenue-estimates-manually"></a>Ručná správa odhadov výnosov

V projekte odhadu výnosov s pevnou cenou alebo na stránke **Odhadnúť dopyt** (**Projektový manažment a účtovníctvo** > **Zostavy a otázky** > **Dopyty odhadov a zostavy**) vyberte **Odhady**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Spravovanie odhadov výnosov pomocou pravidelného procesu

Prejdite na **Projektový manažment a účtovníctvo** > **Pravidelné** > **Odhady** a vyberte zodpovedajúci proces.

## <a name="create-a-revenue-estimate"></a>Vytvorenie odhadu výnosov

Ak chcete vytvoriť odhad výnosov, vykonajte nasledujúce kroky. 

1. Prejdite na **Projektový manažment a účtovníctvo** > **Pravidelné** > **Odhady**.
2. Vyberte **Nové**. Na stránke **Vytvorenie odhadu** vyberte nasledujúce parametre:

   - **Kód obdobia**: Tento kód určuje, ako často sa zaúčtujú odhady.
   - **Dátum odhadu**: Dátum spracovania odhadu.
   - **Kontinuálne**: Začiarknutím tohto políčka vytvoríte odhady iba vtedy, ak boli odhady zaúčtované v predchádzajúcom období, alebo ak je odhad prvým vytvoreným odhadom. Ak túto možnosť nezvolíte, vytvoria sa odhady, aj keď odhady neboli zaúčtované v predchádzajúcom období.
   - **Metóda nákladov na dokončenie**: Definujte, ako odhadnúť zostávajúcu prácu na projekte. Viac informácií nájdete v časti [Metódy nákladov na dokončenie](cost-complete-methods.md).
   - **Metóda dokončenia** : Vyberte metódu dokončenia z nasledujúcich možností:
     - **Automaticky**: Percento dokončenia sa počíta automaticky a na základe nákladových riadkov zahrnutých do výpočtu. Šablóna nákladov definuje nákladové riadky, ktoré sú zahrnuté.
     - **Ručne**: Percento dokončenia sa rovná percentuálnemu podielu dokončenia posledného odhadu. Po vytvorení odhadu môžete zmeniť **Ručný výpočet** na stránke **Odhady**.
     - **Zo šablóny nákladov**: Kombinácia automatickej a ručnej metódy. Táto možnosť je nastavená automaticky alebo ručne v závislosti od predvolenej hodnoty v šablóne nákladov.
   - **Model prognózy**: Vyberte prognózy model pre odhad.
   - **Vytlačiť zoznam odhadov**: Vytvorenie a zobrazenie zoznamu odhadov. Zoznam obsahuje stav aktuálnej funkcie. Akékoľvek varovania týkajúce sa odhadu si môžete vytlačiť do zostavy. Nasledujúce podmienky spôsobujú, že v zozname odhadov sa zobrazia varovania:
     - Percento dokončenia viac ako 100 percent.
     - Percento dokončenia menej ako 0 percent.
     - Záporná suma v stĺpci **Na dokončenie**.
     - Odhad bez zodpovedajúcej výšky zmluvy.
     - Odhad bez pripojeného odhadu nákladov.
   - **Zobraziť Infolog**: Vyberte túto možnosť, aby ste dostali správu, ktorá obsahuje informácie o odhadovaných projektoch, ktoré boli spracované pri spustení úlohy.


## <a name="post-wip-or-accruals"></a>Zaúčtovať WIP alebo prírastky

Po vyhodnotení odhadov sa tieto odhady vyhodnotia, znížia alebo zvýšia. Potom môžete zaúčtovať WIP, keď pracujete s princípom posudzovania **Dokončená zmluva** alebo vystaviť prírastky, keď pracujete s princípom posudzovania **Dokončené percento**.
  
Stav odhadovaného obdobia sa zmení z **Vytvorené** na **Zaúčtované**.

## <a name="reverse-wip-or-accruals"></a>Obrátiť WIP alebo prírastky

Využite možnosť obrátenia na pripísanie už zaúčtovaných WIP alebo prírastkov a potom vytvorte odhady pre dané obdobie.

> [!NOTE]
> Ak chcete obrátiť obdobie, ktoré sa nachádza medzi ostatnými obdobiami, obráťte potrebné odhadované obdobia a potom ich znova zaúčtujte. Pretože všetky nasledujúce obdobia závisia od odhadov z predchádzajúceho obdobia, nevynechávajte žiadne obdobia.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Odstránenie odhadovaného projektu a dokončenie projektu

Posledným krokom v procese odhadu je odstránenie odhadovaného projektu a ukončenie projektu s pevnou cenou, keď percento dokončenia dosiahne 100 percent.

Pri spustení odstránenia nastane nasledovné:

- Pre projekt s pevnou cenou s dokončenou zmluvou sa hodnoty WIP vymažú zo súvahových účtov a zaúčtujú sa na účty ziskov a strát.
- Pre projekt s pevnou cenou s dokončeným percentom sa prírastky odstránia z účtov ziskov a strát.

Odhad zmení stav na **Odstránené**.

> [!NOTE]
> V špeciálnych prípadoch môže percento presiahnuť 100 percent. Ak sa to stane, znížte percento dokončenia pomocou položky **Nastaviť metódu nákladov na dokončenie na nulu**, aby ste dosiahli 100 percent.

## <a name="reverse-elimination"></a>Opačné odstránenie

1. Prejdite do **Projektové riadenie a účtovníctvo** > **Pravidelné** > **Odhady** > **Opačné odstránenie**. 
2. Na table akcií, na karte **Proces** v skupine **Údržba** vyberte **Odhad**. 
3. Vyberte **Opačné odstránenie**.

Táto stránka sa používa na otočenie všetkých odstránení so stanoveným dátumom odhadu a so stavom odhadu **Odstránené**. Stav transakcie sa zmení po výbere príslušných polí.

Týmto sa tiež automaticky zmení stav projektu na **Prebiehajúce**, ak je fáza projektu nastavená na dokončenú. Stav odhadu obdobia projektu sa mení späť na **Zaúčtované**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]