---
title: Nastavenie cenníkov
description: Tento článok poskytuje informácie o tom, ako nastaviť cenníky nákladov a predaja.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8a6d96f4a5a8d97e86bbd00413e21f69255a48c5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917687"
---
# <a name="set-up-price-lists"></a>Nastavenie cenníkov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Cenníky v Dynamics 365 Project Operations predstavujú katalóg sadzieb. Ceny vyjadrujú náklady, predaj a fakturačné sadzby. V závislosti od toho, či cenník vyjadruje nákladové sadzby alebo predajné a fakturačné sadzby, je kontext cenníka **Predaj** alebo **Náklady**.

Nasledujúce rozšírenia sú špecifické pre Project Operations a sú aplikované na cenníky z Dynamics 365 Sales.

- **Kontext**: Toto pole má podporované hodnoty, **Náklady** a **Predaj**. Hodnota **Nákup** nie je podporovaná. Nastavte kontext na **Náklady** a vytvorte cenník nákladov alebo nastavte kontext na **Predaj** pre predajný cenník. Cenníky nákladov určujú cenu pre typ nákladov v záznamoch o odhadoch a skutočných hodnotách. Cenníky predajných cien riešia cenu na základe odhadovaných a skutočných záznamov o fakturovaných a fakturovaných typoch predaja.
- **Časová jednotka** : Toto je predvolená časová jednotka, pre ktorú je cena nastavená v príslušnej tabuľke **Cena roly** pre tento cenník.
- **Entita cenníka**: Toto skryté pole je v časti Project Operations určené na odlíšenie cenových ponúk, ktoré sú špecifické pre danú ponuku alebo zmluvu, od tých, ktoré sú štandardné a globálne použiteľné.

## <a name="price-list-header"></a>Hlavička cenníka

Nasledujúca tabuľka obsahuje polia na karte **Všeobecné**, ktorá je jedinečná pre Project Operations alebo má významné zmeny v správaní z cenníkov v Sales.

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| Meno | Karta **Všeobecné** a formuláre **Rýchle vytvorenie** | Identita cenníka. | Cenník zobrazuje túto hodnotu na všetkých stránkach so zoznamami a v rozbaľovacích možnostiach.|
| Kontext | Karta **Všeobecné** a formuláre **Rýchle vytvorenie** | Toto pole je možné nastaviť na **Náklady** alebo **Predaj**. | Cenník s kontextom nastaveným na **Náklady** sa používa na vyhľadanie ceny odhadov nákladov a skutočných nákladov. Cenník s kontextom nastaveným na **Predaj** sa používa na vyhľadanie ceny odhadov predaja a skutočných predajov. Iba cenníky, ktoré majú nastavený kontext na **Predaj** môžu byť pripojené k cenníkom pre zákazníkov, cenové ponuky projektu a projektové zmluvy. |
| Počiatočný dátum | Karta **Všeobecné** a formuláre **Rýchle vytvorenie** | Počiatočný dátum obdobia, v ktorom je cenník platný. | Toto pole sa spolu s poľom **Dátum ukončenia** používa na určenie, ktorý cenník je použiteľný pre určitý odhad alebo riadok skutočnej hodnoty. |
| Konečný dátum | Karta **Všeobecné** a formuláre **Rýchle vytvorenie** | Konečný dátum obdobia, v ktorom je cenník platný. | Toto pole sa spolu s poľom **Dátum začiatku** používa na určenie, ktorý cenník je použiteľný pre určitý odhad alebo riadok skutočnej hodnoty. |
| Mena | Karta **Všeobecné** a formuláre **Rýchle vytvorenie** | Toto pole sa používa na predvolenú menu v každom riadku položky, kategórie alebo cenníka súvisiaceho s týmto cenníkom. | V cenníkoch **Predaj**, roly, kategórie alebo riadky položiek cenníka nemožno vytvoriť v inej mene, ako je táto mena. V cenníkoch **Náklady**, môžete vytvoriť cenový riadok role v akejkoľvek mene. Tu definovaná mena sa používa ako predvolená. Používateľské nastavenie, ktoré súvisí s cenami rolí, môže túto hodnotu prepísať, aby umožnilo nastavenie sadzby nákladov práce v akejkoľvek mene. Sadzby ceny kategórie a náklady položky cenníka je možné nastaviť iba v tu definovanej mene. |
| Jednotka času | Karta **Všeobecné** a formuláre **Rýchle vytvorenie** | Toto pole sa používa na predvolenie časovej jednotky v každom riadku položky súvisiacej s týmto cenníkom. | Hodnota tohto poľa sa používa iba pri nastavení ceny súvisiacej roly. V cenníkoch **Náklady** a **Predaj**, môžete vytvoriť cenový riadok role v akejkoľvek časovej jednotke. Tu definovaná časová jednotka sa používa ako predvolená. Používateľské nastavenie, ktoré súvisí s cenami rolí, môže túto hodnotu prepísať, aby umožnilo nastavenie sadzby nákladov práce a sadzby fakturácie v akejkoľvek časovej jednotke. |
| Popis | Karta **Všeobecné** a formuláre **Rýchle vytvorenie** | Toto je textové pole a umožňuje použiť viacriadkový popis cenníka. | Toto pole sa zobrazuje v zobrazeniach **Priradené** pre cenník v rôznych entitách, ktoré majú súvisiace cenníky. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]