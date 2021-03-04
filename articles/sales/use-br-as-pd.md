---
title: Použitie rezervovateľného zdroja ako cenovej dimenzie
description: Táto téma poskytuje informácie o používaní rezervovateľného zdroja ako cenovej dimenzie.
author: Rumant
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0c5cb85f7c43f7b2fd9c367d7f7ac9c3250e0a1
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643102"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Použitie rezervovateľného zdroja ako cenovej dimenzie

 _**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_ 

Táto téma poskytuje informácie o používaní rezervovateľného zdroja ako cenovej dimenzie. Ak je vaša cenová stratégia nastavená tak, že každý rezervovateľný zdroj musí mať konkrétnu cenu alebo nákladovú sadzbu, použite rezervovateľný zdroj ako cenovú dimenziu.

## <a name="prerequisites"></a>Predpoklady
Pred dokončením postupov v tejto téme musíte mať pre svoju organizáciu nové riešenie cenovej dimenzie. Ak ste si ho ešte nevytvorili, pozrite si stránku [Vytvorenie vlastných polí a entít](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Pridanie poľa Rezervovateľný zdroj do formulárov a zobrazení
Ak chcete zviditeľniť pole **Rezervovateľný zdroj** v riešení cenovej dimenzie, musíte pole pridať do všetkých formulárov a zobrazení ako entitu.

V nasledujúcej tabuľke sú uvedené všetky vopred pripravené formuláre a zobrazenia podľa entít. Nové pole budete musieť pridať do všetkých ďalších formulárov alebo zobrazení vo svojich prispôsobených entitách.

|   Entity        | Formuláre   |Zobrazenia        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena roly| Informácia | - Ceny kategórií aktívnych zdrojov<br> - Priradené ceny kategórií zdrojov |
|  Prirážka k cene roly| Informácia| - Aktívna prirážka k cene roly<br>- Priradená prirážka k cene roly |
|  Podrobnosti o riadku cenovej ponuky| - Informácie o projekte<br>- Rýchle vytvorenie projektu| - Podrobnosti o riadku aktívnej cenovej ponuky<br>- Kombinované podrobnosti o riadku cenovej ponuky<br>- Priradené podrobnosti o riadku cenovej ponuky |
|  Podrobnosti o riadku projektovej zmluvy| - Informácie o projekte<br>- Rýchle vytvorenie projektu| - Kombinované podrobnosti o riadku zmluvy<br>- Aktívne podrobnosti o riadku zmluvy<br>- Priradené podrobnosti o riadku zmluvy |
|  Projektová úloha| - Informácia<br>- Nový formulár| &nbsp; |
|  Člen projektového tímu| - Informácia<br>- Nový formulár| - Aktívni členovia projektového tímu<br>- Členovia projektového tímu<br>- Priradení členovia projektového tímu |
|  Zadanie času| - Informácia<br>- Vytvorenie zadania času| - Moje zadania času podľa dátumu<br>- Moje zadania času na tento týždeň<br>- Zadania času na schválenie|
|  Záznam v účtovnom denníku| - Informácia<br>- Rýchle vytvorenie| - Aktívne záznamy v účtovnom denníku<br>- Priradený záznam v účtovnom denníku |
|  Podrobnosti o riadku faktúry| - Informácia<br>- Rýchle vytvorenie| - Aktívne podrobnosti o riadku faktúry<br>- Fakturovateľné transakcie faktúr<br>- Bezplatné transakcie faktúr<br>- Priradené podrobnosti o riadku faktúry <br>- Nefakturovateľná transakcia faktúry|
|  Skutočnosť| - Informácia<br>- Aktívne skutočné hodnoty| Priradená skutočná hodnota |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Nastavenie rezervovateľného zdroja ako cenovej dimenzie
Ak chcete nastaviť rezervovateľný zdroj ako cenovú dimenziu, postupujte podľa týchto pokynov:

1. Prejdite do časti **Nastavenia** > **Parametre**. 
2. Na stránke **Parameter**, na karte **Cenové dimenzie založené na čiastke**, skontrolujte, či mriežka zobrazuje záznamy v entite **Cenové dimenzie**. 
2. Pridajte **Rezervovateľný zdroj** do tohto zoznamu cenových dimenzií ako **msdyn_bookableresource**. 
3. V položkách **Vzťahuje sa na náklady** a **Vzťahuje sa na predaj** vyberte hodnotu.
4. V poli **Typ dimenzie** vyberte položku **Založené na čiastke**. 
5. Vyberte prioritu nákladov a predaja rezervovateľného prostriedku. Rezervovateľný zdroj má zvyčajne najvyššiu prioritu, ak je zahrnutý ako cenová dimenzia. Aby ste zabezpečili toto správanie, nastavte prioritu na **1** (alebo **0** podľa toho, ako počítate prioritu).

## <a name="set-up-pricing-dimension-field-names"></a>Nastavte názvy polí cenových dimenzií

Ak je názov poľa cenovej dimenzie v tabuľke **Cena roly** odlišný od názvu poľa v ktorejkoľvek z ostatných entít, v ktorých sa používa predvolená cena, záznam o cenovej dimenzii musí byť oboznámený o rôznych názvoch.  

Pre rezervovateľný zdroj, má entita **Členovia projektového tímu** mierne odlišný názov poľa od toho, ktoré sa volá v entite **Cena roly**: 

 - Entita **Členovia projektového tímu** = **msdyn_bookableresourceid**
 - Entita **Cena roly** = **msdyn_bookableresource**

Záznam cenovej dimenzie pre **msydn_bookableresource** musí byť oboznámený s týmto rozdielom.

1. Dvakrát kliknite na riadok v mriežke **Cenová dimenzia**, čím otvoríte stránku dimenzie **msdyn_bookableresource**.
2. Na stránke dimenzie kliknite na kartu **Súvisiace** a vyberte **Názvy polí cenových dimenzií**.

  ![Názvy kariet polí cenových dimenzií](media/PD-fieldname.png)

3. V priradenom zobrazení, ktoré sa otvorí, vyberte **Pridať nový názov poľa cenovej dimenzie**.

  ![Pridajte Názvy polí cenových dimenzií](media/Add-NewPD-fieldname.png)

  Toto otvára stránku **Názov poľa novej cenovej dimenzie** pre **msdyn_bookableresource**. 

4. Na stránke **Nový názov poľa cenovej dimenzie** pridajte **msdyn_projectteam** do poľa **Logický názov entity**.
5. Pridajte **msdyn_bookableresourceid** do poľa **Názov poľa**.

 ![Názov formulára Nová cenová dimenzia](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]