---
title: Správa projektových cenníkov v cenovej ponuke
description: Táto téma poskytuje informácie o entite Projektový cenník.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4bd4e9cb22bfd6a86fd86e5fc403cb185aab140a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277762"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Správa projektových cenníkov v cenovej ponuke

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations rozširuje cenníkovú entitu v Dynamics 365 Sales. 

## <a name="key-entities"></a>Kľúčové entity

Cenník obsahuje informácie, ktoré poskytujú štyri rôzne entity:

- **Cenník**: Táto entita uchováva informácie o kontexte, mene, dátovej účinnosti a časovej jednotke pre čas tvorby cien. Kontext ukazuje, či cenník vyjadruje nákladové sadzby alebo predajné sadzby. 
- **Mena**: Táto entita uchováva menu cien v cenníku. 
- **Dátum**: Táto entita sa používa, keď sa systém pokúsi zadať predvolenú cenu transakcie. Vyberie sa cenník, ktorý má dátum účinnosti, ktorý zahŕňa dátum transakcie. Ak sa nájde viac ako jeden cenník, ktorý je efektívny pre dátum transakcie a je pripojený k súvisiacej cenovej ponuke, zmluve alebo organizačnej jednotke, potom nie je žiadna cena predvolená. 
- **Čas**: Táto entita uchováva jednotku času, v ktorej sú vyjadrené ceny, napríklad denné alebo hodinové sadzby. 

Entita cenníka má tri súvisiace tabuľky, ktoré ukladajú ceny:

  - **Cena roly**: Táto tabuľka uchováva sadzbu pre kombináciu rolí a hodnôt organizačných jednotiek a používa sa na nastavenie cien na základe rolí pre ľudské zdroje.
  - **Cena transakčnej kategórie**: Táto tabuľka ukladá ceny podľa transakčnej kategórie a používa sa na nastavenie cien výdavkových kategórií.
  - **Položky v cenníku**: Táto tabuľka ukladá ceny pre katalóg produktov.
 
Cenník je karta s oceneniami. Karta s oceneniami je kombináciou entity cenníka a súvisiacich riadkov v tabuľke cena role, cena transakčnej kategórie a položky cenníka.

## <a name="resource-roles"></a>Zdrojové roly

Termín *zdrojová rola* odkazuje na množinu zručností, kompetencií a certifikátov, ktoré musí daná osoba vykonať, aby na projekte vykonala konkrétnu množinu úloh.

Čas ľudských zdrojov sa naceňuje na základe roly, že zdroj vykoná konkrétny projekt. Pre čas ľudských zdrojov, sú rozpočty a fakturácie založené na role zdroja. Čas môže byť ocenený v ktorejkoľvek jednotke v **Časovej** skupine jednotiek.

Jednotková skupina **Čas** sa vytvorí pri inštalácii Project Operations. Má predvolenú jednotku **hodina**. Nie je možné vymazať, premenovať ani upraviť atribúty jednotkovej skupiny **Čas** ani jednotky **Hodina**. Do skupiny **časových** jednotiek však môžete pridať ďalšie jednotky. Ak sa pokúsite odstrániť jednotkovú skupinu **Čas** alebo jednotku **Hodina**, môže dôjsť k zlyhaniu v obchodnej logike.
 
## <a name="transaction-categories-and-expense-categories"></a>Kategórie transakcií a kategórie nákladov

Cestovné a iné náklady, ktoré vzniknú konzultantom projektu, sú účtované zákazníkovi. Oceňovanie kategórií výdavkov prebieha pomocou cenníkov. Letecká tarifa, hotel, a požičovňa áut sú príklady pre kategóriu nákladov. Každý riadok cenníka pre náklady určuje ceny pre konkrétnu kategóriu nákladov. Na kategórie cenových výdavkov sa používajú tieto tri spôsoby:

- **Na úrovni nákladu**: Výdavkový náklad sa fakturuje zákazníkovi a nepoužije sa žiadna prirážka.
- **Percento prirážky**: Percento oproti skutočným nákladom sa fakturuje zákazníkovi. 
- **Cena za jednotku**: Fakturačná cena je nastavená pre každú jednotku kategórie výdavkov. Čiastka, ktorá je fakturovaná zákazníkovi sa vypočíta na základe počtu jednotiek nákladov, ktoré konzultant hlási. Vzdialenosť používa metódu cenotvorby cena za jednotku. Napríklad, kategória nákladov za vzdialenosť môže byť nakonfigurovaná na 30 amerických dolárov (USD) za deň alebo 2 USD za míľu. Keď konzultant hlási vzdialenosť na projekte, suma na fakturáciu sa vypočíta na základe počtu míľ, ktoré konzultant oznámil.
 
## <a name="project-sales-pricing-and-overrides"></a>Predajné ceny projektu a ich prepísanie

V prípade projektových ponúk a zmlúv má cenník projektu odlišný vzor prepísania ceny ako cenník produktov. V radku cenovej ponuky založenej na katalógu produktov, môžete prepísať cenu do rolí a kategórií priamo v riadku cenovej ponuky, pretože každý riadok cenovej ponuky poukazuje na presne jednu položku katalógu. V riadku cenovej ponuky založenej na projekte však nie je možné prepísať cenu na roly a kategórie priamo v riadku cenovej ponuky. Použite cenník projektu na podporu dvoch odlišných vzorov prepísania.

> [!NOTE]
> Odporúčame, že máte samostatný cenník pre vaše projektové zdroje a položky katalógu, kvôli rozdielom v správaní medzi oboma pri prepismi cenotvorby.

Každá z nasledujúcich entít môže mať jednu alebo viac priradených predajných cenníkov pre cenotvorbu projektu:

- Zákaznícke (konto) 
- Príležitosť 
- Cenová ponuka 
- Projektová zmluva

Združenie týchto entít s cenníkmi je indikované projektovými cenníkmi. Môžete priradiť jeden alebo viac cenníkov s entitami zákazníka, príležitosti, cenovej ponuky a projektovej predajnej zmluvy.

Predvolený zoznam projektových cenníkov nie je automaticky zadaný v zázname zákazníka. Zoznam projektových cenníkov však môžete manuálne priložiť k záznamu zákazníka. Avšak, mali by ste manuálne priložiť projektový cenník len vtedy, ak máte vlastnú cenovú dohodu so zákazníkom. 

Ak je zoznam projektových cenníkov pripojený k predajnej entite, overujú sa nasledujúce informácie:

- Cenník má kontext **Predaj**. 
- Mena zákazníka sa musí zhodovať s menou uvedenou v cenníku. 

Na projektovej zmluve sa používa nasledujúce poradie priority na automatické nastavenie súvisiacich projektových cenníkov:

1. Ponuka
2. Príležitosť
3. Zákazník 
4. Globálne nastavenia 

Ak je projektový cenník predvolene zadaný, systém overí, či mena zodpovedá mene zákazníka, a či predvolené cenníky, ktoré boli zadané, majú kontext **Predaj**.

Môžete priradiť viacero cenníkov s entitami zákazníka, príležitosti, cenovej ponuky a projektovej zmluvy. Táto funkcia podporuje predvolený dátum predvolené ceny pre dlho-bežiaci projekt zmluvy, kde môžete požadovať viac ako jeden cenník na účet pre cenové aktualizácie, ktoré nastanú z dôvodu inflácie. Ak však cenové zoznamy, ktoré priradíte k entite zákazník, príležitosť, cenová ponuka alebo zmluva o projekte, majú prekrývajúcu sa účinnosť dátumu, predvolené ceny môžu byť nesprávne. Preto by ste sa mali uistiť, že projektové cenníky, ktoré majú prekrývanie dátumovej efektívnosti nie sú spojené s týmito entitami.

### <a name="deal-specific-price-overrides"></a>Dohoda-špecifická cena sa prepíše

Môžete vytvoriť dohodou špecifikované prepisy pre určité projektové cenníky, ktoré sú predvolene zadané v cenovej ponuke alebo projektovej zmluve.

V predvolenom nastavení projektovej zmluvy vždy dostane kópiu hlavný predajný cenník namiesto priameho prepojenia na neho. Toto správanie pomáha zaručiť, že cenové dohody so zákazníkom pre vyhlásenie o dielo (SOW) sa nemenia, ak sa zmení hlavný cenník.

V cenovej ponuke však môžete použiť hlavný cenník. Alternatívne môžete tiež skopírovať hlavný cenník a upraviť ho tak, aby sa vytvoril vlastný cenník, ktorý sa vzťahuje len na danú cenovú ponuku. Ak chcete vytvoriť nový cenník, ktorý je špecifický pre cenovú ponuku, na stránke **cenová ponuka** vyberte položku **vytvoriť vlastnú tvorbu cien**. Prístup k projektovému cenníku špecifických dohôd môžete získať iba z cenovej ponuky. 

Keď vytvoríte vlastný projektový cenník, skopírujú sa iba súčasti projektu z cenníka. Inými slovami, nový cenník vytvorený ako kópia existujúceho zoznamu projektových cien, ktorý je priložený k cenovej ponuke, a tento nový cenník má iba súvisiace ceny rolí a ceny transakcií kategórie.
  
## <a name="tracking-costs"></a>Sledovanie nákladov

Project Operations sleduje náklady na využívanie času ľudských zdrojov na projektoch. Tiež sleduje náklady na iné výdavky, ktoré vzniknú v priebehu projektu, ako sú cestovné výdavky.

Rovnako ako fakturačné sadzby, ceny za ľudské zdroje sú tiež nastavené pomocou cenníkov. Tu sú hlavné rozdiely v správaní zoznamu nákladov a predajného cenníka:

- Miera zdrojových nákladov nemôže byť prepísaná na konkrétny projekt, zmluvu alebo cenovú ponuku. Avšak, fakturačné sadzby môžu byť prepísané na založené na dohode, ak sú vykonané zmeny, ktoré sú špecifické pre povahu dohody. 

- Nasledujúca objednávka sa používa na vyriešenie zoznamu nákladových cien:

    1. Cenník, ktorý je pripojený k organizačnej jednotke.
    2. Cenník, ktorý je pripojený k parametrom Project Operations. Vzhľadom na to, že obstarávacie cenníky v mnohých rôznych menách môžu byť pripojené k parametrom, PSA prebehne spárovanie menu medzi menou zmluvnej organizačnej jednotky projektu, zmluvy alebo cenovej ponuky a menou obstarávacieho cenníka.
    3. V prípade výdavkov sa metódy oceňovania nákladov a prirážky za cenu nevzťahujú na zoznamy cenových cien. Aj v prípade, že sa tieto metódy oceňovania používajú v riadkoch cenníka nákladových cien na nastavenie nákladovej kategórie, systém ich ignoruje a nezadá sa žiadna predvolená cena.


[!INCLUDE[footer-include](../includes/footer-banner.md)]