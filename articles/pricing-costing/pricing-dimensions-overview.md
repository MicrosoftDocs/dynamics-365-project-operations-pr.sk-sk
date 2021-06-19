---
title: Prehľad cenových dimenzií
description: Táto téma poskytuje informácie o cenových dimenziách v Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01ba11e34e7d8a59716fa9d8c8be3389ab380048
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005000"
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

![Screenshot z parametrov Project Service so zvýrazneným "použiteľné pre predaj"](media/PS-OOB-parameters.png)

Ak potrebujete ceny alebo náklady na svoje zdroje pomocou ďalších atribútov, môžete vytvoriť prispôsobené polia, entity a dimenzie. Ďalšie informácie nájdete v nasledujúcej téme. 
  
  > [!NOTE]
  > Postupy musia byť ukončené v poradí, v akom sú uvedené.

1. [Vytvorenie riešenia pre vlastné cenové dimenzie](../sales/create-solution-custompd.md)
2. [Vytvorenie vlastných polí a entít](create-custom-fields-entities-pricing-dimensions.md)
3. [Pridanie vlastných polí do entít nastavenia cien a transakcií](add-custom-fields-price-setup-transactional-entities.md)
4. [Nastavenie vlastných polí ako cenových dimenzií](set-up-custom-fields-pricing-dimensions.md)
5. [Aktualizácia atribútov doplnkov na zahrnutie nových dimenzií cien](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Ceny ľudských zdrojov času
Ako organizácia ceny ľudských zdrojov času je často dôležitým strategickým vzhľadom, že priamo ovplyvňuje ziskovosť organizácie. Práca s finančnými tímami a cvičením hláv, keď vaša organizácia je pripravená zistiť, ako chce nastaviť fakturáciu a ceny za ľudské zdroje času.

Ďalšie informácie o cenách zahŕňajú, či chcete opätovne použiť polia alebo entity, ktoré momentálne nie sú dimenziami cien, ale vzťahujú sa na dimenziu cien pre vašu organizáciu. Polia ako **transakčná kategória** (**msdyn_transactioncategory**) a **rezervovateľný zdroj** (**bookableresource**) sú príklady kandidátov dimenzie. 

Zvážte, či by mala byť vaša cenová dimenzia tabuľkou alebo množinou možností. Ak predpokladáte zmeny hodnôt dimenzie, ktoré budú presahovať 10 alebo 12 a potrebujete ďalšie atribúty týchto hodnôt, môžete vytvoriť entitu, a nie množinu možností. Udržiavanie množiny možností, ako napríklad pridávanie alebo odstraňovanie hodnôt, vyžaduje správcu alebo vývojára, zatiaľ čo pridávanie nových riadkov do tabuľky môže vykonať väčšina používateľov.

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