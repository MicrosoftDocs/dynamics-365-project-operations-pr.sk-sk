---
title: Sledovanie predajov v rámci projektu
description: Táto téma poskytuje informácie o tom, ako Project Operations sleduje pokrok oproti výnosom z práce na projekte.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: fff5fa6b12dddd780eb6bf77edca85a3a0c0629c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583465"
---
# <a name="project-sales-tracking"></a>Sledovanie predajov v rámci projektu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations sleduje odhady pracovných síl a výnosov na plán projektu s maximálne požadovanou podrobnosťou. Odhad výnosov z práce je založený na plánovanom úsilí a všeobecných alebo pomenovaných zdrojoch, ktoré sú priradené ku každej úlohe spojenej s uzlom v projektovom pláne. Keď sa projekt začne a ľudia začnú reportovať čas o rôznych projektových úlohách, zhrnú sa skutočné výnosy z práce, čo spustí výpočet projekcií.

## <a name="labor-revenue-tracking-view"></a>Zobrazenie sledovania výnosov z práce

Na stránke **Projekty** na karte **Sledovanie** môžete vybrať **Sledovanie** > **Náklady** a otvoriť zobrazenie **Sledovanie nákladov**. Alebo môžete vybrať **Použite** > **Sadzba fakturácie** a otvoriť zobrazenie **Sledovanie výnosov** , ktoré ukazuje pokrok vo výnosoch z práce pre každú úlohu v pláne projektu. Toto zobrazenie tiež porovnáva skutočné výnosy z práce vynaložené na úlohu s plánovanými výnosmi z práce. Project Operations používa na výpočet metrík výnosov z práce nasledovné vzorce:

- **Plánované výnosy**: Odhadované hodnoty predaja na všetky priradenia zdrojov k každej úlohe listového uzla
- **Skutočné výnosy**: Súčet všetkých skutočných nefakturovaných predajov za čas zaznamenaný na úlohe
- **Fakturovateľné výnosy %**: Skutočné výnosy ÷ Odhad výnosov pri dokončení
- **Zostávajúce výnosy**:Odhad výnosov pri dokončení – Skutočné výnosy
- **Odhadované výnosy pri dokončení**: Zostávajúce výnosy + Skutočné výnosy
- **Odchýlka výnosov**: Plánované výnosy – Odhadované výnosy pri dokončení


> [!NOTE]
> Project Operations zobrazuje iba výnosy z práce na stránke **Projekt** na karte **Sledovanie**. Keďže materiály a náklady je možné odhadnúť a sledovať na základe spotreby, tieto výnosy nie sú zahrnuté vo výnosoch uvedených na karte **Sledovanie**. Táto karta je navrhnutá tak, aby fungovala iba na opätovné premietnutie výnosov z práce opätovným premietnutím úsilia.  
> Všetky zobrazené sumy výnosov sa prevedú na menu nákladov projektu. Mena nákladov projektu je mena zmluvnej jednotky na projekte. Pre projekty s pevnou cenou čísla výnosov v zobrazení **Sledovania výnosov z práce** nie sú relevantné, pretože nefakturované skutočné hodnoty predaja sa nezaznamenávajú pri schvaľovaní času.
> Odhadované hodnoty predaja za čas, ktoré sú uvedené na karte **Odhad** projektu, sa nemusia pridať do plánovanej hodnoty výnosov na karte **Sledovanie**. Zdroj tohto nesúladu je z dvoch možných dôvodov:
><ol>
   ><li> Karta <b>Odhady</b> zobrazuje odhadované výnosy v mene predaja, zatiaľ čo karta <b>Sledovanie</b> zobrazuje plánované výnosy prevedené do meny nákladov. </li>
   ><li> Keď sa odhadovaný predaj prevedie na zmluvnú menu, ako je uvedené na karte <b>Odhady</b>, pri konverzii sa vykonávajú kroky, ktoré by mohli viesť k strate presnosti: </li>
><ol>
><li> Odhadovaná výška predaja v mene zmluvy sa najprv prevedie na základnú menu (prepočet 1).</li>
><li> Odhadovaná výška predaja v základnej mene sa prevedie na menu projektových nákladov (prepočet 2). </li>
></ol>
></ol>
> V obidvoch krokoch sa použije presnosť meny, čo má za následok odchýlku plánovaného výnosu v mene projektu od plánovaného predaja v zmluvnej mene.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Preplánovanie výnosov na úlohy listových uzlov

Mzdové výnosy na úlohu listového uzla nemožno na projekte priamo premietnuť na karte **Sledovanie** na stránke **Projekt**. Môžete však použiť zobrazenie **Sledovanie úsilia** na preplánovanie zostávajúceho úsilia na vykonanie úlohy. To spôsobí prepočet zostávajúcich výnosov na úlohu. Nasleduje popis toho, ako to funguje.

1. Manažér projektu môže preplánovať úsilie na úlohy aktualizáciou predvolenej hodnoty v poli **Zostávajúce úsilie** novým odhadom zostávajúceho úsilia na úlohu. Preplánovanie spôsobuje prepočet odhadu úsilia úlohy po dokončení (EAC), percentuálneho pokroku a projektovanej odchýlky úsilia pri úlohe. EAC, odhad do dokončenia (ETC) a percento pokroku na súhrnných úlohách sú tiež prepočítané a vytvárajú nový predpoklad variácie úsilia.
2. Na základe novej hodnoty pre zostávajúce úsilie na úlohe systém vypočíta zostávajúce úsilie v zobrazení **Sledovanie výnosov**. Ak chcete vypočítať zostávajúce výnosy na základe zostávajúceho úsilia, systém najskôr vypočíta priemerné výnosy na jednu hodinu úsilia na súhrnnej úlohe ako plánované výnosy alebo plánované úsilie. Plánované výnosy sú súčtom výnosov na všetky priradenia zdrojov k úlohe. Priemerné výnosy za hodinu sa používajú na výpočet zostávajúcich výnosov na novo projektované zostávajúce úsilie týkajúce sa úlohy.
3. Prepočítajú sa odhadované výnosy na dokončenie a percentuálna spotreba výnosov na úlohe listového uzla.
4. Vypočíta sa hodnota výnosov na dokončenie súhrnných úloh až po koreňový uzol.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Preplánovanie výnosov na súhrnné úlohy

Môžete preplánovať mzdové výnosy na súhrnné úlohy alebo kontajnerové úlohy. Mzdové výnosy na súhrnnú úlohu projektu však nemôžete preplánovať priamo na karte **Sledovanie** na stránke **Projekt**. Podobne ako v prípade úloh listových uzlov, prepracovanie súhrnných a kontajnerových úloh je možné vykonať pomocou zobrazenia **Sledovanie úsilia**. V tomto zobrazení môžete opätovne preplánovať zostávajúce úsilie na súhrnnú úlohu a spôsobiť prepočet zostávajúcich výnosov na súhrnnú úlohu. Nasleduje popis toho, ako to funguje.

1. Manažér projektu môže preplánovať úsilie na úlohy aktualizáciou predvolenej hodnoty v poli **Zostávajúce úsilie** novým odhadom **zostávajúceho úsilia** na úlohu. Preplánovanie spôsobuje prepočet odhadu úlohy po dokončení (EAC), percentuálneho pokroku a projektovanej odchýlky úsilia pri úlohe. Odhad pri dokončení, odhad do dokončenia a percento pokroku na súhrnných úlohách sú tiež prepočítané a vytvárajú nový predpoklad variácie úsilia.
2. Na základe novej hodnoty v poli **Zostávajúce úsilie** v úlohe systém vypočíta zostávajúce úsilie v zobrazení **Sledovanie výnosov**. Ak chcete vypočítať zostávajúce výnosy na základe zostávajúceho úsilia, systém najskôr vypočíta priemerné výnosy na jednu hodinu úsilia na súhrnnej úlohe ako plánované výnosy alebo plánované úsilie. Plánované výnosy sú súčtom výnosov na všetky priradenia zdrojov k úlohe. Tieto Priemerné výnosy za hodinu sa potom použijú na výnosov na novo projektované zostávajúce úsilie týkajúce sa úlohy.
3. Prepočítajú sa odhadované výnosy na dokončenie a percentuálna spotreba výnosov na súhrnnú úlohu.
4. Nová hodnota predpokladaných výnosov na dokončenie sa rozdelí na podradené úlohy v rovnakom pomere ako bolo pri originálnych plánovaných výnosoch v rámci úlohy.
5. Vypočíta sa nový odhadovaný výnos na dokončenie každej z jednotlivých úloh až po listový uzol. Na základe tejto hodnoty sa prepočítajú zostávajúce výnosy a percentuálna hodnota výnosov ovplyvnených podradených úloh až po listové uzly na základe hodnoty výnosov na dokončenie. To má za následok nové predpoklady pre variáciu výnosov úlohy. 
6. Vypočíta sa hodnota výnosov na dokončenie súhrnných úloh až po koreňový uzol.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

