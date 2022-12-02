---
title: Prepísania cien s dátumom účinnosti
description: Tento článok vysvetľuje, ako nastaviť prepísania cien pre konkrétne ceny v cenníku.
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
# <a name="date-effective-price-overrides"></a>Prepísania cien s dátumom účinnosti 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

*Prepísania cien s dátumom účinnosti* poskytuje spôsob, ako prepísať alebo zmeniť konkrétne ceny v cenníku. Napríklad máte štandardný cenník platný, ktorý platí od 1. januára 2022 do 31. decembra 2022. Tento cenník obsahuje ceny pre mnoho rolí. Cena, ktorá je nastavená pre rolu **Sieťový technik**, je 100 amerických dolárov (USD) za hodinu. Keď sieťový technik zaznamená čas medzi 1. januárom 2022 a 31. decembrom 2022, cena za čas je 100 USD. 1. októbra 2022 musíte upraviť cenu *iba* pre rolu **Sieťový technik**, zo 100 USD za hodinu na 110 USD za hodinu. Funkcia **Prepísania cien s dátumom účinnosti** vám umožňuje nastaviť túto zmenu ako prepísanie riadka pre cenu konkrétnej roly. Nemusíte teda kopírovať celý cenník a meniť cenu len toho jedného riadka.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Prepísanie cien s dátumom účinnosti pre cenu práce

Proces nastavenia prepísania cien s dátumom účinnosti pre čas práce na projekte pozostáva z dvoch základných krokov.

1. Povoľte funkciu **Prepísania cien s dátumom účinnosti**.
1. Nastavte prepísanie cien s dátumom účinnosti.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Povolenie funkcie Prepísania cien s dátumom účinnosti

> [!NOTE]
> Po povolení funkcie **Prepísania cien s dátumom účinnosti** ju už nemožno vypnúť.

Ak chcete povoliť funkciu **Prepísania cien s dátumom účinnosti**, postupujte podľa týchto krokov.

1. Prejdite do časti **Nastavenia** \> **Parametre**.
1. Otvorte záznam **Parametre**.
1. Na table akcií na karte **Ovládací prvok funkcie** vyberte **Povoliť prepísania cien s dátumom účinnosti**.
1. V dialógovom okne potvrdenia kliknite na tlačidlo **OK**.
1. Po chvíli obnovte prehliadač. Teraz by mali byť k dispozícii možnosti prepísania cien s dátumom účinnosti. Budete vedieť, že tieto možnosti boli povolené, ak sa na table Akcia viac nebude zobrazovať možnosť **Povoliť prepísania cien s dátumom účinnosti**.

### <a name="set-up-a-date-effective-price-override"></a>Nastavenie prepísania cien s dátumom účinnosti

Prepísania cien s dátumom účinnosti je možné nastaviť v cenníkoch **Náklady**, **Predaj** alebo **Nákup**.

> [!NOTE]
>Správanie sa funkcie **Prepísania cien s dátumom účinnosti** má v súčasnosti nasledujúce obmedzenia:
>
> - Funkciu **Prepísania cien s dátumom účinnosti** v Project Operations podporujú iba ceny rolí a prirážky k cenám rolí.
> - Pri kopírovaní cenníka pomocou akcie **Kopírovať** na stránke **Podrobnosti cenníka**, a keď vytvoríte projektový cenník zo štandardného alebo vlastného cenníka počas vytvárania zmluvy, prepísania cien s dátumom účinnosti sa **neskopírujú** zo zdrojového cenníka.

Ak chcete nastaviť prepísania cien s dátumom účinnosti pre cenu roly alebo prirážky k cene roly, postupujte podľa týchto krokov.

1. Otvorte stránku pre cenník, pre ktorý chcete nastaviť prepísania cien s dátumom účinnosti.
1. Vyberte kartu **Ceny rolí**. Táto karta obsahuje zoznam všetkých záznamov **Cena roly** v cenníku.
1. Vyberte záznam **Cena roly**, pre ktorý chcete nastaviť novú prepísanú cenu s dátumom účinnosti, a potom dvakrát ťuknite (alebo dvakrát kliknite) na položku **Cena roly**, čím otvoríte stránku **Podrobnosti o cene roly**.
1. Vyberte kartu **Prepísania s dátumom účinnosti**. V mriežke na tejto karte sú uvedené všetky prepísania cien s dátumom účinnosti pre vybratý záznam **Cena roly**.
1. Na paneli s nástrojmi nad mriežkou vyberte **Nové prepísanie ceny roly**. Otvorí sa jazdec **Nové prepísanie ceny roly**.
1. Zadajte dátum účinnosti, jednotku a novú cenu pre prepísanie ceny. Následne vyberte položku **Uložiť** a zatvorte formulár.

> [!NOTE]
> - Prepísanie ceny s dátumom účinnosti pre cenu roly alebo prirážku k cene roly je použiteľné pre rovnakú kombináciu hodnôt cenovej dimenzie, ktorá existuje v nadradenom riadku **Cena roly** alebo **Prirážka k cene roly**.
> - Dátum, ktorý je vybraný v poli **Platnosť od** by mal byť v rámci dátumov platnosti nadradeného cenníka. Prepísanie ceny nadobudne účinnosť v deň, ktorý je vybraný v poli **Platnosť od** a bude platiť do konca dátumu ukončenia nadradeného cenníka. Ak nastavíte iné prepísanie ceny s dátumom účinnosti pre rovnakú cenu roly, prvé prepísanie ceny nadobudne účinnosť v dátum, ktorý je vybratý v poli **Platnosť od** a bude platiť až do začiatku druhého prepísania.

## <a name="examples"></a>Príklady

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Príklad 1: Určenie dátumu účinnosti pre cenu roly, ktorý má prednosť pred cenou roly

Nasledujúci príklad ukazuje, ako sa určuje dátumu účinnosti pre konkrétnu cenu roly, pre ktorú sú nastavené prepísania cien roly.

**Cenník A: od 1. januára do 30. júna**

*Cena roly*

| Cena roly | Jednotka | Cena | Vplyv na ceny prichádzajúcich transakcií |
|---|---|---|---|
| Sieťový technik | Hodina | 100 | Táto cena sa použije pri všetkých transakciách, pri ktorých je dátum transakcie medzi 1. januárom a 14. marcom. |

*Prepísanie ceny roly*

| Účinnosť od | Jednotka | Cena | Vplyv na ceny prichádzajúcich transakcií |
|---|---|---|---|
| Marec 15 | Hodina | 110 | Táto cena sa použije pri všetkých transakciách, pri ktorých je dátum transakcie medzi 15. marcom a 30. marcom. |
| Apríl 1 | Hodina | 120 | Táto cena sa použije pri všetkých transakciách, pri ktorých je dátum transakcie medzi 1. aprílom a 30. júnom. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Príklad 2: Určenie dátumu účinnosti pre prirážku k cene roly, ktorý má prednosť pred prirážkou k cene roly

Nasledujúci príklad ukazuje, ako sa určuje dátumu účinnosti pre konkrétnu prirážku k cene roly, pre ktorú sú nastavené prepísania prirážky k cene roly.

**Cenník A: od 1. januára do 30. júna**

*Cena roly*

| Cena roly | Pracovný čas | Jednotka | Cena | Vplyv na ceny prichádzajúcich transakcií |
|---|---|---|---|---|
| Sieťový technik | Normálny | Hodina | 100 | Táto cena sa použije pri všetkých transakciách, pri ktorých je dátum transakcie medzi 1. januárom a 14. marcom. |

*Prirážka k cene roly*

| Organizačná jednotka | Pracovný čas | Prirážka % |
|---|---|---|
| Contoso US | Nadčas | 10 % |

*Prepísanie prirážky k cene roly*

| Účinnosť od | Cena | Vplyv na ceny prichádzajúcich transakcií |
|---|---|---|
| Marec 15 | 20 % | Táto percentuálna prirážka sa použije pri všetkých transakciách, pri ktorých je dátum transakcie medzi 15. marcom a 30. marcom. |
| Apríl 1 | 25 % | Táto prirážka sa použije pri všetkých transakciách, pri ktorých je dátum transakcie medzi 1. aprílom a 30. júnom. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
