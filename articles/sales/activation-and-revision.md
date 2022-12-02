---
title: Aktivácia a revízia projektovej cenovej ponuky
description: Tento článok poskytuje informácie o aktivácii a revízii cenových ponúk v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410394"
---
# <a name="activate-and-revise-a-project-quote"></a>Aktivácia a revízia projektovej cenovej ponuky

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Funkcie aktivácie a revízie vám pomôžu sledovať vytváranie verzií pre projektové cenové ponuky počas fáz odhadu a vyjednávania. Keď je koncept cenovej ponuky aktivovaný, zmení sa len na čítanie.

Funkcie aktivácie a revízie vám umožňujú vykonávať nasledujúce úlohy:

- Získať alebo stratiť cenové ponuky až po aktivácii.
- Revidovať cenovú ponuku, aby ste vykonali zmeny existujúcej cenovej ponuky alebo vytvorili novú verziu.

> [!NOTE]
> Keď je funkcia aktivácie a revízie cenových ponúk povolená, nie je možné ju vypnúť.

Ak chcete zapnúť možnosť aktivovať a revidovať cenové ponuky na základe projektu, postupujte podľa týchto krokov.

1. Prejdite do časti **Nastavenia** \> **Parametre**.
1. Otvorte záznam **Parametre**.
1. Na table akcií na karte **Ovládanie funkcií** vyberte **Povoliť aktiváciu a revíziu cenových ponúk**.
1. V dialógovom okne potvrdenia kliknite na tlačidlo **OK**.
1. Po chvíli obnovte prehliadač. Teraz by mali byť dostupné možnosti aktivácie a revízie. Budete vedieť, že tieto možnosti boli povolené, ak sa tlačidlo **Povoliť aktiváciu a revízie cenových ponúk** nebude viac zobrazovať na table akcií.

## <a name="activating-a-quote"></a>Aktivácia cenovej ponuky

Po aktivácii funkcie na aktiváciu a revíziu cenových ponúk nebudú tlačidlá **Uzavrieť cenovú ponuku ako využitú** a **Uzavrieť cenovú ponuku ako nevyužitú** dostupné pre koncepty cenových ponúk projektov. Sú dostupné až po aktivácii cenovej ponuky.

Aktivácia predstavuje etapu v procese cenovej ponuky, keď chcete zabrániť ďalším zmenám cenovej ponuky. V tejto etape sa cenová ponuka odošle na internú kontrolu alebo zákazníkovi.

Tlačidlá **Uzavrieť cenovú ponuku ako využitú** a **Uzavrieť cenovú ponuku ako nevyužitú** na table Akcia sú dostupné pre aktivované cenové ponuky. V závislosti od výsledku internej alebo zákazníckej kontroly môžete použiť jedno z týchto tlačidiel na uzavretie aktivovanej cenovej ponuky. Výberom možnosti **Revidovať cenovú ponuku** môžete uskutočniť rokovania a zmeny aktivovaných cenových ponúk.

## <a name="revising-a-quote"></a>Revízia cenovej ponuky

Ak musíte vykonať zmeny v aktivovanej cenovej ponuke, vyberte **Revidovať cenovú ponuku**. Cenová ponuka je uzavretá a je použitý kód dôvodu **revidované**. Potom sa vytvorí nová ponuka, ktorá má rovnaké ID a zvýšené číslo revízie. Všetky podrobnosti z pôvodnej cenovej ponuky sa skopírujú do novej cenovej ponuky. Nová cenová ponuka je v stave konceptu a možno ju podľa potreby upraviť.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
