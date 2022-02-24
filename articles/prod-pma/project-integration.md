---
title: Integrácia služby Microsoft Project Client
description: Plánovanie a údržba plánu projektu môžu byť zložité, takže projektoví manažéri musia používať nástroje, ktoré im pomáhajú zvládnuť túto úlohu. Integrácia so službou Microsoft Project Client poskytuje podporu pre otvorenie a správu štruktúry rozdelenia práce na projekte.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084425"
---
# <a name="microsoft-project-client-integration"></a>Integrácia služby Microsoft Project Client

[!include [banner](../includes/banner.md)]

Plánovanie a údržba plánu projektu môžu byť zložité, takže projektoví manažéri musia používať nástroje, ktoré im pomáhajú zvládnuť túto úlohu. Integrácia so službou Microsoft Project Client poskytuje podporu pre otvorenie a správu štruktúry rozdelenia práce na projekte. Manažér projektu môže akékoľvek zmeny zverejniť späť do štruktúry rozdelenia práce na projekte v Dynamics 365 Finance.

> [!NOTE]
> Ak používate júlovú aktualizáciu (verzia 10.0.4), musíte si nainštalovať KB 4054797 a 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurácia doplnku Microsoft Project Client
Pre umožnenie integrácie s Microsoft Project Client musí byť nainštalovaný doplnok Microsoft Dynamics 365 v klientskej aplikácii Microsoft Project používateľa. To sa deje otvorením **Pracovného priestoru riadenia projektu**.

•   Kliknite na **Konfigurácia doplnku Project Client** zo sekcie **Odkazy** > **Nastavenie** pracovného priestoru.

•   Kliknite na **Otvoriť** a po výzve na **Spustiť**.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Otvorte a upravte existujúci koncept štruktúry rozdelenia práce Microsoft Project Client
Ak má projekt v Dynamics 365 Finance už má vytvorenú štruktúru rozdelenia práce, štruktúru rozdelenia práce je možné otvoriť v aplikácii Microsoft Project Client, ak je štruktúra rozdelenia práce v stave konceptu. Ak ju chcete otvoriť zo stránky **Projekt**, kliknite na odkaz **Otvoriť v Microsoft Project** na karte **Plán**. Túto stránku je tiež možné otvoriť v rámci aplikácie Microsoft Project Client kliknutím na **Otvoriť** v **Microsoft Dynamics 365**. Zo zoznamu vyberte **Právnická osoba** a **Projekt**.

> [!NOTE]
> Ak používate ako prehliadač Internet Explorer, budete musieť kliknúť na **Uložiť** a manuálne otvoriť z umiestnenia, do ktorého sa súbor stiahne. Alebo kliknite na **Uložiť a otvoriť**, čím sa súbor otvorí v Microsoft Project Client. Pri ukladaní nepremenujte názov súboru.

Pred vykonaním akýchkoľvek úprav súboru pomocou programu Microsoft Project Client je potrebné vykonať kontrolu. Kliknite na kartu **Odhlásiť** na karte **Microsoft Dynamics 365**. Toto zabráni ostatným používateľom súčasne upravovať štruktúru rozdelenia práce v rámci aplikácie Finance. Ak chcete zverejniť štruktúru rozdelenia práce po dokončení akýchkoľvek úprav, kliknite na **Prihlásiť** na karte **Microsoft Dynamics 365**.

Ak už bol projektový tím pridaný do projektu v službe Finance, zoznam zdrojov sa vyplní členmi tímu. Ak do projektu ešte nebol pridaný projektový tím, môžete vybrať zdroje a vytvoriť tím v rámci Microsoft Project Client kliknutím na tlačidlo **Zdroje** na karte **Microsoft Dynamics 365**. 

Nasledujúce údaje budú v rámci procesu registrácie synchronizované späť do služby Finance:

•   Názov úlohy

•   Počiatočný dátum

•   Dátum dokončenia

•   Predchodcovia

•   Názvy zdrojov

•   Kategória

•   Kategória zdroja

•   Pracovné hodiny

•   Poznámky

•   Priorita

> [!NOTE]
> Ak do svojho súboru Microsoft Project Client pridáte ďalšie stĺpce, neuložia sa do súboru a nezobrazia sa pri opätovnom otvorení súboru.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Vytvorte štruktúru rozdelenia práce pre existujúci projekt pomocou Microsoft Project Client
Ak chcete vytvoriť novú štruktúru rozdelenia práce pomocou Microsoft Project Client, postupujte podľa nasledujúcich pokynov:


1.  Otvorte Microsoft Project Client.

2.  Na karte **Microsoft Dynamics 365** kliknite na položku **Otvoriť**.

3.  Vyberte **Právnu entitu** pre projekt.

4.  Vyberte **Projekt**.

5.  Kliknite na **Odhlásiť** na karte **Microsoft Dynamics 365**.

6.  Keď ste pripravení na zverejnenie v službe Finance, kliknite na ikonu **Prihlásiť** na karte **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Výmena existujúcej štruktúry rozdelenia práce pre existujúci projekt pomocou Microsoft Project Client
Ak chcete vytvoriť novú štruktúru rozdelenia práce pomocou Microsoft Project Client a nahradiť existujúcu štruktúru rozdelenia práce pre existujúci projekt, postupujte nasledovne:

1.  Otvorte Microsoft Project Client.

2.  Vytvorte plán v Microsoft Project Client.

3.  Na karte **Microsoft Dynamics 365** Kliknite na **Uložiť zmeny** > **Nahradiť existujúci projekt**.

4.  Vyberte **Právnu entitu** pre projekt.

5.  Vyberte **Projekt**.

6.  Kliknite na tlačidlo **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Vytvorenie nového projektu v rámci Microsoft Project Client


1.  Otvorte Microsoft Project Client.

2.  Vytvorte plán v Microsoft Project Client.

3.  Na karte **Microsoft Dynamics 365** kliknite na **Uložiť zmeny** > **Uložiť do nového projektu**.

4.  Vyberte **Právnu entitu** pre projekt.

5.  V prípade potreby zadajte **ID projektu**.

6.  Zadajte **Názov produktu**.

7.  Vyberte **Typ projektu**, **Projektová skupina** a **ID projektovej zmluvy**. Prípadne môžete vytvoriť novú projektovú zmluvu kliknutím na **Nová**.

8.  Vyberte **Kalendár**, ktorý sa má použiť na zabezpečenie zdrojov.

11. Kliknite na tlačidlo **OK**.
