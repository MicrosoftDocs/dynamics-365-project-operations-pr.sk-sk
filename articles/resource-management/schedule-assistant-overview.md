---
title: Prehľad asistenta plánovania
description: Táto téma poskytuje informácie o práci s asistentom plánovania pri rezervácii zdrojov.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908574"
---
# <a name="schedule-assistant-overview"></a>Prehľad asistenta plánovania

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Asistent plánovania sa používa na rezerváciu zdrojov na základe požiadaviek definovaných projektovým manažérom. Asistent plánovania sa pri hľadaní zdroja spolieha na parametre uvedené v požiadavke na zdroj. Asistent plánovania odporúča zdroje, ktoré zodpovedajú príslušným požiadavkám, ako sú časové okná alebo potrebné zručnosti.

Po identifikácii vhodných zdrojov môže manažér zdrojov alebo projektu rezervovať zdroj pre prácu.

## <a name="prerequisites"></a>Predpoklady

Asistent plánovania je súčasťou riešenia Universal Resource Scheduling. Toto riešenie je zahrnuté a nainštalované spolu s Dynamics 365 Project Operations, Dynamics 365 Field Service a Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Zosúlaďovanie požiadaviek a zdrojov

Vygenerovaná požiadavka na zdroj je založená na podrobnostiach, ako napríklad:

-   Charakteristiky
-   Roly
-   Organizačné jednotky
-   Predvoľby zdrojov
-   Obrysy úsilia
-   Časové pásmo

Asistent plánovania používa tieto podrobnosti na filtrovanie zdrojov.

## <a name="launch-the-schedule-assistant"></a>Spustite asistenta plánovania

Existujú dva spôsoby spustenia asistenta plánovania. Ak používate hybridný režim, v mriežke člena tímu môžete vybrať ľubovoľného člena tímu s nesplnenou požiadavkou na zdroje a potom vybrať možnosť **Rezervovať**. Ak používate centrálny režim, správca zdrojov vyhľadá a vyberie zdroj.

## <a name="schedule-assistant-filters"></a>Filtre asistenta plánovania

Po spustení asistenta plánovania sa podrobnosti z požiadavky na zdroj zobrazia ako filtrované hodnoty na ľavej table. Správca zdrojov alebo projektový manažér môže doladiť výsledky úpravou filtrov tak, aby vyhovovali potrebám plánovania.

Na table filtra sú zobrazené možnosti súvisiace s prácou, vrátane:

-   Začiatok a koniec práce
-   Charakteristiky
-   Roly
-   Organizačné jednotky
-   Spoločnosť zaisťujúca zdroje
-   Typy zdrojov
-   Preferované zdroje
