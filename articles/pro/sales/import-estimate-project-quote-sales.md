---
title: Importujte odhady z projektu do riadku cenovej ponuky projektu
description: Tento článok poskytuje informácie o tom, ako importovať odhady z projektu do riadku cenovej ponuky projektu.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 61c9660f18882d12a7da8965c23b65e408256219
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824506"
---
# <a name="import-estimates-from-a-project-to-a-project-quote-line"></a>Importujte odhady z projektu do riadku cenovej ponuky projektu 

_**Vzťahuje sa na:** Čiastočné nasadenie – dohoda o fakturácii pro forma, Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Ak je projekt vytvorený počas štádia predpredaja, môžete zvoliť importovanie finančného odhadu z projektu do riadka ponuky cenovej založenej na projekte.

1. Uistite sa, že riadok ponuky založenej na projekte obsahuje informácie o projekte v poli **Projekt**.
2. Na karte **Podrobnosti o riadku cenovej ponuky** vyberte **Importovať z odhadu projektu**.
3. Na otvorenej dialógovej stránke vyberte jednu z nasledujúcich možností súhrnu.

  - **Trieda transakcie**
  - **Kategória**
  - **Rola** 
  - **Projektová úloha**

Na základe vášho výberu sa skopíruje odhad z projektu pre všetky triedy transakcií zahrnutých v tomto riadku cenovej ponuky. Ak chcete skontrolovať, ktoré triedy transakcií sú zahrnuté, vyberte kartu **Všeobecné** na riadku cenovej ponuky založenej na projekte a skontrolujte hodnoty pre **Zahrnúť čas**, **Zahrnúť výdavky**, **Zahrnúť materiály** a **Zahrnúť poplatky**.  Ak chcete skontrolovať, ktoré úlohy sú zahrnuté, vyberte kartu **Fakturovateľné úlohy** v riadku cenovej ponuky.

V závislosti od priradených úloh a zahrnutých tried transakcií sa odhady pre tieto kombinácie úloh a tried transakcií importujú do riadka cenovej ponuky.

Keď importujete odhady, systém predvolene nastaví cenu na základe cenníkov projektu pripojených k cenovej ponuke a typu fakturácie nastaveného v riadku cenovej ponuky založenej na projekte. Ak je úloha, rola alebo kategória nastavená na riadku cenovej ponuky založenej na projekte ako nespoplatniteľná, importovaný riadok odhadu sa nastaví ako nespoplatniteľný a nebude sa zvyšovať k uvedenej hodnote riadka cenovej ponuky.

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
|||1. 10. 2020 | 3.34 | 840 | 2800 |

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
