---
title: Nastavte prevod meny na výpočet predajných cien z nákladových sadzieb
description: Tento článok vysvetľuje, ako nakonfigurovať správanie pri prevode meny, ktoré sa použije v Microsoft Dynamics 365 Project Operations keď sa predajné transakcie generujú z nákladových transakcií.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816700"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Nastavte prevod meny na výpočet predajných cien z nákladových sadzieb

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

V Microsoft Dynamics 365 Project Operations je možné predajné ceny pre kategórie výdavkov nastaviť ako číselné hodnoty alebo ich možno nastaviť tak, aby sa vypočítali na základe vynaložených nákladov.

Keď sú nastavené na výpočet na základe vzniknutých nákladov, sú k dispozícii nasledujúce možnosti:

- V rámci nákladov
- Zvýšte percento nákladov

V scenároch, v ktorých sú náklady vynaložené v mene, ktorá sa líši od meny predaja pre projektový kontrakt, je potrebný prevod meny na výpočet predajnej ceny na základe nákladov.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Správanie pri prevode meny, ktoré používa natívne Dataverse výmenné kurzy

Operácie projektu štandardne používajú výmenné kurzy, ktoré sú uložené v tabuľke Mena v Dataverse. Ak chcete nakonfigurovať operácie projektu na používanie natívnych výmenných kurzov na výpočet predajných cien z nákladov, postupujte podľa týchto krokov.

1. Prejdite na **Operácie projektu \> Nastavenia \> Parametre**.
1. Otvorte stránku s podrobnosťami **Parametre projektu** .
1. Nastavte pole **Logika konverzie meny** na prázdnu hodnotu.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Správanie pri prevode meny, ktoré používa výmenné kurzy z finančných a prevádzkových aplikácií

Výmenné kurzy v tabuľke meny, ktorá je natívne dostupná v Dataverse , nie sú platné. Preto nemusia byť vždy prispôsobené požiadavkám, ktoré máte na výpočet predajných cien z nákladových sadzieb.

Výmenné kurzy z prostredia financií a operácií môžete použiť na výpočet predajnej ceny v predajnej mene z nákladového kurzu v nákladovej mene. Ak chcete nakonfigurovať toto správanie pri konverzii meny, postupujte podľa týchto krokov.

1. Na stránke **Parametre projektu**  pridajte pole **Logika prevodu meny** . Potom prispôsobenie uložte a publikujte.
1. Prejdite na **Operácie projektu \> Nastavenia \> Parametre**.
1. Otvorte stránku s podrobnosťami **Parametre projektu** . 
1. V poli **Správanie konverzie meny** nastavte na hodnotu **Rozšírené s záložným nastavením na predvolené**.
1. Udeľte  **používateľovi aplikácie s dvojitým zápisom** rola zabezpečenia **Globálne čítanie**  týmto tabuľkám:

    - msdyn\_ zmenárne
    - msdyn\_ výmenné páry
    - msdyn\_ typy výmenných kurzov

1. Vo svojom finančnom a prevádzkovom prostredí spustite nasledujúce mapy s duálnym zápisom s počiatočnou synchronizáciou:

    - Typ výmenného kurzu (msdyn\_ typy výmenných kurzov)
    - Menový pár s výmenným kurzom (msdyn\_ páry výmenných kurzov)
    - Výmenné kurzy CDS (výmenné kurzy msdyn\_)

Po dokončení týchto zmien sprístupní duálny zápis výmenné kurzy z finančného a prevádzkového prostredia v Dataverse. Projektové operácie potom použijú tieto výmenné kurzy na konverziu nákladových kurzov na menu predaja zmluvy.

> [!NOTE]
> Toto správanie pri prevode meny sa vzťahuje len na výpočet predajných cien z nákladových sadzieb. Nepoužije sa na všeobecný výpočet hodnôt základnej meny. Hodnoty základnej meny budú vždy používať natívne Dataverse výmenné kurzy bez ohľadu na to, či dokončíte tento postup.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
