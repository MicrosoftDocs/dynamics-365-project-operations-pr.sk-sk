---
title: Použitie kategórií obstarávania s nákupnými objednávkami projektu a čakajúcimi faktúrami dodávateľa
description: Tento článok popisuje, ako nakonfigurovať kategórie obstarávania, ktoré možno použiť s nákupnými objednávkami projektu a čakajúcimi faktúrami dodávateľa.
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
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Použitie kategórií obstarávania s nákupnými objednávkami projektu a čakajúcimi faktúrami dodávateľa

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Odborníci na nákup môžu vytvárať a udržiavať katalógy položiek a služieb, ktoré možno použiť v nákupných objednávkach projektu a čakajúcich faktúrach dodávateľa. [Katalógy obstarávania](/dynamics365/supply-chain/procurement/procurement-catalogs) vám poskytujú jednoduchý spôsob kategorizácie nákupov bez toho, aby ste museli konfigurovať a používať vydaný katalóg produktov. Každá kategória obstarávania môže byť priradená ku kategórii projektu pre transakcie času, nákladov alebo položiek. Po zaúčtovaní čakajúcej faktúry dodávateľa, ktorá používa kategóriu obstarávania, systém vytvorí skutočné údaje o čase, výdavkoch alebo materiáli projektu, transakcie projektu a položky vedľajšej účtovnej knihy.

## <a name="minimum-version-requirements"></a>Minimálne požiadavky na verziu

Nasledujúce verzie sú potrebné na používanie kategórií obstarávania s projektovými objednávkami pre Microsoft Dynamics 365 Project Operations scenáre neskladované/založené na zdrojoch:

- Riešenie Project Operations Dataverse, verzia 4.41.0.45 alebo novšia
- Prostredie na riadenie financií a prevádzok verzie 10.0.26 alebo novšej

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Spustenie máp duálneho zápisu pre podporu kategórií obstarávania

Uistite sa, že mapovanie pre **riadok entity exportu faktúr projektu dodávateľa projektu Project Operations msdyn\_projectvendorinvoicelines** používa verziu 1.0.0.4 alebo novšiu.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Povolenie kľúča funkcie pre kategórie obstarávania

Ak chcete povoliť funkciu používania kategórií obstarávania s objednávkami projektu, postupujte podľa týchto krokov.

1. V Dynamics 365 Finance otvorte pracovný priestor **Správa funkcie**.
1. V zozname funkcií nájdite funkciu **Použitie kategórií obstarávania v Project Operations pre scenáre založené na zdrojoch/neskladované materiály** a stlačte možnosť **Povoliť**.

> [!IMPORTANT]
> Predpokladom je povolenie funkcie **Povoliť faktúry dodávateľa v Project Operations pre scenáre založené na zdrojoch/neskladované materiály**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapovanie kategórií projektov v hierarchii kategórií obstarávania

Podľa týchto krokov mapujte kategórie projektov na kategórie obstarávania v hierarchii **Kategória obstarávania**:

1. Prejdite do **Obstarávanie a získavanie zdrojov \> Kategórie obstarávania**.
1. Vyberte **Upraviť hierarchiu kategórií**.
1. Vyberte požadovaný uzol hierarchie kategórií a potom na karte **Priradiť kategórie projektu** priraďte uzol ku kategórii projektu z kategórie **Čas**, **Výdavok** alebo **Projekt položky** (t. j. kategória **Predvolený čas** alebo **Predvolené náklady**).
1. Vyberte **Uložiť**.
1. Zatvorí stránku.

> [!NOTE]
> Mapovanie kategórie obstarávania na kategóriu projektu je voliteľné. Ak kategória obstarávania nie je namapovaná, systém použije hodnotu, ktorá je nastavená v poli **Položka** v časti **Predvolené hodnoty kategórie projektu** na karte **Project Operations v Dynamics 365 Customer Engagement** na stránke **Parametre projektového riadenia a účtovníctva**.
