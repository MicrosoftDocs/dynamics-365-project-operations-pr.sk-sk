---
title: Samostatná rezervácia zdrojov
description: Táto téma poskytuje informácie o požiadavkách na predbežnú rezerváciu.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 97323b73-c6de-4a7f-b889-19d4c42cf17a
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 08a8b46ee03fb93b30d178756e38c3086880f774
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755663"
---
# <a name="soft-book-requirements"></a>Požiadavky na predbežnú rezerváciu.

Požiadavku na zdroje možno rezervovať na pevno. Pevná rezervácia vytvára návrh, ktorý spotrebuje kapacitu prostriedku. Návrh sa potom odošle späť žiadateľovi na schválenie. Predbežná rezervácia predbežne pridá zdroj do projektového tímu a má iný stav na tabuli plánovania, ale nespotrebuje kapacitu prostriedku. Na predbežné rezervovanie zdroja na tabuli plánovania nastavte pole **Stav rezervácie** na **Predbežné**.

![Stav rezervácie je nastavený na Predbežné](media/Resource-Management-image77.png)

Keď sa karta **Tím** nachádza v zobrazení **Vymenovaní členovia tímu**, tu sa zobrazí zdroj. Predbežne rezervované hodiny sa vykážu v stĺpci **Počet predbežne rezervovaných hodín**.

![Predbežne rezervované hodiny v zobrazení Vymenovaní členovia tímu](media/Resource-Management-image78.png)

Členovia tímu, ktorí sú predbežne rezervovaní, nemôžu byť priradení k úlohám.

![Členov tímu, ktorý je predbežne rezervovany, priradený k úlohe](media/Resource-Management-image79.png)

Na karte **Vyrovnanie** sa pre predbežne rezervovaný zdroj nezobrazujú žiadne rezervácie, pretože karta **Vyrovnanie** zohľadňuje iba pevné rezervácie.

![Predbežne rezervovaný zdroj bez rezervácií na karte Vyrovnanie](media/Resource-Management-image80.png)

> [!NOTE]
> Zdroj nemožno predbežne rezervovať z požiadavky, ktorá bola vygenerované zo všeobecného člena tímu.

Na tabuli plánovania sa na predbežnú rezerváciu zdroja využíva iné farebné označenie.

![Predbežné rezervácie na tabuli plánovania](media/Resource-Management-image81.png)

Ak chcete predbežnú rezerváciu zmeniť na pevnú, na tabuli plánovania kliknite pravým tlačidlom na predbežnú rezerváciu, kde stlačte možnosť **Zmeniť stav** \> **Pevne rezervovať** \> **Pevne**.

![Zmena stavu rezervácie na pevný](media/Resource-Management-image82.png)

Rezervácia sa zmení a stav sa zmení na tabuli plánovania. Keďže stav rezervácie je teraz **Pevný**, zdroj je zobrazený ako rezervovaný a jeho kapacita a dostupnosť sa upravia.

Rovnakú metódu môžete použiť na zrušenie pevnej rezervácie alebo predbežnej rezervácie z tabule plánovania.

Ak chcete konvertovať predbežne rezervovaný prostriedok na pevne rezervovaný prostriedok, na projektovej karte **Tím** vyberte zdroj, a potom stlačte **Potvrdiť**.

![Príkaz potvrdenia](media/Resource-Management-image83.png)
