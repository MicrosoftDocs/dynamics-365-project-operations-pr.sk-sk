---
title: Subdodávateľské zmluvy v rámci vydania skoršieho prístupu v októbri 2021
description: Táto téma poskytuje prehľad možností subdodávateľských zmlúv v Project Operations, ktoré sú súčasťou vydania skoršieho prístupu v októbri 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383714"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Subdodávateľské zmluvy v rámci vydania skoršieho prístupu v októbri 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma poskytuje prehľad možností subdodávateľských zmlúv v Dynamics 365 Project Operations, ktoré sú súčasťou vydania skoršieho prístupu v októbri 2021. Táto množina funkcií nie je pripravená na produkčné ani živé prostredie, takže tieto funkcie zostanú vo vydaní pre skorší prístup, kým nevyjde celá množina funkcií. Dôrazne odporúčame, aby ste množinu funkcií subdodávateľských zmlúv nepoužívali pre scenáre živej produkcie, kým nebude odstránený banner verzie Preview. 

Nasledujúci zoznam poskytuje prehľad toho, čo je v súčasnosti k dispozícii vo verzii skoršieho prístupu z októbra 2021:

1. Projektový manažér vytvorí subdodávateľskú zmluvu s dodávateľom. Pre subdodávateľskú zmluvu sa štandardne používajú cenníky, ktoré sú pripojené k záznamu dodávateľa. Dodávateľský obchodný vzťah má typ vzťahu **Dodávateľ** alebo **Poskytovateľ**.

2. Projektový manažér môže všetky nákupy podrobne rozpísať ako riadkové položky v subdodávateľskej zmluve. Riadky subdodávateľskej zmluvy môžu byť pre čas, náklady alebo produkty. Trieda transakcie riadka subdodávateľskej zmluvy určuje, na čo je daný riadok určený.

3. Account manažér dodávateľa a projektový manažér môžu iterovať prostredníctvom subdodávateľskej zmluvy. Ceny možno upravovať v nákupných cenníkoch, ktoré sú pripojené k subdodávateľskej zmluve.

4. V tomto bode alebo neskôr v procese, ak je riadok subdodávateľskej zmluvy určený pre čas, account manažér dodávateľa spojí kontakty dodávateľa s každým riadkom subdodávateľskej zmluvy. Toto priradenie poskytuje informácie projektovému manažérovi, ktorý pracuje na subdodávateľskej zmluve. Keď je kontakt dodávateľa priradený k riadku subdodávateľskej zmluvy, systém automaticky vytvorí rezervovateľný zdroj z kontaktu, ak rezervovateľný zdroj ešte neexistuje.

5. Spôsob fakturácie na každom riadku subdodávateľskej zmluvy môže byť **Pevná cena** alebo **Čas a materiál**. V prípade riadkov subdodávateľských zmlúv s pevnou cenou sa nastaví plán faktúr založený na medzníkoch.

Zostávajúce kroky v toku obchodného procesu pre subdodávateľskú zmluvu, ktoré sú popísané v Prehľade, momentálne nie sú k dispozícii. Keď budú pridané nové funkcie, táto téma bude aktualizovaná. 

Nasledujúci obrázok predstavuje vydanie Subdodávateľské zmluvy so skorším prístupom v kontraste s obchodným procesom typu end-to-end.

![Postup procesu subdodávateľských zmlúv](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Riadky subdodávateľskej zmluvy založené na množstve a na práci, vydanie so skorším prístupom
Vo vydaní so skorším prístupom z októbra 2021 sú podporované iba riadky subdodávateľských zmlúv založené na množstve. To znamená, že riadok subdodávateľskej zmluvy je možné použiť na nákup času, výdavkov alebo materiálu od dodávateľa, ale nie celého súboru práce. To tiež znamená, že nakupované množstvo (jednotky času, výdavky alebo množstvo materiálu) na riadku subdodávateľskej zmluvy je možné použiť na akýkoľvek projekt v systéme.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
