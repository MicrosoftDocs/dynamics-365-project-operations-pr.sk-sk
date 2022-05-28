---
title: Použite kategórie obstarávania s projektovými nákupnými objednávkami a čakajúcimi faktúrami dodávateľa
description: Táto téma popisuje, ako nakonfigurovať kategórie obstarávania, ktoré možno použiť s projektovými nákupnými objednávkami a čakajúcimi faktúrami dodávateľa.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613366"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Použite kategórie obstarávania s projektovými nákupnými objednávkami a čakajúcimi faktúrami dodávateľa

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Odborníci na nákup môžu vytvárať a udržiavať katalógy položiek a služieb, ktoré možno použiť v projektových nákupných objednávkach a čakajúcich faktúrach dodávateľa. [Katalógy obstarávania](/dynamics365/supply-chain/procurement/procurement-catalogs) vám ponúka jednoduchý spôsob kategorizácie nákupov bez toho, aby ste museli konfigurovať a používať vydaný katalóg produktov. Každá kategória obstarávania môže byť priradená ku kategórii projektu pre transakcie času, nákladov alebo položiek. Po zaúčtovaní čakajúcej faktúry dodávateľa, ktorá používa kategóriu obstarávania, systém vytvorí skutočné údaje o čase, výdavkoch alebo materiáli projektu, transakcie projektu a položky vedľajšej knihy.

## <a name="minimum-version-requirements"></a>Minimálne požiadavky na verziu

Nasledujúce verzie sú potrebné na používanie kategórií obstarávania s projektovými objednávkami pre Microsoft Dynamics 365 Project Operations scenáre bez zásob/založené na zdrojoch:

- Projektové operácie Dataverse verzia riešenia 4.41.0.45 alebo novšia
- Prostredie financií a operácií verzie 10.0.26 alebo novšej

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Spustite mapy s duálnym zápisom pre podporu kategórií obstarávania

Uistite sa, že mapovanie pre **Projektové operácie integrácia projekt dodávateľ faktúra riadok export entity msdyn\_ projectvendorinvoicelines** používa verziu 1.0.0.4 alebo novšiu.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Povoľte funkčný kľúč pre kategórie obstarávania

Ak chcete povoliť funkciu používania kategórií obstarávania s projektovými objednávkami, postupujte podľa týchto krokov.

1. V Dynamics 365 Finance otvorte súbor **Správa funkcií** pracovnom priestore.
1. V zozname funkcií nájdite **Použite kategórie obstarávania v projektových operáciách pre scenáre založené na zdrojoch/bez zásob** funkciu a potom vyberte **Povoliť**.

> [!IMPORTANT]
> Predpokladom je, že musíte povoliť aj **Povoľte čakajúce faktúry dodávateľa v projektových operáciách pre scenáre založené na zdrojoch/nezásoby** vlastnosť.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapujte kategórie projektov v hierarchii kategórií obstarávania

Podľa týchto krokov mapujte kategórie projektov na kategórie obstarávania v **Kategória obstarávania** hierarchia:

1. Ísť do **Obstarávanie a získavanie zdrojov \> Kategórie obstarávania**.
1. Vyberte **Upraviť hierarchiu kategórií**.
1. Vyberte požadovaný uzol hierarchie kategórií a potom na **Priraďte kategórie projektu** priraďte uzol ku kategórii projektu z **čas**, Výdavok**, príp **,Projekt položky** kategória (t.j **Predvolený čas** alebo **Predvolené náklady** kategória).
1. Vyberte **Uložiť**.
1. Zatvorí stránku.

> [!NOTE]
> Mapovanie kategórie obstarávania na kategóriu projektu je voliteľné. Ak kategória obstarávania nie je namapovaná, systém použije hodnotu, ktorá je nastavená v **Položka** poli v **Predvolené nastavenia kategórie projektu** oddiel na **Projektové operácie na Dynamics 365 Zapojenie zákazníkov** záložku **Projektový manažment a účtovné parametre** stránku.
