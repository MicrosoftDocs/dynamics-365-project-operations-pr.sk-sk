---
title: Vytvoriť zadanie času
description: Táto téma poskytuje informácie o tom, ako vytvoriť zadania času.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0d0e21d0964788564d3db9173c3a0b3378cd0049b4455a23ccc1bccd1c21d9e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990425"
---
# <a name="create-time-entries"></a>Vytvoriť zadanie času

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V predchádzajúcich verziách Dynamics 365 Project Service Automation boli zadané časové zápisy na týždennej báze. Vo verzii 3 Project Service Automation, časové zadávania sú zapisujú na dennej báze. Po vytvorení niekoľkých časových položiek ich však môžete hromadne vytvárať alebo kopírovať.

## <a name="create-a-time-entry"></a>Vytvoriť zadanie času

Ak chcete vytvoriť zadanie času, postupujte podľa týchto krokov.

1. Na stránke **Zadania času** stlačte možnosť **Nové**.
2. V dialógovom okne **Rýchle vytvorenie: Zadanie času** zadajte dobu trvania položky v minútach, hodinách alebo dňoch. Trvanie musí byť zadané v nasledujúcom formáte *x* minút, *x* hodín alebo *x* dní. Hodiny a dni je taktiež možné zadať pomocou desatinných miest, napríklad *x.x* hod. alebo *x.x* dní.
3. Vyberte typ časovej položky a projekt, pre ktorý zadávate časovú položku.
4. V poli **Projektová úloha** nájdite úlohu pre túto časovú položku.

    > [!NOTE]
    > Ak vytvárate časovú položku pre úlohu, ktorá nie je priradená používateľovi, v poli **Úloha projektu** vyberte tlačidlo **Hľadať**, vyberte položku **Zmeniť zobrazenie** a potom vyberte **Všetky aktívne projektové úlohy** na vypísanie všetkých úloh.

5. Zadajte prípadne vyžadovaný popis a potom stlačte možnosť **Uložiť a zavrieť**.

Po vytvorení a uložení časovej položky ho môžete upraviť v mriežke časového vstupu. Mriežka časového vstupu podporuje dva formáty:

- Môžete zadať časové zápisy vo formáte **hh:mm**. Tento formát sa potom skonvertuje na hodiny a zlomky.
- Môžete zadať hodiny a zlomky priamo.

Všimnite si, že zlomky hodiny nie sú minúty. Preto 1,5 hodín predstavuje 1 hodinu a 30 minút. Rovnaké pravidlo platí pre zlomky dňa. Jeden deň je 24 hodín a 0,5 dní predstavuje 12 hodín.

## <a name="bulk-create-time-entries"></a>Hromadné vytvorenie zadaní času

Po vytvorení niekoľkých časových položiek ich môžete skopírovať na hromadné vytvorenie dodatočných časových položiek.

1. Na stránke **Zadania času** stlačte možnosť **Kopírovať týždeň**.
2. V skupine poľa **Obdobie od** použite polia **Počiatočný dátum** a **Koncový dátum** na definovanie rozsahu dátumov, z ktorého sa majú kopírovať časové položky.
3. V skupine poľa **Obdobie do** v poli **Počiatočný dátum** zadajte dátum vytvorenia položiek času.
4. Výberom položky **Kopírovať** vytvoríte kópiu časových položiek zodpovedajúcich dňu týždňa, ktorý je zadaný v skupine poľa **Obdobie do**. Napríklad, pondelkové časové zadanie z minulého týždňa bude skopírované do pondelka pre týždeň uvedený v skupine poľa **Obdobie do**.

## <a name="import-data-for-time-entries"></a>Import údajov pre zadania času

Môžete importovať údaje z projektových rezervácií a priradení. Keď importujete údaje, môžete zadať rozsah dátumov rezervácií, ktoré chcete importovať, a potom explicitne vybrať rezervácie, ktoré by sa mali vytvoriť ako časové zadania **Koncept**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Možnosti zoskupovania, zoraďovania, vyhľadávania a filtrovania

Položky času môžete zoskupiť a filtrovať podľa dimenzií, ktoré sú zadané v stĺpcoch. V poli **Zoskupiť podľa** vyberte dimenziu, ktorá sa má použiť na filtrovanie časových položiek. Záznamy časových položiek môžete zoradiť vo vzostupnom alebo zostupnom poradí pomocou šípky zoradiť v záhlaví stĺpcov. Okrem toho môžete zobraziť alebo skryť položky výberom tlačidla **Filter** na hlavičke stĺpcov a potom do **vyhľadávacieho** poľa zadajte text, ktorý by sa mal použiť na vyhľadávanie časových položiek podľa názvu projektu, úlohy projektu, času položka alebo zdroj.


[!INCLUDE[footer-include](../includes/footer-banner.md)]