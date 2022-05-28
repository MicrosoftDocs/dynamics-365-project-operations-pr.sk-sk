---
title: Odstránenie odhadu projektu
description: Táto téma poskytuje informácie o odstránení odhadu projektu po jeho dokončení.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 267b5ffab7ef3a6776c31100deea81fb523752b6
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684109"
---
# <a name="eliminate-a-project-estimate"></a>Odstránenie odhadu projektu

[!include [banner](../includes/banner.md)]

Odhady projektu poskytujú finančné náhľady pre prácu, ktorá sa odhaduje a plánuje pre projekt. Ak chcete pracovať s odhadmi projektu, musíte pripojiť projekt k projektu odhadu. Projekt odhadu je vždy založený na existujúcom projekte, avšak na jeden projekt odhadu sa môže vzťahovať viac projektov. K projektom odhadu je možné pripojiť iba investičné projekty s pevnou cenou a tieto projekty musia patriť do rovnakej projektovej skupiny ako projekt odhadu.

Ak chcete vylúčiť projekt odhadu, musí byť dokončený. Nasledujúce kroky vysvetľujú, ako odstrániť odhad.

1. Prejdite do časti **Riadenie projektu a účtovníctvo** > **Všetky projekty** a otvorte projekt. 
2. Na karte **Spravovať** vyberte **Odhady** a na stránke **Odhad** vyberte možnosť **Eliminovať**.
3. Na stránke **Odstrániť odhad** na karte **Všeobecné** nastavte nasledujúce možnosti:

   - **Kód obdobia**: Vyberte kód obdobia a vyberte vhodné projekty odhadu. 
   - **Dátum odhadu** : Vyberte vhodný dátum odhadu na odstránenie.
   - **Eliminovať varovaniami WIP**: Túto možnosť povoľte, ak chcete dostávať oznámenie, keď bude eliminovaný odhad spojený s prebiehajúcou prácou (WIP). Ak táto možnosť nie je povolená, eliminovanie nemôže pokračovať, ak existujú neodhadnuté transakcie. 
   > [!NOTE]
   > Táto možnosť je k dispozícii, iba ak sa na projekt odhadu použije eliminácia. Nie je k dispozícii, ak používate pravidelné zverejňovanie zverejňovania. Toto nastavenie funguje s nastaveniami na karte **Odhad** na stránke **Parametre projektu** v skupine poľa **Povoliť eliminovanie, ak existujú neodhadované transakcie**.
   - **Nastaviť etapu na dokončenú**: Povolením tejto možnosti nastavíte po spustení eliminácie etapu projektu odhadu na **Dokončený**.
   - **Vytlačiť zoznam odhadov**: Vyberte informácie, ktoré sa majú zahrnúť pri vytlačení zoznamu odhadov.
   - **Zobraziť Infolog**: Povolením tejto možnosti zobrazíte Infolog.
   - **Dátum zverejnenia**: Vyberte dátum zverejnenia odhadu v hlavnej knihe.

4.  Vyberte položku **OK**.
5. Po dokončení procesu eliminácie sa projekt eliminovaného odhadu zobrazí so zápornou hodnotou. 

Ak ste nemali v úmysle eliminovať odhad, môžete vybrať eliminovaný odhad a vybrať **Vrátiť eliminovanie**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]