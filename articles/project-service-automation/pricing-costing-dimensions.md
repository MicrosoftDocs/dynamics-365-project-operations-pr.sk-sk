---
title: Domovská stránka dimenzíí ceny a ocenenia
description: Táto téma poskytuje prehľad dimenzií cien.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755567"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Domovská stránka dimenzíí ceny a ocenenia

Dimenzie, ktoré sa používajú v ľudských zdrojoch na stanovenie cien a nákladov, spadajú do dvoch kategórií:

- Ľudia
- Plánovaná práca

Z tohto dôvodu existujú dva typy hodnôt dimenzie ceny k dispozícii v Project Service Automation (PSA): 

- **Množina možností** – dimenzie, ktoré sú pevnými enumeráciami pre množinu hodnôt.
- **Hodnoty založené na entite** - Dimenzie, ktoré môžu byť rôznorodá množina hodnôt.

## <a name="pricing-dimensions"></a>Cenové dimenzie

PSA lode s predvolenou sadou cenových dimenzií. Tieto môžete zobraziť tak, že prejdete **Project Service** > **parametre**. V zázname parametra, karta **cenové dimenzie založené na čiastke**, overuje, že role, **msdyn_resourcecategory** a zdrojová organizačná jednotka, **msdyn_organizationalunit** majú polia **Vzťahujúce sa na predaj** a **vzťahujúce sa na náklad** nastavené na **Áno**. To vám umožní nastaviť cenu a náklady pre každú rolu a organizačnú jednotku kombinácie.

![Screenshot z parametrov Project Service so zvýrazneným "použiteľné pre predaj"](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Ak ste boli používateľom polí role out-of-box a organizačnej jednotky ako cenové dimenzie pred verziou 3 PSA, nebudú žiadne pozorovateľné zmeny. Môžete naďalej používať Project Service ako zvyčajne. 

Ak potrebujete ceny alebo náklady na svoje zdroje pomocou ďalších atribútov, môžete vytvoriť prispôsobené polia, entity a dimenzie. Ďalšie informácie nájdete v nasledujúcich témach, avšak uvedomte si, že musíte vykonať postupy v uvedenom poradí:

- [Vytvorte vlastné polia a entity](create-custom-fields-entities.md)
- [Pridanie vlastných polí do cenového nastavenia a transakčných entít](field-references.md)
- [Nastavenie vlastných polí ako dimenzií cien](set-up-pricing-dimensions.md)
- [Aktualizácia atribútov doplnkov na zahrnutie nových dimenzií cien](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Ceny ľudských zdrojov času
Ako organizácia ceny ľudských zdrojov času je často dôležitým strategickým vzhľadom, že priamo ovplyvňuje ziskovosť organizácie. Práca s finančnými tímami a cvičením hláv, keď vaša organizácia je pripravená zistiť, ako chce nastaviť fakturáciu a ceny za ľudské zdroje času.

Ďalšie informácie o cenách zahŕňajú, či chcete opätovne použiť polia alebo entity, ktoré momentálne nie sú dimenziami cien, ale vzťahujú sa na dimenziu cien pre vašu organizáciu. Polia ako **transakčná kategória** (**msdyn_transactioncategory**) a **rezervovateľný zdroj** (**bookableresource**) sú príklady kandidátov dimenzie. 

Mali by ste tiež zvážiť, či by mal byť váš cenový rozmer tabuľka alebo množina možností. Ak predpokladáte zmeny hodnôt dimenzie, ktoré budú presahovať 10 alebo 12 a potrebujete ďalšie atribúty týchto hodnôt, môžete vytvoriť entitu, a nie množinu možností. Udržiavanie množiny možností, ako napríklad pridávanie alebo odstraňovanie hodnôt, vyžaduje správcu alebo vývojára, zatiaľ čo pridávanie nových riadkov do tabuľky môže vykonať väčšina používateľov.

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
