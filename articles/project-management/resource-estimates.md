---
title: Finančné odhady pre čas zdrojov na projektoch
description: Táto téma poskytuje informácie o spôsobe výpočtu finančných odhadov pre čas.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aab5c11a7dc23331c935403a4f96ec7197ec1572
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592573"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Finančné odhady pre čas zdrojov na projektoch

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Finančné odhady pre čas sa počítajú na základe troch faktorov: 

- Typ všeobecného alebo vymenovaného člena tímu priradeného ku každej úlohe listového uzla v pláne projektu. 
- Typ alebo zložitosť práce.
- Rozloženie úsilia na priradenie zdroja k úlohe. 

Prvé dva faktory ovplyvňujú jednotkové náklady alebo fakturačnú rýchlosť priradenia zdroja. Jednotkové náklady alebo fakturačná sadzba priradenia zdroja sa určuje podľa atribútov prideleného zdroja. Medzi tieto atribúty patria organizačná jednotka, do ktorej zdroj patrí, a štandardná rola zdroja. Môžete tiež pridať vlastné atribúty relevantné pre vaše podnikanie pre daný zdroj, napríklad štandardný názov alebo úroveň skúseností, a nechať ich, aby ovplyvnili jednotkové náklady alebo fakturačnú sadzbu priradenia.
Okrem atribútov zdroja môžu atribúty práce, ako napríklad úloha, ovplyvniť aj jednotkovú fakturačnú sadzbu alebo mieru nákladov na priradenie. Napríklad, keď sú niektoré úlohy zložitejšie, výsledkom priradenia zdroja k týmto konkrétnym úlohám sú vyššie jednotkové náklady alebo fakturačná rýchlosť ako pri úlohách, ktoré sú menej zložité.   

Tretí faktor poskytuje počet hodín pri tejto sadzbe. V prípadoch, keď úloha pokrýva dve cenové obdobia, je pravdepodobné, že prvá časť priradenia zdrojov pre túto úlohu sa nákladovo a cenovo odlišuje od druhej časti úlohy. Odhad úsilia pre každé priradenie zdrojov je komplexná hodnota uložená s denným rozložením úsilia za deň.

Podrobné pokyny týkajúce sa nastavenia vlastných atribútov práce a zdrojov ako cenových a nákladových dimenzií nájdete v [Prehľade dimenzií cien](../pricing-costing/pricing-dimensions-overview.md).

Finančný odhad pre každé priradenie zdrojov sa počíta ako **sadzba za hodinu pre priradenie vynásobená počtom hodín.**  Podobne ako odhad úsilia, aj finančný odhad nákladov a výnosov pre každé priradenie zdrojov je komplexná hodnota uložená s denným rozdelením peňažnej sumy za deň. 

## <a name="summarizing-financial-estimates-for-time"></a>Zhrnutie finančných odhadov pre čas
Finančný odhad pre čas pre úlohu listového uzla je súčtom finančných odhadov všetkých priradení zdrojov pre danú úlohu.

Finančný odhad pre čas pre súhrnnú alebo nadradenú úlohu je súčtom finančných odhadov všetkých jej podradených úloh. Toto sú odhadované náklady na prácu na projekte. 

![Odhady zdrojov.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Predvolená obstarávacia cena a mena nákladov

Predvolená obstarávacia cena pochádza z cenníkov pripojených k zmluvnej jednotke projektu. Mena nákladov projektu je vždy menou zmluvnej jednotky projektu. Pri priradení zdroja je finančný odhad nákladov uložený v mene nákladov projektu. Mena, v ktorej je v cenníku nastavená nákladová sadzba, sa niekedy líši od meny nákladov na projekt. V týchto prípadoch aplikácia prevedie menu, v ktorej je nastavená obstarávacia cena, pre menu projektu. Na mriežke **Odhady** sa všetky odhady nákladov zobrazia a zhrnú v mene nákladov projektu. 

## <a name="default-bill-rate-and-sales-currency"></a>Predvolené sadzby fakturácie a meny predaja

Predvolená predajná cena pochádza z cenníkov projektu pripojených k zmluve o súvisiacom projekte pri získaní obchodu, alebo zo súvisiacej cenovej ponuky projektu, ak je obchod stále v štádiu pred predajom. Mena predaja projektu je vždy menou cenovej ponuky projektu alebo projektovej zmluvy. Pri priradení zdroja je finančný odhad predajov uložený v mene predajov projektu. Na rozdiel od nákladov sa predajná cena stanovená v cenníku nemôže nikdy líšiť od predajnej meny projektu. Neexistuje scenár, v ktorom by bola potrebná konverzia meny. Na mriežke **Odhady** sa všetky odhady predajov zobrazia a zhrnú v mene predajov projektu. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
