---
title: Denník integrácie v aplikácii Project Operations
description: Táto téma poskytuje informácie o práci s denníkom integrácie v aplikácii Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a5f4d524530594bd3118f9b320acf4033c5d503
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948349"
---
# <a name="integration-journal-in-project-operations"></a>Denník integrácie v aplikácii Project Operations

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Časové a výdavkové položky vytvoria transakcie **Skutočná hodnota**, ktoré predstavujú operatívny pohľad na prácu dokončenú na projekte. Dynamics 365 Project Operations poskytuje účtovníkom nástroj na kontrolu transakcií a úpravu účtovných atribútov podľa potreby. Po dokončení kontroly a úprav sa transakcie zapíšu do vedľajšej účtovnej knihy projektu a hlavnej účtovnej knihy. Účtovník môže vykonávať tieto činnosti pomocou denníka **Integrácia Project Operations** (**Dynamics 365 Finance** > **Projektový manažment a účtovníctvo** > **Denníky** > **Integrácia Project Operations**.

![Postup integračného denníka](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Vytvorenie záznamov v denníku Integrácia Project Operations

Záznamy v denníku Integrácia Project Operations sa vytvárajú pomocou periodického procesu **Import z pracovnej verzie tabuľky**. Tento proces môžete spustiť v ponuke **Dynamics 365 Finance** > **Projektový manažment a účtovníctvo** > **Periodické** > **Integrácia Project Operations** > **Import z pracovnej verzie tabuľky**. Proces môžete spustiť interaktívne alebo ho podľa potreby nakonfigurovať tak, aby bežal na pozadí.

Po periodickom spúšťaní procesu sa nájdu všetky skutočné hodnoty, ktoré ešte nie sú pridané do denníka Integrácia Project Operations. Pre každú skutočnú transakciu sa vytvorí záznam v účtovnom denníku.
Systém zoskupuje záznamy v účtovnom denníku do samostatných denníkov na základe hodnoty vybranej v poli **Jednotka periódy v denníku Integrácia Project Operations** (**Financie** > **Projektový manažment a účtovníctvo** > **Nastavenie** > **Parametre projektového manažmentu a účtovníctva**, karta **Project Operations v Dynamics 365 Customer Engagement**). Možné hodnoty pre toto pole sú:

  - **Dni**: Skutočné hodnoty sú zoskupené podľa dátumu transakcie. Pre každý deň sa vytvára samostatný denník.
  - **Mesiace**: Skutočné hodnoty sú zoskupené podľa kalendárnych mesiacov. Pre každý mesiac sa vytvára samostatný denník.
  - **Roky**: Skutočné hodnoty sú zoskupené podľa kalendárnych rokov. Pre každý rok sa vytvára samostatný denník.
  - **Všetky**: Všetky skutočné transakcie sú zahrnuté v rovnakom denníku integrácie. Ak denník nie je k dispozícii pri spustení periodického procesu, napríklad ak je denník v procese aktualizácie transakcií, vytvorí sa nový denník.

Riadky denníka sa vytvárajú na základe skutočných hodnôt projektu. Nasledujúci zoznam obsahuje niektoré z najvýznamnejších predvolených a transformačných pravidiel:

  - Každá skutočná transakcia projektu má riadok v denníku Integrácia Project Operations. Transakcie nákladov a nefakturovaných predajov pre typ fakturácie podľa času a materiálu sú zobrazené na samostatných riadkoch.
  - Pole **Dátum** predstavuje dátum transakcie. Pole **Dátum účtovnej uzávierky** predstavuje dátum, kedy je transakcia zaznamenaná do účtovnej knihy. Ak je dátum účtovania v [uzavretom finančnom období](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) a je nastavený parameter **Automaticky nastaviť dátum účtovania na otvorenie obdobia účtovnej knihy** na karte **Financie** na stránke **Parametre projektového manažmentu a účtovníctva**, systém upraví účtovný dátum transakcie na prvý dátum v nasledujúcom otvorenom období účtovnej knihy.
  - Pole **Kupón** zobrazuje číslo kupónu pre každú skutočnú transakciu. Poradie čísel kupónov je definované na karte **Číselné sekvencie** na stránke **Parametre projektového manažmentu a účtovníctva**. Každému riadku je priradené nové číslo. Po zapísaní kupónu môžete zobraziť, ako súvisia transakcie nákladov a nefakturovaných predajov výberom možnosti **Súvisiace kupóny** na strane **Transakcia kupónu**.
  - Pole **Kategória** predstavuje transakciu projektu a predvolené hodnoty založené na kategórii transakcií pre skutočnú hodnotu súvisiaceho projektu.
    - Ak je **Kategória transakcie** nastavená v skutočnej hodnote projektu a súvisiaca **Kategória projektu** existuje v danom právnom subjekte, kategória je predvolene nastavená na túto kategóriu projektu.
    - Ak **Kategória transakcie** nie je nastavená v skutočnej hodnote projektu, systém použije hodnotu v poli **Predvolené hodnoty kategórie projektu** na karte **Project Operations v Dynamics 365 Customer Engagement** na stránke **Parametre projektového manažmentu a účtovníctva**.
  - Pole **Zdroj** predstavuje zdroj projektu súvisiaci s touto transakciou. Zdroj sa používa ako referencia v návrhoch projektových faktúr zákazníkom.
  - Pole **Výmenný kurz** predvolené z nastavenia **Výmenný kurz mien** v Dynamics 365 Finance. Ak nastavenie výmenného kurzu chýba, periodický proces **Import z pracovnej verzie** nepridá záznam do denníka a do protokolu vykonania úlohy sa pridá chybové hlásenie.
  - Pole **Vlastnosť riadka** predstavuje typ fakturácie v skutočných hodnotách projektu. Mapovanie vlastnosti riadka a typu fakturácie je definované na karte **Project Operations v Dynamics 365 Customer Engagement** na stránke **Parametre projektového manažmentu a účtovníctva**.

V záznamoch účtovného denníka integrácie Project Operations je možné aktualizovať iba tieto účtovné atribúty:

- **Skupina dane z fakturovaného predaja** a **Skupina dane z fakturovaného predaja položky**
- **Finančné dimenzie** (pomocou akcie **Rozdelenie súm**)

Integračné záznamy v účtovnom denníku je možné odstrániť, avšak všetky nezverejnené riadky sa do denníka vložia znova po opätovnom spustení periodického procesu **Import z pracovnej verzie**.

Keď aktualizuje denník integrácie, vytvoria sa transakcie vedľajšej účtovnej knihy a hlavnej účtovnej knihy projektu. Používajú sa pri následnej fakturácii zákazníka, rozpoznávaní výnosov a finančnom vykazovaní.


[!INCLUDE[footer-include](../includes/footer-banner.md)]