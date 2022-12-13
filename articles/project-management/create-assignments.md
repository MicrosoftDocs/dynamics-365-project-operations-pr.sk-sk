---
title: Vytvorenie priradení zdrojov
description: Tento článok poskytuje informácie o vytváraní priradení všeobecných a pomenovaných zdrojov.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812013"
---
# <a name="create-resource-assignments"></a>Vytvorenie priradení zdrojov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_


Priradenie zdroja je priame priradenie člena projektového tímu k úlohe listového uzla. Tento článok poskytuje informácie o rôznych spôsoboch priradenia zdrojov.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Vytvorte všeobecného člena tímu prostredníctvom priradenia úlohy


Keď vytvoríte všeobecného člena tímu prostredníctvom priradenia úlohy, vytvoríte zástupný symbol alebo všeobecný zdroj. Tento všeobecný zdroj popisuje charakteristiky pomenovaného prostriedku, na ktorom chcete v konečnom dôsledku pracovať na úlohách. Potom vygenerujete požiadavku alebo odošlete požiadavku pomocou požiadavky, ktorá sa používa na vyhľadanie a rezerváciu uvedeného zdroja.

1. Na mriežke plánu stlačte ikonu zdroja v bunke **Zdroj**.
2. Zadajte názov, ktorý bude slúžiť ako názov zástupného zdroja. Napríklad, programový manažér
3. Vybert **vytvoriť** a v poli **rýchle vytvorenie porjektového člena tímu**, nastavte rolu pre všeobecný zdroj.
4. Priraďte potrebné úlohu k tomuto zástupnému zdroju výberom zdroja v časti **Výber zdroja** pre úlohy. Zdroje uvedené pod položkou **Členovia tímu**.
5. Keď skončíte priraďovanie všeobecného zdroja, na karte **Tím**  vyberte všeobecný zdroj a potom vyberte **Generovať požiadavku** na vytvorenie požiadavky na zdroj pre všeobecný zdroj.
6. Stlačte možnosť **Rezervovať** pre všeobecný zdroj a potom použite tabuľu plánovania na vyhľadanie a rezerváciu skutočného zdroja. Požiadavku môžete tiež odoslať na vyplnenie manažérovi zdroja.
7. Keď sa generický zdroj úplne naplní pomenovaným zdrojom, generický zdroj sa z tímu odstráni. (Čiastočné splnenie požiadavky na zdroj nebude mať za následok priradenie zdroja.) Priradenia úloh pre generický zdroj sú priradené k pomenovanému zdroju, ktorý splnil požiadavku na zdroj generického zdroja.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Priradenie pomenovaného zdroja zo zoznamu všetkých rezervovateľných zdrojov

Pole vyhľadávania možno v časti **Výber zdroja** použiť na vyhľadanie všetkých aktívnych rezervovateľných zdrojov a ich priradenie k úlohe listového uzla. Prostriedky pridelené týmto spôsobom sa pridajú do tímu bez akýchkoľvek rezervácií. To je podobné ako pridanie člena tímu a výber možnosti **Nič** ako spôsob prideľovania. Zdroje sa zobrazia na kartách **Tím**, **Priradenie zdroja** a **Odsúhlasenie** ako zdroje s tým, že im bude chýbať priradenie a rezervácia. Ak chcete využiť ich dostupnosť, zarezervujte ich.

1. Z mriežky úloh, tabule alebo časovej osi prejdite na bunku **Priradené používateľovi**.
2. Do vyhľadávacieho poľa začnite písať meno. Výsledky vyhľadávania pre názov sú zobrazené vo **výbere zdroja** v časti **iné zdroje**.
3. Vyberte zdroj, ktorý chcete priradiť k úlohe, alebo vyberte názov zdroja v časti **Ďalšie tímové zdroje**.

## <a name="editing-resource-assignment-contours"></a>Upravovanie kontúr priradenia zdrojov

V predvolenom nastavení, keď sú zdroje priradené k úlohe v pláne, ich úsilie sa lineárne rozdelí na každý zdroj na základe pracovného času daného zdroja a režimu plánovania projektu. Projektový manažér môže použiť mriežku priraďovania zdrojov na spresnenie odhadov úsilia každého zdroja, ktorý je priradený k jednej alebo viacerým úlohám v rôznych časových intervaloch. Táto funkcia pomáha projektovým manažérom vytvárať presnejšie odhady nákladov a predaja, ktoré sú riadené kontúrami priradenia zdrojov, ktoré sa generujú, keď je zdroj priradený k úlohe. Okrem toho môžu projektoví manažéri ľahšie reflektovať dopyt po zdrojoch, ktorý je potrebný na vytvorenie dopytu v požiadavke na zdroj.

### <a name="navigation"></a>Navigácia

Ak chcete získať prístup k mriežke na úpravu obrysu, projektový manažér najskôr vyberie kartu **Úlohy** na hlavnej stránke projektu a potom vyberie položku **Zadania** tab.

![Karta Úlohy na karte Úlohy na hlavnej stránke projektu.](media/AssignmentGrid.png)

Mriežka podporuje dva spôsoby zoskupovania: **zoskupiť podľa zdroja** a **zoskupiť podľa úlohy**. Na rozdiel od zobrazenia mriežky sa stĺpce nedajú konfigurovať. Jediné viditeľné stĺpce sú **Priradené**, **Názov úlohy**, **Začiatok zadania**,** Dokončenie zadania **a** Úsilie priradenia **.

Keď je mriežka na začiatku vykreslená, začína na najskoršom obryse priradenia. Ak váš rozvrh neobsahuje žiadne úlohy, ktoré vyžadujú úsilie, mriežka bude prázdna a nič nevykreslí.

![Prázdna mriežka úloh.](media/emptyassignmentgrid.png)

Ak chcete zobraziť svoje kontúry a rôzne časové škály, k dispozícii je aj mriežka priradenia zdrojov len na čítanie a mriežka zosúladenia zdrojov.

### <a name="resource-calendars"></a>Kalendáre zdrojov

Schopnosť upraviť obrys pre konkrétny deň sa riadi pracovnými dňami zdroja, ako je uvedené v jeho kalendári. Ak je bunka pre daný zdroj zakázaná, tento zdroj nemá počas tohto obdobia pracovné dni.

Obrysy zdroja môžu presahovať aktuálny dátum začiatku a konca priradenej úlohy. Ak sa obrys aktualizuje tak, že je po najnovšom dátume ukončenia úlohy alebo najskoršom dátume začiatku úlohy, dátum ukončenia alebo dátum začiatku úlohy sa podľa potreby zmení. Ak je však obrys aktualizovaný tak, že je skorší ako dátum začiatku úlohy, ktorá je prepojená s predchodcom, aktualizácia zlyhá, pretože priradenie spustí úlohu spustenia pred dokončením jej predchodcu a toto správanie momentálne nie je podporované.

### <a name="co-authoring"></a>Spolutvorba

Zmeny v mriežke priradenia zdrojov sa automaticky prejavia vo všetkých súvisiacich zobrazeniach vrátane zobrazenia grafu, časovej osi, tabule a mriežky. Ak projekt kontroluje viacero používateľov súčasne, všetky zmeny, ktoré vykoná jeden používateľ, sa prejavia v mriežke. Naopak, všetky zmeny vykonané v mriežke priradenia zdrojov sa zobrazia všetkým ostatným používateľom, ktorí si prezerajú projekt v tej istej relácii.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
