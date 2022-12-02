---
title: Konfigurácia parametrov správy výdavkov
description: Tento článok popisuje parametre, ktoré riadia všeobecné správanie v správe výdavkov.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 6432e119f38071b028c013561bab99820778a11d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931487"
---
# <a name="configure-expense-management-parameters"></a>Konfigurácia parametrov správy výdavkov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok popisuje parametre riadiace všeobecné správanie v správe výdavkov.

## <a name="general"></a>Všeobecné

| Pole                                                    | Popis |
|----------------------------------------------------------|-------------|
| Štandardná sadzba na najazdené kilometre                                 | Zadajte sadzbu náhrady výdavkov na najazdené kilometre. Táto sadzba sa vynásobí počtom kilometrov, ktoré sa zadajú do výdavku na výpočet sumy, ktorá sa refunduje za cestovné náklady. |
| Overiť účel výdavkov                                 | Zapnutím tejto možnosti obmedzíte používateľov na existujúcu množinu hodnôt nakonfigurovanú v poli **Účel výkazu výdavkov** pri vytváraní výkazov výdavkov. |
| Osobné výdavky uhradené osobou                                | Vyberte, kto je zodpovedný za zaplatenie všetkých čiastok transakcií kreditnou kartou, ktoré sú kategorizované ako osobné. |
| Zobraziť celú správu o výdavkoch pri návrate               | Vyberte túto možnosť, ak chcete zobraziť všetky výdavky výkazu výdavkov, keď sa zobrazia podrobnosti pôvodného dokumentu pre konkrétny poukaz, ktorý bol vygenerovaný pri zaúčtovaní výkazu výdavkov. |
| Predbežná autorizácia cesty je povinná                 | Vyberte túto možnosť, ak chcete, aby zamestnanec mohol predložiť správu o výdavkoch, aby bola predložená a schválená cestovná požiadavka. |
| Pred uverejnením príspevku povoľte úpravy distribúcií            | Vyberte, či možno rozdelenia výkazu výdavkov upravovať pred jeho zaúčtovaním. |
| Vyhodnoťte politiky riadenia výdavkov                     | Vyberte, kedy sa majú výdavky vyhodnocovať, aby ste určili, či došlo k porušeniu politiky výdavkov. Porušenie výdavkov je možné vyhodnotiť pri zadaní a uložení záznamu o výdavkoch alebo po predložení výdavku na schválenie. Po uložení riadku výdavkov sa vyhodnotia pravidlá politiky pre požadované potvrdenia. |
| Povoliť medzipodnikové výdavkové riadky                         | Vyberte, či je možné do výkazu výdavkov zahrnúť výdavky pre iné právnické osoby. |
| Povoliť úpravy výmenného kurzu výdavkov kreditnej karty | Vyberte túto možnosť, aby ste používateľovi umožnili upravovať výmenný kurz importovaných výdavkov na kreditnú kartu. |
| Polia viacúrovňovej hierarchie, ktoré sa majú zobraziť                  | Vyberte, ktoré polia schvaľovateľa sa zobrazia, keď je typ priradenia pracovného postupu nastavený na hierarchiu, a výber **Hierarchia** je nastavený na použitie hierarchie schvaľovania, viacúrovňového schválenia výdavkov. Keď sa pre pracovný postup použije viacúrovňová schvaľovacia hierarchia, vybraté polia sa zobrazia vo výkaze výdavkov a je možné ich upravovať. |
| Zadajte číslo kreditnej karty zamestnanca                        | Vyberte, či možno zadať 15-znakové alebo 16-znakové číslo a uložiť ho do poľa **ID karty** na stránke **Kreditné karty** pre zamestnanca. |
| Potvrďte účel žiadosti o cestu                      | Zapnutím tejto možnosti obmedzíte používateľov na existujúcu množinu hodnôt nakonfigurovanú v poli **Účel výkazu výdavkov** pri vytváraní cestovných požiadaviek. |

## <a name="financial"></a>Financial

| Pole                                                                                    | Popis |
|------------------------------------------------------------------------------------------|-------------|
| Názov denného účtovného denníka hlavnej knihy                                                                | Vyberte názov denníka hlavnej knihy, do ktorého sa účtujú schválené výkazy výdavkov. |
| Povoliť vrátenie daní z výdavkov                                                        | Vyberte túto možnosť, ak chcete povoliť vrátenie dane z výdavkov pre oprávnené výdavky. Túto možnosť nie je možné zvoliť, ak sú povolené americké dane z obratu a dane z používania. |
| Okamžité zverejnenie platby vopred v hotovosti                                                           | Vyberte túto možnosť, ak chcete po dokončení procesu platby a prevodu zaúčtovať schválenú platbu vopred v hotovosti. Ak táto možnosť nie je vybratá, proces platby a prevodu vygeneruje nezverejnený všeobecný denník. |
| Správny účtovný dátum počas zverejnenia                                                   | Vyberte túto možnosť, ak chcete aktualizovať účtovný dátum pri zaúčtovaní výdavkov, ak je súčasné obdobie pozastavené alebo uzavreté. Účtovný dátum bude nastavený na nasledujúce otvorené obdobie. |
| Povoliť zoskupovanie transakcií na základe účtu s odchýlkami uvedeného v spôsobe platby       | Vyberte túto možnosť, ak chcete zosumarizovať nákladové transakcie pre výkaz výdavkov na základe účtu s odchýlkami, ktorý je uvedený v spôsobe platby pre výdavky. |
| Vrátane dane                                                                             | Vyberte túto možnosť, ak chcete do sumy výdavkov predvolene zahrnúť daň z predaja. |
| Uvoľniť ťarchy pri zatváraní cestovných požiadaviek                                      | Vyberte túto možnosť, aby ste uvoľnili zaťažené prostriedky po zatvorení schválenej cestovnej požiadavky. |
| Povoliť predloženie cestovnej požiadavky pri prekročení rozpočtu pre register rozpočtu a rozpočet projektu | Vyberte túto možnosť, aby ste zamestnancom umožnili predkladať cestovné požiadavky na schválenie, aj keď presahujú povolený rozpočet nastavený v registri rozpočtu alebo povolený rozpočet projektu. |
| Povoliť predloženie výkazu výdavkov pri prekročení rozpočtu pre register rozpočtu a rozpočet projektu     | Vyberte túto možnosť, aby ste zamestnancom umožnili predkladať výkazy výdavkov na schválenie, aj keď presahujú povolený rozpočet nastavený v registri rozpočtu alebo povolený rozpočet projektu. |
| Povoliť schválenie výkazu výdavkov pri prekročení rozpočtu iba pre register rozpočtu                 | Vyberte túto možnosť, aby ste schvaľovateľom umožnili schvaľovať výkazy výdavkov, ktoré presahujú povolený rozpočet nastavený v registri rozpočtu. |

## <a name="per-diem"></a>Denne

| Pole                                 | Popis |
|---------------------------------------|-------------|
| Minimálne hodiny pre diéty            | Zadajte predvolený minimálny počet hodín, ktoré musí zamestnanec za deň odpracovať, aby mohol dostávať diéty za cestovné náklady. Táto hodnota sa používa ako predvolená hodnota iba pre pole **Minimálne hodiny** pre úrovne denných diét. |
| Percento jedla                          | Zadajte predvolené percento diét ktoré sa používa v prvý a posledný deň výdavkov spojených s cestovaním, keď je pole **Vypočítať zníženie stravného o** je nastavené buď na **Typ jedla za deň** alebo **Počet jedál za deň**. Pracovný deň v prvý a posledný deň môže byť kratší ako štandardný pracovný deň. Preto sa výška diét v tieto dni môže líšiť od štandardnej sumy. Ak je percento nastavené na **0** (nula), odpočty za prvý a posledný deň budú 0,00. |
| Percentá pre hotel                         | Zadajte predvolené percento diéty pre hotely, ktoré sa používajú v prvý a posledný deň výdavkov spojených s cestovaním. Pracovný deň v prvý a posledný deň môže byť kratší ako štandardný pracovný deň. Preto sa výška diét v tieto dni môže líšiť od štandardnej sumy. Ak je percento nastavené na **0** (nula), odpočty za prvý a posledný deň budú 0,00. |
| Ostatné percentá                         | Zadajte predvolené percento diéty pre rôzne výdavky, ktoré sa používajú v prvý a posledný deň výdavkov spojených s cestovaním. Pracovný deň v prvý a posledný deň môže byť kratší ako štandardný pracovný deň. Preto sa výška diét v tieto dni môže líšiť od štandardnej sumy. Ak je percento nastavené na **0** (nula), odpočty za prvý a posledný deň budú 0,00. |
| Zníženie percenta na raňajky | Zadajte čiastku, o ktorú sa diéty znižujú na raňajky. Napríklad, ak zamestnanec dostane bezplatné raňajky, možno budete chcieť znížiť sumu diét o 10 percent. |
| Zníženie percenta na obed     | Zadajte čiastku, o ktorú sa diéty znižujú na obed. Napríklad, ak zamestnanec dostane bezplatný obed, možno budete chcieť znížiť sumu diét o 15 percent. |
| Zníženie percenta na večeru    | Zadajte čiastku, o ktorú sa diéty znižujú na večeru. Napríklad, ak zamestnanec dostane bezplatnú večeru, možno budete chcieť znížiť sumu diét o 25 percent. |
| Vypočítať zníženie jedla o           | Zadajte, ako má systém vypočítať zníženie denných diét výberom, či je zníženie založené na type jedla na cestu alebo na deň, alebo či je založené na počte povolených jedál za deň. |
| Zaokrúhľovanie diét                     | Vyberte typ zaokrúhľovania, ktorý sa použije pri výdavkoch na diéty. Ak vyberiete bežné zaokrúhľovanie, všetky náklady na diéty, ktoré majú čiastku 0,50, sa zaokrúhlia na 1,00 a všetky diéty, ktoré majú menej ako 0,50, sa zaokrúhlia nadol na 0,00. |
| Výpočet základu diéty na          | Vyberte, či sa výška diéty zakladá na kalendárnom dni alebo 24-hodinovom období. |

## <a name="fax-cover-pages"></a>Titulné strany faxu

| Pole                          | Popis |
|--------------------------------|-------------|
| Pokyny                   | Zadajte pokyny, ktoré musia zamestnanci dodržiavať pri vytváraní titulnej stránky pre fax, ktorý sa používa na odosielanie potvrdeniek týkajúcich sa výkazu výdavkov. Ak chcete zadať text, ktorý sa zobrazí v konkrétnom jazyku, na základe jazyka používateľa, zvoľte **Preklady**. |
| ID používateľa (informácie o čiarovom kóde) | Vyberte túto možnosť, ak chcete uložiť jedinečný identifikátor zamestnanca do čiarového kódu použitého na titulnej strane faxu. |
| Čiarový kód                       | Vyberte čiarový kód, ktorý sa použije na titulnej strane faxu. V správe výdavkov sú podporované čiarové kódy 39 a 128. |

## <a name="anti-corruption"></a>Protikorupčné opatrenia

| Pole                                 | Popis |
|---------------------------------------|-------------|
| Zobraziť protikorupčné osvedčenie   | Vyberte túto možnosť, ak chcete zobraziť protikorupčný text pri vytváraní výkazu výdavkov. Potom je možné povoliť konkrétne kategórie výdavkov, ktoré budú vyžadovať výber protikorupčného osvedčenia vo výkaze výdavkov. Napríklad kategória darčekov, ktorá sa týka výdavkov vládnej organizácie, môže vyžadovať, aby zamestnanec potvrdil, že výdavky zodpovedajú politike spoločnosti, ktorá sa týka úradníkov vládnej organizácie. |
| Protikorupčná správa pre zadávateľa | Zadajte text, ktorý by sa mal zobraziť zamestnancovi, ktorý vytvára výkaz výdavkov. Ak chcete zadať text, ktorý sa zobrazí v konkrétnom jazyku, na základe jazyka používateľa, zvoľte **Preklady**. |
| Protikorupčná správa pre schvaľovateľa  | Zadajte text, ktorý by sa mal zobraziť schvaľovateľovi pri vytvorení výkazu výdavkov. Ak chcete zadať text, ktorý sa zobrazí v konkrétnom jazyku, na základe jazyka používateľa, zvoľte **Preklady**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]