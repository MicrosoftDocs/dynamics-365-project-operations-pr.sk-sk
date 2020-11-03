---
title: Vytvorenie vlastných polí a entít ako cenových dimenzií
description: Táto téma poskytuje informácie o tom, ako vytvoriť vlastné množiny možností alebo entity.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084402"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Vytvorenie vlastných polí a entít ako cenových dimenzií

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Vykonajte nasledujúce kroky kedykoľvek, kedy chcete vytvoriť vlastnú množinu možností alebo entitu.

> [!IMPORTANT]
> Odporúčame, aby ste robili všetky zmeny cenových dimenzií v samostatnom riešení. Táto dôležitá najlepšia prax poskytuje flexibilitu v budúcnosti na aktualizáciu alebo odstránenie zmien podľa potreby, pomôže pri opätovnom použití vašej práce a uľahčuje port týchto zmien na inú inštanciu. Potom, čo ste vykonali všetky požadované zmeny, exportujte toto riešenie ako **spravované riešenie** a importujte ho do iných inštancií na opätovné použitie nastavení cien.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Vytvorenie vlastného riešenia pre dimenzie cien
1. Prejdite do ponuky **Nastavenia** > **Riešenia** a potom vyberte **Nové** , ak chcete vytvoriť nové riešenie. 
2. Pomenujte riešenie, **dimenzie cien \<your organization name>** , zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Vytvorte vlastné polia a množiny možností v riešení dimenzie ceny

Cenový rozmer môže byť množina možností alebo entita. Obidva musia byť vytvorené vo vašom cenovom riešení. Postup v tomto procese vysvetľuje, ako vytvoriť dimenzie založené na entite a dimenzie založené na množine možností.

### <a name="entity-based-dimensions"></a>Dimenzie založené na entite

1. Prejdite do ponuky **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**.
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity**.
3. Vyberte **Nové** , ak chcete vytvoriť novú entitu s názvom **Štandardný nadpis**. 
4. Zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.


### <a name="option-set-based-dimensions"></a>Dimenzie založené na množine možností 
Môžete vytvoriť dve dimenzie založené na množine možností. Použite **miesto pracovného prostriedku** na sledovanie ceny na **domácom** mieste práce a **na mieste** práce a používania **zdrojových pracovných hodín** s hodnotami **pravidelný** a **nadčasy** ak chcete použiť značku pri dokončení práce.


1. Prejdite do ponuky **Nastavenia** > **Riešenia** a dvakrát kliknite na **Dimenzie cien \<your organization name>**. 
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Množina možností**. 
3. Vyberte **Nové** , ak chcete vytvoriť novú množinu možností, zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.

## <a name="create-data-for-entity-based-dimensions"></a>Vytvorenie údajov pre dimenzie založené na entite

Údaje pre dimenzie založené na entite môžete vytvoriť manuálne alebo pomocou Microsoft Excel importu alebo služobných hovorov. Použite kroky v tomto postupe na vytvorenie dvoch štandardných titulov, **systémový inžinier** a **starší systémový inžinier** z dimenzie založenej na entite, **štandardný nadpis**. Ak sú údaje, ktoré chcete vytvoriť, malé, ako je to v nasledovnom príklade, môžete použiť štandardný formulár.

1. Vyberte **Rozšírené vyhľadávanie** , vyberte entitu **Štandardný názov** a potom vyberte **Výsledky**. Zobrazia sa všetky riadky v entite **štandardnej** nadpisu.
2. Vyberte **Nový** , v poli **Názov** zadajte „Systémový inžinier“ a potom vyberte **Uložiť**.
3. Zatvorí formulár. 
4. Opakujte kroky 1 - 3 na vytvorenie ďalšieho štandardného názvu pre "Starší Systémový inžinier".

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Pridajte všetky požadované entity a súvisiace súčasti do riešenia Dimenzia ceny
Budete musieť pridať nasledujúce entity do vášho cenového riešenia. Postupujte podľa krokov v tomto postupe, tak aby sa niektoré dôležité zmeny schémy v cenovom riešení tak, že entity sa dozvedia o nových cenových dimenziách.

1. Vyberte **Nastavenia** > **Riešenia** a dvakrát kliknite na **Dimenzie cien \<your organization name>**. 
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Pridať existujúce** > **Entity**.
3. V dialógovom okne **súčasti riešenia** vyberte nasledujúce entity:

  - Skutočná hodnota
  - Rezervovateľný zdroj
  - Riadok odhadu
  - Podrobnosti o riadku faktúry
  - Záznam v účtovnom denníku
  - Podrobnosti o riadku projektovej zmluvy
  - Člen projektového tímu
  - Podrobnosti o riadku cenovej ponuky
  - Prirážka k cene roly
  - Cena roly 
  - Zadanie času 


> [!NOTE]
> Nezabudnite zahrnúť všetky formuláre a zobrazenia pre každú vybranú entitu.

4. Keď sa zobrazí výzva na zahrnutie všetkých závislých entít pre entity vybraté vyššie, vyberte **Nie**.

