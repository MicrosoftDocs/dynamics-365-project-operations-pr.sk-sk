---
title: Vytvorte vlastné polia a entity
description: Táto téma vysvetľuje, ako vytvoriť množiny možností a entity vo vlastnom riešení v platforme Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f501bcc106a296f35bba996b6ab3a8b758cefb1926033faf04ee23c42bc94d39
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992450"
---
# <a name="create-custom-fields-and-entities"></a>Vytvorte vlastné polia a entity 

[!include [banner](../includes/psa-now-project-operations.md)]

Dokončite nasledujúce kroky kedykoľvek, kedy chcete vytvoriť vlastnú množinu možností alebo entitu na Power Apps platforme.  
Postupy v tejto téme by mali byť dokončené pomocou webového rozhrania Project Service Automation (PSA).

> [!IMPORTANT]
> Odporúčame, aby ste robili všetky zmeny cenových dimenzií v samostatnom riešení. Táto dôležitá najlepšia prax poskytuje flexibilitu v budúcnosti na aktualizáciu alebo odstránenie zmien podľa potreby, pomôže pri opätovnom použití vašej práce a uľahčuje port týchto zmien na inú inštanciu. Potom, čo ste vykonali všetky požadované zmeny, exportujte toto riešenie ako **spravované riešenie** a importujte ho do iných inštancií na opätovné použitie nastavení cien.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Vytvorte vlastné polia a množiny možností v riešení dimenzie ceny

Cenový rozmer môže byť množina možností alebo entita. Obidva musia byť vytvorené vo vašom cenovom riešení. Postup v tomto procese vysvetľuje, ako vytvoriť dimenzie založené na entite a dimenzie založené na množine možností.

### <a name="entity-based-dimensions"></a>Dimenzie založené na entite

1. V PSA kliknite na položku **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**.
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity**.
3. Kliknite na **nové**, ak chcete vytvoriť novú entitu s názvom **štandardný nadpis**. Zadajte zostávajúce požadované informácie a kliknite na **Uložiť**.

> ![Definícia entity Štandardný názov.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimenzie založené na množine možností 
Môžete vytvoriť dve dimenzie založené na množine možností. Použite **miesto pracovného prostriedku** na sledovanie ceny na **domácom** mieste práce a **na mieste** práce a používania **zdrojových pracovných hodín** s hodnotami **pravidelný** a **nadčasy** ak chcete použiť značku pri dokončení práce.


1. V PSA kliknite na položku **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**. 
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Množina možností**. 
3. Kliknite na **nové**, ak chcete vytvoriť novú množinu možností, zadajte zostávajúce požadované informácie a potom kliknite na **uložiť**.

> ![Množina možností na základe cenovej dimenzie nazvanej Pracovná poloha zdroja.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Množina možností na základe cenovej dimenzie nazvanej Pracovná doba zdroja.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Vytvorenie údajov pre dimenzie založené na entite

Údaje pre dimenzie založené na entite môžete vytvoriť manuálne alebo pomocou Microsoft Excel importu alebo služobných hovorov. Použite kroky v tomto postupe na vytvorenie dvoch štandardných titulov, **systémový inžinier** a **starší systémový inžinier** z dimenzie založenej na entite, **štandardný nadpis**. Ak sú údaje, ktoré chcete vytvoriť, malé, ako je to v nasledovnom príklade, môžete použiť štandardný formulár.

1. V PSA kliknite na **Rozšírené vyhľadávanie**. Vyberte entitu **štandardný nadpis** a potom kliknite na **výsledky**. Zobrazia sa všetky riadky v entite **štandardnej** nadpisu.
2. Kliknite na položku **Nový**. V poli **Názov** zadajte text " Systémový inžinier" a potom kliknite na tlačidlo **Uložiť**.
3. Zavrite formulár. 
4. Opakujte kroky 1 - 3 na vytvorenie ďalšieho štandardného názvu pre "Starší Systémový inžinier".

> ![Vzorové údaje pre entitu Štandardný nadpis.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]