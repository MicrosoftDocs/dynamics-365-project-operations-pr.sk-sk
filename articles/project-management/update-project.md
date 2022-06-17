---
title: Vytvorenie a aktualizácia projektu
description: Tento článok poskytuje informácie o aktualizácii projektov Projektové operácie.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911109"
---
# <a name="create-and-update-a-project"></a>Vytvorenie a aktualizácia projektu

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Nasleduje súhrn polí, ktoré je možné aktualizovať v projekte po jeho vytvorení. To zahŕňa aj všetky príslušné dôsledky založené na týchto aktualizáciách.

## <a name="project-detail-fields"></a>Polia podrobností projektu

- **Názov**: Názov projektu.
- **Popis**: Prehľad projektu.
- **Zákazník**: Spoločnosť, ktorej bude projekt dodaný.
- **Šablóna kalendára** : Pracovný čas projektu. Po zmene poľa sa prepočíta celý plán.
- **Mena**: Mena pre projekt. Predvolená hodnota pre toto pole je založená na mene, ktorá je definovaná v zmluvnej jednotke. Keď sa aktualizuje zmluvná jednotka, aktualizuje sa aj pole.
- **Zmluvná jednotka**: Organizačná jednotka, ktorá zastupuje skupinu spoločností alebo divízie, ktorá je primárne zodpovedná za získanie predaja a riadenie poskytovania práce a služieb zákazníkovi.  Ak nie je definovaná organizačná jednotka projektového manažéra, toto pole má predvolenú hodnotu definovanú v parametroch projektu.
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
