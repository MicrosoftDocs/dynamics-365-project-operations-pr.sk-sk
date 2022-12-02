---
title: Prehľad cenových dimenzií
description: Tento článok poskytuje informácie o cenových dimenziách v Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 294dcff8e9717aaa3a0459daf87cb7d608c96106
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918055"
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

![Snímka obrazovky z parametrov Project Service so zvýrazneným „Vzťahuje sa na predaj“.](media/PS-OOB-parameters.png)

Ak potrebujete ceny alebo náklady na svoje zdroje pomocou ďalších atribútov, môžete vytvoriť prispôsobené polia, entity a dimenzie. Ďalšie informácie nájdete v nasledujúcich článkoch. 
  
  > [!NOTE]
  > Postupy musia byť ukončené v poradí, v akom sú uvedené.

1. [Vytvorenie riešenia pre vlastné cenové dimenzie](../sales/create-solution-custompd.md)
2. [Vytvorenie vlastných polí a entít](create-custom-fields-entities-pricing-dimensions.md)
3. [Pridanie vlastných polí do entít nastavenia cien a transakcií ](add-custom-fields-price-setup-transactional-entities.md)
4. [Nastavenie vlastných polí ako cenových dimenzií ](set-up-custom-fields-pricing-dimensions.md)
5. [Aktualizácia atribútov doplnkov na zahrnutie nových dimenzií cien](update-plugin-attributes-pd.md)


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


[!INCLUDE[footer-include](../includes/footer-banner.md)]