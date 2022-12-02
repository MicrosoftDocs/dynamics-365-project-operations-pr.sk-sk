---
title: Použiť kategóriu transakcií ako dimenziu cien
description: Tento článok poskytuje informácie o používaní kategórie transakcie ako cenovej dimenzie.
author: Rumant
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 1a1c2dc17c2092e5364d90e7efc1f13aee80703e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915755"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Použiť kategóriu transakcií ako dimenziu cien

[!include [banner](../includes/psa-now-project-operations.md)]

Tento článok ukazuje, ako používať kategóriu transakcie ako cenovú dimenziu. Skôr, ako začnete, ak ste ešte nevytvorili riešenie dimenzie cien, budete musieť vytvoriť novú. Ak už máte riešenie dimenzie cien, môžete vykonať zmeny v tomto riešení. Ak ste pre vašu organizáciu nevytvorili nové riešenie cenovej dimenzie, dokončite postupy v článku [Vytvorte vlastné polia a entity](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Pridanie kategórie transakcie do formulárov a zobrazení
Ak chcete, aby sa kategória transakcie zobrazovala v používateľskom rozhraní v riešení dimenzie cien, budete musieť prejsť všetkými formulármi a pohľadmi kľúčových entít a pridať tieto polia do formulárov a zobrazení týchto entít.
Nasledujúca tabuľka je komplexný zoznam predpripravených formulárov a zobrazení, uvedených podľa entity, ktoré budú musieť byť aktualizované novými poľami. Ak sa vo vašich prispôsobeniach týchto entít nachádzajú ďalšie zobrazenia alebo formuláre, pridajte do nich aj nové polia.

|  Entita        | Formuláre     |Zobrazenia        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena roly|• Informácia |• Ceny kategórií aktívnych zdrojov<br> • Priradené zobrazenie cien kategórií zdrojov|
|  Prirážka k cene roly|Informácia|• Aktívna prirážka k cene roly<br>• Priradené zobrazenie prirážok k cenám rol|
|  Podrobnosti o riadku cenovej ponuky|• Informácie o projekte<br>• Rýchle vytvorenie projektu|• Podrobnosti o riadku aktívnej cenovej ponuky<br>• Kombinované podrobnosti o riadku cenovej ponuky<br>• Priradené zobrazenie podrobností o riadku cenovej ponuky|
|  Podrobnosti o riadku projektovej zmluvy|• Informácie o projekte<br>• Rýchle vytvorenie projektu|• Kombinované podrobnosti riadka zmluvy<br>• Aktívne podrobnosti o riadku zmluvy<br>• Priradené zobrazenie podrobností o riadku zmluvy|
|  Projektová úloha|Informácia<br>• Nový formulár||
|  Člen projektového tímu|Informácia<br>• Nový formulár|• Aktívni členovia projektového tímu<br>• Členovia projektového tímu<br>• Priradené zobrazenie členov projektového tímu|
|  Zadanie času|Informácia<br>• Vytvoriť zadanie času|• Moje zadania času podľa dátumu<br>• Moje zadania času na tento týždeň<br>• Zadania času na schválenie|
|  Záznam v účtovnom denníku|Informácia<br>• Rýchle vytvorenie|• Aktívne záznamy v účtovnom denníku<br>• Priradené zobrazenie záznamov v účtovnom denníku|
|  Podrobnosti o riadku faktúry|Informácia<br>• Rýchle vytvorenie|• Aktívne podrobnosti o riadku faktúry<br>• Fakturovateľné transakcie faktúr<br>• Bezplatné transakcie faktúr<br>• Priradené zobrazenie podrobností o riadku faktúry<br>• Nefakturovateľná transakcia faktúry|
|  Skutočná hodnota|• Informácia<br>• Aktívne skutočné hodnoty|• Priradené zobrazenie skutočných hodnôt|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Nastaviť kategóriu transakcií ako dimenziu cien

1. Vo webovom rozhraní prejdite do ponuky **Project Service** > **Nastavenia** > **Parametre**. 
2. Na stránke **Parameter**, na kartu **Cenové dimenzie založené na čiastke**, si všimnite, že mriežka na karte zobrazuje záznamy v **Cenové dimenzie** entity.
3. Pridajte **Kategória transakcie** do tohto zoznamu a nastavte polia **Vzťahuje sa na náklady** a **Vzťahuje sa na predaj** na **Áno**.
4. V poli **Typ dimenzie** zvoľte možnosť **Na základe sumy** a potom zvoľte prioritu pre **Kategóriu transakcie** súvisiacu s nákladmi a predajom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
