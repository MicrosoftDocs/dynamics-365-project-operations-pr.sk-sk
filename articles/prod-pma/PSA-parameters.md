---
title: Parametre integrácie Project Service Automation
description: Táto téma vysvetľuje, ako nakonfigurovať spôsob zadávania predvolených údajov pri integrácii Microsoft Dynamics 365 for Project Service Automation so službou Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9793b680fc2be3b300689c4aded8005470f30519
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006440"
---
# <a name="project-service-automation-integration-parameters"></a>Parametre integrácie Project Service Automation

[!include[banner](../includes/banner.md)]

Na stránke **Integračné parametre Project Service Automation** môžete nakonfigurovať, ako sa pri integrácii Dynamics 365 Project Service Automation s Dynamics 365 Finance zadávajú predvolené údaje. Pre úspešnú synchronizáciu projektov z Project Service Automation do Finance je potrebné nastaviť nasledujúce polia.

Ak chcete otvoriť stránku **Integračné parametre Project Service Automation**, prejdite do časti **Projektové riadenie a účtovníctvo**\> **Konfigurácia**\> **Parametre integrácie Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - Integrácia projektovej úlohy, kategórie výdavkov na transakciu, odhady hodín, odhady výdavkov a blokovanie funkcií sú k dispozícii vo verzii 8.0.
> - Integrácia skutočných hodnôt je k dispozícii vo verzii 8.0.1 alebo novšej.


| Karta                    | Pole                | Popis |
|------------------------|----------------------|-------------|
| Všeobecné                | Predvolený typ projektu | Vyberte predvolený typ projektu. Keď sa projekty synchronizujú z Project Service Automation, táto hodnota sa použije, ak ste v šablóne integrácie nezadali predvolenú hodnotu. Počas synchronizácie sa pole **Typ projektu** nových projektov nastaví na túto hodnotu. Hodnota sa však môže aktualizovať, keď sa riadky projektových zmlúv synchronizujú z Project Service Automation. |
|                        | Kategória času        | Vyberte predvolenú kategóriu času. Táto hodnota sa použije, keď sa z Project Service Automation synchronizujú odhady hodín. Keď sa z Project Service Automation synchronizujú odhady hodín a skutočné hodnoty hodín, pole **Kategória** nových predpovedí hodín projektu v službe Finance je nastavené na túto hodnotu. |
|                        | Kategória poplatkov         | Vyberte predvolenú kategóriu poplatkov. Táto hodnota sa použije, keď sa z Project Service Automation synchronizujú skutočné hodnoty poplatkov. Keď sa z Project Service Automation synchronizujú skutočné hodnoty poplatkov, pole **Kategória** nových transakcií poplatkov v službe Finance je nastavené na túto hodnotu. |
| Predvolené hodnoty projektovej skupiny | Typ projektu         | Kliknutím na položku **Nový** pridáte riadok, kde môžete vybrať typ projektu, pre ktorý môžete nastaviť predvolenú skupinu projektov. Konkrétny typ projektu je možné v konfigurácii zvoliť iba raz. |
|                        | Skupina projektov        | Vyberte predvolenú skupinu projektov pre vybratý typ projektu. Keď sa z Project Service Automation synchronizujú nové projekty, pole **Skupina projektov** je nastavené na predvolenú hodnotu pre typ projektu, ak ste v šablóne integrácie nezadali predvolenú hodnotu. |
| Predvolené hodnoty typu fakturácie  | Typ fakturácie         | Kliknutím na položku **Nový** pridáte riadok, kde môžete vybrať typ fakturácie a pre ktorý môžete nastaviť predvolenú vlastnosť riadka. Konkrétny typ fakturácie je možné v konfigurácii zvoliť iba raz. |
|                        | Vlastnosť riadka        | Vyberte predvolenú vlastnosť riadka pre vybratý typ fakturácie. Pri synchronizácii nových odhadov hodín, nových odhadov výdavkov alebo nových skutočných hodnôt z Project Service Automation sa pole **Vlastnosť riadka** nastaví na predvolenú hodnotu pre typ fakturácie. |
| Blokovanie funkcií  | Nevzťahuje sa       | Vyberte funkciu, ktorá pochádza z Project Service Automation a ktorú chcete zakázať v službe Finance pre projekty a zmluvy. Môžete napríklad vypnúť schopnosť upravovať zmluvy a projekty, vytvárať štruktúry rozdelenia práce a zadávať časové rozvrhy v službe Finance. Polia súvisiace s účtovníctvom budú naďalej povolené, aj keď ich nastavenie parametrov nesprístupní. V predvolenom nastavení sú povolené všetky funkcie. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]