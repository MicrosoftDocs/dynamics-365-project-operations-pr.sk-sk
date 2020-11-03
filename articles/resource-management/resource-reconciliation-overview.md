---
title: Prehľad odsúhlasenia zdrojov
description: Táto téma poskytuje informácie o tom, ako zaistiť, že rezervácie zdrojov a priradenia k projektom sú v súlade.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e2b16a6e1c48769ed4d903e546804ba1c4e1c4fa
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084306"
---
# <a name="resource-reconciliation-overview"></a>Prehľad odsúhlasenia zdrojov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Pre členov tímu sú rezervácie a priradenia voľne spojené. Inými slovami, zdroje môžu mať úlohy, ale žiadne rezervácie, alebo môžu mať rezerváciu, ale žiadne úlohy. V ideálnom prípade by mali byť rezervácie a úlohy zarovnané tak, aby zdroje zaplnili kapacity na plnenie úloh. Rezervácie však môžu byť založené na dostupnosti a časovanie úloh sa môže zmeniť, keď projekt pokračuje. Preto voľné spojenie rezervácií a úloh poskytuje flexibilitu.

Karta **Zosúladenie** vo formulári **Projekt** umožňuje projektovým manažérom zosúladiť rezervácie členov tímu a ich úlohy pre projektové tímy.

Na karte **Zosúladenie** sa zobrazujú aj rezervácie a priradenia na úrovni jednotlivých priradení úloh pre každého člena tímu. Hodiny sa zobrazujú v bunkách, ktoré môžu reprezentovať časové periódy od mesiacov po dni.

Na karte sa tiež zobrazuje celková čistá suma projektu spolu so stĺpcom **Celkovo**.

Pre každý zdroj karta vypočíta rozdiel medzi rezerváciami člena tímu a súhrnom priradení úloh člena tímu. V ideálnom prípade by tento rozdiel mal byť 0 (nula). Inými slovami, nemal by existovať žiadny rozdiel medzi rezerváciou a úlohami. Rozdiely sú farebné a zatienené aby upozornili na dve podmienky:

- **Nedostatok rezervácií** – Nedostatky rezervácií sa objavia, keď má zdroj viac priradení než rezervácie. Keďže táto kapacita nebola vyhradená, projektový manažér by túto podmienku mal chcieť napraviť rozšírením rezervácií prostriedkov na krytie deficitu.
- **Rozšírené rezervácie** – Nadmerná rezervácia nastane, keď sa zdroj zarezervuje do projektu, no nebude priradený k úlohám. Táto podmienka môže byť prijateľná v prípadoch, keď bol zdroj rezervovaný do projektu pred priradením úlohy. V ostatných prípadoch však zdroj nie je naplánovaný na priraďenie k úlohe. V takýchto prípadoch by mal projektový manažér zvážiť zrušenie rezervácií prostriedku tak, aby sa kapacita mohla použiť pre iný projekt.

V niektorých prípadoch, keď zobrazíte čas na vyššej úrovni ako na úrovni dňa (napríklad na úrovni mesiaca), môže sa zobraziť čistý rozdiel nula pre zdroj (inými slovami, rezervácie = úlohy). Avšak, ak si prezriete čas na úrovni týždňa, môžete vidieť, že existujú úlohy nula hodín a rezervácie 40 hodín v prvom týždni, ale úlohy 40 hodín a rezervácie nula hodín v druhom týždni. Celkovo sú rezervácie a úlohy zmierené, ale líšia sa od jedného týždňa do nasledujúceho.

Keď zobrazíte čas na vyšších úrovniach, bunky na karte **odsúhlasenie** majú indikátor, ktorý vám oznámi, že existujú rozdiely na nižších úrovniach. Dvojitým kliknutím na bunku môžete zväčšiť zobrazenie rozdielu. Potom môžete kliknutím pravým tlačidlom myši na vzdialiť. Výberom prostriedku a následným použitím ovládacieho prvku **ďalší rozdiel** na paneli s nástrojmi mriežky môžete prejsť na ďalší rozdiel medzi rezerváciami a priradeniami pre daný zdroj. Potom môžete použiť na vrátenie kontrolu **predchádzajúci rozdiel**. V časti **nastavenia** môžete tiež vypnúť ukazovateľ rozdielu a správanie navigácie.


Ak máte priradenia úloh pre zdroj, ale žiadne rezervácie, na stránke **projekty** na karte **odsúhlasenie** vyberte nedostatok rezervácie a potom vyberte položku **rozšíriť rezerváciu.** Zobrazí sa dialógové okno **rozšíriť rezerváciu** a zobrazí sa rezervácia, ktorá je potrebná na vyriešenie nedostatku zdroja. Zobrazuje aj existujúce rezervácie zdrojov vo všetkých projektoch alebo iných plánovateľných entitách. Ak vyberiete **OK** , ak chcete vytvoriť rezerváciu zdroja bez ohľadu na dostupnosť tohto prostriedku, môžete spôsobiť prekročenie rezervácie.

Projektový manažér alebo správca zdrojov potom môže pomocou tabule plánovania spravovať všetky situácie, v ktorých je zdroj prerezervovaný nad rámec jeho kapacity.

