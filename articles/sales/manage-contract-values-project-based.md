---
title: Práca s riadkami zmluvy založenej na projekte
description: Táto téma poskytuje informácie o riadkoch zmluvy založenej na projekte.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 14d880eccd5547c122ebe37b63022e64fa2fb6fe
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181741"
---
# <a name="work-with-projectbased-contract-lines"></a>Práca s riadkami zmluvy založenej na projekte

Riadky zmluvy založené na projekte v Dynamics 365 Project Operations sú navrhnuté tak, aby uchovávali odhad a fakturačné dohody pre konkrétne komponenty projektovej úlohy na zákazke. Štruktúra riadka zmluvy založeného na projekte sa rozširuje pre odhady projektu a scenáre fakturácie s týmito konceptmi:

- Spôsob fakturácie
- Mapovanie projektov a úloh
- Zahrnuté triedy transakcií
- Limit, ktorý sa nesmie prekročiť
- Nastavenie účtovateľnosti
- Odhady pomocou podrobností riadku zmluvy
- Zákazníci v riadku zmluvy

Nasledujúce polia sú obsiahnuté na karte **Všeobecné** riadkov zmluvy založenej na projekte. Tieto polia pomáhajú vytvoriť základ pre podrobný základný odhad a mechanizmy fakturácie pre prácu založenú na projekte.

| Pole | Popis | Nadväzujúci vplyv |
| --- | --- | --- |
| **Názov** | Názov riadka zmluvy, ktorý identifikuje samostatnú zložku zmluvy, ktorá sa odhaduje. Pri projektovej zmluve vytvorenej z cenovej ponuky sa táto hodnota skopíruje z príslušnej hodnoty riadku cenovej ponuky založeného na projekte. | Hodnota tohto poľa je skopírovaná na riadok projektovej faktúry, ktorý je vytvorený z tohto riadka zmluvy pri vytváraní faktúry. |
| **Spôsob fakturácie** | V prípade projektovej zmluvy vytvorenej z cenovej ponuky sa táto hodnota skopíruje z príslušného poľa v riadku cenovej ponuky. Toto je množina možností, ktorá predstavuje dva hlavné modely uzatvárania zmlúv podporované aplikáciou Project Operations:</br>- **Pevná cena**</br>- **Čas a materiál** | Skutočná transakcia bude spracovaná na základe spôsobu fakturácie odkazovaného riadka zmluvy. Ak má riadok zmluvy, na ktorý odkazuje skutočná hodnota, časovú a materiálovú metódu fakturácie, vytvorí sa skutočný záznam o nákladoch a nevyfakturovaných predajoch. Ak má riadok zmluvy, na ktorý odkazuje skutočná hodnota, spôsob fakturácie s pevnou cenou, vytvorí sa iba skutočná hodnota nákladu. |
| **Project** | Toto pole sa používa na identifikáciu projektu, ktorý sa použije na vykonanie práce na tejto zákazke. | Hodnota v tomto poli sa použije v spojení s poľami **Zahrnuté úlohy** a **Zahrnuté triedy transakcií** na vyriešenie odkazu na riadok zmluvy na zázname riadka so skutočnou alebo odhadovanou hodnotou. |
| **Zahrnúť čas** | Príznak označuje, či sú na tomto riadku zmluvy zahrnuté časové transakcie alebo náklady na prácu vo vybratom projekte. Hodnota **Nie** označuje, že na tomto riadku zmluvy nebudú zahrnuté časové transakcie ani náklady na prácu. Hodnota **Áno** naznačuje, že budú. | Hodnota tohto poľa sa použije v spojení s projektom na vyriešenie odkazu na riadok zmluvy na zázname riadka so skutočnou alebo odhadovanou hodnotou. |
| **Zahrnúť výdavok** | Príznak označuje, či budú na tomto riadku zmluvy zahrnuté nákladové výdavky vo vybratom projekte. Hodnota **Nie** označuje, že na tomto riadku zmluvy nebudú zahrnuté nákladové výdavky. Hodnota **Áno** naznačuje, že budú. | Hodnota tohto poľa sa použije v spojení s projektom na vyriešenie odkazu na riadok zmluvy na zázname riadka so skutočnou alebo odhadovanou hodnotou. |
| **Zahrnúť poplatok** | Príznak označuje, či budú na tomto riadku zmluvy zahrnuté poplatky vo vybratom projekte. Hodnota **Nie** označuje, že na tomto riadku zmluvy nebudú zahrnuté poplatky. Hodnota **Áno** naznačuje, že budú. | Hodnota tohto poľa sa použije v spojení s projektom na vyriešenie odkazu na riadok zmluvy na zázname riadka so skutočnou alebo odhadovanou hodnotou. |
| **Zmluvná suma** | Na riadku zmluvy s pevnou cenou ide o dohodnutú hodnotu, ktorá bude zákazníkovi fakturovaná za všetky pracovné komponenty spojené s týmto riadkom zmluvy. Na riadku zmluvy s časom a materiálom je táto suma odhadovanou hodnotou toho, čo bude zákazníkovi fakturované za všetky pracovné komponenty spojené s týmto riadkom zmluvy. V prípade projektovej zmluvy vytvorenej z cenovej ponuky sa táto hodnota skopíruje z príslušného poľa v riadku cenovej ponuky. Ak má riadok zmluvy založený na projekte podrobnosti riadku, toto pole je uzamknuté pre úpravy a je zosumarizované z čiastky v podrobnostiach riadku zmluvy. | Ak má riadok zmluvy podrobnosti o riadku, je možné túto hodnotu upraviť zmenou čiastok v detaile riadku. Na riadku zmluvy s pevnou cenou sa táto hodnota používa na generovanie sumy pred zdanením v periodických medzníkoch na fakturovanie. |
| **Odhad dane** | Používateľ môže toto pole upraviť a do riadku zmluvy vložiť predpokladanú sumu dane. Ak má riadok zmluvy založený na projekte podrobnosti riadku, toto pole je uzamknuté pre úpravy a je zosumarizované z čiastky dane v podrobnostiach riadku zmluvy. | Ak má riadok zmluvy podrobnosti o riadku, je možné túto hodnotu upraviť zmenou čiastok dane v podrobnostiach riadka. Na riadku zmluvy s pevnou cenou sa táto hodnota používa na generovanie dane v periodických medzníkoch na fakturovanie. |
| **Zmluvná suma po zdanení** | Suma v riadku zmluvy po zdanení. Toto pole je iba na čítanie a počíta sa ako **Zmluvná suma + daň**. | Na riadku zmluvy s pevnou cenou sa táto hodnota používa na generovanie periodických medzníkoch na fakturovanie. |
| **Limit, ktorý sa nesmie prekročiť** | Používateľ môže toto pole upravovať a je k dispozícii iba na riadkoch zmlúv založených na projektoch, ktoré majú metódu fakturácie nastavenú ako čas a materiál. | Používateľ môže toto pole upraviť. Keď skutočný čas a výdavky odkazujú na tento riadok zmluvy pre čas a materiál, suma na skutočnom sa vyhodnotí oproti limitu na riadku tejto zmluvy, ktorý sa nesmie prekročiť, po zaúčtovaní už vynaložených a pridelených súm. |
| **Rozpočet zákazníka** | Toto pole sa dá upravovať a kopíruje sa zo zodpovedajúceho poľa na riadku cenovej ponuky, ak zmluva bola vytvorená z cenovej ponuky. | Toto pole slúži iba na informačné účely a nemá žiadny následný význam. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Pravidlo overenia možností na karte Všeobecné v riadkoch zmlúv založených na projektoch

Pravidlo: Projekt a určitá trieda transakcií môžu byť v zmluve zahrnuté iba v jednom riadku zmluvy založenej na projekte.

| Zmluva | Riadok zmluvy | Project | Zahrnúť čas | Zahrnúť výdavok | Zahrnúť poplatok | Platný/neplatný | Dôvod                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Áno          | Áno             | Áno         | Neplatný       | Porušuje pravidlo. Čas, výdavky a poplatky za projekt P1 sú zahrnuté v oboch riadkoch zmluvy, CL1 a CL2.                                                                                       |
| C1       | CL2           | P1      | Áno          | Áno             | Áno         | Neplatný       | Porušuje pravidlo. Čas, výdavky a poplatky za projekt P1 sú zahrnuté v oboch riadkoch zmluvy, CL1 a CL2.                                                                                       |
| C1       | CL1           | P1      | Áno          | No              | Áno         | Neplatný       | Porušuje pravidlo. Čas a poplatky za projekt P1 sú zahrnuté v oboch riadkoch zmluvy, CL1 a CL2.                                                                                                   |
| C1       | CL2           | P1      | Áno          | Áno             | Áno         | Neplatný       | Porušuje pravidlo. Čas a poplatky za projekt P1 sú zahrnuté v oboch riadkoch zmluvy, CL1 a CL2.                                                                                                   |
| C1       | CL1           | P1      | Áno          | No              | Áno         | Platné           | Čas a poplatky za projekt P1 sú zahrnuté v CL1. Výdavky na projekt P1 sú zahrnuté v CL2. </br>   Čo sa týka každého riadku zmluvy, nedochádza k žiadnemu prekrývaniu, a preto je to platné.  |
| C1       | CL2           | P1      | No           | Áno             | No          | Platné           | Čas a poplatky za projekt P1 sú zahrnuté v CL1. Výdavky na projekt P1 sú zahrnuté v CL2. </br>   Čo sa týka každého riadku zmluvy, nedochádza k žiadnemu prekrývaniu, a preto je to platné.  |
| C1       | CL1           | P1      | Áno          | Áno             | Áno         | Neplatný       | Porušuje pravidlo. Čas, výdavky a poplatky za projekt P1 sú zahrnuté v riadkoch dvoch zmlúv.                                                                                               |
| CL2      | CL2           | P1      | Áno          | Áno             | Áno         | Neplatný       | Porušuje pravidlo. Čas, výdavky a poplatky za projekt P1 sú zahrnuté v riadkoch dvoch zmlúv.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]