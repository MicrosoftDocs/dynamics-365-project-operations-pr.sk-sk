---
title: Projektové faktúry pro forma
description: Táto téma poskytuje informácie o projektových faktúrach pro forma v Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3d02728ce682781eb8816e0c2239cf62f88adfa8c5d2a0aab280be053c2a5ae6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992945"
---
# <a name="proforma-project-pnvoices"></a>Projektové faktúry pro forma

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Fakturácia projektov pro forma je užitočná, pretože poskytuje projektovým manažérom druhú úroveň schválenia pred vytvorením faktúr pre zákazníkov. Prvá úroveň schválenia sa dokončí, keď sú schválené zadania času, výdavkov a materiálu, ktoré predkladajú členovia projektového tímu.

Čiastočné nasadenie Dynamics 365 Project Operations nie je navrhnutý na generovanie faktúr orientovaných na zákazníka. Nasledujúci zoznam ukazuje, prečo nie je možné generovať faktúry:

- Neobsahujú daňové informácie.
- Iné meny nie je možné previesť na fakturačnú menu.
- Faktúry nie je možné správne naformátovať na tlač.

Namiesto toho môžete použiť finančný alebo účtovný systém na vytváranie faktúr orientovaných na zákazníka, ktoré používajú informácie z generovaných návrhov faktúr.

## <a name="creating-project-invoices"></a>Vytváranie projektových faktúr

Projektové faktúry možno vytvoriť po jednom alebo hromadne. Môžete ich vytvoriť manuálne, alebo môžu byť nakonfigurované tak, aby boli generované v automatizovaných spusteniach.

### <a name="manually-create-project-invoices"></a>Manuálne vytváranie projektových faktúr 

Na stránke so zoznamom **Projektové zmluvy** môžete vytvoriť projektové faktúry samostatne pre každú projektovú zmluvu, alebo môžete hromadne vytvárať faktúry pre viacero projektových zmlúv.

   - Ak chcete vytvoriť faktúru pre konkrétnu projektovú zmluvu, na stránke zoznamu **projektových zmlúv** otvorte projektovú zmluvu a potom vyberte **Vytvoriť faktúru**.

   Faktúra sa generuje pre všetky transakcie vybratej projektovej zmluvy, ktoré majú stav **pripravené na fakturáciu**. Tieto transakcie zahŕňajú čas, výdavky, materiál, míľniky, produktové riadky zmlúv a ďalšie nevyfakturované riadky denníka predaja, ktoré mohli byť potvrdené.

Hromadné vytváranie faktúr:

1. Na stránke zoznam **projektových zmlúv** vyberte jednu alebo viacero projektových zmlúv, pre ktoré chcete vytvoriť faktúru, a potom vyberte položku **vytvoriť projektové faktúry**.
2. Upozorňujúce hlásenie vás informuje o tom, že pred tým, ako sa vytvoria faktúry, môže dôjsť k oneskoreniu. Tento proces je tiež zobrazený. Stlačením **OK** zatvorte dialógové okno.

   Faktúra sa generuje pre všetky transakcie v riadku projektovej zmluvy, ktoré majú stav **pripravené na fakturáciu**. Tieto transakcie zahŕňajú čas, výdavky, materiál, míľniky, produktové riadky zmlúv a ďalšie nevyfakturované riadky denníka predaja, ktoré mohli byť potvrdené.

3. Ak chcete zobraziť faktúry, ktoré sú generované, prejdite do **Predaj** \> **Fakturácia** \> **Faktúry**. Pre každú zmluvu o projekte uvidíte jednu faktúru.

### <a name="set-up-automated-creation-of-project-invoices"></a>Nastavenie automatického vytvárania projektových faktúr 

Ak chcete nakonfigurovať automatické vytváranie faktúr, postupujte podľa týchto krokov.

1. Prejdite do časti **Nastavenia** \> **Dávkové úlohy**.
2. Vytvorte dávkovú úlohu a pomenujte ju **Vytvorenie faktúr Project Operations**. Názov dávkovej úlohy musí obsahovať výraz "Vytvoriť faktúry".
3. V poli **typ úlohy** vyberte položku **žiadne**. Štandardne je **frekvencia denne** a **je aktívne** možnosti nastavená na **Áno.**
4. Vyberte **spustiť pracovný postup**. V dialógovom okne **Vyhľadanie záznamu** sa zobrazia nasledujúce pracovné postupy:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Vyberte **ProcessRunCaller** a potom **pridať**.
6. V ďalšom dialógovom okne kliknite na **OK**. Pracovný postup **spánok** je nasledovaný pracovným postupom **proces**.

    Môžete tiež vybrať **processrunner** v kroku 5. Potom, keď vyberiete **OK**, pracovný postup **proces** je nasledovaný pracovným postupom **spánok**.

Pracovné postupy **processruncaller** a **processrunner** vytvárajú faktúry. **ProcessRunCaller** volá **processrunner**. **ProcessRunner** je pracovný postup, ktorý vytvára faktúry. Tento pracovný postup prechádza cez všetky riadky zmluvy, pre ktoré musia byť vytvorené faktúry, a vytvára faktúry. Ak chcete určiť riadky zmluvy, pre ktoré musia byť vytvorené faktúry, pracovný postup sa pozerá na dátumy vystavenia faktúry pre riadky zmluvy. Ak riadky zmluvy patriace do jednej zmluvy majú rovnaký dátum spustenia faktúry, transakcie sa skombinujú do jednej faktúry, ktorá má dva riadky faktúry. Ak neexistujú žiadne transakcie na vytvorenie faktúr, nevytvoria sa žiadne faktúry.

Po dokončení **procesrunnera**, sa volá **processruncaller**, ktorý poskytuje čas ukončenia a je uzavretý. **ProcessRunCaller** potom spustí časovač, ktorý beží 24 hodín od zadaného času ukončenia. Na konci časovača, je **processruncaller** uzavretý.

Dávková úloha pre vytváranie faktúr je opakujúca sa úloha. Ak je táto dávková úloha spustená mnohokrát, sú vytvorené viaceré inštancie úlohy, ktoré môžu spôsobovať chyby. Aby ste tento problém obišli, spustite dávkový proces len raz, a reštartujte ho len v prípade, že prestane fungovať.

> [!NOTE]
> Hromadná fakturácia sa spustí iba pre riadky zmlúv projektu, ktoré sú konfigurované podľa plánov faktúr. Riadok zmluvy s metódou fakturácie podľa fixnej ceny musí mať nakonfigurované medzníky. V riadku zmluvy projektu s metódou fakturácie podľa času a materiálu bude potrebné zostaviť plán fakturácie založený na dátume. To isté platí pre riadok zmluvy založený na projekte.      
 
### <a name="edit-a-draft-invoice"></a>Úprava konceptu faktúry

Pri vytváraní návrhu faktúry projektu, všetky nefakturované predajné transakcie, ktoré boli vytvorené, keď boli schválené zadania času a výdavkov sú stiahnuté na faktúru. Ak je faktúra stále v štádiu návrhu, môžete vykonať nasledujúce úpravy:

- Odstráňte alebo upravte podrobnosti riadka faktúry.
- Editujte a upravte množstvo a typ fakturácie.
- Priamo pridajte čas, výdavky, materiál a poplatky ako transakcie na faktúre. Túto funkciu môžete použiť, ak je riadok faktúry priradený k riadku zmluvy, ktorý umožňuje tieto triedy transakcií.

Výberom **potvrdiť** potvrďte faktúru. Táto akcia je jednosmerná akcia. Keď vyberiete možnosť **Potvrdiť**, faktúra bude iba na čítanie a vytvorí účtované predajné skutočné hodnoty z každého detailu riadka faktúry pre každý riadok faktúry. Ak podrobnosti riadka faktúry odkazujú na skutočné hodnoty nefakturovaného predaja, obnovia sa tiež skutočné hodnoty nefakturovaného predaja. Akýkoľvek detail riadka faktúry, ktorý bol vytvorený z položky využitia času, výdavkov alebo materiálu, bude odkazovať na skutočnú hodnotu nefakturovaného predaja. Systémy integrácie hlavnej účtovnej knihy môžu toto storno použiť na zvrátenie rozpracovanej projektovej práce (WIP) na účtovné účely.

### <a name="correct-a-confirmed-invoice"></a>Oprava potvrdenej faktúry

Potvrdené faktúry môžu byť editované. Keď opravíte potvrdenú faktúru, vytvorí sa nový koncept opravnej faktúry. Pretože predpoklad je, že chcete zvrátiť všetky transakcie a množstvá z pôvodnej faktúry, táto opravná faktúra obsahuje všetky transakcie z pôvodnej faktúry a všetky množstvá na nej sú nulové.

Ak existujú transakcie, ktoré nevyžadujú opravu, môžete ich odstrániť z konceptu opravnej faktúry. Ak chcete zvrátiť alebo vrátiť iba čiastočné množstvo, môžete upraviť pole **množstvo** v detaile riadka. Ak otvoríte detail riadka faktúry, môžete vidieť pôvodné množstvo faktúry. Potom môžete upraviť aktuálne množstvo faktúr tak, aby bolo menšie ako alebo väčšie ako pôvodné množstvo faktúry.

Po potvrdení opravnej faktúry, sú stornované pôvodné fakturované skutočné hodnoty a sú vytvorené nové fakturované skutočné hodnoty predaja. Ak bolo množstvo znížené, rozdiel spôsobí nové vytvorenie aj ďalších nefakturovaných skutočných hodnôt predaja. Ak bol napríklad pôvodný fakturovaný predaj osem hodín a detail riadka opravnej faktúry má znížené množstvo šiestich hodín, pôvodný fakturovaný predajný riadok sa vráti späť a vytvoria dve nové skutočné hodnoty:

- Skutočná hodnota fakturovaného predaja je šesť hodín.
- Skutočná hodnota nefakturovaného predaja sú dve hodiny. Táto transakcia môže byť fakturovaná neskôr alebo označená ako nefakturovateľná v závislosti od rokovaní so zákazníkom.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
