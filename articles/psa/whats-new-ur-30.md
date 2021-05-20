---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 30, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 30, V3
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852893"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 30. Táto verzia má číslo V3.10.51.61 a v apríli 2021 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.

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