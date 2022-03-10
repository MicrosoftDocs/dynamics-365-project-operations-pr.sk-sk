---
title: Vytvorenie vlastných polí a entít ako cenových dimenzií
description: Táto téma poskytuje informácie o tom, ako vytvoriť vlastné množiny možností alebo entity.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 40a6a4173cb0e4d7ea5bcf24c8954fe9d7e079d1e9ecf4aac252b5133f12d3ff
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003655"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Vytvorenie vlastných polí a entít ako cenových dimenzií

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Vykonajte nasledujúce kroky vždy, keď chcete vytvoriť vlastnú množinu možností alebo entitu, ktorú budete používať ako cenovú dimenziu. Ďalšie informácie sa dozviete v článku [Prehľad cenových dimenzií](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Odporúčame, aby ste robili všetky zmeny cenových dimenzií v samostatnom riešení. Tento dôležitý najlepší postup poskytuje v budúcnosti flexibilitu pri aktualizácii alebo odstraňovaní zmien podľa potreby. To tiež pomôže pri opätovnom použití vašej práce a uľahčí prenos týchto zmien do inej inštancie. Po vykonaní všetkých požadovaných zmien exportujte toto riešenie ako **spravované riešenie** a importujte ho do iných inštancií, aby ste mohli znova použiť nastavenie cien.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Vytvorte vlastné polia a množiny možností v riešení dimenzie ceny

Cenový rozmer môže byť množina možností alebo entita. Obidva musia byť vytvorené vo vašom cenovom riešení. Postup v tomto procese vysvetľuje, ako vytvoriť dimenzie založené na entite a dimenzie založené na množine možností.

### <a name="entity-based-dimensions"></a>Dimenzie založené na entite
Ak chcete vytvoriť dimenzie založené na entitách, postupujte takto:

1. Prejdite do ponuky **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**.
2. V prehľadávači riešení, na ľavom navigačnom paneli, vyberte **Entity**.
3. Vyberte **Nové**, ak chcete vytvoriť novú entitu s názvom **Štandardný nadpis**. 
4. Zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.

> ![Definícia entity Štandardný názov.](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimenzie založené na množine možností 
Môžete vytvoriť dve dimenzie založené na množine možností. 

- Použite **Miesto pracovného zdroja** na sledovanie ceny miesta práce **Doma** a práce **Na mieste**. 
- Použite **Pracovná doba zdrojov** s hodnotami **Pravidelná** a **Nadčasy** na aplikovanie prirážky, keď je práca dokončená.

Nasledujúca grafika poskytuje pohľad na dimenziu **Miesto pracovného zdroja**. 

> ![Množina možností na základe cenovej dimenzie nazvanej Pracovná poloha zdroja.](media/Option-set-PD-called-Resource-Work-Location.png)

Nasledujúca grafika poskytuje pohľad na dimenziu **Pracovná doba zdroja**. 

> ![Množina možností na základe cenovej dimenzie nazvanej Pracovná doba zdroja.](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Prejdite do ponuky **Nastavenia** > **Riešenia** a dvakrát kliknite na **Dimenzie cien \<your organization name>**. 
2. V prehľadávači riešení, na ľavom navigačnom paneli, vyberte **Množinu možností**. 
3. Vyberte **Nové**, ak chcete vytvoriť novú množinu možností, zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.

## <a name="create-data-for-entity-based-dimensions"></a>Vytvorenie údajov pre dimenzie založené na entite

Údaje pre dimenzie založené na entite môžete vytvoriť manuálne alebo pomocou Microsoft Excel importu alebo služobných hovorov. Použite kroky v tomto postupe na vytvorenie dvoch štandardných titulov, **systémový inžinier** a **starší systémový inžinier** z dimenzie založenej na entite, **štandardný nadpis**. Ak sú údaje, ktoré chcete vytvoriť, malé, ako je to v nasledovnom príklade, môžete použiť štandardný formulár.

1. Vyberte **Rozšírené vyhľadávanie**.
2. Vyberte entitu **Štandardný nadpis** a potom vyberte **Výsledky**. Zobrazia sa všetky riadky v entite **štandardnej** nadpisu.
3. Vyberte **Nový**, v poli **Názov** zadajte „Systémový inžinier“ a potom vyberte **Uložiť**.
4. Zatvorí stránku. 
5. Opakujte kroky 1 - 3 na vytvorenie ďalšieho štandardného názvu pre "Starší Systémový inžinier".

> ![Vzorové údaje pre entitu Štandardný nadpis.](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]