---
title: Projekty odhadov výnosov s pevnou cenou
description: Tento článok poskytuje informácie o výnosoch s pevnou cenou v projektoch.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928405"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projekty odhadov výnosov s pevnou cenou 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Keď vytvoríte riadok projektov zmluvy s nasledujúcimi atribútmi v Dynamics 365 Project Operations v rámci Microsoft Dataverse, systém automaticky vytvorí projekt odhadu výnosov s pevnou cenou. Informácie v tomto projekte vychádzajú z tohto:

  - Metóda fakturácie s pevnou cenou.
  - Priradený projekt.
  - Aspoň jeden míľnik definovaný na karte **Plán faktúry** na stránke **Riadok projektovej zmluvy**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Kontrola projektov odhadov výnosov s pevnou cenou
Ak chcete skontrolovať projekty odhadov výnosov s pevnou cenou, postupujte takto:

1. V prostredí Dynamics 365 Finance prejdite na **Projektový manažment a účtovníctvo** > **Projekty** > **Projekty odhadov výnosov s pevnou cenou**.
2. Vyberte projekt, ktorý chcete zobraziť, a dvojitým kliknutím na **Odhad ID projektu** otvorte záznam a skontrolujte podrobnosti o projekte.
3. Rozbaľte kartu **Projekt**. Jeden projekt uvidíte v mriežke **Vybrané projekty**. Systém to používa ako predvolený projekt, pretože ide o projekt priradený k riadku projektovej zmluvy. 
4. Ak chcete zmeniť pridruženie, vyberte ďalšie projekty a pridajte ich do mriežky **Vybrané projekty**. Ak je v tejto mriežke vybratých viac projektov, vypočíta sa percento dokončenia projektu a odhady výnosov pre všetky vybrané projekty.

  Náklady na projekt, profil výnosov, šablónu nákladov a kód obdobia je možné nastaviť ručne. Ak nie sú nastavené ručne, hodnoty sa nastavia predvolene počas prvého výpočtu odhadu pre projekt pomocou pravidiel nakonfigurovaných pre profily nákladov a výnosov projektu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]