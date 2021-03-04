---
title: Správa viacerých zákazníkov v projektových zmluvách – čiastočné
description: Táto téma poskytuje informácie o správe viacerých zákazníkov v projektových zmluvách.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b248dabdbd5239b140da7c99d3f38609facfe75e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181336"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Správa viacerých zákazníkov v projektových zmluvách – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Projektové zmluvy v Dynamics 365 Project Operations podporujú scenár, keď zmluva zahŕňa viacerých zákazníkov, ktorí financujú obchod. Karta **Zhrnutie** na stránke **Zmluva o projekte** obsahuje pole **Zákazník**. Toto pole identifikuje primárneho zákazníka obchodu. Ďalší zákazníci v rámci obchodu môžu byť nastavení na karte **Zákazníci** stránky **Projektová zmluva**.

Všetci zmluvní zákazníci uvedení v projektovej zmluve o projekte predvolene vystupujú ako zákazníci riadku zmluvy v akýchkoľvek nových projektových riadkoch zmlúv, ktoré sú vytvorené pre projektovú zmluvu. Existujúce riadky zmlúv založené na projekte nededia nových zmluvných zákazníkov, pretože sa vytvárajú nové záznamy.

Produktové riadky zmluvy sú automaticky spojené s primárnym zákazníkom.

Zmluvní zákazníci a zákazníci riadkov zmluvy môžu byť pridaní, aktualizovaní alebo vymazaní kedykoľvek pred získaním zmluvy.

## <a name="primary-customer"></a>Primárny zákazník

Zákazník uvedený na karte **Zhrnutie** projektovej zmluvy ako potenciálny zákazník je primárnym zákazníkom zmluvy. Pri pokuse o odstránenie primárneho zákazníka zo zoznamu zákazníkov v zmluve sa zobrazí chybové hlásenie, že záznam primárneho zákazníka v zmluve nie je možné odstrániť.

Primárneho zákazníka nemožno aktualizovať zo zoznamu zmluvných zákazníkov. Namiesto toho zmeňte potenciálneho zákazníka na karte **Zhrnutie** zmluvy. Keď sa toto pole aktualizuje na stránke **Zhrnutie zmluvy**, nový zákazník sa pridá ako nový zmluvný zákazník s nastaveným príznakom **Primárny**. Predchádzajúci primárny zákazník bude naďalej zákazníkom na základe zmluvy.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Vytvorenie, aktualizácia alebo odstránenie záznamu zmluvného zákazníka

Zmluvného zákazníka je možné vytvoriť, aktualizovať alebo vymazať z karty **Zákazníci** na stránke **Projektová zmluva**. Polia v nasledujúcej tabuľke sa nachádzajú v zázname zmluvného zákazníka projektovej zmluvy a mali by ste ich mať na pamäti pri práci so zmluvou.

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| **Obchodný vzťah** | Mriežku je možné upravovať na karte **Zmluvní zákazníci** a vo formulároch **Hlavný** a **Rýchle vytvorenie** pre zmluvného zákazníka. | Zobrazenie zoznamu všetkých aktívnych účtov. Po vytvorení záznamu je toto pole uzamknuté. Ak chcete aktualizovať obchodný vzťah, odstráňte záznam a znova ho vytvorte. Ak ste zaznamenali nejaké skutočné hodnoty alebo ak je záznam zmluvného zákazníka primárnym zákazníkom, nemôžete záznam odstrániť. | Zmluvní zákazníci sa pri vytvorení riadka zmluvy prekopírujú ako zákazníci riadka zmluvy. |
| **Percento rozdelenia fakturácie** | Mriežku je možné upravovať na karte **Zmluvní zákazníci** a vo formulároch **Hlavný** a **Rýchle vytvorenie** pre zmluvného zákazníka. | Predstavuje percento každej nevyfakturovanej predajnej transakcie, ktorá sa pripisuje tomuto zmluvnému zákazníkovi. | Skopírované do nových riadkov zmluvy a do zákazníkov v riadkoch projektovej zmluvy na nových riadkoch projektovej zmluvy. |
| **Meno kontaktu platiteľa** | Mriežku je možné upravovať na karte **Zmluvní zákazníci** a vo formulároch **Hlavný** a **Rýchle vytvorenie** pre zmluvného zákazníka. | Toto textové pole by sa malo použiť na identifikáciu kontaktnej osoby faktúry pre zákazníka. Toto pole sa predvolene získava zo záznamu súvisiaceho obchodného vzťahu. | Skopírované do poľa **Fakturovať na názov zmluvy** na faktúre, ktorá sa generuje pre tohto zákazníka. |
| **Fakturačné meno** | Mriežku je možné upravovať na karte **Zmluvní zákazníci** a vo formulároch **Hlavný** a **Rýchle vytvorenie** pre zmluvného zákazníka | Toto textové pole by sa malo použiť na identifikáciu kontaktnej osoby faktúry pre zákazníka. Toto pole sa predvolene získava zo záznamu súvisiaceho obchodného vzťahu. | Skopírované do poľa **Fakturovať na názov zmluvy** na faktúre, ktorá sa generuje pre tohto zákazníka. |
| **Platobné podmienky** | Mriežku je možné upravovať na karte **Zmluvní zákazníci** a vo formulároch **Hlavný** a **Rýchle vytvorenie** pre zmluvného zákazníka. | Hodnoty sa predvolene získavajú zo záznamu súvisiaceho obchodného vzťahu. | Skopírované do poľa **Fakturovať na názov zmluvy** na faktúre, ktorá sa generuje pre tohto zákazníka. |
| **Zaokrúhľuje** | Mriežku je možné upravovať na karte **Zmluvní zákazníci** a vo formulároch **Hlavný** a **Rýchle vytvorenie** pre zmluvného zákazníka. | Označuje, či je tento zákazník predvoleným zákazníkom zaokrúhľovania pre túto dohodu. Na projektovej zmluve môže byť iba jeden zákazník zaokrúhľovania. | Keď rozdelenie nákladov a nefakturovaných predajov na množstvo vedie k rozdielu v zaokrúhľovaní, použije sa tento rozdiel na skutočnú hodnotu, ktorá sa mapuje na tohto zákazníka. |
| **Limit, ktorý sa nesmie prekročiť** | Mriežku je možné upravovať na karte **Zmluvní zákazníci** a vo formulároch **Hlavný** a **Rýchle vytvorenie** pre zmluvného zákazníka | Označuje, či existuje dohodnutý limit alebo strop celkovej sumy, ktorá bude zákazníkovi fakturovaná za túto zákazku. | **Limit, ktorý sa nesmie prekročiť** nastavený na úrovni zmluvného zákazníka sa bude vyhodnocovať na základe **Nefakturovaných skutočných predajov**, ktoré odkazujú na tohto zmluvného zákazníka. |

## <a name="edit-billing-split-percentages"></a>Upraviť percentá rozdelenia fakturácie

Percento rozdelenia fakturácie je možné upravovať pomocou priameho editovania mriežky. Ak percentá rozdelenia fakturácie nedosiahnu 100 percent, zobrazí sa chyba. Po úprave percenta rozdelenia fakturácie chybu odstránite obnovením stránky.

Môžete tiež vybrať **Rovnomerne distribuovať** na podradenej mriežke **Zmluvní zákazníci** a rovnomerne rozdeliť fakturáciu medzi všetkých zmluvných zákazníkov. Ak existuje faktor zaokrúhľovania, pridá sa k zákazníkovi zaokrúhľovania. Jeden zo zmluvných zákazníkov je vždy označený ako zákazník **zaokrúhľovania**, čo znamená, že záznam zmluvného zákazníka bude mať príznak zaokrúhľovania vždy nastavený na **Áno**. Spravidla ide o primárneho zmluvného zákazníka, ale je možné ho tiež zmeniť.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]