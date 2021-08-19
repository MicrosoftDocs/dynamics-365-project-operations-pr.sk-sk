---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 32, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 32, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994880"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 32. Táto verzia má číslo V3.10.53.108 a je všeobecne dostupná prostredníctvom automatickej aktualizácie od júna 2021.

## <a name="update-release-32"></a>Aktualizácia vydania 32

### <a name="bug-fixes"></a>Opravy chýb

#### <a name="general"></a>Všeobecné

- Ak hlavná aktualizácia zlyhá, mali by sa zablokovať iba hlavné vstupné body aplikácie, aby sa zabezpečilo, že zdieľané entity sú stále prístupné.

#### <a name="time-and-expense"></a>Čas a výdavky

Vyriešili sa tieto problémy:

- **TimeEntriesImportFromResourceAssignment** neuchováva čas začiatku a konca pre časť krivky priradenia zdrojov.
- Keď vyberiete možnosť **Otvoriť záznam** v mriežke **Časový záznam**, môže vám to zabrániť vo výbere ďalších formulárov.
- Počas importu priradení k časovým záznamom by dotaz na kód klienta mohol vygenerovať dlhú adresu URL, ktorá spôsobí zlyhanie dotazu.
- Na mriežke **Časový záznam** po odstránení hodnoty z bunky nezostane pozornosť zameraná na mriežku.
- Tlačidlo **Odmietnuť** bolo odstránené zo zobrazenia **Spracúvanie schválení** v prípade moderných schválení.
- Stabilita a výkon hromadného schválenia časového záznamu sú ovplyvnené blokovaním a nesprávnou manipuláciou s prispôsobeniami, ktoré sa týkajú entity **Časový záznam**.

#### <a name="project-planning"></a>Plánovanie projektu

- Výnimka odkazu na hodnotu null sa vygeneruje, keď aktualizujete projekt, ktorý má v poli **Zmluvná jednotka** hodnotu null.
- **Obnoviť súčty projektu** nesprávne vypočíta zostávajúce náklady a zostávajúce predaje v rámci projektu.
- Nadbytočné výpočty cien ovplyvňujú výkon, ktorý súvisí s aktualizáciami kriviek priradenia zdrojov.

#### <a name="resource-management"></a>Správa zdrojov

Nasledujúci problém bol opravený:

- Ak je kapacita kalendára rezervovateľného zdroja viac ako 1, Project Service Automation nesprávne rozpozná kapacitu ako 0 (nula). Preto sa v zobrazení plánu objaví nekonečná slučka.

#### <a name="sales"></a>Predaj

Vyriešili sa tieto problémy:

- Keď sa vytvorí záznam v účtovnom denníku, ktorý má vlastný typ transakcie, dôjde k nasledujúcej výnimke odkazu na hodnotu null: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Roly a kategórie, ktoré sú neaktívne ešte pred skopírovaním cenovej ponuky, by sa nemali pridávať do zúčtovateľných rolí a kategórií v rámci novoskopírovanej cenovej ponuky.
- Dátum dokumentu a dátum zaúčtovania nie sú zosúladené s dátumom začiatku uvedeným v riadku faktúry, ktorý je vytvorený priamo z konceptu faktúry.
- Výnimky odkazu na hodnotu null sa generujú v scenároch, ktoré súvisia s deaktiváciou rolí a kategórií pred skopírovaním cenovej ponuky.
- Akcia **Aktualizovať ceny** na stránke **Projekty** neaktualizuje odhady výdavkov a odhady materiálov.
