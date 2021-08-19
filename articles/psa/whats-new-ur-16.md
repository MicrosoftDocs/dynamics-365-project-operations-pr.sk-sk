---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 16, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 16, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f577cd8407b0f12607c56891eeadb1071f659cff67bd9f086a6b3bbec6376e9d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004420"
---
# <a name="project-service-automation-update-release-16-v3"></a>Aktualizácia pre Project Service Automation, vydanie 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.  Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia preferovaného riešenia](/dynamics365/project-service/upgrade-psa-home-page).
Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu PSA V3, vydanie 16. Táto verzia má číslo zostavy V3.10.6.34 a je všeobecne dostupná prostredníctvom samoaktualizácie v januári 2020.


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



[!INCLUDE[footer-include](../includes/footer-banner.md)]