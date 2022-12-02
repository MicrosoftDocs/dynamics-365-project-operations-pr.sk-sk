---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 30, V3
description: Tento článok obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 30, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: ad00b126a13e18a5de47df335aea06b9690efa13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925093"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 30. Táto verzia má číslo V3.10.51.61 a v apríli 2021 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.

## <a name="update-release-30"></a>Aktualizácia vydania 30

### <a name="bug-fixes"></a>Opravy chýb

**Čas a výdavky**

Vyriešili sa tieto problémy:

- Pri vytváraní a ukladaní záznamu času na stránke **Rýchle vytvorenie**, ak je odstránené pole **Rola**, sa vyskytne chyba.
- Filter zadania času použije nesprávny operátor filtra.
- Po výbere možnosti **Kopírovať týždeň** na ovládacom prvku zadania času sa skopírované časové rozvrhy nezobrazia automaticky.

**Správa zdrojov**

Vyriešili sa tieto problémy:

- Po predĺžení rezervácie je stav rezervácie priradený k tvrdej rezervácii nesprávny. Predĺženie rezervácie rešpektuje stav rezervácie definovaný ako **Pridelený** v metadátach nastavenia rezervácie.
- Ak nie je zadaný platný stav rezervácie, chybové hlásenie nie je správne lokalizované.

**Riadenie projektov**

Vyriešili sa tieto problémy:

- Projekty nemožno vytvoriť v jednej mene a zahrnúť súvisiace úlohy v inej mene.

**Predaj**

Vyriešili sa tieto problémy:

- Po skopírovaní cenníka sa ceny neaktualizujú.
- Uzavretie cenovej ponuky ako získanej sa nepodarí, ak má detail ceny pôvodnú hodnotu.
- V entite **Projektová úloha** bola položka **Odhadovaný náklad** premenovaná na **Plánovaný náklad (základný)**.
- Pri vytváraní alebo mazaní faktúr sa generuje výnimka odkazu na hodnotu null.
