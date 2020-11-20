---
title: Cenove ponuky a riadky cenovej ponuky
description: Táto téma poskytuje informácie o jednotkových skupinách a jednotkách.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 509bc089e69ec234ddfdecb789c2e446286da82b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129472"
---
# <a name="quotes-and-quote-lines"></a>Cenove ponuky a riadky cenovej ponuky

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V Dynamics 365 Project Service Automation, existujú dva typy cenových ponúk: projektové cenové ponuky a predajných cenové ponuky. Tieto dva typy sa líšia nasledujúcimi spôsobmi:

- V predajnej cenovej ponuke existuje len jedna mriežka pre položky v riadku. V projektovej cenovej ponuke sú dve mriežky pre položky riadka: jeden pre riadky projektu a jeden pre produktové rady.
- Predajná cenová ponuka podporuje aktiváciu a revízie. Projektová cenová ponuka nepodporuje tieto procesy.
- K predajnej cenovej ponuke môžete priložiť viacero objednávok. K projektovej cenovej ponuke môžete priložiť iba jednu zmluvu projektu.
- Môžete vyhrať predajnú cenovú ponuku a ponechať súvisiacu príležitosť otvorenú. Po víťaznej projektovej cenovej ponuke sa uzavrie súvisiaca príležitosť.
- Predajná cenová ponuka nezahŕňa niektoré polia a koncepty, ktoré sú súčasťou projektovej cenovej ponuky. Polia zahŕňajú **zmluvnú jednotku**, **Account Manager** a **faktúra na kontaktné meno**.  
- Predajné cenové ponuky a projektové cenové ponuky sú tiež identifikované ako pole založené na množine možností, ktoré je pomenovaná **typ**. Pre predajnú ponuku má toto pole hodnotu **Založené na položke**. Pre projektovú cenovú ponuku, má hodnotu **založené na práci**.

Táto téma sa zameria na detaily projektových ponúk.

Projektová cenová ponuka v PSA môže mať viac riadkov položiek alebo riadkov cenovej ponuky. V skutočnosti, projektová cenová ponuka má dve mriežky pre riadkové položky. Jedna mriežka je pre riadky založené na projekte, ktoré umožňujú podrobné odhady. Druhá mriežka je pre riadky založené na produkte, ktoré používajú jednoduchú jednotkovú cenu a prístup založený na množstve.

- **Založené na projekte** - Suma (kótovaná hodnota) je určená po odhadnutí, koľko práce je potrebnej. Môžete odhadnúť prácu na vysokej úrovni, alebo ju môžete odhadnúť priamo ako riadkové detaily pod každým riadkom cenovej ponuky. Na záver môžete odhadnúť prácu založenú na odhadoch základov pomocou projektu a projektového plánu. Riadky cenovej ponuky založené na projekte sa nachádzajú iba v cenových ponukách založených na projekte, ktoré sú vytvorené pomocou Project Service Automation. Tento typ riadka cenovej ponuky je prispôsobeným formulárom v riadkoch cenovej ponuky, ktoré sú k dispozícii v Microsoft Dynamics 365 Sales.
- **Založené na produkte** - Suma (kótovaná hodnota) je určená na základe množstva predaných jednotiek a jednotkovej predajnej ceny výrobku. Produkt na riadku cenovej ponuky založenej na produkte môže pochádzať z katalógu produktov v predaji alebo môže byť produktom, ktorý definujete. Tento typ riadka cenovej ponuky je k dispozícii aj v cenových ponukách, ktoré sú vytvorené pomocou PSA.

Čiastka v cenovej ponuke je súčtom riadkov založených na produkte a riadkov založených na projekte.

> [!NOTE]
> Cenové ponuky a riadky cenových ponúk sa v zariadení PSA nevyžadujú. Proces projektu môžete spustiť pomocou projektovej zmluvy (predaného projektu). Vždy je však potrebná príležitosť bez ohľadu na to, či začnete s ponukou alebo projektovou zmluvou.

## <a name="project-based-quote-lines"></a>Zobrazuje riadky cenovej ponuky založené na projekte.

Riadok cenovej ponuky založený na projekte v PSA má nasledujúce metódy fakturácie:

- Čas a materiál
- Pevná cena

### <a name="time-and-material"></a>Čas a materiál

Metóda fakturácie času a materiálu je založená na spotrebe. Keď vyberiete túto fakturačnú metódu, zákazník sa fakturuje, pretože v projekte vzniknú náklady. Faktúry sú vytvorené na základe dátumu periodickej frekvencie. Počas predajného procesu poskytuje ponuková hodnota časovej a materiálnej zložky iba odhad konečných nákladov pre zákazníka. Dodávateľ sa zaväzuje dokončiť projekt presne na ponukovú hodnotu. Komponenty času a materiálu zvyšujú riziko zákazníka. Zákazníci by mohli chcieť rokovať o dodatočnom neprekračovaní doložiek, aby sa minimalizovalo ich riziko. PSA nepodporuje nastavenie neprekračovať doložky.

### <a name="fixed-price"></a>Pevná cena

V metóde fakturovania pevnej ceny sa dodávateľ zaväzuje dodávať projekt za pevnú cenu zákazníkovi. Zákazníkovi sa fakturuje ponuková hodnota riadka s pevnou cenou, bez ohľadu na náklady, ktoré dodávateľ vyrobil na doručenie daného riadka cenovej ponuky. Hodnota riadka s pevnou cenou sa fakturuje jedným z nasledujúcich spôsobov: 

- Ako paušálna suma na začiatku alebo na konci projektu, alebo keď je dosiahnutý míľnik projektu. 
- Na základe frekvencie založenej na dátume rovnakých splátok pevnej hodnoty v riadku cenovej ponuky. Tieto splátky sú známe ako periodické míľniky.
- V splátkach, ktoré majú peňažnú hodnotu, ktorá je v súlade s pokrokom práce alebo konkrétne míľniky, ktoré sú dosiahnuté na projekte. V tomto prípade sa hodnota každej splátky môže líšiť, ale všetky sa musia pridať do pevnej hodnoty v riadku cenovej ponuky.

PSA podporuje všetky tri typy fakturačných rozvrhov pre riadky s pevnou cenou.

## <a name="transaction-classification"></a>Klasifikácia transakcie

Profesionálne servisné organizácie zvyčajne oceňujú a fakturujú svojich zákazníkov podľa klasifikácie nákladov. V PSA sú náklady reprezentované nasledujúcimi klasifikáciami transakcií:

- **Čas** – Táto klasifikácia predstavuje náklady na prácu alebo ľudské zdroje ' čas na projekte.
- **Výdavok**: – Táto klasifikácia predstavuje všetky ostatné druhy výdavkov na projekt. Pretože výdavky môžu byť široko klasifikované, väčšina organizácií vytvára podkategórie, ako je cestovanie, požičovňa áut, hotel, alebo kancelárske potreby.
- **Poplatok** – Táto klasifikácia predstavuje rôzne režijné náklady, penále a iné položky, ktoré sú účtované zákazníkovi. 
- **Daň** – Táto klasifikácia predstavuje čiastky dane, ktoré používatelia pridajú pri zadávaní výdavkov.
- **Materiálová transakcia** – Táto klasifikácia predstavuje skutočné hodnoty z produktových radov na potvrdenej faktúre projektu.
- **Míľnik** – Táto klasifikácia je používaná logikou fakturácie fixnej ceny v psa.

Jedna alebo viacero klasifikácií transakcie môže byť priradených ku riadkom cenovej ponuky. Po zvíťazení cenovej ponuky sa priradenie medzi klasifikáciou transakcie a riadkom cenovej ponuky prevedie do riadka zmluvy.
 
> ![Screenshot mapovania typov transakcií do ponukových a zmluvných riadkov](media/basic-guide-5.png)
  
Cenová ponuka môže napríklad obsahovať nasledujúce dva riadky cenovej ponuky: 
- Konzultačná práca, ktorá používa metódu fakturácie času a materiálu, kde sa uplatňujú klasifikácie transakcií s časom a poplatkami. Napríklad všetky transakcie času a poplatkov pre príklad **Dynamics AX Implementácie** projektu sú fakturované zákazníkovi na základe času a materiálov, ktoré sa používajú. 
- Súvisiace cestovné výdavky, ktoré používajú metódu účtovania pevnej ceny. Napríklad, všetky cestovné výdavky na **Dynamics AX implementáciu** príkladný projekt sú fakturované pevnou peňažnou hodnotou.

> [!NOTE]
> Kombinácia projektu a klasifikácie transakcií **času**, **nákladov** a **poplatkov**, ktoré súvisia s riadkom cenovej ponuky alebo riadkom zmluvy, musia byť jedinečná. Ak je rovnaká kombinácia projektovej a transakčnej triedy priradená k viac ako jednému riadku zmluvy alebo riadku cenovej ponuky, PSA nebude pracovať správne.

## <a name="billing-types"></a>Typy fakturácie

Pole **typy fakturácie** definuje koncept možnosti vzniku daňovej povinnosti v PSA. Je to množina možností, ktorá má nasledujúce možné hodnoty:

- **Účtovateľné** – náklady, ktoré vznikli touto úlohou/kategóriou, sú priame náklady, ktoré riadia realizáciu projektu a zákazník bude za túto prácu platiť. Platba môže byť podaná ako časovo-materiálová alebo fixná-cena dojednania. Zamestnanec, ktorý tento čas trávi, však získa zodpovedajúci kredit za jeho fakturovateľné využitie.
- **Neúčtovateľné** – náklady, ktoré vznikli touto úlohou/kategóriou, sú považované za priame náklady, ktoré riadia realizáciu projektu, no napriek tomu zákazník nerozpozná tento fakt a nebude za túto prácu platiť. Zamestnanec, ktorý trávi tento čas, nebude pripísaný na fakturovateľné využitie.
- **Bezplatné** – náklady, ktoré vznikli touto úlohou/kategóriou, sú považované za priame náklady, ktoré riadia realizáciu projektu a zákazník rozozná tento fakt. Zamestnanec, ktorý trávi tento čas, bude pripísaný na fakturovateľné využitie. Táto cena však nie je účtovaná zákazníkovi.
- **Nie je k dispozícii** – náklady vynaložené na interné projekty, ktoré nevyžadujú sledovanie výnosov, sa sledujú pomocou tejto možnosti.

## <a name="invoice-schedule"></a>Plán faktúry

Plán faktúry je séria dátumov, ktoré sa pri fakturácii projektu vyskytnú. Môžete voliteľne vytvoriť plán fakturácie v riadku cenovej ponuky v zariadení PSA. Každý riadok cenovej ponuky môže mať vlastný plán fakturácie. Ak chcete vytvoriť plán fakturácie, musíte poskytnúť nasledovné hodnoty atribútov:

- Dátum začatia fakturácie 
- Dátum dodania, ktorý predstavuje koncový dátum fakturácie projektu
- Frekvencia faktúr

PSA používa tieto tri hodnoty atribútov na generovanie predbežného súboru dátumov na zriadenie fakturácie.

## <a name="invoice-frequency"></a>Frekvencia faktúr

Faktúra frekvencia je entita, ktorá uchováva hodnoty atribútov, ktoré pomáhajú vyjadriť frekvenciu vytvárania faktúr. Nasledujúce atribúty vyjadrujú alebo definujú entitu frekvencia faktúr:

- **Obdobie** - obdobia mesačne, dvakrát týždenne, a týždenne sú podporované. 
- **Spustenia za obdobie** - pre týždenné a dvojtýždňové obdobie, môžete definovať iba jedno spustenie za obdobie. V mesačných obdobiach môžete definovať medzi jedným a štyrmi spusteniami za obdobie. 
- **Dni spustenia** – dni, kedy sa má fakturácia spustiť. Tento atribút môžete nastaviť dvoma rôznymi spôsobmi:
  - **Pracovné dni** – môžete napríklad určiť, že fakturácia sa spustí každý pondelok alebo každý druhý pondelok. Zákazníci, ktorí musia nastaviť fakturáciu na spustenie v pracovnom dni, môžu preferovať tento typ konfigurácie. 
  - **Kalendárne dni** – môžete napríklad určiť, že fakturácia sa spustí v siedmom a dvadsiatom prvom dni každého mesiaca. Niektoré organizácie môžu preferovať tento typ konfigurácie, pretože to pomáha zaručiť, že fakturácia je spustená na pevný harmonogram každý mesiac.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Plán fakturácie pre riadok cenovej ponuky s pevnou cenou

Pre riadok cenovej ponuky s pevnou cenou môžete použiť mriežku **plánu fakturácie** na vytvorenie míľnikov fakturácie, ktoré sa rovnajú hodnote riadka cenovej ponuky.

- Ak chcete vytvoriť rovnako rozdelené fakturačné míľniky, vyberte frekvenciu fakturácie, zadajte dátum začiatku fakturácie v riadku cenovej ponuky a vyberte **požadovaný dátum dokončenia** cenovej ponuky v sekcii **súhrn** v hlavičke cenovej ponuky. Potom vyberte **generovať periodické míľniky** na vytvorenie rovnomerne rozdelených míľnikov na základe vybranej frekvencie faktúr. 
- Ak chcete vytvoriť míľnik fakturácie paušálnej čiastky, vytvorte míľnik a potom zadajte hodnotu riadka cenovej ponuky ako čiastku míľnika.
- Ak chcete vytvoriť fakturačné míľniky, ktoré sú založené na konkrétnych úlohách v pláne projektu, vytvorte míľnik a mapujte ho na prvok plánu projektu v používateľskom rozhraní fakturačného míľnika.
