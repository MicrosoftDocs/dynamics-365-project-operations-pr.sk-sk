---
title: Fakturácia v Project Service Automation
description: Táto téma poskytuje informácie o fakturácii.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365  Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 8d95f17aba0a4cab65a6f020aade5e19568de3be
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755510"
---
# <a name="invoicing-in-project-service-automation"></a>Fakturácia v Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Fakturácia v Dynamics 365 Project Service Automation je užitočná, pretože poskytuje projektovým manažérom druhú úroveň schválenia pred vytvorením faktúr pre zákazníkov. Prvá úroveň schválenia sa dokončí, keď sú schválené zadania času a výdavkov, ktoré predkladajú členovia projektového tímu.

PSA nie je navrhnutý tak, aby generoval faktúry orientované na zákazníka z nasledujúcich dôvodov:

- Neobsahuje daňové informácie.
- Nie je možné konvertovať iné meny do fakturačnej meny pomocou správne nakonfigurovaných výmenných kurzov.
- Nie je možné správne formátovať faktúry tak, aby mohli byť vytlačené.

Namiesto toho môžete použiť finančný alebo účtovný systém na vytváranie faktúr orientovaných zákazníkom, ktoré používajú informácie z návrhov faktúr, ktoré sú generované v PSA.

## <a name="creating-project-invoices-in-psa"></a>Vytváranie projektových faktúr v PSA

Projektové faktúry možno vytvoriť po jednom alebo hromadne. Môžete ich vytvoriť manuálne, alebo môžu byť nakonfigurované tak, aby boli generované v automatizovaných spusteniach.

### <a name="manually-create-project-invoices-in-psa"></a>Vytvorte projektové faktúry v PSA manuálne

Na stránke **Projektové zlmuvy** môžete vytvoriť projektové faktúry samostatne pre každú projektovú zmluvu, alebo môžete hromadne vytvárať faktúry pre viacero projektových zmlúv.

Ak chcete vytvoriť faktúru pre konkrétnu projektovú zmluvu, postupujte podľa tohto kroku.

- Na stránke zoznam **projektových zmlúv** otvorte zmluvu o projekte a potom vyberte položku **vytvoriť faktúru**.

    ![Vytváranie projektových faktúr pre konkrétnu projektovú zmluvu](media/CreateProjectInvoicesOneByOne.png)

    Faktúra sa generuje pre všetky transakcie vybratej projektovej zmluvy, ktoré majú stav **pripravené na fakturáciu**. Tieto transakcie zahŕňajú čas, výdavky, míľniky a riadky zmluvy založené na produkte.

Ak chcete hromadne vytvárať faktúry, postupujte podľa týchto krokov.

1. Na stránke zoznam **projektových zmlúv** vyberte jednu alebo viacero projektových zmlúv, pre ktoré musíte vytvoriť faktúru, a potom vyberte položku **vytvoriť projektové faktúry.**

    ![Hromadné vytváranie projektových faktúr](media/CreateProjectInvoicesBulk.png)

    Upozorňujúce hlásenie vás informuje o tom, že pred tým, ako sa vytvoria faktúry, môže dôjsť k oneskoreniu. Tento proces je tiež zobrazený.

2. Stlačením **OK** zatvorte dialógové okno.

    Faktúra sa generuje pre všetky transakcie v riadku projektovej zmluvy, ktoré majú stav **pripravené na fakturáciu**. Tieto transakcie zahŕňajú čas, výdavky, míľniky a riadky zmluvy založené na produkte.

3. Ak chcete zobraziť faktúry, ktoré sú generované, prejdite na **Predaj** \> **fakturácia** \> **faktúry**. Pre každú zmluvu o projekte uvidíte jednu faktúru.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Nastavenie automatického vytvárania projektových faktúr v PSA

Ak chcete nakonfigurovať automatické vytváranie faktúr v PSA, postupujte podľa týchto krokov.

1. Prejdite do ponuky **Project Service** \> **Nastavenia** \> **dávkové úlohy**.
2. Vytvorte dávkovú úlohu a pomenujte ju **PSA vytvoriť faktúry**. Názov dávkovej úlohy musí obsahovať výraz "Vytvoriť faktúry".
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
 
### <a name="edit-a-draft-psa-invoice"></a>Úprava konceptu faktúry PSA

Pri vytváraní návrhu faktúry projektu, všetky nefakturované predajné transakcie, ktoré boli vytvorené, keď boli schválené zadania času a výdavkov sú stiahnuté na faktúru. Ak je faktúra stále v štádiu návrhu, môžete vykonať nasledujúce úpravy:

- Odstráňte alebo upravte podrobnosti riadka faktúry.
- Editujte a upravte množstvo a typ fakturácie.
- Priamo pridajte čas, náklady a poplatky ako transakcie na faktúre. Túto funkciu môžete použiť, ak je riadok faktúry priradený k riadku zmluvy, ktorý umožňuje tieto triedy transakcií.

Výberom **potvrdiť** potvrďte faktúru. Akcia potvrdiť je jednosmerná akcia. Keď vyberiete možnosť **potvrdiť**, systém urobí faktúru iba na čítanie a vytvorí účtované predajné skutočné hodnoty z každého detailu riadka faktúry pre každý riadok faktúry. Ak podrobnosti riadka faktúry odkazujú na skutočné hodnoty nefakturovaného predaja, systém tiež obnoví skutočné hodntoy nefakturovaného predaja. (Všetky podrobnosti riadka faktúry, ktoré boli vytvorené zo zadania času alebo výdavkov budú odkazovať na skutočné hodnoty nefakturovaného predaja.) Finančné integračné systémy môžu použiť tento zvrat na zvrátenie prebiehajúcej práce projektu (WIP) na účtovné účely.

### <a name="correct-a-confirmed-psa-invoice"></a>Oprava povrdenej PSA faktúry

Potvrdené faktúry PSA môžu byť editované (opravené). Keď opravíte potvrdenú faktúru, vytvorí sa nový koncept opravnej faktúry. Pretože predpoklad je, že chcete zvrátiť všetky transakcie a množstvá z pôvodnej faktúry, táto opravná faktúra obsahuje všetky transakcie z pôvodnej faktúry a všetky množstvá na nej sú 0 (nula).

Ak niektoré transakcie nevyžadujú opravu, môžete ich odstrániť z konceptu opravnej faktúry. Ak chcete zvrátiť alebo vrátiť iba čiastočné množstvo, môžete upraviť pole **množstvo** v detaile riadka. Ak otvoríte detail riadka faktúry, môžete vidieť pôvodné množstvo faktúry. Potom môžete upraviť aktuálne množstvo faktúr tak, aby bolo menšie ako alebo väčšie ako pôvodné množstvo faktúry.

Po potvrdení opravnej faktúry, sú stornované pôvodné fakturované skutočné hodnoty a sú vytvorené nové fakturované skutočné hodnoty predaja. Ak bolo množstvo znížené, rozdiel spôsobí nové vytvorenie ďalších nefakturovaných skutočných hodnôt predaja. Ak bol napríklad pôvodný fakturovaný predaj osem hodín a detail riadka opravnej faktúry má znížené množstvo šiestich hodín, PSA obnoví pôvodný fakturovaný predajný riadok a vytvorí dve nové skutočné hodnoty:

- Skutočná hodnota fakturovaného predaja je šesť hodín.
- Skutočná hodnota nefakturovaného predaja sú dve hodiny. Táto transakcia môže byť fakturovaná neskôr alebo označená ako nefakturovateľná v závislosti od rokovaní so zákazníkom.
