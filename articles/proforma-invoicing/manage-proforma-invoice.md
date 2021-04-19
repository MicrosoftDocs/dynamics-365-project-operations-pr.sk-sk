---
title: Správa projektovej faktúry pro forma
description: Táto téma poskytuje informácie o tom, ako spravovať a pracovať s projektovými faktúrami pro forma.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9fd357648f8166cbcbe91ca1922739585f9fcfa9
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867240"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Správa projektovej faktúry pro forma

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

V Dynamics 365 Project Operations sa faktúry pro forma vytvárajú ako rozšírenie k faktúram v Dynamics 365 Sales. Pokiaľ však ide o fakturáciu, existuje medzi procesom fakturácie v Sales a Project Operations veľa rozdielov. Nie je napríklad možné vytvoriť novú faktúru zo stránky **Zoznam faktúr** v Project Operations, ale je to možné urobiť v Sales. Tieto rozdiely a rozšírenia sú zavedené na podporu procesov fakturácie pre projekty, ktoré sa líšia od bežnej faktúry za predajnú objednávku.

> [!IMPORTANT]
> Z dôvodu týchto rozdielov nepoužívajte faktúry v aplikáciách Sales a Project Operations zameniteľne.

## <a name="invoice-header"></a>Hlavička faktúry

Nasledujúce informácie sú k dispozícii v hlavičke faktúry pro forma v aplikácii Project Operations.

| Pole | Miesto | Popis |
| --- | --- | --- | 
| **ID faktúry** | Karta **Súhrn** | ID sa vygeneruje automaticky po vytvorení faktúry pro forma. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. Toto pole sa používa ako referencia pre každú faktúru pro forma. |
| **Názov** | Karta **Súhrn** | Predvolene nastavte na názov projektovej zmluvy. Toto je možné upravovať. | 
| **Mena** | Karta **Súhrn** | Predvolene nastavte na menu projektovej zmluvy. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Cenník** | Karta **Súhrn** | Predvolene nastavte cenník projektovej zmluvy. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Príležitosť** | Karta **Súhrn** | Odkaz na prepojenú príležitosť. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Zmluva** | Karta **Súhrn** | Odkaz na prepojenú projektovú zmluvu. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Zákazník** | Karta **Súhrn** | Odkaz na prepojenú projektovú zmluvu. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Opis** | Karta **Súhrn** | Textové pole, ktoré popisuje faktúru. Toto je možné upravovať. | 
| **Fakturovať komu** a súvisiace polia | **Karta Súhrn** | Predvolené hodnoty sú stanovené od zákazníka projektovej zmluvy. Toto je možné upravovať.  | 
| **Status** | Karta **Súhrn** | Nastavuje nasledujúce možnosti: **Aktívne**, **Zatvorené**, **Zaplatené** a **Zrušené** a je možné ich upravovať. Medzi nepodporované stavy aplikácie Project Operations patria **Zatvorené** a **Zrušené**. </br> Stav je nastavený na **Aktívne**, keď je vystavená faktúra. </br>Stav by mal byť nastavený na **Zaplatené** až po potvrdení faktúry.  | 
| **Stav projektovej faktúry** | Karta **Súhrn** | Nastavuje nasledujúce možnosti: **Koncept**, **Prebieha kontrola** a **Potvrdené** a je možné ich upravovať. V stavoch **Koncept** a **Prebieha kontrola** je možné faktúru upravovať. Faktúru nie je možné upravovať po potvrdení. | 
| **Podrobná čiastka** | Karta **Súhrn** | Súčet súm na všetkých riadkoch faktúry po zálohách a odpočtoch. Pole iba na čítanie, ktoré je uzamknuté pred úpravami.  Toto pole sa používa na výpočet konečnej sumy. | 
| **Zľava (%)** | Karta **Súhrn** | Toto pole je možné upraviť a zadať percento zľavy. Toto pole nie je podporované funkciami aplikácie Project Operations. Toto pole nie je podporované.|  
| **Suma zľavy** | Karta **Súhrn** | Toto pole je možné upraviť a zadať sumu zľavy. Toto pole nie je podporované funkciami aplikácie Project Operations. Toto pole nie je podporované. |  
| **Suma bez prepravného** | **Karta Súhrn** | Celková suma na faktúre po uplatnení zliav. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. Toto pole sa používa na výpočet konečnej sumy.  | 
| **Čiastka za prepravné** | Karta **Súhrn** | Toto pole je možné upraviť a zadať sumu prepravného. Toto pole nie je podporované funkciami aplikácie Project Operations. Toto pole nie je podporované. |
| **Celková daň** | Karta **Súhrn** | Celková daň zo všetkých riadkov faktúry na faktúre. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Celková čiastka** | Karta **Súhrn** | Súčet sumy po zľavách a daniach. Súčet predstavuje sumu, ktorú musí zákazník zaplatiť. | 

## <a name="project-based-invoice-lines"></a>Riadky faktúr založených na projekte

V aplikácii Project Operations je vždy jeden riadok faktúry pre každý riadok projektovej zmluvy. Riadok faktúry sa vytvorí, aj keď neexistujú žiadne skutočné hodnoty. Nasledujúce informácie sú k dispozícii na riadku faktúry pro forma.

| Pole | Miesto | Popis | 
| --- | --- | --- |
| **ID faktúry** | Karta **Všeobecné** | Odkaz na ID faktúry. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. Odkaz na ID faktúry je možné použiť na prechod späť na hlavičku faktúry. | 
| **Názov** | Karta **Všeobecné** | Názov riadku faktúry nastavený predvolene z názvu riadku zmluvy. Toto je možné upravovať. |
| **Project** | Karta **Všeobecné** | Projekt na riadku zmluvy súvisiaceho projektu. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. Odkaz na projekt je možné použiť na navigáciu k projektu. | 
| **Spôsob fakturácie** | Karta **Všeobecné** | Spôsob fakturácie na riadku zmluvy súvisiaceho projektu. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Suma v riadku zmluvy** | Karta **Všeobecné** | Sumu zmluvy v riadku zmluvy súvisiaceho projektu. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Fakturované doteraz** | Karta **Všeobecné** | Súčet súm na všetkých podrobnostiach o riadkoch faktúry tejto faktúry. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Suma** | Karta **Všeobecné** | Súčet súm na všetkých účtovateľných podrobnostiach o riadkoch faktúry tejto faktúry. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. Toto pole sa používa na výpočet konečnej sumy v hlavičke faktúry. | 
| **Daň** | Karta **Všeobecné** | Súčet súm daní na všetkých podrobnostiach o riadkoch faktúry tohto riadka faktúry. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. Toto pole sa používa na výpočet konečnej sumy dane v hlavičke faktúry. | 
| **Celková suma** | Karta **Všeobecné** | Súčet celkových súm (**Daň + Sumy**) na všetkých účtovateľných podrobnostiach o riadkoch faktúry tohto riadka faktúry. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. Toto pole sa používa na výpočet konečnej sumy v hlavičke faktúry. |

## <a name="invoice-line-details"></a>Podrobnosti o riadku faktúry

Každý riadok faktúry vo faktúre projektu obsahuje podrobnosti o riadku faktúry. Tieto podrobnosti o riadku súvisia s nevyfakturovanými skutočnými hodnotami a medzníkmi predaja, ktoré sa týkajú riadku zmluvy, na ktorý odkazuje riadok faktúry. Všetky tieto transakcie sú označené ako **Pripravené na fakturáciu**.

Pre riadok **Faktúra za čas a materiál** sú podrobnosti riadku faktúry sú zoskupené na stránke **Účtovateľné**, **Neúčtovateľné** a **Zadarmo** na stránke **Riadok faktúry**. Podrobnosti **Účtovateľný riadok faktúry** sa pripočítavajú do celkovej sumy riadkov faktúry. **Bezplatné** a **Neúčtovateľné skutočné hodnoty** sa nepripočítavajú do celkovej sumy riadkov faktúry.

Pre riadok **Faktúra s pevnou cenou** sa podrobnosti riadka faktúry sa vytvárajú z medzníkov, ktoré sú označené ako **Pripravené na fakturáciu** na príslušnom riadku zmluvy. Po vytvorení detailu riadka faktúry z medzníka sa stav fakturácie v medzníku aktualizuje na **Bola vytvorená faktúra pre zákazníka**.

### <a name="edit-invoice-line-details"></a>Úprava podrobností riadka faktúry

Nasledujúce polia sú k dispozícii v podrobnosti riadka faktúry, za ktorým stojí skutočná hodnota nefakturovaného predaja.

| Pole | Popis |
| --- | --- | 
| **Riadok faktúry** | Odkaz na **ID riadka faktúry**. Toto pole je iba na čítanie a pre úpravy je uzamknuté. Tento odkaz je možné použiť na prechod späť na hlavičku faktúry. | 
| **Opis** | Opis podrobnosti riadka faktúry. Nastavené ako predvolené z poľa **Interné poznámky** v **Zadaní času** a z poľa **Popis** v **Zadaní výdavkov**. Toto pole je možné upravovať.| 
| **Externý opis** | Opis podrobnosti riadka faktúry. Nastavené ako predvolené z poľa **Externé poznámky** v **Zadaní času** a z poľa **Popis** v **Zadaní výdavkov**. Toto pole je možné upravovať. Tento popis možno použiť na určenie toho, čo by malo byť na vytlačenej faktúre, ktorá sa odošle zákazníkovi. V aplikácii Project Operations nemá faktúra pro forma všetky požadované funkcie na konfiguráciu nastavení tlače pre faktúru. | 
| **Počiatočný dátum** | Toto pole je iba na čítanie, ktoré je predvolene nastavené zo zdroja skutočných hodnôt. |
| **Project** | Toto pole je iba na čítanie, a je predvolene nastavené zo zdroja skutočných hodnôt do projektu na príslušnom riadku zmluvy. |  
| **Úloha** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Kategória transakcie** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Rola** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |  
| **Rezervovateľný zdroj** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Spoločnosť zaisťujúca zdroje** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Zdrojová jednotka** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Počet** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |  
| **Plán jednotky** | Pre podrobnosti riadku faktúry je čas vždy nastavený na čas a nemožno ho upravovať. Pre výdavky je to predvolene nastavené zo skutočných hodnôt výdavkov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Jednotka** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |  
| **Cena** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Mena** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Množstvo** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Daň** | Nastavené predvolene zo skutočných údajov zdroja. Toto pole je možné upravovať.| 
| **Celková čiastka** | Vypočítavané pole, vypočítané ako **Suma + daň**. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Typ fakturácie** | Nastavené predvolene zo skutočných údajov zdroja. Toto pole je možné upravovať. Výberom možnosti **Účtovateľné** sa pridá riadok k celkovej sume riadkov faktúry. **Bezplatné** a **Neúčtovateľné** sa vylúči z celkovej sumy riadkov faktúry.| 
| **Vyberte produkt** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Produkt** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Názov produktu** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |  
| **Opis pridaného** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Typ transakcie** | Toto pole je iba na čítanie, ktoré je predvolene nastavené zo zdroja skutočných hodnôt na **Fakturovaný predaj**. |  
| **Trieda transakcie** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 

Nasledujúce polia sú k dispozícii v podrobnosti riadka faktúry, ktorý je podložený medzníkom.

| Pole | Popis |
| --- | --- | 
| **Riadok faktúry** | Odkaz na **ID riadka faktúry**. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. Odkaz je možné použiť na prechod späť na hlavičku faktúry.  | 
| **Opis** | Opis podrobnosti riadka faktúry. Nastavený predvolene z opisu medzníka zdroja. | 
|**Externý opis** | Opis podrobností riadka faktúry, ktorý je predvolene nastavený z opisu medzníka zdroja. Toto pole možno použiť na určenie toho, čo by malo byť na vytlačenej faktúre, ktorá sa odošle zákazníkovi. V aplikácii Project Operations nemá faktúra pro forma všetky požadované funkcie na konfiguráciu nastavení tlače pre faktúru. | 
| **Dátum začatia** | Nastavené ako predvolené z dátumu **Medzníka** medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Project** | Nastavené predvolene z medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Úloha** | Nastavené predvolene z medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Kategória transakcie** | Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Rola** | Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Rezervovateľný zdroj** | Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Zdrojová jednotka** | Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Plán jednotky** | Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Jednotka** | Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Cena** | Nastavené predvolene zo sumy medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Mena** | Nastavené predvolene z medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Suma** | Nastavené predvolene zo sumy medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Daň** | Nastavené predvolene zo sumy dane medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Celková suma** | Nastavené predvolene z celkovej sumy medzníka zdroja. Toto pole je možné upravovať. | 
| **Typ fakturácie** | Predvolene vždy nastavené na **Účtovateľné**. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Typ transakcie** | Nastavené predvolene z medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 
| **Trieda transakcie** | Nastavené predvolene z medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | 

## <a name="refresh-invoice-transactions"></a>Obnovenie fakturačných transakcií

Ak máte skutočné údaje, ktoré prišli po vytvorení faktúry, môžete ich zahrnúť do faktúry.

1. V **Zobrazení backlogu pre fakturáciu** označte údaje ako **Pripravené na fakturáciu**.   
2. Otvorte návrh faktúry pro forma a na páse s nástrojmi **Akcie** vyberte **Obnoviť transakcie v riadku faktúry**.

  Podrobnosti riadka na faktúre sa vytvárajú pre všetky skutočné hodnoty, ktoré sú dátované v minulosti a sú označené ako **Pripravené na fakturáciu**, ale nie je uvedené na faktúre.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
