---
title: Správa príležitostí založených na projekte
description: Tento článok poskytuje informácie o tom, ako pracovať s príležitosťami, ktoré súvisia s projektmi.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 29e5a2c91186021eee9bb23aba3d42228fcd9381
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933235"
---
# <a name="manage-project-based-opportunities"></a>Správa príležitostí založených na projekte

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Spoločnosti založené na projekte majú svoje operácie doručovania zvyčajne rozmiestnené vo viacerých krajinách a geografických oblastiach. Náklady na realizáciu a dodávku projektu sa môžu líšiť v závislosti od toho, ktorá geografická oblasť alebo divízia spravuje dodávku. To môže mať naopak vplyv na marže dohody. Na poskytovanie služieb založených na projekte sa zvyčajne vyžaduje veľké množstvo času na ľudské zdroje, značné cestovné náklady, náklady na materiál a ďalšie výdavky.

Príležitosti založené na projekte v Dynamics 365 Project Operations sú navrhnuté s rozšíreniami pre Dynamics 365 Sales. Tento článok poskytuje podrobnosti o rôznych oblastiach a obchodnej logike zahrnutých v dodatočných funkciách, ktoré vyžadujú spoločnosti založené na projekte na správu príležitostí založených na projekte.

## <a name="view-all-project-based-opportunities"></a>Zobrazenie všetkých príležitostí založených na projekte

Zoznam všetkých príležitostí založených na projekte je uvedený na stránke so zoznamom **Príležitosť**. 

1. Prejdite do časti **Predaj** > **Príležitosti**.
2. Pomocou **prepínača zobrazení** vyberte ďalšie filtrované zobrazenia príležitostí. Môžete si vytvoriť svoje vlastné zobrazenia s vlastnými kritériami filtra, pomocou ktorých môžete nakonfigurovať tieto zobrazenia a možnosti navigácie.

Na tejto stránke so zoznamom alebo na stránke s podrobnosťami je možné vytvárať alebo odstraňovať projektové príležitosti.

## <a name="business-process-flow-for-project-based-deals"></a>Tok obchodného procesu pre obchody založené na projekte

Nasledujúce toky obchodného procesu sú podporované pre obchody na základe projektu v Project Operations:

- Potenciálny zákazník pre obchodný proces príležitosti
- Proces predaja príležitosti

### <a name="lead-to-opportunity-business-process"></a>Potenciálny zákazník pre obchodný proces príležitosti 
Potenciálny zákazník pre proces predaja príležitostí podporuje nasledujúce fázy:

| Fáza | Mapovaná entita | Funkcie |
| --- | --- | --- |
| Schváliť | Potenciálny zákazník | Kvalifikovanie potenciálneho zákazníka na vytvorenie obchodného vzťahu, kontaktu alebo príležitosti. |
| Vyvinúť | Príležitosť | Vytvorenie príležitosti na pridanie ďalších informácií pre vykonanú prácu, kľúčových účastníkov projektu a konkurenciu. |
| Navrhnúť | Príležitosť | Vytvorenie návrhu a získanie súhlasu od interného hodnotiaceho tímu. |
| Zatvoriť | Príležitosť | Získanie príležitosti na uzavretie obchodu. |

### <a name="opportunity-sales-process"></a>Proces predaja príležitosti
Proces predaja príležitosti v Project Operations je rozšírením obchodného toku procesu predaja príležitosti v aplikácii Sales. Tento obchodný proces je navrhnutý tak, aby hneď po zakúpení podporoval nasledujúce etapy v rámci príležitosti založenej na projekte.

| Fáza | Mapovaná entita | Funkcie |
| --- | --- | --- |
| Schváliť | Príležitosť | Kvalifikovanie potenciálneho zákazníka na vytvorenie obchodného vzťahu, kontaktu alebo príležitosti. |
| Navrhnúť | Ponuka | Vytvorenie návrhu pomocou projektových cenových ponúk a získanie súhlasu od interného hodnotiaceho tímu. |
| Zmluva | Projektová zmluva | Po získaní cenovej ponuky vytvorte zmluvu a začnite s realizáciou a dodávkou projektu. |
| Zatvoriť | Projektová zmluva | Úspešne dokončite prácu a uzatvorte projektovú zmluvu. |

> [!NOTE]
> Ak sa s potenciálnym zákazníkom začala dohoda na základe projektu, prednosť má obchodný proces potenciálneho zákazníka príležitosti.
>
> Ak sa začala dohoda na základe projektu s príležitosťou, prednosť má proces predaja príležitosti.

Môžete upraviť tok obchodného procesu produktu alebo vytvoriť vlastné toky obchodných procesov, aby ste mohli podľa potreby sledovať svoj proces predaja. Ďalšie informácie o toku obchodných procesov si prečítajte v časti [Prehľad tokov obchodných procesov](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]