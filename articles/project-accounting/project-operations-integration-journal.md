---
title: Denník integrácie v aplikácii Project Operations
description: Tento článok poskytuje informácie o práci s denníkom Integration v Project Operations.
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

Čas, výdavky, poplatky a materiálové položky vytvárajú **Skutočné** transakcie, ktoré predstavujú operačný pohľad na prácu dokončenú na projekte. Dynamics 365 Project Operations poskytuje účtovníkom nástroj na kontrolu transakcií a úpravu účtovných atribútov podľa potreby. Po dokončení kontroly a úprav sa transakcie zapíšu do vedľajšej účtovnej knihy projektu a hlavnej účtovnej knihy. Účtovník môže tieto činnosti vykonávať pomocou **Integrácia projektových operácií** denník (**Dynamics 365 Finance** > **Projektový manažment a účtovníctvo** > **Denníky** > **Integrácia projektových operácií** denník.

![Postup integračného denníka.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Vytvorenie záznamov v denníku Integrácia Project Operations

Záznamy v denníku Integrácia Project Operations sa vytvárajú pomocou periodického procesu **Import z pracovnej verzie tabuľky**. Tento proces môžete spustiť tak, že prejdete na **Dynamics 365 Finance** > **Projektový manažment a účtovníctvo** > **Pravidelné** > **Integrácia projektových operácií** > **Import z pracovnej tabuľky**. Proces môžete spustiť interaktívne alebo ho podľa potreby nakonfigurovať tak, aby bežal na pozadí.

Po periodickom spúšťaní procesu sa nájdu všetky skutočné hodnoty, ktoré ešte nie sú pridané do denníka Integrácia Project Operations. Pre každú skutočnú transakciu sa vytvorí záznam v účtovnom denníku.
Systém zoskupuje riadky žurnálu do samostatných žurnálov na základe hodnoty vybratej v **Jednotka obdobia v denníku Project Operations Integration** lúka (**Financie** > **Projektový manažment a účtovníctvo** > **Nastaviť** > **Projektový manažment a účtovné parametre**, **projektu na Dynamics 365 Customer Engagement** karta). Možné hodnoty pre toto pole sú:

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
    - Ak **Kategória transakcie** nie je nastavený v Project fact, systém použije hodnotu v **Predvolené nastavenia kategórie projektu** pole na **Operácie projektu na Dynamics 365 Customer Engagement** kartu na **Projektový manažment a účtovné parametre** stránku.
  - Pole **Zdroj** predstavuje zdroj projektu súvisiaci s touto transakciou. Zdroj sa používa ako referencia v návrhoch projektových faktúr zákazníkom.
  - The **Výmenný kurz** pole predvolené od **Výmenný kurz meny** nastaviť v Dynamics 365 Finance. Ak nastavenie výmenného kurzu chýba, periodický proces **Import z pracovnej verzie** nepridá záznam do denníka a do protokolu vykonania úlohy sa pridá chybové hlásenie.
  - Pole **Vlastnosť riadka** predstavuje typ fakturácie v skutočných hodnotách projektu. Vlastnosť linky a mapovanie typu fakturácie sú definované na **Operácie projektu na Dynamics 365 Customer Engagement** kartu na **Projektový manažment a účtovné parametre** stránku.

V záznamoch účtovného denníka integrácie Project Operations je možné aktualizovať iba tieto účtovné atribúty:

- **Skupina dane z fakturovaného predaja** a **Skupina dane z fakturovaného predaja položky**
- **Finančné dimenzie** (pomocou akcie **Rozdelenie súm**)

Riadky žurnálu integrácie možno vymazať. Všetky nezaúčtované riadky sa však po opätovnom spustení do denníka znova vložia **Import zo stagingu** periodický proces.

### <a name="post-the-project-operations-integration-journal"></a>Uverejnite denník integrácie projektových operácií

Keď aktualizuje denník integrácie, vytvoria sa transakcie vedľajšej účtovnej knihy a hlavnej účtovnej knihy projektu. Používajú sa pri následnej fakturácii zákazníka, rozpoznávaní výnosov a finančnom vykazovaní.

Vybraný denník integrácie projektových operácií možno zaúčtovať pomocou **Príspevok** na stránke denníka integrácie Project Operations. Všetky denníky je možné automaticky zaúčtovať spustením procesu na adrese **Periodiky** > **Integrácia projektových operácií** > **Post Project Operations integračný denník**.

Zaúčtovanie je možné vykonávať interaktívne alebo hromadne. Upozorňujeme, že všetky časopisy, ktoré majú viac ako 100 riadkov, budú automaticky zaúčtované v dávke. Ak chcete dosiahnuť lepší výkon, keď sa žurnály, ktoré majú veľa riadkov, uverejňujú v dávke, povoľte **Post Project Operations integračný denník pomocou viacerých dávkových úloh** funkcia v **Správa funkcií** pracovnom priestore. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Preneste všetky riadky s chybami účtovania do nového denníka

> [!NOTE]
> Ak chcete použiť túto funkciu, povoľte **Preneste všetky riadky s chybami účtovania do nového denníka integrácie projektových operácií** funkcia v **Správa funkcií** pracovnom priestore.

Táto funkcia pomáha zlepšiť skúsenosti s denníkom integrácie Project Operations. Keď je povolená, problémy s časovaním duálneho zápisu a problémy s nastavením už nebránia uverejňovaniu platných žurnálov. Počas účtovania do denníka integrácie projektových operácií systém overí každý riadok v denníku. Zaúčtuje všetky riadky, ktoré nemajú chyby a vytvorí nový denník pre všetky riadky, ktoré majú chyby účtovania.

Ak chcete skontrolovať žurnály, ktoré majú riadky s chybami účtovania, prejdite na **Projektový manažment a účtovníctvo** \> **Denníky** \> **Denník integrácie projektových operácií** a filtrujte zoznam časopisov pomocou **Pôvodný denník** lúka. Nasledujúci obrázok ukazuje príklad, kde sú žurnály na **Denník integrácie projektových operácií** stránka bola filtrovaná týmto spôsobom.

![Pôvodný žurnál zobrazený na stránke žurnálu integrácie Project Operations.](./media/transferLines-originalJournal.png)

Ak je periodická dávková úloha nakonfigurovaná na zaúčtovanie denníka integrácie, pokus o zaúčtovanie sa zopakuje a denníky sa zaúčtujú, ak bol problém s načasovaním vyriešený. Všetky zostávajúce žurnály by sa mali manuálne preskúmať tak, že si prezriete denníky a vykonáte všetky požadované kroky.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
