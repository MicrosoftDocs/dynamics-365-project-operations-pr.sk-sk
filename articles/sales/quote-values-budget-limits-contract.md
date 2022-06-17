---
title: Nastavenia projektovej cenovej ponuky
description: Tento článok poskytuje informácie o informáciách a nastaveniach, ktoré sa vzťahujú na cenové ponuky projektov a ovplyvňujú ich.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 661dd40edeea890ad684b801bcc99ce2c242bb9b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931947"
---
# <a name="header-details-for-project-based-quotes"></a>Podrobnosti hlavičky pre projektové cenové ponuky

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_


Tento článok vysvetľuje informácie, ktoré sa týkajú cenovej ponuky projektu. Patria sem nastavenia, ktoré majú vplyv na všetky riadky cenovej ponuky, a informácie o ponuke, ktoré sú zhrnuté vo všetkých riadkových položkách a slúžia na zvýšenie kľúčových ukazovateľov výkonu cenovej ponuky projektu.

V nasledujúcej tabuľke je uvedený zoznam polí so súhrnnými informáciami v cenovej ponuke projektu, ktoré sú jedinečné pre Dynamics 365 Project Operations alebo majú niektoré dôležité zmeny správania v porovnaní s cenovými ponukami z Dynamics 365 Sales.

| **Pole** | **Miesto** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- | --- |
| Zadať | Karta Súhrn (skrytá) | Toto pole množiny možností má nasledujúce možnosti:</br>- Založené na práci (k dispozícii iba vtedy, keď je nainštalovaný Project Operations)</br>- Založené na položke (k dispozícii iba vtedy, keď sú nainštalované Project Operations a Sales)</br>- Služba založená na údržbe (k dispozícii, keď je nainštalovaná služba Dynamics 365 Field Service) | Keď použijete aplikáciu Project Operations, hodnota tohto poľa sa automaticky nastaví na **Založené na práci**. Klasifikuje príležitosť ako založenú na projekte. Cenová ponuka by mala byť založená na projekte, aby umožnila všetky rozšírenia a funkcie špecifické pre projekt. |
| Vlastniaca spoločnosť | Súhrn | Právnická entita, ktorá bude zodpovedať za náklady a výnosy, ktoré vzniknú z tohto projektu alebo z projektov spojených s touto cenovou ponukou. Po vytvorení cenovej ponuky z príležitosti sa toto pole skopíruje z príslušného poľa v príležitosti. | Vlastnená spoločnosť je rovnaká ako pojem právna entita v module **Projektové riadenie a účtovníctvo** v Project Operations. Všetky náklady a výnosy z tohto projektu sa zaúčtujú v hlavnej účtovnej knihe vlastniacej spoločnosti. |
| Potenciálny zákazník | Karta súhrnu | Odkaz na záznam zákazníka spoločnosti zákazníka alebo obchodného vzťahu. Platný zákazník, na ktorého sa odkazuje cenová ponuka projektu, musí byť nastavený ako zákazník v spoločnosti, ktorá vlastní cenovú ponuku. Vlastniaca spoločnosť zobrazuje zoznam právnických entít, ktoré sú nastavené v module **Projektové riadenie a účtovníctvo** v Project Operations. Po vytvorení cenovej ponuky z príležitosti sa toto pole skopíruje z príslušného poľa v príležitosti. | Mena v cenovej ponuke projektu je predvolene založená na mene zákazníka. Túto možnosť však možno zmeniť pred uložením cenovej ponuky. |
| Manažér obchodného vzťahu | Karta súhrnu | Meno manažéra obchodného vzťahu pre túto dohodu. Po vytvorení cenovej ponuky z príležitosti sa toto pole skopíruje z príslušného poľa v príležitosti. | Manažér obchodného vzťahu je zodpovedný za riadenie vzťahov so zákazníkom po dokončení tohto projektu. Na základe rezervovateľného záznamu zdroja naviazaného na manažéra obchodného vzťahu je v zmluvnej jednotke predvolená cenová ponuka projektu.|
| Zmluvná jednotka | Karta súhrnu | Organizačná jednotka, ktorá je zodpovedná za realizáciu projektu alebo projektov spojených s touto cenovou ponukou. Po vytvorení cenovej ponuky z príležitosti sa toto pole skopíruje z príslušného poľa v príležitosti. | Zmluvnou jednotkou je divízia spoločnosti, ktorá bude po uzatvorení obchodu realizovať projekty. Každá zmluvná jednotka má menu, ktorá sa používa na vykazovanie odhadovaných a skutočných nákladov vzniknutých počas realizácie projektu. |
| Cenník produktov | Karta súhrnu | Toto je cenník, ktorý sa používa na predvolené ceny v riadkoch cenových ponúk založených na produkte. Zoznam možností pre toto pole zobrazuje zoznam cenníkov, kde sa mena cenníka zhoduje s menou v ponuke. Po vytvorení cenovej ponuky z príležitosti sa toto pole skopíruje z príslušného poľa v príležitosti. Toto pole príležitosti je predvolené zo záznamu obchodného vzťahu, ale je možné ho zmeniť. | Po získaní cenovej ponuky sa hodnota poľa skopíruje do vytvorenej zmluvy projektu. |
| Mena | Karta súhrnu | Označuje menu, ktorá sa použije na hlásenie hodnoty tejto dohody. Je to tiež mena, v ktorej bude zákazníkovi vystavená faktúra, ak dôjde k získaniu obchodu. Po vytvorení cenovej ponuky z príležitosti sa toto pole skopíruje z príslušného poľa v príležitosti. Toto pole príležitosti je predvolené zo záznamu obchodného vzťahu, ale používateľ ho môže zmeniť.  | Po uložení cenovej ponuky už toto pole nie je možné upravovať. Používa sa na predvolenie cenníkov produktov a projektov v cenovej ponuke. Mena v cenovej ponuke sa používa na zhodu s menou v cenníku. |
| Limit, ktorý sa nesmie prekročiť | Karta súhrnu | Naznačuje vyjednaný horný limit konečnej hodnoty, s ktorou zákazník v prípade tejto dohody súhlasí. | Tento horný limit sa hodnotí počas vykonávania a je použiteľný vo všetkých riadkových položkách a projektoch spojených s touto dohodou. |
| Požadovaný čas doručenia | Karta súhrnu | Po vytvorení cenovej ponuky z príležitosti sa toto pole skopíruje z príslušného poľa v príležitosti. | Tento dátum sa používa ako konečný dátum na generovanie plánov faktúr. |

Ďalej sú uvedené karty a kľúčové ukazovatele výkonu, ktoré sú k dispozícii v ponuke projektu a sú jedinečné pre Project Operations alebo majú niektoré dôležité zmeny v správaní cenových ponúk predaja:

| **Pole** | **Miesto** | **Opis** |
| --- | --- | --- |
| Analýza ziskovosti | Karta na cenovej ponuke | Karta zobrazuje nasledujúce metriky:</br>- Celkové účtovateľné náklady</br></br>- Celkové neúčtovateľné náklady</br>- Celkové výnosy</br>- Celkové výnosy (základné)</br>- Hrubý zisk</br>- Upravený hrubý zisk|
| Porovnanie s očakávaniami zákazníka | Karta na cenovej ponuke | Táto karta zobrazuje nasledujúce metriky:</br>- Odhadované dokončenie</br>- Požadované dokončenie</br>- Rozpočet zákazníka</br>- Hodnota ponuky |
| Analýza cenovej ponuky | Karta na cenovej ponuke | Táto karta sumarizuje nasledujúce najlepšie kľúčové ukazovatele výkonu týkajúce sa cenovej ponuky projektu</br>- Porovnanie s očakávaniami zákazníka, pokiaľ ide o rozpočet a plán</br>- Hrubý zisk</br>- Upravený hrubý zisk |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
