---
title: Čo je nové október 2022 – Nasadenie Project Operations lite
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní nasadenia Microsoft Dynamics 365 Project Operations lite z októbra 2022.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806767"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Čo je nové október 2022 – Nasadenie Project Operations lite

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.57.0.176

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

| Oblasť funkcií | Názov funkcie | Ďalšie informácie |
| --- | --- | --- |
| Plánovanie a sledovanie projektu | **Externé plánovanie projektových operácií**<br>Režim externého plánovania umožňuje zákazníkom natívne vytvárať, aktualizovať a odstraňovať entity, ktoré súvisia so štruktúrami rozdelenia práce (WBS) pomocou natívnych Dataverse API, bez aktuálnych obmedzení, ktoré vynucuje Project for the Web. . | [Externé plánovanie](/dynamics365/project-operations/project-management/external-scheduling) |
| Nasadenie a konfigurácia | <p>**Umožnite zákazníkom vybrať si typ nasadenia**<br>Produktom riadené aktualizácie (PDU) Project Operations sa používajú na automatickú inštaláciu riešenia Project Operations Dual-write, keď sú v prostredí nainštalované riešenia Dual-write core a orchestrácie.</p><p>Táto funkcia predstavuje nový parameter **Správanie pri aktualizácii riešenia** v parametroch projektu. Keď je tento parameter nastavený na **Len Lite**, PUD už nebudú automaticky inštalovať riešenie Project Operations s duálnym zápisom, aj keď sú v prostredí nainštalované riešenia s duálnym zápisom a orchestrácia. Toto správanie bude prínosom pre zákazníkov, ktorí plánujú používať riešenia s duálnym zápisom na integráciu predajných objednávok do finančných a prevádzkových aplikácií, ale chcú používať Project Operations v zjednodušenom režime (to znamená bez integrácie do finančných a prevádzkových aplikácií).</p> | |

## <a name="quality-updates"></a>Aktualizácie kvality

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2316317 | Systém umožňuje vytvárať faktúry, ktoré nemajú žiadne zúčtovateľné transakcie. |
| Fakturácia a tvorba cien | 2737300 | Pred otvorením formulára overte dostupnosť poľa zákazníka. |
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
| Správa zdrojov | 2751560 | Nekonzistentné preferované organizačné jednotky v požiadavke na zdroj. |
| Subdodávateľské zmluvy | 2907231 | Fáza procesu faktúr dodávateľa nemôže postúpiť. |
| Čas a výdavky | 2867363 | Záznamy nevypadnú zo zobrazenia Neprítomnosti/Dovolenky na schválenie, keď sú zaradené do poradia na schválenie. |
| Čas a výdavky | 2894405 | TESA: Nepoužívaný adresár POC spôsobuje problémy s dodržiavaním predpisov. |
