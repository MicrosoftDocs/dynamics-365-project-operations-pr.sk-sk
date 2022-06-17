---
title: Prehľad štruktúry rozdelenia práce
description: Štruktúra rozdelenia práce (WBS) je popis práce, ktorá sa bude robiť pre projekt. Je to hierarchia úloh, ktorá predstavuje porozumenie projektového tímu zloženiu práce a veľkosti, nákladom a trvaniu každej zložky alebo úlohy.
author: Yowelle
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f1a77c6e4e5f0926ff7afe1066f9a0cf7cdfb51
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920677"
---
# <a name="work-breakdown-structures-overview"></a>Prehľad štruktúry rozdelenia práce

[!include [banner](../includes/banner.md)]

Štruktúra rozdelenia práce (WBS) je popis práce, ktorá sa bude robiť pre projekt. Je to hierarchia úloh, ktorá predstavuje porozumenie projektového tímu zloženiu práce a veľkosti, nákladom a trvaniu každej zložky alebo úlohy. WBS má tri hlavné účely:

-   Popis členenia alebo zloženie práce v úlohách.
-   Definovanie projektu práce.
-   Odhad nákladov na každú úlohu.

Miera podrobnosti WBS závisí od úrovne presnosti požadovanej v odhadoch a úrovne sledovania, ktorá sa vyžaduje v porovnaní s týmito odhadmi. Projekty, ktoré majú veľmi nízku toleranciu voči sklzom v pláne alebo nákladoch, zvyčajne vyžadujú podrobnejšiu štruktúru WBS a dôsledné sledovanie postupu práce a nákladov oproti štruktúre WBS. Tento druh projektu je bežný v stavebnom a strojárskom priemysle. 

Naproti tomu projekty v odvetviach, ako sú médiá a reklama, softvér a IT infraštruktúra, bývajú jedinečné a produktivita závisí od skúseností a kompetencií jednotlivca, ktorý vykonáva danú úlohu. Preto tieto odvetvia používajú štruktúru WBS na získanie približnej veľkosti projektu, nie na podrobné sledovanie jeho priebehu. 

Budovanie štruktúry WBS je intenzívny proces, ktorý sa zvyčajne robí dlho, a ktorý si vyžaduje spoluprácu a informácie od najrôznejších ľudí. Tento článok popisuje, ako môžete použiť vylepšenia WBS na splnenie vašich požiadaviek na odhady a sledovanie.

## <a name="prerequisites-for-creating-a-wbs"></a>Požiadavky na vytvorenie štruktúry WBS
Ak chcete vytvoriť štruktúru WBS, musíte byť schopní vytvoriť pracovný plán a odhadnúť cenu práce.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Predpoklady pre vytvorenie pracovného plánu

Ak chcete využiť všetky možnosti plánovania funkcií štruktúry WBS, vykonajte nasledujúce nastavenie:

1.  Nastavte predvolený kalendár a kalendár projektu:
    1.  Kliknite na **Projektové riadenie a účtovníctvo** &gt; **Nastaviť** &gt; **Parametre projektového riadenia a účtovníctva** &gt; **Plánovanie**. V poli **Predvolený pracovný kalendár** zadajte predvolený kalendár. Toto bude predvolený pracovný kalendár pre každý nový projekt, ktorý sa vytvorí.
    2.  Môžete zmeniť predvolený kalendár pre konkrétny projekt. Kliknite na stránku s podrobnosťami o projekte a potom na rýchlej karte **Projektový tím a plánovanie** aktualizujte pole **Plánovací kalendár** výberom iného kalendára.

2.  Nastavte si štandardné pracovné dni a pracovný čas. Kalendár, ktorý nastavíte ako pracovný kalendár pre váš projekt, sa použije v štruktúre WBS na zistenie nasledujúcich informácií:

-   Pracovné dni a sviatky
-   Počet pracovných hodín za deň

Kliknutím na **Správa organizácie** &gt; **Bežné** &gt; **Kalendáre** nastavíte pracovné dni a pracovný čas kalendára alebo vytvoríte nový kalendár.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Nevyhnutné predpoklady na odhad nákladov na prácu

Ak chcete komplexné možnosti štruktúry WBS na odhad nákladov, mali by ste nastaviť náklady a predajné ceny pracovníkov, kategórie práce, výdavkov, poplatkov a položiek.

-   Ak chcete nastaviť náklady a predajnú cenu kategórií práce, výdavkov a poplatkov, kliknite na **Projektové riadenie a účtovníctvo** &gt; **Nastaviť** &gt; **Ceny**.
-   Ak chcete nastaviť náklady a predajnú cenu položiek, použite stránku **Obchodné zmluvy** pre každú položku v zozname **Vydané produkty** v správe informácií o produkte.

## <a name="creating-a-wbs"></a>Vytváranie WBS
Vytvorenie štruktúry WBS zahŕňa tri činnosti:

1.  **Rozdelenie práce** – Vytvorte rozdelenie práce do spravovateľných blokov alebo úloh.
2.  **Pracovný plán** – Odhadnite čas, ktorý je potrebný na dokončenie úlohy, nastavte vzájomné závislosti úloh a vyberte počiatočný a konečný dátum úloh.
3.  **Odhad nákladov** – Odhadnite náklady na každú úlohu.

Nasledujúce časti popisujú, ako môžu schopnosti štruktúry WBS pomôcť pri každej z týchto aktivít.

### <a name="work-decomposition"></a>Rozdelenie práce

Vytvorenie rozkladu alebo rozdelenia práce je zvyčajne prvým krokom v procese vytvárania štruktúry WBS. Štruktúra WBS podporuje nasledujúce základné konštrukcie pre rozklad alebo rozdelenie práce. 

**Projekt hlavnej úlohy** Projekt hlavnej úlohy je súhrn úlohy najvyššej úrovne pre projekt. Všetky ostatné úlohy projektu sú vytvorené pod ním. Názov koreňovej úlohy je vždy nastavený na názov projektu. Úsilie, dátumy a trvanie koreňového uzla sumarizujú hodnoty pre úlohy pod koreňovou úlohou. Nemôžete upraviť vlastnosti koreňového uzla, ani ho odstrániť.

**Zhrnutie alebo kontajnerové úlohy** Súhrnná úloha je úloha, ktorá má pod sebou podradené úlohy alebo čiastkové úlohy. Súhrnná úloha nemá žiadne pracovné úsilie, ani vlastné náklady. Namiesto toho sú pracovné úsilie a náklady na súhrnnú úlohu súčtom pracovného úsilia a nákladov na čiastkové úlohy. Najskorší dátum čiastkových úloh sa používa ako dátum začatia súhrnnej úlohy a najneskorší koncový dátum čiastkovej úlohy sa používa ako dátum ukončenia. Môžete upraviť názov súhrnnej úlohy, alebo nemôžete upraviť vlastnosti plánovania pre úsilie, dátumy a trvanie. Ak odstránite súhrnnú úlohu, odstránite aj všetky jej čiastkové úlohy. 

**Úlohy listového uzla** Úloha listového uzla predstavuje najpodrobnejší pracovný balík projektu. Listový uzol má odhadnuté úsilie, plánovaný počet zdrojov, plánovaný dátum začatia a ukončenia a trvanie. 

Aby umožnili vytvorenie pracovnej hierarchie alebo rozkladu projektu, môžete dokončiť nasledujúce hierarchické operácie. 

**Nová úloha** Akákoľvek nová úloha, ktorú vytvoríte, sa automaticky pridá pod koreňový uzol a úlohe sa automaticky priradí číslo štruktúry WBS. Číslo štruktúry WBS predstavuje úroveň úlohy v hierarchii. Pre úlohy v prvej úrovni v rámci úlohy koreňového uzla sa požíva schéma číslovania 1, 2, 3 a tak ďalej. Pre úlohy, ktoré sú pod prvou úrovňou v rámci projektu koreňového uzla, sa požíva schéma číslovania 1.1, 1.2, 1.3 a tak ďalej. Pre každú úroveň pridanú pod predchádzajúcu úroveň sa pridá nová bodkovaná séria čísel. 

V súčasnosti nemôžete číslovanie štruktúry WBS prispôsobiť. 

**Znížiť úroveň úlohy** Keď znížite úroveň úlohy, stane sa podriadenou úlohe, ktorá jej predchádza. Číslo štruktúry WBS novej podradenej úlohy sa automaticky prepočíta na základe čísla štruktúry WBS jej novej nadradenej úlohy. Nadradená úloha je teraz súhrnnou alebo kontajnerovou úlohou, a preto sa stáva súhrnom jej čiastkových úloh. 

> [!NOTE] 
> Keď znížite úroveň úlohy pod úlohu, ktorá bola pred operáciou zníženia úlohy listovým uzlom, novo vytvorená súhrnná úloha stratí svoje vlastné dátumy, úsilie a počet zdrojov. Teraz používa súhrn hodnôt svojich nových čiastkových úloh. 

**Zvýšiť úroveň úlohy** Keď zvýšite úroveň úlohy, prestane byť čiastkovou úlohou jej nadradenej úlohy. Číslo štruktúry WBS tejto úlohy sa automaticky prepočíta tak, aby odrážalo novú úroveň úlohy v hierarchii. Úsilie, náklady a dátumy predchádzajúcej nadradenej úlohy tejto úlohy sa prepočítajú tak, aby vylúčili túto úlohu. 

**Posunúť nahor a posunúť nadol** Keď kliknete na **Posunúť nahor** a **Posunúť nadol**, zmeníte pozíciu úlohy v hierarchii nadradených úloh. Pozícia úlohy neovplyvní úsilie, náklady, dátumy ani trvanie úlohy. Číslo štruktúry WBS tejto úlohy sa však automaticky prepočíta tak, aby odrážalo novú pozíciu úlohy.

### <a name="schedule-estimation"></a>Odhad plánu

Odhad plánu je zvyčajne druhým krokom pri vytváraní štruktúry WBS. Ako najlepší postup by ste mali po vytvorení úloh dokončiť odhad plánu. Stránka **Štruktúra rozdelenia práce** v službe Finance má dve sekcie. Horná tabla je určená na odhad plánu a dolná tabla obsahuje kartu **Odhadované náklady a výnosy**, ktorú môžete použiť na odhad nákladov. 
**Závislosti úloh** V štruktúre WBS môžete vytvoriť vzťah predchodcu medzi úlohami. Keď úlohe priradíte úlohy predchodcu, táto úloha môže začať iba vtedy, ak sa dokončili všetky jej predchádzajúce úlohy. Plánovaný dátum začatia úlohy sa automaticky nastaví na najaktuálnejší dátum všetkých jej predchodcov. 

**Plánovanie úloh** Nasledujúce faktory určujú plánovanie úloh listového uzla:

-   Predchodcovia
-   Úsilie
-   Počet zdrojov
-   počiatočný a koncový dátum,

Dátum začiatku úlohy listového uzla, ktorá nemá prednastavených predchodcov, sa automaticky nastaví na počiatočný dátum plánovania projektu. Trvanie úlohy listového uzla sa vždy vypočítava ako počet pracovných dní medzi dátumom začatia a skončenia. 

*<strong><em>Pravidlá plánovania</em></strong>* Keď je zapnutá pomoc s automatickým plánovaním, na plánovanie úloh pre úlohy listového uzla platia nasledujúce pravidlá:

-   Počiatočný a koncový dátum úlohy musí byť vždy pracovný deň, v súlade s plánovacím kalendárom projektu.
-   Dátum začatia úlohy, ktorá má predchodcov, sa automaticky nastaví na posledný dátum ukončenia svojich predchodcov.
-   Úsilie pre úlohu sa automaticky počíta takto:

Počet ľudí × Trvanie × Počet hodín v štandardný pracovný deň v kalendári projektu. 

V niektorých prípadoch sa budete chcieť od týchto pravidiel odchýliť. Môžete vypnúť automatické plánovanie, aby ste zabránili tomu, aby služba Finance automaticky nastavovala alebo opravovala akékoľvek vlastnosti úloh listových uzlov. Keď zadáte informácie o úlohe, ktorá spôsobí porušenie akýchkoľvek pravidiel plánovania, zobrazí sa pre úlohu ikona chyby plánovania. Ak si neželáte, aby sa zobrazovali chyby plánovania, kliknite na ikonu **Zobrazujú sa chyby plánovania** a túto funkciu vypnite. 

> [!NOTE] 
> Hodnoty súhrnnej alebo kontajnerovej úlohy sa naďalej počítajú ako súčet hodnôt čiastkových úloh, bez ohľadu na to, či je zapnutá alebo vypnutá automatická pomoc s plánovaním. 

**Oprava chýb plánovania** Keď je zapnutá pomoc s automatickým plánovaním, je pravdepodobné, že nedôjde k chybám v plánovaní. Ak však vypnete pomoc s automatickým plánovaním a neskôr ju znova zapnete, v štruktúre WBS sa môžu zobraziť ikony chýb plánovania. 

**Oprava chýb plánovania podľa úloh** Keď dvakrát kliknete na ikonu chyby plánovania pre konkrétnu úlohu, v dialógovom okne sa zobrazia všetky chyby plánovania pre danú úlohu. Môžete sa rozhodnúť, ktoré chyby plánovania pre úlohu opravíte. 

**Oprava všetkých chýb plánovania** Ak chcete, aby služba Finance opravila všetky chyby plánovania v štruktúre WBS, na table Akcia kliknite na **Opraviť všetky nezrovnalosti v plánovaní**. 

> [!NOTE] 
> Táto vlastnosť môže spôsobiť významné úpravy štruktúry WBS. Chyby sa opravia v nasledujúcom poradí:

1.  Odhadované úsilie pri všetkých úlohách sa upraví tak, aby sa rovnalo kapacite definovanej v kalendári projektu.
2.  Dátum začatia každej úlohy sa upraví tak, aby sa úloha spustila po dokončení všetkých úloh, ktoré jej predchádzali.
3.  Dátum začatia každej úlohy sa upraví tak, aby sa odstránili medzery v dátumoch začatia úloh, ktoré jej predchádzali.

### <a name="cost-estimation"></a>Odhad nákladov

Ako už bolo spomenuté vyššie v tomto dokumente, zadávate odhad nákladov pre každú úlohu listového uzla pomocou karty **Odhadované náklady a výnosy** v dolnej table na stránke **Štruktúra rozdelenia práce**. 

> [!NOTE] 
> Nemôžete upraviť odhad nákladov pre súhrnnú alebo kontajnerovú úlohu. Odhad nákladov pre súhrnnú úlohu sa rovná súčtu odhadu nákladov na jej úlohy listového uzla. Odhadované celkové náklady na každú úlohu sa počítajú ako súčet odhadovaných nákladov pre nasledujúce typy transakcií:

-   Práca
-   Položka alebo materiál
-   Výdavky

Typ transakcie **Poplatok** sa používa na odhad výnosov založených na poplatkoch. Tento typ transakcie nemá nákladovú zložku, a preto sa pri odhadovaní nákladov nezohľadňuje. 

Typ transakcie **Na obchodný vzťah** sa používa na zaznamenanie zmluvnej hodnoty predaja v projekte s pevnou hodnotou. Pri odhadovaní nákladov sa tento typ transakcie tiež nezohľadňuje. 

Keď odhadujete náklady na prácu, materiál a výdavky pre každú úlohu, musíte k odhadovaným nákladom priradiť kategóriu projektu. 

**Odhad nákladov na prácu** Pre každú úlohu listového uzla priradíte pracovné úsilie v hodinách a predvolenú kategóriu. Preto keď nastavujete plán pre úlohu, odhad nákladov na prácu pre túto úlohu sa automaticky pridá do predvolenej kategórie pre prácu. Tento odhad nákladov sa zobrazuje na karte **Odhadované náklady a výnosy** v mriežke **Podrobnosti o riadku** pre túto úlohu. Ak požadujete viac odhadov nákladov na prácu, môžete ich pridať na tejto karte. Ak na základe odhadu nákladov na prácu zvýšite alebo znížite počet hodín, plán úlohy sa automaticky prepočíta. 

**Odhad výdavkov a nákladov na materiál** Karta **Odhadované náklady a výnosy** tiež umožňuje odhadnúť výdavky a náklady na materiál pre úlohu, ak požadujete odhady. 

Náklady a predajná cena pre každý riadok odhadu práce alebo výdavkov sú založené na nastavení, ktoré je definované pre každú kategóriu v cenových tabuľkách v časti **Projektové riadenie a účtovníctvo** &gt; **Nastavenie** &gt; **Určenie ceny**. Položky, náklady a predajná cenu sa pridajú predvolene zo zmlúv o položke alebo obchode v stránke so zoznamom **Vydané produkty** v správe informácií o produkte.

## <a name="tracking-progress-on-the-wbs"></a>Priebeh sledovania v štruktúre WBS
Niektoré odvetvia sledujú priebeh projektu oproti štruktúre WBS na veľmi podrobnej úrovni, zatiaľ čo iné sledujú priebeh na vyššej úrovni štruktúry WBS. Táto časť popisuje, ako môžete použiť sledovanie štruktúry WBS na splnenie požiadaviek projektu. 

Služba Finance má tri zobrazenia pre štruktúru WBS projektu: zobrazenie Plánovanie, zobrazenie Sledovanie úsilia a zobrazenie Sledovanie nákladov.

### <a name="planning-view"></a>Zobrazenie Plánovanie

Zobrazenie Plánovanie zobrazuje plánovaný alebo základný odhad plánu a informácií o nákladoch. Aj keď neexistujú žiadne funkcie na sledovanie verzie a základnej úrovne pre projekt štruktúry WBS, hodnoty v tomto zobrazení majú predstavovať základnú verziu. Časti Odhad plánu a Odhad nákladov tohto článku popisujú toto zobrazenie a spôsob jeho použitia na vytvorenie WBS.

### <a name="effort-tracking-view"></a>Zobrazenie sledovania úsilia

Zobrazenie Sledovanie úsilia zobrazuje sledovanie priebehu úloh v štruktúre WBS. Porovnáva akumulované hodiny skutočného úsilia pre danú úlohu s plánovanými hodinami úsilia. Nasledujúce vzorce poskytujú hodnoty v zobrazení Sledovanie úsilia:

-   Percento priebehu = skutočné úsilie k dnešnému dňu ÷ plánované úsilie na úlohu
-   Zostávajúce úsilie (tiež známe ako Odhad do dokončenia \[ETC\]) = plánované úsilie – skutočné úsilie k dnešnému dňu
-   Odhad pri dokončení (EAC) = zostávajúce úsilie + skutočné úsilie k dnešnému dňu
-   Odchýlka predpokladaného úsilia = Plánované úsilie – EAC

Zobrazenie Sledovanie úsilia zobrazuje projekciu odchýlky úsilia pre danú úlohu na základe toho, či je úroveň EAC väčšia alebo menšia ako plánované úsilie:

-   Ak je úroveň EAC vyššia ako plánované úsilie, úloha sa plánuje trvať dlhšie, než bolo pôvodne naplánované a prekračuje plán.
-   Ak je úroveň EAC nižšia ako plánované úsilie, úloha sa plánuje trvať kratšie, než bolo pôvodne naplánované a predbieha plán.

**Opätovná projekcia úsilia projektového manažéra** Príležitostne bude musieť projektový manažér alebo iná osoba, ktorá sleduje priebeh projektu, revidovať pôvodné odhady úlohy. Z rôznych dôvodov sa úloha môže pohybovať rýchlejšie alebo pomalšie, ako sa pôvodne predpokladalo. Napríklad sa zmenšil rozsah alebo pracovníci majú menej skúseností, ako sa pôvodne plánovalo. Projekcie sú vnímaním odhadov projektovým manažérom vzhľadom na aktuálny stav projektu. Vo všeobecnosti by ste nemali meniť základné čísla, pretože základ projektu predstavuje dôkladne zverejnený dokument plánu projektu a odhadu nákladov, s ktorým súhlasili všetky zúčastnené strany. 

Existujú dva spôsoby, ktorými môžu projektoví manažéri upraviť úsilie vynaložené na úlohy:

-   Úprava zostávajúceho úsilia, ktoré sa automaticky nastaví na aktualizáciu skutočného zostávajúceho úsilia vynaloženého na úlohu.
-   Úprava percenta priebehu, ktoré sa automaticky nastaví na aktualizáciu skutočného priebehu úlohy.

Oba z týchto prístupov spôsobujú prepočítanie úlohy ETC, EAC a percenta priebehu a predpokladaného úsilie rozptylu úlohy. EAC, ETC a percento priebehu na súhrnných úlohách sú tiež prepočítané a dochádza k aktualizácii predpokladaného rozptylu úsilia. 

**Upravené úsilie pri súhrnných úlohách** Môžete upraviť úsilie týkajúce sa súhrnných alebo kontajnerových úloh. Bez ohľadu na to, či upravíte tieto hodnoty pomocou zostávajúceho úsilia alebo percenta priebehu v oblasti súhrnných úloh, výpočet prebehne automaticky v nasledujúcom poradí:

1.  EAC, ETC a percento pokroku v úlohe sú vypočítané.
2.  Nový EAC sa rozdelí na podradené úlohy v rovnakom pomere ako bolo pôvodné množstvo EAC.
3.  Vypočíta sa nový EAC pre každú úlohu listového uzla.
4.  Zvyšné úsilie a percento priebehu sa prepočítajú pre všetky ovplyvnené podradené úlohy na základe novej hodnoty EAC. Prepočíta sa tiež rozptyl úsilia pri vykonávaní úloh.
5.  EAC súhrnných úloh sa tiež prepočítava z listových uzlov.

Kliknutím na **Rozbaliť na úroveň** v zobrazení Sledovanie úsilia nastavte úroveň, na ktorej sa má sledovať a udržiavať vaša štruktúra WBS. Štruktúra WBS sa automaticky rozšíri na túto úroveň v zobrazení Sledovanie úsilia, kedykoľvek ho otvoríte.

### <a name="cost-tracking-view"></a>Zobrazenie sledovania nákladov

Zobrazenie Sledovanie nákladov zobrazuje sledovanie spotreby nákladov na úlohu. V tomto zobrazení sa skutočné náklady, ktoré sa doteraz vynaložili na úlohu, porovnajú s plánovanými nákladmi na úlohu. Nasledujúce vzorce poskytujú hodnoty v zobrazení Sledovanie nákladov:

-   Percento spotrebovaných nákladov = skutočné náklady k dnešnému dňu ÷ plánované náklady na úlohu
-   Náklady na dokončenie (CTC) = plánované náklady – skutočné náklady k dnešnému dňu
-   Odhad pri dokončení (EAC) = CTC + skutočné náklady k dnešnému dňu
-   Predpokladaná odchýlka nákladov = plánované náklady – EAC

Zobrazenie Sledovanie nákladov zobrazuje projekciu odchýlky nákladov pre danú úlohu na základe toho, či je úroveň EAC väčšia alebo menšia ako plánované náklady:

-   Ak je úroveň EAC vyššia ako plánované náklady, plánuje sa, že úloha bude stáť viac, než bolo pôvodne naplánované a prekračovať rozpočet.
-   Ak je úroveň EAC nižšia ako plánované náklady, plánuje sa, že úloha bude stáť menej, než bolo pôvodne naplánované a rozpočet bude nižší.

**Opätovná projekcia nákladov zo strany projektového manažéra** Projektoví manažéri musia na overenie pôvodného odhadu nákladov na úlohu použiť CTC. Projektový manažér môže upraviť hodnotu CTC na náklady potrebné na splnenie úlohy. Ak upravíte hodnotu CTC, prepočítajú sa CTC, EAC a percento spotrebovaných nákladov úlohy a projektovaný rozptyl nákladov na úlohu. EAC, ETC a percento spotrebovaných nákladov na súhrnné úlohy sú tiež prepočítané a dochádza k aktualizácii predpokladaného rozptylu nákladov. 

> [!NOTE] 
> Keď v zobrazení Sledovanie úsilia revidujete úsilie pre úlohu štruktúry WBS, v zobrazení Sledovanie nákladov sa prepočítajú CTC, EAC, percento spotrebovaných nákladov a projektovaný rozptyl nákladov úlohy. Revízie nákladov však neovplyvnia hodnoty v zobrazení Sledovania úsilia, pretože náklady podľa typu transakcie (práca, materiál alebo výdavky) alebo kategórie projektu nie sú revidované. 

**Revízia projekcie nákladov na súhrnné úlohy** Môžete revidovať náklady na súhrnné úlohy a výpočty prebehnú automaticky v nasledujúcom poradí:

1.  Prepočítajú sa EAC, CTC a percento nákladov spotrebovaných na úlohu.
2.  Nové EAC sa rozdelí na podradené úlohy v rovnakom pomere ako bolo pri pôvodnom EAC pri úlohách.
3.  Pre každú úlohu sa počíta nový EAC.
4.  CTS a percento spotrebovaných nákladov sa prepočítajú pre ovplyvnené podradené úlohy na základe hodnoty EAC. Prepočíta sa tiež rozptyl nákladov pri vykonávaní úloh.
5.  Na základe tejto zmeny sa prepočíta EAC pre všetky súhrnné úlohy.

Kliknutím na **Rozbaliť na úroveň** v zobrazení Sledovanie nákladov nastavte úroveň, na ktorej sa má sledovať a udržiavať vaša štruktúra WBS. Štruktúra WBS sa rozšíri na túto úroveň v zobrazení Sledovanie nákladov, kedykoľvek ho otvoríte.

### <a name="earned-value-management"></a>Správa zarobených hodnôt

Na sledovanie priebehu projektu môžete použiť metódu zarobených hodnôt (EVM). Metriky zarobených hodnôt si môžete pozrieť v Centre rolí projektového manažéra. Komponent grafu zarobených hodnôt zobrazuje časovo rozložené hodnoty plánovanej hodnoty a skutočných nákladov. Získaná hodnota k aktuálnemu dátumu sa zobrazuje ako bod. Časovo rozložené údaje o získanej hodnote nie sú momentálne k dispozícii. 

Časová fáza v grafe zarobených hodnôt sa zobrazuje podľa týždňa alebo mesiaca. Táto časť popisuje tri piliere EVM: plánovanú hodnotu, zarobenú hodnotu a skutočné náklady. 

**Plánovaná hodnota** Teória EVM uvádza, že graf plánovanej hodnoty predstavuje mieru, akou tím projektu plánoval získať hodnotu projektu. 

Služba Finance používa pravidlo 0:100 pri vykresľovaní plánovanej hodnoty. Podľa tohto pravidla sa hodnota úlohy zverejní k úlohe k dátumu ukončenia. Až do ukončenia úlohy na 100 percent sa nezverejní žiadna hodnota. 

V časti Projektový manažment a účtovníctvo zadáte dátum ukončenia listových uzlov a plánované náklady na ne. Keď je graf plánovanej hodnoty zobrazený podľa týždňa, je plánovaná hodnota zosumarizovaná za týždeň pre všetky úlohy listového uzla počas trvania projektu. 

**Zarobená hodnota** Teória EVM uvádza, že graf zarobenej hodnoty predstavuje mieru, akou tím projektu v skutočnosti zarába hodnotu projektu. 

Služba Finance používa pravidlo 0:100 pri vykresľovaní zarobenej hodnoty. Podľa tohto pravidla sa hodnota úlohy zverejní k úlohe k dátumu ukončenia. Až do ukončenia úlohy na 100 percent sa nezverejní žiadna hodnota. 

Pri výpočte zarobenej hodnoty sa berie do úvahy percento priebehu každej úlohy. Podľa pravidla 0:100 sa na výpočet zarobenej hodnoty ku koncu daného obdobia berú do úvahy iba úlohy, ktoré sú splnené v danom období. Zarobená hodnota v projekte sa počíta pre všetky úlohy, ktoré boli dokončené pri vytvorení grafu. 

> [!NOTE] 
> V súčasnosti systém na sledovanie štruktúry WBS nemá dátové štruktúry na ukladanie historických percent priebehu v každej úlohe. Získanú hodnotu je preto možné nahlásiť až v čase, keď je kocka spracovaná. Kocku pravidelne spracúvajte, aby ste aktualizovali údaje o zarobených hodnotách, ktoré sa zobrazujú v Centre rolí. 

**Skutočné náklady** Teória EVM uvádza, že graf skutočných nákladov predstavuje mieru, akou sa peniaze vynakladajú na projekt. 

Transakcie, ktoré sa zaúčtujú do projektu, sa používajú na vykreslenie riadku skutočných nákladov. Náklady sú zhrnuté podľa dátumu. Tieto údaje sa potom použijú na vytvorenie grafu skutočných nákladov podľa týždňa alebo mesiaca v grafe zarobenej hodnoty.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Ako používať koncepty plánovanej hodnoty, zarobenej hodnoty a skutočných nákladov

**Rozptyl plánu** Počas plánovania vytvoríte predpoveď pre prácu na časovej osi. Preto je plánovanou hodnotou rýchlosť, s akou si plánovači mysleli, že sa na projekte dokončí práca. Po dokončení projektu sú práce dokončené a projekt získava hodnotu. Porovnaním plánovanej hodnoty so zarobenou hodnotou môžete vidieť, ako prebiehajú práce na projekte. Výsledok tohto porovnania sa nazýva rozptyl plánu. 

Ak je plánovaná hodnota za obdobie vyššia ako zarobená hodnota, objem práce vykonanej na projekte je menší, ako bol plánovaný. Preto je projekt oneskorený za plánom. Pretože plánovaná hodnota a zarobená hodnota sú vyjadrené v peňažných hodnotách, je časovému oneskoreniu projektu pridelená aj peňažná hodnota. 

Ak je plánovaná hodnota za obdobie nižšia ako zarobená hodnota, objem práce vykonanej na projekte je väčší, ako bol plánovaný. Preto projekt predbieha plán. Táto doba predstihu má tiež peňažnú hodnotu.

**Rozptyl nákladov** Pretože zarobená hodnota používa ako multiplikátor obstarávaciu cenu, zarobená hodnota označuje cenu práce vykonanej na projekte. Pri práce na projekte protokol transakcií poskytuje záznamy o peniazoch, ktoré sa v skutočnosti minú na tento projekt. Porovnaním zarobenej hodnoty so skutočnými nákladmi môžete zobraziť množstvo vynaložených peňazí/zarobenú hodnotu. Výsledok tohto porovnania sa nazýva rozptyl nákladov. 

Ak sú skutočné náklady vynaložené na určité obdobie väčšie ako zarobená hodnota, bolo vynaložených viac peňazí ako sa zarobilo. Preto je projekt nad rámec rozpočtu. 

Ak sú skutočné náklady vynaložené na určité obdobie nižšie ako zarobená hodnota, bolo vynaložených menej peňazí ako sa zarobilo. Preto je projekt pod rámec rozpočtu.

## <a name="wbs-templates"></a>Šablóny štruktúry WBS
Pomocou funkcie šablón štruktúry WBS môžete vytvoriť štandardné šablóny pre projekty. Ak projekty, ktoré vaša spoločnosť ponúka, zahŕňajú veľa opakovateľnej práce, mali by ste zvážiť vytvorenie šablóny štruktúry WBS. 

Šablónu štruktúry WBS môžete vytvoriť zo štruktúry WBS existujúceho projektu, aby sa znalosti a osvedčené postupy, ktoré ste získali počas plánovania daného projektu, mohli v budúcnosti znova použiť na podobných projektoch. Niekedy však nemusí mať zmysel uložiť celú štruktúru WBS ako šablónu. Preto môžete pre projekt vytvoriť šablóny aj z častí štruktúry WBS.

### <a name="saving-a-projects-wbs-as-a-template"></a>Uloženie štruktúry WBS projektu ako šablóny

Po vytvorení šablóny ju môžete importovať do štruktúry WBS nového projektu pod koreňovým uzlom alebo do ľubovoľnej úlohy v štruktúre WBS projektu.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Import šablóny štruktúry WBS do štruktúry WBS projektu

Pri importovaní úloh sú úlohy v šablóne usporiadané podľa dátumu začatia úlohy, pod ktorú sa importujú. Počas importu sa vzťahy predchodcu v úlohách šablón používajú na výpočet dátumov začatia importovaných úloh. Štandardný pracovný kalendár cieľového projektu sa použije na výpočet konečných dátumov importovaných úloh, aby sa zachovali pracovné dni a štandardná pracovná doba, ktoré sú definované v pracovnom kalendári aktuálneho projektu. 

Sumy nákladov a predajné ceny v riadkoch odhadov sa používajú na zabezpečenie toho, že ceny špecifické pre projekt alebo projektovú zmluvu majú platné dátumy.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Rozdiely medzi štruktúrou WBS projektu a šablónou štruktúry WBS

-   Úlohy v šablónach štruktúry WBS neobsahujú dátumy začiatku a konca.

Pracovné a nepracovné dni nie sú pre šablóny štruktúry WBS stanovené.

-   Šablóny štruktúry WBS vždy používajú plánovací kalendár, ktorý je nastavený ako predvolený pre všetky projekty.

Predvolený plánovací kalendár sa používa iba na zistenie hodín v štandardný pracovný deň.

-   Vzťahy predchodcu sa neskopírujú do šablóny štruktúry WBS.

Pretože šablóny štruktúry WBS nemajú dátumy, logika počiatočného dátumu, ktorá je založená na dátume ukončenia predchodcu, sa nevyžaduje.

-   Riadok odhadu nákladov práce sa automaticky vytvorí, keď sa úloha vytvorí v šablóne štruktúry WBS. Predajná cena a výška nákladov sa skopírujú od vybraného pracovníka.

Výdavky a náklady na položku je možné vytvoriť manuálne, rovnako ako je to možné v štruktúre WBS projektu.

-   Chyby plánovania sa zobrazia, ak existujú odchýlky od nasledujúceho vzorca:

Úsilie = počet zdrojov × doba trvania × počet hodín v štandardný pracovný deň 

Kliknutím na **Opraviť všetky chyby plánovania** môžete opraviť všetky chyby plánovania súčasne. 

Prípadne môžete chyby plánovania opraviť jednotlivo kliknutím na ikonu varovania pre každú úlohu.





[!INCLUDE[footer-include](../includes/footer-banner.md)]