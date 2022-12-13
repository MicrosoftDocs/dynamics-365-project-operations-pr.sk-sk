---
title: Čo je nové Október 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní Microsoft Dynamics 365 Project Operations  z októbra 2022 pre scenáre založené na zdrojoch alebo bez zásob.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806752"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové Október 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.57.0.176
- Projektový manažment a účtovníctvo v prostrední Dynamics 365 Finance, verzia 10.0.30

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

| Oblasť funkcií | Názov funkcie | Ďalšie informácie |
| --- | --- | --- |
| Plánovanie a sledovanie projektu | **Externé plánovanie projektových operácií**<br>Režim externého plánovania umožňuje zákazníkom natívne vytvárať, aktualizovať a odstraňovať entity, ktoré súvisia so štruktúrami rozdelenia práce (WBS) pomocou natívnych Dataverse API, bez aktuálnych obmedzení, ktoré vynucuje Project for the Web. . | [Externé plánovanie](/dynamics365/project-operations/project-management/external-scheduling) |
| Nasadenie a konfigurácia | <p>**Umožnite zákazníkom vybrať si typ nasadenia**<br>Produktom riadené aktualizácie (PDU) Project Operations sa používajú na automatickú inštaláciu riešenia Project Operations Dual-write, keď sú v prostredí nainštalované riešenia Dual-write core a orchestrácie.</p><p>Táto funkcia predstavuje nový parameter **Správanie pri aktualizácii riešenia** v parametroch projektu. Keď je tento parameter nastavený na **Len Lite**, PUD už nebudú automaticky inštalovať riešenie Project Operations s duálnym zápisom, aj keď sú v prostredí nainštalované riešenia s duálnym zápisom a orchestrácia. Toto správanie bude prínosom pre zákazníkov, ktorí plánujú používať riešenia s duálnym zápisom na integráciu predajných objednávok do finančných a prevádzkových aplikácií, ale chcú používať Project Operations v zjednodušenom režime (to znamená bez integrácie do finančných a prevádzkových aplikácií).</p> | |
| Fakturácia a tvorba cien | <p>**Konverzia meny pre transakciu predaja nevyfakturovaných nákladov v integrovaných prostrediach**<br>Pre zákazníkov, ktorí používajú Project Operations integrované s finančnými a operačnými aplikáciami (t. j. v type nasadenia zdroj/nezásobené), výmenné kurzy zvyčajne ovládajú finančné a prevádzkové aplikácie. Ak by sa však mala kategória nákladov oceniť pomocou metódy výpočtu ceny „v nákladoch“ alebo „prirážka k nákladom“ pri fakturácii zákazníkovi, výmenný kurz, ktorý sa používa na výpočet sumy predaja, použije výmenné kurzy v Dataverse, nie výmenné kurzy z finančných a prevádzkových aplikácií.</p><p>Táto funkcia predstavuje nový parameter **Správanie pri prevode meny** v parametroch projektu. Keď je tento parameter nastavený na **Rozšírené o záložné**, nevyfakturované predajné sumy pri nákladových transakciách sa vypočítajú pomocou výmenných kurzov z finančných a prevádzkových aplikácií.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

V tomto vydaní nie sú k dispozícii žiadne aktualizácie máp duálneho zápisu Project Operations. Aktuálny zoznam a verzie máp duálneho zápisu Project Operations nájdete na v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../environment/resource-dual-write-maps.md).

Pri aktualizácii riešenia Project Operations Dataverse a verzie riešenia Finance vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí, no zároveň aktivujte všetky mapy príslušnej tabuľky. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spúšťaní mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky v mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v časti Sprievodca riešením problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2316317 | Systém umožňuje vytvárať faktúry, ktoré nemajú žiadne zúčtovateľné transakcie. |
| Fakturácia a tvorba cien | 2737300 | Pred vstupom do formulára overte dostupnosť polí **Zákazníka** . |
| Fakturácia a tvorba cien | 2744948 | Pridajte nulovú kontrolu pre spôsob fakturácie. |
| Fakturácia a tvorba cien | 2763515 | Popisovač chyby odkazu, keď chýba kúpna zmluva na faktúre. |
| Fakturácia a tvorba cien | 2844301 | Vytvorenie hromadnej faktúry zlyhá z dôvodu chyby. |
| Fakturácia a tvorba cien | 2845869 | Nesprávne uloženie organizačnej služby. |
| Fakturácia a tvorba cien | 2853729 | Podrobnosti roly a ceny sa aktualizujú pri zmene typu fakturácie. |
| Fakturácia a tvorba cien | 2940350 | Keď sa stanovujú skutočné ceny, mali by sa automaticky zadávať iba aktívne cenníky. |
| Nasadenie a konfigurácia | 3001206 | Entita msdyn\_ replaylogheader bráni inováciám zákazníckych organizácií. |
| Správa príležitostí | 2755582 | Rukoväť výnimiek odkazu s hodnotou Null v Pomocníkovi pravidiel rozdelenia fakturácie. |
| Správa príležitostí | 2761477 | Keď sa použije rozdelená fakturácia, odstránením míľnika (hlavičky) sa zanechajú osirotené míľniky. |
| Správa príležitostí | 2767595 | Keď sa záznam o použití materiálu otvorí v hlavnom formulári, rezervovateľný zdroj pre záznam sa zmení na aktuálne prihláseného používateľa. |
| Plánovanie a sledovanie projektu | 2790384 | Časový limit Pending OperationSet je príliš krátky. |
| Plánovanie a sledovanie projektu | 2957840 | Úlohy nie je možné ukladať a stĺpce nie je možné pridávať na stránku **Úlohy** v Integrated Project Operations. |
| Správa zdrojov | 2751560 | Nekonzistentné preferované organizačné jednotky v požiadavke na zdroj. |
| Subdodávateľské zmluvy | 2853245 | Párovanie pre skutočné hodnoty riadku faktúry dodávateľa neaktualizuje stav overenia, ak je riadok zmluvy už prepojený s riadkom faktúry dodávateľa. |
| Subdodávateľské zmluvy | 2907231 | Fáza procesu faktúr dodávateľa nemôže postúpiť. |
| Čas a výdavky | 2867363 | Záznamy nevypadnú zo zobrazenia Neprítomnosti/Dovolenky na schválenie, keď sú zaradené do poradia na schválenie. |
| Čas a výdavky | 2894405 | TESA: Nepoužívaný adresár POC spôsobuje problémy s dodržiavaním predpisov. |

### <a name="project-management-and-accounting-in-finance"></a>Projektový manažment a účtovníctvo vo Finance

Informácie o opravách zahrnutých v tejto aktualizácii nájdete po prihlásení do Microsoft Dynamics Lifecycle Services a zobrazení [článku vedomostnej databázy](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
