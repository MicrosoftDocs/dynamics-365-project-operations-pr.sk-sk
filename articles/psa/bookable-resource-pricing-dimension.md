---
title: Použiť rezervovateľný zdroj ako cenovú dimenziu
description: Táto téma poskytuje informácie o používaní rezervovateľného prostriedku ako dimenzie cien.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d9b25a768f892d83c09d37ce76291d6c8e75b1be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145017"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Použiť rezervovateľný zdroj ako cenovú dimenziu

[!include [banner](../includes/psa-now-project-operations.md)]

Táto téma poskytuje informácie o používaní rezervovateľného prostriedku ako dimenzie cien. Skôr, ako začnete, ak ste ešte nevytvorili riešenie dimenzie cien, budete musieť vytvoriť novú. Ak už máte riešenie dimenzie cien, môžete vykonať zmeny v tomto riešení. Ak ste pre vašu organizáciu nevytvorili nové riešenie dimenzie cien, dokončite postupy v téme [Vytvorte vlastné polia a entity](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Pridanie rezervovateľného prostriedku do formulárov a zobrazení
Ak chcete, aby sa polia zobrazovali v používateľskom rozhraní v riešení dimenzie cien, budete musieť prejsť všetkými formulármi a pohľadmi kľúčových entít služby Project Service a pridať tieto polia do formulárov a zobrazení týchto entít.
Nasledujúca tabuľka je komplexný zoznam out-of-box formulárov a zobrazenia, uvedené podľa entity, ktoré budú musieť byť aktualizované. Ak sa vo vašich prispôsobeniach týchto entít nachádzajú ďalšie zobrazenia alebo formuláre, pridajte do nich aj nové polia.
Otvorte Prieskumníka riešení pre riešenie cenovej dimenzie a potom kliknite na **publikovať všetky prispôsobenia**.


|   Entita        | Formuláre   |Zobrazenia        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena roly|Informácia |• Ceny kategórií aktívnych zdrojov<br> • Priradené zobrazenie cien kategórií zdrojov|
|  Prirážka k cene roly|Informácia|• Aktívna prirážka k cene roly<br>• Priradené zobrazenie prirážok k cenám rol|
|  Podrobnosti o riadku cenovej ponuky|• Informácie o projekte<br>• Rýchle vytvorenie projektu|• Podrobnosti o riadku aktívnej cenovej ponuky<br>• Kombinované podrobnosti o riadku cenovej ponuky<br>• Priradené zobrazenie podrobností o riadku cenovej ponuky|
|  Podrobnosti o riadku projektovej zmluvy|• Informácie o projekte<br>• Rýchle vytvorenie projektu|• Kombinované podrobnosti riadka zmluvy<br>• Aktívne podrobnosti o riadku zmluvy<br>• Priradené zobrazenie podrobností o riadku zmluvy|
|  Projektová úloha|Informácia<br>• Nový formulár||
|  Člen projektového tímu|Informácia<br>• Nový formulár|• Aktívni členovia projektového tímu<br>• Členovia projektového tímu<br>• Priradené zobrazenie členov projektového tímu|
|  Zadanie času|Informácia<br>• Vytvoriť zadanie času|• Moje zadania času podľa dátumu<br>• Moje zadania času na tento týždeň<br>• Zadania času na schválenie|
|  Záznam v účtovnom denníku|Informácia<br>• Rýchle vytvorenie|• Aktívne záznamy v účtovnom denníku<br>• Priradené zobrazenie záznamov v účtovnom denníku|
|  Podrobnosti o riadku faktúry|Informácia<br>• Rýchle vytvorenie|• Aktívne podrobnosti o riadku faktúry<br>• Fakturovateľné transakcie faktúr<br>• Bezplatné transakcie faktúr<br>• Priradené zobrazenie podrobností o riadku faktúry<br>• Nefakturovateľná transakcia faktúry|
|  Skutočná hodnota|Informácia<br>• Aktívne skutočné hodnoty|• Priradené zobrazenie skutočných hodnôt|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Nastaviť rezervovateľný zdroj ako cenovú dimenziu

1. Vo webovom rozhraní prejdite do ponuky **Project Service** > **Nastavenia** > **Parametre**. Na stránke **parameter**, na kartu **Cenové dimenzie založené na čiastke**, všimnite si, že mriežka na karte zobrazuje záznamy v cenách dimenzie entity. 
2. Pridajte **Rezervovateľný zdroj** do tohto zoznamu cenových dimenzií ako **msdyn_bookableresource**. 
3. Uveďte kontext, v ktorom rezervovateľný zdroj funguje ako cenový rozmer a nastavte hodnoty **vzťahuje sa na náklady** a **vzťahuje sa na predaj**.
4. V poli **typ dimenzie** vyberte položku **založené na čiastke**. 
5. Vyberte prioritu nákladov a predaja rezervovateľného prostriedku. Zvyčajne, ak sú zahrnuté ako cenový rozmer, rezervovateľný zdroj má najvyššiu prioritu, takže nastavenie na **1** (alebo **0** v závislosti od toho, ako budete počítať prioritu) by zabezpečilo, toto správanie.

## <a name="set-up-pricing-dimension-field-names"></a>Nastavte názvy polí cenových dimenzií

Ak je názov poľa cenovej dimenzie v tabuľke **Cena role** odlišný od názvu poľa v ktoromkoľvek z ostatných entít, v ktorých je potrebné, aby cena pracovala, musí byť záznam o cenovej dimenzii informovaný o rôznych názvoch.    
Pre rezervovateľný zdroj, má entita **Členovia projektového tímu** mierne odlišný názov poľa (**msdyn_bookableresourceid**) z toho, čo sa nazýva **cena role** entity (**msdyn_bookableresource**). Záznam cenového rozdielu pre **msydn_bookableresource** musí byť o tomto informovaný. 
1. Vykonáte to tak, že dvakrát kliknete na riadok v mriežke **cenový rozmer**, čím otvoríte stránku dimenzie **msdyn_bookableresource**.
2. Na stránke dimenzia kliknite na kartu **príbuzné** na položku **názvy polí dimenzie ocenenia**.

 ![Názvy kariet polí cenových dimenzií](media/PD-fieldname.png)

4. V priradenom zobrazení ktoré sa otvorí, kliknite na **Pridať nový názov poľa dimenzie ceny**.

 ![Pridajte Názvy polí cenových dimenzií](media/Add-NewPD-fieldname.png)


Toto otvára stránku **Názov poľa novej cenovej dimenzie** pre **msdyn_bookableresource**. 

5. Pridajte **msdyn_projectteam** do poľa **logický názov entity** a **msdyn_bookableresourceid** do poľa **Názov poľa**. Uložte záznam.

 ![Názov formulára Nová cenová dimenzia](media/PD-fieldname-Added.png)
