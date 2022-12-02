---
title: Migrácia plne fakturovaných míľnikov fakturácie počas prepnutia
description: Tento článok vysvetľuje, ako migrovať míľniky fakturácie s pevnou cenou, ktoré boli zákazníkovi fakturované za otvorené projektové zmluvy pred dátumom uvedenia do prevádzky.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028721"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrácia plne fakturovaných míľnikov fakturácie počas prepnutia

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

## <a name="scenario"></a>Scenár

Spoločnosť Contoso začne používať Microsoft Dynamics 365 Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách. V rámci aktivít prepnutia musí realizačný tím migrovať otvorené projektové zmluvy zo starého systému. Niektoré z projektových zmlúv obsahujú riadky zmlúv, ktoré využívajú metódu účtovania s pevnou cenou a už boli čiastočne fakturované koncovému zákazníkovi. Realizačný tím musí migrovať tieto fakturačné míľniky ako **Faktúra pre zákazníka bola zaúčtovaná**, pretože musia byť zahrnuté do celkovej hodnoty zmluvy na účely vykazovania výnosov. Zostatky zákazníkov v pohľadávkach a hlavnej účtovnej knihe však nesmú byť ovplyvnené.

## <a name="solution"></a>Riešenie

### <a name="prerequisites"></a>Požiadavky

- Musí byť nainštalovaný Dynamics 365 Finance 10.0.24 alebo novší.
- Prostredie, v ktorom budú dokončené kroky migrácie, musí byť v režime údržby. Počas migrácie míľnikov by sa nemali vykonávať žiadne iné činnosti.
- Kroky migrácie sa musia dodržať presne tak, ako je tu popísané, a možno ich použiť len na aktivitu prepnutia. Spoločnosť Microsoft nepodporuje žiadne iné použitie tejto funkcie.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Vytvorenie prepínacej verzie mapy duálneho zápisu pre míľniky integrácie riadka zmluvy Project Operations 

1. Uistite sa, že cieľové mapovanie pre entitu **Míľniky integrácie riadka zmluvy Project Operations** je aktuálna. 

    1. Vo Finance prejdite na **Správa údajov** \> **Dátové entity** a vyberte položku **Míľniky integrácie riadka zmluvy Project Operations**. 
    2. Vyberte **Upraviť cieľové mapovania**. 
    3. Na stránke **Mapovanie etapy do cieľa** vyberte **Generovať mapovanie** a potom potvrďte, že chcete vygenerovať mapovanie.

2. Zastavte a obnovte mapu duálneho zápisu **Míľniky integrácie riadka zmluvy Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Prejdite do **Správa údajov** \> **Duálny zápis**, vyberte mapu a otvorte jej podrobnosti. 
    2. Vyberte **Stop** a počkajte, kým systém nezastaví mapu. 
    3. Vyberte **Obnoviť tabuľky**.

3. Pridajte mapovanie pre stav transakcie.

    1. Vyberte **Pridať mapovanie**.
    2. Na novom riadku, v stĺpci **Aplikácie na riadenie financií a prevádzok** vyberte pole **TRANSSTATUS \[TRANSSTATUS\]**.
    3. V stĺpci **Microsoft Dataverse** vyberte **msdyn\_invoicestatus \[Invoice status\]**.
    4. V stĺpci **Typ mapy** vyberte šípku doprava (**\>**).
    5. V dialógovom okne, ktoré sa zobrazí, v poli **Smer synchronizácie**, vyberte **Dataverse do aplikácií na riadenie financií a prevádzok**.
    6. Vyberte **Pridať transformáciu**.
    7. V poli **Typ transformácie** vyberte položku **ValueMap**.
    8. Vyberte **Pridať mapovanie hodnoty**.
    9. V ľavom poli s hodnotou zadajte **4**. V pravom poli s hodnotou zadajte **192350001**. 
    10. Kliknite na položku **Uložiť** a potom zatvorte dialógové okno.

4. Vyberte **Uložiť ako** a uložte verziu mapy duálneho zápisu. 
5. Na table **Pridať tabuľku** v poli **Vydavateľ** vyberte **Predvolený vydavateľ**.
6. V poli **Verzia** zadajte verziu.
7. V poli **Popis** zadajte poznámku o tejto prepínacej verzii mapy. 
8. Vyberte **Uložiť**.
9. Spustite mapu.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrácia fakturovaných míľnikov do prostredia Dataverse

1. V prostredí Project Operations Dataverse vytvorte míľniky, ktoré majú stav faktúry **Pripravené na fakturáciu**. V tejto chvíli nemigrujte žiadne míľniky, ktoré neboli fakturované.

    > [!NOTE]
    > Pred migráciou míľnikov fakturácie sa uistite, že finančné dimenzie súvisiace s riadkom projektovej zmluvy sú nastavené podľa očakávania. Po dokončení migrácie nie je možné upravovať finančné dimenzie.

2. Po migrácii všetkých míľnikov zastavte nasledujúce mapy duálneho zápisu:

    - Míľniky integrácie riadka zmluvy Project Operations (msdyn\_contractlinescheduleofvalues)
    - Skutočné hodnoty integrácie Project Operations (msdyn\_actuals)
    - Návrh projektovej faktúry V2 (faktúry)

    Na zastavenie máp postupujte takto:

    1. V Finance prejdite do **Správa údajov** \> **Duálny zápis**, vyberte mapu a otvorte jej podrobnosti.
    2. Vyberte **Stop** a počkajte, kým systém nezastaví mapu.

3. V prostredí Project Operations Dataverse môžete vytvárať a potvrdzovať proforma faktúry za fakturačné míľniky. 

    1. Na mape lokality prejdite do projektových zmlúv, vyberte zmluvy a potom vyberte **Vytvárať faktúry**.
    2. Po vytvorení faktúr ich otvorte z ponuky **Faktúry** na mape lokality a potom vyberte **Potvrdiť**.

    Tento krok vytvorí požadované záznamy v prostredí Dataverse. Nemá to však vplyv na financie a pohľadávky, pretože predtým uvedené mapy duálneho zápisu boli zastavené.

4. Po potvrdení všetkých proforma faktúr vráťte všetky mapy duálneho zápisu do pôvodného stavu.

    1. Aktualizujte verziu mapy duálneho zápisu **Míľniky integrácie riadka zmluvy Project Operations** (**msdyn\_contractlinescheduleofvalues**) späť na originál. 
    2. Vyberte mapu duálneho zápisu v zozname máp, vyberte **Verzia mapy tabuľky** a potom vyberte pôvodnú verziu mapy tabuľky.
    3. Vyberte **Uložiť**.
    4. Reštartujte nasledujúce mapy duálneho zápisu:

        - Míľniky integrácie riadka zmluvy Project Operations (msdyn\_contractlinescheduleofvalues)
        - Skutočné hodnoty integrácie Project Operations (msdyn\_actuals)
        - Návrh projektovej faktúry V2 (faktúry)

Míľniky sú teraz migrované a systém je pripravený na ďalšie kroky v aktivite prepnutia.
