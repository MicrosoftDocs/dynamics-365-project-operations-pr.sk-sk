---
title: Koncepty finančného odhadu
description: Táto téma poskytuje informácie o finančných odhadoch projektov v Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 74b2499cc706e03658cadeb088df154100051cbc7cce386b2e4d50dbdb5c197f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989210"
---
# <a name="financial-estimation-concepts"></a>Koncepty finančného odhadu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

V Dynamics 365 Project Operations môžete svoje projekty finančne odhadnúť v dvoch etapách: 
1. Počas predpredajnej etapy pred získaním obchodu. 
2. Počas fázy realizácie po vytvorení projektovej zmluvy. 

Finančný odhad pre projektovú prácu môžete vytvoriť na ktorejkoľvek z nasledujúcich 3 stránok:
- Stránka **Riadok cenovej ponuky** pomocou podrobností riadkov cenovej ponuky.  
- Stránka **Riadok projektovej zmluvy** pomocou podrobností riadkov zmluvy. 
- Stránka **Projekt** pomocou stránok s kartami **Úlohy** alebo **Odhady výdavkov**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Použitie projektovej cenovej ponuky na vytvorenie odhadu
Na cenovej ponuke založenej na projekte, môžete použiť entitu **Podrobnosti o riadku cenovej ponuky** na odhad práce potrebnej na doručenie projektu. Potom môžete tento odhad zdieľať so zákazníkom.

Riadky cenovej ponuky založenej na projekte môžu mať nula alebo ľubovoľný počet podrobností o riadku cenovej ponuky. Podrobnosti riadka cenovej ponuky sa používajú na odhad času, výdavkov alebo poplatkov. Microsoft Dynamics 365 Project Operations neumožňuje odhady materiálu v detailoch riadku cenovej ponuky. Tieto sa nazývajú triedy transakcií. Odhadované čiastky dane možno zadať aj v triede transakcie.

Okrem tried transakcií majú podrobnosti o riadku cenovej ponuky typ transakcie. Pre podrobnosti riadka cenovej ponuky sú podporované dva typy transakcií: **Cena** a **Projektová zmluva**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Použitie projektovej zmluvy na vytvorenie odhadu

Ak ste použili cenovú ponuku, keď ste vytvorili zmluvu založenú na projekte, odhad, ktorý ste urobili pre každý riadok cenovej ponuky v ponuke, sa skopíruje do zmluvy o projekte. Štruktúra projektovej zmluvy je ako štruktúra projektovej cenovej ponuky, ktorá má riadky, podrobnosti riadka a fakturačné plány.

Odhady možno vykonať priamo v projektovej zmluve, ako v projektovej cenovej ponuke. Pri projektovej cenovej ponuke sa odhad vykoná pomocou riadkov zmluvy a podrobností riadka zmluvy. Podrobnosti riadka zmluvy môžu byť vytvorené aj z projektového plánu vytvoreného pomocou odhadu prístupu zdola nahor.

Podrobnosti riadka projektovej zmluvy sa môžu používať na odhad času, výdavkov alebo poplatkov. Odhadované čiastky dane možno zadať aj v detaile riadku zmluvy.

Odhady materiálu nie sú povolené v podrobnostiach riadku zmluvy.

## <a name="use-a-project-to-create-an-estimate"></a>Použitie projektu na vytvorenie odhadu 

Môžete odhadnúť čas a náklady na projekty. Project Operations nepodporuje odhady materiálov alebo poplatkov za projekty.

Odhady času sa generujú pri vytváraní úlohy a identifikujú atribúty všeobecného zdroja, ktorý je potrebný na vykonanie úlohy. Odhady sa generujú z úloh plánovania. Odhady času sa nevytvoria, ak vytvoríte všeobecných členov tímu mimo kontextu plánu.

Odhady výdavkov sú zadané v mriežke na stránke **Odhady výdavkov**.

Vytvorenie odhadu pre projekt sa považuje za najlepší postup, pretože v pláne projektu môžete pre každú úlohu vytvoriť podrobné odhady práce alebo času a výdavkov zdola nahor. Tento podrobný odhad potom môžete použiť na vytvorenie odhadov pre každý riadok cenovej ponuky a vytvoriť tak ešte dôveryhodnejšiu cenovú ponuku pre zákazníka. Keď importujete alebo vytvoríte podrobný odhad na riadku cenovej ponuky pomocou plánu projektu, Project Operations importuje hodnoty predaja a hodnoty nákladov z týchto odhadov. Po importe si môžete pozrieť ziskovosť, marže a metriky uskutočniteľnosti v ponuke projektu.

## <a name="understanding-estimates"></a>Porozumenie odhadom

Použite nasledujúcu tabuľku ako príručku na pochopenie obchodnej logiky vo fáze odhadu.

| Scenár                                                                                                                                                                                                                                                                                                                                          | Záznam entity                                                                                                                                                                                                       | Typ transakcie | Trieda transakcie | Dodatočné informácie                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Keď potrebujete odhadnúť predajnú hodnotu času na cenovú ponuku                                                                                                                                                                                                                                                                                    | Záznam riadka podrobností cenovej ponuky (QLD) je vytvorený                                                                                                                                                                               | Projektová zmluva | Time        | Pole transakcie pôvodu na strane predaja QLD riadka odkazuje na náklady na strane QLD |
|                                                                                                                                                                                                                                                                                     | Druhý QLD záznam je vytvorený systémom na uloženie zodpovedajúcej hodnoty nákladov. Všetky nepeňažné polia sú skopírované z predaja QLD na náklady QLD systému.                                                                                                                                                                               | Náklady | Time        | Pole transakcie pôvodu na strane predaja podrobností riadka cenovej ponuky (QLD) odkazuje na riadok náklady na strane QLD |
| Keď potrebujete odhadnúť predajnú hodnotu času na zmluve                                                                                                                                                                                                                                                                                 | Záznam riadka projektovej zmluvy (CLD) je vytvorený                                                                                                                                                                    | Projektová zmluva | Time        | Pole transakcie pôvodu na strane predaja CLD riadka odkazuje na náklady na strane CLD      |
|                                                                                                                                                                                                                                                                                  | Druhý CLD záznam je vytvorený systémom na uloženie zodpovedajúcej hodnoty nákladov. Všetky nepeňažné polia sú skopírované z predaja CLD na náklady CLD systémom.                                                                                                                                                                    | Náklady | Time        | Pole transakcie pôvodu na strane predaja CLD riadka odkazuje na náklady na strane CLD      |
| Keď používateľ popisuje zdroj na projektovej úlohe                                                                                                                                                                                                                                                                                            | Odhad záznamu riadka na zobrazenie predajnej hodnoty úlohy sa vytvorí pri vytvorení úlohy so všetkými požadovanými dimenziami cien. Roly a organizačné jednotky sú cenové dimenzie | Projektová zmluva | Čas        |                                                                                   |
|     | Odhad záznamu riadka na zobrazenie nákladovej hodnoty úlohy sa vytvorí pri vytvorení úlohy so všetkými požadovanými dimenziami cien. Všetky nepeňažné polia sú skopírované z riadka odhadu predaja do riadku odhadu nákladov systému. Rola a organizačná jednotka sú cenové dimenzie pre sadzby nákladov aj fakturácie.                                                                                                                                                                                                                | Náklady             | Čas           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Prispôsobenie entít Podrobnosti o riadku cenovej ponuky a Podrobnosti o riadku zmluvy

Ak ste do podrobností riadka cenovej ponuky pridali vlastné pole a chcete, aby systém zadal hodnotu poľa ako predvolenú hodnotu v riadku súvisiacich nákladov, ktorý vytvára, použite nástroje na registráciu doplnku **PreOperationContractLineDetailUpdate** a **PreOperationQuoteLineDetailUpdate**. Tieto doplnky sa musia znova zaregistrovať po zmene podrobností riadka cenovej ponuky alebo podrobností riadka zmluvy. Postupujte podľa týchto krokov na dokončenie úlohy:

1. Otvorte PluginRegistrationTool a pripojte sa k online inštancii.
2. Vyberte položku **Hľadať** a vyhľadajte doplnok, ktorý chcete aktualizovať.
3. Vyberte doplnok a potom na hlavnej stránke kliknite na možnosť **Vybrať**.
4. Vyberte krok doplnku, ktorý chcete aktualizovať, kliknite pravým tlačidlom myši a potom vyberte položku **aktualizovať.**
5. V dialógovom okne **aktualizovať existujúci krok** v poli **filtrovanie atribútov** vyberte elipsové tlačidlo (**...**):
6. V dialógovom okne **Výber atribútov** vyberte začiarkavacie políčka pre vlastné atribúty.
7. Kliknite na tlačidlo **OK** pre zatvorenie dialógového okna a potom vyberte **aktualizovať krok.**
8. Opakujte kroky 1 až 7 pre druhý doplnok.
9. Zatvorte **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
