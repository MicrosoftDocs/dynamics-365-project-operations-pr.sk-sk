---
title: Konfigurácia účtovníctva pre interné projekty
description: Táto téma poskytuje informácie o tom, ako nastaviť účtovné postupy pre interné projekty v aplikácii Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287617"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurácia účtovníctva pre interné projekty

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Interné projekty umožňujú spoločnostiam sledovať náklady spojené s činnosťami, ktoré sa zákazníkom neúčtujú. Príklady interných projektov zahŕňajú:

- Vývoj produktu, napríklad mobilnej aplikácie, a sledovanie nákladov spojených s vývojom.
- Správa času a výdavkov pred predajom. Tento interný projekt pred predajom je možné neskôr previesť na fakturovateľný projekt v prípade získania cenovej ponuky.

Akýkoľvek projekt, ktorý nie je spojený so zmluvou v rámci Dynamics 365 Project Operations, sa považuje za interný. Profily nákladov a výnosov projektu sa nepoužívajú na určenie účtovných pravidiel projektu. Náklady na interné projekty sa vždy účtujú pomocou zásad ziskov a strát. Účty hlavnej knihy pre zverejňovania sú definované na stránke **Nastavenia zverejňovania v hlavnej knihe**.

- Časové transakcie sa zverejňujú zaúčtovaním účtu **Náklady** a pripísaním na účet **Alokácia miezd**.
- Výdavkové transakcie sa zverejňujú zaúčtovaním účtu **Náklady** a pripísaním na **Účet s odchýlkami pre výdavky**.

Po pridaní transakcií do projektu, ak je projekt spojený so zmluvou o projekte, systém vráti všetky akumulované transakcie a vytvorí nové fakturovateľné transakcie. Fakturovateľné transakcie sa riadia účtovnými pravidlami definovanými v príslušnom profile nákladov a výnosov projektu.




[!INCLUDE[footer-include](../includes/footer-banner.md)]