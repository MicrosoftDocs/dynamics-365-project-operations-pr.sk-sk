---
title: Správa časových pásiem
description: Po vytvorení projektu je jeho časové pásmo založené na časovom pásme definovanom v použitej šablóne pracovnej doby.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c3feb05e1b2e81add1b0df886a5a69ced229eb72
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578543"
---
# <a name="manage-time-zones"></a>Správa časových pásiem

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_


## <a name="projects"></a>Projekty

Po vytvorení projektu je časové pásmo založené na časovom pásme definovanom v použitej šablóne pracovnej doby. Vo formulári **Projekt** sú dátumy vždy relatívne k časovému pásmu používateľa, ktorý je prihlásený na každej karte, s výnimkou karty **Úloha**. Pri zobrazení štruktúry rozdelenia práce sa dátumy vždy zobrazia v časovom pásme projektu.

## <a name="tasks"></a>Úlohy

Po vytvorení úlohy sa začiatočný čas, konečný čas a hodiny/deň riadia pracovnými hodinami projektu. Napríklad, ak je úloha vytvorená s projektom, ktorého časové pásmo je -8 PST a má nasledujúcu pracovnú dobu: pondelok až piatok od 9:00 do 17:00, každá úloha vytvorená bez priradenia bude rešpektovať čas začiatku a konečný čas kalendára projektu.

## <a name="manage-resources-with-time-zones"></a>Správa zdrojov s časovými pásmami

Pre presné a predvídateľné výsledky pri používaní možnosti **Predĺžiť rezerváciu** musia byť splnené dva kľúčové predpoklady:  

- Používateľ musí nakonfigurovať časové pásmo svojho zariadenia tak, aby zodpovedalo časovému pásmu definovanému v časti **Nastavenia prispôsobení** v systéme.
 
  ![Nastavenia časového pásma v systéme Windows 10.](media/reconcile-assignments-03.png)

  ![Nastavenia časového pásma v nastaveniach prispôsobenia.](media/reconcile-assignments-04.png)
 
- Rezervovateľný zdroj musí mať najmenej jednu minútu pracovného času, ktorá sa prekrýva s obrysmi, ktoré sa používajú na definovanie požadovaného rozšírenia. Napríklad, nasledujúce zdroje s pracovnou dobou, ktorá spadá od 9:00 do 19:00. 

  ![Porovnanie obrysov zdrojov.](media/reconcile-assignments-05.png)

Nasledujúca tabuľka zobrazuje:

- Šablóna kalendára projektu
- Zdroj A: Tento zdroj má rovnaký kalendár a je v rovnakom časovom pásme ako projekt. Čas začiatku rezervácie bude 9.00.
- Zdroj B: Tento zdroj sa nachádza v inom časovom pásme ako projekt a začína sa o 7:00 v danom časovom pásme. Rezervácie sa však začnú o 9.00, pretože ide o najskorší čas začiatku obrysu priradenia.
- Zdroje C a D: Zdroje sa nachádzajú v rôznych časových pásmach, ktoré sa navzájom líšia a líšia sa od projektu, a ich rezervácie sa začínajú najskôr v príslušných dostupných začiatočných časoch.

|Entity  |Kalendár  |
|-|-|
|Šablóna kalendára projektu   | ![kalendár projektu.](media/reconcile-assignments-06.png) |
|Zdroj A  | ![Kalendár zdroja A.](media/reconcile-assignments-06.png) |
|Zdroj B  |  ![Kalendár zdroja B.](media/reconcile-assignments-07.png) |
|Zdroj C  |  ![Kalendár zdroja C.](media/reconcile-assignments-08.png) |
|Zdroj D  | ![Kalendár zdroja D.](media/reconcile-assignments-09.png)  |
 
Keď prejdete na zobrazenie **Vyrovnanie** zobrazia sa priradenia zdrojov a súvisiace nedostatky rezervácií.

![Zobrazenie odsúhlasenia pred predĺžením.](media/reconcile-assignments-10.png)

Po použití funkcie rozšíreného rezervovania pre každý zdroj sa rezervácie úspešne rozšíria na každý zdroj, pretože pracovná doba každého zdroja sa prekrýva s obrysmi nedostatku.

![Zobrazenie odsúhlasenia po rozšírení rezervácie.](media/reconcile-assignments-11.png) 

Upozorňujeme, že bližší pohľad na podrobnosti rezervácií ukazuje rozdiely v začiatočnom čase rezervácií. Rezervácie sa začnú najskôr ako začiatočný čas obrysu priradenia a najskôr ako dostupný začiatočný čas zdroja.

![Nové rezervácie zdrojov na tabuli plánovania.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]