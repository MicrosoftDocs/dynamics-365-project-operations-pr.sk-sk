---
title: Navrhnite projektové zdroje
description: Tento článok poskytuje informácie o navrhovaní zdrojov projektu.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 379c75578846e2834321045edc7deb116aff7b06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930843"
---
# <a name="propose-project-resources"></a>Navrhnite projektové zdroje

[!include [banner](../includes/psa-now-project-operations.md)]

Správcovia zdrojov môžu navrhnúť zdroj projektového manažéra pomocou požiadavky prostriedku.

1. V mriežke požiadavky alebo samotnej žiadosti vyberte položku **Vyhľadať zdroje**.
2. Na stránke **Asistent plánovania** vyberte zdroj a potom v table stav **Vytvoriť rezerváciu zdroja** v poli **Stav rezervácie** zvoľte možnosť **Rezervovať**.

    ![Vybratý navrhovaný zdroj.](media/Resource-Management-image62.png)

Nasledujúce aktualizácie stavu sa vyskytujú:

- Na stránke **Asistent plánovania** sa aktualizujú indikátory stavu, ktoré naznačujú, že rezervácia je navrhnutá a nie je pevne rezervovaná.

    ![Indikátory stavu navrhovanej rezervácie na stránke Asistenta plánovania.](media/Resource-Management-image63.png)

- Na žiadosť o prostriedok, stav sa zmení na **Vyžaduje kontrolu**.

    ![Stav požiadavky na zdroj sa zmenil na Vyžaduje kontrolu.](media/Resource-Management-image64.png)

- Na karte **Tím** projektu sa hodnota všeobecných členov tímu **Stav žiadosti** zmenila na **Vyžaduje kontrolu**.

    ![Stav žiadosti všeobecného člena tímu sa zmenila na karte Tím na Vyžaduje kontrolu.](media/Resource-Management-image48.png)

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

![Zobrazenie využitia zdroja.](media/Resource-Management-image65.png)

Každá bunka v mriežke predstavuje percento fakturovateľného využitia prostriedku v období, ako je napríklad deň, týždeň alebo mesiac. Na vyfarbenie buniek sa používajú nasledujúce vzorce:

- **Zelená:** Fakturovateľné využitie \>= Cieľové využitie zdroja
- **Žltá:** Cieľové využitie – 20 \<Fakturovateľná využitie \< Cieľové využitie
- **Červená:** Fakturovateľná využitie \< Cieľové využitie – 20

Keďže zobrazenie **Využitie zdroja** je založené na tabuli plánovania, môžete filtrovať výsledky pomocou možností filtrovania tabule plánovania.

Mriežka si vyžaduje, aby ste stanovili cieľové využitie buď roly, alebo individuálneho zdroja. Ak tak chcete urobiť, prejdite na **Zdroje** \> **Zdrojové roly**.

Okrem toho musí byť priradená predvolená rola pre každý rezervovateľný prostriedok. Prejdite do **Zdroje** \> **Zdroje**. Na karte **Project Service** skontrolujte, či je definovaná rola prostriedku a že pole **Je predvolená** je nastavené na **Áno**. Môžete pridať ďalšie roly, kde **Je predvolená = nie**. Úloha, kde **Je predvolená = Áno** sa používa na vyhodnotenie využitia prostriedku proti cieľu pre túto rolu.

![Súbor predvolenej roly.](media/Resource-Management-image67.png)

Na karte **Project Service** môžete tiež nastaviť individuálne cieľové využitie prostriedku. Výpočet využitia potom použije cieľové využitie na vyhodnotenie cieľového prostriedku namiesto cieľa predvolenej roly prostriedku.

Využitie sa zobrazuje pre zdroj len vtedy, ak tento prostriedok schválil účtovateľný čas počas obdobia, ktoré je zobrazené v mriežke.

## <a name="resource-availability"></a>Dostupnosť zdroja

Je dôležité, aby správcovia zdrojov mohli zobraziť dostupnosť zdrojov a aktualizovať rezervácie. V niektorých prípadoch neexistuje žiadny formálny dopyt (požiadavka na zdroje), ale správca prostriedkov musí reagovať na neplánovaný dopyt, ktorý sa dodáva prostredníctvom kanálov, ako je e-mail, telefonát alebo okamžitá správa. Správcovia zdrojov používajú tabule plánovania na aktualizáciu zdrojov a rezervácií.

Pracovné hodiny prostriedkov sa používajú ako základ pre výpočet dostupnosti prostriedku. Rezervácie zdrojov spotrebúvajú kapacitu zdrojov.

![Tabuľa plánovania.](media/Resource-Management-image68.png)

Tabule plánovania používajú farby a tieňovanie na zobrazovanie rezervácií, dostupnosti a nadmernej rezervácie, ako aj stav rezervácií. Nastavenie v nastaveniach tabule plánovania vám umožňuje zobraziť legendu.

Ak sa vedľa individuálneho rezervovateľného prostriedku na tabuli plánovania zobrazí šípka ukazujúca vpravo, zdroj možno rozbaliť a zobraziť podrobnosti o práci, na ktorej je zdroj rezervovaný.

![Rezervovateľný zdroj rozbalený na tabuli plánovania.](media/Resource-Management-image69.png)

Pretože Dynamics 365 Project Service Automation používa systém Universal Resource Scheduling, ak ste tiež Dynamics 365 Field Service nainštalovali, môžete zobraziť podrobnosti o rezerváciách zdrojov pre projekty, pracovné objednávky a všetky ostatné entity, na ktoré ste rozšírili plánovanie.

![Podrobnosti o rezerváciách zdrojov pre projekty a objednávky prác.](media/Resource-Management-image70.png)

Ak chcete zobraziť ďalšie podrobnosti o jednotlivých prostriedkoch, kliknite naň pravým tlačidlom a otvorte kartu zdroja.

![Karta zdroja.](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
