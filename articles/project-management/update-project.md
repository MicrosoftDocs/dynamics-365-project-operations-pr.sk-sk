---
title: Aktualizácia projektu
description: Táto téma poskytuje informácie o aktualizácii projektov Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897831"
---
# <a name="update-a-project"></a>Aktualizácia projektu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Ďalej je uvedený súhrn polí, ktoré je možné aktualizovať po vytvorení projektu, a všetkých príslušných dôsledkov aktualizácií.

## <a name="project-detail-fields"></a>Polia podrobností projektu

- **Názov**: Názov projektu.
- **Popis**: Prehľad projektu.
- **Zákazník**: Spoločnosť, ktorej bude projekt dodaný.
- **Šablóna kalendára** : Pracovný čas projektu. Po zmene poľa sa prepočíta celý plán.
- **Mena**: Mena pre projekt. Toto pole je predvolené na základe meny definovanej v zmluvnej jednotke. Keď sa aktualizuje zmluvná jednotka, aktualizuje sa aj pole.
- **Zmluvná jednotka**: Organizačná jednotka, ktorá zastupuje skupinu spoločností alebo divízie, ktorá je primárne zodpovedná za získanie predaja a riadenie poskytovania práce a služieb zákazníkovi. 
- **Projektový manažér** : Člen projektového tímu, ktorý je oprávnený kontrolovať a schvaľovať časové zadania a výdavky.

## <a name="estimate-fields"></a>Polia odhadu

- **Odhadovaný dátum začatia**: Dátum začiatku projektu. Po aktualizácii tohto poľa sa všetky úlohy v projekte presunú úmerne s novým dátumom začatia.
- **Dátum dokončenia**: Dátum ukončenia projektu.
- **Úsilie**: Odhadované úsilie projektu. Po pridaní úloh do projektu už toto pole nie je možné upravovať.
- **Odhadované mzdové náklady**: Odhadované mzdové náklady projektu. Po pridaní mzdových nákladov do projektu už toto pole nie je možné upravovať.
- **Odhadované výdavky** : Odhadované výdavky na projekt. Po pridaní výdavkov do projektu už toto pole nie je možné upravovať.

## <a name="project-actual-fields"></a>Skutočné polia projektu
- **Skutočný začiatok** : Dátum zahájenia projektu.
- **Skutočný koniec**: Bude aktualizované po dokončení projektu.

## <a name="project-status-fields"></a>Polia pre stav projektu

- **Celkový stav projektu**: Celkový stav projektu poskytnutý projektovým manažérom.
- **Komentáre**: Popis týkajúci sa aktuálneho stavu projektu poskytnutý projektovým manažérom.

