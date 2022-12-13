---
title: Úpravy projektu
description: Tento článok poskytuje informácie o úpravách projektu.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788375"
---
# <a name="project-adjustments"></a>Úpravy projektu

_**Vzťahuje sa na:** Project Operations pre scenáre založené na zdrojoch/výrobe_

## <a name="adjustments-overview"></a>Prehľad úprav

Microsoft Dynamics 365 Project Operations  môžete nakonfigurovať tak, aby používatelia mohli vykonávať zmeny v zaúčtovaných transakciách. Transakcie projektu môžete upraviť jednotlivo alebo môžete vybrať viacero transakcií naraz v zozname všetkých transakcií projektu. Úpravy projektu sa používajú napríklad na hromadnú aktualizáciu fakturovateľného stavu, prepočítanie nákladov po zmene konfigurácie alebo aktualizáciu zdrojov financovania.

Používatelia môžu pristupovať k funkcii úpravy projektu niekoľkými spôsobmi:

- Pomocou stránky  **Upraviť transakcie**, na ktorú sa dostanete z  **Projektového manažmentu a účtovníctva** \> **Nastavenie**.
- Pomocou tlačidla **Úprava** na stránke **Zaúčtované transakcie projektu** dostupné z **Projektový manažment a účtovníctvo** \> **Transakcie**.
- Pomocou tlačidla **Úprava** na stránke **Zaúčtované transakcie projektu** v kontexte projektu. Táto stránka je prístupná z **Projektový manažment a účtovníctvo** \> **Všetky projekty**.

Ak chcete povoliť úpravy, musíte povoliť jeden alebo viac stavov transakcie z **Projektový manažment a účtovníctvo** \> **Projektový manažment a účtovné parametre** na **Všeobecné** v sekcii **Povoliť úpravu stavu transakcie**. Príklady stavov transakcií zahŕňajú zaúčtované transakcie, fakturované transakcie alebo eliminované transakcie. Každý stav transakcie, ktorý je nastavený na **Nie**, bude mať transakcie v tomto stave, ktoré sa v procese úpravy nezobrazia ako voliteľné na úpravu.

Možnosť konfigurácie s názvom **Vždy vytvoriť transakciu úpravy**  je momentálne dostupná v časti Správa projektu a parametre účtovania. Túto možnosť môžete vypnúť, ak chcete aktualizovať pôvodnú transakciu namiesto vytvárania nových transakcií počas úpravy v podmnožine scenárov. Bolo oznámené, že podpora tohto parametra bude ukončená do 1. marca 2023. Po 1. marci 2023 sa bude systém vždy správať, ako keby bola táto možnosť povolená.

## <a name="adjustments-process-flow"></a>Priebeh procesu úprav

Nasledujúce kroky ukazujú typický postup úprav spracovania.

1. Otvorte stránku **Úpravy projektu** .
2. Vyberte **Vybrať** pre vyhľadanie transakcií, ktoré spĺňajú očakávané kritériá na úpravu.
3. V zozname transakcií vyberte všetky transakcie alebo podmnožinu transakcií na úpravu.
4. Vyberte **Upraviť** a upravte atribúty na riadku. Prípadne, ak boli hodnoty zadané manuálne počas zadávania transakcie, môžete zvoliť zadanie predvolených systémových hodnôt.
5. Vráti sa zoznam transakcií a v stĺpci **Čaká úprava**  sa zobrazí značka začiarknutia, ktorá označuje, kde boli vykonané zmeny. Všetky úpravy, ktoré majú čakajúce zmeny, sú zobrazené v dolnej polovici stránky. Tam môžete vykonať ďalšie podrobné zmeny nad rámec toho, čo bolo zobrazené na predchádzajúcej stránke.
6. Výberom možnosti **Zaúčtovať**  zaúčtujete transakcie úprav.

V závislosti od konfigurácie sa zvyčajne vytvárajú nové transakcie na úpravu.

- Pole **Stav faktúry**  pôvodnej transakcie je nastavené na **Upravené**.
- Na stornovanie pôvodnej transakcie sa vytvorí stornovacia transakcia a pole **Stav**  je nastavené na  **Upravené**.
- Vytvorí sa nová transakcia so zmenami, ktoré boli vykonané počas procesu úpravy.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Výber viacerých zaúčtovaných transakcií projektu naraz pre úpravy a dobropisy

Nová funkcia, ktorá bola predstavená vo verzii 10.0.30, umožňuje výber viacerých transakcií na úpravu naraz na stránke **Zaúčtované transakcie projektu** .

Predtým, ako budete môcť túto funkciu používať, musí byť vo vašom systéme povolená. Správcovia môžu použiť pracovný priestor  **Správa funkcií**  na kontrolu stavu funkcie a jej aktiváciu, ak je to potrebné. V pracovnom priestore **Správa funkcií**  vyhľadajte a vyberte **Zaúčtované transakcie projektu s viacerými výbermi pre úpravy a dobropisy**, a potom vyberte **Povoliť teraz**.

Táto funkcia umožňuje nasledujúce kľúčové funkcie:

- Dá sa k nemu dostať zo stránky zaúčtovanej transakcie v rámci projektu pomocou existujúceho tlačidla **Úprava** .
- Umožňuje viacriadkové ovládanie výberu na stránke **Zaúčtované transakcie projektu** . Pred začatím úprav môžete na stránku zoznamu použiť filtre a vybrať svoje záznamy.
- Deaktivuje tlačidlo **Úprava**, ak nie je možné upraviť akúkoľvek jednotlivú transakciu alebo ak vyberiete kombináciu dobropisov a denníkov spolu namiesto jednotlivých.
- Z dôvodu pridania ovládacieho prvku výberu viacerých riadkov už odkaz **Zaviazané náklady**  na páse s nástrojmi nie je zakázaný, ak vyberiete viacero riadkov.
- Pridáva nasledujúcu varovnú správu: „Vybrali ste viac ako (vybraný počet) záznamov na úpravu. Pokračovanie v tejto akcii môže chvíľu trvať. Naozaj chcete pokračovať v tejto akcii?"

Táto funkcia tiež odstraňuje krok 2 z toku procesu, ktorý bol popísaný vyššie v tomto článku. Preto všetky transakcie, ktoré boli vybraté pred otvorením stránky  **Upraviť transakcie**, budú zahrnuté do zoznamu transakcií na úpravu. Na ich vyhľadávanie nemusíte použiť tlačidlo **Vybrať** .

> [!NOTE] 
> Aj keď je táto funkcia zakázaná, stále môžete vybrať viacero záznamov na úpravu. Iba jeden záznam však *zostane vybratý* a dialógové okno **Vybrať transakcie**  sa zobrazí ihneď po výbere možnosti otvorené úpravy.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Stavy transakcií úprav, ktoré možno povoliť alebo zakázať pre úpravy

Nasledujúce stavy možno povoliť alebo zakázať na karte **Všeobecné** na stránke **Parametre riadenia projektu a účtovníctva** :

- Uverejnené
- Návrh faktúry
- Fakturované
- Odhadované
- Eliminovaný
- Počiatočný zostatok (hodina)

## <a name="adjustment-parameters"></a>Parametre nastavenia

Tieto parametre sú uvedené na stránke **Parametre projektového manažmentu a účtovníctva** na karte **Všeobecné** pod **Úprava** skupina a upraví správanie pre spôsob spracovania úprav. 

| Názov parametra | Description |
|----------------|-------------
| Vždy vytvorte transakciu úpravy | Ak je tento parameter povolený, proces úpravy vždy vytvorí novú reverznú transakciu a novú upravenú transakciu, keď dôjde k finančnému alebo vykazovaciemu vplyvu. Ak je parameter zakázaný, proces úpravy aktualizuje pôvodnú transakciu namiesto vytvorenia storna a novej transakcie pre scenár, ako je aktualizácia textu transakcie. |
| Pole automatickej aktualizácie | Ak je tento parameter povolený, systém prepočíta obstarávaciu a predajnú cenu. |
| Použiť dátum úpravy ako nový projekt | Tento parameter sa používa na presun transakcií do budúceho fiškálne obdobie predtým, ako systém túto funkciu podporoval. Neodporúčame vám ho používať, pretože mení obchodný dátum transakcie a v budúcom vydaní bude zastarané. |
| Povoliť uzavreté aktivity | Zvyčajne nie je možné vytvoriť transakcie pre uzavreté aktivity. Ak je tento parameter povolený, toto správanie je prepísané. Preto je možné vytvárať opravné položky k uzavretým činnostiam. |
