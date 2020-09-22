---
title: Čo je nové v aktualizácii Project Service Automation, vydanie 16, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 16, V3
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755582"
---
# <a name="project-service-automation-v3-update-release-16"></a>Aktualizácia Project Service Automation V3, vydanie 16
S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.

Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia preferovaného riešenia](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page). Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu PSA V3, vydanie 16. Táto verzia má číslo zostavy V3.10.6.34 a je všeobecne dostupná prostredníctvom samoaktualizácie v januári 2020

## <a name="update-release-16"></a>Aktualizácia vydania 16

### <a name="bug-fixes"></a>Opravy chýb

-   Čas a výdavky

    -   Oprava: Používatelia, ktorí sa pokúšajú odoslať vymazané údaje o časoch a výdavkoch na schválenie, teraz dostanú príslušné chybové správy.

-   Riadenie projektov

    -   Oprava: Jednotky zabezpečujúce zdroje definované pre členov tímu v šablónach sa rešpektujú, pričom šablóny sa použijú na nový projekt.

    -   Oprava: Vylepšené spracovanie opätovného pridelenia vlastníctva záznamu.

    -   Oprava: Projekty, ktoré sa práve kopírujú, sa skopírujú až po dokončení všetkých operácií kopírovania.

-   Správa zdrojov

    -   Oprava: Rozšírenie rezervácií teraz zvláda krátke trvanie správne a pre predĺžené rezervácie už nevytvára nulové hodiny.

    -   Oprava: Zobrazenie odsúhlasenia sa teraz vykreslí, keď je časové pásmo projektu +5:30 GMT a čas používateľa je iný.

-   Sales

    -   Oprava: Keď sa odstráni projekt mapovaný na riadok zmluvy a mapuje sa nový projekt, skutočné záznamy o novom projekte neboli prehodnocované na základe pravidiel fakturácie a stanovovania cien definovaných v riadku zmluvy. Toto bolo v tomto vydaní opravené. Ceny a skutočné záznamy o novo mapovanom projekte sa zvrátia a znovu sa vytvoria správne na základe cenových a fakturačných pravidiel riadka zmluvy. Skutočné záznamy nemapovaného projektu sa následne v dôsledku toho prehodnotia a znovu vytvoria.

    -   Oprava: K riadku odhadu bola pridaná ďalšia validácia poľa **Čiastka**, aby sa zabezpečilo, že nulové hodnoty nebudú pretrvávať.

    -   Oprava: Po aktualizácii skutočností v projekte bolo do hlavného formulára projektu pridané tlačidlo obnovenia, ktoré používateľom umožňuje opätovnú synchronizáciu skutočností.

    -   Oprava: Keď používatelia vykonajú inováciu z 2.X na 3.X, budú povolené projekty s hodnotou NULL pre názov projektu.

