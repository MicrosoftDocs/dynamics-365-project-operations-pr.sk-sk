---
title: Použitie kategórie transakcie ako cenovej dimenzie
description: Táto téma poskytuje informácie o používaní poľa Kategória transakcie ako cenovej dimenzie.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ab8093aca9a33bbbaef41c6fc7d33cad930bfadd13b0f7587c3de9032ac0d630
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996140"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Použitie kategórie transakcie ako cenovej dimenzie


_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_


Táto téma vysvetľuje, ako používať pole **Kategória transakcie** ako cenovú dimenziu. 

## <a name="prerequisites"></a>Predpoklady
Pred dokončením postupov v tejto téme musíte mať pre svoju organizáciu nové riešenie cenovej dimenzie. Ak ste si ho ešte nevytvorili, pozrite si stránku [Vytvorenie vlastných polí a entít ako cenových dimenzií](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Pridanie poľa Kategória transakcie do formulárov a zobrazení
Ak chcete zviditeľniť pole **Kategória transakcie** v riešení cenovej dimenzie, musíte pole pridať do všetkých formulárov a zobrazení ako entitu.

V nasledujúcej tabuľke sú uvedené všetky vopred pripravené formuláre a zobrazenia podľa entít. Nové pole budete musieť pridať do všetkých ďalších formulárov alebo zobrazení vo svojich prispôsobených entitách.

|  Entity        | Formuláre     |Zobrazenia        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena roly| Informácia |- Ceny kategórií aktívnych zdrojov<br> - Priradené ceny kategórií zdrojov |
|  Prirážka k cene roly| Informácia|- Aktívna prirážka k cene roly<br>- Priradená prirážka k cene roly |
|  Podrobnosti o riadku cenovej ponuky|- Informácie o projekte<br>- Rýchle vytvorenie projektu| - Podrobnosti o riadku aktívnej cenovej ponuky<br>- Kombinované podrobnosti o riadku cenovej ponuky<br>- Priradené podrobnosti o riadku cenovej ponuky |
|  Podrobnosti o riadku projektovej zmluvy|- Informácie o projekte<br>- Rýchle vytvorenie projektu|- Kombinované podrobnosti o riadku zmluvy<br>- Aktívne podrobnosti o riadku zmluvy<br>- Priradené podrobnosti o riadku zmluvy |
|  Projektová úloha|- Informácia<br>- Nový formulár| &nbsp; |
|  Člen projektového tímu|- Informácia<br>- Nový formulár|- Aktívni členovia projektového tímu<br>- Členovia projektového tímu<br>- Priradení členovia projektového tímu |
|  Zadanie času|- Informácia<br>- Vytvorenie zadania času|- Moje zadania času podľa dátumu<br>- Moje zadania času na tento týždeň<br>- Zadania času na schválenie|
|  Záznam v účtovnom denníku|- Informácia<br>- Rýchle vytvorenie|- Aktívne záznamy v účtovnom denníku<br>- Priradený záznam v účtovnom denníku|
|  Podrobnosti o riadku faktúry|- Informácia<br>- Rýchle vytvorenie|- Aktívne podrobnosti o riadku faktúry<br>- Fakturovateľné transakcie faktúr<br>- Bezplatné transakcie faktúr<br>- Priradené podrobnosti o riadku faktúry <br>- Nefakturovateľná transakcia faktúry|
|  Skutočnosť|- Informácia<br>- Aktívne skutočné hodnoty| Priradené skutočné hodnoty |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Nastavenie poľa Kategória transakcie ako cenovej dimenzie

1. Prejdite do časti **Nastavenia** > **Parametre**. 
2. Na stránke **Parametre**, na karte **Cenové dimenzie založené na čiastke**, skontrolujte, či mriežka zobrazuje záznamy v entite **Cenové dimenzie**.
3. Pridajte **Kategória transakcie** do tohto zoznamu a nastavte polia **Vzťahuje sa na náklady** a **Vzťahuje sa na predaj** na **Áno**.
4. V poli **Typ dimenzie** zvoľte možnosť **Na základe sumy** a potom zvoľte prioritu pre **Kategóriu transakcie**, ktorá sa týka nákladov a predajov.


[!INCLUDE[footer-include](../includes/footer-banner.md)]