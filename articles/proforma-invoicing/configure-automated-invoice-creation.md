---
title: Konfigurácia automatického vytvárania faktúr
description: Táto téma poskytuje informácie o spôsobe konfigurácie systému na automatické generovanie faktúr.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 295c3b099c9670c930fb2ba2fd208be63a77217f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122452"
---
# <a name="configure-automatic-invoice-creation"></a>Konfigurácia automatického vytvárania faktúr

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_


Vykonajte nasledujúce kroky na konfiguráciu automatického vytvárania faktúr v aplikácii Dynamics 365 Project operations.

1. Prejdite do časti **Nastavenia** > **Dávkové úlohy**.
2. Vytvorte dávkovú úlohu a pomenujte ju **Vytvorenie faktúr Project Operations**. Názov dávkovej úlohy musí obsahovať slová „vytvorenie faktúr“.
3. V poli **Typ úlohy** vyberte položku **Žiadne**. Štandardne je **frekvencia denne** a **je aktívne** možnosti nastavená na **Áno.**
4. Vyberte **spustiť pracovný postup**. V dialógovom okne **vyhľadať záznam** sa zobrazia tri pracovné postupy:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Vyberte **ProcessRunCaller** a potom **pridať**.
6. V ďalšom dialógovom okne kliknite na **OK**. Pracovný postup **spánok** je nasledovaný pracovným postupom **proces**.

  > [!NOTE]
  > Môžete tiež vybrať **processrunner** v kroku 5. Potom, keď vyberiete **OK**, pracovný postup **proces** je nasledovaný pracovným postupom **spánok**.

Pracovné postupy **processruncaller** a **processrunner** vytvárajú faktúry. **ProcessRunCaller** volá **processrunner**. **ProcessRunner** je pracovný postup, ktorý skutočne vytvára faktúry. Prechádza všetky riadky zmluvy, pre ktoré musia byť vytvorené faktúry, a vytvára faktúry pre tieto riadky. Ak chcete určiť riadky zmluvy, pre ktoré musia byť vytvorené faktúry, úloha sa pozerá na dátumy spustenia faktúry pre riadky zmluvy. Ak riadky zmluvy patriace do jednej zmluvy majú rovnaký dátum spustenia faktúry, transakcie sa skombinujú do jednej faktúry, ktorá má dva riadky faktúry. Ak neexistujú žiadne transakcie na vytvorenie faktúr, úloha vynechá vytvorenie faktúry.

Po dokončení **procesrunnera**, sa volá **processruncaller**, ktorý poskytuje čas ukončenia a je uzavretý. **ProcessRunCaller** potom spustí časovač, ktorý beží 24 hodín od zadaného času ukončenia. Na konci časovača, je **processruncaller** uzavretý.

Dávková úloha pre vytváranie faktúr je opakujúca sa úloha. Ak je táto dávková úloha spustená mnohokrát, sú vytvorené viaceré inštancie úlohy a spôsobujú chyby. Preto by ste mali spustiť dávkový proces len raz, a mali by ste ho reštartovať iba v prípade, že prestane fungovať.

> [!NOTE]
> Hromadná fakturácia sa spustí iba pre riadky zmlúv projektu, ktoré sú konfigurované podľa plánov faktúr. Riadok zmluvy s metódou fakturácie podľa fixnej ceny musí mať nakonfigurované medzníky. V riadku zmluvy projektu s metódou fakturácie podľa času a materiálu bude potrebné zostaviť plán fakturácie založený na dátume. To isté platí pre riadok zmluvy založený na projekte.     
