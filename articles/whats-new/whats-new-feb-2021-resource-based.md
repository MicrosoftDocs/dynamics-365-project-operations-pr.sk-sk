---
title: Čo je nové vo februári 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Tento článok poskytuje informácie o aktualizáciách kvality dostupných vo vydaní Project Operations z februára 2021 pre scenáre založené na zdrojoch/nezásobách.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 38fede1746bcb09700c9c9c5e20653e0c39fea2a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910663"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové vo februári 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa vzťahuje na nasledujúce Dynamics 365 Project Operations komponenty a verzie:

- Project Operations v prostredí Dataverse 4.7.0.95
- Projektový manažment a účtovníctvo v prostredí Dynamics 365 Finance verzia 10.0.16 

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| **Fakturácia a tvorba cien** | 2053736 | Podrobnosti o riadku faktúry sú teraz prístupné po prechode na položku **Faktúra** > **Súvisiace informácie**. |
| **Fakturácia a tvorba cien** | 2122613 | Akcie **Aktivovať** a **Deaktivovať** boli odstránené zo združovacích entít **Cenník**. |
| **Fakturácia a tvorba cien** | 2128606 | Vyriešil sa problém s **ullReferenceException** v doplnku **GetEstimatesForProject**. |
| **Nasadenie a konfigurácia** | 2139346 | Vyriešil sa problém s importom nespravovaného riešenia **Dynamics365ProjectOperationsDualWrite**. |
| **Nasadenie a konfigurácia** | 2140569 | Projektové riešenie nesmie byť nainštalované v prostrediach Dataverse Teams. |
| **Nasadenie a konfigurácia** | 2086991 | Obmedzené prispôsobenie lokalizácie webových zdrojov. |
| **Správa príležitostí** | 2136794 | Zobrazenie správneho chybového hlásenia, keď zlyhá proces **Potvrdiť faktúru** alebo **Označiť faktúru ako zaplatenú**. |
| **Správa príležitostí** | 2139330 | Zmena projektového manažéra na projekte nesmie resetovať vlastniacu spoločnosť späť na predvolenú hodnotu. |
| **Správa príležitostí** | 2146376 | Opravená suma dane v nezúčtovateľnom stave je vytvorená z potvrdenia faktúry. |
| **Plánovanie a sledovanie projektu** | 2099879 | Nasadenie prostredia Dataverse musí vytvoriť predvolenú kategóriu transakcií so statickým ID a nie náhodne vygenerovať jednu pre každé prostredie. |
| **Plánovanie a sledovanie projektu** | 2128577 | Opravené oprávnenia používateľa služby na spustenie projektu na aktualizáciu kategórie transakcií pri priradení zdroja. |
| **Plánovanie a sledovanie projektu** | 2164035 | Opravené problémy s funkciou **Kopírovať projekt**. |
| **Zadanie času** | 2129161 | Uplatňujú sa prísnejšie obmedzenia, aby sa zabezpečilo, že používatelia nebudú môcť meniť a aktualizovať zadaný alebo schválený časový údaj. |
| **Zadanie času** | 2103572 | Schválenie času pre časové zadania mimo projektu nesmie hľadať rolu schvaľovateľa projektu. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v Dynamics 365 Finance 

Viac informácií o riadení projektov a účtovníctve v Dynamics 365 Finance nájdete na [Čo je nové Január 2021 – Projektové operácie pre scenáre založené na zdrojoch/nezásobách](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Regulačné aktualizácie

Informácie o regulačných aktualizáciách pre aplikácie Finance and Operations nájdete na [Regulačné aktualizácie](/dynamics365/finance/localizations/regulatory-updates). Ďalším spôsobom, ako sa dozvedieť o regulačných aktualizáciách, je prihlásiť sa do služby Lifecycle Services (LCS) a pozrieť si plánované aktualizácie právnych predpisov pomocou nástroja na vyhľadávanie problémov. Vyhľadávanie problémov vám umožňuje vyhľadávať podľa krajiny, typu funkcie a vydania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]