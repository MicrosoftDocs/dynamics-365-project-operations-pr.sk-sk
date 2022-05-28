---
title: Zmeny správy zdrojov (Project Service Automation 3. x)
description: Táto téma poskytuje informácie o zmenách v oblasti správy zdrojov.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d19b8b453c544bb4c6fd11a8b9f750cb08e0c168
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595517"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Zmeny správy zdrojov (Project Service Automation 3. x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Časti tejto témy poskytujú informácie o zmenách, ktoré boli vykonané v oblasti správy zdrojov Dynamics 365 Project Service Automation verzie 3. x.

## <a name="project-estimates"></a>Odhady projektu

Namiesto toho, aby bol založený na entite **msdyn\_projecttask** (**Projektová úloha**), odhady projektu sú založené na entite **msdyn\_resourceassignment** (**Priradenie zdroja**). Priradenia prostriedkov sa stali "zdrojom pravdy" pre plánovanie úloh a určovanie cien.

## <a name="line-tasks"></a>Riadkové úlohy

V PSA 3.x sú úlohy v riadku zastarané (zastarané). Úlohy teraz poukazujú na celú úlohu namiesto úloh riadkov.

Nasledujúci príklad ukazuje, ako úlohu, ktorá sa nazýva "Skúšobná úloha" je priradená členom tímu A a B v starších verziách PSA a PSA 3.x.

- **Pred PSA 3.x:**

    - Skúšobná úloha

        - Skúšobná úloha – úloha riadka 1

            - Priradenie k A

        - Skúšobná úloha – úloha riadka 2

            - Priradenie k B

- **PSA 3.x:**

    - Skúšobná úloha

        - Priradenie k A
        - Priradenie k B

## <a name="unassigned-assignment"></a>Nepriradené priradenie

V PSA 3.x, nepriradené nasadenie je priradenie, ktoré je priradené členov tímu **NULL** a zdroju **NULL**. Nepriradené nasadenia sa môžu vyskytnúť v niekoľkých prípadoch:

- Ak bola úloha vytvorená, ale ešte nebola priradená žiadnemu členovi tímu, nepriradené nasadenie sa vždy vytvorí. 
- Ak sa odstránia všetci postupníci úlohy, nepriradené nasadenie je pre túto úlohu znova vytvorené.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Plánovanie polí v entite Projektová úloha

Polia v entite **msdyn\_projecttask** boli zastarané alebo presunuté do entity **msdyn\_resourceassignment**, alebo sa na ne dnes odkazuje z entity **msdyn\_projectteam** (**Člen projektového tímu**).

| Zastarané pole v msdyn\_projecttask (Projektová úloha) | Nové pole na msdyn\_resourceassignment (priradenie prostriedkov) | Komentár |
|---|---|---|
| msdyn\_assignedresources | Žiadne | |
| msdyn\_assignedteammembers | Žiadne | |
| msdyn\_numberofresources | Žiadne | |
| msdyn\_scheduledhours | Žiadne | |
| msdyn\_effortcontour | msdyn\_plannedwork | Formát dátovej štruktúry zápisu objektov JavaScript (JSON), ktorý je uložený v poli, sa zmenil. |

## <a name="schedule-contour"></a>Naplánovať obrys

Obrys plánu sa ukladá do poľa **Plánovaná práca** (**msdyn\_plannedwork**) každej entity **Priradenie zdroja** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Štruktúra

Nová štruktúra obrysu plánu pozostáva z flexibilných časových plátkov, ktoré sú definované pre každý deň plánu. Každý časový plátok má nasledujúce vlastnosti:

- **Začiatok** – Ide o začiatok pracovného času na deň podľa kalendára projektu.
- **Koniec** – Ide o koniec pracovného času na deň podľa kalendára projektu.
- **Hodiny** – Počet hodín, ktoré sú priradené v deň.

**Príklad**

Tento príklad používa kalendár projektu, kde pracovný deň je od 9 hodín do 5 hodín v časovom pásme UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automatické plánovanie a manuálne plánovanie

Ak je úloha automaticky naplánovaná, hodiny sú načítané dopredu a trvanie úlohy môže byť znížené.

**Príklad**

Nasledujúca úloha je automaticky naplánovaná na 18 hodín počas troch dní (december 3, 2018 až december 5, 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Ak je úloha manuálne naplánovaná, hodiny sú rovnomerne rozdelené do všetkých dátumov.

**Príklad**

Nasledujúca úloha je manuálne naplánovaná na 18 hodín počas troch dní (december 3, 2018 až december 5, 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Jednotka priradenia

Jednotka priradenia bola zastaraná v PSA 3.x. Úloha úsilia hodín je teraz rovnomerne rozdelená, na deň, medzi všetky pridelené zdroje.

**Príklad**

V tomto príklade je úloha priradená k dvom prostriedkom a je automaticky naplánovaná na 36 hodín počas troch dní (3. decembra 2018 až 5. decembra, 2018).

- Priradenie 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Priradenie 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Cenové dimenzie

V PSA 3.x, dimenzie týkajúce sa zdroja (napríklad **Rola** a **Organizačná jednotka**) boli odstránené z entity **msdyn\_projecttask**. Tieto polia je teraz možné načítať z príslušného člena projektového tímu **(msdyn\_projectteam**) priradenia prostriedkov (**msdyn\_resourceassignment**) pri vygenerovaný projektových odhadov. Nové pole **msdyn\_organizationalunit** bolo pridané do entity **msdyn\_projectteam**.

| Zastarané pole v msdyn\_projecttask (Projektová úloha) | Pole z msdyn\_projectteam (člen projektového tímu), ktoré sa používa namiesto |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Kontúry

Ceny a odhad obrysy polia boli zastarané v entite **msdyn\_projecttask**. Boli presunuté do entity **msdyn\_resourceassignment**.

| Zastarané pole v msdyn\_projecttask (Projektová úloha) | Nové pole na msdyn\_resourceassignment (priradenie prostriedkov) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Nasledovné polia boli pridané do entity **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Tieto polia plánované, skutočné a zostávajúce náklady a predaja sa nezmenia na entitu **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
