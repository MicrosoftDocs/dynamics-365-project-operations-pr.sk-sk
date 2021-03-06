---
title: Cenové ponuky – Kľúčové koncepty
description: Táto téma poskytuje informácie o cenových ponukách projektov a cenových ponukách predaja dostupných v Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b252f6e02d0809c352d3665731ec5e02e4e9a73f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898461"
---
# <a name="quotes---key-concepts"></a>Cenové ponuky – Kľúčové koncepty

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

V Dynamics 365 Project Operations existujú dva typy cenových ponúk: projektové a predajné. Tieto dva typy cenových ponúk sa líšia nasledujúcimi spôsobmi:

- **Mriežky pre riadkové položky**: V predajnej cenovej ponuke existuje len jedna mriežka pre položky v riadku. Projektová cenová ponuka má dve mriežky pre riadkové položky. Jedna mriežka je pre projektové riadky a druhá pre produktové riadky.
- **Aktivácia a revízie**: Predajné cenové ponuky podporujú aktiváciu a revízie. Tieto procesy nie sú v prípade projektovej cenovej ponuky podporované.
- **Pripojené objednávky**: K predajnej cenovej ponuke môžete priložiť viacero objednávok. K projektovej cenovej ponuke je možné priložiť iba jednu zmluvu projektu.
- **Víťazná cenová ponuka**: Keď vyhráte predajnú cenovú ponuku, príslušná príležitosť môže zostať otvorená. Po víťaznej projektovej cenovej ponuke sa uzavrie súvisiaca príležitosť.
- **Polia a koncepty**: Predajná cenová ponuka nezahŕňa niektoré polia a koncepty, ktoré sú súčasťou projektovej cenovej ponuky. Polia zahŕňajú **zmluvnú jednotku**, **Account Manager** a **faktúra na kontaktné meno**.  
- **Typ**: Predajné cenové ponuky a projektové cenové ponuky sú tiež identifikované poľom založeným na množine možností – **Typ**. Pre predajnú ponuku má toto pole hodnotu **Založené na položke**. Pre projektovú cenovú ponuku, má hodnotu **založené na práci**.

Táto téma sa zameriava na detaily projektových ponúk.

Projektová cenová ponuka v Project Operations môže mať viac riadkov položiek alebo riadkov cenovej ponuky. V skutočnosti, projektová cenová ponuka má dve mriežky pre riadkové položky. Jedna mriežka je pre riadky založené na projekte, ktoré umožňujú podrobné odhady. Druhá mriežka je pre riadky založené na produkte, ktoré používajú jednoduchú jednotkovú cenu a prístup založený na množstve.

- **Založené na projekte**: Hodnota uvedené v cenovej ponuke je určená po odhadnutí, koľko práce je potrebnej. Prácu môžete odhadnúť na vysokej úrovni, priamo ako podrobnosti o riadku pod každým riadkom cenovej ponuky, alebo na základe prízemných odhadov pomocou projektu a plánu projektu. Riadky cenovej ponuky založené na projekte sa nachádzajú iba v cenových ponukách založených na projekte, ktoré sú vytvorené pomocou Project Operations. Tento typ riadka cenovej ponuky je prispôsobeným formulárom v riadkoch cenovej ponuky, ktoré sú k dispozícii v Microsoft Dynamics 365 Sales.

- **Založené na produkte**: Hodnota uvedená v cenovej ponuke je určená na základe množstva predaných jednotiek a jednotkovej predajnej ceny. Produkt na riadku cenovej ponuky založenej na produkte môže pochádzať z katalógu produktov v predaji alebo môže byť produktom, ktorý definujete. Tento typ riadka cenovej ponuky je k dispozícii aj v cenových ponukách založených na projektoch, ktoré sú vytvorené pomocou Project Operations.

Čiastka v cenovej ponuke je súčtom riadkov založených na produkte a riadkov založených na projekte.

> [!NOTE]
> Cenové ponuky a riadky cenových ponúk sa v Project Operations nevyžadujú. Proces projektu môžete spustiť pomocou projektovej zmluvy (predaného projektu). Vždy je však potrebná príležitosť bez ohľadu na to, či začnete s ponukou alebo projektovou zmluvou.

## <a name="project-based-quote-lines"></a>Riadky cenových ponúk založené na projekte

Riadok cenovej ponuky založenej na projekte v Project Operations má nasledujúce metódy fakturácie:

- Čas a materiál
- Pevná cena

### <a name="time-and-material"></a>Čas a materiál

Metóda fakturácie času a materiálu je založená na spotrebe. Keď vyberiete túto fakturačnú metódu, zákazník sa fakturuje, pretože v projekte vzniknú náklady. Faktúry sú vytvorené na základe dátumu periodickej frekvencie. Počas predajného procesu poskytuje ponuková hodnota časovej a materiálnej zložky iba odhad konečných nákladov pre zákazníka. Dodávateľ sa zaväzuje dokončiť projekt presne na ponukovú hodnotu. Komponenty času a materiálu zvyšujú riziko zákazníka. Zákazníci by mohli chcieť rokovať o dodatočnom neprekračovaní doložiek, aby sa minimalizovalo ich riziko. Project Operations nepodporuje nastavenie neprekračovať doložky.

### <a name="fixed-price"></a>Pevná cena

V metóde fakturovania pevnej ceny sa dodávateľ zaväzuje dodávať projekt za pevnú cenu zákazníkovi. Zákazníkovi sa fakturuje ponuková hodnota riadka s pevnou cenou, bez ohľadu na náklady, ktoré dodávateľ vyrobil na doručenie daného riadka cenovej ponuky. Hodnota riadka s pevnou cenou sa fakturuje jedným z nasledujúcich spôsobov: 

- Ako paušálna suma na začiatku alebo na konci projektu, alebo keď je dosiahnutý míľnik projektu. 
- Na základe frekvencie založenej na dátume rovnakých splátok pevnej hodnoty v riadku cenovej ponuky. Tieto splátky sú známe ako periodické míľniky.
- V splátkach, ktoré majú peňažnú hodnotu, ktorá je v súlade s pokrokom práce alebo konkrétne míľniky, ktoré sú dosiahnuté na projekte. V tomto prípade sa hodnota každej splátky môže líšiť, ale všetky sa musia pridať do pevnej hodnoty v riadku cenovej ponuky.

Project Operations podporuje všetky tri typy fakturačných rozvrhov pre riadky cenovej ponuky s pevnou cenou.

## <a name="transaction-classification"></a>Klasifikácia transakcie

Profesionálne servisné organizácie zvyčajne oceňujú a fakturujú svojich zákazníkov podľa klasifikácie nákladov. Náklady reprezentované nasledujúcimi klasifikáciami transakcií:

- **Čas**: Táto klasifikácia predstavuje náklady na prácu alebo čas ľudských zdrojov na projekte.
- **Výdavok**: Táto klasifikácia predstavuje všetky ostatné druhy výdavkov na projekt. Pretože výdavky môžu byť široko klasifikované, väčšina organizácií vytvára podkategórie, ako je cestovanie, požičovňa áut, hotel, alebo kancelárske potreby.
- **Poplatok**: Táto klasifikácia predstavuje rôzne režijné náklady, penále a iné položky, ktoré sú účtované zákazníkovi. 
- **Daň**: Táto klasifikácia predstavuje čiastky dane, ktoré používatelia pridajú pri zadávaní výdavkov.
- **Materiálová transakcia**: Táto klasifikácia predstavuje skutočné hodnoty z produktových radov na potvrdenej faktúre projektu.
- **Míľnik**: Táto klasifikácia je používaná logikou fakturácie fixnej ceny.

Jedna alebo viacero klasifikácií transakcie môže byť priradených ku riadkom cenovej ponuky. Po zvíťazení cenovej ponuky sa priradenie medzi klasifikáciou transakcie a riadkom cenovej ponuky prevedie do riadka zmluvy.
  
Cenová ponuka môže napríklad obsahovať nasledujúce dva riadky cenovej ponuky: 

- Konzultačná práca, ktorá používa metódu fakturácie času a materiálu, kde sa uplatňujú klasifikácie transakcií s časom a poplatkami. Napríklad všetky transakcie času a poplatkov pre príklad **Dynamics AX Implementácie** projektu sú fakturované zákazníkovi na základe času a materiálov, ktoré sa používajú. 
- Súvisiace cestovné výdavky, ktoré používajú metódu účtovania pevnej ceny. Napríklad, všetky cestovné výdavky na **Dynamics AX implementáciu** príkladný projekt sú fakturované pevnou peňažnou hodnotou.

> [!NOTE]
> Kombinácia projektu a klasifikácie transakcií **času**, **nákladov**a **poplatkov**, ktoré súvisia s riadkom cenovej ponuky alebo riadkom zmluvy, musia byť jedinečná. Ak je rovnaká kombinácia projektovej a transakčnej triedy priradená k viac ako jednému riadku zmluvy alebo riadku cenovej ponuky, Project Operations nebude pracovať správne.

## <a name="billing-types"></a>Typy fakturácie

Pole **Typy fakturácie** definuje koncept účtovateľnosti. Je to množina možností, ktorá má nasledujúce možné hodnoty:

- **Účtovateľné**: Náklady, ktoré vznikli touto rolou/kategóriou, sú priame náklady, ktoré riadia realizáciu projektu a zákazník bude za túto prácu platiť. Platba môže byť podaná ako časovo-materiálová alebo fixná-cena dojednania. Zamestnanec, ktorý tento čas trávi, však získa zodpovedajúci kredit za jeho fakturovateľné využitie.
- **Neúčtovateľné**: Náklady, ktoré vznikli touto rolou/kategóriou, sú považované za priame náklady, ktoré riadia realizáciu projektu, no napriek tomu zákazník nerozpozná tento fakt a nebude za túto prácu platiť. Zamestnanec, ktorý trávi tento čas, nebude pripísaný na fakturovateľné využitie.
- **Bezplatné**: Náklady, ktoré vznikli touto rolou/kategóriou, sú považované za priame náklady, ktoré riadia realizáciu projektu a zákazník rozozná tento fakt. Zamestnanec, ktorý trávi tento čas, bude pripísaný na fakturovateľné využitie. Táto cena však nie je účtovaná zákazníkovi.
- **Nie je k dispozícii**: Náklady vynaložené na interné projekty, ktoré nevyžadujú sledovanie výnosov, sa sledujú pomocou tejto možnosti.

## <a name="invoice-schedule"></a>Plán faktúry

Plán faktúry je séria dátumov, ktoré sa pri fakturácii projektu vyskytnú. Môžete voliteľne vytvoriť plán fakturácie v riadku cenovej ponuky. Každý riadok cenovej ponuky môže mať vlastný plán fakturácie. Ak chcete vytvoriť plán fakturácie, musíte poskytnúť nasledovné hodnoty atribútov:

- Dátum začatia fakturácie 
- Dátum dodania, ktorý predstavuje koncový dátum fakturácie projektu
- Frekvencia faktúr

Tieto tri hodnoty atribútov sa používajú na generovanie predbežného súboru dátumov na zriadenie fakturácie.

## <a name="invoice-frequency"></a>Frekvencia faktúr

Faktúra frekvencia je entita, ktorá uchováva hodnoty atribútov, ktoré pomáhajú vyjadriť frekvenciu vytvárania faktúr. Nasledujúce atribúty vyjadrujú alebo definujú entitu frekvencia faktúr:

- **Obdobie**: Obdobia mesačne, dvojtýždenne, a týždenne sú podporované. 
- **Spustenia za obdobie**: Pre týždenné a dvojtýždňové obdobie môžete definovať iba jedno spustenie za obdobie. V mesačných obdobiach môžete definovať medzi jedným a štyrmi spusteniami za obdobie. 
- **Dni spustenia**: Dni, kedy sa má fakturácia spustiť. Tento atribút môžete nastaviť dvoma rôznymi spôsobmi:
  - **Pracovné dni**: Môžete napríklad určiť, že fakturácia sa spustí každý pondelok alebo každý druhý pondelok. Zákazníci, ktorí musia nastaviť fakturáciu na spustenie v pracovnom dni, môžu preferovať tento typ konfigurácie. 
  - **Kalendárne dni**: Môžete napríklad určiť, že fakturácia sa spustí v siedmom a dvadsiatom prvom dni každého mesiaca. Niektoré organizácie môžu preferovať tento typ konfigurácie, pretože to pomáha zaručiť, že fakturácia je spustená na pevný harmonogram každý mesiac.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Plán fakturácie pre riadok cenovej ponuky s pevnou cenou

Pre riadok cenovej ponuky s pevnou cenou môžete použiť mriežku **plánu fakturácie** na vytvorenie míľnikov fakturácie, ktoré sa rovnajú hodnote riadka cenovej ponuky.

- Ak chcete vytvoriť rovnako rozdelené fakturačné míľniky, vyberte frekvenciu fakturácie, zadajte dátum začiatku fakturácie v riadku cenovej ponuky a vyberte **požadovaný dátum dokončenia** cenovej ponuky v sekcii **súhrn** v hlavičke cenovej ponuky. Potom vyberte **generovať periodické míľniky** na vytvorenie rovnomerne rozdelených míľnikov na základe vybranej frekvencie faktúr. 
- Ak chcete vytvoriť míľnik fakturácie paušálnej čiastky, vytvorte míľnik a potom zadajte hodnotu riadka cenovej ponuky ako čiastku míľnika.
- Ak chcete vytvoriť fakturačné míľniky, ktoré sú založené na konkrétnych úlohách v pláne projektu, vytvorte míľnik a mapujte ho na prvok plánu projektu v používateľskom rozhraní fakturačného míľnika.
