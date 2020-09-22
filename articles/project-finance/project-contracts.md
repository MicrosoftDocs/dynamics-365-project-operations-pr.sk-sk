---
title: Projektové zmluvy
description: Táto téma poskytuje príklady projektových zmlúv, ktoré môžete vytvoriť pre rôzne typy projektov a zdrojov financovania, a ako môžete spravovať zmluvy a fakturovať zákazníkom projektu.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755616"
---
# <a name="project-contracts"></a>Projektové zmluvy

[!include [banner](../includes/banner.md)]

Tento článok poskytuje príklady projektových zmlúv, ktoré môžete vytvoriť pre rôzne typy projektov a zdrojov financovania, a ako môžete spravovať zmluvy a fakturovať zákazníkom projektu.

Typ projektu, ktorý vytvoríte pre projektovú zmluvu, určuje metódu, ktorá sa používa na fakturáciu zákazníkom projektu. Môžete upraviť projektovú zmluvu a súvisiaci projekt, ale nemôžete zmeniť typ projektu. 

Použitím projektovej zmluvy môžete fakturovať jeden alebo viac projektov súčasne. Zmluva o projekte tiež pomáha zaručiť konzistentný postup fakturácie pre každý podprojekt v štruktúre projektu. 

Každý projekt, ktorý bude fakturovaný, musí byť spojený s projektovou zmluvou. Nastavenia projektovej zmluvy sa vzťahujú na všetky projekty a čiastkové projekty, ktoré sú spojené s danou projektovou zmluvou. 

V projektovej zmluve môže byť uvedený jeden alebo viac zdrojov financovania. Preto môžete rozdeliť fakturáciu medzi viacerých poskytovateľov financovania, nastaviť limity financovania tak, aby sa zdrojom financovania neúčtovalo viac ako zadaná suma, a nakonfigurovať pravidlá financovania účtovania výdavkov.

## <a name="funding-for-project-contracts"></a>Financovanie projektových zmlúv
Niektoré zmluvy o projekte určujú, že zodpovednosť za financovanie nákladov na projekt je zdieľaných viac strán. Tu sú niektoré príklady:

-   Veľký zákazník, ktorý má viac divízií, požaduje, aby sa financovanie projektu rozdelilo podľa divízií.
-   Vaša spoločnosť zdieľa náklady na veľký projekt s externou organizáciou.
-   Cestný projekt spolufinancujú dve obce.
-   Prepojovací projekt je financovaný z vládneho grantu a súkromnej spoločnosti.

V Dynamics 365 Finance, môžete rozdeliť fakturáciu za jednu transakciu alebo za celý projekt medzi viacerých zákazníkov, granty alebo organizácie. 

V prípade projektov, ktoré majú viacerých donorov, sa všetky strany, ktoré prispievajú na financovanie pokročilého projektu financovania, nazývajú zdroje financovania. Keď je zákazník, organizácia alebo grant definovaný ako zdroj financovania, možno ho priradiť k jednému alebo viacerým pravidlám financovania. Pravidlá financovania obsahujú kritériá, ktoré určujú spôsob alokovania poplatkov pre rôzne zdroje financovania projektu. 

Pretože položky na sklade, napríklad tie, ktoré sa objavujú na požiadavkách na objednávku a objednávkach, nemožno rozdeliť, nie je možné v čase distribúcie rozdeliť sumu nákladov medzi viac zdrojov financovania. Preto hodnota zdroja financovania zostáva 0 (nula) až do zaúčtovania emisie zásob. Keď sa zaúčtuje výdaj zásob, čiastka nákladov sa rozdelí podľa pravidiel distribúcie účtov pre projekt.

Tu je niekoľko krokov, ktoré môžete urobiť, aby ste uľahčili rozdelenie fakturácie medzi viac zdrojov financovania:

-   Zadajte, aby všetky transakcie, ktoré sú zadané pre projekt, používali rovnakú menu predaja ako zmluva o projekte.
-   Nastavte limity financovania tak, aby sa za projekt nefinancoval zdroj financovania vyšší ako stanovená suma.
-   Nakonfigurujte pravidlá financovania a limity financovania pre každého pracovníka, položku, kategóriu, skupinu kategórií a typ transakcie (alebo pre všetky typy transakcií).
-   Vyberte voliteľné dátumy začatia a ukončenia, aby ste určili obdobie, v ktorom je každé pravidlo financovania platné.
-   Uveďte percento, za ktoré je zodpovedný každý zdroj financovania.
-   Uveďte, ktorý zdroj financovania je zodpovedný za zaokrúhľovanie rozdielov, ktoré sú spôsobené výpočtami alokácie financovania.
-   Nastavte pravidlá, ktoré určujú, ako sa náklady na projekt fakturujú externým zákazníkom a účtujú interným organizáciám.
-   Transakcie zaznamenávajte na pozdržanom finančnom účte, až kým nezískate ďalšie financovanie alebo kým sa nerozhodnete znášať náklady interne.

Na určenie, ktorá daňová skupina sa má priradiť k transakcii, sa v projekte vyhľadá priradenie daňovej skupiny. Ak na úrovni projektu nebolo vykonané žiadne priradenie daňových skupín, prehľadá sa projektová zmluva.

### <a name="example-multiple-funding-sources-simple"></a>Príklad: Viacero zdrojov financovania (jednoduché)

Nasledujúca tabuľka poskytuje scenáre riadenia alokácie financovania medzi viacerými zdrojmi financovania. Tieto scenáre sú založené na nasledujúcich predpokladoch:

-   Nastavenie priorít sa zohľadňuje v alokácii finančných prostriedkov pred uplatnením ďalších kritérií pravidla financovania.
-   Nebolo určené žiadne časové rozpätie, ktoré by definovalo obdobie d, kedy je pravidlo financovania platné.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenár</strong></td>
<td><strong>Zdroj financovania</strong></td>
<td><strong>Percento pridelenia</strong></td>
<td><strong>Pridelenie priority</strong></td>
</tr>
<tr class="even">
<td>Chcete alokovať náklady na jeden zdroj financovania, kým sa nevyčerpajú jeho finančné prostriedky, alokovať náklady na druhý zdroj financovania, kým sa nevyčerpajú jeho finančné prostriedky, a nakoniec alokovať zvyšné náklady na tretí zdroj financovania.</td>
<td><ul>
<li>Zdroj　financovania　1</li>
<li>Zdroj　financovania　2</li>
<li>Zdroj　financovania　3</li>
</ul></td>
<td><ul>
<li>100 %</li>
<li>100 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Chcete prideliť 75 percent nákladov jednému zdroju financovania a 25 percent druhému zdroju financovania. Keď je ktorýkoľvek z týchto zdrojov financovania vyčerpaný, chcete zaplatiť zostávajúce náklady z tretieho zdroja financovania.</td>
<td><ul>
<li>Zdroj　financovania　1</li>
<li>Zdroj　financovania　2</li>
<li>Zdroj　financovania　3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Chcete prideliť 75 percent nákladov jednému zdroju financovania a 25 percent druhému zdroju financovania. Keď je ktorýkoľvek z týchto zdrojov financovania vyčerpaný, chcete rozdeliť zostávajúce náklad medzi tretí zdroj financovania a štvrtý zdroj financovania.</td>
<td><ul>
<li>Zdroj　financovania　1</li>
<li>Zdroj　financovania　2</li>
<li>Zdroj　financovania　3</li>
<li>Zdroj　financovania　4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Chcete prideliť prvých 25 percent nákladov jednému zdroju financovania a zvyšok druhému zdroju financovania.</td>
<td><ul>
<li>Zdroj　financovania　1</li>
<li>Zdroj　financovania　2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Príklad: Viacero zdrojov financovania (komplexné)

Máte tri zdroje financovania, ktoré chcete použiť v nasledujúcom poradí:

1.  Používajte zdroj financovania 2 a zdroj financovania 3 rovnako, kým sa nevyčerpá zdroj financovania 2.
2.  Pokračujte v používaní zdroja financovania 3, kým sa nevyčerpá.
3.  Použite zdroj financovania 1 po vyčerpaní zdroja financovania 3.

Ak chcete dosiahnuť tento cieľ, musíte najprv vykonať nasledujúci postup:

-   Nastavte limity financovania pre zdroj financovania 2 a zdroj financovania 3 pre ich príslušné výšky.
-   Vytvorte si nasledujúce pravidlá financovania:
    -   Pravidlo 1 (Priorita 1): Prideliť 50 percent transakcií na zdroj financovania 2 a 50 percent na zdroj financovania 3.
    -   Pravidlo 2 (Priorita 2): Prideliť 100 percent transakcií zdroju financovania 3.
    -   Pravidlo 3 (Priorita 3): Prideliť 100 percent transakcií zdroju financovania 1.

Toto nastavenie funguje, pretože transakcie sa kontrolujú podľa pravidiel a obmedzení, aby sa určilo, či sa niektoré z nich na danú transakciu vzťahujú. Ak sa na transakciu nevzťahujú žiadne konkrétne pravidlá alebo limity, použije sa pravidlo Všetky transakcie. Pravidlo Všetky transakcie sa zhoduje so všetkými transakciami. 

Ak sa zistí pravidlo, ktoré sa zhoduje s transakciou, použije sa najskôr percento, ktoré bolo v danom pravidle pridelené, ale až potom, čo sa zhody porovnajú s limitmi, ktoré boli stanovené. Ak bol limit splnený a zdroje zdroja financovania sú vyčerpané, pravidlo financovania spojené s limitom financovania sa nebude brať do úvahy a program skontroluje ďalšie platné pravidlo. 

V niektorých prípadoch možno podľa pravidla prideliť iba časť transakcie. Môže sa to stať, pretože pri alokácii transakcie sa dosiahne limit. V takom prípade je podľa tohto pravidla pridelená iba určitá suma, napríklad 50 percent na každý zdroj financovania. To je prípad pravidla 1, ktoré je opísané skôr v tejto časti. Zvyšok je pridelený podľa nasledujúceho pravidla v poradí. 

Nasledujúca tabuľka skúma tento scenár podrobnejšie.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Zameranie</strong></td>
<td><strong>Podrobné informácie</strong></td>
</tr>
<tr class="even">
<td>Pravidlá financovania</td>
<td><ul>
<li>Pravidlo 1 (priorita 1): Všetky transakcie. Zdroj 2 prideľte na 50% a zdroj financovania 3 na 50%.</li>
<li>Pravidlo 2 (priorita 2): Všetky transakcie. Prideľte zdroj financovania 3 na 100%.</li>
<li>Pravidlo 3 (priorita 2): Všetky transakcie. Prideľte zdroj financovania 1 na 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Limity financovania</td>
<td><ul>
<li>Limit zdroja financovania 1 = 10,000.00</li>
<li>Limit zdroja financovania 2 = 500.00</li>
<li>Limit zdroja financovania 3 = 750.00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transakcia 1</td>
<td><strong>Hodnota transakcie:</strong> 100.00<strong>Financovanie:</strong> Transakcia je platená iba podľa pravidla 1, pretože transakcia je úplne zaplatená po uplatnení pravidla 1. Transakcia je financovaná rovnakým dielom medzi zdrojom financovania 2 a zdrojom financovania 3.
<ul>
<li>Zdroj financovania 2: 50.00</li>
<li>Zdroj financovania 3: 50.00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transakcia 2</td>
<td><strong>Hodnota transakcie:</strong> 5,000.00<strong>Financovanie:</strong> Transakcia sa platí podľa všetkých troch pravidiel. <strong>Pravidlo 1</strong>
<ul>
<li>Zdroj financovania 2: 450.00</li>
<li>Zdroj financovania 3: 450.00</li>
</ul>
<strong>Pravidlo 2</strong>
<ul>
<li>Zdroj financovania 3: 250.00 (= 750.00 – 50.00 – 450.00)</li>
</ul>
<strong>Pravidlo 3</strong>
<ul>
<li>Zdroj financovania 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Celkové prostriedky, ktoré sú rozdelené pre každý zdroj financovania</td>
<td><ul>
<li>Zdroj financovania 1: 3,850.00</li>
<li>Zdroj financovania 2: 500.00</li>
<li>Zdroj financovania 3: 750.00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Pravidlá fakturácie
Pri rokovaniach o zákazke na projekt so zákazníkom definujete, ako a kedy môžete zákazníkovi fakturovať prácu na projekte. Po nastavení zmluvy o projekte a projektu môžete nastaviť fakturačné pravidlá pre projekt. Pravidlá fakturácie vychádzajú z podmienok projektu, ktoré sú uvedené v projektovej zmluve. Pravidlá fakturácie, ktoré môžete vytvoriť, závisia od podmienok zmluvy o projekte a typu projektu, napríklad Čas a materiál alebo Fixná cena, ktorý priradíte k pravidlu fakturácie. Pre projektovú zmluvu môžete vytvoriť viac ako jedno fakturačné pravidlo. Pravidlo fakturácie môžete tiež priradiť viacerým projektom, ktoré sú spojené s rovnakou zmluvou o projekte a majú podobné fakturačné podmienky. 

Môžete nastaviť nasledujúce typy pravidiel fakturácie:

-   **Jednotka dodávky** – Fakturujte zákazníka, keď dokončíte jednotku dodávky. Jednotky dodávky definujete v zmluve.
-   **Pokrok** - Fakturujte zákazníka, keď dokončíte stanovené percento projektu. Môžete nastaviť fakturačné pravidlo na automatický výpočet percenta dokončenej práce alebo môžete ručne vypočítať percento dokončenej práce a sumu, ktorá sa má fakturovať zákazníkovi.
-   **Medzník** – Fakturujte zákazníkovi celú sumu medzníka projektu, keď sa tento míľnik dosiahne.
-   **Poplatok** – Fakturujte zákazníka za svoje služby plus poplatok za správu, čo je zvyčajne percento z ceny služieb.
-   **Čas a materiál** – Fakturovať zákazníka za hodnotu času a materiálov použitých na projekte.

Pre všetky typy pravidiel fakturácie môžete určiť percento zadržania, ktoré sa odpočíta z faktúr zákazníka, kým projekt nedosiahne dohodnutú fázu. Percento zadržania platby je uvedené v projektovej zmluve. Suma sa počíta na základe a od celkovej hodnoty riadkov vo faktúre od zákazníka. 

Pre pravidlá fakturácie **Čas a materiál** a **Pokrok** môžete priradiť spoplatnené kategórie. Spoplatnené kategórie označujú transakcie, ktoré by mali byť zahrnuté vo faktúrach zákazníkov. 

Keď ste pripravení fakturovať zákazníkovi, suma fakturovaná za projekt sa vypočíta na základe pravidiel fakturácie a vygeneruje sa návrh faktúry projektu. 

Nasledujúce časti poskytujú príklady, ktoré ukazujú, ako nastaviť a spravovať pravidlá fakturácie pre projekt.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Príklad: Vytvorte fakturačné pravidlo založené na počte dodaných jednotiek

Vaša organizácia uzatvára dohodu o poskytnutí celkovo piatich školení zamestnancom zákazníka za cenu 10 000 za školenie. Fakturujete zákazníkovi po každom školení. 

Pri nastavovaní pravidiel fakturácie pre zmluvu používate tieto hodnoty:

-   Jednotkou dodávky je jedno školenie.
-   Jednotková cena je 10 000 za školenie.
-   Celkový počet jednotiek je päť školení.

Po absolvovaní jedného školenia môžete vytvoriť faktúru za 10 000 kusov za prvú dodanú jednotku a odoslať faktúru zákazníkovi.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Príklad: Vytvorte fakturačné pravidlo, ktoré je založené na zadanom percente dokončenia projektu (manuálny výpočet)

Vaša organizácia, softvérová konzultačná spoločnosť, uzavrie so zákazníkom dohodu o vývoji časti produktu, ktorý zákazník vyvíja. Vaša organizácia súhlasí s dodaním softvérového kódu v priebehu šiestich mesiacov. Zákazník súhlasí s tým, že zaplatí vašej organizácii za prácu celkovo 100 000. Pravidlo fakturácie vytvoríte tak, aby ste zákazníkovi fakturovali na základe percenta práce dokončenej na projekte, ako je uvedené v zmluve.

-   Na konci prvého mesiaca sa stretnete so zákazníkom, aby ste určili percento dokončenej práce. Keď zákazník a zákazník skontrolujú projekt, rozhodnete sa, že je projekt dokončený na 15 percent.
-   Vytvoríte faktúru za 15,000 (15 percent zo 100 000) a odošlete ju zákazníkovi.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Príklad: Vytvorte fakturačné pravidlo, ktoré je založené na zadanom percente dokončenia projektu (automatický výpočet)

Vaša organizácia, firma zaoberajúca sa vývojom softvéru, súhlasí s vytvorením balíka mzdového účtovníctva pre zákazníka za 30 000. Zákazník súhlasí s tým, že zaplatí vašej organizácii na základe percentuálnej hodnoty dokončenej práce. Odhadujete, že náklady na projekt sú 20 000. Zmluva o projekte špecifikuje kategórie prác, ktoré použijete v procese fakturácie. Nastavíte pravidlá fakturácie, ktoré automaticky počítajú čiastky faktúry za percento práce dokončenej pre každú kategóriu. Nastavíte rozpočet pre každú kategóriu:

-   **Vývoj** - Náklady 15 000 a výnosy 20 000
-   **Inštalácia** - Náklady 5 000 a výnosy 10 000

Pri prvom vytváraní zákazníckej faktúry sa suma faktúry automaticky počíta na základe nasledujúcich informácií:

-   Po mesiaci pracovník projektu odovzdá časový harmonogram projektu. Náklady na hodiny pracovníka sú 5 000 za vývoj a 1 000 za inštaláciu. Vývojové práce sú dokončené na 33 percent (5 000 skutočných nákladov/15 000 rozpočtových nákladov) a inštalačné práce sú dokončené z 20 percent (1 000 skutočných nákladov/5 000 rozpočtových nákladov).
-   Suma faktúry 8 667 sa počíta automaticky (33 percent z 20 000 + 20 percent z 10 000).
-   Vytvoríte faktúru za 8,667 a odošlete ju zákazníkovi.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Príklad: Vytvorte pravidlo fakturácie založené na dohodnutých míľnikoch

Vaša organizácia, manažérska poradenská firma, súhlasí s uskutočnením prieskumu trhu so spotrebným produktom, ktorý zákazník plánuje predať. Zákazník súhlasí s používaním vašich služieb po dobu troch mesiacov, počnúc marcom, a zaväzuje sa zaplatiť vašej organizácii 50 000. Projekt má tri míľniky:

-   Medzník 1: Zhromažďovanie údajov o spotrebiteľoch - 31. marca
-   Míľnik 2: Analýza spotrebiteľských údajov - 30. apríla
-   Míľnik 3: Predstavte návrh životaschopnosti produktu - 31. mája

Zákazník súhlasí s tým, že zaplatí vašej organizácii 10 000 za prvý míľnik, 20 000 za druhý míľnik a 20 000 za tretí míľnik. 

Pri vytváraní projektovej zmluvy súhlasíte s tým, že zákazníkovi vyúčtujete fakturáciu na základe míľnika, ktorý bol dokončený. Nastavenie pravidla fakturácie obsahuje nasledujúce kroky:

-   Definujte míľniky projektu.
-   Definujte sumu, ktorá sa má fakturovať zákazníkovi po dokončení každého míľnika.

Keď je prvý míľnik dokončený 31. marca, označíte míľnik ako dokončený, potom vytvoríte faktúru za 10 000 a pošlete ju zákazníkovi. Faktúru za míľnik nemôžete vytvoriť, kým neoznačíte míľnik ako dokončený.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Príklad: Vytvorte fakturačné pravidlo založené na službách plus poplatok za správu

Vaša organizácia, konzultačná spoločnosť v oblasti riadenia, súhlasí s vykonaním prieskumu trhu s cieľom vyhodnotiť životaschopnosť produktu, ktorý vyvíja zákazník, maloobchodná spoločnosť. Podmienky dohody určujú, že budete poskytovať služby svojim trom najlepším konzultantom v oblasti riadenia, ktorí budú výskum uskutočňovať na základe času a materiálov. Zákazník súhlasí s tým, že zaplatí 100 za hodinu plus 10-percentný poplatok za správu za konzultačné hodiny účtované projektu. 

Keď nastavujete projektovú zmluvu, vytvorte pravidlo fakturácie a pripočítajte 10-percentný poplatok za správu k konzultačným hodinám účtovaným projektu. 

Pri vytváraní faktúry pre zákazníka sa zákazníkovi účtuje 10-percentný poplatok za správu plus cena za konzultačné hodiny. Napríklad ak traja konzultanti na projekte pracovali spolu 200 hodín, na základe tohto výpočtu sa vytvorí faktúra za 22 000 kusov:

-   200 hodín pri 100 za hodinu = 20 000
-   10-percentný poplatok za správu = 2 000
-   Celková suma faktúry = 22 000

Ak sú poplatky zdaniteľné zákazníkom a v projektovej zmluve vyberiete skupinu dane z obratu, skupina dane z obratu sa automaticky zadá do pravidla fakturácie poplatkov.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Príklad: Vytvorte fakturačné pravidlo pre hodnotu času a materiálov

Vaša organizácia, spoločnosť zaoberajúca sa softvérovým poradenstvom, súhlasí s poskytnutím piatich technických konzultantov na prácu na projekte vývoja softvéru pre zákazníka na nasledujúcich šesť mesiacov. Zákazník sa zaväzuje zaplatiť 150 za každú konzultačnú hodinu plus náklady na kancelárske potreby. Vaša organizácia zašle zákazníkovi na konci každého mesiaca faktúru. 

Pri uzatváraní zmluvy o projekte súhlasíte s tým, že budete zákazníkovi každý mesiac fakturovať čas a materiály týkajúce sa projektu. Vytvoríte fakturačné pravidlo, ktoré obsahuje nasledujúce informácie:

-   Zmluvné obdobie je šesť mesiacov.
-   Konzultačný čas sa počíta so sadzbou 150 za hodinu.
-   Kancelárske potreby sa fakturujú v cene a celkové náklady na projekt nesmú prekročiť 10 000.
-   Zákaznícku faktúru vytvoríte na konci každého kalendárneho mesiaca počas projektu.

Počas prvého mesiaca konzultanti projektu zaznamenali spolu 800 hodín. Náklady na kancelárske potreby, ktoré sa účtujú za projekt, sú 2 000. Preto na konci mesiaca vytvoríte faktúru za 122 000, ktorá sa počíta ako 800 hodín pri 150 za hodinu, plus 2 000 za kancelárske potreby.



