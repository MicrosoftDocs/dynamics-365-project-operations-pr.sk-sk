---
title: Čo je nové alebo zmenené v Project Operations, október 2021 pre scenáre na sklade/výrobe
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú dostupné vo vydaní Project Operations z októbra 2021 pre scenáre na sklade/výrobe.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 449cab5880c29cf110c9c5a266cbb4b102b5fc83
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818329"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Čo je nové alebo zmenené v Project Operations, október 2021 pre scenáre na sklade/výrobe

_**Vzťahuje sa na:** Project Operations pre scenáre založené na zdrojoch/výrobe_

Táto téma sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Projektový manažment a účtovníctvo v prostredí Dynamics 365 Finance verzia 10.0.22
 
## <a name="quality-updates"></a>Aktualizácie kvality

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
|--------------|------------------|----------------|
| Projektový manažment a účtovníctvo | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Rozpracovaná práca na projekte (WIP) a sumy časovo rozlíšených výnosov nie sú správne stornované, keď sa zaúčtuje medzipodniková zákaznícka faktúra. |
| Projektový manažment a účtovníctvo | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | The **Zabráňte uzavretiu projektu, ak existujú otvorené transakcie** funkčnosť nefunguje. |
| Projektový manažment a účtovníctvo | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Klasifikácia fakturácie na faktúre s voľným textom automaticky nevypĺňa dimenzie z projektov, keď je táto funkcia povolená. |
| Projektový manažment a účtovníctvo | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | V scenároch, ktoré sa netýkajú medzipodnikov, nie sú sumy WIP a časovo rozlíšené príjmy správne stornované pri zaúčtovaní projektovej faktúry. |
| Projektový manažment a účtovníctvo | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Debetné a kreditné hodnoty sa prepnú, keď sa doplnok Microsoft Excel použije s denníkom výdavkov projektu a **Typ ofsetového účtu** pole je nastavené na **Projekt**. |
| Projektový manažment a účtovníctvo | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Suma, ktorá je zaúčtovaná v projektových transakciách, je nadhodnotená v objednávke projektu, ktorá zahŕňa skladové položky a ktorá má neodpočítateľné sumy dane, keď **UseTax** je označený. |
| Projektový manažment a účtovníctvo | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Systém rozdelí sumu medzi výkazy ziskov a strát projektu a výkazy WIP projektu. |
| Projektový manažment a účtovníctvo | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Po úprave požiadavky na čiastočne vrátenú položku je inventár na sklade nesprávny. |
| Projektový manažment a účtovníctvo | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Názvy zdrojov sú duplikované v Project Operations, keď sú upravované v Microsoft Project. |
| Projektový manažment a účtovníctvo | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Medzipodnikové výkazy výdavkov, ktoré majú medzipodnikové účty splatné náklady na faktúru dodávateľa, sa najskôr zaúčtujú do **Náklady na WIP projektu** typ príspevku. Počas spracovania sa však náklady súvisiace s odhadom účtujú na **Náklady na projekt** typ príspevku namiesto očakávaného **Medzipodnikové náklady** typ príspevku. |
| Projektový manažment a účtovníctvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Výsledky udržania dodávateľa v transakciách nákladov projektu sa nezobrazujú. |
| Projektový manažment a účtovníctvo | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Časový výkaz musí zaokrúhliť sumu transakcie v mene transakcie na určený počet desatinných miest na všetkých účtovných distribúciách a položkách prideľovania všeobecných účtov. |
| Projektový manažment a účtovníctvo | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Množstvo požiadaviek na položky projektu sa automaticky aktualizuje, keď sú plánované objednávky splnené. |
| Projektový manažment a účtovníctvo | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Číslo kupónu, zostatok dodávateľa typu transakcie a číslo účtu nemožno stornovať na preddavkovej faktúre nákupnej objednávky. |
| Projektový manažment a účtovníctvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Medzipodniková faktúra dodávateľa je poškodená, keď je zapnutá integrácia faktúry dodávateľa. |
| Projektový manažment a účtovníctvo | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Keď vytvoríte denník výdavkov projektu, suma nákladov sa zobrazí v **Kredit** lúka. |
| Projektový manažment a účtovníctvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Platobné podmienky na projektových faktúrach nefungujú podľa očakávania. |
| Projektový manažment a účtovníctvo | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Poukazy časového rozvrhu možno opätovne použiť, keď je číselná postupnosť nastavená ako súvislá. |
| Projektový manažment a účtovníctvo | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCÚZSKO: The **Manuálne zadržiavacie množstvo** logika nezodpovedá **Automatická suma zadržania** logiky v návrhu faktúry Projektovej zmluvy. |
| Projektový manažment a účtovníctvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Po uvoľnení zadržania dodávateľa má účtovanie poukážky nesprávne ďalšie riadky. |
| Projektový manažment a účtovníctvo | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Keď **Dátum vystavenia faktúry** pole na **Vytvorte návrh faktúry** sa stránka zmení, môže sa vyskytnúť nasledujúca chyba: "Odkaz na objekt nie je nastavený na inštanciu objektu." |
| Projektový manažment a účtovníctvo | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Pri pokuse o schválenie časového výkazu z **TSLine** pracovný tok a pre sobotu a nedeľu existuje zásada časového rozvrhu. |
| Projektový manažment a účtovníctvo | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Typ položky projektu počiatočného zostatku je vylúčený **Súhrny transakcií návrhu faktúry** keď je vypočítaný súčet faktúry návrhu faktúry. |
| Projektový manažment a účtovníctvo | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ak sú náklady na spotrebu vo výrobnej zákazke projektu 0 (nula), pri pokuse o odhad sa vyskytne nasledujúca chyba: "Pokus o delenie nulou." |
| Projektový manažment a účtovníctvo | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Mobilná aplikácia Project Timesheet pre Android prestane reagovať. Problém súvisí s **TimeEntryDataManager ArgumentNullException**. |
| Projektový manažment a účtovníctvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Denník integrácie Project Operations zlyhá, keď ho zaúčtujete, pretože v účte chýbajú dimenzie. Účet, ktorému chýbajú rozmery, však nie je účtom, do ktorého odosielate. |
| Projektový manažment a účtovníctvo | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | The **Randiť** filter vo vyhľadávaniach sa nevymaže, keď je odstránený z **Vyberte** dialógové okno na **Poštovné náklady** stránku. |
| Projektový manažment a účtovníctvo | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Obnoviť celú distribúciu** zlyhá a zobrazí chybu pre časové výkazy, ktoré sú vytvorené pre projekt **Iba čas** typu. |
| Projektový manažment a účtovníctvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | The **Projekt** kartu nie je možné upravovať na čakajúcej faktúre dodávateľa, keď je k položke priradená kategória obstarávania. |
| Projektový manažment a účtovníctvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigačná tabla chýba, ak nie ste prihlásení do Project Operations Dataverse. |
| Projektový manažment a účtovníctvo | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Pri transakciách úpravy medzipodnikových projektov existujú problémy v cieľovej spoločnosti. |
| Projektový manažment a účtovníctvo | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Viazané náklady na projekt vypočítavajú nesprávne množstvo a nákladovú cenu, ak bola objednávka spracovaná spoločnosťou **Proces nákupnej objednávky na konci roka** v hlavnej knihe. |
| Projektový manažment a účtovníctvo | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Keď sa projektová výrobná zákazka, ktorá obsahuje zákazky kvality, vykáže ako dokončená, vyskytne sa nasledujúca chyba: „Žiadna virtuálna transakcia označená transakciou zásob.“ |
| Projektový manažment a účtovníctvo | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Keď sa zaúčtuje faktúra týkajúca sa projektu, vyskytne sa nasledujúca chyba: "Vyčíslený text Projekt - náklady - položka neexistuje." |
| Projektový manažment a účtovníctvo | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Pri ručnom nahromadení výnosov sa nepriame náklady zdvojnásobia. |
| Projektový manažment a účtovníctvo | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Akruálne príjmy a účtovanie WIP nevytvára transakcie. |
| Projektový manažment a účtovníctvo | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivácia čakajúcej ceny zlyhá pre štandardnú nákladovú položku, keď existuje prijatá objednávka projektu. |
| Projektový manažment a účtovníctvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Prevrátená hodnota WIP z účtovania faktúry sa líši od pôvodne zaúčtovanej hodnoty WIP z časového záznamu. |
| Projektový manažment a účtovníctvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Existuje problém zaúčtovania pre výnosy fakturované za projekt v prípadoch aplikovaných záloh, kde transakcie na poukážke nie sú v rovnováhe. |
| Projektový manažment a účtovníctvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Vytvorenie odhadu po zaúčtovaní návrhu faktúry blokuje import opravných riadkov v Projektových operáciách. |
| Projektový manažment a účtovníctvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Úprava plne fakturovaného medzníka by nemala byť možná. |
| Projektový manažment a účtovníctvo | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Keď sa použijú automatické poplatky, medzipodnikovú zákaznícku faktúru za časový výkaz nemožno zaúčtovať a zobrazí sa chybové hlásenie. |
| Projektový manažment a účtovníctvo | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adresa v podprojekte nie je správne aktualizovaná. |
| Projektový manažment a účtovníctvo | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Nákladová cena pre požiadavky na položky sa aktualizuje s nákupnou cenou pre konsolidované nákupné objednávky. |
| Projektový manažment a účtovníctvo | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Zaúčtovaná cena nie je správna po aktualizácii nákupnej ceny a parametra **Aktivujte riadenie zmien** je umožnené. |
| Cestovanie a výdavky | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Všetky používateľské výdavky sa zobrazia pri vyhľadávaní kategórie v mobilnej aplikácii Výdavky. |
| Cestovanie a výdavky | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nesprávne sumy transakcií dodávateľa a transakcií dane z obratu sa účtujú z nákladu, ktorý bol vytvorený z transakcie kreditnou kartou. |
| Cestovanie a výdavky | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Keď obnovíte stránky výkazu výdavkov, zobrazí sa irelevantné varovné hlásenie. |
| Cestovanie a výdavky | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Keď odstránite dočasného schvaľovateľa a potom ho znova odošlete prostredníctvom pracovného postupu, použije sa nesprávny dočasný schvaľovateľ. |
| Cestovanie a výdavky | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Vyskytne sa chyba účtovania, ktorá súvisí s nastavením najazdených kilometrov. |
| Cestovanie a výdavky | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribúcia neaktualizuje právnickú osobu, keď sa nepripojená transakcia znovu pridá do výkazu výdavkov o medzipodnikových nákladoch. |

### <a name="regulatory-updates"></a>Regulačné aktualizácie

Informácie o regulačných aktualizáciách pre aplikácie Finance and Operations nájdete na [Regulačné aktualizácie](/dynamics365/finance/localizations/regulatory-updates). Môžete sa tiež prihlásiť do Microsoft Dynamics Lifecycle Services (LCS) a použiť nástroj na vyhľadávanie problémov na zobrazenie plánovaných regulačných aktualizácií. Vyhľadávanie problémov vám umožňuje vyhľadávať podľa krajiny alebo regiónu, typu funkcie a vydania.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
