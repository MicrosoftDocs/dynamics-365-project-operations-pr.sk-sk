---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 40, V3
description: Tento článok obsahuje zoznam funkcií a opráv, ktoré sú k dispozícii v Microsoft Dynamics 365 Project Service Automation Aktualizácia vydania 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912811"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre Project Service Automation Update Release 40, V3. Táto verzia má číslo zostavenia V3.10.61.61 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie vo februári 2022.

## <a name="update-release-40"></a>Aktualizácia vydania 40

### <a name="features"></a>Funkcie
Fáza 1 inovácie z Project Service Automation na Project Operations – Lite bude vydaná vo februári 2022 pre všetkých zákazníkov. Ak chcete skontrolovať oprávnenosť, pozri [Inovujte z Automatizácie projektových služieb na Projektové operácie](upgrade-project-operations-non-stocked.md). Ak sa aplikácia nezobrazí vo vašej inštancii v Power Platform Admin Center, kontaktujte podporu a požiadajte o povolenie letu pre vaše prostredia. Vaša žiadosť musí obsahovať zoznam ID prostredí, kde je potrebné let povoliť.

### <a name="bug-fixes"></a>Opravy chýb

Vyriešili sa tieto problémy.

**Čas a výdavky**
- Po odmietnutí alebo zrušení záznamu času chýba záznam poznámky. 

**Predaj**

- Keď aktualizujete odhady nákladov alebo predaja pomocou vopred pripravených doplnkov, máte nesprávne povolené odosielanie dát JSON, ktoré nie sú platné mimo používateľského rozhrania.
- Keď aktualizujete riadky cenových ponúk pomocou rýchleho zobrazenia, máte povolené aktivovať cenové ponuky.
