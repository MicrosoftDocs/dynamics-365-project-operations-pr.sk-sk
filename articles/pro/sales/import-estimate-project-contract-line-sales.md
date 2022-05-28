---
title: Import odhadu do riadka zmluvy založenej na projekte – čiastočné
description: Táto téma poskytuje informácie o importovaní finančných odhadov z projektu do riadka zmluvy.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 52abaa785b50b914e7813aaf4660504ee99129d6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582085"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Import odhadu do riadka zmluvy založenej na projekte – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

V Dynamics 365 Project Operations si môžete importovať odhady z projektu do riadka zmluvy založenej na projekte.

1. Overte si, či bolo vyplnené pole **Projekt** v riadku zmluvy založenej na projekte.
2. Na karte **Podrobnosti o riadku zmluvy** vo vedľajšej mriežke vyberte kartu **Importovať z odhadu projektu**. Otvorí sa dialógové okno s možnosťami sumarizácie. Dostupné možnosti sumarizácie sú **Trieda transakcie**, **Kategória**, **Rola** a **Projektová úloha**.
3. Na základe výberu pre sumarizáciu sa prekopíruje odhad z projektu pre všetky triedy transakcií a úlohy zahrnuté v tomto riadku zmluvy. Ak chcete skontrolovať, ktoré triedy transakcií sú zahrnuté, na karte **Všeobecné** v riadku zmluvy založenej na projekte skontrolujte hodnoty v poliach **Zahrnúť čas**, **Zahrnúť výdavky** a **Zahrnúť poplatky**. 
4. Ak chcete zistiť, ktoré úlohy sú zahrnuté, vyberte kartu **Fakturovateľné úlohy** v riadku zmluvy. Na základe priradených úloh, ktoré majú pole **Zahrnuté triedy transakcií** nastavené na **Áno** sa všetky odhady pre tieto kombinácie úloh a tried transakcií importujú do riadku zmluvy.

Keď importujete odhady, systém predvolene nastaví cenu na základe cenníkov projektu pripojených k zmluve a typu fakturácie nastaveného v riadku zmluvy. Ak je úloha, rola alebo kategória v riadku zmluvy nastavená ako nespoplatniteľná, importovaný riadok odhadu je nespoplatniteľný a nebude sa pripočítavať k zmluvnej hodnote v riadku zmluvy.

Ak riadok zmluvy obsahuje podrobnosti o riadku, polia **Hodnota zmluvy** a **Odhadovaná daň** v riadku zmluvy sa zosumarizujú a nebude možné ich upravovať.

Keď je vybratých viac možností sumarizácie, systém sa pokúsi o sumarizáciu podľa všetkých vybratých možností. Výsledkom výstupu sumarizácie je viac importovaných riadkov zmluvy, ako keby ste vybrali iba jednu možnosť sumarizácie.

Napríklad, ak má projekt nasledujúce odhadované riadky výdavkov.

| Úloha | Kategória | Dátum | Počet | Jednotková cena | Množstvo |
| --- | --- | --- | --- | --- | --- |
| Úloha A | Letenky | 1. 10. 2020 | 4 | 400 | 1600 |
| Úloha B | Hotel | 1. 10. 2020 | 4 | 200 | 800 |
| Úloha C | Hotel | 1. 11. 2020 | 2 | 200 | 400 |

Keď sa používateľ rozhodne sumarizovať podľa **Triedy transakcií**, importujú sa nasledujúce informácie.

| Úloha | Kategória | Dátum | Počet | Jednotková cena | Množstvo |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 1. 10. 2020 | 3.34 | 840 | 2800 |

Keď sa používateľ rozhodne sumarizovať podľa **Triedy transakcií** a **Kategórie**, importujú sa nasledujúce informácie.

| Úloha | Kategória | Dátum | Počet | Jednotková cena | Množstvo |
| --- | --- | --- | --- | --- | --- |
| Úloha A | Letenky | 1. 10. 2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 1. 10. 2020 | 6 | 200 | 1200 |

Keď sa používateľ rozhodne sumarizovať podľa položiek **Trieda transakcií**, **Kategória** a **Úloha listového uzla**, importujú sa nasledujúce položky. Všimnite si, že tento výsledok je rovnaký ako výsledok projektu:

| Úloha | Kategória | Dátum | Počet | Jednotková cena | Množstvo |
| --- | --- | --- | --- | --- | --- |
| Úloha A | Letenky | 1. 10. 2020 | 4 | 400 | 1600 |
| Úloha B | Hotel | 1. 10. 2020 | 4 | 200 | 800 |
| Úloha C | Hotel | 1. 11. 2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]