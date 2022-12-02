---
title: Synchronizujte stav projektu, aby ste zabránili vstupu do uzavretých projektov
description: Tento článok vysvetľuje, ako synchronizovať stav projektu, aby ste zabránili zadávaniu do neaktívnych alebo uzavretých projektov.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348126"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Synchronizujte stav projektu, aby ste zabránili vstupu do uzavretých projektov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

## <a name="scenario"></a>Scenár

Spoločnosť Contoso používa Microsoft Dynamics 365 Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek. V rámci bežných obchodných aktivít môžu byť projekty dokončené alebo pozastavené. Projekt môžete deaktivovať, aby ste sa uistili, že sa negenerujú žiadne výdavky ani faktúry.

## <a name="solution"></a>Riešenie

### <a name="prerequisites"></a>Požiadavky

-   Musí byť nainštalovaný Microsoft Dynamics 365 Finance 10.0.29 alebo novší.
-   Mapu duálneho zápisu 1.0.0.3 pre projekty V2 (msdyn\_projects) je potrebné nainštalovať alebo manuálne nakonfigurovať, ako je popísané nižšie.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Vytvorenie aktualizovanej verzie mapy duálneho zápisu Project Operations integration Projects V2

Ak chcete aktualizovať mapu duálneho zápisu Project Operations Projects V2:

1. Prejdite do pracovného priestoru **Správa údajov** a vyberte **Duálny zápis**.
2. Vyberte dlaždicu **Duálny zápis**.
3. V stĺpci **Mapa tabuľky** nájdite a vyberte **Project V2 (msdyn\_projects)** a potom vyberte Zastaviť.
4. Výberom názvu mapy otvorte mapu a potom vyberte **[Žiadna]**.
5. V dialógovom okne Vybrať stĺpec vyberte **statecode \[Stav projektu\]** a potom vyberte OK. Môžete písať **state** v hodnote filtra na zúženie zoznamu.
6.  Vyberte **Pridať alebo upraviť transformáciu** v stĺpci **typ mapy** na úpravu transformácie.
7.  Z **Typu transformácie** vyberte **ValueMap**.
8.  Vyberte **Pridať mapovanie hodnoty** a potom pridajte nasledujúce **Kľúče** a **Hodnoty**:

   Key       | Hodnota 
   ----------|-------
   InProcess | 0     
   dokončené | 1     

![Snímka obrazovky so zobrazením mapovania s duálnym zápisom](media/projectstage-dw-mapping.png)

9. Vyberte **Uložiť**.
10. A hornej časti stránky **Duálny zápis > Projekty V2 (msdyn_projects)** vyberte **Uložiť ako**.
11. Z **Pridať tabuľku** v poli **Vydavateľ** vyberte **Predvolený vydavateľ CDS**.
12. Nastavte pole **Verzia** na 1.0.0.3.
13. Napíšte **Popis** a potom vyberte **Uložiť**.
14. Z hornej časti stránky **Duálny zápis > Projekty V2 (msdyn_projects)** vyberte **Spustiť** spustite mapu a potom vyberte **Áno**, ak sa zobrazí výzva na potvrdenie pred spustením. 

### <a name="close-a-newly-completed-project"></a>Zatvorte novo dokončený projekt

Dynamics 365 Finance používa pole **etapa projektu** na rozlíšenie medzi projektmi, ktoré **prebiehajú** alebo **sú dokončené**. V **dokončených** projektoch nemôžu vznikať výdavky ani byť fakturované zákazníkom.

1. Otvorte projekt na deaktiváciu.
2. Na páse s nástrojmi vyberte položku **Deaktivovať**.

> [!NOTE]
> Projekt môžete deaktivovať alebo zavrieť, pretože v kontexte Finance sa budú oba správať rovnako.

3. V časti Finance otvorte stránku **Zoznam všetkých projektov**.
4. Potvrďte, že sa deaktivovaný projekt nezobrazuje v zozname.
5. Vo filtri **ukázať projekty** nad zoznamom zmeňte hodnotu z **Aktívne** na **Všetky**.
6. Teraz uvidíte deaktivovaný projekt.

Ak sa pokúsite zaznamenať čas alebo výdavky do tohto projektu vo Finance, nemali by ste vidieť projekt na výber. Ak manuálne zadáte číslo projektu vo výdavku, zobrazí sa hlásenie „Fáza projektu je dokončená neumožňuje zaznamenávanie do projektu“. Fakturácia a iné fakturačné funkcie by mali byť deaktivované, pretože budú v kontexte uzavretého projektu.

