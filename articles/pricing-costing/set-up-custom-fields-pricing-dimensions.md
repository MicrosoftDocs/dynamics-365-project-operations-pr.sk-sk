---
title: Nastavenie vlastných polí ako cenových dimenzií
description: Táto téma poskytuje informácie o tom, ako nastaviť cenové dimenzie pomocou vlastných polí.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d40a80f80bd766bfc19e831ea805a4043baf0030
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004730"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Nastavenie vlastných polí ako cenových dimenzií

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Pred začatím tejto témy sa predpokladá, že ste dokončili postupy v témach, [Vytvorenie vlastných polí a entít](create-custom-fields-entities-pricing-dimensions.md) a [Pridanie požadovaných vlastných polí do cenového nastavenia a transakčných entít](add-custom-fields-price-setup-transactional-entities.md). Ak ste tieto postupy nedokončili, vráťte sa späť a dokončite ich a potom sa vráťte na túto tému. 

Táto téma poskytuje informácie o nastavení vlastných dimenzií cien. Na stránke **Parametre**, sa na karte **Cenové dimenzie založené na čiastke** zobrazujú záznamy v entitách cenovej dimenzie. V predvolenom nastavení sú na tejto karte v mriežke dva riadky:

- **msdyn_resourcecategory** (Rola)
- **msdyn_OrganizationalUnit** (Organizačná jednotka)

> [!IMPORTANT]
> Tieto riadky neodstraňujte. Ak ich však nepotrebujete, môžete ich spraviť neplatnými v špecifickom kontexte nastavením možností **Vzťahuje sa na náklady**, **Vzťahuje sa na predaj** a **Vzťahuje sa na nákup** na možnosť **Nie**. Nastavenie týchto hodnôt atribútov na **Nie** má rovnaký účinok, ako nemať pole ako cenovú dimenziu.

Aby sa pole stalo cenovou dimenziou, musí byť:

- Vytvorená ako pole v entitách **Cena roly** a **Prirážky k cenám rol**. Pre ďalšie informácie o postupuje [Pridanie vlastných polí do cenového nastavenia a transakčných entít](add-custom-fields-price-setup-transactional-entities.md).

- Vytvorená ako riadok v tabuľke **Cenová dimenzia**. Pridajte napríklad riadky dimenzie ocenenia, ako je uvedené v nasledujúcom obrázku. 

![Riadky čiastkovo založenej dimenzie oceňovania](media/Amt-based-PD.png)

Pracovné hodiny zdroja (**msdyn_resourceworkhours**) sú pridané ako dimenzie založené na prirážke a boli pridané do mriežky na karte **Cenová dimenzia založená na prirážke**.

![Riadky dimenzie ceny na základe zrážky](media/Markup-based-PD.png)


> [!IMPORTANT]
> Akákoľvek zmena údajov cenovej dimenzie v tejto tabuľke, existujúcich alebo nových, je prenesená na obchodnú logiku určovania cien po obnovení vyrovnávacej pamäte. Čas obnovenia vyrovnávacej pamäte môže trvať až 10 minút. Nechajte potrebný čas na zobrazenie zmien v predvolenej logike ceny, ktorá musí byť výsledkom zmien v údajoch dimenzie ceny.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atribúty tabuľky dimenzie cien
Nasledujúce časti poskytujú informácie o rôznych atribútoch v tabuľke **Cenové dimenzie**.

### <a name="pricing-dimension-name"></a>Názov cenovej dimenzie
Táto hodnota by mala byť presne rovnaká ako názov schémy poľa, ktoré sa pridá do tabuľky **Cena roly** pre vlastné cenové dimenzie. Ďalšie informácie o pridávaní polí do tabuľky **Cena roly** nájdete v téme [Pridanie vlastných polí do cenového nastavenia a transakčných entít](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Typ dimenzie
Existujú dva typy cien dimenzií:
  
  - **Dimenzie založené na sume**: : hodnoty dimenzie z kontextu vstupu sa porovnajú s hodnotami dimenzie v riadku **Cena roly** a cena/náklady sa predvolene získavajú priamo z tabuľky **Cena roly**.
  - **Dimenzie založené na prirážke**: Ide o dimenzie, kde sa používa nasledujúci 3-stupňový proces na získanie ceny/nákladov:
 
    1. Hodnoty dimenzie nezaložené na prirážke z kontextu vstupu sa spárujú s riadkom Cena roly, aby sa získala základná sadzba.
    2. Hodnoty dimenzie z kontextu vstupu sa spárujú s riadkom **Prirážka k cene roly**, aby sa získala percentuálna hodnota prirážky.
    3. Percentuálna hodnota prirážky z druhého kroku sa aplikuje na základnú sadzbu získanú z tabuľky **Cena roly** v prvom kroku, aby sa dospelo ku konečnej cene/nákladom.
   
   Nasledujúca tabuľka znázorňuje výpočet cenových označení.
  
| Rola        | Organizačná jednotka    |Miesto výkonu práce      |Štandardný názov      |Pracovná doba zdroja      |  Označenie|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|U zákazníka            |                    |Nadčas                 |15     |
|             | Contoso India|Lokálny             |                    |Nadčas                 |10     |
|             | Contoso – USA   |Lokálny             |                    |Nadčas                 |20     |


Ak zdroj z Contoso India, ktorého základná sadzba je 100 USD, pracuje u zákazníka a vykáže 8 hodín bežnej pracovnej doby a 2 hodiny nadčasov v zadaní času, systém ceny využije základnú sadzbu 100 pre nasledujúcich 8 hodín, čím sa dosiahne 800 USD. Pre 2 hodiny nadčas, bude prirážka 15 % použitá na základnú sadzbu 100 na získanie jednotkovej ceny 115 USD a zaznamená celkové náklady na 230 USD.

### <a name="applicable-to-cost"></a>Vzťahuje sa na náklady 
Ak je nastavená na hodnotu **Áno**, znamená to, že hodnota dimenzie z kontextu vstupu by sa mala použiť na zhodu s poľami **Cena roly** a **Prirážka k cene roly** pri načítavaní sadzieb nákladov a prirážky.

### <a name="applicable-to-sales"></a>Vzťahuje sa na predaj
Ak je nastavená na hodnotu **Áno**, znamená to, že hodnota dimenzie z kontextu vstupu by sa mala použiť na zhodu s poľami **Cena roly** a **Prirážka k cene roly** pri načítavaní sadzieb fakturácie a prirážky.

### <a name="applicable-to-purchase"></a>Vzťahuje sa na nákup
Ak je nastavená na hodnotu **Áno**, znamená to, že hodnota dimenzie z kontextu vstupu by sa mala použiť na zhodu s poľami **Cena roly** a **Prirážka k cene roly** pri načítavaní sadzieb nákupnej ceny. Scenáre subdodávok nie sú podporované, takže toto pole sa nepoužíva. 

### <a name="priority"></a>Priorita
Nastavenie priority dimenzie pomáha pri stanovení ceny, aj keď nedokáže nájsť presnú zhodu medzi hodnotami vstupnej dimenzie a hodnotami z tabuliek **Cena roly** alebo **Prirážka k cene roly**. V tomto scenári, sa budú používať nulové hodnoty pre nepriradené hodnoty dimenzie vážením dimenzií v poradí ich priority.

- **Priorita nákladov**: Hodnota dimenzie nákladov na dimenziu bude znamenať hmotnosť tohto rozmeru pri párovaní s nastavením cien nákladov. Hodnota **Priorita nákladov** musí byť jedinečná naprieč dimenziami, ktoré sa **vzťahujú na náklady**.
- **Priorita predaja**: Hodnota dimenzie predaja na dimenziu bude znamenať hmotnosť tohto rozmeru pri párovaní s nastavením cien predajov alebo sadzieb fakturácie. Hodnota **Priorita predaja** musí byť jedinečná naprieč dimenziami, ktoré sa **Vzťahuje sa na predaj**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]