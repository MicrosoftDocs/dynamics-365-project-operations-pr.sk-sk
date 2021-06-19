---
title: Domovská stránka dimenzíí ceny a ocenenia
description: Táto téma poskytuje prehľad dimenzií cien.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9a2e2f7ed394229bbc553af9e616a6f322857195
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009275"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Domovská stránka dimenzíí ceny a ocenenia

[!include [banner](../includes/psa-now-project-operations.md)]

Dimenzie použité na stanovenie cien a nákladov práce v projektových organizáciách ovplyvňujú nasledujúce atribúty:

- Ľudia, ktorí vykonávajú prácu súvisiacu s ich skúsenosťami, rolou alebo geografickou polohou
- Práca, ktorá sa má vykonávať, súvisí s jej mierou zložitosti alebo dennou dobou

Vzhľadom na typický charakter týchto atribútov práce a ľudí potrebných na výkon práce sú v aplikácii Project Service Automation k dispozícii dva typy hodnôt cenových dimenzií: 

- **Množiny možností** – Atribúty, ktoré sú pevnými enumeráciami pre množinu hodnôt.
- **Hodnoty založené na entite** - Atribúty, ktoré môžu mať rôznorodú množinu hodnôt, ktoré sú konečné, ale môžu sa časom meniť.

## <a name="pricing-dimensions"></a>Cenové dimenzie

PSA lode s predvolenou sadou cenových dimenzií. Tieto môžete zobraziť tak, že prejdete **Project Service** > **parametre**. V zázname parametra, karta **cenové dimenzie založené na čiastke**, overuje, že role, **msdyn_resourcecategory** a zdrojová organizačná jednotka, **msdyn_organizationalunit** majú polia **Vzťahujúce sa na predaj** a **vzťahujúce sa na náklad** nastavené na **Áno**. To vám umožní nastaviť cenu a náklady pre každú rolu a organizačnú jednotku kombinácie.

![Screenshot z parametrov Project Service so zvýrazneným "použiteľné pre predaj"](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Ak ste boli používateľom polí role out-of-box a organizačnej jednotky ako cenové dimenzie pred verziou 3 PSA, nebudú žiadne pozorovateľné zmeny. Môžete naďalej používať Project Service ako zvyčajne. 

Ak potrebujete ceny alebo náklady na svoje zdroje pomocou ďalších atribútov, môžete vytvoriť prispôsobené polia, entity a dimenzie. Ďalšie informácie nájdete v nasledujúcich témach, avšak uvedomte si, že musíte vykonať postupy v uvedenom poradí:

- [Vytvorte vlastné polia a entity](create-custom-fields-entities.md)
- [Pridanie vlastných polí do cenového nastavenia a transakčných entít](field-references.md)
- [Nastavenie vlastných polí ako cenových dimenzií](set-up-pricing-dimensions.md)
- [Aktualizácia atribútov doplnkov na zahrnutie nových dimenzií cien](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Ceny ľudských zdrojov času
Ako organizácia ceny ľudských zdrojov času je často dôležitým strategickým vzhľadom, že priamo ovplyvňuje ziskovosť organizácie. Práca s finančnými tímami a cvičením hláv, keď vaša organizácia je pripravená zistiť, ako chce nastaviť fakturáciu a ceny za ľudské zdroje času.

Ďalšie informácie o cenách zahŕňajú, či chcete opätovne použiť polia alebo entity, ktoré momentálne nie sú dimenziami cien, ale vzťahujú sa na dimenziu cien pre vašu organizáciu. Polia ako **transakčná kategória** (**msdyn_transactioncategory**) a **rezervovateľný zdroj** (**bookableresource**) sú príklady kandidátov dimenzie. 

Zvážte, či by mala byť vaša cenová dimenzia tabuľkou alebo množinou možností. Ak predpokladáte zmeny hodnôt dimenzie, ktoré budú presahovať 10 alebo 12, a potrebujete ďalšie atribúty týchto hodnôt, vytvorte entitu, a nie množinu možností. Udržiavanie množiny možností, ako napríklad pridávanie alebo odstraňovanie hodnôt, vyžaduje správcu alebo vývojára, zatiaľ čo pridávanie nových riadkov do tabuľky môže vykonať väčšina obchodných používateľov.

Nasledujúci príklad zobrazuje fakturačné sadzby, ktoré sú nastavené na základe role a zdrojov organizačnej jednotky, ku ktorej zdroj patrí. Ceny sú zvyčajne založené na platovom pásme zamestnanca a organizačnej jednotky, ku ktorej patria. V tomto príklade budú tabuľky fakturačnej a nákladovej sadzby vyzerať takto.

**Vzorka fakturačných sadzieb**

| Rola        | Organizačná jednotka    |Jednotka      |Cena      |Mena  |
| ------------|-------------|----------|----------:|----------|
| Vývojár   | Contoso – USA  |Hodina | 200|USD     |
| Vývojár   | Contoso India |Hodina|   112|USD     |


**Vzorka nákladových sadzieb**

| Platové pásmo     | Organizačná jednotka    |Jednotka      |Cena      |Mena  |
| ----------------|-------------|----------|----------:|----------|
| Moje company_Band1 | Contoso – USA  |Hodina | 145|USD     |
| Moje company_Band2 | Contoso India |Hodina|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]