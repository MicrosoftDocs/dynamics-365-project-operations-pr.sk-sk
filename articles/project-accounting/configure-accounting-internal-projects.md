---
title: Konfigurácia účtovníctva pre interné projekty
description: Tento článok poskytuje informácie o tom, ako nastaviť účtovné postupy pre interné projekty v Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919481"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurácia účtovníctva pre interné projekty

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Interné projekty umožňujú spoločnostiam sledovať náklady spojené s činnosťami, ktoré sa zákazníkom neúčtujú. Príklady interných projektov zahŕňajú:

- Vývoj produktu, napríklad mobilnej aplikácie, a sledovanie nákladov spojených s vývojom.
- Správa času a výdavkov pred predajom. Tento interný projekt pred predajom je možné neskôr previesť na fakturovateľný projekt v prípade získania cenovej ponuky.

Akýkoľvek projekt, ktorý nie je spojený so zmluvou v rámci Dynamics 365 Project Operations, sa považuje za interný. Profily nákladov a výnosov projektu sa nepoužívajú na určenie účtovných pravidiel projektu. Náklady na interné projekty sa vždy účtujú pomocou zásad ziskov a strát. Účty hlavnej knihy pre zverejňovania sú definované na stránke **Nastavenia zverejňovania v hlavnej knihe**.

- Časové transakcie sa zverejňujú zaúčtovaním účtu **Náklady** a pripísaním na účet **Alokácia miezd**.
- Výdavkové transakcie sa zverejňujú zaúčtovaním účtu **Náklady** a pripísaním na **Účet s odchýlkami pre výdavky**.
- Transakcie položiek sa účtujú na ťarchu účtu **Náklady** a pripisujú na účet **Náklady – položka**.

Po pridaní transakcií do projektu, ak je projekt spojený so zmluvou o projekte, systém vráti všetky akumulované transakcie a vytvorí nové fakturovateľné transakcie. Fakturovateľné transakcie sa riadia účtovnými pravidlami definovanými v príslušnom profile nákladov a výnosov projektu.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
