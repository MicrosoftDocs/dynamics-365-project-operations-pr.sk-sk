---
title: Použite kategórie obstarávania s objednávkami projektu a čakajúcimi faktúrami dodávateľa
description: Tento článok popisuje, ako nakonfigurovať kategórie obstarávania, ktoré možno použiť s projektovými nákupnými objednávkami a čakajúcimi faktúrami dodávateľa.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028629"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Použite kategórie obstarávania s objednávkami projektu a čakajúcimi faktúrami dodávateľa

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Odborníci na nákup môžu vytvárať a udržiavať katalógy položiek a služieb, ktoré možno použiť v projektových nákupných objednávkach a čakajúcich faktúrach dodávateľa. [Katalógy obstarávania](/dynamics365/supply-chain/procurement/procurement-catalogs) vám ponúka jednoduchý spôsob kategorizácie nákupov bez toho, aby ste museli konfigurovať a používať vydaný katalóg produktov. Každá kategória obstarávania môže byť priradená ku kategórii projektu pre transakcie času, nákladov alebo položiek. Po zaúčtovaní čakajúcej faktúry dodávateľa, ktorá používa kategóriu obstarávania, systém vytvorí skutočné údaje o čase, výdavkoch alebo materiáli projektu, transakcie projektu a položky vedľajšej knihy.

## <a name="minimum-version-requirements"></a>Minimálne požiadavky na verziu

Nasledujúce verzie sú potrebné na používanie kategórií obstarávania s objednávkami projektu pre Microsoft Dynamics 365 Project Operations scenáre bez zásob/založené na zdrojoch:

- Projektové operácie Dataverse verzia riešenia 4.41.0.45 alebo novšia
- Financie a prevádzkové prostredie verzie 10.0.26 alebo novšej

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Spustite mapy s duálnym zápisom pre podporu kategórií obstarávania

Uistite sa, že mapovanie pre **Projektové operácie integrácia projekt dodávateľ faktúra riadok export entity msdyn\_ projectvendorinvoicelines** používa verziu 1.0.0.4 alebo novšiu.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Povoľte funkčný kľúč pre kategórie obstarávania

Ak chcete povoliť funkciu používania kategórií obstarávania s objednávkami projektu, postupujte podľa týchto krokov.

1. V Dynamics 365 Finance otvorte súbor **Správa funkcií** pracovnom priestore.
1. V zozname funkcií nájdite **Použite kategórie obstarávania v projektových operáciách pre scenáre založené na zdrojoch/bez zásob** funkciu a potom vyberte **Povoliť**.

> [!IMPORTANT]
> Predpokladom je, že musíte povoliť aj **Povoľte čakajúce faktúry dodávateľa na projektových operáciách pre scenáre založené na zdrojoch/nezásoby** vlastnosť.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapujte kategórie projektov v hierarchii kategórií obstarávania

Podľa týchto krokov mapujte kategórie projektov na kategórie obstarávania v **Kategória obstarávania** hierarchia:

1. Ísť do **Obstarávanie a získavanie zdrojov \> Kategórie obstarávania**.
1. Vyberte **Upraviť hierarchiu kategórií**.
1. Vyberte požadovaný uzol hierarchie kategórií a potom na **Priraďte kategórie projektu** priraďte uzol ku kategórii projektu z **Čas**, **·**, alebo, **Projekt položky** kategória (t.j **Predvolený čas** alebo **Predvolené náklady** kategória).
1. Vyberte **Uložiť**.
1. Zatvorí stránku.

> [!NOTE]
> Mapovanie kategórie obstarávania na kategóriu projektu je voliteľné. Ak kategória obstarávania nie je namapovaná, systém použije hodnotu, ktorá je nastavená v **Položka** poli v **Predvolené nastavenia kategórie projektu** oddiel na **Projektové operácie na Dynamics 365 Zapojenie zákazníkov** kartu z **Projektový manažment a účtovné parametre** stránku.
