---
title: Kontrola navrhovaných zdrojov
description: Táto téma poskytuje informácie o tom, ako navrhovať projektové zdroje.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3d2ab3ba9e5b18a2b42acaa2dc51ad94b8189274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584983"
---
# <a name="review-proposed-resources"></a>Kontrola navrhovaných zdrojov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Správcovia zdrojov môžu navrhnúť zdroj projektového manažéra pomocou požiadavky prostriedku.

Ak chcete skontrolovať navrhnuté zdroje, postupujte takto:

1. V mriežke **Požiadavka** alebo samotnej žiadosti vyberte položku **Vyhľadať zdroje**.
2. Na stránke **Asistent plánovania** vyberte zdroj a potom potvrďte, že všetky navrhované hodiny sú zahrnuté v navrhovanej rezervácii.
3. Na table **Vytvoriť rezerváciu zdroja** nastavte pole **Stav rezervácie** na **Navrhované**, a potom vyberte **Rezervovať**.

    > [!NOTE]
    > Nastavenie **Stav rezervácie** na **Navrhované** nerezervuje zdroj napevno a nenahrádza generický zdroj menovaným členom tímu.

    Nasledujúce aktualizácie stavu sa vyskytujú:

    - Na stránke **Asistent plánovania** sa aktualizujú indikátory stavu, ktoré naznačujú, že rezervácia je navrhnutá a nie je pevne rezervovaná.
    - Na žiadosť o prostriedok, stav sa zmení na **Vyžaduje kontrolu**.
    - Na karte **Tím** projektu sa hodnota všeobecných členov tímu **Stav žiadosti** zmenila na **Vyžaduje kontrolu**.

Projektový manažér môže prijať alebo zamietnuť návrh.

Keď správcovia zdrojov spracúvajú žiadosti o prostriedky, môžu použiť ktorýkoľvek z nasledujúcich prístupov:

- Navrhnite viacero zdrojov na uspokojenie dopytu, ak nie je k dispozícii žiadny jediný prostriedok na splnenie požadovaných hodín. Navrhované hodiny sa potom rozdelia medzi viaceré zdroje, ktoré môžu uspokojiť požadované hodiny. V tomto scenári, hodiny nemožno prekrývať.
- Navrhnite menej zdrojov, než je požadované. V tomto scenári, navrhovaná kapacita prostriedku je menšia ako požadované hodiny, ktoré žiadateľ zadal. Keď žiadateľ akceptuje navrhované zdroje, je vytvorená požiadavka nesplnených zdrojov na zachytenie zostávajúcich požiadaviek.
- Zarezervujte viacero zdrojov na uspokojenie dopytu, ak nie je k dispozícii žiadny jediný prostriedok na dokončenie prác.
- Rezervujte menej zdrojov, než je požadované. V tomto scenári, rezervované hodiny sú menej ako požadované hodiny. Systém vás prevedie navrhnutím zdrojov namiesto rezervácií, aby žiadateľa mohol overiť a sledovať zostávajúci dopyt.

## <a name="resource-availability"></a>Dostupnosť zdroja

Správcovia zdrojov musia byť schopní zobraziť dostupnosť zdrojov a aktualizovať rezervácie. V niektorých prípadoch neexistuje žiadny formálny dopyt (požiadavka na zdroje). Správca zdrojov však musí reagovať na neplánovaný dopyt, ktorý prichádza prostredníctvom iných kanálov, ako sú e-maily, telefónne hovory alebo rýchle správy. Správcovia zdrojov používajú **tabuľu plánovania** na aktualizáciu zdrojov a rezervácií.

Pracovné hodiny zdrojov sa používajú ako základ pre výpočet dostupnosti zdroja. Rezervácie zdrojov spotrebúvajú kapacitu zdrojov.

**Tabuľa plánovania** používa farby a tieňovanie na zobrazovanie rezervácií, dostupnosti a nadmernej rezervácie, ako aj stavu rezervácií. Nastavenie na **Tabuli plánovania** umožňuje zobraziť legendu.

Ak sa vedľa individuálneho rezervovateľného zdroja na **tabuli plánovania** zobrazí šípka ukazujúca vpravo, zdroj možno rozbaliť a zobraziť podrobnosti o práci, na ktorej je zdroj rezervovaný.

Pretože Dynamics 365 Project Operations používa systém Universal Resource Scheduling, ak ste tiež Dynamics 365 Field Service nainštalovali, môžete zobraziť podrobnosti o rezerváciách zdrojov pre projekty, pracovné objednávky a všetky ostatné entity, na ktoré ste rozšírili plánovanie.

Ak chcete zobraziť ďalšie podrobnosti o príslušnom zdroji, kliknite naň pravým tlačidlom a otvorte kartu zdroja.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
