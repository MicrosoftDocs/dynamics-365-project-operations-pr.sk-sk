---
title: Kontrola navrhovaných zdrojov
description: Táto téma poskytuje informácie o tom, ako navrhovať projektové zdroje.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279292"
---
# <a name="review-proposed-resources"></a>Kontrola navrhovaných zdrojov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Správcovia zdrojov môžu navrhnúť zdroj projektového manažéra pomocou požiadavky prostriedku.

1. V mriežke požiadavky alebo samotnej žiadosti vyberte položku **Vyhľadať zdroje**.
2. Na stránke **Asistent plánovania** vyberte zdroj a potom v table stav **Vytvoriť rezerváciu zdroja** v poli **Stav rezervácie** zvoľte možnosť **Rezervovať**.

Nasledujúce aktualizácie stavu sa vyskytujú:

- Na stránke **Asistent plánovania** sa aktualizujú indikátory stavu, ktoré naznačujú, že rezervácia je navrhnutá a nie je pevne rezervovaná.
- Na žiadosť o prostriedok, stav sa zmení na **Vyžaduje kontrolu**.
- Na karte **Tím** projektu sa hodnota všeobecných členov tímu **Stav žiadosti** zmenila na **Vyžaduje kontrolu**.

Projektový manažér môže buď prijať, alebo zamietnuť návrh.

Keď správcovia zdrojov spracúvajú žiadosti o prostriedky, môžu použiť ktorýkoľvek z nasledujúcich prístupov:

- Navrhnite viacero zdrojov na uspokojenie dopytu, ak nie je k dispozícii žiadny jediný prostriedok na splnenie požadovaných hodín. Navrhované hodiny sa potom rozdelia medzi viaceré zdroje, ktoré môžu uspokojiť požadované hodiny. V tomto scenári, hodiny nemožno prekrývať.
- Navrhnite menej zdrojov, než je požadované. V tomto scenári, navrhovaná kapacita prostriedku je menšia ako požadované hodiny, ktoré žiadateľ zadal. Preto, keď žiadateľ akceptuje navrhované prostriedky, nesplnených zdrojov požiadavka je vytvorená na zachytenie zostávajúcich požiadaviek.
- Zarezervujte viacero zdrojov na uspokojenie dopytu, ak nie je k dispozícii žiadny jediný prostriedok na dokončenie prác.
- Rezervujte menej zdrojov, než je požadované. V tomto scenári, rezervované hodiny sú menej ako požadované hodiny. Systém vás prevedie navrhnutie zdrojov namiesto rezervácií, aby žiadateľa mohol overiť a sledovať zostávajúci dopyt.

## <a name="resource-availability"></a>Dostupnosť zdroja

Je dôležité, aby správcovia zdrojov mohli zobraziť dostupnosť zdrojov a aktualizovať rezervácie. V niektorých prípadoch neexistuje žiadny formálny dopyt (požiadavka na zdroje), ale správca prostriedkov musí reagovať na neplánovaný dopyt, ktorý sa dodáva prostredníctvom kanálov, ako je e-mail, telefonát alebo okamžitá správa. Správcovia zdrojov používajú tabule plánovania na aktualizáciu zdrojov a rezervácií.

Pracovné hodiny prostriedkov sa používajú ako základ pre výpočet dostupnosti prostriedku. Rezervácie zdrojov spotrebúvajú kapacitu zdrojov.

Tabule plánovania používajú farby a tieňovanie na zobrazovanie rezervácií, dostupnosti a nadmernej rezervácie, ako aj stav rezervácií. Nastavenie v nastaveniach tabule plánovania vám umožňuje zobraziť legendu.

Ak sa vedľa individuálneho rezervovateľného prostriedku na tabuli plánovania zobrazí šípka ukazujúca vpravo, zdroj možno rozbaliť a zobraziť podrobnosti o práci, na ktorej je zdroj rezervovaný.

Pretože Dynamics 365 Project Operations používa systém Universal Resource Scheduling, ak ste tiež Dynamics 365 Field Service nainštalovali, môžete zobraziť podrobnosti o rezerváciách zdrojov pre projekty, pracovné objednávky a všetky ostatné entity, na ktoré ste rozšírili plánovanie.

Ak chcete zobraziť ďalšie podrobnosti o jednotlivých prostriedkoch, kliknite naň pravým tlačidlom a otvorte kartu zdroja.



[!INCLUDE[footer-include](../includes/footer-banner.md)]