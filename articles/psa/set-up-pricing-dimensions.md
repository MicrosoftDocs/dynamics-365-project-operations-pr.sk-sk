---
title: Nastavenie vlastných polí ako cenových dimenzií
description: Táto téma poskytuje informácie o nastavení vlastných dimenzií cien.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
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
ms.openlocfilehash: 9503b6528f91f86cc1ebe1c7ed6111171e74c4a3cbf83b3f68810c3ee5efdd28
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002350"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Nastavenie vlastných polí ako cenových dimenzií 

[!include [banner](../includes/psa-now-project-operations.md)]

Pred začatím tejto témy sa predpokladá, že ste dokončili postupy v témach, [Vytvorte vlastné polia a entity](create-custom-fields-entities.md) a [Pridanie vlastných polí do cenového nastavenia a transakčných entít](field-references.md). Ak ste tieto postupy nedokončili, vráťte sa späť a dokončite ich a potom sa vráťte na túto tému. 

Táto téma poskytuje informácie o nastavení vlastných dimenzií cien. Vo webovom rozhraní Project Service na stránke **Parametre** karta **Cenové dimenzie založené na čiastke** zobrazí záznamy v entitách dimenzií cien. V predvolenom nastavení Project Service inštalácia vytvorí 2 riadky v mriežke na tejto karte:

- **msdyn_resourcecategory** (Rola)
- **msdyn_OrganizationalUnit** (Organizačná jednotka)

> [!IMPORTANT]
> Tieto riadky neodstraňujte. Ak ich však nepotrebujete, môžete ich spraviť neplatnými v špecifickom kontexte nastavením možností **Vzťahuje sa na náklady**, **Vzťahuje sa na predaj** a **Vzťahuje sa na nákup** na možnosť **Nie**. Nastavenie týchto hodnôt atribútov na **Nie** má rovnaký účinok, ako nemať pole ako cenovú dimenziu.

Aby sa pole stalo cenovou dimenziou, musí byť:

- Vytvorená ako pole v entitách **Cena roly** a **Prirážky k cenám rol**. Pre ďalšie informácie o postupuje [Pridanie vlastných polí do cenového nastavenia a transakčných entít](field-references.md).
- Vytvorená ako riadok v tabuľke **Cenová dimenzia**. Pridajte napríklad riadky dimenzie ocenenia, ako je uvedené v nasledujúcom obrázku. 

![Riadky cenovej dimenzie na základe sumy.](media/Amt-based-PD.png)

Všimnite si, že pracovné hodiny zdroja (**msdyn_resourceworkhours**) sú pridané ako dimenzie založené na značkách a boli pridané do mriežky na karte **Cenová dimenzia založená na prirážke**.

![Riadky cenovej dimenzie na základe prirážky.](media/Markup-based-PD.png)

> [!IMPORTANT]
> Akákoľvek zmena cien dimenzie údajov v tejto tabuľke, existujúce alebo nové, je prenesená na obchodnú logiku ceny Project Service výhradne po obnovení vyrovnávacej pamäte. Čas obnovenia vyrovnávacej pamäte môže trvať až 10 minút. Nechajte potrebný čas na zobrazenie zmien v predvolenej logike ceny, ktorá musí byť výsledkom zmien v údajoch dimenzie ceny.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atribúty tabuľky dimenzie cien
Nasledujúce časti poskytujú informácie o rôznych atribútoch v tabuľke **Cenové dimenzie**.

### <a name="pricing-dimension-name"></a>Názov cenovej dimenzie
Táto hodnota by mala byť presne rovnaká ako názov schémy poľa, ktoré sa pridá do tabuľky **Cena roly** pre vlastné cenové dimenzie. Ďalšie informácie o pridávaní polí do tabuľky **Cena roly** nájdete v téme [Pridanie vlastných polí do cenového nastavenia a transakčných entít](field-references.md).

### <a name="type-of-dimension"></a>Typ dimenzie
Existujú dva typy cien dimenzií:
  
  - **Dimenzie založené na sume**: : hodnoty dimenzie z kontextu vstupu sa porovnajú s hodnotami dimenzie v riadku **Cena roly** a cena/náklady sa predvolene získavajú priamo z tabuľky **Cena roly**.
  - **Dimenzie založené na prirážke**: Ide o dimenzie, kde Project Service prijme nasledujúci 3-stupňový proces na získanie ceny/nákladov
 
    1. Project Service vyrovná hodnoty dimenzie nezaložené na prirážke z kontextu vstupu k riadku ceny roly, aby získal základnú sadzbu.
    2. Project Service vyrovná všetky dimenzie z kontextu vstupu k riadku **Prirážka k cene roly**, aby získal percentuálnu hodnotu prirážky.
    3. Project Service použije percento značenia z druhého kroku na základnú sadzbu získanú z tabuľky **Cena roly** v prvom kroku, aby sa dospelo ku konečnej cene/cene.
   
   Nasledujúca tabuľka znázorňuje výpočet cenových označení.
  
| Rola        | Organizačná jednotka    |Miesto výkonu práce      |Štandardný názov      |Pracovná doba zdroja      |  Označenie|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|U zákazníka            |                    |Nadčas                 |15     |
|             | Contoso India|Lokálny             |                    |Nadčas                 |10     |
|             | Contoso – USA   |Lokálny             |                    |Nadčas                 |20     |


Ak zdroj z Contoso India, ktorého základná sadzba je 100 USD, pracuje u zákazníka a vykáže 8 hodín bežnej pracovnej doby a 2 hodiny nadčasov v zadaní času, systém ceny Project Service využije základnú sadzbu 100 pre nasledujúcich 8 hodín, čím sa dosiahne 800 USD. Pre 2 hodiny nadčas, bude prirážka 15 % použitá na základnú sadzbu 100 na získanie jednotkovej ceny 115 USD a zaznamená celkové náklady na 230 USD.

### <a name="applicable-to-cost"></a>Vzťahuje sa na náklady 
Ak je nastavená na hodnotu **Áno**, znamená to, že hodnota dimenzie z kontextu vstupu by sa mala použiť na zhodu s poľami **Cena roly** a **Prirážka k cene roly** pri načítavaní sadzieb nákladov a prirážky.

### <a name="applicable-to-sales"></a>Vzťahuje sa na predaj
Ak je nastavená na hodnotu **Áno**, znamená to, že hodnota dimenzie z kontextu vstupu by sa mala použiť na zhodu s poľami **Cena roly** a **Prirážka k cene roly** pri načítavaní sadzieb fakturácie a prirážky.

### <a name="applicable-to-purchase"></a>Vzťahuje sa na nákup
Ak je nastavená na hodnotu **Áno**, znamená to, že hodnota dimenzie z kontextu vstupu by sa mala použiť na zhodu s poľami **Cena roly** a **Prirážka k cene roly** pri načítavaní sadzieb nákupnej ceny. V súčasnosti Project Service nepodporuje subdodávateľské scenáre, takže toto pole sa nepoužíva. 

### <a name="priority"></a>Priorita
Nastavenie priority dimenzie pomáha Project Service pri stanovení ceny, aj keď nedokáže nájsť presnú zhodu medzi hodnotami vstupnej dimenzie a hodnotami z tabuliek **Cena roly** alebo **Prirážka k cene roly**. V tomto scenári, Project Service bude používať nulové hodnoty pre nepriradené hodnoty dimenzie vážením dimenzií v poradí ich priority.

- **Priorita nákladov**: Hodnota dimenzie nákladov na dimenziu bude znamenať hmotnosť tohto rozmeru pri párovaní s nastavením cien nákladov. Hodnota **Priorita nákladov** musí byť jedinečná naprieč dimenziami, ktoré sa **vzťahujú na náklady**.
- **Priorita predaja**: Hodnota dimenzie predaja na dimenziu bude znamenať hmotnosť tohto rozmeru pri párovaní s nastavením cien predajov alebo sadzieb fakturácie. Hodnota **Priorita predaja** musí byť jedinečná naprieč dimenziami, ktoré sa **Vzťahuje sa na predaj**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]