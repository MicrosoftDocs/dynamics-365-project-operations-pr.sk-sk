---
title: Prehľad odsúhlasenia zdrojov
description: Táto téma poskytuje informácie, ktoré vám pomôžu zaistiť zosúladenie rezervácií a priradení zdrojov k projektom.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: be171063c21318f517a37f3088e3f577fd4b6715
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000860"
---
# <a name="resource-reconciliation-overview"></a>Prehľad odsúhlasenia zdrojov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Pre členov tímu sú rezervácie a priradenia voľne spojené. Inými slovami, zdroje môžu mať úlohy a žiadne rezervácie, alebo môžu mať rezerváciu a žiadne úlohy. V ideálnom prípade by mali byť rezervácie a úlohy zarovnané tak, aby zdroje zaplnili kapacity na plnenie úloh. Rezervácie však môžu byť založené na dostupnosti a časovanie úloh sa môže zmeniť, keď projekt pokračuje. Preto voľné spojenie rezervácií a úloh poskytuje flexibilitu.

Karta **Odsúhlasenie** na stránke **Projekty** umožňuje projektovým manažérom zosúladiť rezervácie členov tímu a ich úlohy pre projektové tímy.

Na karte **odsúhlasenie** sa zobrazujú rezervácie a priradenia na úrovni jednotlivých priradení úloh pre každého člena tímu. V bunkách sa zobrazujú hodiny, ktoré môžu reprezentovať časové periódy od mesiacov ku dňom. Na karte sa tiež zobrazuje celková čistá suma projektu spolu so stĺpcom **Celkovo**.

Pre každý zdroj karta **Vyrovnanie** vypočíta rozdiel medzi rezerváciami člena tímu a súhrnom priradení úloh člena tímu. V ideálnom prípade by tento rozdiel mal byť 0 (nula). Inými slovami, nemal by existovať žiadny rozdiel medzi rezerváciou a úlohami. Rozdiely sú farebné a zatienené aby upozornili na dve podmienky:

- **Nedostatok rezervácií** – Nedostatky rezervácií sa objavia, keď má zdroj viac priradení než rezervácie. Keďže kapacita nebola vyhradená, projektový manažér by túto podmienku mal chcieť napraviť rozšírením rezervácií prostriedkov na krytie deficitu.
- **Rozšírené rezervácie** – Nadmerná rezervácia nastane, keď sa zdroj zarezervuje do projektu, no nebude priradený k úlohám. Táto podmienka môže byť prijateľná v prípadoch, keď bol zdroj rezervovaný do projektu pred priradením úlohy. V iných prípadoch, ak neexistuje plán priradenia zdroja k úlohám, by však projektový manažér mal zvážiť zrušenie rezervácií zdroja. Týmto spôsobom je možné kapacitu využiť na iný projekt.

V niektorých prípadoch, keď zobrazíte čas na vyššej úrovni ako na úrovni dňa (napríklad na úrovni mesiaca), môže sa zobraziť čistý rozdiel nula pre zdroj (inými slovami, rezervácie sa rovnajú úlohám). Avšak, ak si prezriete čas na úrovni týždňa, môžete vidieť, že existujú úlohy nula hodín a rezervácie 40 hodín v prvom týždni, ale úlohy 40 hodín a rezervácie nula hodín v druhom týždni. Celkovo sú rezervácie a úlohy zmierené, ale líšia sa od jedného týždňa do nasledujúceho.

Keď zobrazíte čas na vyšších úrovniach, bunky na karte **Odsúhlasenie** majú indikátor, ktorý vám oznámi, že existujú rozdiely na nižších úrovniach. Dvojitým klepnutím na bunku môžete zväčšiť zobrazenie rozdielu. Potom môžete vybrať a podržať (alebo kliknúť pravým tlačidlom myši) na vzdialenie. Výberom prostriedku a následným použitím ovládacieho prvku **Ďalší rozdiel** na paneli s nástrojmi mriežky môžete prejsť na ďalší rozdiel medzi rezerváciami a priradeniami pre daný zdroj. Potom môžete použiť na vrátenie kontrolu **predchádzajúci rozdiel**. V časti **nastavenia** môžete tiež vypnúť ukazovateľ rozdielu a správanie navigácie.

Ak máte priradenia úloh pre zdroj, ale žiadne rezervácie, na karte **Odsúhlasenie** na stránke **Projekty** vyberte nedostatok rezervácie a potom vyberte položku **Rozšíriť rezerváciu.** Dialógové okno **Rozšíriť rezerváciu** zobrazuje rezerváciu, ktorá je potrebná na vyriešenie nedostatku zdroja. Dialógové okno zobrazuje aj existujúce rezervácie zdrojov vo všetkých projektoch alebo iných plánovateľných entitách. Ak vyberiete **OK**, ak chcete vytvoriť rezerváciu zdroja bez ohľadu na dostupnosť tohto prostriedku, môžete spôsobiť prekročenie rezervácie.

Rezervácie, ktoré sa vytvárajú prostredníctvom servera **Rozšíriť rezerváciu**, sú spojené s požiadavkou primárneho projektu. Pri iniciovaní rozšírenia nie je možné určiť konkrétnu požiadavku, ktorú je potrebné predĺžiť, pretože zdroj môže byť spojený s viac ako jednou požiadavkou pre projekt.

Projektový manažér alebo správca zdrojov potom môže pomocou tabule plánovania spravovať všetky situácie, v ktorých je zdroj prerezervovaný nad rámec jeho kapacity.


[!INCLUDE[footer-include](../includes/footer-banner.md)]