---
title: Prehľad cenových dimenzií
description: Táto téma poskytuje informácie o cenových dimenziách v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898235"
---
# <a name="pricing-dimensions-overview"></a>Prehľad cenových dimenzií

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dimenzie, ktoré sa používajú v ľudských zdrojoch na stanovenie cien a nákladov, spadajú do dvoch kategórií:

- Ľudia
- Plánovaná práca

Z tohto dôvodu existujú dva typy hodnôt cenovej dimenzie:

- **Množiny možností**: Dimenzie, ktoré sú pevnými enumeráciami pre množinu hodnôt.
- **Hodnoty založené na entite**: Dimenzie, ktoré môžu byť rôznorodými množinami hodnôt.

## <a name="pricing-dimensions"></a>Cenové dimenzie

Dynamics 365 Project Operations sa dodáva s predvolenou množinou cenových dimenzií. Tieto cenové dimenzie môžete zobraziť tak, že prejdete do **Project Operations** > **Parametre**. V zázname parametra, karta **cenové dimenzie založené na čiastke**, overuje, že role, **msdyn_resourcecategory** a zdrojová organizačná jednotka, **msdyn_organizationalunit** majú polia **Vzťahujúce sa na predaj** a **vzťahujúce sa na náklad** nastavené na **Áno**. Po povolení týchto polí môžete nastavovať cenu a náklady pre kombináciu každej roly a organizačnej jednotky.

Ak potrebujete ceny alebo náklady na svoje zdroje pomocou ďalších atribútov, môžete vytvoriť prispôsobené polia, entity a dimenzie.

## <a name="pricing-human-resource-time"></a>Ceny ľudských zdrojov času
Ako organizácia ceny ľudských zdrojov času je často dôležitým strategickým vzhľadom, že priamo ovplyvňuje ziskovosť organizácie. Práca s finančnými tímami a cvičením hláv, keď vaša organizácia je pripravená zistiť, ako chce nastaviť fakturáciu a ceny za ľudské zdroje času.

Ďalšie informácie o cenách zahŕňajú, či chcete opätovne použiť polia alebo entity, ktoré momentálne nie sú dimenziami cien, ale vzťahujú sa na dimenziu cien pre vašu organizáciu. Polia ako **transakčná kategória** (**msdyn_transactioncategory**) a **rezervovateľný zdroj** (**bookableresource**) sú príklady kandidátov dimenzie. 

Zvážte, či by mala byť vaša cenová dimenzia tabuľkou alebo množinou možností. Ak predpokladáte zmeny hodnôt dimenzie, ktoré budú presahovať 10 alebo 12 a potrebujete ďalšie atribúty týchto hodnôt, môžete vytvoriť entitu, a nie množinu možností. Udržiavanie množiny možností, ako napríklad pridávanie alebo odstraňovanie hodnôt, vyžaduje správcu alebo vývojára, zatiaľ čo pridávanie nových riadkov do tabuľky môže vykonať väčšina používateľov.

Nasledujúci príklad zobrazuje fakturačné sadzby, ktoré sú nastavené na základe role a zdrojov organizačnej jednotky, ku ktorej zdroj patrí. Ceny sú zvyčajne založené na platovom pásme zamestnanca a organizačnej jednotky, ku ktorej patria. V tomto príklade budú tabuľky fakturačnej a nákladovej sadzby vyzerať takto.

**Vzorka fakturačných sadzieb**

| Rola        | Org jednotka    |Jednotka      |Cena      |Mena  |
| ------------|-------------|----------|----------:|----------|
| Vývojár   | Contoso US  |Hour | 200|USD     |
| Vývojár   | Blaho India |Hour|   112|USD     |


**Vzorka nákladových sadzieb**

| Platové pásmo     | Org jednotka    |Jednotka      |Cena      |Mena  |
| ----------------|-------------|----------|----------:|----------|
| Moje company_Band1 | Contoso US  |Hour | 145|USD     |
| Moje company_Band2 | Blaho India |Hour|   67|USD     |
