---
title: Vytvorenie medzipodnikových transakcií
description: Táto téma poskytuje informácie o tom, ako vytvárať medzipodnikové transakcie.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d23e45d99be61e93d98a8377ff5fa05b3febb6b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287437"
---
# <a name="create-intercompany-transactions"></a>Vytvorenie medzipodnikových transakcií

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Medzipodnikové transakcie sú časové a nákladové transakcie z projektovej zmluvy, ktoré patria jednej spoločnosti alebo organizačnej jednotke, zatiaľ čo zdroje projektovej zmluvy sú súčasťou inej spoločnosti alebo organizačnej jednotky.

Po schválení medzipodnikovej transakcie sa vytvoria nasledujúce skutočné transakcie

| **Typ transakcie** | **Použitý cenník** | **Mena transakcie** |
| --- | --- | --- |
| Náklady | Cenník obstarávacej ceny zmluvnej jednotky | Mena na riadku s cenou |
| Nefakturovaný predaj. Vytvoria sa iba pre skutočné hodnoty, ktoré sú spojené s riadkom zmluvy s typom fakturácie, časom a materiálom. | Projektový predajný cenník zmluvy | Mena projektu |
| Náklady zdrojovej jednotky | Cenní obstarávacích cien zdrojovej jednotky | Mena na riadku s cenou |
| Predaj medziorganizačných jednotiek | Cenník obstarávacej ceny zmluvnej jednotky | Mena na riadku s cenou |

Náklady, zdrojové jednotkové ceny a nacenenie predajných transakcií medziorganizačných jednotiek a mena závisia od **organizačnej jednotky**. Toto je dôležité mať na pamäti pri rozhodovaní o tom, ako štrukturalizovať spoločnosti a organizačné jednotky vo vašej implementácii.

Keď vytvoríte príležitosť, cenovú ponuku, projektovú zmluvu a záznamy o projekte, systém overí, či sa mena zmluvnej jednotky zhoduje s účtovnou menou zmluvnej spoločnosti. Ak nie sú rovnaké, tieto záznamy nemožno vytvoriť. Mena organizačnej jednotky je definovaná v Dynamics 365 Project Operations, v ponuke **Dataverse** > **Nastavenia** > **Organizačné jednotky**. Účtovná mena spoločnosti je definovaná v Dynamics 365 Finance v ponuke **Hlavná účtovná kniha** > **Nastavenie účtovnej knihy** > **Účtovná kniha**. Mena sa synchronizuje s vaším prostredím Dataverse pomocou mapovania Ledgers Dual Write.

Systém vytvára jednotkové náklady na zdroje a skutočný predaj medziorganizačných jednotiek v nasledujúcich situáciách:

  - Keď sa zdrojová jednotka líši od zmluvnej jednotky
  - Keď sa zdrojová spoločnosť líši od zmluvnej spoločnosti

Do prostredia Dynamics 365 Finance však budú pre ďalšie účtovanie prevedené iba transakcie, ktoré majú inú zdrojovú spoločnosť než zmluvnú spoločnosť.

Účtovanie skutočných hodnôt projektu sa zaznamenáva v denníku integrácie Project Operations vo Finance. Systém vytvorí nasledujúce záznamy v účtovnom denníku.

| **Typ transakcie** | **Právnická osoba** | **Vytvorí projektovú transakciu pri zaúčtovaní** | **Predvolený formulár finančných dimenzií** | **Predvolená skupina dane z fakturovaného predaja a skupina dane z fakturovaného predaja položky** |
| --- | --- | --- | --- | --- |
| Náklady | Nedá sa pridať do integračného denníka | Nie je k dispozícii | Nie je k dispozícii | Nie je k dispozícii |
| Nefakturovaný predaj | Integračný denník požičiavajúcej si právnickej osoby | Áno | Project | **Skupina dane z fakturovaného predaja**: Založená na **zmluvnom zákazníkovi** <br/> **Skupina dane z fakturovaného predaja položky**: Z aktuálnej kategórie projektov právnických osôb v zázname v účtovnom denníku |
| Náklady zdrojovej jednotky | Integračný denník prenajímajúcej právnickej osoby | No | Medzipodnikový zákazník | **Skupina dane z fakturovaného predaja**: Založená na **medzipodnikovom zákazníkovi** <br/> **Skupina dane z fakturovaného predaja položky**: Z aktuálnej kategórie projektov právnických osôb v zázname v účtovnom denníku |
| Medzipodnikové predaje | Integračný denník prenajímajúcej právnickej osoby | No | Medzipodnikový zákazník | **Skupina dane z fakturovaného predaja**: Založená na **medzipodnikovom zákazníkovi** <br/> **Skupina dane z fakturovaného predaja položky**: Z aktuálnej kategórie projektov právnických osôb v zázname v účtovnom denníku |

### <a name="example-intercompany-transactions"></a>Príklad: Medzipodnikové transakcie

Molly Clarková, vývojárka zamestnaná v GBPM, zaznamenáva 10 hodín práce na projekte USPM Adventure Works, ktorý schvaľuje vedúci projektu. Cena vývojára v GBPM je 88 GBP za hodinu. GBPM bude fakturovať USPM 120 USD za hodinu vývojára. USPM bude zákazníkovi Adventure Works fakturovať 200 USD za prácu vykonanú zdrojom GBPM. Ďalšie informácie nájdete v téme [Konfigurácia medzipodnikovej fakturácie](configure-intercompany-invoicing.md).

1. V časti Project Operations prejdite na **Zdroje** a vyberte **Molly Clarková** zo zoznamu. Na karte **Plánovanie** v poli **Spoločnosť** vyberte položku **GBPM**.
2. Prejdite do **Predaj** > **Zákazníci** a vyberte **Nový** na vytvorenie nového záznamu zákazníka pre Adventure Works.
    1. Nastavte spoločnosť **USPM**.
    2. Nastavte **Typ vzťahu** na **Zákazník**.
    3. Vyberte **Skupina zákazníkov 10 – domáci**.
    4. Nastavte menu na **USD**.
    5. Uložte záznam.
3. Prejdite na **Predaj** > **Projektové zmluvy** a vytvorte novú projektovú zmluvu pre Adventure Works.
    1. Nastavte vlastniacu spoločnosť na **USPM** a zmluvnú jednotka ma **Contoso Robotics US**.
    2. Vyberte Adventure Works ako zákazníka.
    3. Vyberte cenník produktu a uložte záznam.
    4. Na karte **Riadky zmluvy** vytvorte nový riadok zmluvy. Nastavte ľubovoľný názov a vyberte **Čas a materiály** ako spôsob účtovania.
    5. Vytvorte nový projekt a spojte ho s týmto riadkom zmluvy.
4. Prihláste sa ako zdroj, **Molly Clarková**. Prejdite na **Projekty** > **Zadanie času** a vytvorte časový údaj pre projekt Adventure Works.
5. Prihláste sa ako projektový manažér. Prejdite do **Projekty** > **Schválenia** a schváľte časovú transakciu zaznamenanú Molly Clarkovou.
6. Prejdite na projekt Adventure Works a vyberte **Súvisiace** > **Skutočnosti**. Vytvoria sa nasledujúce transakcie skutočností.

| **Typ transakcie** | **Cena** | **Mena transakcie** | **Suma** |
| --- | --- | --- | --- |
| Náklady | 120 | USD | 1200 |
| Nefakturovaný predaj | 200 | USD | 2000 |
| Náklady zdrojovej jednotky | 88 | GBP | 880 |
| Predaj medziorganizačných jednotiek | 120 | USD | 1200 |

7. Prihláste sa ako účtovník USPM. Otvorte inštanciu Finance aplikácie Project Operations a vyberte spoločnosť **USPM**. 
8. Prejdite na **Projektové riadenie a účtovníctvo** > **Periodické** > **Project Operations v Customer Engagement** > **Import z pracovnej verzie** a vyberte na spustenie pravidelného procesu. Tento pravidelný proces vyplní integračný denník Project Operations.
9. Prejdite do **Projektové riadenie a účtovníctvo** > **Denníky** > **Integračný denník Project Operations** a skontrolujte riadky denníka. Systém vytvorí nasledujúci riadok.

    | **Typ transakcie** | **Cena** | **Mena transakcie** | **Suma** |
    | --- | --- | --- | --- |
    | Nefakturovaný predaj | 200 | USD | 2000 |

    Ak je systém nastavený na zhromažďovanie výnosov z tohto projektu, zaúčtuje sa toto:

    - Debet: Projekt – hodnota predaja WIP 200 USD
    - Kredit: Projekt – Získané príjmy 200 USD

    Tento nevyfakturovaný predaj je teraz pripravený na fakturáciu. Faktúru pre zákazníka Adventure Works možno v prípade potreby finančne zaúčtovať.

10. Prihláste sa ako účtovník **GBPM**. Otvorte inštanciu Finance aplikácie Project Operations a otvorte spoločnosť **GBPM**. 
11. Prejdite na **Projektové riadenie a účtovníctvo** > **Periodické** > **Project Operations v Customer Engagement** > **Import z pracovnej verzie** a spustite pravidelný proces na vyplnenie denníku integrácie v Project Operations.
12. Prejdite do **Projektové riadenie a účtovníctvo** > **Denníky** > **Integračný denník Project Operations** a skontrolujte riadky. Systém vytvorí nasledujúce riadky.

    | **Typ transakcie** | **Cena** | **Mena transakcie** | **Suma** |
    | --- | --- | --- | --- |
    | Náklady zdrojovej jednotky | 88 | GBP | 880 |
    | Predaj medziorganizačných jednotiek | 120 | USD | 1200 |

    Výsledkom zaúčtovania týchto záznamov sú nasledujúce poukážkové transakcie:

    - Debet: Náklady na projekt 88 GBP
    - Kredit: Alokácia miezd 88 GBP

    Ak je systém nastavený na zhromažďovanie medzipodnikových výnosov, zaúčtuje sa toto:

    - Debet: Projekt – hodnota predaja WIP 120 USD
    - Kredit: Projekt – Získané príjmy 120 USD

    Systém je teraz pripravený na vytvorenie medzipodnikovej faktúry pre zákazníka.


[!INCLUDE[footer-include](../includes/footer-banner.md)]