---
title: Fakturácia preddavku alebo zálohy
description: Táto téma poskytuje informácie o tom, ako fakturovať preddavky a zálohy v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 12bf3822227badcf8c83d84d6aef6c0fdc7a972a
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596211"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Fakturácia preddavkovej alebo zálohovej platby

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations podporuje zmluvy založené na preddavkoch a jednorazové zálohy. V projektovej zmluve môžete zaznamenať plán preddavkov alebo jednorazových záloh. Zaznamenávanie na úrovni projektovej zmluvy však neznamená okamžité získanie preddavku alebo zálohy na použitie. Ak chcete použiť zálohu alebo preddavok na faktúre, ktorá sa zákazníkovi skutočne účtuje, je potrebné najskôr fakturovať preddavok alebo zálohu.

Ak chcete fakturovať preddavok alebo zálohu, vykonajte nasledujúci postup.

1. Vyberte **Predaj** > **Fakturácia** > **Preddavky a zálohy**. 
2. Na stránke **Zálohy a preddavky** použite filter na výber konkrétneho preddavku alebo zálohy na fakturáciu a označte ju ako **Pripravené na fakturáciu**.
3. Vytvorte faktúru manuálne zo zoznamu **Projektová zmluva** na stránke s podrobnosťami. Záloha alebo preddavok je uvedený na koncepte faktúry v časti **Zálohy a preddavky** na stránke **Faktúra**.
4. Potvrďte faktúru. Potom bude preddavok alebo záloha k dispozícii na použitie. Faktúru si môžete overiť na stránke so zoznamom **Preddavky a zálohy**. Pre fakturované zálohy alebo preddavky sa dostupná suma zobrazuje v mriežke.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Vytvorte preddavok alebo zálohu z mriežky faktúry

Zálohu alebo preddavok môžete vytvoriť priamo na faktúre.

1. V koncepte faktúry na vedľajšej mriežke **Zálohy a preddavky** vyberte možnosť **Nové** na vytvorenie nového preddavku alebo zálohy. 
2. Na stránke **Rýchle vytvorenie** pridajte potrebné informácie a potom vyberte **Uložiť**. Preddavok alebo záloha je vytvorená na projektovej zmluve súvisiacej s faktúrou. Preddavok alebo záloha sú automaticky označené ako **Pripravené na fakturáciu** a potom sa pridajú do vedľajšej mriežky **Zálohy a preddavky** na stránke **Faktúra**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Odsúhlasenie vyfakturovaného preddavku alebo zálohy

Po fakturácii preddavku alebo zálohy je možné ich použiť alebo odsúhlasiť na faktúre s časom, nákladmi, medzníkmi alebo inými poplatkami založenými na projekte. Zákazníkovi sa suma jeho faktúry zníži o sumu preddavku alebo zálohy použitej na tejto faktúre.

Na každej faktúre, ktorá sa vygeneruje pre projektovú zmluvu, v ktorej sa fakturovali preddavky alebo zálohy, Project Operation automaticky použije preddavky alebo zálohy pre faktúru.

Môžete si ich prezrieť na mriežke **Použité preddavky a zálohy** na stránke **Faktúra**. Nasledujúca tabuľka poskytuje informácie o poliach v mriežke **Použité preddavky a zálohy** na stránke **Projektová faktúra**.

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| Popis | Mriežka **Použité zálohy a preddavky** na stránke **Projektová faktúra** |Toto pole iba na čítanie poskytuje popis preddavku alebo zálohy použitej na tejto faktúre. Túto hodnotu nie je možné zmeniť na faktúre. Túto hodnotu je možné aktualizovať vo vedľajšej mriežke na stránke **Projektová zmluva**. | Toto pole sa môže zákazníkovi zobraziť na vytlačenej faktúre, aby sa určilo, ktorá záloha alebo preddavok sa na faktúre použije. |
| Dátum doručenia | Mriežka **Použité zálohy a preddavky** na stránke **Projektová faktúra**  | Toto pole iba na čítanie poskytuje dátum fakturácie preddavku alebo zálohy použitej na tejto faktúre. Túto hodnotu nie je možné zmeniť na faktúre. Túto hodnotu je možné aktualizovať vo vedľajšej mriežke na stránke **Projektová zmluva**. | Toto pole sa môže zákazníkovi zobraziť na vytlačenej faktúre na označenie dátumu, kedy bola záloha alebo preddavok prvýkrát fakturovaná zákazníkovi. |
| Množstvo | Mriežka **Použité zálohy a preddavky** na stránke **Projektová faktúra**  | Toto pole iba na čítanie poskytuje sumu preddavku alebo zálohy použitej na tejto faktúre. Túto hodnotu nie je možné zmeniť na faktúre. Túto hodnotu je možné aktualizovať vo vedľajšej mriežke na stránke **Projektová zmluva**. | Toto pole sa môže zákazníkovi zobraziť na vytlačenej faktúre na označenie dátumu pôvodnej sumy zálohy alebo preddavku, ktorú zaplatil zákazník. |
| Využitá suma | Mriežka **Použité zálohy a preddavky** na stránke **Projektová faktúra**  | Toto pole iba na čítanie obsahuje vypočítanú hodnotu, ktorá sumarizuje, aká suma z preddavku alebo zálohy sa použila. | Toto pole sa môže zákazníkovi zobraziť na vytlačenej faktúre na označenie sumy z tejto zálohy alebo preddavku, ktorá sa už použila. |
| Celková čiastka | Mriežka **Použité zálohy a preddavky** na stránke **Projektová faktúra**  | Toto upraviteľné pole obsahuje sumu preddavku alebo zálohy, ktorá sa používa na tejto projektovej faktúre. Táto suma nemôže byť vyššia ako suma, ktorá je k dispozícii v zálohe. Systém ju automaticky vypočíta ako rozdiel medzi poľami **Množstvo** a **Použité množstvo** v mriežke. Toto množstvo môžete znížiť, aby ste použili menej, ako je k dispozícii, ale nemôžete zvýšiť množstvo, aby ste spotrebovali viac, ako je k dispozícii. | Toto pole sa môže zákazníkovi zobraziť na vytlačenej faktúre na označenie sumy z tejto zálohy alebo preddavku, ktorá sa používa na faktúre. |
| Suma zostatku preddavku. | Mriežka **Použité zálohy a preddavky** na stránke **Projektová faktúra**  | Toto pole iba na čítanie obsahuje hodnotu sumy preddavku alebo zálohy, ktorá zostane po potvrdení faktúry. | Toto pole sa môže zákazníkovi zobraziť na vytlačenej faktúre na označenie sumy, ktorá zostane z tejto zálohy alebo preddavku po potvrdení a zaplatení faktúry. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]