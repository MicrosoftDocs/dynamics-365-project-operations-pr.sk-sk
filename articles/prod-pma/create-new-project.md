---
title: Vytvorenie nového projektu
description: Táto téma poskytuje informácie o tom, ako vytvoriť nový projekt.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084499"
---
# <a name="create-a-new-project"></a>Vytvorenie nového projektu

[!include [banner](../includes/banner.md)]

Podľa nasledujúcich pokynov vytvoríte nový projekt.

1. Na stránke **Projektový manažment** vyberte **Nový projekt** a zadajte nasledujúce hodnoty:

    - **Typ projektu:** Čas a materiál
    - **Názov projektu:** Fáza 2 inovácie na XYZ
    - **Skupina projektov:** TM\_WIP
    - **Identifikátor projektovej zmluvy:** 00000002

2. Vyberte **Vytvoriť projekt**.

## <a name="assign-a-resource-to-a-project"></a>Priradenie zdroja k projektu

1. Na stránke **Pracovníci** v zozname **Pracovníci** vyberte záznam pre pracovníka, pre ktorého ste predtým nastavili kompetencie, a otvorte záznam pracovníka.
2. Na table Akcia na karte **Projekt** v skupine **Nastavenie** vyberte **Priradiť projekty**.
3. Na stránke **Priradenia projektu na overenie zdrojov** na karte **Projekty** v poli **Pridať projekt k vybraným projektom** nastavte filter na projekt **Fáza 2 inovácie na XYZ**.
4. Na table **Zostávajúce projekty** vyberte projekt a potom ho kliknutím na tlačidlo so šípkou pridajte na tablu **Vybrané projekty**.

Podľa potreby môžete k zdroju tiež priradiť kategórie. Typ kategórie je buď **Náklady** alebo **Príjem**. Typ kategórie určuje vaša organizácia. Ak pre zdroj nie sú priradené žiadne kategórie, služba Finance vyhľadá predvolenú kategóriu hodinových cien pre náklady a výnosy.

## <a name="set-up-project-resource-and-role-characteristics"></a>Nastavenie zdroja projektu a charakteristiky roly

Projektový manažér môže pomocou funkcie financovania projektu vytvoriť roly, ktoré sú potrebné pre projekt. Roly je možné použiť, ak potvrdené zdroje nie sú pri rezervácii zdrojov stále známe. Roly je možné dočasne rezervovať ako plánované zdroje, aby ste mohli pokračovať v etapách plánovania projektu.

[![Ukážka roly](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenár:** Spoločnosť Contoso bola najatá na dokončenie projektu typu Čas a materiál, ktorý má schválené stanovy projektu. Junior projektový manažér ešte stále dokončuje rozsah projektu. Správca zdrojov v súčasnosti identifikuje konkrétne zdroje, ktoré budú vyhradené na prácu na novom projekte. Z dôvodu kritickej povahy projektu požiadal sponzor projektu jednu z rolí Senior projektového manažéra. Správca zdrojov musí získať nový zdroj a definovať rolu v systéme pre prípad, že junior projektový manažér vyžaduje informácie o zdroji počas plánovania projektu.

Nasledujúce kroky ukazujú, ako môže správca zdrojov nastaviť rolu Senior projektového manažéra a priradiť k nej vlastnosti zdrojov. Neskôr sa dá rola použiť na vyhľadanie dostupných zdrojov, ktoré zodpovedajú požadovaným kompetenciám v oblasti zdrojov.

1. Na stránke **Nastaviť roly** vyberte **Nová** a zadajte nasledujúce hodnoty:

    - **ID roly:** Senior projektový manažér
    - **Opis:** Senior projektový manažér

2. Stlačte možnosť **Vytvoriť**.
3. Vyberte rolu **Senior projektový manažér** a potom vyberte **Nakonfigurovať vlastnosti**.
4. V poli **Typ vlastností** vyberte **Zručnosť**.
5. V poli **Dostupné vlastnosti** zadajte hľadanú zručnosť.
6. V poli **Typ vlastnosti** vyberte **Certifikát**.
7. V poli **Dostupné vlastnosti** zadajte hľadaný typ certifikátu.

## <a name="assign-a-project-resource-to-a-project"></a>Priradenie zdroja projektu k projektu

1. Na stránke **Všetky projekty** vyberte projekt **Fáza 2 inovácie na XYZ**.
2. Na karte **Projektový tím a plánovanie** vyberte **Pridať**.
3. V poli **Rola** vyberte **Člen tímu**.
4. Vyberte **Rezervovať z kalendára**.
5. Na stránke **Dostupnosť zdrojov** vyberte **Zobraziť nastavenia**.
6. Na stránke **Upraviť nastavenia zobrazenia** zadajte nasledujúce hodnoty:

    - **Formát pre zobrazenie rozsahu dátumov:** Deň
    - **Zobraziť popisy dostupnosti:** Áno
    - **Zobraziť zostávajúcu kapacitu:** Áno

7. V zozname zdrojov vyberte zdroj.
8. Vyberte **Pevná rezervácia** a **Plná kapacita**.

## <a name="assign-a-resource-to-a-default-role"></a>Priradenie zdroja k predvolenej role

Aby ste pomohli projektovým manažérom alebo správcom zdrojov, aby sa mohli hlbšie ponoriť do zdrojov, ktoré je možné rezervovať pre projekt. Môžete priradiť predvolenú rolu k existujúcemu zdroju alebo k novo získanému zdroju. Napríklad keď bol Daniel prijatý do zamestnania, mal skúsenosti a zručnosti na to, aby obsadil úlohu obchodného analytika. Správca zdrojov pridelil túto rolu ako predvolenú rolu Daniela. Preto správca zdrojov pridal Daniela do skupiny obchodných analytikov, ktorí sú k dispozícii na prácu na projektoch.

Počas rezervácie zdrojov môžu projektoví manažéri filtrovať zdroje rolí, ktoré sú k dispozícii na prácu na projektoch. Tieto informácie môžu použiť ako jedno kritérium, keď uskutočňujú multikriteriálnu rozhodovaciu analýzu počas plnenia zdrojov. Môžu tiež pridať do filtra ďalšie charakteristiky zdrojov, aby vyhľadali zdroje, ktoré majú špecifické zručnosti, vzdelanie a skúsenosti pre daný projekt.

**Scenár:** Schválený projekt sa začal a rola Senior projektového manažéra bola vyhradená ako plánovaný zdroj počas fázy plánovania projektu. Správca zdrojov teraz získal zdroj na splnenie úlohy Senior projektový manažér.

1. Na stránke **Zoznam zdrojov** vyberte **Daniel Goldschmidt**.
2. Na stránke **Rola zdroja** vyberte **Nová** a zadajte nasledujúce hodnoty:

    - **Účinná:** Zadajte aktuálny dátum.
    - **Exspirácia:** Zadajte **Nikdy**.
    - **Rola:** Zadajte **Senior projektový manažér**.

3. Vyberte **Uložiť** a potom zatvorte stránku.
4. Na karte **Kompetencie** pridajte zručnosť **ProjectMgmt** a certifikát **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]