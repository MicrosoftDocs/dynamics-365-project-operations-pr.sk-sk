---
title: Hlavička/súhrn príležitostí
description: Táto téma poskytuje informácie o dohodách na základe projektu a riadkoch príležitostí založených na projekte.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c4e91c1a869347ac1182db2de1ab9244309eb856
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084239"
---
# <a name="opportunity-headersummary"></a>Hlavička/súhrn príležitostí

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_


Hlavička alebo zhrnutie príležitosti zachytáva celkové informácie o dohode založenej na projekte, ktorá sa vzťahuje na všetky riadky príležitosti založenej na projekte.

Príležitosti založené na projekte v Dynamics 365 Project Operations sú rozšírením príležitostí v Dynamics 365 Sales. Tieto rozšírenia poskytujú ďalšiu funkcionalitu, ktorá je špecifická a vyžaduje sa pre príležitosti založené na projekte. Tieto rozšírenia môžu obsahovať nové polia a akcie na páse s nástrojmi dostupné v príležitostiach založených na projektoch. Možno nájdete niektoré polia, funkčnosť a predvolenú logiku, ktorá je k dispozícii v službe Sales, ale nie je k dispozícii v Project Operations.

Nasledujúca tabuľka obsahuje polia v príležitosti založenej na projekte, ktoré sú buď jedinečné pre operácie projektu, alebo majú niektoré dôležité zmeny v správaní z ponuky Príležitosti v predaji.

| **Pole** | **Miesto** | **Relevantnosť, účel a pokyny** | **Nadväzujúci vplyv** |
| --- | --- | --- | --- |
| Typ | Karta Všeobecné (skrytá) | Toto pole množiny možností má nasledujúce možnosti:</br>- Založené na práci (k dispozícii iba s Project Operations)</br>- Založené na položke (k dispozícii iba vtedy, keď sú nainštalované Project Operations a Sales)</br>- Služba založená na údržbe (k dispozícii, keď je nainštalovaná služba Field Service) | Keď použijete Project Operations, hodnota tohto poľa sa automaticky nastaví na **Založené na práci** , ktorá klasifikuje Príležitosť ako založenú na projekte. Príležitosť by mala byť založená na projekte, aby boli povolené všetky rozšírenia a funkcie na základe projektu v procese následného predaja tejto dohody. |
| Vlastniaca spoločnosť | Karta Všeobecné | Toto je spoločnosť alebo právnická entita, ktorá dodá projekt pre zákazníka. | Informácie o tomto poli sa skopírujú do zodpovedajúceho poľa v cenovej ponuke projektu, ktoré sa vytvorí z tejto príležitosti. |
| Kontakt | Karta Všeobecné | Odkaz na primárny kontakt zákazníka pre túto dohodu. | |
| Konto | Karta Všeobecné | Odkaz na záznam zákazníka spoločnosti zákazníka alebo obchodného vzťahu. | |
| Manažér obchodného vzťahu | Karta Všeobecné | Meno správcu obchodného vzťahu pre túto príležitosť založenú na projekte. | Manažér obchodného vzťahu je zodpovedný za riadenie vzťahov so zákazníkom po dokončení tohto projektu. Na základe rezervovateľného záznamu zdroja viazaného na správcu obchodného vzťahu je predvolená zmluvná jednotka. |
| Zmluvná jednotka | Karta Všeobecné | Organizačná jednotka, ktorá je zodpovedná za realizáciu projektu alebo projektov spojených s týmto obchodom. | Zmluvnou jednotkou je divízia spoločnosti, ktorá po uzatvorení obchodu dokončí projekt(-y). Každá zmluvná jednotka má menu, ktorá sa používa na vykazovanie odhadovaných a skutočných nákladov vzniknutých počas projektu. |

Pre všetky ostatné polia a oddiely na karte **Súhrn** príležitosti si pozrite [Vytváranie alebo úprava príležitostí (Predaj a Centrum predaja)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).
