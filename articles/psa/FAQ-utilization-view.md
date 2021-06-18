---
title: Zobrazte fakturovateľné využívanie zdrojov
description: Táto téma poskytuje informácie o zobrazení využitia zdrojov.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e1c123854209b3cb5c310e3bbcb242c9219279a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992853"
---
# <a name="view-chargeable-utilization-for-resources"></a>Zobrazte fakturovateľné využívanie zdrojov

[!include [banner](../includes/psa-now-project-operations.md)]
 
**Zobrazenie využitia** na stránke **využitie zdrojov Project Service** zobrazuje účtovateľné využitie pre každý rezervovateľný zdroj. Pretože je zobrazenie založené na tabule plánovania, vďaka čomu tu nájdete veľa rovnakých funkcií.

> ![Snímka obrazovky zobrazenia využitia](media/FAQ-utilization-1.png)
 

Výpočet spoplatneného využitia funguje nasledovne:

   Spoplatnené využitie = (Spoplatnená skutočná kapacita hodín) / (kapacita zdroja)

Bunky predstavujú vypočítané spoplatnené využívanie za obdobie vybrané na zobrazenie (dni, týždne alebo mesiace).

Farby v každej bunke zobrazujú spoplatnené využívanie zdroja v porovnaní s ich cieľovým spoplatneným využitím. 

Cieľové využitie môžete nastaviť na predvolené roly zdroja, alebo samotných individuálnych zdrojov. Pri výpočte sa zohľadňuje najprv jednotlivý cieľ, potom predvolená rola zdroja.

## <a name="set-target-on-a-resource"></a>Nastaviť cieľ na zdroj

1. Prejdite do **Zdroje** \> **Zdroje**. 
2. Kliknite na zdroj na otvorenie záznamu. 
3. Na karte **Project Service** môžete nastaviť cieľové využitie zdroja.

> ![Snímka obrazovky využitia karty Project Service na nastavenie cieľového využívania](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Nastavenie cieľového využitia na rolu

1. Prejdite do **Zdroje** \> **role zdrojov**. 
2. Kliknite na rola a otvorte záznam. 
3. Nastavte cieľové využitie roly.

> ![Snímka obrazovky používania Rol zdroja na stanovenie cieľového využitia](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Výpočet fakturovateľných využití zdrojov

Pre výpočet fakturovateľných využití zdroja, budete musieť splniť niektoré predpoklady. 

### <a name="set-default-role-for-individual-resource"></a>Nastaviť predvolenú rolu pre jednotlivé zdroje

Najprv je potrebné, aby bolo cieľové využitie nastavené buď na individuálnom zdroji alebo v rámci rolí zdroja. Ak využívate roly zdroja pre ciele, každý jednotlivý zdroj musí mať predvolenú rolu. 

1. Nastavte to v ponuke **Zdroje** a potom \> **Zdroje**. 
2. Vyberte zdroj, otvorte záznam a potom vyberte kartu **Project Service**. 
3. V mriežke **rolí zdroja** sa presvedčte, či je pre prostriedok jedna rola a je to **predvolená hodnota** nastavená na hodnotu **Áno.**
 
### <a name="change-billing-type-for-resource-role"></a>Zmeňte typ fakturácie pre túto rolu zdroja.

Role prostriedkov je potrebné nastaviť tak, aby mali typ fakturácie **Účtovateľné**. 

1. Prejdite do **Zdroje** \> **role zdrojov**. 
2. Otvorte záznam, ktorý chcete aktualizovať a následne nastavte predvolený typ fakturácie na **Fakturovateľné**.

### <a name="set-working-hours-for-resource-role"></a>Nastavenie pracovnej doby pre role zdrojov
 
Zdroj musí mať na výpočet kapacity pracovné hodiny. 

1. Prejdite do **Zdroje** \> **Zdroje**. 
2. Kliknutím na zdroj otvorte záznam a následne kliknite na možnosť **Zobraziť pracovnú dobu**. 
3. Môžete hromadne aktualizovať zoznam zdrojov priradením **šablóny pracovná doba** zo **zoznamu zdrojov**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Riešenie problémov účtovateľných skutočných údajov hodín

Účtovateľné skutočné údaje hodín sú získavané od entity **skutočných hodnôt**. Skutočné hodnoty fakturačné typu **zdaniteľné** sú zahrnuté do výpočtu a z tohto dôvodu musíte mať projekty so skutočnými hodnotami, ktoré sú zdaniteľné.

Ak nevidíte účtovateľné využitie, tu sú niektoré veci môžete skontrolovať:

- Zdroj má zadefinované pracovné hodiny pre kapacitu.
- Prostriedok má buď jednotlivo definované využitie, alebo má priradenú predvolenú rolu. Rola má zadefinované cieľové využitie.
- Skutočné hodnoty majú fakturačný druh **zdaniteľné** na obdobie pre ktoré očakávate využitie výpočtu. Skontrolujte nasledujúce, ak ste videli skutočné údaje s fakturáciou typy iné než zdaniteľná:

  - Úloha na skutočné má predvolené fakturačné typu niečo iné než zdaniteľná.
  - Úloha na riadku zmluvy projektu podporu projektu bol nastavený non-zdaniteľné.
  - Projekt nemá priradený riadok zmluvy.



[!INCLUDE[footer-include](../includes/footer-banner.md)]