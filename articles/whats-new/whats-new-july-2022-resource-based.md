---
title: Novinky v júli 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Tento článok poskytuje informácie o aktualizáciách kvality dostupných vo vydaní Microsoft Dynamics 365 Project Operations Project Operations v júli 2022 pre scenáre založené na zdrojoch/neskladovaných položkách.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403971"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novinky v júli 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.44.0.22
- Projektový manažment a účtovníctvo v prostrední Dynamics 365 Finance, verzia 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

V tomto vydaní nie sú k dispozícii žiadne aktualizácie máp duálneho zápisu Project Operations. Aktuálny zoznam a verzie máp duálneho zápisu Project Operations nájdete na v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../environment/resource-dual-write-maps.md).

Pri aktualizácii riešenia Project Operations Dataverse a verzie riešenia Finance vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí, no zároveň aktivujte všetky mapy príslušnej tabuľky. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spúšťaní mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky v mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v časti Sprievodca riešením problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Nasadenie a konfigurácia | 2761472 | Chyba inštalácie Project Operations je spracovaná. |
| Fakturácia a tvorba cien | 2746940 | Názov riadka subdodávateľskej zmluvy by mal mať maximálnu dĺžku 100 znakov. |
| Fakturácia a tvorba cien | 2739162 | Zákazníci musia mať možnosť vidieť tlačidlá na páse s nástrojmi v zobrazení mriežky skutočných hodnôt. |
| Plánovanie a sledovanie projektu | 2730318 | Aktualizované overenie pre nepodporované znaky v predmete projektu. |
| Fakturácia a tvorba cien | 2705361 | Skutočné fakturované predaje medzníka musia byť zahrnuté v poliach sledovania projektu. |
| Fakturácia a tvorba cien | 2675880 | Zabráňte prepojeniu projektu s riadkom zmluvy, ktorý nie je založená na práci. |
| Fakturácia a tvorba cien | 2664396 | Ak je cenník cenovej ponuky uložený bez cenovej ponuky, musí sa vyskytnúť chyba, ktorá uvádza, že cenová ponuka nemôže byť prázdna. |
| Fakturácia a tvorba cien | 2184019 | Karta **Fakturácia na základe úlohy** by sa nemala zobrazovať pre projekty, ktoré nemajú žiadnu podpornú zmluvu ani cenovú ponuku. |
| Čas a výdavky | 2754459 | Keď je postup v cloude opakovaného plánovania neaktívny, zobrazí sa banner a vynechá sa asynchrónne spracovanie. |
| Fakturácia a tvorba cien | 2724391 | Chybná výnimka sa vyvolá, keď v pravidle rozdelenej fakturácie projektovej zmluvy chýba hodnota zákazníka. |
| Fakturácia a tvorba cien | 2708638 | Záznam sa nenašiel pri vyhľadávaní pomocou mriežkového vyhľadávania v časti Použitie materiálu a Schválenia použitia materiálu.|
| Fakturácia a tvorba cien | 2686977 | Zabráňte overeniu riadku faktúry počas vytvárania faktúry. |
| Fakturácia a tvorba cien | 2683032 | Kopírovanie fakturovateľných rol a kategórií nepresahuje 5000 záznamov.|
| Fakturácia a tvorba cien | 2673363 | Percento spotreby nákladov na projekte je poškodené, keď pre projekt existujú odhady a skutočné hodnoty úsilia aj výdavkov. |

### <a name="project-management-and-accounting-in-finance"></a>Projektový manažment a účtovníctvo vo Finance

Informácie o opravách zahrnutých v tejto aktualizácii nájdete po prihlásení do Microsoft Dynamics Lifecycle Services (LCS) a zobrazení [článku vedomostnej databázy](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcie sú v nadchádzajúcom vydaní predvolene zapnuté

V nasledujúcej tabuľke sú uvedené funkcie, ktoré sú predvolene zapnuté vo verzii 10.0.29. Väčšinu funkcií, ktoré boli automaticky zapnuté, je možné vypnúť v ponuke [Správa funkcií](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). V budúcnosti môžu byť niektoré funkcie, ktoré boli automaticky zapnuté, odstránené zo Správy funkcií a môžu sa stať povinnými. Táto zmena zaisťuje, že zákazníci používajú aktuálne funkcie, takže vylepšenia môžu stavať na aktuálnych funkciách, keď budú pridané. Funkcie nebudú nikdy automaticky aktivované skôr ako za jeden rok, pokiaľ nie sú určené ako nevyhnutné.

| Názov funkcie | Dátum povolenia | Funkcia bola pridaná | Stav funkcie | Modul |
| --- | --- | --- |--- |--- |
| Povolenie úpravy hodinovej transakcie na základe zmeny prideľovania pravidla financovania | 16. september 2022 | 7. októbra 2020 | Štandardne zapnuté | Projektový manažment a účtovníctvo |
| Funkcia stornovania zálohovej faktúry nákupnej objednávky projektu | 16. september 2022 | 6. októbra 2021 | Štandardne zapnuté | Projektový manažment a účtovníctvo |
| Odstránenie riadkov návrhu faktúry pri používaní Project Operations pre scenáre zložené na zdrojoch/neskladovaných položkách | 16. september 2022 | 6. októbra 2021 | Štandardne zapnuté | Projektový manažment a účtovníctvo |
| Úprava účtovania zaúčtovanej transakcie projektu | 16. september 2022 | 10. mája 2020 | Štandardne zapnuté | Projektový manažment a účtovníctvo |
| Povolenie predvoleného nastavenia účtovania pre projekt | 16. september 2022 | 19. február 2020 | Štandardne zapnuté | Projektový manažment a účtovníctvo |
| Povoliť pre projekt viac riadkov zmluvy | 16. september 2022 | 29. júna 2020 | Štandardne zapnuté | Projektový manažment a účtovníctvo |
| Nastavenie denníkov hodín projektu na čítanie, ak aktuálny stav schválenia neumožňuje úpravy | 16. september 2022 | 6. októbra 2021 | Štandardne zapnuté | Projektový manažment a účtovníctvo |
| Povolenie synchronizácie predajných riadkov z nákupných riadkov, keď sa aktualizujú nákupné riadky a je zapnutý parameter správy zmien nákupných objednávok | 16. september 2022 | 7. októbra 2020 | Štandardne zapnuté | Projektový manažment a účtovníctvo |
| Povolenie Project Operations v Dynamics 365 Customer Engagement | 16. september 2022 | 29. júna 2020 | Štandardne zapnuté | Projektový manažment a účtovníctvo |
| Funkcia korekcie storna transakcie projektu | 16. september 2022 | 13. júl 2020 | Štandardne zapnuté | Projektový manažment a účtovníctvo |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funkcie, ktoré sa stanú povinnými v nadchádzajúcom vydaní

V nasledujúcej tabuľke sú uvedené funkcie, ktoré sú povinné od verzie 10.0.29.

| Názov funkcie | Dátum povolenia | Funkcia bola pridaná | Stav funkcie | Modul |
| --- | --- | --- | --- | --- |
| Výpočet viazanej hodnoty zdroja financovania bez zaokrúhlenia výmenného kurzu | 16. september 2022 | 14. júna 2020 | Povinné | Projektový manažment a účtovníctvo |
| Povolenie účtovania úpravy projektu s rovnakým účtom registra ako pôvodná transakcia | 16. september 2022 | 14. júna 2020 | Povinné | Projektový manažment a účtovníctvo |
| Detail viazanej sumy projektovej zmluvy | 16. september 2022 | 31. august 2019 | Povinné | Projektový manažment a účtovníctvo |
| Povolenie triedenia podľa zdroja počas vytvárania návrhu projektovej faktúry | 16. september 2022 | 31. august 2019 | Povinné | Projektový manažment a účtovníctvo |
