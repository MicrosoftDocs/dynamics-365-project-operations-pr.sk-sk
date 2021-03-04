---
title: Odhadovanie riadka cenovej ponuky založenej na projekte
description: Táto téma poskytuje informácie o tom, ako vytvoriť odhad riadka cenovej ponuky založenej na projekte.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 56892a134c0c739958f7f939214930631dea7420
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180391"
---
# <a name="estimating-a-project-based-quote-line"></a>Odhadovanie riadka cenovej ponuky založenej na projekte

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Riadok cenovej ponuky založenej na projekte obsahuje podrobnosti, ktoré pomáhajú pri odhadovaní nákladov a potenciálnych výnosov z práce potrebnej na dodanie riadka cenovej ponuky.

Ak chcete odhadnúť riadok cenovej ponuky založenej na projekte, v riadku cenovej ponuky založenej na projekte vyberte kartu **Podrobnosti o riadku cenovej ponuky**. Existujú dva spôsoby, ako vytvoriť odhad riadka cenovej ponuky založenej na projekte:

- Ručne vytvorte odhad priamo na riadku cenovej ponuky pomocou podrobností o riadku cenovej ponuky 
- Vytvorte projekt a plán projektu a potom projekt a úlohy v projekte priraďte k riadku cenovej ponuky. Bude povolený proces importu odhadov plánu projektu do riadku cenovej ponuky na základe vami poskytnutých informácií.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Vytvorenie priamych odhadov riadka cenovej ponuky založenej na projekte

Ak chcete vytvoriť odhad riadka cenovej ponuky založenej na projekte, vyberte kartu **Podrobnosti o riadku cenovej ponuky**. Riadková položka, ktorú vytvoríte na tejto karte, zhrnie hodnotu cenovej ponuky pre tento riadok cenovej ponuky. 

Ak chcete vytvoriť podrobnosti riadka cenovej ponuky, zvoľte **+ Nová podrobnosť riadka cenovej ponuky** na vedľajšej mriežke **Podrobnosti riadka cenovej ponuky**. Otvorí sa posúvač rýchleho vytvorenia. Nasledujúce polia vo formulári **Riadok cenovej ponuky**:

| **Pole** | **Miesto** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- | --- |
| Popis | Rýchle vytvorenie | Popis konkrétneho odhadu. | Toto pole predvolene obsahuje podrobnosti príslušného riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Trieda transakcie | Rýchle vytvorenie | Tento rozbaľovací zoznam obsahuje triedy transakcií, ktoré sú zahrnuté na karte **Všeobecné** v riadku cenovej ponuky na základe projektu.  | Toto pole predvolene obsahuje podrobnosti príslušného riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Rola | Rýchle vytvorenie | Osoba, ktorá bude vykonávať túto prácu alebo znáša tieto výdavky. | Toto pole predvolene obsahuje podrobnosti príslušného riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Kategória | Rýchle vytvorenie | Kategória práce alebo výdavku. | Toto pole predvolene obsahuje podrobnosti príslušného riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Počiatočný dátum | Rýchle vytvorenie | Dátum začatia práce. | Toto pole predvolene obsahuje podrobnosti príslušného riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Konečný dátum | Rýchle vytvorenie | Dátum ukončenia práce. | Toto pole predvolene obsahuje podrobnosti príslušného riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Zdrojová jednotka | Rýchle vytvorenie | Zdrojová jednotka, ktorej vzniknú tieto náklady a poskytne zdroj na prácu na nej. | Toto pole predvolene obsahuje podrobnosti príslušného riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. Toto pole sa používa aj pri získavaní obstarávacej ceny. |
| Plán jednotky | Rýchle vytvorenie | Jednotková skupina práce alebo výdavku. Jednotky patria do plánu jednotiek alebo do skupiny jednotiek. Napríklad Míle a KM sú jednotky, ktoré patria do skupiny jednotiek, ktoré popisujú vzdialenosť. | Toto pole predvolene obsahuje podrobnosti príslušného riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Jednotka | Rýchle vytvorenie | Jednotka práce alebo výdavku. | Toto pole predvolene obsahuje podrobnosti príslušného riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Počet | Rýchle vytvorenie | Množstvo práce alebo výdavku | Toto pole predvolene obsahuje podrobnosti príslušného riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Jednotková cena | Rýchle vytvorenie | Fakturačná sadzba za rolu, ktorá vykonáva prácu, alebo predajná cena kategórie výdavkov. Toto pole je predvolené pre Čas na základe kombinácie roly a zdrojových jednotiek v cenníku projektu, ktorý je účinný k dátumu začatia. Pre výdavky je v tomto poli predvolené nastavenie ceny pre kategóriu transakcií v cenníku projektu, ktorý je účinný od dátumu začatia. Ak metóda určovania cien pre kategóriu transakcií nie je cena za jednotku, neexistuje predvolená hodnota a toto pole zostáva nevyplnené. | Nákladová sadzba za rolu, ktorá vykonáva prácu, alebo náklady na jednotku kategórie výdavkov. Toto pole je predvolené pre Čas na základe kombinácie roly a zdrojových jednotiek pre cenu zmluvnej jednotky podľa cenníka s cenovými ponukami, ktorý je účinný k dátumu začatia. Pre výdavky je v tomto poli predvolené nastavenie ceny pre kategóriu transakcií v cenníku obstarávacích cien zmluvnej jednotky, ktorý je účinný od dátumu začatia. Ak metóda určovania cien pre kategóriu transakcií nie je cena za jednotku, neexistuje predvolená hodnota a toto pole zostáva nevyplnené. |
| Odhad dane | Rýchle vytvorenie | Odhadovanú daň pre túto prácu alebo výdavok môžete zadať manuálne. | Toto pole nemá žiadny následný dopad. |
| Množstvo | Rýchle vytvorenie | Do tohto poľa môžete manuálne vložiť informácie, ak polia **Množstvo** a **Cena** zostávajú nevyplnené. Ak tieto polia nie sú prázdne, toto pole bude iba na čítanie a počíta sa ako (Množstvo \* Jednotková cena) + Daň. | Toto pole nemá žiadny následný dopad. |

## <a name="update-prices-on-quote-line-details"></a>Aktualizácia cien v podrobnostiach o riadku cenovej ponuky

Ak ste zmenili ceny v cenníku projektu, ktorý je priložený k cenovej ponuke, alebo v cenníku obstarávacích cien zmluvnej jednotky, môžete vybrať možnosť **Prepočítať** na stránke **Cenová ponuka**, aby ste obnovili ceny v jednotlivých podrobnostiach o riadku cenovej ponuky tak, aby odrážali túto zmenu. Keď vyberiete možnosť **Prepočítať**, zobrazí sa varovanie, ktoré vás informuje, že ceny v podrobnostiach o riadku cenovej ponuky pre všetky riadky cenovej ponuky na tejto cenovej ponuke budú vynulované. Výberom možnosti **Áno** obnovíte ceny pre predaje, ako aj pre podrobnosti o riadkoch cenovej ponuky.

## <a name="access-quote-line-details-for-cost"></a>Prístup k podrobnostiam o riadku cenovej ponuky pre náklady

Na karte **Podrobnosti riadka cenovej ponuky** vyberte riadok v mriežke, aby sa povolili niektoré akcie na paneli nástrojov vedľajšej mriežky. Prvá akcia na paneli s nástrojmi vedľajšej mriežky, keď je vybratá podrobnosť riadka cenovej ponuky **Otvoriť podrobnosti nákladov**. Vyberte **Otvoriť podrobnosti o nákladoch** na zobrazenie súvisiacej nákladovej sadzby a čiastky pre tento riadok cenovej ponuky.

> [!NOTE]
> Zmena hodnoty zdrojovej jednotky, množstva, dátumov, rolí alebo kategórií v podrobnostiach o riadku cenovej ponuky pre náklady zmení príslušné hodnoty v podrobnostiach o riadku cenovej ponuky pre predaj.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Mena v podrobnostiach o riadku cenovej ponuky pre náklady a predaj

Mena v podrobnostiach o riadku cenovej ponuky pre predvolené predaje z cenníka projektu, ktorý je účinný k dátumu začiatku podrobností o riadku cenovej ponuky.

Mena v podrobnostiach o riadku cenovej ponuky pre predvolené náklady z cenníka zmluvnej jednotky cenovej ponuky, ktorý je účinný k dátumu začiatku podrobností o riadku cenovej ponuky.

Výpočty ziskovosti prevádzajú čiastku v podrobnostiach o riadku cenovej ponuky na náklady a predaj do základnej meny prostredia na vykazovanie celkovej odhadovanej marže v cenovej ponuke.

Môže to mať za následok chyby pri zaokrúhľovaní mien a zmeny marží z dôvodu chýbajúcich výmenných kurzov platných k príslušnému dátumu. Tieto výpočty v cenových ponukách projektu používajte iba ako aproximácie a nie ako skutočné zákonné alebo iné výkazy, ktoré si vyžadujú vyššiu presnosť zaokrúhľovania a uvedomenie si dátumu platnosti výmenných kurzov.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]