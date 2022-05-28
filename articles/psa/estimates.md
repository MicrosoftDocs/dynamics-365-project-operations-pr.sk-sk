---
title: Odhady
description: Táto téma poskytuje informácie o odhadoch v Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 978af25fb89feb61e3c6fcfeafa212db034ff5cb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590687"
---
# <a name="estimates"></a>Odhady

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Na cenovej ponuke založenej na projekte, môžete použiť entitu detail riadka cenovej ponuky na odhad práce potrebnej na doručenie projektu. Potom môžete tento odhad zdieľať so zákazníkom.

Riadky cenovej ponuky založenej na projekte nemajú mať žiadne podrobnosti riadka cenovej ponuky. Alternatívne môžu mať veľa podrobností o riadku cenovej ponuky. Podrobnosti riadka cenovej ponuky sa používajú na odhad času, výdavkov alebo poplatkov. PSA neumožňuje odhady materiálu v detailoch riadku cenovej ponuky. Tieto sa nazývajú triedy transakcií. Odhadované čiastky dane možno zadať aj v triede transakcie.

Okrem tried transakcií majú podrobnosti o riadku cenovej ponuky typ transakcie. PSA podporuje dva typy transakcií pre podrobnosti riadka cenovej ponuky: **Cena** a **projektová zmluva**.

## <a name="estimate-by-using-a-contract"></a>Odhad pomocou zmluvy

Ak ste použili cenovú ponuku PSA, keď ste vytvorili zmluvu založenú na projekte, odhad, ktorý ste urobili pre každý riadok cenovej ponuky v ponuke, sa skopíruje do zmluvy o projekte. Štruktúra projektovej zmluvy je ako štruktúra projektovej cenovej ponuky, ktorá má riadky, podrobnosti riadka a fakturačné plány.

Odhady možno vykonať priamo v projektovej zmluve, ako v projektovej cenovej ponuke. Pri projektovej cenovej ponuke sa odhad vykoná pomocou riadkov zmluvy a podrobností riadka zmluvy. Podrobnosti riadka zmluvy môžu byť vytvorené aj z projektového plánu vytvoreného pomocou odhadu prístupu zdola nahor.

Podrobnosti riadka projektovej zmluvy sa môžu používať na odhad času, výdavkov alebo poplatkov. Odhadované čiastky dane možno zadať aj v detaile riadku zmluvy.

PSA neumožňuje odhady materiálu v detailoch riadku zmluvy.

Procesy, ktoré sú podporované na projektovej zmluve, sú vytvorenie a potvrdenie faktúry. Vytváranie faktúr vytvorí koncept faktúry založenej na projekte, ktorá zahŕňa všetky nefakturované skutočné hodnoty predaja až do aktuálneho dátumu.

Potvrdenie robí zmluvu iba na čítanie a zmení jej stav od **konceptu** k **potvrdeniu**. Po tejto akcii ju nemôžete vrátiť späť. Keďže táto akcia je trvalá, najlepšia skúška je uchovávať zmluvu v stave **konceptu**.

Jediné rozdiely medzi navrhnutými zmluvami a potvrdenými zmluvami sú ich postavenie a skutočnosť, že návrh zmluvy možno upraviť, zatiaľ čo potvrdené zmluvy nemôžno. Vytváranie faktúr a sledovanie skutočných hodnôt možno vykonať na návrhoch zmlúv a potvrdených zmluvách.

PSA nepodporuje príkazy na zmenu zmlúv alebo projektov.

## <a name="estimating-projects"></a>Odhadovanie projektov

Môžete odhadnúť čas a náklady na projekty. PSA neumožňuje odhady materiálov alebo poplatkov na projektoch.

Odhady času sa generujú pri vytváraní úlohy a identifikujú atribúty všeobecného zdroja, ktorý je potrebný na vykonanie úlohy. Odhady sa generujú z úloh plánovania. Odhady času sa nevytvoria, ak vytvoríte všeobecných členov tímu mimo kontextu plánu.

Odhady výdavkov sú zadané v mriežke na stránke **odhady**.

## <a name="understanding-estimation"></a>Porozumenie odhadu

Použite nasledujúcu tabuľku ako príručku na pochopenie obchodnej logiky vo fáze odhadu.

| Scenár                                                                                                                                                                                                                                                                                                                                          | Záznam entity                                                                                                                                                                                                       | Typ transakcie | Trieda transakcie | Dodatočné informácie                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Keď potrebujete odhadnúť predajnú hodnotu času na cenovú ponuku                                                                                                                                                                                                                                                                                    | Záznam riadka podrobností cenovej ponuky (QLD) je vytvorený                                                                                                                                                                               | Projektová zmluva | Time        | Pole transakcie pôvodu na strane predaja QLD riadka odkazuje na náklady na strane QLD |
|                                                                                                                                                                                                                                                                                     | Druhý QLD záznam je vytvorený systémom na uloženie zodpovedajúcej hodnoty nákladov. Všetky nepeňažné polia sú skopírované z predaja QLD na náklady QLD systému.                                                                                                                                                                               | Náklady | Time        | Pole transakcie pôvodu na strane predaja podrobností riadka cenovej ponuky (QLD) odkazuje na riadok náklady na strane QLD |
| Keď potrebujete odhadnúť predajnú hodnotu času na zmluve                                                                                                                                                                                                                                                                                 | Záznam riadka projektovej zmluvy (CLD) je vytvorený                                                                                                                                                                    | Projektová zmluva | Time        | Pole transakcie pôvodu na strane predaja CLD riadka odkazuje na náklady na strane CLD      |
|                                                                                                                                                                                                                                                                                  | Druhý CLD záznam je vytvorený systémom na uloženie zodpovedajúcej hodnoty nákladov. Všetky nepeňažné polia sú skopírované z predaja CLD na náklady CLD systémom.                                                                                                                                                                    | Náklady | Time        | Pole transakcie pôvodu na strane predaja CLD riadka odkazuje na náklady na strane CLD      |
| Keď používateľ popisuje zdroj na projektovej úlohe                                                                                                                                                                                                                                                                                            | Odhad záznamu riadka na zobrazenie predajnej hodnoty úlohy sa vytvorí pri vytvorení úlohy so všetkými požadovanými dimenziami cien. Roly a organizačné jednotky sú dimenzie ceny OOB Project Service | Projektová zmluva | Time        |                                                                                   |
|     | Odhad záznamu riadka na zobrazenie nákladovej hodnoty úlohy sa vytvorí pri vytvorení úlohy so všetkými požadovanými dimenziami cien. Všetky nepeňažné polia sú skopírované z riadka odhadu predaja do riadku odhadu nákladov systému. Role a organizačná jednotka sú OOB PSA dimenzie ceny pre obe náklady a fakturačné sadzby.                                                                                                                                                                                                                | Náklady             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Prispôsobenie podrobností riadka cenovej ponuky a podrobností entít riadkov zmluvy

Ak ste do podrobností riadka cenovej ponuky pridali vlastné pole a chcete, aby systém zadal hodnotu poľa ako predvolenú hodnotu v riadku súvisiacich nákladov, ktorý vytvára, použite doplnok PreOperationContractLineDetailUpdate a PreOperationQuoteLineDetailUpdate registračné nástroje. Tieto doplnky sa musia znova zaregistrovať po zmene podrobností riadka cenovej ponuky alebo podrobností riadka zmluvy. Postupujte podľa týchto krokov na dokončenie úlohy:

1. Otvorte PluginRegistrationTool a pripojte sa k online inštancii.
2. Vyberte položku **Hľadať** a vyhľadajte doplnok, ktorý chcete aktualizovať.

    ![Dialógové okno Prehľadávať strom.](media/basic-guide-19.png)

3. Vyberte doplnok a potom na hlavnej stránke vyberte položku **vybrať**.
4. Vyberte krok doplnku, ktorý chcete aktualizovať, kliknite pravým tlačidlom myši a potom vyberte položku **aktualizovať.**

    ![Výber kroku v doplnku.](media/basic-guide-20.png)

5. V dialógovom okne **aktualizovať existujúci krok** v poli **filtrovanie atribútov** vyberte elipsové tlačidlo (**...**):
 
    ![Dialógové okno Aktualizovať existujúci krok.](media/basic-guide-21.png)

6. V dialógovom okne **Výber atribútov** vyberte začiarkavacie políčka pre vlastné atribúty.

    ![Dialógové okno Vyberte atribúty.](media/basic-guide-22.png)

7. Kliknite na tlačidlo **OK** pre zatvorenie dialógového okna a potom vyberte **aktualizovať krok.**
 
    ![Tlačidlo Aktualizovať krok.](media/basic-guide-23.png)

8. Opakujte kroky 1 až 7 pre druhý doplnok.
9. Zatvorte nástroj PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
