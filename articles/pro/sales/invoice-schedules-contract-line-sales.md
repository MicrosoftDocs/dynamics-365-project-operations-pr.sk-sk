---
title: Vytváranie plánov faktúr v riadku zmluvy založenej na projekte – čiastočné
description: Táto téma poskytuje informácie o vytváraní plánov faktúr a medzníkov.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 728a35b2b69fb63a2b20f218c250365c5068370f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180346"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Vytváranie plánov faktúr v riadku zmluvy založenej na projekte – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Plán faktúry môžete pripojiť k riadku zmluvy založenej na projekte. Fakturácia je povolená až po získaní zmluvy na vytvorenie projektovej zmluvy. Plány faktúr umožňujú automatické vytváranie konceptov faktúr pre riadok zmluvy založenej na projekte. Ak plánujete faktúry vytvárať vždy manuálne, môžete preskočiť vytváranie plánov faktúr na riadkoch zmluvy založenej na projekte alebo na riadku zmluvy.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Vytvorenie plánu faktúry za čas a materiál v riadku zmluvy založenej na projekte

Keď riadok zmluvy založený na projekte obsahuje metódu fakturácie času a materiálu, môžete vytvoriť plán faktúr na základe dátumu. Ak chcete automaticky generovať harmonogram faktúr na základe dátumu, postupujte nasledovne.

1. Prejdite do **Nastavenie** > **Frekvencie faktúr** na nastavenie frekvencie faktúr.
2. Otvorte projektovú zmluvu a na karte **Zhrnutie** nastavte požadovaný dátum dodania.
3. Otvorte riadok zmluvy pre čas a materiál, pre ktorý chcete vytvoriť plán fakturácie založený na dátume. 
4. Na karte **Plán faktúr** vyberte dátum začatia fakturácie a frekvenciu fakturácie. 
5. Na vedľajšej mriežke vyberte **Generovať plán faktúr**.

    Systém generuje plán faktúr s nasledujúcimi informáciami v poli:

    - **Dátum spustenia faktúry** je nastavený na dátum na základe frekvencie faktúr.
    - **Dátum uzávierky transakcie** je nastavený deň pred **Dátumom spustenia faktúry**.
    - **Stav spustenia** je automaticky nastavený **Nie je spustený**. Keď sa úloha automatického vytvárania faktúr spustí pre určitý **Dátum spustenia faktúry**, toto pole sa aktualizuje na **Spustenie bolo úspešné** alebo **Spustenie zlyhalo**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Vytvorenie plánu faktúry s pevnou cenou pre riadok zmluvy založenej na projekte

Keď má riadok zmluvy založenej na projekte metódu fakturácie s pevnou cenou, môžete vytvoriť časový plán faktúr založený na medzníku. Vykonajte nasledujúce kroky a automaticky vygenerujte plán fakturácie na základe medzníka pre pevnú skupinu medzníkov, ktoré sa rovnomerne rozložia pre kalendárne obdobie.

1. Prejdite do **Nastavenie** > **Frekvencie faktúr** na nastavenie frekvencie faktúr.
2. Otvorte projektovú zmluvu a na karte **Zhrnutie** nastavte požadovaný dátum dodania.
3. Otvorte riadok zmluvy s pevnou cenou, v ktorom potrebujete vytvoriť plán medzníkov. 
4. Na karte **Plán faktúr (Medzníky fakturácie)** vyberte dátum začatia fakturácie a frekvenciu fakturácie. 
5. Na vedľajšej mriežke vyberte **Generovať periodické medzníky**.

    Systém generuje plán faktúr s nasledujúcimi informáciami o medzníku.

    - **Názov medzníka** je nastavený na dátum, ktorý je určený na základe frekvencie faktúr.
    - **Dátum medzníka** je nastavený na dátum, ktorý je určený na základe frekvencie faktúr.
    - **Suma medzníka** sa počíta vydelením sumy zmluvy na riadku zmluvy založenej na projekte počtom medzníkov určených frekvenciou, začiatkom fakturácie a požadovanými termínmi dodania.
    - Ak má riadok zmluvy hodnotu v poli **Odhadovaná výška dane**, toto pole je tiež priradené každému medzníku rovnako pri generovaní periodických medzníkov.

Medzníky fakturácie by sa mali rovnať zmluvnej hodnote riadka zmluvy založenej na projekte. Ak nie sú rovnaké, dôjde k chybe. Túto chybu môžete opraviť tak, že vytvoríte, upravíte alebo odstránite medzníky tak, že overíte, či čiastkové medzníky fakturácie dosahujú celkovú zmluvnú hodnotu riadka. Po vykonaní zmien obnovte stránku.

### <a name="manually-create-milestones"></a>Manuálne vytváranie medzníkov

Medzníky pevnej ceny je možné generovať manuálne, ak nie sú pravidelne rozdelené. Ak chcete vytvoriť medzník manuálne, vykonajte nasledujúce kroky.

1. Otvorte riadok zmluvy s pevnou cenou, v ktorom chcete vytvoriť medzník. 
2. Na karte **Plán faktúry** na vedľajšej mriežke vyberte **+ Vytvoriť nový medzník riadka zmluvy**.
3. Vo formulári **Vytvorenie medzníka** zadajte požadované informácie na základe nasledujúcej tabuľky. 

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| Názov medzníka | Rýchle vytvorenie | Textové pole pre názov medzníka. | Toto pole je súčasťou medzníka riadka projektovej zmluvy a faktúry. |
| Projektová úloha | Rýchle vytvorenie | Ak je medzník viazaný na úlohu projektu, použite tento odkaz na pridanie vlastnej logiky a nastavenie stavu medzníka na základe stavu úlohy. | Tento odkaz na úlohu nemá žiadny následný dopad. |
| Dátum medzníka | Rýchle vytvorenie | Dátum, kedy by mal proces automatického vytvárania faktúry hľadať stav tohto medzníka, aby sa zohľadnil pri fakturácii. | Toto je súčasťou medzníka riadka projektovej zmluvy a faktúry. |
| Stav faktúry | Rýchle vytvorenie | Po vytvorení medzníka je tento stav vždy nastavený na **Nepripravené na fakturáciu** alebo **Nezačaté**. | Toto je súčasťou medzníka riadka projektovej zmluvy a faktúry. |
| Suma riadka | Rýchle vytvorenie | Suma alebo hodnota medzníka, ktorá bude fakturovaná zákazníkovi. | Toto pole je súčasťou medzníka riadka projektovej zmluvy a faktúry, |
| Daň | Rýchle vytvorenie | Suma dane použitá pre medzník. | Toto je súčasťou medzníka riadka projektovej zmluvy a faktúry. |

4. Vyberte položku **Uložiť a zavrieť**.
