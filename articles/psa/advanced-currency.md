---
title: Viacmenové scenáre (verzia 3.x)
description: Táto téma poskytuje informácie o viacmenových scenároch.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7be029eeca3129d30f4bec1bf9b180a0a5122a86
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084474"
---
# <a name="multiple-currency-scenarios"></a>Viacmenové scenáre

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 má dva koncepty mien:

- **Mena transakcie** Mena v ktorej sa transakcia vyskytuje. 
- **Základná mena** - mena inštancie Dynamics 365. Táto mena je nastavená, keď je poskytnutá inštancia Dynamics 365. Nemôže byť zmenená.

Napríklad, Blaho USA predal 100 tričiek zákazníkovi vo Veľkej Británii za 15 ounds sterling (GBP) každé. Nasledujúca tabuľka zobrazuje spôsob, ako sa transakcia zaznamená v entite Objednávky Produktu.

| Produkt | Množstvo | Cena za jednotku | Mena | Čiastka | Výmenný kurz | Cena za jednotku (Základná)| Množstvo (Základné)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Tričko | 100      | 15             | GBP      | 1500   | 0.94          | 17.25$               | 1725$       |

Stĺpec **Mena** zobrazuje menu transakcie, ktorá je menou, v ktorej sa predaj vyskytol. Stĺpec **Výmenný kurz** je výmenný kurz medzi menou transakcie a základnou menou. Základná mena je americký dolár (USD). Táto základná mena bola nastavená, keď bola poskytnutá inštancia Dynamics 365.
Ako ukazuje tabuľka, každá transakcia je zaznamenaná v mene transakcie a v základnej mene. Dynamics 365 používa výmenný kurz na výpočet čiastky základnej meny.

## <a name="project-service-automation-extensions"></a>Rozšírenie Project Service Automation

Dynamics 365 Project Service Automation ovplyvňuje menu transakcie, pretože obchodné transakcie majú zvyčajne dva aspekty: náklad a predaj.

Nasledujúce entity sa považujú za obchodné transakcie:

- Podrobnosti o riadku cenovej ponuky
- Podrobnosti o riadku projektovej zmluvy
- Riadok odhadu
- Záznam v účtovnom denníku
- Podrobnosti o riadku faktúry
- Skutočná hodnota

V každej z týchto entít je záznam, ktorý predstavuje čiastku nákladov alebo čiastku predaja. Pokiaľ ide o ľubovoľnú entitu Dynamics 365, ktorá má pole **Čiastka** , každý záznam obsahuje čiastky v mene transakcií a v základnej mene. 

PSA rozširuje koncept transakcie meny pre náklady a predaje nasledujúcimi spôsobmi:

- Náklad transakcie meny pre časové transakcie vždy pochádza z meny organizačnej jednotky, ktorá vlastní alebo spravuje projekt. Táto organizačná jednotka je známa ako zmluvná jednotka.
- Predajná mena transakcie pre transakcie času a výdavkov vždy pochádza z meny projektu zmluvy.
- Náklad transakcie meny pre výdavky pochádza z meny, ktorá vytvorila záznam výdavok.

## <a name="multiple-currency-scenario"></a>Viacmenový scenár

Táto časť opisuje príklad projektu, v ktorom Blaho UK dodáva zákazníkovi, ktorý sa volá Fabrikam, Japonsko. Tu je, ako bol nastavený scenár:

1. GBP a Japonský jen (JPY) sú nastavené v časti **Nastavenia** \> **Riadenie Podnikania** \> **Meny**. 
2. Konto zákazníka s názvom **Fabrikam-Japan** je nastavené a JPY je vybraný ako mena na účte.
3. Je nastavená organizačná jednotka s názvom **Blaho UK** a v mene sa vyberie GBP.
4. Vytvorí sa zmluva o projekte, kde je **Blaho UK** špecifikované ako zmluvná jednotka a **Fabrikam – Japonsko** je špecifikované ako zákazník.
5. Riadky projektových zmlúv sú vytvorené na základe fakturačných dojednaní pre rôzne triedy transakcií na projekte, ako je napríklad fakturácia za čas verzus fakturácia za výdavky.
6. Projekt sa vytvorí tam, kde je **Blaho UK** špecifikovaný ako zmluvná jednotka. Tento projekt je vytvorený a priradený k riadkom projektových zmlúv.


Počas odhadu, ktorý používa detail riadka cenovej ponuky, podrobnosti riadka zmluvy alebo riadok odhadu plánu, sa v entite vždy vytvoria dva záznamy. Jeden riadok je pre náklad, a druhý riadok je pre predaj.

- V predvolenom nastavení je mena transakcie v zázname nákladov nastavená na menu zmluvnej jednotky projektu. V tomto prípade je menou GBP.
- V predvolenom nastavení je mena transakcie v zázname predaja nastavená na menu projektovej zmluvy. V tomto prípade je menou JPY.

Ak sú skutočné údaje vytvorené pre čas pomocou časového záznamu alebo záznamu v účtovnom denníku, vyskytne sa nasledovné správanie:

- V predvolenom nastavení je mena transakcie v zázname nákladov nastavená na menu zmluvnej jednotky projektu.
- V predvolenom nastavení je mena transakcie v zázname predaja nastavená na menu projektovej zmluvy.

Ak sú skutočné údaje vytvorené pre výdavky pomocou záznamu výdavkov alebo záznamu v účtovnom denníku, vyskytne sa nasledovné správanie:

- Čiastku výdavkov môžete zaznamenať v ľubovoľnej mene. Vyberte menu pomocou výberu meny na stránke **Expense Entry** alebo na stránke **Journal Line**. V predvolenom nastavení je mena transakcie pre záznam nákladov nastavená na menu výdavkového záznamu. 
- V predvolenom nastavení je mena transakcie pre záznam predaja nastavená na menu projektovej zmluvy. Ak chcete nastaviť túto menu, systém najprv prevedie čiastku transakcie v mene, ktorú používateľ zadal do základnej meny. Potom prevedie čiastku na menu projektovej zmluvy. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Vypočítava sa súhrn, keď sú projektové skutočné údaje zaznamenané vo viacerých menách transakcie

Dynamics 365 automaticky spracováva súhrn čiastok v rôznych menách. Tu je príklad.

| Trieda transakcie | Typ transakcie| Date   | Zdroj | Kategória transakcie | Množstvo | Jednotková cena | Čiastka      | Výmenný kurz | (Základná) Suma |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Nefakturovaný predaj   | 14. Jún | Erik  |                      | 8 hod    | 20,000 JPY    | 160,000 JPY | 123           | 1,300.81 USD    |
| Time              | Nefakturovaný predaj   | 15. Jún | Erik  |                      | 8 hod    | 20,000 JPY    | 160,000 JPY | 123           | 1,300.81 USD    |
| Výdavok           | Nefakturovaný predaj   | 16. Jún | Erik  | Hotel                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265.95 USD     |
| Výdavok           | Nefakturovaný predaj   | 17. Jún | Erik  | Požičovňa áut           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159.57 USD     |

Na výpočet celkovej hodnoty nefakturovaného predaja v projekte, môžete vytvoriť súhrnné pole pre **Amount** pole na všetky súvisiace skutočné hodnoty nefakturovaný predajov. skutočné hodnoty. Pole súhrnu je konštrukcia pre Dynamics 365, ktorý umožňuje rýchle vzorce na súvisiace záznamy.
