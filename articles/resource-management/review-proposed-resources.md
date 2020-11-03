---
title: Kontrola navrhovaných zdrojov
description: Táto téma poskytuje informácie o tom, ako navrhovať projektové zdroje.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084331"
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

## <a name="billable-utilization"></a>Fakturovateľné využitie

Zdroje môžu mať cieľové fakturovateľné využitie. Tento cieľ využitia je buď definovaný ako atribút na zdroja predvolenú rolu, alebo nastavenie na záznam jednotlivých rezervovateľných zdrojov. Výpočty využitia sú založené na skutočných hodinách, ktoré zdroje hlásili pomocou schválených časových položiek.

Na výpočet využitia sa používajú nasledujúce vzorce:

- Fakturovateľné využitie = Spoplatnená skutočná kapacita hodín ÷ kapacita zdroja
- Nefakturovateľné využitie = skutočný čas s fakturáciou typu ID = Nefakturovateľné, doplnkové alebo nie je k dispozícii ÷ zdroj kapacity
- Interné = skutočný čas bez predajnej zmluvy ÷ kapacita zdrojov
- Kapacita zdrojov = pracovné hodiny zdroja – mimo pracoviska – dni pracovného času

**Zobrazenie využitia** prostriedkov môžete nájsť na table **Zdroje**.

Každá bunka v mriežke predstavuje percento fakturovateľného využitia prostriedku v období, ako je napríklad deň, týždeň alebo mesiac. Na vyfarbenie buniek sa používajú nasledujúce vzorce:

- **Zelená:** Fakturovateľné využitie \>= Cieľové využitie zdroja
- **Žltá:** Cieľové využitie – 20 \<Fakturovateľná využitie \< Cieľové využitie
- **Červená:** Fakturovateľná využitie \< Cieľové využitie – 20

Keďže zobrazenie **Využitie zdroja** je založené na tabuli plánovania, môžete filtrovať výsledky pomocou možností filtrovania tabule plánovania.

Mriežka si vyžaduje, aby ste stanovili cieľové využitie buď roly, alebo individuálneho zdroja. Ak tak chcete urobiť, prejdite na **Zdroje** \> **Zdrojové roly**.

Okrem toho musí byť priradená predvolená rola pre každý rezervovateľný prostriedok. Prejdite do **Zdroje** \> **Zdroje**. Na karte **Project Service** skontrolujte, či je definovaná rola prostriedku a že pole **Je predvolená** je nastavené na **Áno**. Môžete pridať ďalšie roly, kde **Je predvolená = nie**. Úloha, kde **Je predvolená = Áno** sa používa na vyhodnotenie využitia prostriedku proti cieľu pre túto rolu.

Na karte **Project Service** môžete tiež nastaviť individuálne cieľové využitie prostriedku. Výpočet využitia potom použije cieľové využitie na vyhodnotenie cieľového prostriedku namiesto cieľa predvolenej roly prostriedku.

Využitie sa zobrazuje pre zdroj len vtedy, ak tento prostriedok schválil účtovateľný čas počas obdobia, ktoré je zobrazené v mriežke.

## <a name="resource-availability"></a>Dostupnosť zdroja

Je dôležité, aby správcovia zdrojov mohli zobraziť dostupnosť zdrojov a aktualizovať rezervácie. V niektorých prípadoch neexistuje žiadny formálny dopyt (požiadavka na zdroje), ale správca prostriedkov musí reagovať na neplánovaný dopyt, ktorý sa dodáva prostredníctvom kanálov, ako je e-mail, telefonát alebo okamžitá správa. Správcovia zdrojov používajú tabule plánovania na aktualizáciu zdrojov a rezervácií.

Pracovné hodiny prostriedkov sa používajú ako základ pre výpočet dostupnosti prostriedku. Rezervácie zdrojov spotrebúvajú kapacitu zdrojov.

Tabule plánovania používajú farby a tieňovanie na zobrazovanie rezervácií, dostupnosti a nadmernej rezervácie, ako aj stav rezervácií. Nastavenie v nastaveniach tabule plánovania vám umožňuje zobraziť legendu.

Ak sa vedľa individuálneho rezervovateľného prostriedku na tabuli plánovania zobrazí šípka ukazujúca vpravo, zdroj možno rozbaliť a zobraziť podrobnosti o práci, na ktorej je zdroj rezervovaný.

Pretože Dynamics 365 Project Operations používa systém Universal Resource Scheduling, ak ste nainštalovali aj Dynamics 365 Field Service, môžete zobraziť podrobnosti o rezerváciách zdrojov pre projekty, objednávky prác a všetky ostatné entity, na ktoré ste rozšírili plánovanie.

Ak chcete zobraziť ďalšie podrobnosti o jednotlivých prostriedkoch, kliknite naň pravým tlačidlom a otvorte kartu zdroja.

