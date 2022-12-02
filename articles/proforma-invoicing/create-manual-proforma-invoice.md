---
title: Faktúry pro forma
description: Tento článok poskytuje informácie o faktúrach pro forma v Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7b56c3908cce3115d5c95a4b1b233db70fb6c149
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920585"
---
# <a name="proforma-invoices"></a>Faktúry pro forma

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Fakturácia pro forma je užitočná, pretože poskytuje projektovým manažérom druhú úroveň schválenia pred vytvorením faktúr pre zákazníkov. Prvá úroveň schválenia sa dokončí, keď sú schválené zadania času, výdavkov a materiálu, ktoré predkladajú členovia projektového tímu. Potvrdené faktúry pro forma sú k dispozícii v module Projektové účtovníctvo v Project Operations. Účtovníci projektu môžu vykonávať ďalšie aktualizácie, ako je napríklad daň z obratu, účtovníctvo a rozloženie faktúr.


## <a name="creating-project-invoices"></a>Vytváranie projektových faktúr

Projektové faktúry možno vytvoriť po jednom alebo hromadne. Môžete ich vytvoriť manuálne, alebo môžu byť nakonfigurované tak, aby boli generované v automatizovaných spusteniach.

### <a name="manually-create-project-invoices"></a>Manuálne vytváranie projektových faktúr 

Na stránke **Projektové zlmuvy** môžete vytvoriť projektové faktúry samostatne pre každú projektovú zmluvu, alebo môžete hromadne vytvárať faktúry pre viacero projektových zmlúv.

Ak chcete vytvoriť faktúru pre konkrétnu projektovú zmluvu, postupujte podľa tohto kroku.

- Na stránke zoznam **projektových zmlúv** otvorte zmluvu o projekte a potom vyberte položku **vytvoriť faktúru**.

    Faktúra sa generuje pre všetky transakcie vybratej projektovej zmluvy, ktoré majú stav **pripravené na fakturáciu**. Tieto transakcie zahŕňajú čas, výdavky, materiál, medzníky a ďalšie nevyfakturované riadky denníka predaja.

Ak chcete hromadne vytvárať faktúry, postupujte podľa týchto krokov.

1. Na stránke zoznam **projektových zmlúv** vyberte jednu alebo viacero projektových zmlúv, pre ktoré musíte vytvoriť faktúru, a potom vyberte položku **vytvoriť projektové faktúry.**

    Upozorňujúce hlásenie vás informuje o tom, že pred tým, ako sa vytvoria faktúry, môže dôjsť k oneskoreniu. Tento proces je tiež zobrazený.

2. Stlačením **OK** zatvorte dialógové okno.

    Faktúra sa generuje pre všetky transakcie v riadku projektovej zmluvy, ktoré majú stav **pripravené na fakturáciu**. Tieto transakcie zahŕňajú čas, výdavky, materiál, medzníky a ďalšie nevyfakturované riadky denníka predaja.

3. Ak chcete zobraziť faktúry, ktoré sú generované, prejdite na **Predaj** \> **fakturácia** \> **faktúry**. Pre každú zmluvu o projekte uvidíte jednu faktúru.

### <a name="set-up-automated-creation-of-project-invoices"></a>Nastavenie automatického vytvárania projektových faktúr 

Ak chcete nakonfigurovať automatické vytváranie faktúr, postupujte podľa týchto krokov.

1. Prejdite do časti **Nastavenia** \> **Dávkové úlohy**.
2. Vytvorte dávkovú úlohu a pomenujte ju **Vytvorenie faktúr Project Operations**. Názov dávkovej úlohy musí obsahovať výraz "Vytvoriť faktúry".
3. V poli **typ úlohy** vyberte položku **žiadne**. Štandardne je **frekvencia denne** a **je aktívne** možnosti nastavená na **Áno.**
4. Vyberte **spustiť pracovný postup**. V dialógovom okne **vyhľadať záznam** sa zobrazia tri pracovné postupy:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Vyberte **ProcessRunCaller** a potom **pridať**.
6. V ďalšom dialógovom okne kliknite na **OK**. Pracovný postup **spánok** je nasledovaný pracovným postupom **proces**.

    Môžete tiež vybrať **processrunner** v kroku 5. Potom, keď vyberiete **OK**, pracovný postup **proces** je nasledovaný pracovným postupom **spánok**.

Pracovné postupy **processruncaller** a **processrunner** vytvárajú faktúry. **ProcessRunCaller** volá **processrunner**. **ProcessRunner** je pracovný postup, ktorý skutočne vytvára faktúry. Prechádza všetky riadky zmluvy, pre ktoré musia byť vytvorené faktúry, a vytvára faktúry pre tieto riadky. Ak chcete určiť riadky zmluvy, pre ktoré musia byť vytvorené faktúry, úloha sa pozerá na dátumy spustenia faktúry pre riadky zmluvy. Ak riadky zmluvy patriace do jednej zmluvy majú rovnaký dátum spustenia faktúry, transakcie sa skombinujú do jednej faktúry, ktorá má dva riadky faktúry. Ak neexistujú žiadne transakcie na vytvorenie faktúr, úloha vynechá vytvorenie faktúry.

Po dokončení **procesrunnera**, sa volá **processruncaller**, ktorý poskytuje čas ukončenia a je uzavretý. **ProcessRunCaller** potom spustí časovač, ktorý beží 24 hodín od zadaného času ukončenia. Na konci časovača, je **processruncaller** uzavretý.

Dávková úloha pre vytváranie faktúr je opakujúca sa úloha. Ak je táto dávková úloha spustená mnohokrát, sú vytvorené viaceré inštancie úlohy a spôsobujú chyby. Preto by ste mali spustiť dávkový proces len raz, a mali by ste ho reštartovať iba v prípade, že prestane fungovať.

> [!NOTE]
> Hromadná fakturácia sa spustí iba pre riadky zmlúv projektu, ktoré sú konfigurované podľa plánov faktúr. Riadok zmluvy s metódou fakturácie podľa fixnej ceny musí mať nakonfigurované medzníky. V riadku zmluvy projektu s metódou fakturácie podľa času a materiálu bude potrebné zostaviť plán fakturácie založený na dátume. To isté platí pre riadok zmluvy založený na projekte.      
 
### <a name="edit-a-draft-invoice"></a>Úprava konceptu faktúry

Pri vytváraní návrhu faktúry projektu, všetky nefakturované predajné transakcie, ktoré boli vytvorené, keď boli schválené zadania času, výdavkov a použitia materiálu, sú stiahnuté na faktúru. Ak je faktúra stále v štádiu návrhu, môžete vykonať nasledujúce úpravy:

- Odstráňte alebo upravte podrobnosti riadka faktúry.
- Editujte a upravte množstvo a typ fakturácie.

Výberom **potvrdiť** potvrďte faktúru. Akcia potvrdiť je jednosmerná akcia. Keď vyberiete možnosť **potvrdiť**, systém urobí faktúru iba na čítanie a vytvorí účtované predajné skutočné hodnoty z každého detailu riadka faktúry pre každý riadok faktúry. Ak podrobnosti riadka faktúry odkazujú na skutočné hodnoty nefakturovaného predaja, systém tiež obnoví skutočné hodntoy nefakturovaného predaja. (Všetky podrobnosti riadka faktúry, ktoré boli vytvorené zo zadania času alebo výdavkov budú odkazovať na skutočné hodnoty nefakturovaného predaja.) Finančné integračné systémy môžu použiť tento zvrat na zvrátenie prebiehajúcej práce projektu (WIP) na účtovné účely.

> [!NOTE]
> Potvrdené faktúry pro forma a súvisiace záznamy, ako sú riadky faktúr a podrobnosti riadkov faktúr, nemožno upravovať ani mazať. 

### <a name="correct-a-confirmed-invoice"></a>Oprava potvrdenej faktúry

Potvrdené faktúry môžu byť editované (opravené). Keď opravíte potvrdenú faktúru, vytvorí sa nový koncept opravnej faktúry. Pretože predpoklad je, že chcete zvrátiť všetky transakcie a množstvá z pôvodnej faktúry, táto opravná faktúra obsahuje všetky transakcie z pôvodnej faktúry a všetky množstvá na nej sú 0 (nula).

Ak niektoré transakcie nevyžadujú opravu, môžete ich odstrániť z konceptu opravnej faktúry. Ak chcete zvrátiť alebo vrátiť iba čiastočné množstvo, môžete upraviť pole **množstvo** v detaile riadka. Ak otvoríte detail riadka faktúry, môžete vidieť pôvodné množstvo faktúry. Potom môžete upraviť aktuálne množstvo faktúr tak, aby bolo menšie ako alebo väčšie ako pôvodné množstvo faktúry.

Po potvrdení opravnej faktúry, sú stornované pôvodné fakturované skutočné hodnoty a sú vytvorené nové fakturované skutočné hodnoty predaja. Ak bolo množstvo znížené, rozdiel spôsobí nové vytvorenie ďalších nefakturovaných skutočných hodnôt predaja. Ak bol napríklad pôvodný fakturovaný predaj osem hodín a detail riadka opravnej faktúry má znížené množstvo šiestich hodín, pôvodný fakturovaný predajný riadok sa vráti späť a vytvoria dve nové skutočné hodnoty:

- Skutočná hodnota fakturovaného predaja je šesť hodín.
- Skutočná hodnota nefakturovaného predaja sú dve hodiny. Táto transakcia môže byť fakturovaná neskôr alebo označená ako nefakturovateľná v závislosti od rokovaní so zákazníkom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
