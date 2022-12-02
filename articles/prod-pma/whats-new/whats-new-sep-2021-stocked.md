---
title: Aké sú novinky alebo zmeny v Project Operations, september 2021 pre scenáre založené na zdrojoch/výrobe
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní Project Operations zo septembra 2021, pre scenáre založené na zdrojoch/výrobe.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: be0f397df4a3e1973e1f5546e43b2cf9578950a0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029871"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Aké sú novinky alebo zmeny v Project Operations, september 2021 pre scenáre založené na zdrojoch/výrobe

_**Vzťahuje sa na:** Project Operations pre scenáre založené na zdrojoch/výrobe_

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Projektový manažment a účtovníctvo v prostrední Dynamics 365 Finance, verzia 10.0.21
 
## <a name="quality-updates"></a>Aktualizácie kvality

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
|---|---|---|
| Projektový manažment a účtovníctvo | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Ak rola manažéra nákupu získa prístup k jednej právnickej osobe, získa tiež prístup ku všetkým projektom vo všetkých právnických osobách. |
| Projektový manažment a účtovníctvo | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Problém so zaokrúhľovaním dane z pridanej hodnoty (DPH) nastáva, keď je dobropis vyrovnaný oproti pôvodnej projektovej faktúre. |
| Projektový manažment a účtovníctvo | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Na overenie rozpočtu použite alternatívny rozpočet projektu. |
| Projektový manažment a účtovníctvo | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Cenová skupina **Predajná cena hodiny** nie je vypočítaná podľa štruktúry rozdelenia práce pre cenové ponuky projektov. |
| Projektový manažment a účtovníctvo | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Eliminácia odhadu zlyhá, keď funkcia **Povoliť menu projektovej zmluvy na výpočet odhadu** je aktivovaná. |
| Projektový manažment a účtovníctvo | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorizácia dane z predaja podľa množstva sa pripočíta k sume predajnej ceny, keď sa daň z použitia použije v skupine dane z predaja v denníku výdavkov projektu. |
| Projektový manažment a účtovníctvo | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Podmienená daň nie je správne vypočítaná pri poslednej platbe, keď bolo na faktúry s nákupnou objednávkou uplatnené zadržanie a platba vopred predajcu. |
| Projektový manažment a účtovníctvo | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Sledovanie úprav nefunguje pre denníky počiatočných zostatkov. |
| Projektový manažment a účtovníctvo | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Pridelenie revízie rozpočtu projektu podľa obdobia** je rozdelené na všetky rozpočtové obdobia. Po odoslaní pridelenia sa záznam nevymaže. |
| Projektový manažment a účtovníctvo | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Účty WIP zaúčtované do hlavnej knihy majú nesprávnu sumu. |
| Projektový manažment a účtovníctvo | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Schválenie denníka hodín projektu nefunguje. |
| Projektový manažment a účtovníctvo | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Ak je limit financovania neoznačený, predajná cena úpravy projektu sa neaktualizuje o nepriame náklady. |
| Projektový manažment a účtovníctvo | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Požiadavku na položku nie je možné vytvoriť, keď je hlavička tabuľky Predaj fakturovaná a záložná nákupná objednávka pre existujúce riadky bola dokončená. |
| Projektový manažment a účtovníctvo | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Suma zadržania pre pravidlo fakturácie, ktoré má míľnik pre iný projekt, nie je zaúčtovaná v zodpovedajúcom ID projektu, ktorý bol vybratý pre míľnik. Namiesto toho je zaúčtovaná s prvým projektom. |
| Projektový manažment a účtovníctvo | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Keď vyberiete **Nastavenie finančnej dimenzie** na návrhu faktúry, vyskytne sa nasledujúca chyba: „Nie je možné odovzdať objekt typu 'Dynamic.AX .Application.FormIntControl' do typu 'Dynamics.AX .Application.FormStringControl'." |
| Projektový manažment a účtovníctvo | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Zostava **faktúry za projekt** preskočí riadky. |
| Projektový manažment a účtovníctvo | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Pri výpočte kontroly nákladov pre investičný projekt sa vyskytne chyba. |
| Projektový manažment a účtovníctvo | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metóda **ProjTable::InitFromCustTable - canDeletePostalAddress** spôsobí problém s výkonom. |
| Projektový manažment a účtovníctvo | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Chybové hlásenie by malo byť jasnejšie ako „Neočakávaná chyba“. |
| Projektový manažment a účtovníctvo | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Dávková úloha zaúčtovania faktúr projektu spracuje a zaúčtuje návrh faktúry, aj keď riadky faktúry neboli vygenerované. |
| Projektový manažment a účtovníctvo | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Problém so zaokrúhľovaním sa vyskytuje, keď je konfiguračný kľúč pre verejný sektor vypnutý. Nesprávna cena alebo predajná cena sa vygeneruje v hodinách časového výkazu pre zmluvy, ktoré majú viacero zakladajúcich zdrojov. |
| Projektový manažment a účtovníctvo | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Predajná cena projektu na fakturovanej objednávke projektu je nesprávne vypočítaná, keď je ako model predajnej ceny použitý **Pomer príspevkov**. |
| Projektový manažment a účtovníctvo | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Systém neberie do úvahy aktívne dni medzi tým, keď vypočítava efektívnu mieru práce pre zamestnanca. |
| Projektový manažment a účtovníctvo | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | V medzipodnikovom časovom výkaze sa vyskytla chyba účtovania z dôvodu nasledujúcej chyby overenia: „Žiadny obchodný partner nie je nakonfigurovaný pre právnickú osobu.“ |
| Projektový manažment a účtovníctvo | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Popis z nákupnej objednávky, ktorá má kategóriu výdavkov, sa nenačíta v zozname zaúčtovaných transakcií projektu. |
| Projektový manažment a účtovníctvo | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | V denníkoch položiek, ktoré sú zaúčtované do projektu, je nesprávna konverzia. |
| Projektový manažment a účtovníctvo | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Objednávku môžete potvrdiť aj v prípade, že bol prekročený limit financovania. |
| Projektový manažment a účtovníctvo | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Po výbere ID projektu zmizne sekcia **Oprava/Zrušenie faktúry** na faktúre s voľným textom. |
| Projektový manažment a účtovníctvo | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Pri zaúčtovaní návrhu projektovej faktúry zo zákazky odberateľa projektu, ktorá obsahuje skladovú položku, dochádza k problémom s výkonom. |
| Projektový manažment a účtovníctvo | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Nákupné faktúry projektu nemožno zaúčtovať, pretože sa vyskytla nasledujúca chyba: „Funkcia AccDistProcessorProjectExtension.createForProjectRevenueLine bola nesprávne volaná.“ |
| Projektový manažment a účtovníctvo | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Aktualizujte vytvorenie dávkových úloh odhadu projektu na podporu vykonávania viacerých čiastkových úloh. |
| Projektový manažment a účtovníctvo | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Stav časového rozvrhu nie je možné aktualizovať na **Koncept**, keď je pracovný postup zaseknutý v stave **Zrušené**. |
| Projektový manažment a účtovníctvo | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Sumy zadržania nie sú vypočítané v návrhu faktúry dobropisu, ak existuje viacero riadkov. |
| Projektový manažment a účtovníctvo | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Pri pokuse o zmenu sumy na vygenerovanej faktúre z nákupnej objednávky sa vyskytne nasledujúca chyba: „Transakcie na poukážke nie sú vyrovnané podľa XX/XX/XXXX. (účtovná mena: 0,00 – mena vykazovania: 0,01).“ |
| Projektový manažment a účtovníctvo | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Pri zaúčtovaní návrhu projektovej faktúry v dávkovom režime sa vyskytne problém s výkonom z dôvodu spojenia s **GeneralJournalAccountEntry**. |
| Projektový manažment a účtovníctvo | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Pri zverejnení časového rozvrhu dochádza k problémom s výkonom. |
| Projektový manažment a účtovníctvo | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hierarchia odhadov nákladov v štruktúre rozdelenia práce nie je správne zarovnaná po rozšírení všetkých úloh alebo po manuálnom rozšírení jednej úlohy. |
| Projektový manažment a účtovníctvo | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Excelovú šablónu cenovej ponuky projektu nie je možné pridať do ponuky **Otvorte v Exceli**. |
| Projektový manažment a účtovníctvo | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Číslo oslobodené od dane pre právnickú osobu nie je zahrnuté na vytlačenej faktúre za projekt. |
| Projektový manažment a účtovníctvo | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Pri úprave projektu vo vzťahu k úverovým linkám sa vyskytne chyba „V jednotke inventára sa neaktualizujú žiadne finančné údaje“. |
| Projektový manažment a účtovníctvo | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Po použití KB 461935 nemôžete zaúčtovať odhady, ak prepnete na súvislé číselné poradie. |
| Projektový manažment a účtovníctvo | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** spôsobím že mobilná aplikácia Project timesheet pre Android prestať reagovať. |
| Projektový manažment a účtovníctvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Obrátená hodnota WIP z účtovania faktúry sa líši od pôvodnej zaúčtovanej hodnoty WIP zo zadania času. |
| Projektový manažment a účtovníctvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | V aplikovaných prípadoch zádržného sa transakcie na poukaze nevyrovnajú, keď sa zaúčtujú fakturované príjmy za projekt. |
| Projektový manažment a účtovníctvo | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Keď je povolená funkcia **Zlepšenie výkonnosti plánovania zdrojov projektu**, desatinné hodnoty sú nesprávne zaokrúhlené pre dostupnosť zdrojov a kapacitu. |
| Projektový manažment a účtovníctvo | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Keď je povolená funkcia **Vytvoriť odhady projektu pomocou viacerých dávkových úloh**, vytváranie odhadov v dávke, ktorá má viacero podúloh, funguje len pre aktuálne obdobie. |
| Cestovanie a výdavky | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Zásady týkajúce sa cestovných žiadaniek sa ignorujú a pracovný postup sa schvaľuje bez chýb. |
| Cestovanie a výdavky | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplikácia Mobile Expense neukladá do výdavkového riadku nasledujúce informácie:</p><ul><li>ID projektu</li><li>Či je výdavok zúčtovateľný</li><li>Číslo aktivity</li></ul> |
| Cestovanie a výdavky | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Pole **Priložené doklady** je nastavené na **Áno**, aj keď k výdavkovému riadku nie je priložený žiadny doklad. |
| Cestovanie a výdavky | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Pri zmene kategórie výdavkov na hodnotu **Osobné** sa zobrazí chyba. |
| Cestovanie a výdavky | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Po rozdelení transakcie kreditnou kartou na osobný výdavok nemôžete pripojiť účtenku a upraviť nadradený výdavok. |
| Cestovanie a výdavky | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Politika výdavkov pre medzipodnikové transakcie, ktoré majú ID projektu, nefunguje správne. |
| Cestovanie a výdavky | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Informácia o zaúčtovanom dátume chýba pre zaúčtované výkazy výdavkov. |
| Cestovanie a výdavky | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | V mobilnej aplikácii Výdavok sú problémy so spôsobom úhrady. |
| Cestovanie a výdavky | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Cestovnú požiadavku vytvorenú pre jedného pracovníka je možné použiť pre správu o výdavkoch iného pracovníka pred dátumom delegovania. |
| Cestovanie a výdavky | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Keď sa vytvoríte výdavok, zmeny hodnôt finančnej dimenzie sa neaktualizujú správne na úrovni účtovného rozdelenia v pracovnom priestore **Správa výdavkov**. |
| Cestovanie a výdavky | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Stav schválenia hlavného výdavkového riadku nie je synchronizovaný so stavom schválenia pracovného postupu položkových riadkov. |
| Cestovanie a výdavky | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Ak zaúčtujete výkaz výdavkov a je povolené vymáhanie dane, dôjde k chybe. |
| Cestovanie a výdavky | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Delegát nemôže odstrániť doklady o výdavkoch za prepusteného zamestnanca. |
| Cestovanie a výdavky | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Odstránenie riadku výdavkov trvá dlhšie, ako sa očakávalo, a ovplyvňuje výkon. |
| Cestovanie a výdavky | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** spôsobuje osamostatnenie záznamu **TaxUncommitted**, pretože sa vymaže iba **SourceDocumentLine**. |
| Cestovanie a výdavky | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** neumožňuje, aby **trvExpTrans.ReferenceDataAreaId** vytvorilo novú číselnú postupnosť. |

## <a name="regulatory-updates"></a>Regulačné aktualizácie

Informácie o regulačných aktualizáciách pre aplikácie na riadenie financií a prevádzok nájdete v časti [Regulačné aktualizácie](/dynamics365/finance/localizations/regulatory-updates). Môžete sa tiež prihlásiť do služby Microsoft Dynamics Lifecycle Services (LCS) a pozrieť si plánované aktualizácie právnych predpisov pomocou vyhľadávacieho nástroja problémov. Vyhľadávanie problémov vám umožňuje vyhľadávať podľa krajiny alebo regiónu, typu funkcie a vydania.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
