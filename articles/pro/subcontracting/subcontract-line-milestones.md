---
title: Medzníky v riadku subdodávateľskej zmluvy
description: Táto téma vysvetľuje, ako vytvoriť a udržiavať plán faktúr pre subdodávateľskú zmluvu s dodávateľom založený na medzníkoch.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7f99853f5f649f96225b7d72580db97bb92de7c5
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558521"
---
# <a name="subcontract-line-milestones"></a>Medzníky v riadku subdodávateľskej zmluvy

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

V Dynamics 365 Project Operations môže riadok subdodávateľskej zmluvy s metódou fakturácie s pevnou cenou u dodávateľa špecifikovať plán faktúr založený na medzníkoch.

Medzníky pre fakturáciu dodávateľom je možné generovať automaticky podľa nastavenej frekvencie, alebo ich môžete vytvoriť ručne.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Automatické vytvorenie plánu faktúr založeného na medzníkoch pre riadok subdodávateľskej zmluvy

Vykonajte nasledujúce kroky, aby ste automaticky vygenerovali plán faktúr založený na medzníkoch pre pevnú množinu rovnomerne rozložených medzníkov.

1. Prejdite do ponuky **Nastavenia** > **Frekvencie faktúry** a nastaviť frekvenciu faktúr pre riadky subdodávateľskej zmluvy.
2. Otvorte stránku **Subdodávateľské zmluvy**, otvorte subdodávateľskú zmluvu, s ktorou chcete pracovať, a potom otvorte riadok subdodávateľskej zmluvy s pevnou cenou, pre ktorú sa chystáte vytvoriť medzník.
3. Na karte **Medzníky v riadku subdodávateľskej zmluvy** vyberte **Generovať periodické medzníky**.
4. V dialógovom okne zadajte alebo vyberte rozsah dátumov, počet medzníkov a frekvenciu faktúr. Môžete vybrať dátum začatia alebo počet medzníkov a frekvenciu alebo dátum začatia faktúry alebo dátum ukončenia a frekvenciu faktúr. Nemôžete vybrať dátum ukončenia a počet medzníkov.
Pomocou týchto informácií systém generuje medzníky a záznamy, ktoré sú zobrazené v mriežke **Medzníky**.

   - **Názov medzníka** – Názov medzníka je nastavený na dátum medzníka na základe frekvencie faktúr.
   - **Dátum medzníka** – Dátum na základe frekvencie faktúr.
   - **Suma medzníka** – Vypočítané vydelením hodnoty medzisúčtu na riadku subdodávateľskej zmluvy počtom medzníkov.

Ak má riadok subdodávateľskej zmluvy hodnotu v poli **Odhadovaná čiastka dane**, v tomto poli sa táto hodnota pripočíta ku každému medzníku rovnako pri generovaní pravidelných medzníkov.

Súčet súm medzníkov v riadku subdodávateľskej zmluvy sa musí rovnať hodnotu riadka subdodávateľskej zmluvy. Ak nie sú rovnaké, dôjde k chybe. Chybu môžete opraviť a overiť, či sa celková suma medzníka rovná hodnote riadka subdodávateľskej zmluvy vytvorením, úpravou alebo odstránením sumy medzníka a daní. Po vykonaní zmien stránku uložte a obnovte, aby ste sa vyhli ďalším chybám.

## <a name="manually-create-subcontract-line-milestones"></a>Ručné vytvorenie medzníkov v riadku subdodávateľskej zmluvy

Medzníky s pevnou cenou v riadku subdodávateľskej zmluvy je možné generovať ručne, ak nie sú pravidelne rozdelené. Ak chcete vytvoriť medzník v riadku subdodávateľskej zmluvy, postupujte podľa nasledujúcich krokov.

1. Na navigačnej table vyberte položku **Subdodávateľské zmluvy** a otvorte subdodávateľskú zmluvu, s ktorou chcete pracovať.
2. Otvorte riadok subdodávateľskej zmluvy s pevnou cenou, pre ktorú chcete vytvoriť medzník.
3. Na karte **Medzníky v riadku subdodávateľskej zmluvy** vyberte na vedľajšej mriežke **+ Nový medzník riadka subdodávateľskej zmluvy**.
4. Na stránke **Nový medzník riadka subdodávateľskej zmluvy** zadajte požadované informácie na základe nasledujúcej tabuľky.

    | Pole | Popis |Funkčný vplyv|
    | --- | --- |----------------------|
    | Názov medzníka | Názov medzníka. |Toto sa zobrazí ako prvý stĺpec vo všetkých vyhľadávaniach na základe míľnikov subdodávateľských zmlúv. Riadok faktúry dodávateľa, ktorý je vytvorený na základe tohto míľnika, bude tiež používať názov míľnika riadka subdodávateľskej zmluvy ako predvolený názov riadka faktúry dodávateľa.|
    | Popis | Popis medzníka. |Riadok faktúry dodávateľa, ktorý je vytvorený na základe tohto míľnika, bude tiež používať opis míľnika riadka subdodávateľskej zmluvy ako predvolený opis riadka faktúry dodávateľa.|
    | Dátum medzníka | Dátum, kedy by mal proces automatického vytvárania faktúry vyhľadávať stav tohto medzníka a zohľadniť ho pri fakturácii.| Táto hodnota bude použitá ako predvolený dátum riadka faktúry dodávateľa pri fakturácii pre tento riadok subdodávateľskej zmluvy. |
    | Množstvo | Suma alebo hodnota medzníka, ktorá bude fakturovaná zákazníkovi. |Táto hodnota sa používa ako predvolený suma riadka faktúry dodávateľa pri fakturácii pre tento riadok subdodávateľskej zmluvy. |
    | Daň | Suma dane použitá pre medzník.| Táto hodnota sa používa ako predvolená sumu dane faktúry dodávateľa pri fakturácii pre tento riadok subdodávateľskej zmluvy. |
    | Suma po zdanení | Toto pole iba na čítanie sa počíta ako suma + daň.|Táto hodnota sa používa ako predvolená hodnota riadka faktúry dodávateľa pri fakturácii pre tento riadok subdodávateľskej zmluvy. |
    | Stav faktúry | Pri vytváraní medzníka je tento stav vždy nastavený na **Nie je pripravené na fakturáciu**.|  Keď je stav **Pripravené na fakturáciu**, vytvorenie faktúry dodávateľa obsahuje tento medzník na faktúre dodávateľa. |

5. Vyberte položku **Uložiť a zavrieť**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
