---
title: Odhadovanie riadka cenovej ponuky založenej na projekte
description: Táto téma poskytuje informácie o tom, ako vytvoriť odhad riadka cenovej ponuky založenej na projekte.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 20a318c9f288b08a0984f9c29dced05997622f47
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003425"
---
# <a name="estimating-a-project-based-quote-line"></a>Odhadovanie riadka cenovej ponuky založenej na projekte

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Riadok cenovej ponuky založenej na projekte obsahuje podrobnosti, ktoré pomáhajú pri odhadovaní nákladov a potenciálnych výnosov z práce potrebnej na dodanie riadka cenovej ponuky.

Ak chcete odhadnúť riadok cenovej ponuky založenej na projekte, v riadku cenovej ponuky založenej na projekte vyberte kartu **Podrobnosti o riadku cenovej ponuky**. Existujú dva spôsoby, ako vytvoriť odhad riadka cenovej ponuky založenej na projekte:

- Ručne vytvorte odhad priamo na riadku cenovej ponuky pomocou podrobností o riadku cenovej ponuky. 
- Vytvorte projekt a plán projektu a potom projekt a úlohy v projekte priraďte k riadku cenovej ponuky. Bude povolený proces importu odhadov plánu projektu do riadku cenovej ponuky na základe vami poskytnutých informácií.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Vytvorenie priamych odhadov riadka cenovej ponuky založenej na projekte

Ak chcete vytvoriť odhad riadka cenovej ponuky založenej na projekte, vyberte kartu **Podrobnosti o riadku cenovej ponuky**. Riadková položka, ktorú vytvoríte na tejto karte, zhrnie hodnotu cenovej ponuky pre tento riadok cenovej ponuky. 

Ak chcete vytvoriť podrobnosti riadka cenovej ponuky, zvoľte **Nová podrobnosť riadka cenovej ponuky** na vedľajšej mriežke **Podrobnosti riadka cenovej ponuky**. Otvorí sa posúvač rýchleho vytvorenia. Nasledujúca tabuľka poskytuje podrobnosti o poliach na stránke **Podrobnosti o riadku cenovej ponuky** a ako tieto hodnoty ovplyvňujú funkčnosť.

| **Pole** | **Miesto** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- | --- |
| Popis | Rýchle vytvorenie | Popis konkrétneho odhadu. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Trieda transakcie | Rýchle vytvorenie | Tento rozbaľovací zoznam poskytuje triedy transakcií, ktoré sú zahrnuté na karte **Všeobecné** riadka projektovej cenovej ponuky.  | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Vyberte produkt | Rýchle vytvorenie | Platí, keď je trieda transakcie **Materiál**. Môžete zvoliť, aby ste určili, či tento odhadovaný riadok je pre produkt **Existujúci** (katalógový) alebo **Pridávaný**. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Produkt | Rýchle vytvorenie | ID produktu z katalógu produktov. Toto pole je povolené, iba ak vyberiete **Existujúci** v poli **Vyberte Produkt**. ID sa používa na získanie predajnej ceny z cenníka projektu v cenovej ponuke. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Pridaný produkt | Rýchle vytvorenie | Textové pole na napísanie do názvu produktu. Toto pole je povolené, iba ak vyberiete **Pridaný** v poli **Vyberte produkt**.| Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Rola | Rýchle vytvorenie | Rola osoby, ktorá bude vykonávať túto prácu alebo znášať tieto výdavky. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Kategória | Rýchle vytvorenie | Kategória práce alebo výdavku. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Počiatočný dátum | Rýchle vytvorenie | Dátum začatia práce. | Toto pole predvolene poskytuje podrobnosti riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Konečný dátum | Rýchle vytvorenie | Dátum ukončenia práce. | Toto pole predvolene poskytuje podrobnosti riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Zdrojová jednotka | Rýchle vytvorenie | Zdrojová jednotka, ktorá bude znášať tieto náklady a poskytovať zdroj na prácu na nich. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky a používajú sa pri získavaní obstarávacej ceny. |
| Plán jednotky | Rýchle vytvorenie | Jednotková skupina práce, produktu alebo výdavkov. Jednotky patria do plánu jednotiek alebo do skupiny jednotiek. Napríklad míle a kilometre sú jednotky, ktoré patria do skupiny jednotiek, ktorá popisuje vzdialenosť. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Jednotka | Rýchle vytvorenie | Jednotka práce, produktu alebo výdavkov. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Počet | Rýchle vytvorenie | Množstvo práce, produktu alebo výdavkov. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Jednotková cena | Rýchle vytvorenie |Fakturačná sadzba za rolu, ktorá vykonáva prácu, jednotková cena produktu alebo predajná cena produktu alebo kategória výdavkov. Predvolená hodnota pre toto pole je **Čas** na základe kombinácii hodnôt cenových dimenzií v riadku s cenou roly projektového cenníka, ktorý je účinný od dátumu začatia. Pre **Výdavky** je predvolené hodnota je nastavenia ceny pre kategóriu transakcie v cenníku projektu, ktorý je účinný od dátumu začatia. Ak metóda určovania cien pre kategóriu transakcií nie je cena za jednotku, neexistuje predvolená hodnota a toto pole zostáva prázdne. Pre produkty je predvolená hodnota založená na riadku **Položka cenníka** v cenníku projektu, ktorý je účinný od dátumu začatia.| Nákladová sadzba za rolu, ktorá vykonáva prácu, jednotková cena kategórie výdavkov alebo jednotkové náklady na produkt. Predvolená hodnota pre toto pole je **Čas** na základe kombinácii hodnôt cenových dimenzií v riadku s cenou roly projektového cenníka, ktorý je účinný od dátumu začatia. Pre **Výdavky** je predvolené hodnota je nastavenia ceny pre kategóriu transakcie v cenníku projektu, ktorý je účinný od dátumu začatia. Ak metóda určovania cien pre kategóriu transakcií nie je cena za jednotku, neexistuje predvolená hodnota a toto pole zostáva prázdne. Pre produkty je predvolená hodnota založená na riadku **Položka cenníka** v cenníku projektu, ktorý je účinný od dátumu začatia.|
| Odhad dane | Rýchle vytvorenie | Odhadovanú daň pre túto prácu alebo výdavok môžete zadať manuálne. | Toto pole nemá žiadny následný dopad. |
| Množstvo | Rýchle vytvorenie | Do tohto poľa môžete manuálne vložiť informácie, ak polia **Množstvo** a **Cena** zostávajú nevyplnené. Ak tieto polia nie sú prázdne, toto pole bude iba na čítanie a počíta sa ako (Množstvo \* Jednotková cena) + Daň. | Toto pole nemá žiadny následný dopad. |


## <a name="update-prices-on-quote-line-details"></a>Aktualizácia cien v podrobnostiach o riadku cenovej ponuky

Ak ste zmenili ceny v cenníku projektu, ktorý je priložený k cenovej ponuke, alebo v cenníku obstarávacích cien zmluvnej jednotky, môžete zvoliť **Prepočítať** na stránke **Cenová ponuka**, aby ste obnovili ceny v detailoch jednotlivých riadkov cenovej ponuky tak, aby odrážali túto zmenu. Keď vyberiete **Prepočítať**, zobrazí sa varovanie, ktoré vás informuje, že ceny v podrobnostiach riadka cenovej ponuky pre všetky riadky cenovej ponuky v tejto ponuke sa vynulujú. Výberom možnosti **Áno** obnovíte ceny pre predaje, ako aj pre podrobnosti o riadkoch cenovej ponuky.

## <a name="access-quote-line-details-for-cost"></a>Prístup k podrobnostiam o riadku cenovej ponuky pre náklady

Na karte **Podrobnosti riadka cenovej ponuky** vyberte riadok v mriežke, aby sa povolili niektoré akcie na paneli nástrojov vedľajšej mriežky. Prvá akcia na paneli s nástrojmi vedľajšej mriežky, keď je vybratá podrobnosť riadka cenovej ponuky **Otvoriť podrobnosti nákladov**. Vyberte **Otvoriť podrobnosti o nákladoch** na zobrazenie súvisiacej nákladovej sadzby a čiastky pre tento riadok cenovej ponuky.

> [!NOTE]
> Zmena hodnoty zdrojovej jednotky, množstva, dátumov, rolí alebo kategórií v podrobnostiach o riadku cenovej ponuky pre náklady zmení príslušné hodnoty v podrobnostiach o riadku cenovej ponuky pre predaj.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Mena v podrobnostiach o riadku cenovej ponuky pre náklady a predaj

Mena v podrobnostiach o riadku cenovej ponuky pre predvolené predaje z cenníka projektu, ktorý je účinný k dátumu začiatku podrobností o riadku cenovej ponuky.

Mena v podrobnostiach o riadku cenovej ponuky pre predvolené náklady z cenníka zmluvnej jednotky cenovej ponuky, ktorý je účinný k dátumu začiatku podrobností o riadku cenovej ponuky.

Výpočty ziskovosti prevádzajú čiastku v podrobnostiach o riadku cenovej ponuky na náklady a predaj do základnej meny prostredia na vykazovanie celkovej odhadovanej marže v cenovej ponuke.

> [!POZNÁMKA
> > Mohli by sa vyskytnúť chyby zaokrúhľovania mien a zmenené marže z dôvodu chýbajúcich výmenných kurzov platných k dátumu. Tieto výpočty používajte iba na projektové zmluvy, pretože ide o aproximácie a nejde o skutočné zákonné ani iné zostavy, ktoré si pri výmenných kurzoch vyžadujú vyššiu presnosť zaokrúhľovania a zohľadnenie účinnosti dátumu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
