---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 35, V3
description: Táto téma obsahuje zoznam funkcií a opráv, ktoré sú k dispozícii v aktualizácii Microsoft Dynamics 365 Project Service Automation, vydanie 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 53670e2c7f54f8fccf636b2855e190f5f85c6068
ms.sourcegitcommit: 5bb8ca5055deda57e2b1173a2e45c53b15f61d62
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473284"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation, vydanie 35, V3. Táto verzia má číslo zostavenia V3.10.56.110 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie zo septembra 2021.

## <a name="update-release-35"></a>Aktualizácia vydania 35

### <a name="bug-fixes"></a>Opravy chýb

Vyriešili sa tieto problémy.

**Čas a výdavky**

- Schvaľovateľ projektu dostane chybu oprávnenia na čítanie, keď schváli položky výdavkov pomocou roly **Schvaľovateľ projektu**.
- Schvaľovateľ projektu dostane chybu oprávnenia na zápis v **msdyn_projectapproval**, keď zruší schválený časový záznam s rolou **Schvaľovateľ projektu**.
- Keď vyberiete **Kopírovať týždeň** v položke času v module aplikácie Dynamics 365 pre telefón – Project Resource Hub, vyskytne sa nasledujúca chyba: „...\OfficeProductivity_RibbonRules.js.map: chyba HTTP: stavový kód 404, net:: ERR_HTTP_RESPONSE_CODE_FAILURE.“
- Politika **Skúsiť znova** automaticky schvaľuje položky, ktoré boli predtým odmietnuté.
- Vedľajšia mriežka **Množiny schválení** zobrazuje neaplikovateľné akcie na páse s nástrojmi.
- Ikony chýbajú pre **Projektová úloha** a **Rola zdroja** v entite **Zadanie času**.
- Keď importujete priradenia zdrojov, importované zadania času nemajú správne trvanie pre priradenia, ktoré boli vytvorené pomocou úloh manuálneho režimu.
- **Vymazať** chýba na stránke **Rozšírené vyhľadávanie záznamov zadania času**.
- **Uložiť** chýba na stránke **Informácie o zadaní času**. Tento problém zabraňuje uloženiu zmien, keď je stránka zatvorená.

**Plánovanie projektu**

- Mriežky **Priradenie zdrojov** a **Zosúladenie zdrojov** netriedia zoskupené atribúty podľa abecedy.
- Úlohy nemožno vytvárať, ak je správanie dátumu prispôsobené na **Iba dátum**.

**Správa zdrojov**

- Ak sú nainštalované Dynamics 365 Field Service aj Project Service Automation, vyskytnú sa problémy s prekrytím, keď je **Priradené zobrazenie požiadaviek zdrojov** spojené s hlavnou stránkou.
- Dvojitým kliknutím na **Uložiť** v dialógovom okne **Rýchle vytvorenie člena tímu** zabraňuje vytváraniu požiadavky na zdroje.

**Predaj**

- Zobrazí sa výnimka, ak odstránite úlohu, ktorá je spojená s cenovou ponukou, ktorá má stav **Získané**.