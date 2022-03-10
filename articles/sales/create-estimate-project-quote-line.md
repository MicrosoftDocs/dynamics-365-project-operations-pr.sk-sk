---
title: Odhad riadka projektovej cenovej ponuky
description: Táto téma poskytuje informácie o tom, ako vytvoriť odhad riadka projektovej cenovej ponuky.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 84283ac055aea802fadbd6814ea65a6d3dc01d29e1e3c6290ef11f72f6a75692
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003970"
---
# <a name="estimate-a-project-quote-line"></a>Odhad riadka projektovej cenovej ponuky

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Riadok cenovej ponuky založenej na projekte obsahuje podrobnosti, ktoré pomáhajú pri odhadovaní nákladov a potenciálnych výnosov z práce potrebnej na dodanie riadka cenovej ponuky.

Ak chcete odhadnúť riadok projektovej cenovej ponuky, na riadku cenovej ponuky vyberte kartu **Podrobnosti o riadku cenovej ponuky**. Existujú dva spôsoby, ako vytvoriť odhad riadka projektovej cenovej ponuky:

   - Ručne vytvorte odhad priamo na riadku cenovej ponuky pomocou podrobností o riadku cenovej ponuky. 
   - Vytvorte projekt a plán projektu a potom projekt a úlohy v projekte priraďte k riadku cenovej ponuky. Bude povolený proces importu odhadov plánu projektu do riadku cenovej ponuky na základe vami poskytnutých informácií.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Vytvorenie priamych odhadov riadka cenovej ponuky založenej na projekte

Ak chcete vytvoriť odhady priamo na riadku projektovej cenovej ponuky, postupujte takto:

1. Ak chcete vytvoriť odhad riadka cenovej ponuky založenej na projekte, vyberte kartu **Podrobnosti o riadku cenovej ponuky**. Riadková položka, ktorú vytvoríte na tejto karte, zhrnie hodnotu cenovej ponuky pre tento riadok cenovej ponuky. 
2. Ak chcete vytvoriť podrobnosti riadka cenovej ponuky, zvoľte **Nová podrobnosť riadka cenovej ponuky** na vedľajšej mriežke **Podrobnosti riadka cenovej ponuky**. Otvorí sa posúvač rýchleho vytvorenia. Nasledujúce polia na stránke **Riadok cenovej ponuky**.

| **Pole** | **Miesto** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- | --- |
| Popis | Rýchle vytvorenie | Popis konkrétneho odhadu. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Trieda transakcie | Rýchle vytvorenie | Tento rozbaľovací zoznam obsahuje triedy transakcií, ktoré sú zahrnuté na karte **Všeobecné** v riadku cenovej ponuky na základe projektu.  | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Vyberte produkt | Rýchle vytvorenie | Platí, keď je trieda transakcie **Materiál**. Môžete zvoliť, aby ste určili, či tento odhadovaný riadok je pre produkt **Existujúci** (katalógový) alebo **Pridávaný**. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Produkt | Rýchle vytvorenie | ID produktu z katalógu produktov. Toto pole je povolené, iba ak vyberiete **Existujúci** v poli **Vyberte Produkt**. ID sa používa na získanie predajnej ceny z cenníka projektu v cenovej ponuke. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Pridaný produkt | Rýchle vytvorenie | Textové pole na napísanie do názvu produktu. Toto pole je povolené, iba ak vyberiete **Pridaný** v poli **Vyberte produkt**.| Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Rola | Rýchle vytvorenie | Rola osoby, ktorá bude vykonávať túto prácu alebo znášať tieto výdavky. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Kategória | Rýchle vytvorenie | Kategória práce alebo výdavku. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Počiatočný dátum | Rýchle vytvorenie | Dátum začatia práce. | Toto pole predvolene poskytuje podrobnosti riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Konečný dátum | Rýchle vytvorenie | Dátum ukončenia práce. | Toto pole predvolene poskytuje podrobnosti riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Spoločnosť zaisťujúca zdroje | Rýchle vytvorenie | Spoločnosť zaisťujúca zdroje právna entita, ktorá znáša tieto náklady a poskytuje zdroj na prácu na nich. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky a používajú sa pri získavaní obstarávacej ceny. |
| Zdrojová jednotka | Rýchle vytvorenie | Zdrojová jednotka, ktorá znáša tieto náklady a poskytuje zdroj na prácu na nich. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky a používajú sa pri získavaní obstarávacej ceny. |
| Plán jednotky | Rýchle vytvorenie | Jednotková skupina práce, produktu alebo výdavkov. Jednotky patria do plánu jednotiek alebo do skupiny jednotiek. Napríklad míle a kilometre sú jednotky, ktoré patria do skupiny jednotiek, ktorá popisuje vzdialenosť. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Jednotka | Rýchle vytvorenie | Jednotka práce, produktu alebo výdavkov. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Počet | Rýchle vytvorenie | Množstvo práce, produktu alebo výdavkov. | Táto hodnota predvolene poskytuje podrobnosti súvisiaceho riadka cenovej ponuky pre náklady, ktoré sa vytvárajú automaticky. |
| Jednotková cena | Rýchle vytvorenie |Fakturačná sadzba za rolu, ktorá vykonáva prácu, jednotková cena produktu alebo predajná cena produktu alebo kategória výdavkov. Predvolená hodnota pre **Čas** je založená na kombinácii hodnôt cenových dimenzií v riadku s cenou roly projektového cenníka, ktorý je účinný od dátumu začatia. Pre **Výdavky** je predvolené hodnota je nastavenia ceny pre kategóriu transakcie v cenníku projektu, ktorý je účinný od dátumu začatia. Ak metóda určovania cien pre kategóriu transakcií nie je cena za jednotku, neexistuje predvolená hodnota a toto pole zostáva nevyplnené. Pre produkty je predvolená hodnota tohto poľa založená na riadku **Položka cenníka** v cenníku projektu, ktorý je účinný od dátumu začatia.| Nákladová sadzba za rolu, ktorá vykonáva prácu, jednotková cena kategórie výdavkov alebo jednotkové náklady na produkt. Predvolená hodnota pre **Čas** je založená na kombinácii hodnôt cenových dimenzií v riadku s cenou roly cenníka obstarávacích cien pripojeného k zmluvnej jednotke, ktorý je účinný od dátumu začatia. V prípade výdavkov je predvolená hodnota založená riadku cenníka kategórie cenníka obstarávacích cien pripojeného k zmluvnej jednotke, ktorý je účinný od dátumu začatia. Ak metóda určovania cien pre kategóriu transakcií nie je cena za jednotku, neexistuje predvolená hodnota a toto pole zostáva prázdne. V prípade produktov je predvolená hodnota tohto poľa založená riadku **Položka v cenníku** cenníka obstarávacích cien pripojeného k zmluvnej jednotke, ktorý je účinný od dátumu začatia.|
| Odhad dane | Rýchle vytvorenie | Odhadovanú daň pre túto prácu alebo výdavok môžete zadať manuálne. | Toto pole nemá žiadny následný dopad. |
| Množstvo | Rýchle vytvorenie | Do tohto poľa môžete manuálne vložiť informácie, ak polia **Množstvo** a **Cena** zostávajú nevyplnené. Ak tieto polia nie sú prázdne, toto pole bude iba na čítanie a počíta sa ako (Množstvo \* Jednotková cena) + Daň. | Toto pole nemá žiadny následný dopad. |

## <a name="update-prices-on-quote-line-details"></a>Aktualizácia cien v podrobnostiach o riadku cenovej ponuky

Ak ste zmenili ceny v cenníku projektu, ktorý je priložený k cenovej ponuke, alebo v cenníku obstarávacích cien zmluvnej jednotky, môžete vybrať možnosť **Prepočítať** na stránke **Cenová ponuka**, aby ste obnovili ceny v jednotlivých podrobnostiach o riadku cenovej ponuky tak, aby odrážali túto zmenu. Keď vyberiete **Prepočítať**, zobrazí sa varovanie, ktoré vás informuje, že ceny v podrobnostiach riadka cenovej ponuky pre všetky riadky cenovej ponuky v tejto ponuke sa vynulujú. Výberom možnosti **Áno** obnovíte ceny pre predaje, ako aj pre podrobnosti o riadkoch cenovej ponuky.

## <a name="access-quote-line-details-for-cost"></a>Prístup k podrobnostiam o riadku cenovej ponuky pre náklady

Ak chcete získať prístup k podrobnostiam riadka cenovej ponuky pre náklady, postupujte takto:

1. Na karte **Podrobnosti o riadku cenovej ponuky** vyberte riadok v mriežke, aby ste povolili akcie na paneli nástrojov vedľajšej mriežky. 
2. Vyberte **Otvoriť podrobnosti o nákladoch** na zobrazenie súvisiacej nákladovej sadzby a čiastky pre tento riadok cenovej ponuky.

> [!NOTE]
> Zmena hodnoty zdrojovej jednotky, množstva, dátumov, rolí alebo kategórií v podrobnostiach o riadku cenovej ponuky pre náklady zmení príslušné hodnoty v podrobnostiach o riadku cenovej ponuky pre predaj.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Mena v podrobnostiach o riadku cenovej ponuky pre náklady a predaj

Mena v detaile riadku ponuky pre predaj sa štandardne preberá z cenníka projektu, ktorý je účinný od dátumu začiatku podrobností riadka cenovej ponuky.

Mena v detaile riadka cenovej ponuky pre náklady sa štandardne preberá z cenníka zmluvnej jednotky cenovej ponuky, ktorý je účinný od dátumu začiatku podrobností riadka cenovej ponuky pre náklady.

> [!NOTE]
> Výpočty ziskovosti prevádzajú čiastku v podrobnostiach o riadku cenovej ponuky na náklady a predaj do základnej meny prostredia na vykazovanie celkovej odhadovanej marže v cenovej ponuke. Mohli by sa vyskytnúť chyby zaokrúhľovania mien a zmenené marže z dôvodu chýbajúcich výmenných kurzov platných k dátumu. Tieto výpočty používajte iba na cenové ponuky projektu, pretože ide o aproximácie a nejde o skutočné zákonné ani iné zostavy, ktoré si pri výmenných kurzoch vyžadujú vyššiu presnosť zaokrúhľovania a zohľadnenie účinnosti dátumu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
