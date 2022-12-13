---
title: Odhad riadka zmluvy založenej na projekte
description: Tento článok poskytuje informácie o odhadoch riadka projektovej zmluvy.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 633ad3130a28d75ad10b81e03a883e0a732b1ba8
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825230"
---
# <a name="estimate-a-project-based-contract-line"></a>Odhad riadka zmluvy založenej na projekte

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_ 

V rámci Dynamics 365 Project Operations má riadok zmluvy založenej na projekte podrobnosti, ktoré pomáhajú odhadnúť náklady a potenciálne príjmy z práce súvisiacej s dodaním riadka zmluvy.

Ak chcete odhadnúť riadok zmluvy založenej na projekte, prejdite na kartu **Podrobnosti o riadku zmluvy** na **Riadku zmluvy** založenej na projekte.  Existujú dva spôsoby, ako vytvoriť odhad na riadku zmluvy založenej na projekte:

   - Vytvorte odhad priamo na riadku zmluvy manuálnym pridaním podrobností riadka zmluvy.
   - Vytvorte projekt a plán projektu a potom projekt a úlohy priraďte k riadku zmluvy projektu. To umožňuje proces, pomocou ktorého môžete importovať odhad plánu projektu do riadka zmluvy na základe komponentov zahrnutých v riadku zmluvy.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Priame vytvorenie odhadu na riadku projektovej zmluvy

Ak chcete vytvoriť odhad priamo na riadku projektovej zmluvy, postupujte takto:

1. Prejdite na riadok zmluvy a vyberte kartu **Podrobnosti riadka zmluvy**. Riadky, ktoré vytvoríte na tejto karte, sú zhrnuté a zobrazené ako **Zmluvná hodnota** pre tento **Riadok zmluvy**. 
2. Vo vedľajšej mriežke **Podrobnosti o riadku zmluvy** vyberte **Nová podrobnosť riadka zmluvy**. Otvorí sa posúvač na rýchle vytvorenie. Nasledujúce polia sú k dispozícii na stránke **Podrobnosti o riadku zmluvy**.

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| **Opis** | **Rýchle vytvorenie** | Popis konkrétneho odhadu. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Trieda transakcie** | **Rýchle vytvorenie** | Tento zoznam tried transakcií je uvedený na karte **Všeobecné** riadka projektovej zmluvy. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Vyberte produkt** | **Rýchle vytvorenie** | Platí, keď je trieda transakcie **Materiál**. Môžete zvoliť, aby ste určili, či tento odhadovaný riadok je pre produkt **Existujúci** (katalógový) alebo **Pridávaný**. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Produkt** | **Rýchle vytvorenie** | ID produktu z katalógu produktov. Toto pole je povolené, iba ak vyberiete **Existujúci produkt** v poli **Vyberte produkt**. ID sa používa na získanie predajnej ceny z cenníka projektu v zmluve. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Pridaný produkt** | **Rýchle vytvorenie** | Textové pole na zadanie názvu produktu. Toto pole je povolené, iba ak vyberiete **Pridaný** v poli **Vyberte produkt**.| Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Rola** | **Rýchle vytvorenie** | Rola osoby, ktorá vykonáva túto prácu alebo znáša tieto výdavky. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky.|
| **Kategória** | **Rýchle vytvorenie** | Kategória práce alebo výdavku. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky.|
| **Počiatočný dátum** | **Rýchle vytvorenie** | Dátum začatia práce. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Dátum ukončenia** | **Rýchle vytvorenie** | Dátum ukončenia práce. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Spoločnosť zaisťujúca zdroje** | **Rýchle vytvorenie** | Spoločnosť zaisťujúca zdroje právna entita, ktorá znáša tieto náklady a poskytuje zdroj na prácu na nich. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky a používajú sa pri získavaní obstarávacej ceny. |
| **Zdrojová jednotka** | **Rýchle vytvorenie** | Zdrojová jednotka, ktorá znáša tieto náklady a poskytuje zdroj na prácu na nich. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky a používajú sa pri získavaní obstarávacej ceny. |
| **Plán jednotky** | **Rýchle vytvorenie** | Jednotková skupina práce, produktu alebo výdavkov. Jednotky patria do plánu jednotiek alebo do skupiny jednotiek. Napríklad *míle* a *kilometre (km)* sú jednotky, ktoré patria do skupiny jednotiek, ktoré popisujú vzdialenosť. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Jednotka** | **Rýchle vytvorenie** | Jednotka práce, produktu alebo výdavkov. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Počet** | **Rýchle vytvorenie** | Množstvo práce, produktu alebo výdavkov. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka zmluvy pre náklady, ktoré sa vytvárajú automaticky. |
| **Jednotková cena** | **Rýchle vytvorenie** | Fakturačná sadzba za rolu, ktorá vykonáva prácu, jednotková cena produktu alebo predajná cena produktu alebo kategória výdavkov. Predvolená hodnota pre **Čas** je založená na kombinácii hodnôt cenových dimenzií v riadku s cenou roly projektového cenníka, ktorý je účinný od dátumu začatia. Pre **Výdavky** je predvolené hodnota pre toto pole z nastavenia ceny pre kategóriu transakcie v cenníku projektu, ktorý je účinný od dátumu začatia. Ak metóda určovania cien pre kategóriu transakcií nie je **cena za jednotku**, neexistuje predvolená hodnota a toto pole zostáva nevyplnené. Pre produkty je predvolená hodnota tohto poľa založená na riadku **Položka cenníka** v cenníku projektu, ktorý je účinný od dátumu začatia.| Nákladová sadzba za rolu, ktorá vykonáva prácu alebo jednotková cena kategórie výdavkov alebo jednotkové náklady na produkt. Predvolená hodnota pre **Čas** je založená na kombinácii hodnôt cenových dimenzií v riadku s cenou roly cenníka obstarávacích cien pripojeného k zmluvnej jednotke, ktorý je účinný od dátumu začatia. V prípade **výdavkov** je predvolená hodnota pre toto pole založená riadku cenníka kategórie cenníka obstarávacích cien pripojeného k zmluvnej jednotke, ktorý je účinný od dátumu začatia. Ak metóda určovania cien pre kategóriu transakcií nie je cena za jednotku, neexistuje predvolená hodnota a toto pole zostáva nevyplnené. V prípade produktov je predvolená hodnota tohto poľa založená riadku **Položka v cenníku** cenníka obstarávacích cien pripojeného k zmluvnej jednotke, ktorý je účinný od dátumu začatia.|
| **Odhad dane** | **Rýchle vytvorenie** | Odhadovaná daň za túto prácu alebo výdavok ako vstup používateľa. | &nbsp; |
| **Množstvo** | **Rýchle vytvorenie** | Hodnotu v tomto poli je možné pridať, ak polia **Množstvo** a **Cena** zostávajú nevyplnené. Ak sú polia **Množstvo** a **Cena** vyplnené, pole **Množstvo** je iba na čítanie a počíta sa ako **(Množstvo \* Jednotková cena) + Daň**. | &nbsp; |

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
