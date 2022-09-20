---
title: Prepisy cien platné od dátumu
description: Tento článok vysvetľuje, ako nastaviť prepísanie cien pre konkrétne ceny v cenníku.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446011"
---
# <a name="date-effective-price-overrides"></a>Prepisy cien platné od dátumu 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

*Prepisy cien platné od dátumu* poskytnúť spôsob, ako prepísať alebo zmeniť konkrétne ceny v cenníku. Napríklad máte štandardný cenník platný od 1. januára 2022 do 31. decembra 2022. Tento cenník obsahuje ceny pre mnoho rolí. Cena, ktorá je nastavená pre **Sieťový technik** role je 100 amerických dolárov (USD) za hodinu. Keď sieťový technik zaznamená čas medzi 1. januárom 2022 a 31. decembrom 2022, cena za čas je 100 USD. 1. októbra 2022 musíte upraviť cenu *iba* pre **Sieťový technik** rolu, od 100 USD za hodinu do 110 USD za hodinu. The **Dátum platnosti prepísania cien** funkcia vám umožňuje nastaviť túto zmenu ako prepísanie riadka pre konkrétnu cenu role. Nemusíte teda kopírovať celý cenník a meniť cenu len toho jedného riadku.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Prepisy cien práce platné od dátumu

Proces nastavenia dátumovo efektívnych prepisov cien pre pracovný čas na projekte pozostáva z dvoch základných krokov.

1. Povoliť **Dátum platnosti prepísania cien** vlastnosť.
1. Nastavte prepísanie ceny platné od dátumu.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Povoľte funkciu prepísania cien podľa dátumu platnosti

> [!NOTE]
> Po **Dátum platnosti prepísania cien** funkcia je povolená, nemožno ju vypnúť.

Ak chcete povoliť **Prepisy cien platné od dátumu** funkciu, postupujte podľa týchto krokov.

1. Ísť do **nastavenie** \> **Parametre**.
1. Otvor **Parametre** záznam.
1. Na paneli akcií na **Ovládanie funkcií** kartu, vyberte **Povoliť prepisy cien platné od dátumu**.
1. V dialógovom okne potvrdenia kliknite na tlačidlo **OK**.
1. Po chvíli obnovte prehliadač. Teraz by mali byť k dispozícii možnosti prepisovania cien v závislosti od dátumu. Budete vedieť, že tieto možnosti boli povolené, ak **Povoliť prepisy cien platné od dátumu** sa už nezobrazuje na paneli akcií.

### <a name="set-up-a-date-effective-price-override"></a>Nastavte prepísanie ceny platné od dátumu

Dátumovo platné prepisy cien je možné nastaviť **náklady**, **·**, alebo **Nákup** cenníky.

> [!NOTE]
>Správanie sa **Dátum platnosti prepísania cien** má v súčasnosti nasledujúce obmedzenia:
>
> - Podporujú iba ceny rolí a prirážky cien rolí **Dátum platnosti prepísania cien** funkcie v Project Operations.
> - Pri kopírovaní cenníka pomocou **Kopírovať** akcia na **Podrobnosti cenníka** a keď vytvoríte projektový cenník zo štandardného alebo vlastného cenníka počas vytvárania zmluvy, dátumovo účinné prepísania cien sú **nie** skopírované zo zdrojového cenníka.

Ak chcete nastaviť prepísanie ceny s platnou dátumom pre cenu role alebo prirážku ceny role, postupujte podľa týchto krokov.

1. Otvorte stránku pre cenník, pre ktorý chcete nastaviť prepísanie ceny platné od dátumu.
1. Vyberte **Ceny rolí** tab. Táto karta obsahuje zoznam všetkých **Cena role** záznamy v cenníku.
1. Vyberte **Cena role** zaznamenajte, pre ktoré chcete nastaviť novú prepisovaciu cenu platnú pre dátum, a potom dvakrát ťuknite (alebo dvakrát kliknite) **Cena role** otvoriť **Podrobnosti o cene role** stránku.
1. Vyberte **Dátum účinnosti prepíše** tab. V mriežke na tejto karte sú uvedené všetky dátumy platné prepísania cien pre vybraté položky **Cena role** záznam.
1. Na paneli s nástrojmi nad mriežkou vyberte **Nová rola prepíše cenu**. The **Nová rola prepíše cenu** posúvač sa otvorí.
1. Zadajte dátum účinnosti, jednotku a novú cenu pre prepísanie ceny. Potom vyberte **Uložiť** a zatvorte formulár.

> [!NOTE]
> - Prepísanie ceny roly alebo prirážky ceny roly platné od dátumu je použiteľné pre rovnakú kombináciu hodnôt cenovej dimenzie, ktorá existuje na nadradenom **Cena role** alebo **Prirážka ceny role** riadok.
> - Dátum, ktorý je vybraný v **Účinné od** pole by malo byť v rámci dátumov účinnosti nadradeného cenníka. Prepísanie ceny nadobudne účinnosť v deň, ktorý je vybraný v **Účinné od** pole a bude platiť do konca dátumu ukončenia nadradeného cenníka. Ak nastavíte iné prepísanie ceny platného dátumu pre rovnakú cenu role, prvé prepísanie ceny nadobudne účinnosť v dátum, ktorý je vybratý v **Účinné od** a bude platiť až do začiatku druhého prepísania.

## <a name="examples"></a>Príklady

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Príklad 1: Určenie účinnosti dátumu pre cenu roly, ktorá má prednosť pred cenou roly

Nasledujúci príklad ukazuje, ako sa určuje účinnosť dátumu pre konkrétnu cenu roly, pre ktorú sú nastavené prepisy cien roly.

**Cenník A: od 1. januára do 30. júna**

*Cena role*

| Cena role | Jednotka | Cena | Vplyv na ceny prichádzajúcich transakcií |
|---|---|---|---|
| Sieťový technik | Hodina | 100 | Táto cena sa použije pri všetkých transakciách, ktorých dátum transakcie je medzi 1. januárom a 14. marcom. |

*Prepísanie ceny role*

| Účinné od | Jednotka | Cena | Vplyv na ceny prichádzajúcich transakcií |
|---|---|---|---|
| Marec 15 | Hodina | 110 | Táto cena sa použije pri všetkých transakciách, ktorých dátum transakcie je medzi 15. marcom a 30. marcom. |
| Apríl 1 | Hodina | 120 | Táto cena sa použije pri všetkých transakciách, ktorých dátum transakcie je medzi 1. aprílom a 30. júnom. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Príklad 2: Určenie účinnosti dátumu pre cenovú prirážku role, ktorá má prepísanie prirážky ceny roly

Nasledujúci príklad ukazuje, ako sa určuje účinnosť dátumu pre konkrétnu prirážku ceny role, pre ktorú sú nastavené prepísania prirážky ceny role.

**Cenník A: od 1. januára do 30. júna**

*Cena role*

| Cena role | Pracovný čas | Jednotka | Cena | Vplyv na ceny prichádzajúcich transakcií |
|---|---|---|---|---|
| Sieťový technik | Pravidelné | Hodina | 100 | Táto cena sa použije pri všetkých transakciách, ktorých dátum transakcie je medzi 1. januárom a 14. marcom. |

*Prirážka ceny role*

| Organizačná jednotka | Pracovný čas | Priznať % |
|---|---|---|
| Contoso US | Nadčas | 10 % |

*Prepísanie prirážky ceny role*

| Účinné od | Cena | Vplyv na ceny prichádzajúcich transakcií |
|---|---|---|
| Marec 15 | 20 % | Toto percento prirážky sa použije pri všetkých transakciách, ktorých dátum transakcie je medzi 15. marcom a 30. marcom. |
| Apríl 1 | 25 % | Táto prirážka sa použije pri všetkých transakciách, ktorých dátum transakcie je medzi 1. aprílom a 30. júnom. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
