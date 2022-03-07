---
title: Vypnutie cenovej dimenzie
description: Táto téma poskytuje informácie o vypnutí cenových dimenzií.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3d9f0cb2a054941b07809b61ca14a3145c6d6d06acd6ca40255d5ec9de92be22
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994520"
---
# <a name="turning-off-a-pricing-dimension"></a>Vypnutie cenovej dimenzie

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Možno budete musieť skontrolovať a aktualizovať svoje cenové stratégie každých niekoľko rokov. Všetky aktualizácie, ktoré vykonáte, môžu vyžadovať vypnutie existujúcej dimenzie cien a vytvorenie novej. Napríklad, možno ste predtým oceňovali na základe **Roly**, ale teraz ste sa rozhodli pre cenu podľa **pracovných skúseností**. To môže vyžadovať vypnutie **Roly** ako cenovej dimenzie a vytvorenie **Pracovnej skúsenosti** ako novej cenovej dimenzie. 

Vypnutie cenovej dimenzie, bez ohľadu na to, či je predpripravená alebo vlastná, možno vykonať nastavením možnosti **Vzťahuje sa na náklady** a **Vzťahuje sa na predaj** polia dimenzie cien na **Nie**.

Keď to však urobíte, môže sa zobraziť chybové hlásenie **Cenovú dimenziu nie je možné aktualizovať ani vymazať, ak sú priradené záznamy o cenách**.

![Chyba obchodného procesu pravdepodobne pri vypnutí cenovej dimenzie.](media/Business-Process-Error.png)

Toto chybové hlásenie naznačuje, že existujú cenové záznamy, ktoré boli predtým nastavené pre dimenziu, ktorá je vypnutá. Všetky záznamy **Cena roly** a **Prirážka k cene roly**, ktoré odkazujú na dimenziu, musia byť odstránené pred tým, ako môže byť použiteľnosť na **Nie**. Toto pravidlo sa vzťahuje na dimenzie cien, ktoré nie sú predpripravené, a na všetky vlastné dimenzie cien, ktoré ste mohli vytvoriť. Dôvodom tohto overenia je, že každý **Cena roly** musí mať jedinečnú kombináciu dimenzií. Napríklad na cenníku s názvom **US Cost Rates 2018** máte nasledovné riadky **Cena roly**. 

| Štandardný názov         | Organizačná jednotka    |Jednotka   |Cena  |Mena  |
| -----------------------|-------------|-------|-------|----------|
| Systémový inžinier|Contoso – USA|Hodina| 100|USD|
| Vyšší systémový inžinier|Contoso – USA|Hodina| 150| USD|


Keď vypnete **Štandardný názov** ako cenovú dimenziu a nástroj na určovanie cien vyhľadáva cenu, použije sa iba hodnota **Organizačná jednotka** z kontextu vstupu. Ak je **Organizačná jednotka** vstupného kontextu „Contoso US“, výsledok nebude určujúci, pretože sa budú zhodovať obidva riadky. Ak chcete predísť tomuto scenáru, pri záznamoch **Cena roly** systém overuje, či je kombinácia dimenzií jedinečná. Ak je rozmer vypnutý po vytvorení záznamov **Cena roly**, toto obmedzenie môže byť porušené. Preto je potrebné, aby ste pred vypnutím dimenzie vymazali všetky riadky **Ceny roly** a **Prirážka k cene roly**, ktoré majú vyplnenú hodnotu dimenzie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]