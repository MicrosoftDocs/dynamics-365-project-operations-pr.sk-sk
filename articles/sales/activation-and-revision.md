---
title: Aktivujte a upravte cenovú ponuku projektu
description: Tento článok poskytuje informácie o aktivácii a úprave cenových ponúk v Microsoft Dynamics 365 Project Operations.
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
# <a name="activate-and-revise-a-project-quote"></a>Aktivujte a upravte cenovú ponuku projektu

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Funkcie aktivácie a revízie vám pomôžu sledovať vytváranie verzií pre projektové ponuky počas fáz odhadu a vyjednávania. Keď je koncept ponuky aktivovaný, stane sa len na čítanie.

Funkcie aktivácie a revízie vám umožňujú vykonávať nasledujúce úlohy:

- Vyhrajte alebo prehrajte ponuky až po aktivácii.
- Upravte cenovú ponuku, aby ste vykonali zmeny existujúcej cenovej ponuky alebo vytvorili novú verziu.

> [!NOTE]
> Keď je funkcia aktivácie a revízie cenových ponúk povolená, nie je možné ju vypnúť.

Ak chcete zapnúť možnosť aktivovať a revidovať cenové ponuky na základe projektu, postupujte podľa týchto krokov.

1. Ísť do **nastavenie** \> **Parametre**.
1. Otvor **Parametre** záznam.
1. Na paneli akcií na **Ovládanie funkcií** kartu, vyberte **Povoliť aktiváciu a revíziu cenových ponúk**.
1. V dialógovom okne potvrdenia kliknite na tlačidlo **OK**.
1. Po chvíli obnovte prehliadač. Teraz by mali byť dostupné možnosti aktivácie a revízie. Budete vedieť, že tieto možnosti boli povolené, ak **Povoliť aktiváciu a revíziu cenových ponúk** tlačidlo sa už na paneli akcií nezobrazuje.

## <a name="activating-a-quote"></a>Aktivácia cenovej ponuky

Po aktivácii funkcie na aktiváciu a revíziu cenových ponúk, **Zavrieť ponuku ako vyhral** a **Zavrieť citát ako stratený** Tlačidlá na table akcií nie sú dostupné pre ponuky návrhov projektov. Sú dostupné až po aktivácii cenovej ponuky.

Aktivácia predstavuje fázu v procese cenovej ponuky, keď chcete zabrániť ďalším zmenám ponuky. V tejto fáze sa cenová ponuka odošle na internú kontrolu alebo zákazníkovi.

The **Zavrieť ponuku ako vyhral** a **Zavrieť citát ako stratený** tlačidlá na paneli akcií sú dostupné pre aktivované úvodzovky. V závislosti od výsledku internej alebo zákazníckej kontroly môžete použiť jedno z týchto tlačidiel na uzavretie aktivovanej ponuky. Výberom môžete uskutočniť rokovania a zmeny aktivovaných cenových ponúk **Revidovať citát**.

## <a name="revising-a-quote"></a>Revízia cenovej ponuky

Ak musíte vykonať zmeny v aktivovanej cenovej ponuke, vyberte **Revidovať citát**. Citácia je uzavretá a **revidované** je použitý kód príčiny. Potom sa vytvorí nová ponuka, ktorá má rovnaké ID a zvýšené číslo revízie. Všetky podrobnosti z pôvodnej ponuky sa skopírujú do novej ponuky. Nová cenová ponuka je v stave konceptu a možno ju podľa potreby upraviť.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
