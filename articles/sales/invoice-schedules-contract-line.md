---
title: Vytvorenie plánu faktúr v riadku zmluvy na základe projektu
description: Táto téma poskytuje informácie o vytváraní harmonogramov faktúr a medzníkov pre riadky zmluvy.
author: rumant
ms.date: 10/17/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f84d9935eec13666e3eaaa675908e9bc3d2097c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010130"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Vytvorenie plánu faktúr v riadku zmluvy na základe projektu 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Môžete vytvoriť plán faktúry v riadku zmluvy založenej na projekte. Fakturácia je povolená až po využití zmluvy a vytvorení projektovej zmluvy. Plán faktúr umožňuje automatické vytváranie konceptov faktúr pre riadok zmluvy na základe projektu. Ak však faktúry vytvárate iba ručne, môžete preskočiť vytváranie plánov faktúr pre riadky zmlúv.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Vytvorte harmonogram časových a materiálových faktúr pre riadok zmluvy

Keď riadok zmluvy založený na projekte obsahuje metódu fakturácie času a materiálu, môžete vytvoriť plán faktúr na základe dátumu. Ak chcete automaticky generovať harmonogram faktúr na základe dátumu, postupujte nasledovne.

1. Prejdite do časti **Nastavenia** > **Frekvencie faktúr** a nastavte frekvenciu fakturácie.
2. Prejdite na záznam projektovej zmluvy a na karte **Súhrn** v poli **Požadovaný dátum dodania** vyberte dátum.
3. Otvorte riadok zmluvy **Čas a materiál**, pre ktorý zostavujete plán faktúr na základe dátumu. 
4. Na karte **Plán faktúr** vyberte dátum začatia fakturácie a frekvenciu fakturácie.
5. Na vedľajšej mriežke vyberte **Generovať plán faktúr**. Vygeneruje sa plán faktúr s poľami **Dátum spustenia faktúry**, **Dátum uzávierky transakcie** a **Stav spustenia** nastavené nasledujúcim spôsobom:

    - **Dátum spustenia faktúry**: Tento dátum určený na základe frekvencie faktúr.
    - **Dátum uzávierky transakcie**: Deň pred dátumom spustenia faktúry.
    - **Stav spustenia**: Automaticky nastavený **Nie je spustený**. Keď sa úloha automatického vytvárania faktúr spustí pre určitý dátum spustenia faktúry, toto pole sa aktualizuje na **Spustenie bolo úspešné** alebo **Spustenie zlyhalo**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Vytvorenie plánu faktúr s pevnou cenou pre riadok zmluvy

Keď má riadok zmluvy pevný spôsob fakturácie, môžete vytvoriť plán fakturácie na základe medzníka. 

> [!NOTE]
> Medzníky nemožno vytvoriť pre riadok zmluvy, ak k tomuto riadku zmluvy nie je priradený žiadny projekt.

Vykonaním nasledujúcich krokov vygenerujete plán fakturácie na základe medzníka pre pevne nastavené alebo rovnomerne rozložené medzníky pre kalendárne obdobie.

1. Prejdite do časti **Nastavenia** > **Frekvencie faktúr** a nastavte frekvenciu fakturácie.
2. Prejdite na záznam projektovej zmluvy a na karte **Súhrn** v poli **Požadovaný dátum dodania** vyberte dátum.
3. Otvorte riadok zmluvy **Pevná cena**, pre ktorý vytvárate plán medzníka. Na karte **Medzníky fakturácie** vyberte dátum začatia fakturácie a frekvenciu fakturácie. 
4. Na vedľajšej mriežke vyberte **Generovať periodické medzníky**. Plán faktúr sa generuje s poľami **Názov medzníka**, **Dátum medzníka** a **Suma medzníka** nastavenými nasledovne:

    - **Názov míľnika**: Tento názov je určený frekvenciou fakturácie.
    - **Dátum medzníka**: Tento dátum určený na základe frekvencie faktúr.
    - **Suma medzníka**: Táto suma sa počíta vydelením sumy zmluvy v riadku zmluvy počtom medzníkov, podľa určenia frekvenciou, začiatkom fakturácie a požadovanými termínmi dodania.

    Ak má riadok zmluvy hodnotu v poli **Odhadovaná výška dane**, tak sa toto pole pri generovaní pravidelných medzníkov pridelí rovnomerne každému medzníku.

Medzníky fakturácie by sa mali rovnať zmluvnej hodnote v riadku zmluvy. V opačnom prípade sa na stránke **Riadok zmluvy** zobrazí chyba. Chybu môžete opraviť tak, že vytvoríte, upravíte alebo odstránite medzníky tak, že overíte, či čiastkové medzníky fakturácie obsahujú zmluvne dohodnutú hodnotu riadka. Po vykonaní zmien odstráňte chybu obnovením stránky.

### <a name="manually-create-milestones"></a>Manuálne vytváranie medzníkov

Medzníky s pevnou cenou môžete vygenerovať aj manuálne, ak nie sú pravidelne rozdelené. Podľa nasledujúcich pokynov manuálne vytvorte medzník.

1. Otvorte riadok zmluvy s pevnou cenou, pre ktorý vytvárate medzník a na karte **Plán faktúr** vo vedľajšej mriežke vyberte možnosť **+ Vytvoriť nový medzník riadka zmluvy**. 
2. Na stránke **Vytvorenie medzníka** zadajte požadované informácie na základe nasledujúcej tabuľky.

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| Názov medzníka | Rýchle vytvorenie | Textové pole pre názov medzníka. | Prenesie sa na medzník riadka zmluvy projektu a na faktúru. |
| Projektová úloha | Rýchle vytvorenie | Ak je medzník naviazaný na úlohu projektu, tak pomocou tohto odkazu pridáte vlastnú logickú súpravu stavu medzníka na základe stavu úlohy. | Aplikácia nemá žiadny následný dopad tohto odkazu na úlohu. |
| Dátum medzníka | Rýchle vytvorenie | Nastavte dátum, kedy má proces automatického vytvárania faktúr vyhľadávať stav tohto medzníka, aby sa zohľadnil pri fakturácii. | Prenesie sa na medzník riadka zmluvy projektu a na faktúru. |
| Stav faktúry | Rýchle vytvorenie | Keď sa vytvorí medzník, tento stav sa vždy nastaví na **Nepripravené na fakturáciu** alebo **Nezačaté**. | Prenesie sa na medzník riadka zmluvy projektu a na faktúru. |
| Suma riadka | Rýchle vytvorenie | Suma alebo hodnota medzníka, ktorá bude fakturovaná zákazníkovi. | Prenesie sa na medzník riadka zmluvy projektu a na faktúru. |
| Daň | Rýchle vytvorenie | Suma dane použitá pre medzník. | Prenesie sa na medzník riadka zmluvy projektu a na faktúru. |

3. Vyberte položku **Uložiť a zavrieť**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]