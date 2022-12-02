---
title: Možnosti subdodávateľskej zmluvy pre členov projektového tímu
description: Tento článok vysvetľuje možnosti subdodávateľských zmlúv pre členov projektového tímu v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522298"
---
# <a name="subcontracting-options-for-project-team-members"></a>Možnosti subdodávateľskej zmluvy pre členov projektového tímu

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

V Microsoft Dynamics 365 Project Operations môžete vyhodnotiť možnosti subdodávateľských zmlúv dostupné pre jedného alebo viacerých členov projektového tímu. Dostupné možnosti subdodávateľských zmlúv vám umožňujú:

- Vytvoriť novú subdodávateľskú zmluvu a/alebo vytvoriť nové riadky v existujúcej subdodávateľskej zmluve pre vybratých členov projektového tímu. 
- Rezervovať voči už existujúcej subdodávateľskej zmluve a riadku subdodávateľskej zmluvy. 

Môžete si vybrať z dostupných možností subdodávateľských zmlúv pre všeobecných členov projektového tímu alebo si vybrať z členov projektového tímu, ktorí boli obsadení menovaným zdrojom, ktorým je zmluvný pracovník. 

Nie sú k dispozícii žiadne možnosti subdodávateľských zmlúv pre:

- Členov projektového tímu, ktorí boli obsadení zamestnancom. 
- Členov projektového tímu, ktorí sú už priradení k subdodávateľskej zmluve a riadku subdodávateľskej zmluvy. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subdodávateľská zmluva člena projektového tímu bez personálneho obsadenia

Ak chcete skontrolovať a vybrať si z dostupných možností subdodávateľských zmlúv pre bežného člena projektového tímu alebo člena projektového tímu bez personálu, postupujte podľa týchto krokov:

1. Vyberte jeden alebo viac záznamov o členovi projektového tímu, kde je zdrojom všeobecný zdroj.
2. Uistite sa, že žiadny z vybratých záznamov členov projektového tímu už nie je vedený ako subdodávateľ. 
3. Vyberte **Možnosti subdodávateľskej zmluvy** na podmriežke členov projektového tímu. Otvorí sa dialógové okno **Možnosti subdodávateľskej zmluvy**. 
4. Ak ste v kroku 1 vybrali iba jeden záznam člena projektového tímu, budú k dispozícii nasledujúce možnosti:
    - Vytvorte nové riadky subdodávateľskej zmluvy. 
    - Rezervovať voči existujúcej subdodávateľskej zmluve Ak ste v kroku 1 vybrali viacero záznamov členov projektového tímu, jedinou dostupnou možnosťou je vytvorenie nových riadkov subdodávateľskej zmluvy.
5. Možnosť rezervácie voči existujúcemu riadku subdodávateľskej zmluvy vám umožňuje vybrať subdodávateľskú zmluvu a riadok subdodávateľskej zmluvy, voči ktorej chcete rezervovať. Pri výbere riadku subdodávateľskej zmluvy na rezervovanie kapacity by ste sa mali uistiť, že vybraný riadok subdodávateľskej zmluvy je časovo obmedzený a že rola požadovaná od člena projektového tímu sa zhoduje s rolou, ktorá bola zakúpená na riadku subdodávateľskej zmluvy.
6. Keď vyberiete vytvorenie nových riadkov subdodávateľskej zmluvy pre členov projektového tímu, systém vám umožní vybrať subdodávateľskú zmluvu, pre ktorú chcete vytvoriť tieto riadky. Subdodávateľská zmluva, ktorú vyberiete na vytvorenie nových riadkov, by mala byť v stave **Koncept**. S touto možnosťou vytvorenia nových riadkov subdodávateľskej zmluvy pre vybraných členov projektového tímu systém vytvorí jeden riadok subdodávateľskej zmluvy pre čas pre každého člena projektového tímu. Rola, hodiny a dátumy sa skopírujú od člena projektového tímu do každého riadku subdodávateľskej zmluvy, ktorý sa vytvorí. 
7. Keď je všeobecný člen tímu spojený so subdodávateľskou zmluvou a riadkom subdodávateľskej zmluvy, pole **Typ pracovníka** v riadku všeobecného člena tímu sa aktualizuje na **Zmluvný pracovník** a hodnota **Platnosť subdodávateľskej zmluvy** bude nastavená na **Platné**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subdodávka člena projektového tímu s personálnym obsadením

Rovnako ako všeobecní členovia tímu alebo členovia tímu bez personálneho obsadenia, môžete si tiež zobraziť možnosti subdodávateľských zmlúv pre člena projektového tímu s personálnym obsadením, pokiaľ je člen tímu s personálnym obsadením zmluvným pracovníkom. Ak chcete skontrolovať a vybrať si z dostupných možností subdodávateľských zmlúv pre člena projektového tímu s personálnym obsadením alebo pre menovaného člena projektového tímu, postupujte podľa týchto krokov:

1. Vyberte jeden alebo viac záznamov o členovi projektového tímu, kde je zdrojom menovaný zmluvnú pracovník.
2. Uistite sa, že žiadny z vybratých záznamov členov projektového tímu už nie je vedený ako subdodávateľ. 
3. Vyberte **Možnosti subdodávateľskej zmluvy** na podmriežke členov projektového tímu. Otvorí sa dialógové okno **Možnosti subdodávateľskej zmluvy**. 
4. Ak ste v kroku 1 vybrali iba jeden záznam člena projektového tímu, budú k dispozícii nasledujúce možnosti:
      - Vytvorte nové riadky subdodávateľskej zmluvy.
      - Vykonajte rezerváciu vzhľadom na existujúcu subdodávateľskú zmluvu.
  Ak ste v kroku 1 vybrali viacero záznamov členov projektového tímu, jedinou dostupnou možnosťou je vytvorenie nových riadkov subdodávateľskej zmluvy.
5. Možnosť rezervácie voči existujúcemu riadku subdodávateľskej zmluvy vám umožňuje vybrať subdodávateľskú zmluvu a riadok subdodávateľskej zmluvy, voči ktorej chcete rezervovať. Pri výbere riadka subdodávateľskej zmluvy na rezervovanie kapacity by ste mali zabezpečiť nasledovné:
      - Vybraný riadok subdodávateľskej zmluvy je pre čas. 
      - Požadovaná rola člena projektového tímu sa zhoduje s rolou, ktorá bola zakúpená na riadku subdodávateľskej zmluvy. 
      - Dodávateľ, ku ktorému je priradený zmluvný pracovník, je rovnaký ako dodávateľ v subdodávateľskej zmluve.
6. Keď vyberiete vytvorenie nových riadkov subdodávateľskej zmluvy pre členov projektového tímu, systém vám umožní vybrať subdodávateľskú zmluvu, pre ktorú chcete vytvoriť tieto riadky. Pri tejto možnosti by ste sa mali uistiť, že dodávateľ, ku ktorému patrí zmluvný pracovník, je rovnaký ako dodávateľ v subdodávateľskej zmluve. 
7. Subdodávateľská zmluva, ktorú vyberiete na vytvorenie nových riadkov, by mala byť v stave **Koncept**. S touto možnosťou vytvorenia nových riadkov subdodávateľskej zmluvy pre vybraných členov projektového tímu systém vytvorí jeden riadok subdodávateľskej zmluvy pre čas pre každého člena projektového tímu. Rola, hodiny a dátumy sa skopírujú od člena projektového tímu do každého riadku subdodávateľskej zmluvy, ktorý sa vytvorí.  
8. Keď je menovaný člen tímu spojený so subdodávateľskou zmluvou a riadkom subdodávateľskej zmluvy, pole **Typ pracovníka** v riadku menovaného člena tímu sa aktualizuje na **Zmluvný pracovník** a hodnota **Platnosť subdodávateľskej zmluvy** bude nastavená na **Platné**.

## <a name="re-costing-subcontractor-assignments"></a>Preúčtovanie úloh subdodávateľov

Keď je člen projektového tímu (všeobecný alebo menovaný) prepojený s riadkami subdodávateľskej zmluvy pomocou dialógového okna **Možnosti subdodávateľskej zmluvy**, všetky priradenia k úlohám, ktoré má člen tímu, budú prepočítané na základe nákupného cenníka priloženého k subdodávateľskej zmluve. Na karte **Odhady** na stránke **Podrobnosti projektu** vyberte tlačidlo **Aktualizovať ceny** a zobrazíte aktualizované ceny a/alebo kalkulácie vyplývajúce z rozhodnutia uzavrieť subdodávateľskú zmluvu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
