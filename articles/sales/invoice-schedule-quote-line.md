---
title: Plány faktúr v riadkoch cenovej ponuky založenej na projekte
description: Táto téma poskytuje informácie o vytváraní harmonogramov faktúr a medzníkov pre riadky cenových ponúk.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6b443a353c98fe5c7475d8a95c99abe01cd00987
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601083"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Plány faktúr v riadkoch cenovej ponuky založenej na projekte

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Riadok ponuky založenej na projekte umožňuje vyjadriť plán faktúr. Táto možnosť je voliteľná počas fázy cenovej ponuky, pretože aplikácia nepodporuje fakturáciu projektu, keď je naviazaná na riadok cenovej ponuky. Fakturácia je povolená až po získaní cenovej ponuky. Jediným následným dopadom vytvorenia harmonogramu faktúr počas fázy cenovej ponuky je, že sa tento harmonogram faktúr skopíruje do riadku kontraktu založeného na projekte. Ak počas fázy cenovej ponuky nevytvoríte harmonogram faktúr, budete tak môcť urobiť na riadku zmluvy na základe projektu.

Celkovo je cieľom plánov faktúr umožniť automatické vytváranie konceptov faktúr pre riadok zmluvy na základe projektu. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Vytvorte harmonogram časových a materiálových faktúr pre cenovú ponuku založenú na projekte

Keď je metóda fakturácie pre riadok cenovej ponuky založenej na projekte Čas a materiál, systém vygeneruje časový plán faktúr. Ak chcete automaticky generovať harmonogram faktúr na základe dátumu, postupujte nasledovne.

1. Prejdite do časti **Nastavenia** > **frekvencie faktúr** a nastavte frekvenciu fakturácie.
2. Na stránke **Cenové ponuky** otvorte cenovú ponuku projektu a na karte **Súhrn** nastavte požadovaný dátum dodania.
3. Otvorte riadok cenovej ponuky pre čas a materiál, ktorý potrebujete na vytvorenie harmonogramu faktúr založeného na dátume. 
4. Na karte **Plán faktúr** vyberte hodnoty polí **Začiatok fakturácie** a **Frekvencia faktúr**. 
5. Na vedľajšej mriežke vyberte **Generovať plán faktúr**.
6. Aplikácia vygeneruje plán faktúr s poľami **Dátum spustenia faktúry**, **Dátum uzávierky transakcie** a **Stav spustenia** nastavené nasledujúcim spôsobom:

    - **Dátum spustenia faktúry** je nastavený na dátum, ktorý je určený na základe frekvencie faktúr.
    - **Dátum uzávierky transakcie** je nastavený deň pred **Dátumom spustenia faktúry**.
    - **Stav spustenia** je automaticky nastavený **Nie je spustený**. Keď sa úloha automatického vytvárania faktúr spustí pre určitý dátum spustenia faktúry, aktualizuje sa toto pole buď na **Spustenie bolo úspešné** alebo **Spustenie zlyhalo**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Vytvorenie plánu faktúr s pevnou cenou pre cenovú ponuku založenú na projekte

Keď má riadok cenovej ponuky založenej na projekte spôsob fakturácie **Opravené**, systém vytvorí plán fakturácie na základe medzníka. Vykonajte nasledujúce kroky a automaticky vygenerujte tento plán pre pevne nastavenú skupinu medzníkov, ktoré sú rovnomerne rozložené pre kalendárne obdobie.

1. Prejdite do časti **Nastavenia** > **frekvencie faktúr** a nastavte frekvenciu fakturácie.
2. Na stránke **Cenové ponuky** otvorte cenovú ponuku projektu a na karte **Súhrn** nastavte požadovaný dátum dodania.
3. Otvorte riadok cenovej ponuky s pevnou cenou, pre ktorý potrebujete vytvoriť plán medzníka. 
4. Na karte **Plán faktúr** vyberte hodnoty polí **Začiatok fakturácie** a **Frekvencia faktúr**. 
5. Na vedľajšej mriežke vyberte **Generovať periodické medzníky**.
6. Aplikácia vygeneruje plán faktúr s názvom medzníka, dátumom a sumou.

    - Názov medzníka je nastavený na dátum, ktorý je určený na základe frekvencie faktúr.
    - Dátum medzníka je nastavený na dátum, ktorý je určený na základe frekvencie faktúr.
    - Suma medzníka sa počíta vydelením sumy cenovej ponuky v riadku cenovej ponuky založenej na projekte počtom medzníkov, podľa určenia frekvenciou a začiatkom fakturácie a požadovanými termínmi dodania.
    - Ak má riadok cenovej ponuky aj odhadovanú výšku dane, táto hodnota sa pri generovaní pravidelných medzníkov rozdelí rovnako medzi každý medzník.

### <a name="manually-create-milestones"></a>Manuálne vytváranie medzníkov

Medzníky s pevnou cenou je možné generovať aj manuálne, ak nie sú pravidelne rozdelené. Manuálne vytvorenie medzníka:

Otvorte riadok cenovej ponuky s pevnou cenou, v ktorom chcete vytvoriť medzník. Na karte **Plán faktúr** na vedľajšej mriežke **+ Vytvoriť nový medzník riadku cenovej ponuky** a zadajte požadované informácie na základe nasledujúcej tabuľky.

| **Pole** | **Miesto** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- | --- |
| Názov medzníka | Rýchle vytvorenie | Názov medzníka. | Prenesie sa na medzník riadka zmluvy projektu a na faktúru |
| Projektová úloha | Rýchle vytvorenie | Ak je medzník naviazaný na úlohu projektu, môžete pomocou tohto odkazu pridať vlastnú logickú súpravu stavu medzníka na základe stavu úlohy. | Aplikácia nemá žiadny následný dopad tohto odkazu na úlohu. |
| Dátum medzníka | Rýchle vytvorenie | Nastavte dátum, kedy má proces automatického vytvárania faktúr vyhľadávať stav tohto medzníka, aby sa zohľadnil pri fakturácii. | Prenesie sa na medzník riadka zmluvy projektu a na faktúru. |
| Stav faktúry | Rýchle vytvorenie | Keď sa vytvorí medzník, tento stav sa vždy nastaví na **Nepripravené na fakturáciu**. | Prenesie sa na medzník riadka zmluvy projektu a na faktúru. |
| Suma riadka | Rýchle vytvorenie | Suma alebo hodnota medzníka, ktorá bude fakturovaná zákazníkovi. | Prenesie sa na medzník riadka zmluvy projektu a na faktúru. |
| Daň | Rýchle vytvorenie | Výška dane, ktorá sa použije na dosiahnutie medzníka. | Prenesie sa na medzník riadka zmluvy projektu a na faktúru. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]