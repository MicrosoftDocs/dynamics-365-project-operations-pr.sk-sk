---
title: Zabezpečovanie zdrojov pre projekty
description: Táto téma poskytuje informácie o zabezpečovaní zdrojov pre projekty.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755522"
---
# <a name="project-resourcing"></a>Zabezpečovanie zdrojov pre projekty

[!include [banner](../includes/banner.md)]

Táto téma poskytuje informácie o zabezpečovaní zdrojov pre projekty.

Jednou z výziev pre projektových manažérov a manažérov zdrojov počas fázy plánovania projektu je alokácia zdrojov, kde musia určiť a vyhradiť správny zdroj pre prácu na projekte. V Dynamics 365 Finance vám možnosti zdrojov pre projekty umožňujú definovať roly, ktoré sa považujú za dočasné zdroje, ktoré je možné rezervovať pre konkrétnu zákazku alebo časť zákazky. Tento typ zabezpečovania zdrojov umožňuje projektovým manažérom a správcom zdrojov splniť nasledujúce úlohy:

- Definovať rolu, ktorá má požadované kompetencie, aby bolo ľahké spárovať zdroje.
- Pomocou rolí definovať počiatočný plán interakcie, ktorý je založený na rezervovaných zdrojoch.
- Odhadnúť náklady a určiť počiatočný rozpočet na základe pridelených rolí a zdrojov pre projekt.
- Pomocou rolí odhadnúť počet rezervácií zdrojov, ktoré sú potrebné pre každú zákazku.
- Odhadnúť počet zdrojov, ktoré sú potrebné pre celý životný cyklus projektu.
- Navrhnúť koncept štruktúry rozdelenia práce (WBS) pomocou počiatočných priradení zdrojov.

[![Životný cyklus projektu](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Keď bude plánovanie projektu pokračovať, plánované zdroje je možné nahradiť personálnymi zdrojmi. Vedúci projektu sa môže tiež vrátiť späť a aktualizovať rezervácie zdrojov v ktorejkoľvek fáze projektu.

## <a name="set-up-project-resources"></a>Nastavenie zdrojov pre projekty
Musíte si pripraviť kalendár a priradiť ho k zamestnancovi alebo pracovníkovi. Kalendár sa používa na plánovanie projektu a pracovného času zdrojov, ktoré sú rezervované pre projekt. Počas nastavovania kalendára môžu projektoví manažéri v rámci optimalizácie zdrojov vykonať optimalizáciu zdrojov. Na základe harmonogramu kalendára je možné uvaliť obmedzenia na zdroje. Kalendár si môžete nastaviť na stránke **Kalendáre**.

Keď nastavujete pracovníka ako zdroj projektu, môžete si vybrať z pracovníkov, ktorí pracujú v spoločnosti, pre ktorú nastavujete zdroje. Prípadne si môžete vybrať pracovníkov z iných spoločností vo vašej organizácii. Títo pracovníci sú známi ako medzipodnikové zdroje.

Nasledujúce postupy vysvetľujú, ako nastaviť pracovníka ako zdroj projektu vo vašej spoločnosti a ako nastaviť medzipodnikový zdroj projektu.

### <a name="set-up-a-worker-as-a-project-resource"></a>Nastavenie pracovníka ako zdroja projektu

1. Na stránke **Pracovníci** v zozname **Pracovníci** vyberte pracovníka, ktorého pridávate ako zdroje projektu, a otvorte záznam pracovníka.
2. Na table Akcia vyberte možnosť **Projekt** &gt; **Nastaviť** &gt; **Nastavenie projektu**.
3. Vyberte kalendár a potom stránku zavrite.

Môžete tiež určiť predvolené projekty pre zdroj ako typ predbežného priradenia. Predbežné priradenia je možné použiť, keď manažér zdrojov alebo projektový manažér vopred vedia, na ktorých projektoch bude zdroj pracovať. Predbežné priradenia môžu byť tiež založené na žiadosti sponzora projektu alebo zákazníka. Na predbežné priradenie projektu vyberte na stránke **Priradiť projekty** na karte **Projekty** v zozname **Zostávajúce projekty** príslušný projekt.

### <a name="set-up-an-intercompany-resource"></a>Nastavenie medzipodnikového zdroja

Keď nastavíte pracovníka ako medzipodnikový zdroj, musíte dokončiť nastavenie v spoločnosti, ktorá ho prenajíma, ale aj ktorá si ho prenajíma.

**V spoločnosti, ktorá prenajíma**

1. V službe Financie skontrolujte, či je vybratá spoločnosť, ktorá prenajíma, a potom dokončite postup v predchádzajúcej časti „Nastavenie pracovníka ako zdroja projektu“.
2. Na stránke **Účtovanie medzi spoločnosťami** vyberte možnosť **Nové**.
3. V poli **ID právnickej osoby** vyberte spoločnosť, ktorá prenajíma. Vyplňte príslušné polia zodpovedajúcim spôsobom a potom vyberte položku **Uložiť a Zavrieť**.
4. Na stránke **Cena transferu** vyberte možnosť **Nové**.
5. V poli **Právnická osoba, ktorá si prenajíma** vyberte príslušnú spoločnosť.
6. Ak chcete prenajať spoločnosti, ktorá si prenajíma, iba ten zdroj, ktorý ste vytvorili na začiatku tejto časti v poli **Zdroj**, vyberte názov zdroja, ktorý ste vytvorili. Ak chcete v spoločnosti, ktorá prenajíma, sprístupniť všetky zdroje pre spoločnosť, ktorá si prenajíma, nechajte pole **Zdroje** prázdne.
7. Na stránke **Parametre projektového riadenia a účtovníctva**, na karte **Medzipodnikové**, nastavte možnosť **Povoliť medzipodnikové plánovanie zdrojov a časové rozvrhy** na **Áno**.

**V spoločnosti, ktorá si prenajíma**

- Na stránke **Zoznam zdrojov** vo filtri vyhľadávania zadajte názov zdroja, ktorý ste vytvorili pre spoločnosť, ktorá prenajíma, aby ste overili, či je uvedený v zozname zdrojov spoločnosti, ktorá si prenajíma.

## <a name="manage-resource-competencies"></a>Spravovanie kompetencií v oblasti zdrojov
Kompetencie v oblasti zdrojov sú podstatnou súčasťou riadenia zdrojov. Kompetencie môžu byť použité ako základ pre určenie zdrojov, ktoré majú správnu rovnováhu medzi zručnosťami, vzdelaním, certifikáciou a skúsenosťami s projektom. Tieto informácie by ste mali nastaviť pre každý zdroj a pravidelne ich aktualizovať. Týmto spôsobom môžete maximalizovať schopnosti, keď sa priraďujú konkrétne kompetencie zdrojov počas priradenia zdrojov projektu.

[![Príklady zručností, certifikácií, vzdelania a projektových skúseností](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Nasledujúce postupy vysvetľujú, ako nastaviť niektoré kompetencie pre zdroj.

Na nastavenie kompetencií pracovníka môžete použiť buď stránku so zoznamom **Pracovníci** v sekcii Ľudské zdroje alebo stránku so zoznamom **Zdroje** v časti Projektové riadenie a účtovníctvo. Pre nasledujúce postupy sa použije stránka so zoznamom **Pracovníci** v sekcii Ľudské zdroje.

### <a name="set-up-competencies-certificates"></a>Nastavenie kompetencií: Certifikáty

1. Na stránke so zoznamom **Pracovníci** vyberte riadok pre pracovníka, o ktorom chcete pridať informácie o certifikáte.
2. Na table Akcia na karte **Pracovník** v skupine **Kompetencie** vyberte **Certifikáty**.
3. Vyberte **Nový** a potom v poli **Typ certifikátu** vyberte **PMP**.
4. V poli **Dátum začiatku** vyberte **1.10.2015** a následne **Uložiť**.

### <a name="set-up-competencies-skills"></a>Nastavenie kompetencií: Odbornosti

1. Na stránke so zoznamom **Pracovníci** skontrolujte, či je stále vybraný pracovník, ktorého ste použili v predchádzajúcom postupe. Na table Akcia na karte **Pracovník** v skupine **Kompetencie** potom vyberte **Odbornosti**.
2. Vyberte **Nové**.
3. V poli **Odbornosť** vyberte **Projektový manažment**.
4. V poli **Úroveň** vyberte **5 Expert**.
5. V poli **Dátum úrovne** vyberte **1-/14/2014**.
6. V poli **Roky skúseností** zadajte **10**.
7. Vyberte **Uložiť** a potom zatvorte stránku.

## <a name="create-a-new-project"></a>Vytvorenie nového projektu
1. Na stránke **Projektový manažment** vyberte **Nový projekt** a zadajte nasledujúce hodnoty:

    - **Typ projektu:** Čas a materiál
    - **Názov projektu:** Fáza 2 inovácie na XYZ
    - **Skupina projektov:** TM\_WIP
    - **Identifikátor projektovej zmluvy:** 00000002

2. Vyberte **Vytvoriť projekt**.

### <a name="assign-a-resource-to-a-project"></a>Priradenie zdroja k projektu

1. Na stránke **Pracovníci** v zozname **Pracovníci** vyberte záznam pre pracovníka, pre ktorého ste predtým nastavili kompetencie, a otvorte záznam pracovníka.
2. Na table Akcia na karte **Projekt** v skupine **Nastavenie** vyberte **Priradiť projekty**.
3. Na stránke **Priradenia projektu na overenie zdrojov** na karte **Projekty** v poli **Pridať projekt k vybraným projektom** nastavte filter na projekt **Fáza 2 inovácie na XYZ**.
4. Na table **Zostávajúce projekty** vyberte projekt a potom ho kliknutím na tlačidlo so šípkou pridajte na tablu **Vybrané projekty**.

Podľa potreby môžete k zdroju tiež priradiť kategórie. Typ kategórie je buď **Náklady** alebo **Príjem**. Typ kategórie určuje vaša organizácia. Ak pre zdroj nie sú priradené žiadne kategórie, služba Finance vyhľadá predvolenú kategóriu hodinových cien pre náklady a výnosy.

### <a name="set-up-project-resource-and-role-characteristics"></a>Nastavenie zdroja projektu a charakteristiky roly

Projektový manažér môže pomocou funkcie financovania projektu vytvoriť roly, ktoré sú potrebné pre projekt. Roly je možné použiť, ak potvrdené zdroje nie sú pri rezervácii zdrojov stále známe. Roly je možné dočasne rezervovať ako plánované zdroje, aby ste mohli pokračovať v etapách plánovania projektu.

[![Ukážka roly](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenár:** Spoločnosť Contoso bola najatá na dokončenie projektu typu Čas a materiál, ktorý má schválené stanovy projektu. Junior projektový manažér ešte stále dokončuje rozsah projektu. Správca zdrojov v súčasnosti identifikuje konkrétne zdroje, ktoré budú vyhradené na prácu na novom projekte. Z dôvodu kritickej povahy projektu požiadal sponzor projektu jednu z rolí Senior projektového manažéra. Správca zdrojov musí získať nový zdroj a definovať rolu v systéme pre prípad, že junior projektový manažér vyžaduje informácie o zdroji počas plánovania projektu.

Nasledujúce kroky ukazujú, ako môže správca zdrojov nastaviť rolu Senior projektového manažéra a priradiť k nej vlastnosti zdrojov. Neskôr sa dá rola použiť na vyhľadanie dostupných zdrojov, ktoré zodpovedajú požadovaným kompetenciám v oblasti zdrojov.

1. Na stránke **Nastaviť roly** vyberte **Nová** a zadajte nasledujúce hodnoty:

    - **ID roly:** Senior projektový manažér
    - **Opis:** Senior projektový manažér

2. Stlačte možnosť **Vytvoriť**.
3. Vyberte rolu **Senior projektový manažér** a potom vyberte **Nakonfigurovať vlastnosti**.
4. V poli **Typ vlastností** vyberte **Zručnosť**.
5. V poli **Dostupné vlastnosti** zadajte hľadanú zručnosť.
6. V poli **Typ vlastnosti** vyberte **Certifikát**.
7. V poli **Dostupné vlastnosti** zadajte hľadaný typ certifikátu.

### <a name="assign-a-project-resource-to-a-project"></a>Priradenie zdroja projektu k projektu

1. Na stránke **Všetky projekty** vyberte projekt **Fáza 2 inovácie na XYZ**.
2. Na karte **Projektový tím a plánovanie** vyberte **Pridať**.
3. V poli **Rola** vyberte **Člen tímu**.
4. Vyberte **Rezervovať z kalendára**.
5. Na stránke **Dostupnosť zdrojov** vyberte **Zobraziť nastavenia**.
6. Na stránke **Upraviť nastavenia zobrazenia** zadajte nasledujúce hodnoty:

    - **Formát pre zobrazenie rozsahu dátumov:** Deň
    - **Zobraziť popisy dostupnosti:** Áno
    - **Zobraziť zostávajúcu kapacitu:** Áno

7. V zozname zdrojov vyberte zdroj.
8. Vyberte **Pevná rezervácia** a **Plná kapacita**.


### <a name="assign-a-resource-to-a-default-role"></a>Priradenie zdroja k predvolenej role

Aby ste pomohli projektovým manažérom alebo správcom zdrojov, aby sa mohli hlbšie ponoriť do zdrojov, ktoré je možné rezervovať pre projekt. Môžete priradiť predvolenú rolu k existujúcemu zdroju alebo k novo získanému zdroju. Napríklad keď bol Daniel prijatý do zamestnania, mal skúsenosti a zručnosti na to, aby obsadil úlohu obchodného analytika. Správca zdrojov pridelil túto rolu ako predvolenú rolu Daniela. Preto správca zdrojov pridal Daniela do skupiny obchodných analytikov, ktorí sú k dispozícii na prácu na projektoch.

Počas rezervácie zdrojov môžu projektoví manažéri filtrovať zdroje rolí, ktoré sú k dispozícii na prácu na projektoch. Tieto informácie môžu použiť ako jedno kritérium, keď uskutočňujú multikriteriálnu rozhodovaciu analýzu počas plnenia zdrojov. Môžu tiež pridať do filtra ďalšie charakteristiky zdrojov, aby vyhľadali zdroje, ktoré majú špecifické zručnosti, vzdelanie a skúsenosti pre daný projekt.

**Scenár:** Schválený projekt sa začal a rola Senior projektového manažéra bola vyhradená ako plánovaný zdroj počas fázy plánovania projektu. Správca zdrojov teraz získal zdroj na splnenie úlohy Senior projektový manažér.

1. Na stránke **Zoznam zdrojov** vyberte **Daniel Goldschmidt**.
2. Na stránke **Rola zdroja** vyberte **Nová** a zadajte nasledujúce hodnoty:

    - **Účinná:** Zadajte aktuálny dátum.
    - **Exspirácia:** Zadajte **Nikdy**.
    - **Rola:** Zadajte **Senior projektový manažér**.

3. Vyberte **Uložiť** a potom zatvorte stránku.
4. Na karte **Kompetencie** pridajte zručnosť **ProjectMgmt** a certifikát **PMP**.

## <a name="set-up-role-based-pricing"></a>Nastavte ceny na základe rolí
Pre roly je možné nastaviť všetky ceny týkajúce sa nákladov, predajov a prenosov.

1. Na stránke **Predajná cena (hodina)** vyberte **Nový** a zadajte dátum účinnosti.
2. V stĺpci **Rola** vyberte rolu.
3. V stĺpci **Určenie ceny** zadajte cenu pre vybratú rolu zdroja.

## <a name="form-a-project-team"></a>Vytvorenie projektového tímu
Ak chcete použiť roly, ktoré boli predtým v projekte nastavené, musí projektový manažér priradiť tieto roly k projektu. K projektu je možné priradiť viac rolí. Aby sa predišlo zámene, sú tieto roly počas rezervácie automaticky označené. Ak napr. projektový manažér vyžaduje troch softvérových inžinierov, tri roly softvérového inžiniera, ktoré majú označenie **softvérový inžinier 1**, **softvérový inžinier 2** a **softvérový inžinier 3** sa generujú automaticky. Ak boli pre danú rolu predtým nastavené vlastnosti, použijú sa ako filter počas hľadania zdroja. Podľa potreby je možné pridať ďalšie vlastnosti, aby sa hľadanie ešte vylepšilo.

Nastavenia zobrazenia je možné tiež prispôsobiť, aby sa získal lepší prehľad o dostupnosti zdrojov. K dispozícii sú možnosti zobrazenia hodinovej, dennej, týždennej, mesačnej, štvrťročnej a ročnej dostupnosti. K dispozícii je tiež možnosť zobraziť dostupnú a zostávajúcu kapacitu zdrojov. Táto možnosť je užitočná na správu času, keď odhadujete dostupný čas na aktivity alebo dostupnosť zdrojov.

Projektový manažér môže na stránke zvoliť rolu a potom, ak je k dispozícii zdroj, ktorý vyhovuje požiadavke, vybrať rezerváciu zdroja na vyplnenie roly. Upozorňujeme, že v tomto okamihu fázy plánovania nie je potrebné rezervovať zdroje. Pri vytváraní štruktúry WBS môžete roly nahradiť personálnymi zdrojmi pre projekt. Ak sú roly nahradené personálnymi zdrojmi v štruktúre WBS, nastavenie zdrojov automaticky aktualizuje zoznam a plánovanie projektového tímu.

[![Zoznam projektového tímu, ktorý zahŕňa roly aj skutočné zdroje](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektový manažér má rôzne možnosti rezervácie zdroja pre projekt, ako napr. **Zostávajúca kapacita**, **Plná kapacita**, **Percento kapacity** a **Uveďte hodiny**. Tieto možnosti rezervácie je možné kedykoľvek zrušiť, ak sa zmení priradenie zdrojov. Podporované sú dva typy rezervácií:

- **Pevná rezervácia** – Rezervácia zdroja bola schválená a bolo potvrdené, že bude pracovať na zákazke po stanovenú dobu.
- **Predbežná rezervácia** – Rezervácia zdroja bola predbežne nastavené na prácu na zákazke po stanovenú dobu.

Nasledujúci postup vysvetľuje, ako vytvoriť projektový tím.

### <a name="create-a-project-team"></a>Vytvorenie projektového tímu

1. Na stránke so zoznamom **Všetky projekty** vyberte projekt a potom vyberte **Upraviť**.
2. Na karte **Projektový tím a plánovanie** v poli **Naplánujte dátum ukončenia** zadajte do poľa dátum začatia plánu plus jeden mesiac. Napríklad, ak je dátum začatia plánu 24. júna 2017 (24. 6. 2017), zadajte **24/07/2017**.
3. Stlačte možnosť **Pridať**.
4. V table **Pridať do projektu roly** v poli **Rola** vyberte **Senior projektový manažér**.
5. Vyberte **Požadované kompetencie**.
6. Na stránke **Vybrať vlastnosti** sú predvolene vybrané vlastnosti, ktoré ste predtým nastavili pre rolu Senior projektového manažéra. Vyberte položku **OK**.
7. Na stránke **Pridajte do projektu roly** v poli **Počet zdrojov** zadajte **1**.
8. V poli **Zdroje** vyhľadávanie zobrazuje všetky zdroje, ktoré majú požadované kompetencie. Vyberte **Daniel Goldschmidt** a potom **Vytvoriť**.
9. Na stránke **Projekt** vyberte položku **Pridať**.
10. V table **Pridať do projektu roly** v poli **Rola** vyberte **Člen tímu**. V poli **Počet zdrojov** zadajte **5**.
11. Stlačte možnosť **Vytvoriť**.
12. Na stránke **Projekty** vyberte **Vyplniť zdroj**.

## <a name="resource-capacity-synchronization"></a>Synchronizácia kapacity zdroja
Procesy synchronizácie zdrojov pomáhajú zaručiť, že informácie pre kalendár a základný kalendár sa prenášajú až do plánovania zdrojov projektu. Ak dôjde k zmene kalendára, procesy vykonajú požadované aktualizácie plánovania zdrojov projektu. Procesy tiež pomáhajú zvýšiť výkon, pretože informácie o zdrojoch z kalendára sú synchronizované vopred. Preto sa aktualizácie informácií o plánovaní zdrojov vyskytujú rýchlejšie. Odporúčame naplánovať procesy ako dávkové, nie po jednom. V opačnom prípade existuje riziko, že niekto zabudne na zahrnuté dátumy pri poslednej synchronizácie informácií. Ak sa nepoužívajú zahrnuté dátumy, počas synchronizácie dátumov môžu nastať medzery.

![Synchronizácia kalendára](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Synchronizácia súhrnov kapacity zdroja

Proces synchronizácie je navrhnutý tak, aby synchronizoval všetky informácie z kalendára zdrojov. Tieto informácie zahŕňajú informácie základného kalendára o akýchkoľvek zmenách v tabuľke kapacity kalendára zdrojov projektu. Ak sú do projektu pridané nové zdroje, synchronizácia pomáha zaručiť, že sú k dispozícii aktualizované informácie z kalendára. Túto synchronizáciu je možné vykonať kedykoľvek.

Odporúčame používať dávku. Možnosti sú k dispozícii počas synchronizácie rezervácií kapacity.

1. Vyberte **Projektové riadenie a účtovníctvo** &gt; **Pravidelne** &gt; **Synchronizácia kapacity** &gt; **Synchronizácia súhrnov kapacity zdroja**.
2. Nastavte možnosti v nasledujúcej tabuľke.

    | Možnosť      | Popis |
    |-------------|-------------|
    | Kód obdobia | Voliteľne vyberte kód intervalu dátumu hlavnej účtovnej knihy, aby ste nastavili dátumy začiatku a konca procesu synchronizácie pre súhrn kapacity zdrojov. |
    | Počiatočný dátum  | Zadajte dátum začatia procesu synchronizácie pre súhrn kapacity zdrojov. |
    | Dátum skončenia    | Zadajte dátum ukončenia procesu synchronizácie pre súhrn kapacity zdrojov. |

[![Proces synchronizácie](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Nastavenie rolí v šablónach štruktúry WBS
Projektoví manažéri môžu nastaviť šablóny štruktúry WBS, ktoré môžu použiť pri vytváraní štruktúry WBS pre nové projekty. Projektoví manažéri môžu pridávať roly pri vytváraní šablón. Pomocou nasledujúceho postupu môžete priradiť rolu šablóne štruktúry WBS.

1. Vyberte **Projektové riadenie a účtovníctvo** &gt; **Nastaviť** &gt; **Projekty** &gt; **Šablóny štruktúry rozdelenia práce**.
2. Vyberte **Podrobnosti** pre vybranú šablónu štruktúry WBS.
3. Vyberte úlohu v zozname a potom v poli **Rola** vyberte rolu, ktorú chcete priradiť k úlohe.

### <a name="work-with-a-wbs"></a>Práca so štruktúrami WBS

Môžete vytvoriť novú štruktúru WBS alebo skopírovať štruktúru WBS z existujúcej šablóny štruktúry WBS. Projektový manažér môže ľahko spravovať zdroje prideľovaním rolí novým úlohám v štruktúre WBS. Roly je možné vymeniť buď po získaní zdroja, alebo po identifikácii potvrdeného zdroja na prácu na úlohe. Táto flexibilita umožňuje projektovým manažérom vykonávať tieto úlohy:

- Určiť počet zdrojov, ktoré sú potrebné pre pracovné balíčky štruktúry WBS.
- Odhadnúť náklady na projekt.
- Stanoviť predbežný rozpočet.
- Odhadnúť trvanie aktivity na základe rolí a zdrojov.
- Vypracovať niektoré plány riadenia projektu na základe dostupných informácií o projekte.

Do štruktúry WBS boli pridané ďalšie možnosti, aby sa lepšie využila funkčnosť zdrojov.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Možnosť</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Priradenia zdrojov</td>
<td>Zobrazovanie pridelených zdrojov, dátumov, počtu hodín a typu rezervácie pre úlohy v štruktúre WBS.</td>
</tr>
<tr class="even">
<td>Automaticky generovať tím</td>
<td>Automatické pridávanie plánovaných zdrojov pomocou rolí, ktoré sú spojené s úlohou. Služba Finance automaticky navrhuje plánované zdroje pomocou multikriteriálnej rozhodovacej analýzy založenej na rolách. Po nastavení rol a úsilia (hodín) pre úlohy v štruktúre WBS a po uvoľnení štruktúry vyberte <strong>Automaticky generovať tím</strong>. Požadovaný počet plánovaných zdrojov sa pridá do štruktúry WBS a na kartu <strong>Plánovanie projektu a tímu</strong>.</td>
</tr>
<tr class="odd">
<td>Zdroj (rozbaľovací zoznam)</td>
<td>Na stránke <strong>Spustiť priradenie zdrojov</strong> môžete vybrať zdroje pre pevnú alebo predbežnú rezerváciu, na základe zadaného trvania. Môžete upraviť nastavenie zobrazenia, aby ste videli a nastavili trvanie aktivít zdrojov. Zdroje na úrovni pracovného balíka môžete vybrať a priradiť pomocou nasledujúcich možností:
<ul>
<li><strong>Prijať</strong> – Potvrdenie zmien zdroja, ktorý je priradený k úlohe.</li>
<li><strong>Zrušiť</strong> – Zrušenie zmien zdroja, ktorý je priradený k úlohe.</li>
<li><strong>Priradiť automaticky</strong> – Dostupný personálny zdroj, ktorý má zodpovedajúcu rolu, sa automaticky vyberie a priradí k vybranej úlohe.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na stránke **Všetky projekty** vyberte projekt **Fáza 2 inovácie na XYZ**.
2. Vyberte **Plán** &gt; **Aktivity** &gt; **Štruktúra rozdelenia práce**.
3. Vyberte **Nový** a pridajte do štruktúry WBS tieto aktivity prvej úrovne:

    - Inicializácia
    - Plánovanie
    - Vykonáva sa
    - Monitorovanie a riadenie
    - Zatvoriť

4. Nastavenie dátumov a úsilia (hodiny), ako je znázornené na nasledujúcom obrázku.

    [![Nastavenie dátumov a úsilia](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Vyberte riadok úloh **Inicializácia** a potom v poli **Rola** vyberte **Senior projektový manažér**.
6. Stlačte možnosť **Publikovať**.
7. Na rovnakom riadku v poli **Zdroje** vyberte **Daniel Goldschmidt** a potom vyberte **Prijať**.
8. Vyberte riadok úloh **Plánovanie** a potom v priečinku **Rola** vyberte **Obchodný analytik**.
9. Vyberte **Publikovať** a potom vyberte **Automaticky generovať tím**.
10. V dialógovom okne vyberte **Áno**.
11. V poli **Zdroj** overte, či obsahuje hodnotu **Obchodný analytik 1**.
12. Pre zdroj **Obchodný analytik 1** otvorte vyhľadávanie a vyberte **Spustiť priradenie zdrojov**. Potom vyberte pracovníka pre danú úlohu.
13. Vyberte**Predbežné priradenie** &gt; **Plná kapacita**.

    > [!NOTE] 
    > Nedostanete varovanie, že zadaný zdroj je teraz 2, pretože počet zdrojov zostáva 1.

14. Na stránke **Štruktúra rozdelenia práce** overte priradenie zdrojov v štruktúre WBS a potom vyberte **Uložiť**.

## <a name="resource-fulfillment-for-planned-resources"></a>Plnenie zdrojov pre plánované zdroje
Projektový manažér môže naplánovať požadované roly zdrojov pre projekt. Správca zdrojov uvidí tieto plánované zdroje ako požiadavky na stránke **Plnenie zdrojov** a môže priradiť skutočné zdroje.

1. Na stránke **Všetky projekty** vyberte projekt **Fáza 2 inovácie na XYZ**.
2. Vyberte **Projekt** a potom **Upraviť**.
3. Na karte **Projektový tím a plánovanie** vyberte **Pridať**.
4. V dialógovom okne **Pridať roly** vyberte rolu **Vývojár softvéru**.
5. Vyberte **Vytvoriť** a potom zatvorte stránku projektu.
6. Na stránke **Plnenie zdrojov** vyberte **Softvérový vývojár 1** pre **Projekt inovácie XYZ, fáza 2**.
7. Vyberte pracovníka a potom vyberte položku **Priradiť**.
8. Overte, či riadok pre **Softvérový vývojár 1** bol odstránený pre **Projekt inovácie XYZ, fáza 2**.
9. Na karte **Projektový tím a plánovanie** pre projekt **Fáza 2 inovácie XYZ** overte, či bol pracovník, ktorého ste vybrali v predchádzajúcom kroku, pridaný ako **Vývojár softvéru**.

## <a name="requests-for-project-resources"></a>Žiadosti o zdroje pre projekty
Funkcie pre plánovanie zdrojov projektu slúži iba na to, aby správcovia zdrojov distribuovali personálne zdroje na zákazky alebo projekty. Ak chcete povoliť túto funkciu, dokončite nasledujúce úlohy alebo skontrolujte, či boli dokončené:

- Nastaviť číselné sekvencie.
- Nastavte pracovné postupy riadenia projektu a účtovníctva.
- Povoliť pracovné postupy týkajúce sa požiadaviek na zdroje.

Po dokončení predchádzajúcich úloh môžete podľa potreby dokončiť nasledujúce úlohy:

- Vytvoriť požiadavku na zdroj z personálne obsadeného zdroja s predbežnou rezerváciou.
- Monitorovať požiadavky na zdroje.
- Splniť požiadavky na zdroje.
- Vyžiadajte si personálny zdroj zo štruktúry WBS.
- Zarezervujte si zdroje pre projekt bez toho, aby ste museli vyžadovať personálny zdroj.

## <a name="monitor-project-teams"></a>Monitorovanie projektových tímov
1. Na stránke **Všetky projekty** vyberte prepojenie **ID projektu** pre projekt **Fáza 2 inovácie XYZ**.
2. Na rýchlej karte **Projektový tím a plánovanie** skontrolujte správnosť zdrojov projektu, ktoré sú uvedené.
