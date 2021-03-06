---
title: Vytvorenie projektových cenových ponúk z príležitostí
description: Táto téma poskytuje informácie o vytváraní cenových ponúk projektu z príležitostí.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898551"
---
# <a name="create-project-quotes-from-opportunities"></a>Vytvorenie projektových cenových ponúk z príležitostí

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Cenové ponuky je možné vytvárať z projektových príležitostí nasledujúcimi spôsobmi:

- Na karte **Cenové ponuky**, na stránke **Príležitosť projektu**
- V toku procesu predaja príležitosti
- Aktualizáciou odkazu príležitosti v existujúcej cenovej ponuke

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>Na karte Cenové ponuky, na stránke Projektová príležitosť

Ak chcete vytvoriť projektovú cenovú ponuku z príležitosti, vykonajte nasledujúce kroky.

1. Otvorte stránku **Projektová príležitosť** a vyberte kartu **Cenové ponuky**. 
2. Na vedľajšej mriežke **Cenové ponuky** vyberte **+** na vytvorenie novej projektovej cenovej ponuky založenej na príležitosti. Všetky riadky príležitostí a súvisiace cenníky projektu sa skopírujú do novej cenovej ponuky príležitosti.

## <a name="from-the-opportunity-sales-process-flow"></a>V toku procesu predaja príležitosti

Ak chcete vytvoriť cenovú ponuku z toku predajného procesu príležitosti, vykonajte nasledujúce kroky.

1. V toku procesu predaja príležitosti otvorte príležitosť.
2. Vyberte etapu **Schváliť**. 
3. Vyberte **Ďalej** a potom vyberte **+ Vytvoriť** na vytvorenie novej cenovej ponuky. Väčšina informácií na karte **Súhrn** pre túto novú cenovú ponuku bude mať predvolenú hodnotu z príležitosti. 
4. Zadajte požadované informácie, ktoré chýbajú, alebo podľa potreby aktualizujte predvolené hodnoty na karte **Súhrn**,
5. Vyberte položku **Uložiť**. Vytvorí sa nová cenová ponuka a spojí sa s príležitosťou. Teraz si môžete pozrieť informácie o cenovej ponuke na karte **Cenové ponuky** na stránke **Príležitosť**. 

   Proces predaja príležitosti sa posúva do ďalšej fázy, **Navrhnúť**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Aktualizáciou odkazu príležitosti v existujúcej cenovej ponuke

Existujúca cenová ponuka môže byť prepojená s príležitosťou. Ak chcete aktualizovať informácie o príležitosti pre existujúcu cenovú ponuku, vykonajte nasledujúce kroky.

1. Otvorte stránku **Cenová ponuka** a vyberte kartu **Súhrn**.
2. V poli **Príležitosť** vyberte príležitosť, ktorú chcete prepojiť s cenovou ponukou. Cenovú ponuku si môžete pozrieť v mriežke **Cenové ponuky** v časti Príležitosť. 
3. Pomocou procesu predaja príležitosti sa príležitosť môže presunúť do ďalšej fázy, **Navrhnúť**. 

   Keď presuniete príležitosť do tejto fázy, môžete si vybrať túto cenovú ponuku zo zoznamu cenových ponúk spojených s touto príležitosťou. Výber tejto cenovej ponuky znamená, že sa s ňou posúvate vpred.

   Všetky ostatné cenové ponuky spojené s príležitosťou budú stále k dispozícii a aktívne, kým sa jedna z nich nevyužije. Proces predaja môžete presunúť späť do predchádzajúcej fázy **Kvalifikovať**, a vybrať ďalšiu ponuku, s ktorou budete pokračovať ďalej.
