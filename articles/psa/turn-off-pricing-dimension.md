---
title: Vypnutie cenovej dimenzie
description: Táto téma ukazuje, ako nastaviť dimenzie cien v riešení Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
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
ms.openlocfilehash: 9f690dfdb40e962ef329f323716f3f755493805d764dbfaa2d4f9d042231cee7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006805"
---
# <a name="turn-off-a-pricing-dimension"></a>Vypnutie cenovej dimenzie

[!include [banner](../includes/psa-now-project-operations.md)]

Možno budete musieť skontrolovať a aktualizovať svoje cenové stratégie každých niekoľko rokov. Všetky aktualizácie, ktoré vykonáte, môžu vyžadovať vypnutie existujúcej dimenzie cien a vytvorenie novej. Napríklad, možno ste predtým oceňovali na základe **Roly**, ale teraz ste sa rozhodli pre cenu podľa **pracovných skúseností**. To môže vyžadovať vypnutie **Role** ako cenovej dimenzie a vytvorenie **pracovných skúseností** ako novej cenovej dimenzie. 

Vypnutie cenovej dimenzie, bez ohľadu na to, či je predpripravená alebo vlastná, možno vykonať nastavením možnosti **Vzťahuje sa na náklady** a **Vzťahuje sa na predaj** polia dimenzie cien na **Nie**.

Avšak, keď to urobíte, môže sa zobraziť nasledujúce chybové hlásenie.

![Chyba obchodného procesu pravdepodobne pri vypnutí cenovej dimenzie.](media/Business-Process-Error.png)


Toto chybové hlásenie naznačuje, že existujú cenové záznamy, ktoré boli predtým nastavené pre dimenziu, ktorá je vypnutá. Všetky záznamy **Cena roly** a **Prirážka k cene roly**, ktoré odkazujú na dimenziu, musia byť odstránené pred tým, ako môže byť použiteľnosť na **Nie**. Toto pravidlo sa vzťahuje na dimenzie cien, ktoré nie sú predpripravené, a na všetky vlastné dimenzie cien, ktoré ste mohli vytvoriť. Dôvodom tohto overenia je, že Project Service má obmedzenie, aby každý záznam **Cena roly** mal jedinečnú kombináciu dimenzií. Napríklad na cenníku s názvom **US Cost Rates 2018** máte nasledovné riadky **Cena roly**. 

| Štandardný názov         | Organizačná jednotka    |Jednotka   |Cena  |Mena  |
| -----------------------|-------------|-------|-------|----------|
| Systémový inžinier|Contoso – USA|Hodina| 100|USD|
| Vyšší systémový inžinier|Contoso – USA|Hodina| 150| USD|


Keď vypnete **štandardný názov** ako cenový rozmer a nástroj na určovanie cien Project Service vyhľadáva cenu, použije sa iba hodnota **Organizačná jednotka** z kontextu vstupu. Ak je **Organizačná jednotka** vstupného kontextu „Contoso US“, výsledok nebude určujúci, pretože sa budú zhodovať obidva riadky. Ak chcete predísť tomuto scenáru, pri záznamoch **Cena roly**, Project Service overuje, že kombinácia dimenzií je jedinečná. Ak je rozmer vypnutý po vytvorení záznamov **Cena roly**, toto obmedzenie môže byť porušené. Preto je potrebné, aby ste pred vypnutím dimenzie vymazali všetky riadky **Ceny roly** a **Prirážka k cene roly**, ktoré majú vyplnenú hodnotu dimenzie.



[!INCLUDE[footer-include](../includes/footer-banner.md)]