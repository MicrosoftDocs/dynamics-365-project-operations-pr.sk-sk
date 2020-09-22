---
title: Vytvorte vlastné polia a entity
description: Táto téma vysvetľuje, ako vytvoriť množiny možností a entity vo vlastnom riešení v platforme Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755651"
---
# <a name="create-custom-fields-and-entities"></a>Vytvorte vlastné polia a entity 

Dokončite nasledujúce kroky kedykoľvek, kedy chcete vytvoriť vlastnú množinu možností alebo entitu na Power Apps platforme.  
Postupy v tejto téme by mali byť dokončené pomocou webového rozhrania Project Service Automation (PSA).

> [!IMPORTANT]
> Odporúčame, aby ste robili všetky zmeny cenových dimenzií v samostatnom riešení. Táto dôležitá najlepšia prax poskytuje flexibilitu v budúcnosti na aktualizáciu alebo odstránenie zmien podľa potreby, pomôže pri opätovnom použití vašej práce a uľahčuje port týchto zmien na inú inštanciu. Potom, čo ste vykonali všetky požadované zmeny, exportujte toto riešenie ako **spravované riešenie** a importujte ho do iných inštancií na opätovné použitie nastavení cien.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Vytvorenie vlastného riešenia pre dimenzie cien
1. V PSA, kliknite na **nastavenia** > **riešenia** a potom kliknite na **nové** ak chcete vytvoriť nové riešenie. 
2. Pomenujte riešenie, **\<názov vašej organizácie>dimenzie cien**, zadajte zostávajúce požadované informácie a potom kliknite na tlačidlo **Uložiť**.

> ![Vytvorenie vlastného riešenia pre dimenzie cien](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Vytvorte vlastné polia a množiny možností v riešení dimenzie ceny

Cenový rozmer môže byť množina možností alebo entita. Obidva musia byť vytvorené vo vašom cenovom riešení. Postup v tomto procese vysvetľuje, ako vytvoriť dimenzie založené na entite a dimenzie založené na množine možností.

### <a name="entity-based-dimensions"></a>Dimenzie založené na entite

1. V PSA, kliknite na **nastavenia** > **riešenia** a potom dvojklik na **\<názov vašej organizácie> cenové dimenzie**.
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity**.
3. Kliknite na **nové**, ak chcete vytvoriť novú entitu s názvom **štandardný nadpis**. Zadajte zostávajúce požadované informácie a kliknite na **Uložiť**.

> ![Definícia entity so Štandardným nadpisom](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimenzie založené na množine možností 
Môžete vytvoriť dve dimenzie založené na množine možností. Použite **miesto pracovného prostriedku** na sledovanie ceny na **domácom** mieste práce a **na mieste** práce a používania **zdrojových pracovných hodín** s hodnotami **pravidelný** a **nadčasy** ak chcete použiť značku pri dokončení práce.


1. V PSA, kliknite **nastavenia** > **riešenia** a potom dvojklik na **\<názov vašej organizácie> cenové dimenzie**. 
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Množina možností**. 
3. Kliknite na **nové**, ak chcete vytvoriť novú množinu možností, zadajte zostávajúce požadované informácie a potom kliknite na **uložiť**.

> ![Množina možností na základe cenovej dimenzie nazvanej pracovná poloha zdroja ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Množina možností na základe cenovej dimenzie nazvanej hodinová poloha zdroja ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Vytvorenie údajov pre dimenzie založené na entite

Údaje pre dimenzie založené na entite môžete vytvoriť manuálne alebo pomocou Microsoft Excel importu alebo služobných hovorov. Použite kroky v tomto postupe na vytvorenie dvoch štandardných titulov, **systémový inžinier** a **starší systémový inžinier** z dimenzie založenej na entite, **štandardný nadpis**. Ak sú údaje, ktoré chcete vytvoriť, malé, ako je to v nasledovnom príklade, môžete použiť štandardný formulár.

1. V PSA kliknite na **Rozšírené vyhľadávanie**. Vyberte entitu **štandardný nadpis** a potom kliknite na **výsledky**. Zobrazia sa všetky riadky v entite **štandardnej** nadpisu.
2. Kliknite na položku **Nový**. V poli **Názov** zadajte text " Systémový inžinier" a potom kliknite na tlačidlo **Uložiť**.
3. Zavrite formulár. 
4. Opakujte kroky 1 - 3 na vytvorenie ďalšieho štandardného názvu pre "Starší Systémový inžinier".

> ![Vzorové údaje pre štandardný nadpis entity. ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Pridajte všetky požadované entity PSA a súvisiace súčasti do riešenia dimenzie ceny
Budete musieť pridať nasledujúce entity služby Project Service na vaše cenové riešenie. Postupujte podľa krokov v tomto postupe, tak aby sa niektoré dôležité zmeny schémy v cenovom riešení tak, že entity sa dozvedia o nových cenových dimenziách.

1. V PSA, kliknite na **nastavenia** > **riešenia** a potom dvojklik na **\<názov vašej organizácie> cenové dimenzie**. 
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

> ![Pridanie existujúcich entít do riešenia cenových dimenzií](media/Existing-entities-to-PD-solution.png)

> ![Výber súčastí riešenia](media/Dimension-Components.png)

> [!NOTE]
> Nezabudnite zahrnúť všetky formuláre a zobrazenia pre každú vybranú entitu.

4. Keď sa zobrazí výzva na zahrnutie všetkých závislých entít pre entity vybraté vyššie, kliknite na **nie**.

> ![Nezahrnúť súvisiace súčasti](media/Do-not-include-required.png)


