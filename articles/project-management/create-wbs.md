---
title: Vytvorenie štruktúry rozdelenia práce
description: Táto téma vysvetľuje, ako vytvoriť štruktúru rozdelenia práce (WBS) vrátane základných ovládacích prvkov v novom plánovacom rozhraní.
author: ruhercul
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3b8162d256aa145301fc64bee9682caa8737496f
ms.sourcegitcommit: d3f66dfb5978c5c6b7fd51363c7f9278737c49c1
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/17/2021
ms.locfileid: "7928634"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Vytvorenie štruktúry rozdelenia práce (WBS)

Plán projektu komunikuje, aká práca sa musí dokončiť, ktoré zdroje budú vykonávať prácu, a časový rámec, v ktorom práca musí byť dokončená. Plán odráža všetky práce spojené s realizáciu projektu na čas. V Dynamics 365 Project Operations vytvoríte harmonogram projektu nasledovne:

  - Rozdelenie práce do konkrétnych úloh.
  - Odhad času potrebného na vykonanie každej úlohy.
  - Nastavenie závislostí úloh.
  - Nastavenie trvania úloh.
  - Odhadovanie všeobecných zdrojov, ktoré budú robiť dané úlohy. 

Plán projektu sa vytvorí na karte **Plán** na stránke **Projekt**.

## <a name="tasks"></a>Úlohy

Prvým krokom pri vytváraní plánu projektu je rozdelenie na zvládnuteľné porcie. Plán v Project Operations podporuje nasledujúce funkcie:

- Súhrn alebo zásobník úloh
- Úlohy listového uzla

### <a name="summary-tasks"></a>Súhrnné úlohy

Súhrnné úlohy môžu ukladať ďalšie súhrnné úlohy alebo úlohy listových uzlov. Nemajú na seba žiadne pracovné úsilie alebo náklady. Namiesto toho ich pracovné úsilie a náklady sú súhrnom úsilia a nákladov na ich kontajnerové úlohy. Počiatočný dátum súhrnnej úlohy je dátum začatia kontajnerovej úlohy a koncový dátum je dátum ukončenia kontajnerovej úlohy. Názov súhrnnej úlohy je možné upraviť, ale nie je možné upraviť vlastnosti plánovania, vrátane úsilia, dátumov a trvania. Ak odstránite súhrnnú úlohu, odstránite aj všetky jej kontajnerové úlohy.

### <a name="leaf-node-tasks"></a>Úlohy listového uzla

Úloha listového uzla predstavuje najpodrobnejšiu prácu na projekte. Majú odhadnuté úsilie, zdroje, plánovaný dátum začatia a ukončenia a celkové trvanie.

## <a name="create-a-task-hierarchy"></a>Vytvorte hierarchiu úloh

### <a name="add-a-task"></a>Pridanie úlohy

Ak chcete pridať jednu alebo viac úloh, postupujte podľa nasledujúcich krokov.

1. Prejdite na **Projekty** a vyberte a otvorte záznam projektu, pre ktorý chcete vytvoriť plán. 
2. Vyberte kartu **Úlohy**. 
3. Vyberte **Pridať novú úlohu**, zadajte názov úlohy a potom stlačte kláves Enter.
2. Zadajte iný názov úlohy a znova stlačte kláves Enter, až kým nebudete mať úplný zoznam úloh.

### <a name="manage-hierarchy-of-a-task"></a>Spravujte hierarchiu úlohy

Keď je úroveň úlohy znížená, stane sa podradenou úlohou úlohe, ktorá je priamo nad ňou. ID plánu úlohy sa potom prepočíta tak, že je založené na ID plánu svojho nového nadradeného a sleduje prehľad schémy číslovania. Nadradená úloha je teraz súhrnnou úlohou. Preto sa stáva súhrnom jej podradených úloh. Keď je úroveň úlohy zvýšená, táto už nie je podradená úloha úlohe, ktorá bola jej nadradenou úlohou. Potom sa prepočítajú ID plánu tak, aby odrážal aktualizovanú hĺbku a pozíciu úlohy v hierarchii. Úsilie, náklady a dátumy predchádzajúcej nadradenej úlohy sa prepočítajú tak, aby nezahŕňali túto úlohu.

Ak chcete znížiť alebo zvýšiť úlohu, postupujte podľa nasledujúcich krokov.

1. Na stránke **Projekt**, na karte **Úlohy**, v časti **Súhrnné úlohy** vyberte tri zvislé bodky vedľa názvu úlohy a potom vyberte **Vytvoriť vedľajšiu úlohu**. 
2. Vyberte úlohu, ktorú chcete znížiť alebo zvýšiť. Ak chcete vybrať viac ako jednu úlohu, vyberte úlohu, stlačte a podržte Ctrl a potom vyberte ďalšiu úlohu.
2. Výberom **Znížiť** alebo **Zvýšiť podúlohu** presuňte úlohy pod alebo zo súhrnných úloh.

### <a name="move-tasks-up-and-down"></a>Posun úloh nahor a nadol

Úlohy je možné presunúť na ľubovoľnú úroveň v štruktúre rozdelenia práce jedným z dvoch spôsobov:

- Vyberte ešte jednu úlohu a presuňte ich na požadované miesto.
- Vyberte jednu alebo viac úloh, kliknite pravým tlačidlom myši a vyberte **Vystrihnúť**, vyberte cieľovú bunku v pláne, potom kliknite pravým tlačidlom myši a vyberte **Vložiť**.

## <a name="task-attributes"></a>Atribúty úlohy

Názov úlohy popisuje prácu, ktorá sa musí dokončiť. V Project Operations, atribúty priradené k úlohe popisujú plán úlohy a jeho personálne požiadavky.

## <a name="schedule-attributes"></a>Naplánovať atribúty

Atribúty **Úsilie**, **dátum začiatku**, **dátum konca** a **trvanie** určujú plán úlohy.

Nasledujúca tabuľka zobrazuje ďalšie atribúty plánu.

| **Konečný zobrazovaný názov** | **Konečný popis** |
| --- | --- |
| Vynaložené úsilie (hodiny) | Vykonaná práca na úlohe v hodinách. |
| Trvanie: | Zobrazuje trvanie v dňoch pre danú úlohu. |
| Celkové úsilie | Celková práca na úlohe v hodinách. |
| Koniec | Dátum a čas dokončenia. |
| % dokončenia | Percento úlohy, ktorá je dokončená. |
| Projektový kontajner | Panel úloh možno zoskupiť podľa kontajnera, aby mal každý kontajner svoj vlastný stĺpec. |
| Zostávajúce úsilie (hodiny) | Zostávajúca práca na úlohe v hodinách. |
| Podľa začiatku | Dátum a čas začatia. |
| Meno | Názov úlohy. |
| Identifikátor | ID úlohy v štruktúre rozdelenia práce. |

Ako správca môžete definovať vlastné polia pre entitu úlohy. Polia sa však na mriežke rozvrhu nedajú zobraziť. Ak chcete zobraziť svoje vlastné polia, pridajte ich na stránku s podrobnosťami **Projektová úloha**.

## <a name="staffing-attributes"></a>Personálne atribúty

Personálne atribúty sú prístupné prostredníctvom poľa **zdroje** v pláne. Môžete vyhľadať existujúci zdroj alebo vybrať **Vytvoriť** a na paneli **Rýchle vytvorenie** pridať člena projektového tímu ako nový zdroj.  Keď hľadáte zdroj pomocou nástroja na výber zdrojov v mriežke úloh, zobrazení dosky alebo Gantt, vyhľadávanie vráti buď existujúcich členov projektového tímu alebo aktívne rezervovateľné zdroje.

Polia **rola**, **zdrojová jednotka** a **názov pozície** sa používajú na popis personálnych požiadaviek na úlohu. Tieto personálne atribúty spolu s plánom úloh sa používajú na vyhľadanie dostupných zdrojov na vykonanie tejto úlohy.

   - **Role** : Zadajte typ zdroja, ktorý je potrebný na vykonanie úlohy.,
   - **Zdrojová jednotka**: zadajte jednotku, z ktorej by mali byť pridelené zdroje pre úlohu. Tento atribút ovplyvňuje odhady nákladov a predaja na úlohy, ak sú náklady a fakturačná sadzba zdroja nastavené na zdrojové jednotky.
   - **Názov pozície**: zadajte popisný názov pre všeobecný zdroj, ktorý slúži ako zástupný symbol pre zdroj, ktorý bude v konečnom dôsledku vykonávať prácu.

Pole **zdroje** obsahuje názov pozície všeobecného zdroja alebo pomenovaného zdroja, keď sa našiel.

Pole **Kategória** obsahuje hodnoty, ktoré označujú širší typ práce, do ktorej môže byť úloha zoskupená. Toto pole neovplyvňuje plánovanie ani personálne obsadenie. Namiesto toho sa pole používa iba na vykazovanie.

## <a name="task-dependencies"></a>Závislosti úloh

Môžete použiť plán v Project Operations na vytvorenie predchodcu vzťahov medzi úlohami. Pole **Predchodca** používa jednu alebo viacero hodnôt na označenie úloh, na ktorých je úloha závislá. Keď sú hodnoty predchodcu priradené k úlohe, úloha môže začať, iba ak sa dokončili všetky predchádzajúce úlohy. Z dôvodu závislosti, plánovaný počiatočný dátum úlohy sa obnoví na dátum po dokončení predchádzajúcich úloh.

Režim úlohy nemá žiadny vplyv na aktualizácie, ktoré sú vykonané na počiatočných a koncových dátumoch predchádzajúcich/závislých úloh.

## <a name="accessibility-and-keyboard-shortcuts"></a>Klávesové skratky a zjednodušenie ovládania

Mriežka **plánu** je plne prístupná a môže sa používať s čítačkami obrazovky, ako sú napríklad Narrator, JAWS alebo NVDA. Môžete prechádzať oblasti mriežky pomocou šípok (ako v Microsoft Excel), môžete použiť klávesu Tab na postúp cez interaktívne prvky používateľského rozhrania, a môžete použiť šípku nadol, klávesu Enter, alebo medzerník pre výber a otvorenie rozbaľovacích ponúk.

## <a name="project-limitations"></a>Projektové obmedzenia 
Ak používate štruktúru rozpisu práce v Project Operations, mali by ste si byť vedomí nasledujúcich obmedzení. Tieto limity platia pre projekty a úlohy. Ďalšie informácie nájdete v časti [Limity a hranice Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

| **Pole**                                          |  **Limit**           |
|----------------------------------------------------|----------------------|
| Maximálny celkový počet úloh pre projekt                  | 500                  |
| Maximálne celkové trvanie pre projekt               | 3650 dní (10 rokov) |
| Maximálny celkový počet zdrojov pre projekt              | 150                  |
| Maximálny celkový počet odkazov (len nasledovník) pre projekt | 600                  |
| Maximálny celkový počet vlastných polí pre projekt          | 10                   |
| Maximálny počet položiek kontrolného zoznamu na úlohu                   | 20                   |

**Obmedzenia úloh**

| **Pole**                               |   **Limit**           |
|-----------------------------------------|-----------------------|
| Maximálna úroveň hierarchie                 | 10 úrovní             |
| Maximálny počet odkazov (nástupca + predchodca) | 20                    |
| Maximálne trvanie listovej úlohy           | 1250 dní             |
| Maximálne trvanie súhrnnej úlohy      | 3650 dní (10 rokov)  |
| Maximálny počet zdrojov priradených k úlohe    | 20 zdrojov          |
| Podporovaný rozsah dátumov pre úlohu         | 1/1/2000 – 12/31/2149 |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
