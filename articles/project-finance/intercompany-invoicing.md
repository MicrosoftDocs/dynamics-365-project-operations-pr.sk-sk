---
title: Medzipodniková fakturácia
description: Tento článok poskytuje informácie a príklady medzipodnikovej fakturácie pre projekty.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0385c796ca1ac02d6b8f66c04dad21bafe15ef8
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755530"
---
# <a name="intercompany-invoicing"></a>Medzipodniková fakturácia

[!include [banner](../includes/banner.md)]

Tento článok poskytuje informácie a príklady medzipodnikovej fakturácie pre projekty.

Vaša organizácia môže mať viac divízií, dcérskych spoločností a ďalších právnych subjektov, ktoré si navzájom prenášajú produkty a služby na účely projektov. Právnická osoba, ktorá poskytuje službu alebo produkt, sa nazýva *požičiavajúca právnická osoba* a právnická osoba, ktorá prijíma službu alebo produkt, sa nazýva *Právnická osoba, ktorá si prenajíma*. 

Na nasledujúcom obrázku je znázornený typický scenár, v ktorom dva právne subjekty, SI FR (Právnická osoba, ktorá si prenajíma) a SI USA (požičiavajúca právnická osoba), zdieľajú zdroje na realizáciu projektu pre zákazníka A. Pre tento scenár má SI FR zmluvu na poskytovanie prác zákazníkovi A. 

[![Príklad medzipodnikovej fakturácie](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Cieľom je zvýšiť flexibilitu a výkonnosť kontroly nákladov, vykazovania výnosov, daní a ceny prevodu pre medzipodnikové projektové transakcie. Okrem toho sú k dispozícii nasledujúce možnosti:

-   Vytvárajte zákaznícke faktúry voči projektu v právnickej osobe, ktorá si prenajíma pomocou medzipodnikových časových výkazov, výdavkov a faktúr dodávateľov v požičiavajúcej právnickej osobe.
-   Podpora výpočtov daní a nepriamych nákladov.
-   Odložiť vykazovanie výnosov v požičiavajúcej právnickej osobe a v prípade, keď by si požičiavajúca právnická osoba mala vykázať náklady.
-   Získavať príjmy z rozpracovania (WIP) v požičiavajúcej právnickej osobe.
-   Nastavte prevodné ceny, ktoré môžu vychádzať z rôznych cenových modelov. Tu sú niektoré príklady:
    -   **Množstvo** – Suma, ktorú zadáte do poľa **Stanovenie ceny** predstavuje skutočnú cenu za množstvo alebo jednotku.
    -   **Výška poplatkov** – Cena/náklady za transakciu plus suma poplatkov, ktoré zadáte v poli **Ceny**.
    -   **Percento poplatkov** - Cena za prevod je cena/náklady za transakciu vynásobená percentom poplatkov, ktoré zadáte do poľa **Ceny**.
    -   **Percento predajnej ceny** - Percento predajnej ceny, ktorá sa prevedie na požičiavajúci právny subjekt.
    -   **Čiastka pod predajnou cenou** - Suma, ktorú si požičiavajúca právnická osoba zadržuje z predajných cien pred prevodom na požičiavajúcu právnickú osobu.
    -   **Pomer príspevkov** - Číslo, ktoré zadáte do poľa **Ceny** je pomer príspevkov, ktorý je vyjadrený ako percento z predajnej ceny.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Príklad 1: Nastavenie parametrov pre medzipodnikovú fakturáciu
V tomto príklade je USSI požičiavajúca právnická osoba a jej zdroje vykazujú čas voči požičiavajúcej právnickej osobe FRSI, ktorá vlastní zmluvu s koncovým zákazníkom. Hodiny a výdavky, ktoré hlásia zamestnanci USSI, je možné zahrnúť do projektovej faktúry, ktorú generuje FRSI. Okrem toho existuje tretí zdroj transakcií, ktoré môžu pochádzať od požičiavajúcej právnickej osoby (v tomto príklade USSI), keď poskytuje služby zdieľaných dodávateľov dcérskym spoločnostiam (napríklad FRSI) a potom tieto náklady prenáša na projekty v rámci týchto dcérskych spoločností. Financie dokončia všetky zodpovedajúce faktúry a výpočty daní. 

V tomto príklade musí byť FRSI zákazníkom v právnickej osobe USSI a USSI musí byť dodávateľom v právnickej osobe FRSI. Potom môžete vytvoriť medzipodnikový vzťah medzi týmito dvoma právnickými osobami. Nasledujúci postup ukazuje, ako nastaviť parametre tak, aby sa obidve právnické osoby mohli zúčastňovať na medzipodnikovej fakturácii.

1. Nastaviť FRSI ako zákazníka v právnickej osobe USSI a nastaviť USSI ako dodávateľa v právnickej osobe FRSI. Existujú tri vstupné body pre kroky, ktoré sú potrebné pre túto úlohu.

   | Krok |                                                       Vstupný bod                                                        |                                                                                                                                                                                               Popis                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | V USSI kliknite na <strong>Pohľadávky</strong> &gt; <strong>Zákazníci</strong> &gt; <strong>Všetci zákazníci</strong>. |                                                                                                                                                                  Vytvorte nový záznam o zákazníkovi pre FRSI a vyberte skupinu zákazníkov.                                                                                                                                                                  |
   |  B   |    Vo FRSI kliknite na <strong>Záväzky</strong> &gt; <strong>Predajcovia</strong> &gt; <strong>Všetci predajcovia</strong>.     |                                                                                                                                                                    Vytvorte nový záznam o predajcovi pre USSI a vyberte skupinu predajcov.                                                                                                                                                                    |
   |  C   |                                  Vo FRSI otvorte záznam dodávateľa, ktorého ste práve vytvorili.                                  | Na paneli akcií na karte <strong>Všeobecné</strong> kliknite v skupine <strong>Nastavenie</strong> na možnosť <strong>Medzipodnikové</strong>. Na stránke <strong>Medzipodnikové</strong> na karte <strong>Obchodný vzťah</strong> nastavte posúvač <strong>Aktívny</strong> do polohy <strong>Áno</strong>. V poli <strong>Zákaznícka spoločnosť</strong> vyberte záznam zákazníka, ktorý ste vytvorili v kroku A. |


2. Kliknite na možnosť **Riadenie projektu a účtovníctvo** &gt; **Nastavte** &gt; **Účtovné parametre projektového riadenia** a potom kliknite na kartu **Medzipodnikové**. Spôsob nastavenia parametrov závisí od toho, či ste požičiavajúcou alebo požičiavajúcou právnickou osobou.
   -   Ak ste požičiavajúcou právnickou osobou, vyberte kategóriu obstarávania, ktorá by sa mala použiť na priradenie faktúr dodávateľa, ktoré sa generujú automaticky.
   -   Ak ste požičiavajúcim právnickým subjektom, pre každý prijímajúci subjekt vyberte predvolenú kategóriu projektu pre každý typ transakcie. Kategórie projektov sa používajú na konfiguráciu dane, keď fakturovaná kategória v medzipodnikových transakciách existuje iba v požičiavajúcej právnickej osobe. Môžete si zvoliť hromadenie výnosov z medzipodnikových transakcií. Toto nahromadenie sa vykoná pri zaúčtovaní transakcií a potom sa zruší, keď sa zaúčtuje medzipodniková faktúra.

3. Cvaknutie **Projektové riadenie a účtovníctvo** &gt; **Nastaviť** &gt;**Ceny** &gt; **Cena za prevod**.
4. Vyberte menu, typ transakcie a model ceny prevodu. Mena, ktorá sa používa na faktúre, je mena, ktorá je nakonfigurovaná v zázname zákazníka pre požičiavajúcu právnickú osobu v požičiavajúcej právnickej osobe. Mena sa používa na priradenie záznamov v tabuľke ceny prevodu.
5. Kliknite na **Hlavná kniha** &gt; **Nastavenie zverejňovania** &gt; **Medzipodnikové účtovníctvo** a vytvorte vzťah pre USSI a FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Príklad 2: Vytvorte a uverejnite medzipodnikový časový rozvrh
USSI, požičiavajúca právnická osoba, musí vytvoriť a zaúčtovať časový rozvrh projektu od FRSI, požičiavajúcej si právnickej osoby. Existujú dva vstupné body pre kroky, ktoré sú potrebné pre túto úlohu.

| Krok | Vstupný bod                                                                       | Popis                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektové riadenie a účtovníctvo** &gt; **Časové rozvrhy** &gt; **Všetky časové rozvrhy** | Vytvorte nový časový rozvrh. Na riadku časového rozvrhu v poli **Právnická osoba** stlačte možnosť **FRSI**. V poli **ID projektu** zvoľte projekt vo FRSI. Zadajte hodiny pre každý deň v týždni. |
| B    | Stránka **Pracovný rozvrh**                                                                | Po spustení pracovného toku uverejnite časový rozvrh a poznačte si číslo poukazu.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Príklad 3: Vytvorte a uverejnite medzipodnikovú faktúru predajcu
USSI, požičiavajúca právnická osoba, musí vytvoriť a zaúčtovať medzipodnikovú faktúru predajcu pre projektu od FRSI, požičiavajúcej si právnickej osoby. Táto faktúra dodávateľa predstavuje externú prácu a náklady, ktoré vykonali dodávatelia, a ktoré sú uhradené zo strany USSI. Existujú dva vstupné body pre kroky, ktoré sú potrebné pre túto úlohu.

| Krok | Vstupný bod                                                                                      | Popis                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Záväzky** &gt; **Faktúry** &gt; **Otvorené faktúry dodávateľa** &gt; **Faktúra nového dodávateľa** | Vytvorte novú faktúru dodávateľa a zadajte služby, ktoré boli obstarané v mene projektu FRSI.                                                                                                                                                                                  |
| B    | Stránka **Faktúra dodávateľa**                                                                      | Zadajte riadky, ktoré zastupujú outsourcované služby v mene FRSI. Na **Podrobnosti o riadku** FastTab na karte **Projekt** pre riadok faktúry v poli **Projektová spoločnosť** zadajte **FRSI**. Zadajte projekt a príslušné informácie. Potom zaúčtujte faktúru dodávateľa. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Príklad 4: Vytvorte a uverejnite medzipodnikovú faktúru
USSI, právnická osoba poskytujúca pôžičky, musí vytvoriť a zaúčtovať medzipodnikovú faktúru. Existujú dva vstupné body pre kroky, ktoré sú potrebné pre túto úlohu.

| Krok | Vstupný bod                                                                                             | Popis                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektové riadenie a účtovníctvo** &gt; **Faktúry projektu** &gt; **Faktúra pre medzipodnikových zákazníkov**  | Kliknutím na možnosť **Nový** otvorte stránku **Vytvoriť medzipodnikovú faktúru**.                                                                                  |
| B    | **Riadenie projektu a účtovníctvo** &gt; **Faktúry projektu** &gt; **Faktúry pre medzipodnikových zákazníkov** | Na stránke **Vytvorte medzipodnikovú faktúru**, zadajte právnickú osobu, zadajte transakciu, ktorá by mala byť zahrnutá, a potom kliknite na tlačidlo **Hľadať**. |
| C    | **Riadenie projektu a účtovníctvo** &gt; **Faktúry projektu** &gt; **Faktúry pre medzipodnikových zákazníkov** | Vyberte transakcie, ktoré chcete fakturovať, alebo kliknite na ikonu **Vybrať všetko** a fakturujte všetky transakcie v zozname a potom kliknite na tlačidlo **OK**.                  |
| D    | Stránka **Medzipodniková faktúra**                                                                       | Zobrazí sa návrh medzipodnikovej faktúry pre zákazníka.                                                                                             |
| E    | Stránka **Medzipodniková faktúra**                                                                       | Kliknite na možnosť **Zverejniť**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Príklad 5: Zaúčtujte faktúru dodávateľa a vystavte faktúru zákazníkovi
Keď požičiavajúca právnická osoba, USSI, zaúčtuje medzipodnikovú faktúru zákazníka, vytvorí sa zodpovedajúca čakajúca faktúra dodávateľa v požičiavajúcej právnickej osobe, FRSI. Po zaúčtovaní tejto faktúry dodávateľa fakturuje FRSI zákazníkovi projektu aj hodiny, ktoré zadal USSI. Existujú tri vstupné body pre kroky, ktoré sú potrebné pre túto úlohu.

| Krok | Vstupný bod                                                                                        | Popis                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Záväzky** &gt; **Faktúry** &gt; **Čakajúce faktúry dodávateľa**                            | Skontrolujte faktúru, aby ste overili, či sú zahrnuté hodnoty časového rozvrhu, a potom odošlite faktúru dodávateľa.                  |
| B    | **Riadenie projektu a účtovníctvo** &gt; **Faktúry projektu** &gt; **Návrhy projektovej faktúry** | Vytvorte novú projektovú faktúru pre projekt a overte, či sa zobrazia hodinové transakcie, ktoré boli zaúčtované.            |
| C    | Stránka **Projektová faktúra**                                                                       | Vyberte projektovú faktúru a potom kliknite na tlačidlo **Zobraziť podrobnosti**, kde skontrolujte náklady a výšku predaja. Potom zverejnite faktúru. |


Viac informácií nájdete na [Konfigurácia fakturácie medzipodnikových projektov](tasks/configure-intercompany-project-invoicing.md).


