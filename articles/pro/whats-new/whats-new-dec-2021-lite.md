---
title: Čo je nové December 2021 – Nasadenie Project Operations lite
description: Tento článok poskytuje informácie o aktualizáciách kvality dostupných vo vydaní nasadenia Project Operations lite v decembri 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914099"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Čo je nové December 2021 – Nasadenie Project Operations lite

_Platí pre: Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

### <a name="subcontract-management"></a>Správa subdodávateľských zmlúv 

- [Členovia projektového tímu v rámci subdodávateľskej zmluvy](../subcontracting/subcontracting-project-team-members.md): Projektový manažér môže vytvoriť menovaných alebo všeobecných členov tímu so subdodávateľskými zmluvami a riadkami subdodávateľskej zmluvy, aby ovplyvnil personálne obsadenie a odhady.
- [Možnosti subdodávateľskej zmluvy pre členov projektového tímu](../subcontracting/subcon-options.md) : Pri výbere zamestnancov pre menovaných alebo všeobecných členov projektového tímu môže projektový manažér skontrolovať existujúce subdodávateľské zmluvy alebo vytvoriť nové subdodávateľské zmluvy pre jedného alebo viacerých členov projektového tímu. 
- [Odhad nákladov v prípade priradení zdrojov v rámci subdodávateľskej zmluvy](../subcontracting/costing-subcon-ra.md) : Odhad nákladov na projekt bude brať do úvahy subdodávateľské priradenia zdrojov a bude ich naceňovať podľa nákupných cenníkov spojených so subdodávateľskými zmluvami. 
- [Konfigurácia tabule plánovania s cieľom zobraziť zmluvných pracovníkov a kapacitu na základe subdodávateľskej zmluvy](../subcontracting/configure-sb-subcon.md): Tabuľa plánovania v Project Operations môže byť teraz nakonfigurovaná tak, aby hľadala a navrhovala typ zmluvného pracovníka rezervovateľných zdrojov a subdodávateľskej kapacity spolu so zamestnancami. Túto konfiguráciu je možné použiť pri hľadaní zdrojov v kontexte personálneho obsadenia pre konkrétnu projektovú požiadavku alebo pri hľadaní mimo kontextu projektovej požiadavky.
- [Personálne zabezpečenie projektu zmluvnými pracovníkmi a kapacitou na základe subdodávateľskej zmluvy](../subcontracting/staffing-cw.md): Zmluvných pracovníkov je teraz možné rezervovať na projekty využívajúce prostredia s tabuľou plánovania.
- [Evidencia času, výdavkov a použitia materiálu pre súčasti v rámci subdodávateľskej zmluvy](../subcontracting/recording-subcon-actuals.md) : Zmluvní pracovníci môžu zaznamenávať čas a výdavky a členovia projektového tímu môžu tiež zaznamenávať využitie materiálov zakúpených prostredníctvom subdodávateľskej zmluvy na projekte. Výsledkom bude zaznamenávanie presných nákladov na projekty, ktoré využívajú zakúpenú kapacitu alebo materiály.
- [Prechody stavov v rámci subdodávateľskej zmluvy](../subcontracting/subcon-states.md): Subdodávateľské zmluvy môžu byť potvrdené na dokončenie rokovaní s predajcom, uzavreté na označenie dokončenia dodávky alebo zrušené na označenie ukončenia zmluvy s predajcom pred dokončením dodávky.

### <a name="task-planning"></a>Plánovanie úloh
- Zlepšené riešenie problémov pre správcov systému. Keď používateľ nemôže otvoriť projekt, správca môže skontrolovať chyby nesúvisiace s licenciou, ktoré sú generované z Project for the Web v [denníkoch plánovania projektu](../../project-management/schedule-api-logs.md).
- [Použite kontrolné zoznamy úloh v Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). V Microsoft Project for the Web môžete k úlohe pridať kontrolný zoznam, aby ste mali prehľad o konkrétnych položkách.

## <a name="quality-updates"></a>Aktualizácie kvality

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| Plánovanie a sledovanie | 2392596 | Rozhrania API plánovania teraz umožňujú aktualizácie polí **Zostávajúce úsilie**, **Dokončené úsilie** a **% dokončené**. |
| Plánovanie a sledovanie | 2478497 | Rozhrania API pre plánovanie **Číslo aktivity** a **ID úlohy** môžu byť pri vstupe prázdne, pretože systém ich vyplní pomocou automatizovaného číslovania.|
| Čas a výdavky | 2468135 | Počet opakovaných pokusov o schválenie sa zníži z piatich na tri. |
| Čas a výdavky | 2468188 | Opravený problém s textom denníka presahujúcim maximálnu dĺžku v atribúte **notetext** entity **anotácia**. |
