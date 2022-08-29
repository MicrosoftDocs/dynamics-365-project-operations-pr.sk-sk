---
title: Možnosti subdodávateľskej zmluvy pre členov projektového tímu
description: Tento článok vysvetľuje možnosti subdodávok pre členov projektového tímu v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5e0955d58365a4ecbe1c053882736f196758816e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261626"
---
# <a name="subcontracting-options-for-project-team-members"></a>Možnosti subdodávateľskej zmluvy pre členov projektového tímu

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

V Microsofte Dynamics 365 Project Operations, môžete vyhodnotiť možnosti subdodávok dostupné pre jedného alebo viacerých členov projektového tímu. Dostupné možnosti subdodávok vám umožňujú:

- Vytvorte novú subdodávku a/alebo vytvorte nové riadky v existujúcej subdodávke pre vybratých členov projektového tímu. 
- Rezerva voči už existujúcej subdodávke a subdodávke. 

Môžete si vybrať z dostupných možností subdodávok pre všeobecných členov projektového tímu alebo si vybrať z členov projektového tímu, ktorí boli obsadení menovaným zdrojom, ktorým je zmluvný pracovník. 

Nie sú k dispozícii žiadne možnosti subdodávok pre nasledovné:

- Členovia projektového tímu, ktorí boli obsadení zamestnancom. 
- Členovia projektového tímu, ktorí sú už priradení k subdodávke a subdodávke. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subdodávky člena projektového tímu bez personálu

Ak chcete skontrolovať a vybrať si z dostupných možností subdodávok pre bežného člena projektového tímu alebo člena projektového tímu bez personálu, postupujte podľa týchto krokov:

1. Vyberte jeden alebo viac záznamov o členovi projektového tímu, kde je zdrojom všeobecný zdroj.
2. Uistite sa, že žiadny z vybratých záznamov členov projektového tímu už nie je zadaný subdodávateľom. 
3. Vyberte **Možnosti subdodávok** na podmriežke členov projektového tímu. The **Možnosti subdodávok** otvorí sa dialógové okno. 
4. Ak ste v kroku 1 vybrali iba jeden záznam člena projektového tímu, budú k dispozícii nasledujúce možnosti:
    - Vytvorte nové subdodávateľské linky. 
    - Rezervovať na existujúcu subdodávku Ak ste v kroku 1 vybrali viacero záznamov členov projektového tímu, jedinou dostupnou možnosťou je vytvorenie nových riadkov subdodávok.
5. Možnosť rezervácie voči existujúcej subdodávke vám umožňuje vybrať subdodávku a subdodávku, voči ktorej chcete rezervovať. Pri výbere subdodávateľskej linky na rezervovanie kapacity by ste sa mali uistiť, že vybraná subdodávateľská linka je časovo obmedzená a že rola požadovaná na členovi projektového tímu sa zhoduje s rolou, ktorá bola zakúpená na subdodávateľskej linke.
6. Keď vyberiete vytvorenie nových riadkov subdodávok pre členov projektového tímu, systém vám umožní vybrať subdodávku, pre ktorú chcete vytvoriť tieto riadky. Subdodávka, ktorú vyberiete na vytvorenie nových riadkov, by mala byť v **Návrh** postavenie. S touto voľbou na vytvorenie nových riadkov subdodávok pre vybraných členov projektového tímu systém vytvorí jeden riadok subdodávok na čas pre každého člena projektového tímu. Rola, hodiny a dátumy sa skopírujú od člena projektového tímu do každého riadku subdodávky, ktorý sa vytvorí. 
7. Keď je generický člen tímu spojený so subdodávkou a subdodávateľskou líniou, **Typ pracovníka** pole v riadku všeobecného člena tímu sa aktualizuje na **Pracovník na dohodu** a **Platnosť subdodávky** hodnota bude nastavená na **Platné**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subdodávky s personálne obsadeným členom projektového tímu

Rovnako ako všeobecní členovia tímu alebo členovia tímu bez personálu, môžete si tiež zobraziť možnosti subdodávok pre člena projektového tímu s personálom, pokiaľ je člen tímu s pracovníkmi zmluvný pracovník. Ak chcete skontrolovať a vybrať si z dostupných možností subdodávok pre zamestnanca alebo menovaného člena projektového tímu, postupujte takto:

1. Vyberte jeden alebo viacero záznamov členov projektového tímu, kde je zdrojom pomenovaný zmluvný pracovník.
2. Uistite sa, že žiadny z vybratých záznamov členov projektového tímu už nie je zadaný subdodávateľom. 
3. Vyberte **Možnosti subdodávok** na podmriežke členov projektového tímu. The **Možnosti subdodávok** otvorí sa dialógové okno. 
4. Ak ste v kroku 1 vybrali iba jeden záznam člena projektového tímu, budú k dispozícii nasledujúce možnosti:
      - Vytvorte nové subdodávateľské linky.
      - Rezerva voči existujúcej subdodávke.
  Ak ste v kroku 1 vybrali viacero záznamov členov projektového tímu, jedinou dostupnou možnosťou je vytvorenie nových riadkov subdodávok.
5. Možnosť rezervácie voči existujúcej subdodávke vám umožňuje vybrať subdodávku a subdodávku, voči ktorej chcete rezervovať. Pri výbere subdodávateľskej linky na rezervovanie kapacity by ste mali zabezpečiť nasledovné:
      - Vybraná subdodávateľská linka je na čas. 
      - Požadovaná rola člena projektového tímu sa zhoduje s rolou, ktorá bola zakúpená na linke subdodávok. 
      - Dodávateľ, ku ktorému je priradený zmluvný pracovník, je rovnaký ako dodávateľ v subdodávke.
6. Keď vyberiete vytvorenie nových riadkov subdodávok pre členov projektového tímu, systém vám umožní vybrať subdodávku, pre ktorú chcete vytvoriť tieto riadky. Pri tejto možnosti by ste sa mali uistiť, že dodávateľ, ku ktorému patrí zmluvný pracovník, je rovnaký ako dodávateľ v subdodávke. 
7. Subdodávka, ktorú vyberiete na vytvorenie nových riadkov, by mala byť v **Návrh** postavenie. S touto voľbou na vytvorenie nových riadkov subdodávok pre vybraných členov projektového tímu systém vytvorí jeden riadok subdodávok na čas pre každého člena projektového tímu. Rola, hodiny a dátumy sa skopírujú od člena projektového tímu do každého riadku subdodávky, ktorý sa vytvorí.  
8. Keď je pomenovaný člen tímu priradený k subdodávke a subdodávateľskej linke, **Typ pracovníka** pole v riadku s názvom člena tímu sa aktualizuje na **Pracovník na dohodu** a **Platnosť subdodávky** hodnota bude nastavená na **Platné**.

## <a name="re-costing-subcontractor-assignments"></a>Preúčtovanie úloh subdodávateľov

Keď je člen projektového tímu (všeobecný alebo pomenovaný) prepojený so subdodávateľskými linkami pomocou **Možnosti subdodávok** dialóg, všetky priradenia k úlohám, ktoré má člen tímu, budú prepočítané na základe nákupného cenníka priloženého k subdodávke. Na **Odhady** kartu na **Podrobnosti projektu** vyberte stránku **Aktualizujte ceny** zobrazíte aktualizované ceny a/alebo kalkulácie vyplývajúce z rozhodnutia uzavrieť subdodávku.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
