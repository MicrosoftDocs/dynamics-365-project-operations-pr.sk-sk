---
title: Správa faktúry pro forma – čiastočné
description: Táto téma poskytuje informácie o práci s faktúrami pro forma.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ca6c2cc8855cfed592057ca129b436450104af99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274072"
---
# <a name="manage-a-proforma-invoice---lite"></a>Správa faktúry pro forma – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

V Dynamics 365 Project Operations sa faktúry pro forma vytvárajú ako rozšírenie k faktúram v Dynamics 365 Sales. Pokiaľ však ide o fakturáciu, existuje medzi procesom fakturácie v Sales a Project Operations veľa rozdielov. Nie je napríklad možné vytvoriť novú faktúru zo stránky **Zoznam faktúr** v Project Operations, ale je to možné urobiť v Sales. Tieto rozdiely a rozšírenia sú zavedené na podporu procesov fakturácie pre projekty, ktoré sa líšia od bežnej faktúry za predajnú objednávku.

> [!IMPORTANT]
> Z dôvodu týchto rozdielov nepoužívajte faktúry v aplikáciách Sales a Project Operations zameniteľne.

## <a name="invoice-header"></a>Hlavička faktúry

Nasledujúce informácie sú k dispozícii v hlavičke faktúry pro forma v aplikácii Project Operations.

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| **ID faktúry** | Karta **Súhrn** | ID sa vygeneruje automaticky po vytvorení faktúry pro forma. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole sa používa ako referencia pre každú faktúru pro forma. |
| **Názov** | Karta **Súhrn** | Predvolene nastavte na názov projektovej zmluvy. Toto pole môže používateľ upravovať. | &nbsp;  |
| **Mena** | Karta **Súhrn** | Predvolene nastavte na menu projektovej zmluvy. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |&nbsp; |
| **Cenník** | Karta **Súhrn** | Predvolene nastavte cenník projektovej zmluvy. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Príležitosť** | Karta **Súhrn** | Odkaz na prepojenú príležitosť. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp;  |
| **Zmluva** | Karta **Súhrn** | Odkaz na prepojenú projektovú zmluvu. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Zákazník** | Karta **Súhrn** | Odkaz na prepojenú projektovú zmluvu. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |&nbsp;  |
| **Opis** | Karta **Súhrn** | Textové pole, ktoré popisuje faktúru. Toto pole môže používateľ upravovať. | &nbsp; |
| **Fakturovať komu** a súvisiace polia | **Karta Súhrn** | Predvolené hodnoty sú stanovené od zákazníka projektovej zmluvy. Toto pole môže používateľ upravovať.  | &nbsp; |
| **Stav** | Karta **Súhrn** | Nastavuje nasledujúce možnosti: **Aktívne**, **Zatvorené**, **Zaplatené** a **Zrušené**, ktoré môže používateľ meniť. | Medzi nepodporované stavy aplikácie Project Operations patria **Zatvorené** a **Zrušené**. </br> Stav je nastavený na **Aktívne**, keď je vystavená faktúra. </br>Stav by mal byť nastavený na **Zaplatené** až po potvrdení faktúry. |
| **Stav projektovej faktúry** | Karta **Súhrn** | Nastavuje nasledujúce možnosti: **Koncept**, **Prebieha kontrola** a **Potvrdené**, ktoré môže používateľ meniť. | V stavoch **Koncept** a **Prebieha kontrola** je možné faktúru upravovať. Faktúru nie je možné upravovať po potvrdení. |
| **Podrobná čiastka** | Karta **Súhrn** | Súčet súm na všetkých riadkoch faktúry po zálohách a odpočtoch. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole sa používa na výpočet konečnej sumy. |
| **Zľava (%)** | Karta **Súhrn** | Toto pole je možné upraviť a zadať percento zľavy. Toto pole nie je podporované funkciami aplikácie Project Operations. | Toto pole nie je podporované. |
| **Suma zľavy** | Karta **Súhrn** | Toto pole je možné upraviť a zadať sumu zľavy. Toto pole nie je podporované funkciami aplikácie Project Operations. | Toto pole nie je podporované. |
| **Suma bez prepravného** | **Karta Súhrn** | Celková suma na faktúre po uplatnení zliav. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole sa používa na výpočet konečnej sumy. |
| **Čiastka za prepravné** | Karta **Súhrn** | Toto pole je možné upraviť a zadať sumu prepravného. Toto pole nie je podporované funkciami aplikácie Project Operations. | Toto pole nie je podporované. |
| **Celková daň** | Karta **Súhrn** | Celková daň zo všetkých riadkov faktúry na faktúre. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Žiadne. |
| **Celková čiastka** | Karta **Súhrn** | Súčet sumy po zľavách a daniach. | Súčet predstavuje sumu, ktorú musí zákazník zaplatiť. |
## <a name="project-based-invoice-lines"></a>Riadky faktúr založených na projekte

V aplikácii Project Operations je vždy jeden riadok faktúry pre každý riadok projektovej zmluvy. Riadok faktúry sa vytvorí, aj keď neexistujú žiadne skutočné hodnoty. Nasledujúce informácie sú k dispozícii na riadku faktúry pro forma.

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| **ID faktúry** | Karta **Všeobecné** | Odkaz na ID faktúry. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Odkaz na ID faktúry je možné použiť na prechod späť na hlavičku faktúry. |
| **Názov** | Karta **Všeobecné** | Názov riadku faktúry nastavený predvolene z názvu riadku zmluvy. Toto pole môže používateľ upravovať. | &nbsp; |
| **Project** | Karta **Všeobecné** | Projekt na riadku zmluvy súvisiaceho projektu. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Odkaz na projekt je možné použiť na navigáciu k projektu. |
| **Spôsob fakturácie** | Karta **Všeobecné** | Spôsob fakturácie na riadku zmluvy súvisiaceho projektu. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Suma v riadku zmluvy** | Karta **Všeobecné** | Sumu zmluvy v riadku zmluvy súvisiaceho projektu. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Fakturované doteraz** | Karta **Všeobecné** | Súčet súm na všetkých podrobnostiach o riadkoch faktúry tejto faktúry. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Suma** | Karta **Všeobecné** | Súčet súm na všetkých účtovateľných podrobnostiach o riadkoch faktúry tejto faktúry. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole sa používa na výpočet konečnej sumy v hlavičke faktúry. |
| **Daň** | Karta **Všeobecné** | Súčet súm daní na všetkých podrobnostiach o riadkoch faktúry tohto riadka faktúry. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole sa používa na výpočet konečnej sumy dane v hlavičke faktúry. |
| **Celková suma** | Karta **Všeobecné** | Súčet celkových súm (**Daň + Sumy**) na všetkých účtovateľných podrobnostiach o riadkoch faktúry tohto riadka faktúry. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole sa používa na výpočet konečnej sumy v hlavičke faktúry. |


## <a name="invoice-line-details"></a>Podrobnosti o riadku faktúry

Každý riadok faktúry vo faktúre projektu obsahuje podrobnosti o riadku faktúry. Tieto podrobnosti o riadku súvisia s nevyfakturovanými skutočnými hodnotami a medzníkmi predaja, ktoré sa týkajú riadku zmluvy, na ktorý odkazuje riadok faktúry. Všetky tieto transakcie sú označené ako **Pripravené na fakturáciu**.

Pre riadok **Faktúra za čas a materiál**, sú podrobnosti o riadku faktúry zoskupené do **Účtovateľné**, **Neúčtovateľné** a **Bezplatné** na stránke **Riadok faktúry**. Podrobnosti **Účtovateľný riadok faktúry** sa pripočítavajú do celkovej sumy riadkov faktúry. **Bezplatné** a **Neúčtovateľné skutočné hodnoty** sa nepripočítavajú do celkovej sumy riadkov faktúry.

Pre riadok **Faktúra s pevnou cenou** sa podrobnosti riadka faktúry vytvárajú z medzníkov, ktoré sú označené ako **Pripravené na fakturáciu** na príslušnom riadku zmluvy. Po vytvorení detailu riadka faktúry z medzníka sa stav fakturácie v medzníku aktualizuje na **Bola vytvorená faktúra pre zákazníka**.

### <a name="edit-invoice-line-details"></a>Úprava podrobností riadka faktúry

Nasledujúce polia sú k dispozícii v podrobnosti riadka faktúry, za ktorým stojí skutočná hodnota nefakturovaného predaja:

| Pole | Popis | Nadväzujúci vplyv |
| --- | --- | --- |
| **Riadok faktúry** | Odkaz na **ID riadka faktúry**. Ide o pole iba na čítanie, ktoré je uzamknuté na úpravy. | Tento odkaz je možné použiť na prechod späť na hlavičku faktúry. |
| **Opis** | Opis podrobnosti riadka faktúry. Nastavené ako predvolené z poľa **Interné poznámky** v **Zadaní času** a z poľa **Popis** v **Zadaní výdavkov**. Pole môže používateľ upravovať.| &nbsp; |
| **Externý opis** | Opis podrobnosti riadka faktúry. Nastavené ako predvolené z poľa **Externé poznámky** v **Zadaní času** a z poľa **Popis** v **Zadaní výdavkov**. Pole môže používateľ upravovať. | Tento popis možno použiť na určenie toho, čo by malo byť na vytlačenej faktúre, ktorá sa odošle zákazníkovi. V aplikácii Project Operations nemá faktúra pro forma všetky požadované funkcie na konfiguráciu nastavení tlače pre faktúru. |
| **Dátum začatia** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole je možné upraviť v detaile nového riadka faktúry, ktorý nie je podložený skutočnými údajmi zdroja. |
| **Project** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Nastavené predvolene na projekt na súvisiacom riadku zmluvy. |
| **Úloha** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Pole je možné upraviť v detaile nového riadka faktúry, ktorý nie je podložený skutočnými údajmi zdroja. Rozbaľovací zoznam zobrazuje všetky úlohy, ktoré sú spojené s riadkom zmluvy príslušného projektu.  |
| **Kategória transakcie** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole je možné upraviť v detaile nového riadka faktúry, ktorý nie je podložený skutočným zdrojom. |
| **Rola** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole je možné upraviť v detaile nového riadka faktúry, ktorý nie je podložený skutočnými údajmi zdroja. |
| **Rezervovateľný zdroj** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole je možné upraviť v detaile nového riadka faktúry, ktorý nie je podložený skutočným zdrojom. |
| **Zdrojová jednotka** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole je možné upraviť v detaile nového riadka faktúry, ktorý nie je podložený skutočnými údajmi zdroja. |
| **Množstvo** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole je možné upraviť v detaile nového riadka faktúry, ktorý nie je podložený skutočnými údajmi zdroja. |
| **Plán jednotky** | Pre podrobnosti riadku faktúry je čas vždy nastavený na čas a nemožno ho upravovať. Pre výdavky je to predvolene nastavené zo skutočných hodnôt výdavkov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Predvolene nastavené na **Čas** na novom riadku faktúry, ktorý nie je podložený skutočnými hodnotami. |
| **Jednotka** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole je možné upraviť v podrobnostiach nového riadka faktúry, ktorý nie je podložený skutočnými údajmi zdroja. |
| **Cena** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Toto pole je možné upraviť v detaile nového riadka faktúry, ktorý nie je podložený skutočnými údajmi zdroja. Ak nie je zadaná žiadna hodnota, je predvolene nastavené po **Uložení**. |
| **Mena** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Nastavené ako predvolené v hlavičke faktúry pri vytváraní nového fakturačného detailu bez skutočného podloženia.  Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Suma** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Vypočítané ako **Množstvo \* Cena** pri vytváraní nového fakturačného detailu bez podloženia skutočnými hodnotami. Vypočíta sa po **Uložení**. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |
| **Daň** | Nastavené predvolene zo skutočných údajov zdroja. Pole môže používateľ upravovať | Toto pole môže používateľ upravovať pri vytváraní podrobností nového riadka faktúry bez podloženia skutočnými hodnotami. |
| **Celková suma** | Vypočítavané pole, vypočítané ako **Suma + daň**. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Typ fakturácie** | Nastavené predvolene zo skutočných údajov zdroja. Pole môže používateľ upravovať. | Výberom možnosti **Účtovateľné** sa pridá riadok k celkovej sume riadkov faktúry. **Bezplatné** a **Neúčtovateľné** sa vylúči z celkovej sumy riadkov faktúry. |
| **Typ transakcie** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Predvolene nastavené na **Fakturovaný predaj** a uzamknuté pri vytváraní novej **Podrobnosti o riadku faktúry** bez podloženia skutočnými hodnotami.  |
| **Trieda transakcie** | Nastavené predvolene zo skutočných údajov zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Nastavené predvolené na základe toho, či sa používateľ rozhodne vytvoriť podrobnosti riadku faktúry pre **Čas**, **Výdavky** alebo **Poplatok** pri súčasnom vytváraní novej **Podrobnosti o riadku faktúry** bez podloženia skutočnými hodnotami. Uzamknuté pre úpravy. |

Nasledujúce polia sú k dispozícii v podrobnosti riadka faktúry, ktorý je podložený medzníkom:

| Pole | Popis | Nadväzujúci vplyv |
| --- | --- | --- |
| **Riadok faktúry** | Odkaz na **ID riadka faktúry**. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | Odkaz je možné použiť na prechod späť na hlavičku faktúry. |
| **Opis** | Opis podrobnosti riadka faktúry. Nastavený predvolene z opisu medzníka zdroja. | &nbsp; |
|**Externý opis** | Opis podrobností riadka faktúry, ktorý je predvolene nastavený z opisu medzníka zdroja. | Toto pole možno použiť na určenie toho, čo by malo byť na vytlačenej faktúre, ktorá sa odošle zákazníkovi. V aplikácii Project Operations nemá faktúra pro forma všetky požadované funkcie na konfiguráciu nastavení tlače pre faktúru. |
| **Dátum začatia** | Nastavené ako predvolené z dátumu **Medzníka** medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Project** | Nastavené predvolene z medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Úloha** | Nastavené predvolene z medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Kategória transakcie** | Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Rola** | Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Rezervovateľný zdroj** | Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Zdrojová jednotka** | Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Plán jednotky** | Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Jednotka** | Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Cena** | Nastavené predvolene zo sumy medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Mena** | Nastavené predvolene z medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. |&nbsp; |
| **Suma** | Nastavené predvolene zo sumy medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Daň** | Nastavené predvolene zo sumy dane medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Celková suma** | Nastavené predvolene z celkovej sumy medzníka zdroja. Pole môže používateľ upravovať | &nbsp; |
| **Typ fakturácie** | Predvolene vždy nastavené na **Účtovateľné**. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Typ transakcie** | Nastavené predvolene z medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |
| **Trieda transakcie** | Nastavené predvolene z medzníka zdroja. Pole iba na čítanie, ktoré je uzamknuté pred úpravami. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Vytvorenie nových podrobností riadka faktúry

Na riadkoch faktúry za čas a materiál môžete vytvoriť nové podrobnosti riadka faktúry. Tieto podrobnosti riadka faktúry nie sú podporované skutočnými hodnotami. Na riadku faktúry za čas a materiál môžete vybrať **Nový** na vytvorenie nových podrobností o riadku faktúry pre triedy transakcií, ktoré sú zahrnuté v riadku zmluvy.

## <a name="refresh-invoice-transactions"></a>Obnovenie fakturačných transakcií

Ak máte skutočné údaje, ktoré prišli po vytvorení faktúry, môžete ich zahrnúť do faktúry.

1. V **Zobrazení backlogu pre fakturáciu** označte údaje ako **Pripravené na fakturáciu**.   
2. Otvorte draft faktúry pro forma a na páse s nástrojmi **Akcie** kliknite na **Obnoviť transakcie v riadku faktúry**.

  Takto sa vytvoria podrobnosti riadka faktúry pre všetky skutočné hodnoty, ktorých dátum je v minulosti a sú označené ako **Pripravené na fakturáciu**, ale ktoré nie sú zahrnuté vo faktúre.

## <a name="product-based-invoice-lines"></a>Riadky faktúr založených na produkte

V Project Operations môžete vytvoriť riadky faktúry pre produkty, ktoré sa nevzťahujú na žiadny projekt, alebo pre všetky projekty spolu s riadkami faktúr založenými na projektoch. Tieto riadky faktúry sa vytvárajú ako riadky zmlúv založené na produktoch a po označení ako pripravené na fakturáciu sa pridávajú ako riadky faktúr na založené na produktoch.

Po pridaní riadkov faktúr založených na produktoch ich nie je možné zmeniť. Môžu byť však vymazané z konceptu faktúry pro forma.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]