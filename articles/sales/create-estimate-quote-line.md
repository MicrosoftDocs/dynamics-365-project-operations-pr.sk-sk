---
title: Vytvorenie odhadov v riadku cenovej ponuky
description: Táto téma poskytuje informácie o tom, ako vytvoriť odhad riadku cenovej ponuky pre projekt.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 97030689eddb88576ffcf9dd848f8a0776512192
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122947"
---
# <a name="create-estimates-on-a-quote-line"></a>Vytvorenie odhadov v riadku cenovej ponuky

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Na cenovej ponuke založenej na projekte, môžete použiť entitu detail riadka cenovej ponuky na odhad práce potrebnej na doručenie projektu. Potom môžete tento odhad zdieľať so zákazníkom.

Riadky cenovej ponuky založenej na projekte nemajú mať žiadne podrobnosti riadka cenovej ponuky. Alternatívne môžu mať veľa podrobností o riadku cenovej ponuky. Podrobnosti riadka cenovej ponuky sa používajú na odhad času, výdavkov alebo poplatkov. Dynamics 365 Project Operations neumožňuje odhady materiálu v detailoch riadku cenovej ponuky. Tieto sa nazývajú triedy transakcií. Odhadované čiastky dane možno zadať aj v triede transakcie.

Okrem tried transakcií majú podrobnosti o riadku cenovej ponuky typ transakcie. Pre podrobnosti riadka cenovej ponuky existujú dva typy transakcií: **Náklady** a **Projektová zmluva**.

## <a name="estimate-by-using-a-contract"></a>Odhad pomocou zmluvy

Ak ste použili cenovú ponuku Project Operations, keď ste vytvorili zmluvu založenú na projekte, odhad, ktorý ste urobili pre každý riadok cenovej ponuky v ponuke, sa skopíruje do zmluvy o projekte. Štruktúra projektovej zmluvy je ako štruktúra projektovej cenovej ponuky, ktorá má riadky, podrobnosti riadka a fakturačné plány.

Odhady možno vykonať priamo v projektovej zmluve, ako v projektovej cenovej ponuke. Pri projektovej cenovej ponuke sa odhad vykoná pomocou riadkov zmluvy a podrobností riadka zmluvy. Podrobnosti riadka zmluvy môžu byť vytvorené aj z projektového plánu vytvoreného pomocou odhadu prístupu zdola nahor.

Podrobnosti riadka projektovej zmluvy sa môžu používať na odhad času, výdavkov alebo poplatkov. Odhadované čiastky dane možno zadať aj v detaile riadku zmluvy.

Odhady materiálu nie sú povolené v podrobnostiach riadku zmluvy.

Procesy, ktoré sú podporované na projektovej zmluve, sú vytvorenie a potvrdenie faktúry. Vytváranie faktúr vytvorí koncept faktúry založenej na projekte, ktorá zahŕňa všetky nefakturované skutočné hodnoty predaja až do aktuálneho dátumu.

Potvrdenie robí zmluvu iba na čítanie a zmení jej stav od **konceptu** k **potvrdeniu**. Po tejto akcii ju nemôžete vrátiť späť. Keďže táto akcia je trvalá, najlepšia skúška je uchovávať zmluvu v stave **konceptu**.

Jediné rozdiely medzi navrhnutými zmluvami a potvrdenými zmluvami sú ich postavenie a skutočnosť, že návrh zmluvy možno upraviť, zatiaľ čo potvrdené zmluvy nemôžno. Vytváranie faktúr a sledovanie skutočných hodnôt možno vykonať na návrhoch zmlúv a potvrdených zmluvách.

Objednávky zmien nie sú podporované v prípade zmlúv alebo projektov.

## <a name="estimating-projects"></a>Odhadovanie projektov

Môžete odhadnúť čas a výdavky na projekty, ale nie materiály alebo poplatky.

Odhady času sa generujú pri vytváraní úlohy a identifikujú atribúty všeobecného zdroja, ktorý je potrebný na vykonanie úlohy. Odhady sa generujú z úloh plánovania. Odhady času sa nevytvoria, ak vytvoríte všeobecných členov tímu mimo kontextu plánu.

Odhady výdavkov sú zadané v mriežke na stránke **odhady**.

## <a name="understand-estimation"></a>Porozumenie odhadu

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

Ak ste do podrobností riadka cenovej ponuky pridali vlastné pole a chcete, aby systém zadal hodnotu poľa ako predvolenú hodnotu v riadku súvisiacich nákladov, ktorý vytvára, použite doplnok PreOperationContractLineDetailUpdate a PreOperationQuoteLineDetailUpdate registračné nástroje. Tieto doplnky sa musia znova zaregistrovať po zmene podrobností riadka cenovej ponuky alebo podrobností riadka zmluvy. Postupujte podľa týchto krokov na dokončenie úlohy:

1. Otvorte PluginRegistrationTool a pripojte sa k online inštancii.
2. Vyberte položku **Hľadať** a vyhľadajte doplnok, ktorý chcete aktualizovať.
3. Vyberte doplnok a potom na hlavnej stránke vyberte položku **vybrať**.
4. Vyberte krok doplnku, ktorý chcete aktualizovať, kliknite pravým tlačidlom myši a potom vyberte položku **aktualizovať.**
5. V dialógovom okne **aktualizovať existujúci krok** v poli **filtrovanie atribútov** vyberte elipsové tlačidlo (**...**):
6. V dialógovom okne **Výber atribútov** vyberte začiarkavacie políčka pre vlastné atribúty.
7. Kliknite na tlačidlo **OK** pre zatvorenie dialógového okna a potom vyberte **aktualizovať krok.**
8. Opakujte kroky 1 až 7 pre druhý doplnok.
9. Zatvorte nástroj PluginRegistrationTool.
