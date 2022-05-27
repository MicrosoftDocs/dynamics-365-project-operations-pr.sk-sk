---
title: Migrujte plne fakturované míľniky fakturácie pri prerušení
description: Táto téma vysvetľuje, ako migrovať míľniky fakturácie s pevnou cenou, ktoré boli zákazníkovi fakturované za otvorené projektové zmluvy pred dátumom uvedenia do prevádzky.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ccdba864a68521024b2c479c12cf5cea616c5bbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576289"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrujte plne fakturované míľniky fakturácie pri prerušení

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

## <a name="scenario"></a>Scenár

Contoso sa spúšťa s Microsoftom Dynamics 365 Project Operations pre scenáre so zdrojmi/nezásobenými zásobami. V rámci cutover aktivít musí realizačný tím migrovať otvorené projektové zmluvy zo starého systému. Niektoré z projektových zmlúv obsahujú zmluvné linky, ktoré využívajú metódu účtovania s pevnou cenou a už boli čiastočne fakturované koncovému zákazníkovi. Realizačný tím musí migrovať tieto fakturačné míľniky ako **Zákaznícka faktúra zaúčtovaná**, pretože musia byť zahrnuté do celkovej hodnoty zákazky na účely vykazovania výnosov. Zostatky zákazníkov v pohľadávkach a hlavnej knihe však nesmú byť ovplyvnené.

## <a name="solution"></a>Riešenie

### <a name="prerequisites"></a>Požiadavky

- Musí byť nainštalovaný Dynamics 365 Finance 10.0.24 alebo novší.
- Prostredie, v ktorom budú dokončené kroky migrácie, musí byť v režime údržby. Počas migrácie míľnikov by sa nemali vykonávať žiadne iné činnosti.
- Kroky migrácie sa musia dodržať presne tak, ako je tu popísané, a možno ich použiť len na aktivitu prerušenia. Spoločnosť Microsoft nepodporuje žiadne iné použitie tejto schopnosti.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Vytvorte skrátenú verziu míľniky zmluvy o integrácii Project Operations mapy s dvojitým zápisom 

1. Uistite sa, že cieľové mapovanie pre **Míľniky zmluvy o integrácii projektových operácií** subjekt je aktuálny. 

    1. V časti Financie prejdite na **Správa údajov** \> **Dátové entity** a vyberte položku **Míľniky zmluvy o integrácii projektových operácií** subjekt. 
    2. Vyberte **Upravte cieľové mapovania**. 
    3. Na **Zloženie mapy do cieľa** stránku, vyberte **Vytvorte mapovanie** a potom potvrďte, že chcete vygenerovať mapovanie.

2. Zastavte sa a obnovte **Míľniky zmluvy o integrácii projektových operácií** (**msdyn\_ zmluvný plán hodnôt**) mapa s dvojitým zápisom. 

    1. Ísť do **Správa údajov** \> **Dvojité písanie**, vyberte mapu a otvorte jej podrobnosti. 
    2. Vyberte **Stop** a počkajte, kým systém nezastaví mapu. 
    3. Vyberte **Obnoviť tabuľky**.

3. Pridajte mapovanie stavu transakcie.

    1. Vyberte **Pridať mapovanie**.
    2. Na novom riadku, v **Financie a prevádzkové aplikácie** vyberte stĺpec **TRANSSTATUS\[ TRANSSTATUS\]** lúka.
    3. V **Microsoft Dataverse** stĺpec, vyberte **msdyn\_ stav faktúry\[ Stav faktúry\]**.
    4. V **Typ mapy** vyberte šípku vpravo (**\>**).
    5. V dialógovom okne, ktoré sa zobrazí, v **Smer synchronizácie** pole, vyberte **Dataverse do aplikácií pre financie a prevádzku**.
    6. Vyberte **Pridať transformáciu**.
    7. V **Typ transformácie** pole, vyberte **ValueMap**.
    8. Vyberte **Mapovanie pridanej hodnoty**.
    9. Do ľavého poľa zadajte **4**. V pravom poli zadajte **192350001**. 
    10. Vyberte **Uložiť** a potom zatvorte dialógové okno.

4. Vyberte **Uložiť ako** uložiť verziu mapy s dvojitým zápisom. 
5. V **Pridať tabuľku** panel, v **Vydavateľ** pole, vyberte **Predvolený vydavateľ**.
6. V **Verzia** zadajte verziu.
7. V **Popis** zadajte poznámku o tejto výrezovej verzii mapy. 
8. Vyberte **Uložiť**.
9. Spustite mapu.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrujte fakturované míľniky do Dataverse životné prostredie

1. V časti Projektové operácie Dataverse prostredia, vytvorte míľniky, ktoré majú stav faktúry **Pripravené na fakturáciu**. V tejto chvíli nemigrujte žiadne míľniky, ktoré neboli fakturované.

    > [!NOTE]
    > Pred migráciou míľnikov fakturácie sa uistite, že finančné dimenzie súvisiace s riadkom projektovej zmluvy sú nastavené podľa očakávania. Po dokončení migrácie nie je možné upravovať finančné dimenzie.

2. Po migrácii všetkých míľnikov zastavte nasledujúce mapy s dvojitým zápisom:

    - Míľniky zmluvy o integrácii projektových operácií (msdyn\_ zmluvný plán hodnôt)
    - Skutočné hodnoty integrácie Project Operations (msdyn\_actuals)
    - Návrh projektovej faktúry V2 (faktúry)

    Ak chcete zastaviť mapy, postupujte takto:

    1. V časti Financie prejdite na **Správa údajov** \> **Dvojité písanie**, vyberte mapu a otvorte jej podrobnosti.
    2. Vyberte **Stop** a počkajte, kým systém nezastaví mapu.

3. V časti Projektové operácie Dataverse prostredia, vytvárať a potvrdzovať proforma faktúry za fakturačné míľniky. 

    1. Na mape lokality prejdite na zmluvy o projekte, vyberte zmluvy a potom vyberte **Vytvárajte faktúry**.
    2. Po vytvorení faktúr ich otvorte z **faktúry** na mape lokality a potom vyberte **Potvrďte**.

    Tento krok vytvorí požadované záznamy v Dataverse životné prostredie. Nemá to však vplyv na financie a pohľadávky, pretože predtým uvedené mapy s duálnym zápisom boli zastavené.

4. Po potvrdení všetkých proforma faktúr vráťte všetky mapy s duálnym zápisom do pôvodného stavu.

    1. Aktualizujte verziu **Míľniky zmluvy o integrácii projektových operácií** (**msdyn\_ zmluvný plán hodnôt**) mapa s dvojitým zápisom späť na originál. 
    2. Vyberte mapu s dvojitým zápisom v zozname máp, vyberte **Verzia stolovej mapy** a potom vyberte pôvodnú verziu mapy tabuľky.
    3. Vyberte **Uložiť**.
    4. Reštartujte nasledujúce mapy s dvojitým zápisom:

        - Míľniky zmluvy o integrácii projektových operácií (msdyn\_ zmluvný plán hodnôt)
        - Skutočné hodnoty integrácie Project Operations (msdyn\_actuals)
        - Návrh projektovej faktúry V2 (faktúry)

Míľniky sú teraz migrované a systém je pripravený na ďalšie kroky v aktivite prerušenia.
