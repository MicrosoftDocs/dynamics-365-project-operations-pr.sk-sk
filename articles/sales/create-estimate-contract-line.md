---
title: Odhad riadka zmluvy založenej na projekte
description: Táto téma poskytuje informácie o odhadoch v riadky zmluvy založenej na projekte.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cdc8984e080d995e3a0b667fe662291b499235b2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278527"
---
# <a name="estimate-a-projectbased-contract-line"></a>Odhad riadka zmluvy založenej na projekte

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_ 

V rámci Dynamics 365 Project Operations má riadok zmluvy založenej na projekte podrobnosti, ktoré pomáhajú odhadnúť náklady a potenciálne príjmy z práce súvisiacej s dodaním riadka zmluvy.

Ak chcete odhadnúť riadok zmluvy založenej na projekte, prejdite na kartu **Podrobnosti o riadku zmluvy** na **Riadku zmluvy** založenej na projekte.  Existujú dva spôsoby, ako vytvoriť odhad na riadku zmluvy založenej na projekte:

   - Vytvorte odhad priamo na riadku zmluvy manuálnym pridaním podrobností riadka zmluvy.
   - Vytvorte projekt a plán projektu a potom projekt a úlohy priraďte k riadku zmluvy projektu. To umožňuje proces, pomocou ktorého môžete importovať odhad plánu projektu do riadka zmluvy na základe komponentov zahrnutých v riadku zmluvy.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Vytvorenie odhadu priamo v riadku zmluvy založenej na projekte

1. Prejdite na riadok zmluvy a vyberte kartu **Podrobnosti riadka zmluvy**. Riadky, ktoré vytvoríte na tejto karte, sú zhrnuté a zobrazené ako **Zmluvná hodnota** pre tento **Riadok zmluvy**. 
2. Vo vedľajšej mriežke **Podrobnosti riadku zmluvy** vyberte **+ Nová podrobnosť riadka zmluvy**. Otvorí sa posúvač na rýchle vytvorenie. Nasledujúce polia sú k dispozícii vo formulári **Podrobnosti riadka zmluvy**:

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| **Opis** | **Rýchle vytvorenie** | Popis konkrétneho odhadu. | Toto pole sa predvolene nastaví na súvisiace podrobnosti riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Trieda transakcie** | **Rýchle vytvorenie** | Táto rozbaľovacia ponuka je zoznamom tried transakcií zahrnutých na karte **Všeobecné** riadka zmluvy založenej na projekte. | Toto pole sa predvolene nastaví na súvisiace podrobnosti riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Rola** | **Rýchle vytvorenie** | Rola osoby, ktorá vykonáva túto prácu alebo znáša tieto výdavky. | Toto pole sa predvolene nastaví na súvisiace podrobnosti riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Kategória** | **Rýchle vytvorenie** | Kategória práce alebo výdavku. | Toto pole sa predvolene nastaví na súvisiace podrobnosti riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Dátum začatia** | **Rýchle vytvorenie** | Dátum začatia práce. | Toto pole sa predvolene nastaví na súvisiace podrobnosti riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Dátum ukončenia** | **Rýchle vytvorenie** | Dátum ukončenia práce. | Toto pole sa predvolene nastaví na súvisiace podrobnosti riadka zmluvy pre náklad, ktorý sa vytvorí automaticky. |
| **Spoločnosť zaisťujúca zdroje** | **Rýchle vytvorenie** | Spoločnosť zaisťujúca zdroje alebo právnická osoba, ktorá znáša tieto náklady a poskytuje zdroj na prácu na nich. | Toto pole sa predvolene nastaví na súvisiace podrobnosti riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. Toto pole sa používa aj pri získavaní obstarávacej ceny. |
| **Zdrojová jednotka** | **Rýchle vytvorenie** | Zdrojová jednotka, ktorá znáša tieto náklady a poskytuje zdroj, aby na nich pracoval. | Toto pole sa predvolene nastaví na súvisiace podrobnosti riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. Toto pole sa používa aj pri získavaní obstarávacej ceny. |
| **Plán jednotky** | **Rýchle vytvorenie** | Jednotková skupina práce alebo výdavku. Jednotky patria do plánu jednotiek alebo do skupiny jednotiek. Napríklad *míle* a *kilometre* sú jednotky, ktoré patria do skupiny jednotiek, ktoré popisujú vzdialenosť. | Toto pole sa predvolene nastaví na súvisiace podrobnosti riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Jednotka** | **Rýchle vytvorenie** | Jednotka práce alebo výdavku. | Toto pole sa predvolene nastaví na súvisiace podrobnosti riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Množstvo** | **Rýchle vytvorenie** | Množstvo práce alebo výdavku. | Toto pole sa predvolene nastaví na súvisiace podrobnosti riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Jednotková cena** | **Rýchle vytvorenie** | Fakturačná sadzba za rolu, ktorá vykonáva prácu, alebo predajná cena kategórie výdavkov. Toto pole je predvolené pre **Čas** na základe kombinácie roly a zdrojových jednotiek v cenníku projektu, ktorý je účinný k dátumu začatia. Pre výdavky sa predvolená hodnota tohto poľa získava z nastavenia ceny pre kategóriu transakcií v cenníku projektu, ktorý platí pre dátum začatia. Ak metóda určovania cien pre kategóriu transakcií nie je **cena za jednotku**, neexistuje predvolená hodnota a toto pole zostáva nevyplnené. | Nákladová sadzba za rolu, ktorá vykonáva prácu, alebo náklady na jednotku kategórie výdavkov. Toto pole nastavuje predvolenú hodnotu pre kombináciu **Času založeného na role** a jednotky zdrojov na riadku s cenou roly v cenníku obstarávacích cien pripojenom k zmluvnej jednotke platnom pre dátum začatia. Pre výdavky je predvolená hodnota tohto poľa založená na riadky kategórie ceny cenníka obstarávacích cien pripojeného k zmluvnej jednotke, ktorý platí pre dátum začatia. Ak metóda určovania cien pre kategóriu transakcií nie je cena za jednotku, neexistuje predvolená hodnota a toto pole zostáva nevyplnené. |
| **Odhad dane** | **Rýchle vytvorenie** | Odhadovaná daň za túto prácu alebo výdavok ako vstup používateľa. | Odhadovaná daň za túto prácu alebo výdavok ako vstup používateľa. |
| **Suma** | **Rýchle vytvorenie** | Túto hodnotu do tohto poľa môže pridať používateľ, ak sú polia **Množstvo** a **Cena** prázdne. Ak sú polia **Množstvo** a **Cena** vyplnené, pole **Množstvo** je iba na čítanie a počíta sa ako **(Množstvo \* Jednotková cena) + Daň**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Aktualizácia cien v podrobnostiach riadkov zmluvy

Ak zmeníte ceny v cenníku projektu, ktorý je pripojený k zmluve, alebo v cenníku obstarávacích cien zmluvnej jednotky, môžete ceny aktualizovať v podrobnostiach jednotlivých riadkov zmluvy, aby sa zmena prejavila. Na stránke **Zmluva** vyberte **Prepočítať**. Zobrazí sa varovanie, ktoré vás bude informovať, že ceny pre všetky riadky zmluvy na tejto zmluve sa resetujú. Vyberte **Áno** na obnovenie cien podrobností predajných a nákladových riadkov zmluvy.

## <a name="access-contract-line-details-for-cost"></a>Prístup k podrobnostiam riadka zmluvy pre náklady

Na karte **Podrobnosti riadka zmluvy** vyberte riadok v mriežke, aby sa zobrazili akcie na paneli nástrojov vedľajšej mriežky. Prvá akcia na paneli nástrojov vedľajšej mriežky je **Otvoriť podrobnosti o nákladoch**. Ak chcete zobraziť nákladovú sadzbu a sumu pre túto podrobnosť riadka zmluvy, vyberte **Otvoriť podrobnosti o nákladoch**. 

> [!NOTE]
> Zmena hodnôt spoločnosti zaisťujúcej zdroje, zdrojovej jednotky, množstva, dátumov, rolí alebo kategórií v podrobnostiach riadka zmluvy pre **Náklady** tiež zmení zodpovedajúce hodnoty v podrobnostiach riadka zmluvy pre **Predaj**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Mena v podrobnostiach riadku zmluvy pre náklady a predaj

Podrobnosti riadku zmluvy pre **Predaj** nastavuje predvolenú menu z cenníka projektu, ktorá je účinná pre dátum začiatku podrobnosti riadka zmluvy.

Podrobnosti riadka zmluvy pre **Náklad** nastavuje predvolenú menu z cenníka zmluvnej jednotky zmluvy, ktorá je účinná pre dátum začiatku podrobnosti riadka zmluvy pre **Náklad**.

Výpočty ziskovosti prevádzajú sumy pre podrobnosti riadka zmluvy pre **Náklad** a **Predaj** do základnej meny prostredia na vykazovanie celkových skutočných a odhadovaných marží zo zmluvy.

> [!NOTE]
> Mohli by sa vyskytnúť chyby zaokrúhľovania mien a zmenené marže z dôvodu chýbajúcich výmenných kurzov platných k dátumu. Tieto výpočty na projektových zmluvách používajte iba ako aproximácie a nie ako skutočné zákonné alebo iné správy, ktoré si pri výmenných kurzoch vyžadujú vyššiu presnosť zaokrúhľovania a zohľadnenia účinnosti podľa dátumu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]