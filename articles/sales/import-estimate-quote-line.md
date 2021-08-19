---
title: Import odhadov pre projekt do riadka cenovej ponuky
description: Táto téma poskytuje informácie o tom, importovať odhady z projektu do riadka projektovej cenovej ponuky.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a9ac27b7694927f9cea88b49310f3106fbc6542cc0f7f1756744b970358c1057
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993530"
---
# <a name="import-estimates-for-a-project-to-a-project-quote-line"></a>Import odhadov pre projekt do riadka cenovej ponuky

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_


Ak je projekt vytvorený počas štádia predpredaja, môžete zvoliť importovanie finančného odhadu z projektu do riadka ponuky cenovej založenej na projekte.

1. Uistite sa, že riadok ponuky založenej na projekte obsahuje informácie o projekte v poli **Projekt**.
2. Na karte **Podrobnosti o riadku cenovej ponuky** vyberte **Importovať z odhadu projektu**.
3. Na otvorenej dialógovej stránke vyberte jednu z nasledujúcich možností súhrnu:

  - **Trieda transakcie**
  - **Kategória**
  - **Rola** 
  - **Projektová úloha**

Na základe vášho výberu sa skopíruje odhad z projektu pre všetky triedy transakcií zahrnutých v tomto riadku cenovej ponuky. Ak chcete skontrolovať, ktoré triedy transakcií sú zahrnuté, vyberte kartu **Všeobecné** na riadku cenovej ponuky založenej na projekte a skontrolujte hodnoty pre položky **Zahrnúť čas**, **Zahrnúť výdavky** a **Zahrnúť poplatky**.

Keď importujete odhady, systém predvolene nastaví cenu na základe cenníkov projektu pripojených k cenovej ponuke a typu fakturácie nastaveného v riadku cenovej ponuky založenej na projekte. Ak je rola alebo kategória nastavená na riadku cenovej ponuky založenej na projekte ako nespoplatniteľná, importovaný riadok odhadu sa nastaví ako nespoplatniteľný a nebude sa zvyšovať k uvedenej hodnote riadka cenovej ponuky.

Ak riadok ponuky obsahuje podrobnosti o riadku, polia **Hodnota cenovej ponuky** a **Odhadovaná daň** v riadku ponuky sa zosumarizujú a nebude možné ich upravovať.

Keď je vybratých viac možností sumarizácie, systém sa pokúsi o sumarizáciu podľa všetkých vybratých možností. Výsledkom je, že výstup importovaných riadkov cenových ponúk bude väčší, ako keby ste vybrali iba jednu možnosť sumarizácie.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
