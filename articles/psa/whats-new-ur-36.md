---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 36, V3
description: Tento článok obsahuje zoznam funkcií a opráv, ktoré sú k dispozícii v aktualizácii Microsoft Dynamics 365 Project Service Automation, vydanie 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: a8942713109075da2503c9d22d40b6ac95ae00be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925001"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation, vydanie 36, V3. Táto verzia má číslo zostavy V3.10.57.152 a je všeobecne dostupná prostredníctvom samoaktualizácie v októbri 2021.

## <a name="update-release-36"></a>Aktualizácia vydania 36

### <a name="bug-fixes"></a>Opravy chýb

Vyriešili sa tieto problémy.

**Všeobecné**
- Názov poľa **Predvolená šablóna pracovnej doby** je na stránke **Parametre projektu** nesprávne preložený.
- Asynchrónne doplnky nespracovávajú správne výnimky súvisiace s príponou **SharedVariableService**.

**Čas a výdavky**
- Ak chýbajú riadky denníka alebo používateľ nemá správne oprávnenia na čítanie riadkov denníka, pri zrušení schválenia projektu sa vyskytne nesprávna chyba.
- Používatelia nemôžu zrušiť schválenie, ak má záznam o výdavkoch alebo čase viac ako jedno súvisiace schválenie projektu.
- **Neprítomnosť** a **Dovolenka** sú nesprávne preložené do čínskeho jazyka pri vyhľadávaní na stránke rýchleho vytvorenia **Zadanie času**.

**Správa zdrojov**
- Používateľ nemôže hľadať zdroje v **Asistent plánovania**, keď je režim zobrazenia nastavený na **Deň**, **Týždeň**, alebo **Mesiac**.
- Všeobecným zdrojom môže byť nesprávne dovolené zadať názvy prázdnych pozícií. 
- Uzavretím zmluvy ako stratenej sa nezrušia budúce rezervácie.

**Predaj**
- Keď má prostredie veľký objem produktov, výkon v mriežke **Odhad materiálov** sa zníži.
- Pri vytváraní projektu zo šablóny nie je mena projektu predvolená pre príslušnú zmluvnú jednotku projektového manažéra.
- Skutočné sumy sa nemusia vždy zhodovať s tým, čo sa odzrkadľuje na termíne projektu, alebo sa čiastky stanú zápornými v konkrétnych scenároch stiahnutia.
- Keď priradíte projekt vytvorený zo šablóny projektu k riadku zmluvy, dôjde k chybe.
- Používatelia môžu odstrániť riadok zmluvy s míľnikmi, **Pripravené na faktúru** a **Faktúra vytvorená**. To by nemalo byť dovolené.
- Keď sú odhady importované z projektu, zúčtovateľnosť podrobností ponuky je nesprávne nastavená, keď je pre riadok ponuky povolená fakturácia podľa úloh.
- Keď pridáte míľnik pre fakturáciu s pevnou cenou, tento míľnik sa v čiastkovej mriežke míľnika prejaví až vtedy, keď sa stránka obnoví.
- Pri vytváraní zmluvy o projekte s názvom ponuky, ktorá má príznak null, sa vygeneruje nulová referencia.
- Úlohy manuálneho režimu, kde je mena projektu odlišná od meny zdroja, majú za následok nesprávne odhady cien.
- Používatelia nemôžu opätovne vyvolať transakciu, ktorá bola úspešne opravená opravnou faktúrou.
- Deaktivované kategórie transakcií sa zobrazia v mriežke **Odhady výdavkov**.



