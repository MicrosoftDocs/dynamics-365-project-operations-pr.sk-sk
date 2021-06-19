---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 22, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 22, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 5694aa27afe7618cfca6b27444393634a9686600
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006575"
---
# <a name="project-service-automation-update-release-22-v3"></a>Aktualizácia pre Project Service Automation, vydanie 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 22. Táto verzia má číslo V 3.10.33.48 a v júni 2020 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.

## <a name="update-release-22"></a>Aktualizácia vydania 22

### <a name="bug-fixes"></a>Opravy chýb



**Čas a výdavky**

Vyriešili sa tieto problémy:

- **Zadania času** sa po importovaní automaticky nepridajú do plánu zadaní času.
- Nástroj na výber dátumu v mriežke **Zadanie času** nerozpoznáva regionálne nastavenia používateľa.

**Správa zdrojov**

Vyriešili sa tieto problémy:

- V manuálnom režime sa zmeny kontúr **Priradenie zdroja** pri generovaní **Požiadaviek na zdroje** nerozpoznávajú.
- **Požiadavky na zdroje** nepodporujú vlastné stavy požiadaviek.

**Riadenie projektov**

Vyriešili sa tieto problémy:

- Dvojité kliknutie na EstimateGridControl nebude mať za následok správnu analýzu čísel holandského formátu.
- Priradené hodiny sa neaktualizujú správne, keď sa priradenia zmenia pomocou doplnku klienta pre osobné počítače Microsoft Project.
- Mriežky na sledovanie projektov a odhady ukazujú nesprávny kód meny predaja, keď je mena zmluvy iná ako mena zákazníka, a organizácia je nakonfigurovaná tak, aby namiesto symbolov meny ukazovala kódy meny.
- Dátum dokončenia pre člena tímu pridá jeden deň, ak je rozvrhnutie pracovnej doby 24 hodín denne.
- V pláne projektu nebude mať pridanie kategórie transakcií do úlohy za následok spustenie automatického ukladania.
- Pri pridaní člena tímu do šablóny projektu sa zobrazí nasledujúca chyba: „Požiadavky na zdroje nemožno priradiť k šablónam projektu“. 
- Skript pravidla pre pás s nástrojmi „msdyn.Approval.CanApproveOrReject“ ukazuje chybu časového limitu.

**Sales**

Vyriešili sa tieto problémy:

- Chybové hlásenie o overení sa nezobrazí, keď je vo vyhľadávaní v cenníku vo formulári/entite „Nový projektový cenník pre cenovú ponuku“ vybratý Cenník obstarávacích cien.
- Uzatvorenie cenovej ponuky ako získanej nemá za následok presun na vytvorenú zmluvu, ak je BPF pripojená k cenovej ponuke v záverečnej etape.
- Vrátenie položky **Nefakturovaný predaj** je spojené s pôvodnými nákladmi, keď je odvolané zadanie času.
- Po výbere tlačidla **Potvrdiť** sa stav faktúry nezmení na **Potvrdená**, pokiaľ sa faktúra neobnoví.


[!INCLUDE[footer-include](../includes/footer-banner.md)]