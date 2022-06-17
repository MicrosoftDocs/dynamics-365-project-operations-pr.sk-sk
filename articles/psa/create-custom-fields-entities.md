---
title: Vytvorte vlastné polia a entity
description: Tento článok vysvetľuje, ako vytvoriť sady možností a entity vo vašom vlastnom riešení v Power Apps plošina.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 3b6f675d604f3b6a6f2465c413ceff3d16815e12
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926933"
---
# <a name="create-custom-fields-and-entities"></a>Vytvorte vlastné polia a entity 

[!include [banner](../includes/psa-now-project-operations.md)]

Dokončite nasledujúce kroky kedykoľvek, kedy chcete vytvoriť vlastnú množinu možností alebo entitu na Power Apps platforme.  
Postupy v tomto článku by sa mali vykonávať pomocou webového rozhrania Project Service Automation (PSA).

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
