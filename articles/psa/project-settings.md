---
title: Projektové nastavenia
description: Táto téma poskytuje informácie o nastaveniach projektového manažmentu.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084527"
---
# <a name="project-settings"></a>Projektové nastavenia

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Na prístup k funkciám plánovania projektu použite nasledujúce nastavenia.

## <a name="work-template"></a>Šablóna práce

Na vytvorenie projektového plánu, musíte vytvoriť šablónu projektového kalendára, ktorá určuje počet pracovných hodín za deň a počas zatváracej doby. Ak chcete vytvoriť šablónu kalendára projektu, priradíte pracovnú šablónu s poľom **šablóna kalendára** projektu. Ak chcete vytvoriť pracovnú šablónu, postupujte podľa týchto krokov.

1. V PSA na ľavom navigačnom paneli, kliknite na **zdroje**. 
2. Na stránke zoznamu **zdroje** , otvrote užívateľské záznamy a vyberte **zobraziť pracovný čas**.

  > [!NOTE]
  > Uistite sa, že povolíte kontextové okná na stránke prehľadávača. To vám umožní zobraziť pracovný čas nastavený pre zdroj.
  
3. Na karte **mesačné zobrazenie** kliknite na položku **nastaviť**. Zobrazí sa zoznam troch možností: 

  - Nový týždenný plán
  - Pracovný plán na jeden deň
  - Voľno

> ![Možnosti nastavenia](media/project-13.png)

4. Vyberte položku **nový týždenný plán** a potom nastavte možnosti pre tento plán prostriedkov. Môžete nastaviť opakujúci sa týždenný plán, parametre pre denné hodiny, zatváraciu dobu, a ďalšie.
5. Nastavte rozsah dátumov, vyberte **uložiť** a potom kliknite na **zavrieť**. 
6. Vráťte sa na ziznam **zdrojov** a vyberte zdroj, pre ktorý nastavíte pracovnú dobu. 
7. Ak chcete nastaviť pracovnú šablónu, vyberte položku **nastaviť kalendár ako**. 
8. V dialógovom okne **pracovná šablóna** zadajte názov pracovnej šablóny a potom vyberte **použiť**. 

Šablónu práce teraz môžete priradiť k šablóne kalendára projektu.

## <a name="resource-roles"></a>Zdrojové roly

Termín *zdrojová rola* odkazuje na množinu zručností, kompetencií a certifikátov, ktoré musí daná osoba vykonať, aby na projekte vykonala konkrétnu množinu úloh. PSA vám umožňuje oceniť a fakturovať role zdroja založené na čase, ku ktorému je zdroj priradený. Každá organizácia musí nastaviť tieto roly pomocou ľavej navigácie v ponuke **Project Service**.

Každá organizácia musí tieto roly nastaviť na stránke **kategórie aktívnych zdrojov**. Ak chcete otvoriť túto stránku, na ľavom navigačnom paneli vyberte **roly prostriedku**.

## <a name="price-lists"></a>Cenníky

Cenníky vám umožňujú vidieť náklady a predajné ceny zdrojov rolí, výdavkových kategórií, produktov a iných prvkov v organizácii. Pred tým ako nastavíte finančné odhady pre prácu, ktorá musí byť dodaná do projektu, mali by ste vytvoriť sprievodný cenník nákladov a predajných cien. V časti parametre by ste tiež mali nastaviť predvolené náklady a predajný cenník, ktorý sa vzťahuje na všetky projekty vytvorené v organizácii. Na stránke **aktívne parametre projektu** , sa uistite, že nastavíte predvolené náklady a predajné cenníky.
