---
title: Správa viacerých zákazníkov v riadkoch zmlúv založených na projekte – čiastočné
description: Táto téma poskytuje informácie o správe viacerých zákazníkov v riadkoch zmlúv založených na projekte.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 23bb4cebd16bd1e8ae572d3e54538756547ae39e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003041"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Správa viacerých zákazníkov v riadkoch zmlúv založených na projekte – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Riadky zmlúv založených na projekte môžu obsahovať zoznam zákazníkov, ktorí sú zodpovední za platbu. Tento zoznam zákazníkov na riadku zmluvy založenej na projekte môže byť rovnaký ako zoznam zákazníkov v zmluve, ale nie je to potrebné. Keď sa získa projektová cenová ponuka a vytvorí sa projektová zmluva, zoznam zákazníkov na riadku cenovej ponuky sa skopíruje do príslušného riadka zmluvy. Zákazníci na cenovej ponuke sú skopírovaní do zmluvy.

Keď je projektová zmluva fakturovaná, zoznam zákazníkov na riadku zmluvy založenej na projekte má prednosť pred zoznamom zákazníkov v zmluve. Zoznam zákazníkov v projektovej zmluve sa používa iba na predvolenie nových riadkov zmluvy.

Všetci zmluvní zákazníci na karte **Zákazníci** v projektovej zmluve predvolene vystupujú ako zákazníci riadku zmluvy v akýchkoľvek nových riadkoch zmlúv, ktoré sú vytvorené pre projektovú zmluvu. Žiadne existujúce riadky zmluvy nebudú dediť nové záznamy zákazníkov zmluvy vytvorené po nich.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Vytvorenie, aktualizácia alebo odstránenie záznamu zákazníka v riadku zmluvy

Zákazníka v riadku zmluvy môžete vytvoriť, aktualizovať alebo odstrániť na karte Zákazníci na riadku zmluvy na stránke Riadky zmlúv založených na projekte. Keď sa na riadok zmluvy založenej na projekte pridá nový zákazník, pridá sa tiež k celkovej zmluve ako zmluvný zákazník s predvoleným nulovým percentuálnym podielom rozdelenia. Percento rozdelenia fakturácie na celkovej zmluve sa skopíruje do nových riadkov zmluvy a do prípadnej projektovej zmluvy. Pri fakturácii zo zmluvy sa však používa percentuálne rozdelenie fakturácie na úrovni riadka zmluvy a nie percento rozdelenia fakturácie na úrovni celkovej zmluvy.

Nižšie sú polia v zázname zákazníka v riadku **Zmluvy** založenej na projekte, na ktorú nezabudnite, keď s ňou pracujete:

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| **Obchodný vzťah** | Editovateľná mriežka na karte **Zmluvní zákazníci** a vo formulároch **Hlavný** a **Rýchle vytvorenie** pre zmluvného zákazníka. | Všetky aktívne obchodné vzťahy. Po vytvorení záznamu je toto pole uzamknuté. Ak chcete aktualizovať pole, odstráňte záznam a vytvorte nový záznam. Ak ste zaznamenali nejaké skutočné hodnoty, nemôžete záznam vymazať. Pre daný obchodný vzťah však môžete percentuálne rozdelenie fakturácie označiť ako nulové. Ak je záznam označený ako nula, budú ovplyvnené všetky budúce skutočné hodnoty nákladov a výnosov, ktoré sú priradené alebo rozdelené tomuto zákazníkovi. | Keď vyberiete obchodný vzťah z hlavného zoznamu obchodných vzťahov, ktorý chcete pridať a uložiť, zákazník na riadku zmluvy sa tiež pridá ako zmluvný zákazník. Zákazníci na riadkoch zmluvy sa používajú pri generovaní faktúr. |
| **Percento rozdelenia fakturácie** | Editovateľná mriežka na karte **Zmluvní zákazníci** a vo formulároch **Hlavný** a **Rýchle vytvorenie** pre zmluvného zákazníka. | Toto pole predstavuje percento každej nevyfakturovanej predajnej transakcie, ktorá sa pripíše tomuto zákazníkovi na riadku zmluvy. | Zákazníci na riadky zmluvy a percentá rozdelenia fakturácie sa používajú pri vytváraní skutočných hodnôt po schválení a pri generovaní faktúry. |
| **Limit, ktorý sa nesmie prekročiť** | Editovateľná mriežka na karte **Zmluvní zákazníci** a vo formulároch **Hlavný** a **Rýchle vytvorenie** pre zmluvného zákazníka. | Označuje, či existuje dohodnutý limit alebo strop celkovej sumy, ktorá bude zákazníkovi fakturovaná pre riadok zmluvy. | Limit, ktorý sa nesmie prekročiť, pre zákazníka v riadku zmluvy, sa používa pri vytváraní skutočných hodnôt a generovaní faktúr. |
| **Zaokrúhľuje** | Editovateľná mriežka na karte **Zmluvní zákazníci** a vo formulároch **Hlavný** a **Rýchle vytvorenie** pre zákazníka v riadku zmluvy. | Toto pole označuje, či je tento zákazník predvoleným zákazníkom zaokrúhľovania pre tento riadok zmluvy založenej na projekte. | Keď generujete skutočnú hodnotu podľa percentuálneho podielu fakturácie, môžu sa vyskytnúť určité rozdiely v zaokrúhľovaní. Tomuto zákazníkovi sa v tomto prípade pripisujú rozdiely v zaokrúhľovaní. |

## <a name="edit-billing-split-percentages"></a>Upraviť percentá rozdelenia fakturácie

Percento rozdelenia fakturácie je možné upravovať v mriežke. Ak percentá rozdelenia fakturácie nedosiahnu 100 percent, nastane chyba. Po úprave percenta rozdelenia fakturácie chybu odstránite obnovením stránky.

Môžete tiež vybrať **Rovnomerne distribuovať** na vedľajšej mriežke zákazníka v riadku zmluvy. Táto akcia rovnomerne prideľuje fakturačné rozdelenie všetkým zákazníkom v riadkoch zmluvy. Ak existuje akýkoľvek faktor zaokrúhľovania, pridá sa k zákazníkovi zaokrúhľovania. Jeden zákazník v riadku zmluvy je vždy označený ako zákazník **Zaokrúhľovania** s príznakom **Zaokrúhľovanie** nastaveným na **Áno**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]