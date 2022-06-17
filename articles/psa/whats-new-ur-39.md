---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 39, V3
description: Tento článok obsahuje zoznam funkcií a opráv, ktoré sú k dispozícii v Microsoft Dynamics 365 Project Service Automation Aktualizácia vydanie 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922471"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre Project Service Automation Update Release 39, V3. Táto verzia má číslo zostavy V3.10.60.170 a je všeobecne dostupná prostredníctvom samoaktualizácie v januári 2022.

## <a name="update-release-39"></a>Aktualizácia vydania 39

### <a name="bug-fixes"></a>Opravy chýb

Vyriešili sa tieto problémy.

**Všeobecné**

- Na mape stránky pre preklad do arabčiny bolo vykonaných niekoľko vylepšení.

**Riadenie projektov**

- Keď zmeníte projektového manažéra v projekte na používateľa, ktorý je už členom tímu v projekte, dôjde k chybe.

**Predaj**

- Vlastník **Cenník projektovej zmluvy** je nesprávne, keď sa cenník vytvára automaticky. 
- Pri aplikovaní cenníka na parameter projektu nie je dodržaná platnosť dátumu cenníka.
- Pri úprave dvoch samostatných cenových ponúk nemusí mať zmluvná jednotka správnu predvolenú hodnotu.
