---
title: Čo je nové v januári 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní Project Operations z januára 2021, pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9d54d5fed6e8ec1535ad798073ac8a1eec36e87d1dbba4cc4acd94d8bbdc5157
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008110"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v januári 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_


Táto téma sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

  - Project Operations v prostredí Dataverse verzie 4.6.0.154
  - Projektový manažment a účtovanie v prostredí Dynamics 365 Finance verzie 10.0.16

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| **Nasadenie a konfigurácia** | 2106818 | Opravené premenovanie webového zdroja, ktoré spôsobovalo problémy spojené s prispôsobením stránky. |
| **Fakturácia a tvorba cien** | 2091908 | Opravená viditeľnosť možností **Zablokovať ceny** a **Použiť aktuálne ceny** na stránke **Faktúra**, keď je aplikácia Project Operations nainštalovaná spolu s Dynamics 365 Field Service. |
| **Fakturácia a tvorba cien** | 2103058 | Obnovená možnosť **Súčty projektu** na spracovanie nulových hodnôt skutočných nákladov v úlohe. |
| **Fakturácia a tvorba cien** | 2116100 | Vylepšené chybové hlásenia používané s funkciou **Správne zadania v skutočných hodnotách**. |
| **Fakturácia a tvorba cien** | 2116129 | Vylepšená viditeľnosť odhadov výdavkov na karte **Odhady** na stránke **Projekty**. |
| **Fakturácia a tvorba cien** | 2119112 | Opravená agregácia skutočných predajov a skutočných nákladov pri použití rôznych výmenných kurzov. |
| **Fakturácia a tvorba cien** | 2134705 | Opravená chyba „Vlastnosť sa nedá prečítať **getResourceString** z nedefinovaného“, keď je otvorená stránka **Faktúra** a nainštalovaná služba Field Service. |
| **Správa príležitostí** | 2022195 | Fakturačná mriežka na základe úlohy na stránke **Projekt** obsahuje ikonu označujúcu, že s touto úlohou je spojený riadok zmluvy alebo cenovej ponuky. |
| **Správa príležitostí** | 2029135 | Opravená chyba obchodného procesu, ktorá sa vyskytla, keď sa používateľ pokúsil otvoriť riadok faktúry na potvrdenej faktúre, ktorá má fakturovanú zálohu. |
| **Správa príležitostí** | 2040713 | Opravená chyba skriptu, ktorá sa vyskytla pri vytváraní faktúry zo zmluvy a je nainštalovaná služba Field Service. |
| **Plánovanie a sledovanie projektu** | 2090202 | Označené obchodné pravidlá, ktoré sa už nepoužívajú ako **Zastarané**. |
| **Čas a výdavky** | 2091249 | Sprísnené ovládacie prvky, aby používatelia nemohli zmeniť úlohu pri zadanom alebo schválenom zadaní času. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v Dynamics 365 Finance

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| **Projektový manažment a účtovníctvo** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Nesprávna zmluvná suma na stránke **Na účet** pre projekt s pevnou cenou s viacerými zdrojmi financovania. |
| **Projektový manažment a účtovníctvo** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Zástupný symbol **Invoiceproposal.PSAnfRefProjId** nezobrazuje ID projektu pre pracovný postup **Skontrolujte návrhy projektových faktúr**. |
| **Projektový manažment a účtovníctvo** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Pri účtovaní návrhov projektových faktúr sa používa nesprávny dátum peňažnej zľavy. |
| **Projektový manažment a účtovníctvo** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Odstránenie a načítanie priradenia zdrojov v Project Operations zdvojnásobí položky prognózy projektu v aplikácii Finance. |
| **Projektový manažment a účtovníctvo** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | V Project Operations nemôžete v aplikácii Dataverse vytvoriť odhady projektu bez toho, aby ste mali na projekte riadok zmluvy. |
| **Projektový manažment a účtovníctvo** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Keď sa náklady zaúčtujú do zostatku, finančná dimenzia transakcie výdavkov na projekt sa nesynchronizuje s príslušným poukazom a účtovným rozdelením výkazu výdavkov. |
| **Projektový manažment a účtovníctvo** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Filter **Stav faktúry** v zaúčtovaných transakciách projektu pre projekty s pevnou cenou nefunguje. |
| **Projektový manažment a účtovníctvo** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminácia reverzného odhadu nefunguje v sekcii **Pravidelné**. |
| **Projektový manažment a účtovníctvo** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Riadky návrhu faktúry je možné v Project Operations vymazať, ak sú integrované v aplikácii Dataverse. |
| **Projektový manažment a účtovníctvo** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Zabránenie povoleniu funkcie viacerých riadkov zmluvy bez integrácie Dataverse. |
| **Projektový manažment a účtovníctvo** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Ak sa fakturácia na účet rovná zisku a strate, fakturovaný príjem je na stránke Odhady uvedený ako nulový. |
| **Projektový manažment a účtovníctvo** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Opravy faktúr nefungujú v integrovaných prostrediach. |
| **Projektový manažment a účtovníctvo** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Pri zaúčtovaní WIP – hodnota predaja vo vnútropodnikovej fakturácii projektu je vybraný nesprávny účet. |
| **Projektový manažment a účtovníctvo** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | V Project Operations nie je možné aktualizovať závislosti na odhadovaných úlohách v Dataverse. |
| **Projektový manažment a účtovníctvo** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Opakované odstraňovanie denníkov integrácie Project Operations v aplikácii Finance vedie k strate údajov. |
| **Projektový manažment a účtovníctvo** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Pri zaúčtovaní návrhu faktúry projektu sa vyskytne nasledujúca chyba: „Transakcia sa nevyrovná v mene prehľadu, keď sa pridá odpočítaná zálohová faktúra“. |
| **Projektový manažment a účtovníctvo** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | V Project Operations je zahrnuté Chybné ID projektu v odpočtoch po aktualizácii predvolenej zmluvy o projekte. |
| **Projektový manažment a účtovníctvo** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Ak je povolená aplikácia Project Operations, odhad a výnosy nemožno dokončiť. |
| **Projektový manažment a účtovníctvo** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | V aplikácii Project Operations odstránenie projektu zo zmluvy nevynuluje predvolený projekt zmluvy. |
| **Projektový manažment a účtovníctvo** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | V aplikácii Project Operations sa na medzipodnikovej faktúre zobrazujú nesprávne riadky výdavkov v zozname **Pridať riadok**. |
| **Cestovanie a výdavky** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Riadky výdavkov nemožno zaúčtovať, pretože v riadku zmluvy chýba nastavenie hodín. |
| **Cestovanie a výdavky** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Ak je overenie projektu/kategórie povinné, kategórie výdavkov spojené s projektom sa v prehľade výdavkov nezobrazia. |
| **Cestovanie a výdavky** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Zostatok hotovostnej zálohy sa neaktualizuje, keď sa výkaz výdavkov zaúčtuje po riadkoch. |
| **Cestovanie a výdavky** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Úloha **Aktualizovať informácie o platbe** zlyhá po zrušení vyrovnaní, keď bola faktúra vyrovnaná s dvoma alebo viacerými platobnými transakciami. |
| **Cestovanie a výdavky** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Nastáva problém s výpočtom redukcie jedla v posledný deň pre kategóriu výdavkov na diéty. |
| **Cestovanie a výdavky** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Zostava **Typ výdavkov na zamestnanca** nezobrazuje rozpis výdavkov, ak bolo prvé pripojenie používateľa v jazyku es-MX. |
| **Cestovanie a výdavky** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Platba dodávateľa za faktúru výkazu výdavkov používa na zaúčtovanie vyrovnania nesprávny súhrnný účet. |
| **Cestovanie a výdavky** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Keď sú zostavy výdavkov zaúčtované so zapnutým nastavením **Povoliť zoskupovanie transakcií na základe účtu s offsetovými platbami** a **Oprava účtovného dátumu pri zaúčtovaní**, účtovné dátumy nie sú zoskupené v tabuľke **Účtovné prerozdelenie**, čo ovplyvňuje záznamy o dani z obratu |
| **Cestovanie a výdavky** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Mapovanie podkategórie výdavkov sa odstráni, keď je začiarkavacie políčko Použiť na náklady zrušené a potom znova začiarknuté. |
| **Cestovanie a výdavky** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Výkaz medzipodnikových výdavkov nie je možné vytvoriť, ak je ID projektu pridané na úrovni hlavičky. |
| **Cestovanie a výdavky** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Nastal problém s platbami výdavkov, keď je suma výdavkov vyššia ako suma v hotovosti. |
| **Cestovanie a výdavky** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Pole **ID projektu** v rámci výkazu medzipodnikových výdavkov je prázdne, ak je rola používateľa priradená konkrétnej organizácii. |
| **Cestovanie a výdavky** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Pri pridávaní nového riadku výdavkov je kategória výdavkov uzamknutá. |
| **Cestovanie a výdavky** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Položkovanie riadkov výkazu výdavkov, ktoré sú už rozdelené, vedie k neúplnému zaúčtovaniu záväzkov\kupónu hlavnej knihy. Z dôvodu duplikácie **TRVEXPTRANS.SOURCEDOCUMENTLINE** je nefunkčný aj prieskumník zdrojov účtovníctva. |
| **Cestovanie a výdavky** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Index pridaný do tabuľky **TRVREQUISITIONLINE**, pre ktorú má zákazník duplikáty, má za následok chybu počas aktualizácie. |
| **Cestovanie a výdavky** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | V aplikácii Project Operations nie je možné vytvoriť alebo schváliť čas s medzipodnikovými úlohami v Dataverse. |

## <a name="regulatory-updates"></a>Regulačné aktualizácie

Informácie o regulačných aktualizáciách pre aplikácie Finance and Operations sú uvedené v časti [Regulačné aktualizácie](/dynamics365/finance/localizations/regulatory-updates). Môžete sa tiež prihlásiť do LCS a pozrieť si plánované regulačné aktualizácie pomocou nástroja na vyhľadanie problému. Vyhľadávanie problémov vám umožňuje vyhľadávať podľa krajiny, typu funkcie a vydania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]