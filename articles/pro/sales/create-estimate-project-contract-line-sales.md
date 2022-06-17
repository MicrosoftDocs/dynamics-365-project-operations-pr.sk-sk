---
title: Odhad riadka zmluvy založenej na projekte – čiastočné
description: Tento článok poskytuje informácie o odhade zmluvnej línie založenej na projekte.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8b4379cc5822d08b55623f0f3d4d49791af90927
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914421"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Odhad riadka zmluvy založenej na projekte – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

V rámci Dynamics 365 Project Operations má riadok zmluvy založenej na projekte podrobnosti, ktoré pomáhajú odhadnúť náklady a potenciálne príjmy z práce súvisiacej s dodaním riadka zmluvy.

Ak chcete odhadnúť riadok zmluvy založenej na projekte, prejdite na kartu **Podrobnosti o riadku zmluvy** na **Riadku zmluvy** založenej na projekte.  Existujú dva spôsoby, ako vytvoriť odhad na riadku zmluvy založenej na projekte:

   - Vytvorte odhad priamo na riadku zmluvy manuálnym pridaním podrobností riadka zmluvy.
   - Vytvorte projekt a plán projektu a potom projekt a úlohy priraďte k riadku zmluvy projektu. To umožňuje proces, pomocou ktorého môžete importovať odhad plánu projektu do riadka zmluvy na základe komponentov zahrnutých v riadku zmluvy.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Vytvorenie odhadu priamo v riadku zmluvy založenej na projekte

Ak chcete vytvoriť odhad priamo na riadku projektovej zmluvy, postupujte takto:

1. Prejdite na riadok zmluvy a vyberte kartu **Podrobnosti riadka zmluvy**. Riadky, ktoré vytvoríte na tejto karte, sú zhrnuté a zobrazené ako **Zmluvná hodnota** pre tento **Riadok zmluvy**. 
2. Vo vedľajšej mriežke **Podrobnosti o riadku zmluvy** vyberte **Nová podrobnosť riadka zmluvy**. Otvorí sa posúvač na rýchle vytvorenie. Nasledujúce polia sú k dispozícii na stránke **Podrobnosti o riadku zmluvy**.

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| **Opis** | **Rýchle vytvorenie** | Popis konkrétneho odhadu. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Trieda transakcie** | **Rýchle vytvorenie** | Tento zoznam tried transakcií je uvedený na karte **Všeobecné** riadka projektovej zmluvy. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Vyberte produkt** | **Rýchle vytvorenie** | Platí, keď je trieda transakcie **Materiál**. Môžete určiť, či tento odhadovaný riadok je pre produkt **Existujúci** (katalógový) alebo **Pridávaný**. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Produkt** | **Rýchle vytvorenie** | ID produktu z katalógu produktov. Toto pole je povolené, iba ak vyberiete **Existujúci produkt** v poli **Vyberte produkt**. ID sa používa na získanie predajnej ceny z cenníka projektu v zmluve. | Táto hodnota predvolene poskytuje podrobnosti riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Pridaný produkt** | **Rýchle vytvorenie** | Textové pole na zadanie názvu produktu. Toto pole je povolené, iba ak vyberiete **Pridaný** v poli **Vyberte produkt**.| Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Rola** | **Rýchle vytvorenie** | Rola osoby, ktorá vykonáva túto prácu alebo znáša tieto výdavky. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky.|
| **Kategória** | **Rýchle vytvorenie** | Kategória práce alebo výdavku. |Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky.|
| **Počiatočný dátum** | **Rýchle vytvorenie** | Dátum začatia práce. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Dátum ukončenia** | **Rýchle vytvorenie** | Dátum ukončenia práce. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Zdrojová jednotka** | **Rýchle vytvorenie** | Zdrojová jednotka, ktorá znáša tieto náklady a poskytuje zdroj na prácu na nich. |Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky a používajú sa pri získavaní obstarávacej ceny. |
| **Plán jednotky** | **Rýchle vytvorenie** | Jednotková skupina práce, produktu alebo výdavkov. Jednotky patria do plánu jednotiek alebo do skupiny jednotiek. Napríklad *míle* a *kilometre (km)* sú jednotky, ktoré patria do skupiny jednotiek, ktoré popisujú vzdialenosť. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Jednotka** | **Rýchle vytvorenie** | Jednotka práce, produktu alebo výdavkov. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Počet** | **Rýchle vytvorenie** | Množstvo práce, produktu alebo výdavkov. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Jednotková cena** | **Rýchle vytvorenie** | Fakturačná sadzba za rolu, ktorá vykonáva prácu, jednotková cena produktu alebo predajná cena produktu alebo kategória výdavkov. Toto pole získava predvolené hodnoty pre **Čas** na základe kombinácie hodnôt cenových dimenzií v riadku s cenou roly projektového cenníka, ktorý je účinný od dátumu začatia. Pre **Výdavky** sa predvolená hodnota tohto poľa získava z nastavenia ceny pre kategóriu transakcií v cenníku projektu, ktorý platí pre dátum začatia. Ak metóda určovania cien pre kategóriu transakcií nie je **cena za jednotku**, neexistuje predvolená hodnota a toto pole zostáva nevyplnené. Pre produkty je predvolená hodnota tohto poľa založená na riadku **Položka cenníka** v cenníku projektu, ktorý je účinný od dátumu začatia.| Nákladová sadzba za rolu, ktorá vykonáva prácu alebo jednotková cena kategórie výdavkov alebo jednotkové náklady na produkt. Toto pole získava predvolené hodnoty pre **Čas** na základe na kombinácii hodnôt cenových dimenzií v riadku s cenou roly cenníka obstarávacích cien pripojeného k zmluvnej jednotke, ktorý je účinný od dátumu začatia. Pre výdavky je predvolená hodnota tohto poľa založená na riadky kategórie ceny cenníka obstarávacích cien pripojeného k zmluvnej jednotke, ktorý platí pre dátum začatia. Ak metóda určovania cien pre kategóriu transakcií nie je cena za jednotku, neexistuje predvolená hodnota a toto pole zostáva nevyplnené. V prípade produktov je predvolená hodnota tohto poľa založená riadku **Položka v cenníku** cenníka obstarávacích cien pripojeného k zmluvnej jednotke, ktorý je účinný od dátumu začatia.|
| **Odhad dane** | **Rýchle vytvorenie** | Odhadovaná daň za túto prácu alebo výdavok. | Odhadovaná daň za túto prácu alebo výdavok. |
| **Množstvo** | **Rýchle vytvorenie** | Hodnotu v tomto poli môžete pridať, ak polia **Množstvo** a **Cena** zostávajú nevyplnené. Ak sú polia **Množstvo** a **Cena** vyplnené, pole **Množstvo** je iba na čítanie a počíta sa ako **(Množstvo \* Jednotková cena) + Daň**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Aktualizácia cien v podrobnostiach riadkov zmluvy

Ak zmeníte ceny v cenníku projektu, ktorý je pripojený k zmluve, alebo v cenníku obstarávacích cien zmluvnej jednotky, môžete ceny aktualizovať v podrobnostiach jednotlivých riadkov zmluvy, aby sa zmena prejavila. Na stránke **Zmluva** vyberte **Prepočítať**. Zobrazí sa varovanie, ktoré vás informuje, že ceny pre všetky riadky zmluvy v tejto zmluve sa resetujú. Vyberte **Áno** na obnovenie cien podrobností predajných a nákladových riadkov zmluvy.

## <a name="access-contract-line-details-for-cost"></a>Prístup k podrobnostiam riadka zmluvy pre náklady

Na karte **Podrobnosti riadka zmluvy** vyberte riadok v mriežke, aby sa zobrazili akcie na paneli nástrojov vedľajšej mriežky. Prvá akcia na paneli nástrojov vedľajšej mriežky je **Otvoriť podrobnosti o nákladoch**. Ak chcete zobraziť nákladovú sadzbu a sumu pre túto podrobnosť riadka zmluvy, vyberte **Otvoriť podrobnosti o nákladoch**. 

> [!NOTE]
> Zmena hodnôt spoločnosti zaisťujúcej zdroje, zdrojovej jednotky, množstva, dátumov, rolí alebo kategórií v podrobnostiach riadka zmluvy pre **Náklady** tiež zmení zodpovedajúce hodnoty v podrobnostiach riadka zmluvy pre **Predaj**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Mena v podrobnostiach riadku zmluvy pre náklady a predaj

Podrobnosti riadku zmluvy pre **Predaj** nastavuje predvolenú menu z cenníka projektu, ktorá je účinná pre dátum začiatku podrobnosti riadka zmluvy.

Podrobnosti riadka zmluvy pre **Náklad** nastavuje predvolenú menu z cenníka zmluvnej jednotky zmluvy, ktorá je účinná pre dátum začiatku podrobnosti riadka zmluvy pre **Náklad**.

Výpočty ziskovosti prevádzajú sumy pre podrobnosti riadka zmluvy pre **Náklad** a **Predaj** do základnej meny prostredia na vykazovanie celkových skutočných a odhadovaných marží zo zmluvy.

> [!NOTE]
> Mohli by sa vyskytnúť chyby zaokrúhľovania mien a zmenené marže z dôvodu chýbajúcich výmenných kurzov platných k dátumu. Tieto výpočty používajte iba na projektové zmluvy, pretože ide o aproximácie a nejde o skutočné zákonné ani iné zostavy, ktoré si pri výmenných kurzoch vyžadujú vyššiu presnosť zaokrúhľovania a zohľadnenie účinnosti dátumu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
