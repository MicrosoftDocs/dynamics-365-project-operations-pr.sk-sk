---
title: Konfigurácia účtovníctva pre interné projekty
description: Táto téma poskytuje informácie o tom, ako nastaviť účtovné postupy pre interné projekty v aplikácii Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012875"
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
