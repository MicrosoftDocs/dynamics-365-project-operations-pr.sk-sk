---
title: Prehľad režimov správy zdrojov
description: Táto téma poskytuje informácie o funkciách Správa zdrojov v Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084252"
---
# <a name="resource-management-modes-overview"></a>Prehľad režimov správy zdrojov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_


Dynamics 365 Project Operations podporuje dva režimy, aby ste mohli vykonať celkový tok rezervácií. Režim správy je definovaný ako parameter projektu a je možné ho upraviť, ak sa zmenia vaše obchodné potreby.    

## <a name="central-mode"></a>Centrálny režim
Pre organizácie, ktoré centralizujú pridelenie zdrojov k projektom poskytuje centrálny režim spôsob, ako zabezpečiť, aby manažéri projektu mohli definovať požiadavky na zdroje na úrovni projektu. Splnenie požiadaviek na zdroje sa deleguje na manažéra zdrojov. Projektoví manažéri môžu prijímať alebo odmietať zdroje, ktoré navrhuje manažér zdrojov.

![Centrálny režim](./media/resource-management-central.png)

Informácie o správe zdrojov v centrálnom režime nájdete na:

- [Priradenie všeobecných rezervovateľných zdrojov k úlohe a generovanie požiadaviek zdrojov](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervácia pomenovaných zdrojov z požiadaviek zdrojov](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Odoslanie žiadosti o zdroj](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Splnenie požiadavky na zdroj](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Prijatie alebo odmietnutie navrhovaného prostriedku projektu zo žiadosti o prostriedok](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybridný režim
Pre organizácie, ktoré požadujú flexibilitu pri prideľovaní zdrojov, umožňuje hybridný režim rezervovať zdroje projektovým manažérom aj manažérom zdrojov.

![Hybridný režim](./media/resource-management-hybrid.png)

Okrem podporovaného procesu v centrálnom režime nájdete v nasledujúcich témach správu všetkých ostatných podporovaných tokov rezervácie v hybridnom režime:

Priama rezervácia zdroja pre projekt:
- [Rezervácia pomenovaných rezervovateľných zdrojov pre projektový tímu a priradenie úloh](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Rezervácia zdroja z požiadaviek zdrojov:
- [Priradenie všeobecných rezervovateľných zdrojov k úlohe a generovanie požiadaviek zdrojov](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervácia pomenovaných zdrojov z požiadaviek zdrojov](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
