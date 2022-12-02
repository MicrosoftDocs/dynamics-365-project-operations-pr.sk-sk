---
title: Denník integrácie v aplikácii Project Operations
description: Tento článok poskytuje informácie o práci s denníkom integrácie v aplikácii Project Operations.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541097"
---
# <a name="integration-journal-in-project-operations"></a>Denník integrácie v aplikácii Project Operations

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Položky času, výdavkov, poplatkov a materiálov vytvoria transakcie **Skutočná hodnota**, ktoré predstavujú operatívny pohľad na prácu dokončenú na projekte. Dynamics 365 Project Operations poskytuje účtovníkom nástroj na kontrolu transakcií a úpravu účtovných atribútov podľa potreby. Po dokončení kontroly a úprav sa transakcie zapíšu do vedľajšej účtovnej knihy projektu a hlavnej účtovnej knihy. Účtovník môže vykonávať tieto činnosti pomocou denníka **Integrácia Project Operations** (**Dynamics 365 Finance** > **Projektový manažment a účtovníctvo** > **Denníky** > **Integrácia Project Operations**.

![Postup integračného denníka.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Vytvorenie záznamov v denníku Integrácia Project Operations

Záznamy v denníku Integrácia Project Operations sa vytvárajú pomocou periodického procesu **Import z pracovnej verzie tabuľky**. Tento proces môžete spustiť v ponuke **Dynamics 365 Finance** > **Projektový manažment a účtovníctvo** > **Periodické** > **Integrácia Project Operations** > **Import z pracovnej verzie tabuľky**. Proces môžete spustiť interaktívne alebo ho podľa potreby nakonfigurovať tak, aby bežal na pozadí.

Po periodickom spúšťaní procesu sa nájdu všetky skutočné hodnoty, ktoré ešte nie sú pridané do denníka Integrácia Project Operations. Pre každú skutočnú transakciu sa vytvorí záznam v účtovnom denníku.
Systém zoskupuje záznamy v účtovnom denníku do samostatných denníkov na základe hodnoty vybranej v poli **Jednotka periódy v denníku Integrácia Project Operations** (**Finance** > **Projektový manažment a účtovníctvo** > **Nastavenie** > **Parametre projektového manažmentu a účtovníctva**, karta **Project Operations** v Dynamics 365 Customer Engagement). Možné hodnoty pre toto pole sú:

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
    - Ak **Kategória transakcie** nie je nastavená v skutočnej hodnote projektu, systém použije hodnotu v poli **Predvolené hodnoty kategórie projektu** na karte **Project Operations** v Dynamics 365 Customer Engagement na stránke **Parametre projektového manažmentu a účtovníctva**.
  - Pole **Zdroj** predstavuje zdroj projektu súvisiaci s touto transakciou. Zdroj sa používa ako referencia v návrhoch projektových faktúr zákazníkom.
  - Pole **Výmenný kurz** sa predvolene nastavuje z nastavenia **Výmenný kurz mien** v Dynamics 365 Finance. Ak nastavenie výmenného kurzu chýba, periodický proces **Import z pracovnej verzie** nepridá záznam do denníka a do protokolu vykonania úlohy sa pridá chybové hlásenie.
  - Pole **Vlastnosť riadka** predstavuje typ fakturácie v skutočných hodnotách projektu. Mapovanie vlastnosti riadka a typu fakturácie je definované na karte **Project Operations v Dynamics 365 Customer Engagement** na stránke **Parametre projektového manažmentu a účtovníctva**.

V záznamoch účtovného denníka integrácie Project Operations je možné aktualizovať iba tieto účtovné atribúty:

- **Skupina dane z fakturovaného predaja** a **Skupina dane z fakturovaného predaja položky**
- **Finančné dimenzie** (pomocou akcie **Rozdelenie súm**)

Integračné záznamy v účtovnom denníku je možné odstrániť. Avšak všetky nezverejnené riadky sa do denníka vložia znova po opätovnom spustení periodického procesu **Import z pracovnej verzie**.

### <a name="post-the-project-operations-integration-journal"></a>Zaúčtovanie denníka integrácie Project Operations

Keď aktualizuje denník integrácie, vytvoria sa transakcie vedľajšej účtovnej knihy a hlavnej účtovnej knihy projektu. Používajú sa pri následnej fakturácii zákazníka, rozpoznávaní výnosov a finančnom vykazovaní.

Vybraný denník integrácie Project Operations možno zaúčtovať pomocou funkcie **Zaúčtovať** na stránke denníka integrácie Project Operations. Všetky denníky je možné automaticky zaúčtovať spustením procesu **Pravidelné** > **Integrácia Project Operations** > **Zaúčtovať integračný denník Project Operations**.

Zaúčtovanie je možné vykonávať interaktívne alebo hromadne. Upozorňujeme, že všetky denníky, ktoré majú viac ako 100 riadkov, budú automaticky zaúčtované v dávke. Ak chcete dosiahnuť lepší výkon, keď sa denníky, ktoré majú veľa riadkov, účtujú v dávke, povoľte funkciu **Zaúčtovať integračný denník Project Operations pomocou viacerých dávkových úloh** v pracovnom priestore **Správa funkcií**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Prenos všetkých riadkov s chybami účtovania do nového denníka

> [!NOTE]
> Ak chcete použiť túto funkciu, povoľte funkciu **Preniesť všetky riadky s chybami účtovania do nového denníka integrácie Project Operations** v pracovnom priestore **Správa funkcií**.

Táto funkcia pomáha zlepšiť skúsenosti s denníkom integrácie Project Operations. Keď je povolená, problémy s časovaním duálneho zápisu a problémy s nastavením už nebránia uverejňovaniu platných denníkov. Počas účtovania do denníka integrácie Project Operations systém overí každý riadok v denníku. Zaúčtuje všetky riadky, ktoré nemajú chyby a vytvorí nový denník pre všetky riadky, ktoré majú chyby účtovania.

Ak chcete skontrolovať denníky, ktoré majú riadky s chybami účtovania, prejdite do **Projektový manažment a účtovníctvo** \> **Denníky** \> **Denník integrácie Project Operations** a filtrujte zoznam denníkov pomocou poľa **Pôvodný denník**. Nasledujúci obrázok ukazuje príklad, kde sú denníky na stránke **Denník integrácie Project Operations** filtrované týmto spôsobom.

![Pôvodný denník zobrazený na stránke denníka integrácie Project Operations.](./media/transferLines-originalJournal.png)

Ak je periodická dávková úloha nakonfigurovaná na zaúčtovanie denníka integrácie, pokus o zaúčtovanie sa zopakuje a denníky sa zaúčtujú, ak bol problém s načasovaním vyriešený. Všetky zostávajúce denníky by sa mali manuálne preskúmať tak, že si prezriete denníky a vykonáte všetky požadované akcie.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
