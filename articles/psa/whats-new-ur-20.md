---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 20, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 20, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 9939e2f354b69dcbc304f4f6e2ac41a00f251fed69f37978059f4053335ee651
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993620"
---
# <a name="project-service-automation-update-release-20-v3"></a>Aktualizácia pre Project Service Automation, vydanie 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 20. Táto verzia má číslo V 3.10.31.37 a v júni 2020 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.

## <a name="update-release-20"></a>Aktualizácia vydania 20

### <a name="bug-fixes"></a>Opravy chýb

**Riadenie projektov**

Vyriešili sa tieto problémy:

- Import členov projektového tímu s metódou pridelenia, ktorý si vyžaduje hodiny, vedie k nejasnému chybovému hláseniu, keď je uvedených nula hodín.
- Používatelia uvidia nesprávnu chybu po zadaní maximálneho počtu znakov do poľa **Opis** pri projektovej úlohe.
- Stránka **Stiahnutie doplnku Microsoft Dynamics 365 Project Service Automation** je presmerovaná na stránku sťahovania v angličtine, keď je jazyk používateľa nastavený na japončinu.
- Ak sa vyskytne chyba servera, niekedy sa zachová označenie synchronizácie na karte **Plán** vo formulári **Projekty**.
- Po zmene úlohy sa na server odosielajú redundantné aktualizácie úloh.

**Sales**

Vyriešili sa tieto problémy:

- Vo formulári **Zmluva** spôsobí dvojité kliknutie na položku **Vytvoriť faktúru** vytvorenie dvoch faktúr pre jeden skutočný záznam.
- V aplikácii Internet Explorer 11 používatelia nemôžu vytvárať záznamy o výdavkoch.
- Zrušenie nákladov a zrušenie nevyfakturovaných skutočných predajov nie je prepojené.
- Tlačidlo **Obnoviť skutočné hodnoty** vo formulári **Projekt** neobnoví **Skutočný počet hodín úlohy**.
- Doplnok **PreValidateProjectTeamMemberCreate** môže vytvoriť duplicitné všeobecné rezervovateľné zdroje, ak je atribút **msdyn_isgenericresourceprojectscoped** nastavený na hodnotu **False**.
- **Prepočítať** slúži na vymazanie fakturovateľných nákladov podrobností o riadku cenovej ponuky na základe produktu a podrobností o riadku zmluvy.
- V určitých situáciách ukazuje doplnok **PostEstimateLineUpdate** chybu nulovej referenčnej výnimky.
- Trvanie časovej fázy na **Grafe analýzy ziskovosti** sa nezhoduje s trvaním nákladov v podrobnostiach o riadku cenovej ponuky s pevnou cenou.
- Jednotka a jednotková skupina nemajú správnu predvolenú hodnotu pre kategórie výdavkov vo formulároch **Podrobnosti o riadku zmluvy** a **Podrobnosti o riadku cenovej ponuky**.
- Zoznamy **Obstarávacej ceny organizačnej jednotky** umožňujú prekrývanie účinnosti podľa dátumu.
- Používatelia nemajú povolené meniť hodnotu **OrgUnit**, keď typ objednávky nie je pracovný, pretože to bude mať za následok chybu nulovej referenčnej výnimky.
- Pri pokuse o navigáciu z formulára **Podrobnosti o riadku cenovej ponuky** späť do formulára **Cenová ponuka** sa formulár obnoví a zobrazí sa karta **Zhrnutie**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]