---
title: Synchronizujte stav projektu, aby ste zabránili vstupu do uzavretých projektov
description: Tento článok vysvetľuje, ako synchronizovať stav projektu, aby ste zabránili vstupu do neaktívnych alebo uzavretých projektov.
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

Contoso je naživo so spoločnosťou Microsoft Dynamics 365 Project Operations pre scenáre so zdrojovými/nezásobenými zásobami. V rámci bežných obchodných aktivít môžu byť projekty dokončené alebo pozastavené. Projekt môžete deaktivovať, aby ste sa uistili, že sa negenerujú žiadne výdavky ani faktúry.

## <a name="solution"></a>Riešenie

### <a name="prerequisites"></a>Požiadavky

-   Microsoft Dynamics Musí byť nainštalovaný 365 Finance 10.0.29 alebo novší.
-   Mapa duálneho zápisu 1.0.0.3 pre projekty V2 (msdyn\_ projekty) je potrebné nainštalovať alebo manuálne nakonfigurovať, ako je popísané nižšie.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Vytvorte aktualizovanú verziu mapy duálneho zápisu Project Operations Integrs Projects V2

Ak chcete aktualizovať mapu dvojitého zápisu Project Operations Projects V2:

1. Choďte na **Správa údajov** pracovný priestor a vyberte **Dvojité písanie**.
2. Vyberte **Dvojité písanie** dlaždica.
3. Z T **Tabuľková mapa** stĺpec, nájdite a vyberte **Projekt V2 (msdyn\_ projekty)** a potom vyberte Zastaviť.
4. Výberom názvu mapy otvorte mapu a potom vyberte **[žiadne]**.
5. V dialógovom okne Vybrať stĺpec vyberte **štátny kód\[ Stav projektu\]** a potom vyberte OK. Môžete písať **štát** v hodnote filtra na zúženie zoznamu.
6.  Vyberte **Pridajte alebo upravte transformáciu** v **typ mapy** na úpravu transformácie.
7.  Od **Typ transformácie** vyberte **ValueMap**.
8.  Vyberte **Pridajte mapovanie hodnoty** a potom pridajte nasledujúce **Keys** a **hodnoty**:

   Key       | Hodnota 
   ----------|-------
   V procese | 0     
   dokončené | 1     

![Snímka obrazovky zobrazujúca mapovanie s duálnym zápisom](media/projectstage-dw-mapping.png)

9. Vyberte **Uložiť**.
10. Z vrcholu **Dvojité zapisovanie > Projekty V2 (msdyn_projects)** stránku, vyberte **Uložiť ako**.
11. Od **Pridať tabuľku** v **Vydavateľ** pole, vyberte **Predvolený vydavateľ CDS**.
12. Nastaviť **Verzia** pole na 1.0.0.3.
13. Typ a **Popis** a potom vyberte **Uložiť**.
14. Z vrcholu **Dvojité zapisovanie > Projekty V2 (msdyn_projects)** stránku, vyberte **Bežať** spustite mapu a potom vyhľadajte **Áno** ak sa zobrazí výzva na potvrdenie pred spustením. 

### <a name="close-a-newly-completed-project"></a>Zatvorte novo dokončený projekt

Dynamics 365 Finance používa **etapa projektu** na rozlíšenie medzi projektmi **v procese** alebo **hotový**. **Dokončené** projekty nemôžu vznikať výdavky ani byť fakturované zákazníkom.

1. Otvorte projekt na deaktiváciu.
2. Na páse s nástrojmi vyberte **Deaktivovať**.

> [!NOTE]
> Projekt môžete deaktivovať alebo zavrieť, pretože v kontexte financií sa budú oba správať rovnako.

3. V časti Financie otvorte **Zoznam všetkých projektov** stránku.
4. Potvrďte, že sa deaktivovaný projekt nezobrazuje v zozname.
5. V **ukázať projekty** filter nad zoznamom, zmeňte hodnotu z **Aktívne** do **Všetky**.
6. Teraz uvidíte deaktivovaný projekt.

Ak sa pokúsite zaznamenať čas alebo výdavky do tohto projektu vo Financie, nemali by ste vidieť projekt na výber. Ak manuálne zadáte číslo projektu na výdaji, zobrazí sa hlásenie ako „Fáza projektu dokončená neumožňuje zaznamenávanie do projektu“. Fakturácia a iné fakturačné funkcie by mali byť deaktivované, pretože budú v kontexte uzavretého projektu.

