---
title: Predbežná rezervácia zdroja
description: Táto téma poskytuje informácie o tom, ako predbežne naplánovať alebo predbežne rezervovať členov projektového tímu.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: cb506a519dbc490ecdd579edf1e3fa5dd0153bdb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084489"
---
# <a name="soft-book-a-resource"></a>Predbežná rezervácia zdroja

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Predbežne môžete naplánovať alebo predbežne zarezervovať zdroj do tímu projektu, aby sa zobrazil váš plán priradenia zdroju k projektu. Predbežné rezervácie nespotrebúvajú dostupnú kapacitu zdroja a člena tímu s predbežným priradením môžete priraďovať k projektovým úlohám. Pretože predbežná rezervácia nespotrebúva kapacitu zdroja, môžete zdroj pevne zarezervovať pre iné úlohy v rámci rovnakého obdobia. Všeobecné zdroje nemožno predbežne zarezervovať, ani predbežná rezervácia nemôže vyplniť požiadavku na všeobecný zdroj.

Predbežne rezervovaní členovia projektového tímu sú uvedení na karte **Tím** stránka **projekt** spolu s ich predbežne zarezervovanými hodinami v stĺpci **počet predbežne rezervovaných hodín** v zobrazení **členovia tímu**. Predbežne zarezervovaní členovia tímu sú uvedení aj na tabule plánovania. Pretože sú predbežne zarezervovaní, tabuľa plánovania nezobrazí žiadnu spotrebu kapacity týchto zdrojov. Predbežne zarezervovaný čas sa nezobrazí na karte **odsúhlasenie** , ani sa nezobrazí v poli **Rozšíriť rezervácie** na karte **odsúhlasenie** na plánovacej tabuli. 

Existujú dva spôsoby predbežnej rezervácie člena tímu do projektu: priamo z tabule plánovania alebo pridaním člena tímu na karte **Tím**. 

## <a name="soft-book-from-the-schedule-board"></a>Predbežná rezervácia použitím tabule plánovania
Ak chcete predbežne rezervovať zdroj z plánovacej tabule, postupujte podľa nasledujúcich krokov. 

1. Zvoľte si kartu **Projekt** v spodnej časti panela **požiadavky na rezervácie** na tabule plánovania.
2. Vyhľadajte si projekt, ku ktorému chcete predbežne zarezervovať zdroj. Ak v zozname existuje veľký počet projektov, vyberte hlavičku stĺpca **projektu** a potom použite filter na vyhľadanie jedného alebo viacerých projektov.
3. Kliknite na projekt a potom potiahnite a pustite ho na časovú os zdroja.
5. V paneli **vytvoriť rezerváciu zdroja** upravte počiatočný a koncový dátum, nastavte **stav rezervácie** na **soft** a potom nastavte hodiny. 
6. Kliknite na **rezervovať**. Späť v projekte sa zdroj zobrazí na karte **Tím** ako zdroj pre projekt. V zobrazení **pomenovaného člena tímu** uvidíte hodiny predbežnej rezervácie v stĺpci **Počet predbežne rezervovaných hodín**.

> [!NOTE]
> Teraz môžete priraďovať predbežne rezervované položky k úlohám na karte **plánovania**. Na karte **odsúhlasenia** budú zdroje zobrazovať deficit rezervácie, ktorý súvisí s ich priradením úloh, pretože karta **odsúhlasenie** zohľadňuje iba pevné rezervácie. Funkciu **Predĺžiť rezerváciu** môžete použiť na pevné rezervovanie zdroja, čím sa odstráni deficit pevných rezervácií v porovnaní s priradeniami zdrojov. Prostredníctvom **správy rezervácie** musíte manuálne zrušiť predbežnú rezerváciu zdroja.

## <a name="soft-book-on-the-team-tab"></a>Predbežná rezervácia na karte Tím

Členov tímu pridávajte priamo na karte **Tím** a následne zmeňte stav ich rezervácie z **Pevné** na **Predbežné** prostredníctvom **správy rezervácií**. Po pridaní člena tímu týmto spôsobom bude výsledkom vždy pevná rezervácia. Výnimkou je, že spôsob priradenia nezvolíte **Žiadny**.

Ak chcete použiť túto metódu, postupujte nasledovne:

1. Na stránke **Project** na karte **Team** kliknite na **New**.
2. Zvoľte si rezervovateľný zdroj, rolu, dátumy od a do.
3. Vyberte metódu prideľovania inú než **Žiadne** :
4. Vyberte položku **Uložiť**. Uvidíte zdroj na mriežke a jeho hodiny v stĺpci **Počet pevne rezervovaných hodín**.
5. Spravujte rezerváciu zdrojov kliknutím na možnosť **Spravovať rezervácie**.
6. Po otvorení tabule plánovania si rozbaľte zdroj, čím si zobrazíte jeho rezervácie. Stav rezervácie bude **Pevná**.
7. Kliknite pravým tlačidlom myši na rezerváciu v časti **Zmena stavu** si zvoľte možnosť **Predbežná rezervácia** \> **Predbežná**. Stav rezervácie bude **Predbežná**.
8. Po zatvorení tabule plánovania uvidíte, že hodiny pre zdroj sa presunuli zo stĺpca **počet pevne rezervovaných hodín** do stĺpca **počet predbežne rezervovaných hodín** na mriežke karty **tím** uvidíte to pri zobrazení **pomenovaných členov tímu**.

> [!NOTE]
> Keď používate **údržbu rezervácií** na zmenu stavu z **pevná** na **predbežná** , a v prípade pevnej rezervácie zdroja do tímu a následného priradenia úloh k zdroju, po použití správy rezervácií na zmenu stavu z Pevné na Predbežné sa ponechá priradenie úlohy daného zdroja. Na karte **odsúhlasenie** bude mať zdroj deficit rezervácie, pretože pri vyrovnávaní rezervácií a pridelení sa zohľadňujú iba pevné rezervácie. Funkciu **Predĺžiť rezerváciu** na karte **odsúhlasenie** môžete použiť na pevné rezervovanie zdroja, čím sa odstráni deficit pevných rezervácií v porovnaní s priradeniami zdrojov. Prostredníctvom **správy rezervácie** musíte zrušiť predbežnú rezerváciu zdroja.

Keď budete pripravený na zmenu predbežne rezervovaného zdroja člena tímu na pevne rezervovaného člena tímu, postupujte nasledovne:

1. Po otvorení tabule plánovania si rozbaľte zdroj, čím si zobrazíte jeho rezervácie. Stav rezervácie bude **Predbežná**.
2. Kliknite pravým tlačidlom myši na rezerváciu V časti **Zmena stavu** si zvoľte možnosť **Pevná rezervácia** \> **Pevná**. Stav rezervácie bude **Pevná**.
3. Po zatvorení tabule plánovania a prechode späť na projekt a otvorení karty **tím** uvidíte, že hodiny pre zdroj sa presunuli zo stĺpca **počet predbežne rezervovaných hodín** do stĺpca **počet pevne rezervovaných hodín** na mriežke karty **tím**. Uvidíte to pri zobrazení **pomenovaných členov tímu**. Ak bol zdroj pridelený úlohám, nebude sa viac zobrazovať ako deficit rezervácie na karte **odsúhlasenie** , pretože rezervácia je odteraz považovaná za pevnú.

