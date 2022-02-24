---
title: Sledovanie nákladov projektu
description: Táto téma poskytuje informácie o tom, ako Project Operations sleduje pokrok oproti mzdovým nákladom a výdavkom na projekt.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28cb692c61ae4137a28973dc1bd70ffd989dd535
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711086"
---
# <a name="labor-cost-tracking-on-projects"></a>Sledovanie mzdových nákladov na projekty

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations sleduje odhady pracovných síl a výdavky na plán projektu s maximálne požadovanou podrobnosťou. Finančný odhad mzdových nákladov je založený na plánovanom úsilí a všeobecných alebo pomenovaných zdrojoch, ktoré sú priradené ku každej úlohe spojenej s uzlom v projektovom pláne. Keď sa projekt začne a ľudia začnú reportovať čas o rôznych projektových úlohách, zhrnú sa skutočné výdavky na prácu, ktorá spustí výpočet projekcií.

## <a name="labor-cost-tracking-view"></a>Zobrazenie sledovania mzdových nákladov

Na stránke **Projekty** na karte **Sledovanie** môžete vybrať **Sledovanie** > **Náklady** a otvoriť zobrazenie **Sledovanie nákladov** a vidieť postup prác vynaložených na každú úlohu v pláne projektu. Tento pohľad tiež porovnáva skutočné mzdové náklady vynaložené na úlohu s plánovanými mzdovými nákladmi. Project Operations používa na výpočet metrík mzdových nákladov nasledovné vzorce:

- **Plánované náklady**: Odhadované náklady na všetky priradenia zdrojov k každej úlohe listového uzla
- **Skutočné náklady**: Súčet všetkých skutočných nákladov za čas zaznamenaný na úlohe
- **Percento spotreby nákladov**: Skutočné náklady ÷ Odhad nákladov na dokončenie
- **Zostávajúce náklady**: Odhad nákladov na dokončenie – Skutočné náklady
- **Náklady na dokončenie**: Zostávajúce náklady + Skutočné náklady
- **Odchýlka nákladov**: Plánované náklady – Odhad nákladov na dokončenie

Každá úloha zobrazuje predpoklad variácie nákladov v úlohe. Ak je odhad nákladov po dokončení vyšší ako plánované náklady, predpokladá sa, že úloha prekročí rozpočet. Ak je odhad nákladov po dokončení nižší ako plánované náklady, predpokladá sa, že úloha bude pod rámec rozpočtu.

>[!NOTE]
> Project Operations zobrazuje iba mzdové náklady na stránke **Projekt** na karte **Sledovanie**. Keďže materiály a náklady je možné odhadnúť a sledovať na základe spotreby, tieto náklady nie sú zahrnuté v nákladoch uvedených na karte **Sledovanie**. Táto karta je navrhnutá tak, aby fungovala iba na opätovné premietnutie nákladov práce opätovným premietnutím úsilia.
Všetky zobrazené sumy nákladov sa prevedú na menu nákladov projektu z meny obstarávacej ceny projektu, ktorá sa používa na určenie nákladovej sadzby. Mena nákladov projektu je mena zmluvnej jednotky na projekte. Odhadované hodnoty nákladov za čas, ktoré sú uvedené na karte **Odhady** na stránke **Projekt** sa nemusia pridávať k plánovaným nákladom na karte **Sledovanie**. Dôvodom tohto rozdielu sú rozdiely v sumarizácii odhadovaných nákladov na mriežke **Odhady** a ako sa plánované náklady vypočítavajú z mriežky **Sledovanie**. 
>
> - **Karta Odhady** vypočítava odhadované náklady pomocou rovnakej meny nákladovej sadzby ako je v cenníku. Potom sa odhadované náklady v mene cenníka prevedú na odhadované náklady v mene nákladov projektu. Odhadované náklady v mene projektu sa zobrazia zaokrúhlené na 2 desatinné miesta. V žiadnom okamihu tejto konverzie sa nepoužíva presnosť meny. 
> - Na karte **Sledovanie** sa výpočet plánovaných nákladov riadi mierne odlišným poradím výpočtu, ktoré spočíva v použití presnosti meny v dvoch fázach: 
   ><ol>
   ><li>Odhadovaná výška nákladov v mene cenníka sa prevedie na základnú menu (prepočet 1).</li>
   ><li>Odhadovaná výška nákladov v základnej mene sa prevedie na menu projektových nákladov (prepočet 2). </li>
   ></ol>
   >Presnosť meny sa používa v oboch krokoch na získanie plánovaných nákladov (na karte **Sledovanie**), ktorá sa mierne odchyľuje od odhadovaných nákladov (v zobrazení **Časovo odstupňované** na karte **Odhady**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Preplánovanie nákladov na úlohy listových uzlov

Mzdové náklady na úlohu listového uzla nemožno na projekte priamo premietnuť na karte **Sledovanie** na **Stránke projektu**. Môžete však použiť zobrazenie **Sledovanie úsilia** na preplánovanie zostávajúceho úsilia na vykonanie úlohy. To spôsobí prepočet zostávajúcich nákladov na úlohu. Nasleduje popis toho, ako to funguje.

1. Manažér projektu môže preplánovať úsilie na úlohy aktualizáciou predvolenej hodnoty v poli **Zostávajúce úsilie** novým odhadom zostávajúceho úsilia na úlohu. Preplánovanie spôsobuje prepočet odhadu úsilia úlohy po dokončení (EAC), percentuálneho pokroku a projektovanej odchýlky úsilia pri úlohe. EAC, odhad do dokončenia (ETC) a percento pokroku na súhrnných úlohách sú tiež prepočítané a vytvárajú nový predpoklad variácie úsilia.
2. Na základe novej hodnoty pre zostávajúce úsilie na úlohe systém vypočíta zostávajúce náklady v zobrazení **Sledovanie nákladov**. Ak chcete vypočítať zostávajúce náklady na základe zostávajúceho úsilia, systém najskôr vypočíta priemerné náklady na jednu hodinu úsilia na úlohe ako plánované náklady alebo plánované úsilie. Plánované náklady sú súčtom nákladov na všetky priradenia zdrojov k úlohe. Priemerná cena za hodinu sa používa na výpočet zostávajúcich nákladov na novo projektované zostávajúce úsilie týkajúce sa úlohy.
3. Prepočítajú sa náklady na dokončenie a percentuálna spotreba nákladov na úlohe listového uzla.
4. Vypočíta sa hodnota nákladov na dokončenie súhrnných úloh až po koreňový uzol.

## <a name="reprojecting-costs-on-summary-tasks"></a>Preplánovanie nákladov na súhrnné úlohy

Môžete preplánovať mzdové náklady na súhrnné úlohy alebo kontajnerové úlohy. Mzdové náklady súhrnnú úlohu projektu však nemôžete preplánovať priamo na karte **Sledovanie** na stránke **Projekt**. Podobne ako v prípade úloh listových uzlov, prepracovanie súhrnných a kontajnerových úloh je možné vykonať pomocou zobrazenia **Sledovanie úsilia**. V tomto zobrazení môžete opätovne preplánovať zostávajúce úsilie na súhrnnú úlohu a spôsobiť prepočet zostávajúcich nákladov na súhrnnú úlohu. Nasleduje popis toho, ako to funguje.

1. Manažér projektu môže preplánovať úsilie na súhrnné úlohy aktualizáciou predvolenej hodnoty zostávajúceho úsilia novým odhadom úlohy. Táto aktualizácia spôsobuje prepočet odhadu súhrnnej úlohy po dokončení (EAC), percentuálneho pokroku a projektovanej odchýlky úsilia pri úlohe. Odhad pri dokončení, odhad do dokončenia a percento pokroku na súhrnných úlohách sú tiež prepočítané a vytvárajú nový predpoklad variácie úsilia.
2. Na základe novej hodnoty pre zostávajúce úsilie na súhrnnej úlohe systém vypočíta zostávajúce náklady v zobrazení **Sledovanie nákladov**. Ak chcete vypočítať zostávajúce náklady na základe zostávajúceho úsilia, systém najskôr vypočíta priemerné náklady na jednu hodinu úsilia na súhrnnej úlohe ako plánované náklady alebo plánované úsilie. Priemerná cena za hodinu sa používa na výpočet nákladov na novo projektované zostávajúce úsilie týkajúce sa súhrnnej úlohy.
3. Prepočítajú sa náklady na dokončenie a percentuálna spotreba nákladov na súhrnnej úlohe.
4. Nové náklady na dokončenie sa rozdelia na podradené úlohy v rovnakom pomere ako bolo pri originálnych plánovaných nákladoch v rámci úlohy.
5. Vypočíta sa nová hodnota nákladov na dokončenie každej z jednotlivých úloh až po listový uzol. Na základe tejto hodnoty sa prepočítajú zostávajúce náklady a percentuálna hodnota spotreby ovplyvnených podradených úloh až po listové uzly na základe hodnoty nákladov na dokončenie. To má za následok nové projekcie pre variáciu nákladov úlohy. 


Pole **Výkonnosť nákladov** je možné nastaviť z údajov o sledovaní. Keď je odchýlka nákladov pre koreňový uzol v zobrazení **Sledovanie nákladov** záporná, môžete toto pole nastaviť na **Pod rámec rozpočtu**. Keď je odchýlka nákladov pre koreňový uzol kladná, môžete nastaviť hodnotu na **Nad rámec rozpočtu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
