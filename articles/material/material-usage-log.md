---
title: Zaznamenanie využitia materiálu na projektoch a projektových úlohách
description: Táto téma obsahuje informácie o tom, ako zaznamenať použitie materiálu v projektoch a projektových úlohách.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d8757049953fab0ad8bf6ee1a1d695fcb6df75b1be52641ad4af3b3137d7a0a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999290"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Zaznamenanie využitia materiálu na projektoch a projektových úlohách

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Keď projektový tím pracuje na úlohách na projekte, spotrebúva alebo používa materiály. Denník použitia materiálu poskytuje spôsob, ako zaznamenať toto použitie, aby ho mohol schváliť projektový manažér a prípadne fakturovať zákazníkovi. 

Ak chcete zaznamenať použitie katalógových alebo pridaných materiálov a predložiť ich schvaľovateľovi, postupujte takto: 

1. Na navigačnej table vyberte možnosť **Použitie materiálu** a potom vyberte **Nový**.
2. Na stránke **Použitie nového materiálu** zadajte požadované informácie o použití materiálu a potom vyberte **Uložiť**.

Nasledujúca tabuľka poskytuje informácie o poliach na stránke **Denník použitia materiálu**. 

| **Pole** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- |
| Popis | Popis konkrétneho použitia materiálu. | Toto pole nemá žiadny následný dopad. |
| Dátum | Dátum, kedy sa predpokladá použitie materiálu. | Toto pole nemá žiadny následný dopad. |
| Project | Zoznam aktívnych projektov. | Výber projektu pre denník použitia materiálu ovplyvní pole **Úloha** a budú sa zobrazovať iba tie úlohy, ktoré sú na projekte. |
| Úloha | Zoznam úloh pre projekt vrátane súhrnu a úloh listových uzlov. | Výber úlohy pre denník použitia materiálu ovplyvní skutočné náklady na materiál a skutočný predaj materiálu pre danú úlohu. Ak je toto pole prázdne, príslušné náklady na použitie materiálu a tržby sa sledujú a sumarizujú iba na úrovni projektu. |
| Vyberte produkt | Uveďte, či je toto použitie materiálu pre **Existujúci** (katalógový) produkt alebo pre **Pridaný** produkt. | Toto pole určuje typ produktu. |
| Produkt | ID produktu z katalógu produktov. Po výbere ID produktu sa pole **Vyberte Produkt** automaticky aktualizuje na **Existujúci produkt**. ID sa používa na načítanie nákladových a predajných cien z cenníka. | Toto pole nemá žiadny následný dopad. |
| Opis pridaného produktu | Textové pole na napísanie do názvu produktu. Toto pole je dostupné, ak vyberiete **Pridaný** produkt v poli **Vyberte produkt**.| Toto pole nemá žiadny následný dopad. |
| Rezervovateľný zdroj| Zdroj, ktorý použil tento materiál na projekt. Predvolená hodnota pre toto pole je rezervovateľný zdroj prihláseného používateľa, ale je možné ju zmeniť tak, aby zaznamenávala využitie v mene ostatných členov projektového tímu. | Toto pole nemá žiadny následný dopad. |
| Jednotková skupina | Predvolená hodnota v tomto poli pochádza z jednotkovej skupiny, ktorá je nastavená ako predvolená pre katalógový produkt. Toto pole môžete aktualizovať, aby ste vybrali inú jednotkovú skupinu. | Toto pole nemá žiadny následný dopad. |
| Jednotka | Predvolená hodnota v tomto poli je predvolenou jednotkou vybraného produktu. Toto pole môžete aktualizovať, aby ste vybrali inú jednotku. | Výsledkom zmeny jednotky je iná predvolená jednotková cena a náklady. |
| Počet | Množstvo produktu, ktoré sa použilo na projekt alebo projektovú úlohu. | Toto pole nemá žiadny následný dopad. |
| Jednotkové náklady | Jednotkové náklady na vybratý produkt a kombinácia jednotiek, ako sú stanovené v príslušnom cenníku nákladov. | Jednotkové náklady sa vždy zobrazujú v mene nákladov projektu. Ak v cenníku nie sú jednotkové náklady na kombinovaný produkt a jednotka, jednotkové náklady sa predvolene nastavia na 0,00. |
| Celkové náklady | Suma nákladov, ktorá sa počíta ako množstvo \* jednotkové náklady.| Suma nákladov sa vždy zobrazuje v mene nákladov projektu. |


## <a name="submit-material-usage-for-review-and-approval"></a>Odoslanie použitia materiálu na kontrolu a schválenie 
Keď zaznamenáte celé svoje využitie materiálu a ste pripravení nechať ho schváliť, musíte odoslať informácie o použití na kontrolu.

1. Prejdite na stránku **Denník použitia materiálu** a vyberte jeden alebo viac záznamov. Alebo vyberte všetky záznamy o použití materiálu pomocou začiarkavacieho políčka v hlavičke.
2. Stlačte možnosť **Odoslať**. Systém spracuje vybrané položky a potom vytvorí žiadosti o schválenie použitia materiálu.

## <a name="recall-a-material-usage-log"></a>Odvolanie denníka použitia materiálu

V prípade potreby môžete odvolať uvedené množstvo materiálu. Čas potrebný na odvolanie položky použitia materiálu závisí od etapy schválenia.  Ak schvaľovateľ ešte neschválil záznam, k odvolaniu môže dôjsť okamžite. Ak však už bol záznam schválený, požaduje sa od schvaľovateľa, aby schválil odvolanie a zrušil transakcie.

1. Prejdite na **Použitie materiálu** a v zozname denníkov použitia materiálu vyberte použitie materiálu, ktoré chcete odvolať.
2. Vyberte položku **Odvolať**. Ak položka použitia materiálu ešte nebola schválená, systém ju okamžite odvolá. Ak položka materiálu už bola schválená, vytvorí sa žiadosť o odvolanie, ktorá informuje schvaľovateľa, že chcete odvolať použitie materiálu. Schvaľovateľ potom potvrdí, že je možné vykonať zrušenie a záznam sa vráti.

## <a name="delete-a-material-usage-log"></a>Odstránenie denníka použitia materiálu

Môžete odstrániť denníky použitia materiálu, ktoré neboli odoslané. Ak chcete odstrániť denník použitia materiálu, ktorý už bol odoslaný, musíte ho najskôr odvolať.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
