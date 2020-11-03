---
title: Inovovať domovskú stránku
description: Táto téma zobrazuje Dynamics 365 Project Service Automation, kde nájdete dôležité informácie o nových a zmenených funkciách a procese inovácie na najnovšiu verziu.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
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
ms.openlocfilehash: 29e7b519b61e8709c025e9906d04aed0156f65eb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084445"
---
# <a name="upgrade-home-page"></a>Inovovať domovskú stránku

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Inovujte z verzie 2.x alebo 1.x na verziu 3.x aplikácie PSA

### <a name="new-instances"></a>Nové inštancie

Od 17. mája 2019, keď sa Project Service Automation vyberie vybratá počas poskytovania novej inštancie, verzia 3. x sa predvolene nainštaluje.

### <a name="existing-instances"></a>Existujúce inštancie

Predtým zákazníci s inštanciou PSA verzia 2.x a potrebe inovácie na verziu 3.x, čo predstavuje verziu PSA založenú na zjednotenom klientskom rozhraní, museli kontaktovať podporu Microsoft a poskytnúť im podrobnosti o svojej inštancii, na základe ktorých im podpora mohla povoliť inováciu inštancie na verziu 3.x. Od 1. marca 2020 budú zákazníci, ktorí majú inštanciu PSA verzie 2.x a potrebujú aktualizovať na verziu 3.x, schopní inovovať svoje inštancie priamo z administračného portálu bez toho, aby museli kontaktovať technickú podporu spoločnosti Microsoft.  

> [!NOTE]
> PSA verzia 3.x obsahuje významné zmeny. Bola vytvorená na rámci zjednoteného rozhrania, aby pomáhala poskytovať zlepšenú používateľskú skúsenosť. Pretvorená aplikácia ponúka jednotné používateľské rozhranie (UI), ktoré nasleduje responzívne princípy dizajnu pre optimálne prezeranie na ľubovoľnej veľkosti obrazovky alebo zariadení. Počas celej aplikácie sa vyskytli ďalšie zmeny. Medzi niektoré z oblastí, ktoré boli zmenené, patria ceny, rezervácie a priraďovanie zdrojov, času, výdavkov a schválenia.

Pred začatím procesu inovácie, odporúčame, aby ste dokončili nasledujúce úlohy:

- Overte, či Dynamics 365 Field Service a Project Service Automation sú nainštalované na identifikovanej inštancii. Ak sú nainštalované obidva riešenia, mali by ste plánovať inováciu skôr, ako obnovíte pravidelné používanie inštancie.
- Pozorne si prečítajte nasledujúce témy. Povedomie a pochopenie zmien medzi verziami vám pomôže s procesom inovácie. Tieto témy poskytujú informácie o hlavných zmenách v PSA, spolu s úvahami a odporúčaniami pre plánovanie inovácie na verziu 3.x.

    - [Čo je nové alebo zmenené v Project Service Automation verzia 3](whats-new-changed-v3.md)
    - [Informácie o inovácii – Project Service Automation verzia 2.x alebo 1.x na verziu 3](upgrade-v3.md)

- Inovujte inštancia izolovaného priestoru na vyhodnotenie zmien vo vykonávaní pred inováciou výrobnej inštancie.

Potom, čo ste preskúmali témy, ktoré boli spomenuté skôr a sú pripravení na upgrade na PSA verzia 3.x alebo verzia UCI, odošlite požiadavku na podporu spoločnosti Microsoft, aby inovácia bola k dispozícii z centra správcu. V žiadosti uveďte podrobnosti o vašej inštancii.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Staršie verzie PSA (PSA verzia 2.x) v novo vytvorenej inštancie

Od mája 17, 2019, všetky nové inštancie budú mať UCI ako predvolený klient. Pre vyrovnanie s touto zmenou, PSA verzia 3.x a Field Service verzia 8.x bude poskytnutá v predvolenom nastavení, pretože tieto verzie sú navrhnuté pre prácu s klientom UCI.

Od 1. marca 2020 už zákazníci Dynamics PSA nebudú môcť vytvárať nové prostredia so staršími verziami PSA, napríklad PSA verzie 2.x alebo nižšej. Akékoľvek nové prostredie bude mať získať iba verziu 3.x PSA.

> [!NOTE]
> Najlepšie skúsenosti pri používaní starších verzií služieb Field Service a PSA nájdete na stránke **Systémové nastavenia** a pre pole **Používanie výhradne nového Zjednoteného rozhrania (odporúča sa)** zvoľte možnosť **Nie** , pretože tieto verzie nie sú navrhnuté tak, aby sa správne načítavali v UCI. Potom, čo ste vypli UCI, môžete otvoriť a spustiť tieto verzie Field Service a PSA pomocou starého webového klienta. 
