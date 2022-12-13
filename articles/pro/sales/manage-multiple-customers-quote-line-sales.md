---
title: Spravujte viacerých zákazníkov na riadkoch projektovej ponuky
description: Tento článok popisuje, ako spravovať viacerých zákazníkov na riadkoch projektovej ponuky.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 70007499ea61e7d81df071cc6d003896d721555b
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824458"
---
# <a name="manage-multiple-customers-on-project-quote-lines"></a>Spravujte viacerých zákazníkov na riadkoch projektovej ponuky

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Riadky ponuky projektu podporujú scenáre, kde každý riadok ponuky obsahuje zoznam zákazníkov, ktorí za ňu platia. Tento zoznam zákazníkov v riadku cenovej ponuky založenej na projekte môže byť rovnaký ako zoznam zákazníkov v cenovej ponuke. Môžete tiež zmeniť zoznam zákazníkov, aby sa líšili. Po získaní ponuku cenovej ponuky na projekt sa zoznam zákazníkov v riadku cenovej ponuky založenej na projekte skopíruje do zodpovedajúceho riadku zmluvy založenej na projekte, aby sa vytvorila prípadná zmluva o projekte. Zákazníci projektovej ponuky založenej na projekte sa skopírujú do projektovej zmluvy.

Keď fakturujete prípadnú projektovú zmluvu, zoznam zákazníkov v riadku zmluvy na základe projektu má prednosť pred zoznamom na projektovej zmluve. Zoznam zákazníkov na zmluve o projekte sa používa na predvolenie nových riadkov zmlúv o projekte.

Všetky cenové ponuky zákazníkov na karte **Zákazníci** cenovej ponuky projektu budú predvolené ako riadok cenovej ponuky zákazníkov na všetkých nových riadkoch cenovej ponuky založenej na projekte vytvorených pre cenovú ponuku na projekt. Žiadne existujúce riadky cenových ponúk založené na projekte nezdedia nové zákaznícke záznamy cenových ponúk vytvorené po nich.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Vytvorenie, aktualizovanie alebo odstránenie záznamu zákazníka riadka cenovej ponuky

Na karte **Zákazníci riadka cenovej ponuky** na stránke **Riadok cenovej ponuky založenej na projekte** môžete vytvoriť, aktualizovať alebo vymazať zákazníka riadka cenovej ponuky. Keď do riadka cenovej ponuky založenej na projekte pridáte nového zákazníka, zákazník sa pridá aj do celkovej ponuky ako zákazník ponuky s predvoleným percentom rozdelenia fakturácie na celkovú cenovú ponuku 0 %. Percento rozdelenia fakturácie na celkovej cenovej ponuke sa skopíruje do nových riadkov cenovej ponuky a do prípadnej projektovej zmluvy. Keď sa však fakturuje zo zmluvy, použije sa percento rozdelenia fakturácie na úrovni riadka cenovej ponuky, nie percento rozdelenia fakturácie na celkovej úrovni zmluvy. 

V nasledujúcej tabuľke sú uvedené polia v zákazníckom zázname riadka cenovej ponuky z riadka cenovej ponuky založenej na projekte.

| Pole | Oblasť | Popis a pokyny | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| **Obchodný vzťah** | Upraviteľná mriežka na karte **Zákazníci riadka cenovej ponuky**, hlavný formulár a formuláre na rýchle vytvorenie pre riadok zákazníka cenovej ponuky. | Zobrazenie zoznamu všetkých aktívnych účtov. Po vytvorení záznamu je toto pole uzamknuté. Ak potrebujete aktualizovať pole, vymažte a znova vytvorte záznam. Ak ste zaznamenali nejaké skutočné hodnoty, záznam nemôžete vymazať. | Keď si vyberiete obchodný vzťah z hlavného zoznamu obchodných vzťahov, ktorý chcete pridať, zákazník riadka cenovej ponuky sa po uložení tiež pridá ako zákazník cenovej ponuky. Po získaní cenovej ponuky sa zákazníci riadka cenovej ponuky prekopírujú k zákazníkom riadka zmluvy o projekte. |
| **Percento rozdelenia fakturácie** | Upraviteľná mriežka na karte **Zákazníci riadka cenovej ponuky**, hlavný formulár a formuláre na rýchle vytvorenie pre riadok zákazníka cenovej ponuky. | Predstavuje percento každej nevyfakturovanej predajnej transakcie, ktorá sa pripíše tomuto zákazníkovi riadka cenovej ponuky. | Skopírované k zákazníkom riadka zmluvy projektu. |
| **Limit, ktorý sa nesmie prekročiť** | Upraviteľná mriežka na karte **Zákazníci riadka cenovej ponuky**, hlavný formulár a formuláre na rýchle vytvorenie pre riadok zákazníka cenovej ponuky. | Označuje, či existuje dohodnutý limit alebo strop celkovej sumy, ktorá bude fakturovaná tomuto zákazníkovi za tento riadok cenovej ponuky. | Skopírované do zákazníkov riadka zmluvy projektu po získaní cenovej ponuky. |
| **Zaokrúhľuje** | Upraviteľná mriežka na karte **Zákazníci riadka cenovej ponuky**, hlavný formulár a formuláre na rýchle vytvorenie pre riadok zákazníka cenovej ponuky. | Označuje, či je tento zákazník predvoleným zákazníkom zaokrúhľovania pre tento riadok cenovej ponuky založenej na projekte. | Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky. |

## <a name="edit-billing-split-percentages"></a>Upraviť percentá rozdelenia fakturácie

Percentuálne rozdelenie fakturácie môžete upraviť priamo. Ak percentá rozdelenia fakturácie nedosiahnu 100 %, dôjde k chybe. Po úprave percentuálnych podielov rozdelenia fakturácie chybu obnovte obnovením stránky riadka cenovej ponuky.

Pomocou akcie rovnomerného rozloženia vo vedľajšej mriežke zákazníkov riadka cenovej ponuky prideľte rozdelenie fakturácie všetkým zákazníkom riadka cenovej ponuky. Ak existuje faktor zaokrúhľovania, pridá sa k zákazníkovi zaokrúhľovania. Jeden zo zákazníkov riadka cenovej ponuky je vždy označený ako zákazník zaokrúhľovania, čo znamená, že v zázname zákazníka riadka cenovej ponuky je príznak zaokrúhľovania nastavený na **Áno**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
