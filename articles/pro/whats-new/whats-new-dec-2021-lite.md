---
title: Čo je nové december 2021 – zjednodušené nasadenie Project Operations
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú dostupné vo vydaní zjednodušeného nasadenia Project Operations z decembra 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942996"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Čo je nové december 2021 – zjednodušené nasadenie Project Operations

_Platí pre: Čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma sa týka nasledujúcich komponentov a verzií Microsoftu Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

### <a name="subcontract-management"></a>Manažment subdodávok 

- [Subdodávky členov projektového tímu](../subcontracting/subcontracting-project-team-members.md) : Projektový manažér môže vytvoriť pomenovaných alebo všeobecných členov tímu so subdodávateľskými a subdodávateľskými líniami, aby ovplyvnil personálne obsadenie a odhad.
- [Možnosti subdodávok pre členov projektového tímu](../subcontracting/subcon-options.md) : Pri výbere zamestnancov pre menovaných alebo všeobecných členov projektového tímu môže projektový manažér skontrolovať existujúce subdodávky alebo vytvoriť nové subdodávky pre jedného alebo viacerých členov projektového tímu. 
- [Odhad nákladov na subdodávateľské priradenia zdrojov](../subcontracting/costing-subcon-ra.md) : Odhad nákladov na projekt bude brať do úvahy subdodávateľské priradenia zdrojov a bude ich stáť podľa nákupných cenníkov spojených so subdodávateľskými zmluvami. 
- [Nakonfigurujte tabuľu plánovania tak, aby zobrazovala zmluvných pracovníkov a subdodávateľskú kapacitu](../subcontracting/configure-sb-subcon.md) : Tabuľa plánovania v Project Operations môže byť teraz nakonfigurovaná tak, aby hľadala a navrhovala typ rezervovateľných zdrojov zmluvného pracovníka a subdodávateľskú kapacitu spolu so zamestnancami. Túto konfiguráciu je možné použiť pri hľadaní zdrojov v kontexte personálneho obsadenia pre konkrétnu projektovú požiadavku alebo pri hľadaní mimo kontextu projektovej požiadavky.
- [Personálne zabezpečenie projektu zmluvnými pracovníkmi a subdodávateľskou kapacitou](../subcontracting/staffing-cw.md) : Zmluvných pracovníkov je teraz možné rezervovať na projekty využívajúce skúsenosti s tabuľou plánovania.
- [Evidencia času, nákladov a spotreby materiálu na projektoch pre subdodávateľské komponenty](../subcontracting/recording-subcon-actuals.md) : Zmluvní pracovníci môžu zaznamenávať čas a výdavky a členovia projektového tímu môžu tiež zaznamenávať využitie materiálov zakúpených pomocou subdodávky na projekte. Výsledkom bude presné zaznamenávanie nákladov na projekty, ktoré využívajú zakúpenú kapacitu alebo materiály.
- [Prechody štátov na subdodávku](../subcontracting/subcon-states.md) : Subdodávky môžu byť potvrdené na dokončenie rokovaní s predajcom, uzavreté na označenie dokončenia dodávky alebo zrušené na označenie ukončenia zmluvy s predajcom pred dokončením dodávky.

### <a name="task-planning"></a>Plánovanie úloh
- Vylepšené riešenie problémov pre správcov systému. Keď používateľ nemôže otvoriť projekt, správca môže skontrolovať chyby, ktoré nesúvisia s licenciou a ktoré sa vygenerujú z Projectu pre web [Protokoly plánovania projektu](../../project-management/schedule-api-logs.md).
- [Použite kontrolné zoznamy úloh v Microsoft Project pre web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). V Microsoft Project pre web môžete k úlohe pridať kontrolný zoznam, aby ste mali prehľad o konkrétnych položkách.

## <a name="quality-updates"></a>Aktualizácie kvality

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| Plánovanie a sledovanie | 2392596 | Rozhrania API plánovania teraz umožňujú aktualizácie **Zostávajúce úsilie**, **dokončené** a **% dokončené** poliach. |
| Plánovanie a sledovanie | 2478497 | Rozhrania API plánovania **Číslo aktivity** a **ID úlohy** polia môžu byť pri vstupe prázdne, pretože systém ich vyplní pomocou automatického číslovania.|
| Čas a výdavky | 2468135 | Počet opakovaných pokusov o schválenie sa zníži z piatich na tri. |
| Čas a výdavky | 2468188 | Opravený problém s textom denníka presahujúcim maximálnu dĺžku v **text poznámky** atribútom **anotácia** subjekt. |
