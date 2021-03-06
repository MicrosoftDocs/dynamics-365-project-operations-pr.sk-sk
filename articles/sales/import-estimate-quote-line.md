---
title: Importovanie odhadov projektu do riadka cenovej ponuky na základe projektu
description: Táto téma poskytuje informácie o importe odhadov z projektu do riadka cenovej ponuky.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908579"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importovanie odhadov projektu do riadka cenovej ponuky na základe projektu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_


Ak je projekt vytvorený počas štádia predpredaja, môžete zvoliť importovanie finančného odhadu z projektu do riadka ponuky cenovej založenej na projekte.

1. Uistite sa, že riadok ponuky založenej na projekte obsahuje informácie o projekte v poli **Projekt**.
2. Na karte **Podrobnosti o riadku cenovej ponuky** vyberte **Importovať z odhadu projektu**.
3. Na otvorenej dialógovej stránke vyberte jednu z nasledujúcich možností súhrnu.

  - **Trieda transakcie**
  - **Kategória**
  - **Rola** 
  - **Projektová úloha**

Na základe vášho výberu sa skopíruje odhad z projektu pre všetky triedy transakcií zahrnutých v tomto riadku cenovej ponuky. Ak chcete skontrolovať, ktoré triedy transakcií sú zahrnuté, vyberte kartu **Všeobecné** na riadku cenovej ponuky založenej na projekte a skontrolujte hodnoty pre položky **Zahrnúť čas**, **Zahrnúť výdavky** a **Zahrnúť poplatky**.

Keď importujete odhady, systém predvolene nastaví cenu na základe cenníkov projektu pripojených k cenovej ponuke a typu fakturácie nastaveného v riadku cenovej ponuky založenej na projekte. Ak je rola alebo kategória nastavená na riadku cenovej ponuky založenej na projekte ako nespoplatniteľná, importovaný riadok odhadu sa nastaví ako nespoplatniteľný a nebude sa zvyšovať k uvedenej hodnote riadka cenovej ponuky.

Ak riadok ponuky obsahuje podrobnosti o riadku, polia **Hodnota cenovej ponuky** a **Odhadovaná daň** v riadku ponuky sa zosumarizujú a nebude možné ich upravovať.

Keď je vybratých viac možností sumarizácie, funkcia sumarizácie sa pokúsi o sumarizáciu podľa všetkých vybratých možností. To znamená, že výstup importovaných riadkov cenových ponúk bude väčší, ako keby ste vybrali iba jednu možnosť sumarizácie.

Napríklad, ak má projekt nasledujúce odhadované riadky výdavkov.

| Úloha | Kategória | Dátum | Počet | Jednotková cena | Množstvo |
| --- | --- | --- | --- | --- | --- |
| Úloha A | Letenky | 1. 10. 2020 | 4 | 400 | 1600 |
| Úloha B | Hotel | 1. 10. 2020 | 4 | 200 | 800 |
| Úloha C | Hotel | 1. 11. 2020 | 2 | 200 | 400 |

Keď sa používateľ rozhodne sumarizovať podľa triedy transakcií, importujú sa nasledujúce informácie.

| Úloha | Kategória | Dátum | Počet | Jednotková cena | Množstvo |
| --- | --- | --- | --- | --- | --- |
| | | 1. 10. 2020 | 3.34 | 840 | 2800 |

Keď sa používateľ rozhodne sumarizovať podľa triedy transakcií a kategórie, importujú sa nasledujúce informácie.

| Úloha | Kategória | Dátum | Počet | Jednotková cena | Množstvo |
| --- | --- | --- | --- | --- | --- |
| Úloha A | Letenky | 1. 10. 2020 | 4 | 400 | 1600 |
| | Hotel | 1. 10. 2020 | 6 | 200 | 1200 |

Keď sa používateľ rozhodne sumarizovať podľa triedy transakcií, kategórie a úlohy listového uzla, importujú sa nasledujúce informácie. Všimnite si, že tento výsledok je rovnaký ako výsledok projektu.

| Úloha | Kategória | Dátum | Počet | Jednotková cena | Množstvo |
| --- | --- | --- | --- | --- | --- |
| Úloha A | Letenky | 1. 10. 2020 | 4 | 400 | 1600 |
| Úloha B | Hotel | 1. 10. 2020 | 4 | 200 | 800 |
| Úloha C | Hotel | 1. 11. 2020 | 2 | 200 | 400 |