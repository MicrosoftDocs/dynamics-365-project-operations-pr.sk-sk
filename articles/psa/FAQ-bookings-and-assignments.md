---
title: Rezervácie zdrojov a ako súvisia s priradením úloh
description: Táto téma poskytuje informácie o tom, ako spravovať pomenované zdroje, rezervácie zdrojov a priradenia úloh a ako navzájom súvisia.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 94deab811a304026dd663a88e869013a3b88fb29674b35fa0b40fa68f8c5ea62
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003114"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Rezervácie zdrojov a ako súvisia s priradením úloh

[!include [banner](../includes/psa-now-project-operations.md)]

Sú dve možnosti ako možno pomenované zdroje zarezervovať k projektovému tímu a priradeným projektovým úlohám:

- Zdroj možno priamo zarezervovať k projektu a následne ho priradiť k úlohám projektu.
- Úlohy možno priradiť ku všeobecným alebo zástupným zdrojom, ktoré sa následne použijú na vyhľadanie a nahradenie všeobecného za skutočný a pomenovaný zdroj. 

V obidvoch prípadoch sa v rámci rezervácie zdrojov zarezervujú kapacity zdroja.

Projektový manažér plánujúci projekt vlastní projektový plán a rozvrh. Použitím všeobecného zdroja pre priradenie a následným vytvorením žiadosti o zdroj môže projektový manažér zarezervovať zdroj do projektu s prvkami, ktoré sú uvedené v projektovom pláne. Môžu zarezervovať zdroje k projektu a následne ich priradiť k úlohe, no neexistuje spôsob, ako priradiť prvky rezervácie k prvkom úloh. Rezervácie nemajú vplyv na plán projektu.

Zohľadnite komplexný projekt s viacerými prekrývajúcimi sa úlohami v prípade, že je potrebné súčasne pracovať na viacerých zdrojoch rovnakého typu. Ak je zdroju pridelený prvok, ktorý sa líši od súčtu ich priradení, je zložité upraviť úlohy tak, aby vyhovovali prvku rezervácií pre ich jednotlivé úlohy a pôvodné prvky.

V nasledujúcom príklade je celková snaha vyžadovaná rovnakým zdrojom zo sady štyroch úloh 62 hodín počas dvojtýždňového obdobia a existuje konkrétny prvok. Ak dôjde k rezervácii zdroja Bob na 62 hodín počas rovnakých dvoch týždňov no s rôznymi prvkami, požiadavka a rezervácie sa prispôsobia.

| **Kontúry úlohy**    | **Celkový počet hodín** | Mo 6/4 | Tu 6/5 | We 6/6 | Th 6/7 | Fr 6/8 | Sa 6/9 | Su 6/10 | Mo 6/11 | Tu 6/12 | We 6/13 | Th 6/14 | Fr 6/15 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Úloha 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Úloha 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Úloha 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Úloha 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Súčty**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Dostupnosť Boba
| **Rezervácia zdroja** | **Celkový počet hodín** | Mo 6/4 | Tu 6/5 | We 6/6 | Th 6/7 | Fr 6/8 | Sa 6/9 | Su 6/10 | Mo 6/11 | Tu 6/12 | We 6/13 | Th 6/14 | Fr 6/15 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Však neexistuje systematický spôsob, ako priradiť prvok zarezervovaných hodín k úlohám na dennej báze. Ak projektový manažér je ochotný zmeniť plán projektu na splnenie dostupnosti zdroja, bude musieť odstrániť priradenie a zabezpečiť, aby všetky úlohy vyhovovali prvkom rezervácie.

V prípade, že organizácia udelila úlohu plánovania projektu manažérovi projektu aj manažérovi zdrojov, manažér projektu nastaví plán, ktorý bude zahŕňať aj prvky požadovanej práce. Správca zdrojov by nemal mať možnosť ovplyvniť plán bez vedomosti projektového manažéra zmenou prvkov úsilie počas rezervácie skutočných zdrojov. Ak je niečo odlišné od čo projektový manažér požiadal Správca prostriedkov, musia dospieť k dohode o tom, aké zmeny sú potrebné v pláne projektu.

Pretože rezervácie a priradenia nie sú úzko prepojené, existuje možnosť zarezervovať prvky tak, aby boli rôzne od prvkov úlohy alebo zmeniť priradenia tak, aby výsledkom toho boli okolnosti, kde budú rezervácie a priradenia nezosúladené.

**Zobrazenie odsúhlasenia**, umožňuje projektovému manažérovi vidieť rezervácie a priradenia pre každého člena projektového tímu. Zobrazenie využíva farby a odtiene na zobrazenie toho, keď sa objaví nesúlad medzi rezerváciami a pridelením člena tímu. Na základe tejto informácie, projektový manažér môže trvať nápravné opatrenia buď rozšíriť zdroj rezervácie pre prípady, ak nie sú úlohy a rezervácie alebo zrušiť rezerváciu, kde zdroje sú rezervované, ale mať žiadne úlohy.

> [!NOTE]
> Ak presuniete úlohu, ktorú ste tvarovali sami, nie sú zachované tieto kontúry. Obrysy sú regenerované podľa kalendár projektu, aby sa zohľadnili zmeny v pracovných hodín a sviatky. Ide o zámerný prvok, pretože systém nepozná úmysel pôvodného tvaru a nedokáže rozhodnúť, či má zmysel zachovávať daný prvok v novom časovom období. Pretože rezervácie a úlohy sú odpojené, rezervácie si udržiavajú pôvodné prvky rezervácie. V tomto prípade budete musieť pristúpiť k zrušeniu a opätovnej rezervácie na nový prvok priradenia.



[!INCLUDE[footer-include](../includes/footer-banner.md)]