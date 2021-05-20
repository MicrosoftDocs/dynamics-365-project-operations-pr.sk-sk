---
title: Prehľad režimov správy zdrojov
description: Táto téma poskytuje informácie o funkcii Správa zdrojov v aplikácii Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d132bcbef5421202d2f4899091f0dc75166dd66
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949968"
---
# <a name="resource-management-modes-overview"></a>Prehľad režimov správy zdrojov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_


Dynamics 365 Project Operations podporuje dva režimy, aby ste mohli vykonať celkový postup rezervácie. Režim správy je definovaný ako parameter projektu a je možné ho upraviť, ak sa zmenia vaše obchodné potreby.    

## <a name="central-mode"></a>Centrálny režim
Pre organizácie, ktoré centralizujú pridelenie zdrojov k projektom poskytuje centrálny režim spôsob, ako zabezpečiť, aby manažéri projektu mohli definovať požiadavky na zdroje na úrovni projektu. Splnenie požiadaviek na zdroje sa deleguje na manažéra zdrojov. Projektoví manažéri môžu prijímať alebo odmietať zdroje, ktoré navrhuje manažér zdrojov.

![Centrálny režim](./media/resource-management-central.png)

Informácie o správe zdrojov v centrálnom režime nájdete na:

- [Priradenie všeobecných rezervovateľných zdrojov k úlohe a generovanie požiadaviek zdrojov](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervácia pomenovaných zdrojov z požiadaviek zdrojov](/dynamics365/project-service/book-named-resource)
- [Odoslanie žiadosti o zdroj](/dynamics365/project-service/submit-resource-request)
- [Splnenie požiadavky na zdroj](/dynamics365/project-service/resource-management-fulfill-requests)
- [Prijatie alebo odmietnutie navrhovaného prostriedku projektu zo žiadosti o prostriedok](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybridný režim
Pre organizácie, ktoré požadujú flexibilitu pri prideľovaní zdrojov, umožňuje hybridný režim rezervovať zdroje projektovým manažérom aj manažérom zdrojov.

![Hybridný režim](./media/resource-management-hybrid.png)

Okrem podporovaného procesu v centrálnom režime nájdete v nasledujúcich témach správu všetkých ostatných podporovaných tokov rezervácie v hybridnom režime:

Priama rezervácia zdroja pre projekt:
- [Rezervácia pomenovaných rezervovateľných zdrojov pre projektový tímu a priradenie úloh](/dynamics365/project-service/assign-named-bookable-resource)

Rezervácia zdroja z požiadaviek zdrojov:
- [Priradenie všeobecných rezervovateľných zdrojov k úlohe a generovanie požiadaviek zdrojov](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervácia pomenovaných zdrojov z požiadaviek zdrojov](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]