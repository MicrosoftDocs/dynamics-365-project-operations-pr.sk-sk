---
title: Priradenie všeobecných rezervovateľných zdrojov k úlohe a projektovému tímu
description: Táto téma poskytuje informácie o rezervovaní všeobecných zdrojoch pre úlohy a projektové tímy.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f461fbd3-1fce-4aeb-a896-a6d14453a5a4
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 82478e2cf97ab03e80e9f5fbb662b3603d5905b9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755681"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Priradenie všeobecných rezervovateľných zdrojov k úlohe a generovanie zdrojových požiadaviek 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Okrem rezervácie a priraďovania pomenovaných alebo skutočných zdrojov do vášho projektu môžete priradiť všeobecné zdroje k úlohám projektu. Tieto zdroje môžu slúžiť ako zástupné symboly pre pomenované zdroje, kým nie ste pripravení na zamestnanie vášho projektu s pomenovaním zdrojov. 

1. V Project Service Automation (PSA), otvorte stránku **Project** a na karte **Schedule**, zadajte názov pozície všeobecného prostriedku v bunke plánu **Resource**. Alebo kliknite na ikonu **Resource** v bunke k otvoreniu výberu zdrojov a potom zadajte názov všeobecného prostriedku, ktorý chcete vytvoriť.

![Vytvorenie a priradenie všeobecného člena tímu](media/RM-how-to-9.png)

Otvorí sa panel **Quick Create: Project Team Member**. 

2. Zadajte rolu a organizačnú jednotku člena tímu všeobecného zdroja a kliknite na tlačidlo **Save**.

![Rýchle vytvorenie všeobecného člena tímu](media/RM-how-to-10.png)

3. Po vytvorení nového člena tímu všeobecného zdroja, je priradený k úlohe. Môžete pokračovať v priraďovaní tohto všeobecného zdroja k iným úlohám v pláne úloh.

![Priradenie existujúceho všeobecného člena tímu k úlohám](media/RM-how-to-11.png)

4. Po priradení všeobecného zdroja môžete vygenerovať zdrojovú požiadavku a naplniť ju priamo rezerváciou alebo odoslaním zdrojovej požiadavky správcovi prostriedkov.

![Generovanie požiadavky na všeobecného člena tímu](media/RM-how-to-12.png)

Na mriežke člena tímu, okrem toho, že je možné použiť výber zdrojov, ako je uvedené vyššie, môžete pridať všeobecné zdroje priamo. Prostriedky sa pridávajú so zdrojovou požiadavkou, ktorá je založená na start/end dátumoch a metóde pridelenia zadanej v paneli **Quick Create: Project Team Member**.

Môžete vidieť rozdiel, ak pridáte všeobecného člena tímu priamo a potom priradíte viac úloh na všeobecný zdroj, ako majú požadovaných hodín na pokrytie. Kliknite na **Generate Requirement** na regeneráciu požiadavky na vyváženie požadovaných hodín proti priradeniam.

Môžete tiež kliknúť na **Resource requirement** odkaz v tímovej mriežke na otvorenie požiadavky a pridanie zručnosti, preferované zdroje, atď.

![Požiadavka na zdroj](media/RM-how-to-13.png)

