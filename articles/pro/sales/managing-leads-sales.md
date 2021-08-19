---
title: Správa potenciálnych zákazníkov – čiastočné
description: Táto téma poskytuje informácie o správe potenciálnych zákazníkov na základe projektu (pro).
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 218461e6b2013b014d59e2846fe19681d785771aa82284db33ff18c8b6b83946
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991415"
---
# <a name="manage-leads---lite"></a>Správa potenciálnych zákazníkov – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Potenciálni zákazníci na základe projektu môžu byť spravovaní a kvalifikovaní v Project Operations. Proces riadenia potenciálnych zákazníkov zahŕňa vytváranie potenciálnych zákazníkov na základe práce a kvalifikáciu týchto potenciálnych zákazníkov. 

## <a name="list-of-project-sales-leads"></a>Zoznam potenciálnych zákazníkov projektu

V časti **Predaj** na ľavej navigačnej table otvorte stránku so zoznamom **Potenciálni zákazníci** na zobrazenie zoznamu všetkých záznamov potenciálnych zákazníkov v systéme. Potenciálni zákazníci v zozname sú založení na práci a iné typy potenciálnych zákazníkov, ktoré je možné vytvoriť, ak máte tiež aplikácie Dynamics 365 Sales alebo Dynamics 365 Field Service.

Môžete vytvoriť filtrované zobrazenie na zobrazenie iba potenciálnych zákazníkov na základe projektu vytvorením filtra pre hodnotu **Typ**. Môžete napríklad vybrať, aby sa zobrazovali iba potenciálni zákazníci na základe práce.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Vytvorenie nového potenciálneho zákazníka pre dohodu na základe projektu

Keď je potenciálny zákazník na základe projektu kvalifikovaný, vytvorí sa príležitosť a obchodný vzťah. Príležitosť na základe projektu je východiskovým bodom pre aktivity zamerané na predaj vo fáze Príležitosť. Príležitosti založené na projekte majú jedinečné možnosti, ktoré sú potrebné na predaj projektovej úlohy. Medzi tieto možnosti patria:

- Spôsoby fakturácie pre čas a materiál a za pevnú cenu
- Viacnásobné účinné cenníky ľudských zdrojov, výdavkov a materiálu vynaloženého na projekty.

Ak chcete, aby kvalifikovaný potenciálny zákazník automaticky vytvoril príležitosť, pri vytváraní potenciálneho zákazníka nastavte atribút **Typ** na **Založené na práci**. Ak zvolíte iný typ, potenciálny zákazník nevytvorí príležitosť založenú na projekte, ak bude kvalifikovaný. Ak sa príležitosť založená na projekte nevytvorí, možnosti súvisiace s možnosťami špecifickými pre projekt nebudú k dispozícii v procesoch následného predaja.

Nasledujúca tabuľka obsahuje dôležité informácie o poli pre potenciálneho zákazníka a následné dôsledky týchto polí.

| **Pole** | **Miesto** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- | --- |
| Predmet | Karta Všeobecné | Toto textové pole by malo obsahovať krátky popis dohody. | Téma potenciálneho zákazníka bude predvolene nastavená ako téma príležitosti a názov cenovej ponuky a zmluva o projekte. |
| Typ | Karta Všeobecné | Toto pole množiny možností má nasledujúce možnosti:</br>- Založené na práci (k dispozícii iba vtedy, keď je nainštalovaný Project Operations)</br>- Založené na položke (k dispozícii iba vtedy, keď sú nainštalované Project Operations a Sales)</br>- Služba založená na údržbe (k dispozícii, keď je nainštalovaná služba Field Service) | Keď je hodnota tohto poľa nastavená na **Založené na práci** pre potenciálneho zákazníka, potenciálny zákazník je kvalifikovaný na vytvorenie príležitosti na základe projektu. Na povolenie všetkých rozšírení a funkcií na základe projektu v procese následného predaja tejto dohody je potrebná príležitosť založená na projekte. |
| Meno | Karta Všeobecné | Krstné meno kontaktu záujemcu | Keď je potenciálny zákazník kvalifikovaný, vytvorí sa účet, kontakt a príležitosť. V tejto hodnote sa nastavuje krstné meno kontaktu. |
| Priezvisko | Karta Všeobecné | Priezvisko kontaktu záujemcu | Keď je potenciálny zákazník kvalifikovaný, vytvorí sa účet, kontakt a príležitosť. V tejto hodnote sa nastavuje priezvisko kontaktu. |
| Spoločnosť | Karta Všeobecné | Názov spoločnosti potenciálneho zákazníka | Keď je potenciálny zákazník kvalifikovaný, vytvorí sa účet, kontakt a príležitosť. V tejto hodnote sa nastavuje názov vytvoreného obchodného vzťahu. |
| Mena | Karta Podrobnosti | Mena potenciálneho zákazníka | Keď je potenciálny zákazník kvalifikovaný, vytvorí sa účet, kontakt a príležitosť. V tejto hodnote sa nastavuje mena vytvoreného obchodného vzťahu. |

## <a name="qualify-a-new-project-based-lead"></a>Kvalifikovanie nového potenciálneho zákazníka na základe projektu

Potenciálni záujemcovia, ktorí majú hodnotu **Typ** nastavenú na **Založené na práci** sa nazývajú potenciálni záujemcovia na základe projektu. Keď je potenciálny zákazník na základe projektu kvalifikovaný, vytvorí sa nasledujúce:

- Obchodný vzťah, ktorý používa pole **Spoločnosť** potenciálneho zákazníka.
- Záznam kontaktu priradený k účtu na základe hodnôt v poliach **Krstné meno** a **Priezvisko** pre potenciálneho zákazníka.
- Príležitosť založená na projekte, ktorá má pole **Typ** nastavené na **Založené na práci**.

Podrobnejšie informácie o kvalifikovaných potenciálnych zákazníkoch nájdete v časti [Kvalifikovanie alebo konvertovanie potenciálnych zákazníkov](/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Tok obchodného procesu pre obchody založené na projekte

Nasledujúce toky obchodného procesu sú podporované pre obchody na základe projektu v Project Operations:

- Potenciálny zákazník pre obchodný proces príležitosti
- Proces predaja príležitosti

Potenciálny zákazník pre proces predaja príležitostí podporuje nasledujúce fázy:

| Názov etapy | Mapovaná entita | Funkcie |
| --- | --- | --- |
| Schváliť | Potenciálny zákazník | Kvalifikovanie potenciálneho zákazníka na vytvorenie obchodného vzťahu, kontaktu alebo príležitosti. |
| Vyvinúť | Príležitosť | Vytvorenie príležitosti na pridanie ďalších informácií pre vykonanú prácu, kľúčových účastníkov projektu a konkurenciu. |
| Navrhnúť | Príležitosť | Vytvorenie návrhu a získanie súhlasu od interného hodnotiaceho tímu. |
| Zatvoriť | Príležitosť | Získanie príležitosti na uzavretie obchodu. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]