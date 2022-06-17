---
title: Vytvorenie a potvrdenie účtovných denníkov zadaní
description: Tento článok poskytuje informácie o tom, ako vytvoriť a potvrdiť vstupné denníky v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912351"
---
# <a name="create-and-confirm-entry-journals"></a>Vytvorenie a potvrdenie účtovných denníkov zadaní

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Záznamové denníky používate na zaznamenávanie skutočných údajov priamo v Microsoft Dynamics 365 Project Operations. Keď používate vstupné denníky, nemusíte zadávať denníky času, nákladov a použitia materiálu do projektových operácií.

Jediný záznamový denník vám umožňuje vytvoriť viacero riadkov denníka. Keď je žurnál potvrdený, riadok žurnálu záznamu zaznamená aktuálnu hodnotu pre nasledujúce podrobnosti:

- Náklady alebo výnosy v závislosti od zvoleného typu transakcie.
- Vybraná trieda transakcie. Dostupné triedy sú **čas**, **·**, **·**, **·**, **a** **daň**.
- Projekt a/alebo úloha, ktorá je vybratá v riadku denníka.

Ak chcete vytvoriť žurnál vstupov v prevádzke projektu, postupujte podľa týchto krokov.

1. Ísť do **Predaj** \> **Transakcie** \> **Denníky**.
2. Na **Vstupné denníky** na stránke so zoznamom vyberte na table akcií **Nový** na vytvorenie denníka.
3. Na **Nový denník** stránke, v **Popis** zadajte popis časopisu.
4. Uistite sa, že **Typ denníka** pole je nastavené na **Vstup** a potom vyberte **Uložiť**. Po uložení nového Účtovného denníka a **Riadky denníka** na stránke denníka by sa mala objaviť karta.
5. Na **Riadky denníka** na paneli s nástrojmi nad mriežkou vyberte **Nový** na vytvorenie riadku vstupného denníka.
6. V **Rýchla tvorba** v dialógovom okne na vytvorenie riadku denníka zápisu nastavte polia podľa popisu v nasledujúcej tabuľke.

    | Pole | Description | Funkčný vplyv |
    | --- | --- | --- |
    | Trieda transakcie | Riadok denníka možno klasifikovať do jednej zo šiestich tried transakcií: **čas**, **·**, **·**, **·**, **·**, alebo **daň**. | The **daň** Transakčná trieda bola v Project Operations zastaraná. <br> Ak vytvoríte a **daň** trieda transakcií, nebude spracovaná pri fakturácii ani pri kalkuláciách nákladov alebo výnosov. **Míľnik** je trieda transakcií iba s príjmami. <br>The **Držiak** trieda transakcie predstavuje preddavok, ktorý bol prijatý od zákazníka. Vždy by mal byť vytvorený ako pár riadkov účtovného denníka predaja a nevyfakturovaného predaja. |
    | Typ transakcie | The **náklady**, **Interorg** a **Jednotkové náklady na zdroje** na zaznamenávanie nákladov by sa mali použiť typy transakcií.<br> The **Nevyfakturovaný predaj** a **Fakturovaný predaj** typy transakcií by sa mali používať na zaznamenávanie výnosov. | The **Držiak** trieda transakcií funguje iba s **Nevyfakturovaný predaj** a **Fakturovaný predaj** typy transakcií.<br> The **Míľnik** trieda transakcií funguje iba s **Fakturovaný predaj** typ transakcie. <br>The **Predaj Interorg** a **Jednotkové náklady na zdroje** typy transakcií sú použiteľné len pre **čas** trieda transakcií a tieto sú dostupné len pre vstupné denníky v scenári nasadenia Lite a nie pri nasadzovaní projektových operácií v scenároch Zdroj / Bez zásob. |
    | Vyberte produkt | Keď **Materiál** Ak je vybratá trieda transakcie, toto pole vám umožňuje určiť, či materiálová transakcia, pre ktorú vytvárate riadok denníka, je existujúci produkt alebo produkt so zápisom. | Ak vyberiete **Zápisný produkt**, môžete zadať názov produktu. |
    | Produkt | Odkaz na produkt z katalógu. | |
    | Description | Popis riadku denníka, ktorý uľahčuje jeho identifikáciu. | Pre riadky denníka nevyfakturovaného predaja sa hodnota použije ako popis pri vytváraní podrobností riadku faktúry. |
    | Vonkajší popis | Popis riadku denníka, ktorý možno použiť na zdieľanie s externými zainteresovanými stranami. | Pre riadky denníka nevyfakturovaného predaja sa hodnota použije ako externý popis pri vytváraní podrobností riadku faktúry. Môže sa objaviť aj na faktúre, ktorá je zaslaná zákazníkovi. |
    | Typ fakturácie | Hodnota, ktorá označuje, či sa riadok denníka bude počítať ako spoplatnená, doplnková alebo neúčtovateľná súčasť projektu. | V typickom toku je typ fakturácie odvodený od dohodnutých podmienok, ktoré sú nastavené v zmluve. Keď však zaznamenáte riadok denníka, môžete do tohto poľa zadať hodnotu. |
    | Dátum dokumentu | Použite dátum, kedy sa transakcia uskutočnila. | |
    | Počiatočný dátum | Použite dátum, kedy transakcia prebehla. | Toto pole sa používa na porovnanie s dátumom vytvorenia faktúry za transakcie **Nevyfakturovaný predaj** typu. Toto porovnanie vám pomôže rozhodnúť sa, či je transakcia s dátumom budúcnosti alebo s dátumom minulosti. Na faktúru budú pridané iba transakcie s dátumom minulosti. |
    | Konečný dátum | Použite dátum, kedy transakcia prebehla. | |
    | Dátum účtovnej uzávierky | Použite dátum, kedy bude účtovný dopad zaznamenaný. | |
    | Zákazník zmluvnej linky | Ak má riadok zmluvy iba jedného zákazníka, toto pole je štandardne nastavené na zákazníka v riadku zmluvy pri uložení riadku denníka. Ak má zmluvná linka viacerých zákazníkov, vyberte správneho zákazníka na zmluvnej linke. | Ak systém nedokáže určiť zákazníka v riadku zmluvy na riadku denníka a ak je prázdny na riadku **Nevyfakturovaný predaj** typu, ktorý je vytvorený z riadku denníka, skutočná nebude fakturovaná. |
    | Project | Vyberte projekt, do ktorého chcete zaznamenať skutočnosť. | Na základe zvoleného projektu, triedy transakcie a úlohy sa systém pokúsi určiť zmluvu, zmluvnú líniu a zmluvnú líniu zákazníka. |
    | Úloha | Vyberte úlohu, na ktorú sa má zaznamenať skutočnosť. | Ak ste úlohy priradili k zmluvným líniám počas nastavovania zmluvy, systém použije vybratú úlohu spolu s triedou projektu a transakcie na určenie zmluvy, zmluvnej línie a zmluvnej línie zákazníka. |
    | Kategória transakcie | Vyberte kategóriu transakcie, do ktorej chcete zaznamenať skutočnú transakciu. | Pre výdavky určuje vybratá kategória transakcie predvolenú cenu, ktorá sa zadá do riadku denníka pri jej uložení. |
    | Rola | Toto pole je relevantné pre riadky denníka času. Vyberte rolu zdroja, ktorý strávil čas na projekte a/alebo úlohe. | Ak pre riadky časového denníka použijete prednastavenú konfiguráciu na zadanie predvolených nákladov na zdroje a sadzieb účtov, zvolená rola sa použije spolu s jednotkou zdrojov na určenie predvolenej ceny, ktorá sa zadá do riadku denníka, keď je to uložené. Ak na zadávanie predvolených cien používate vlastnú konfiguráciu, mali by ste si túto konfiguráciu pozrieť a zistiť, či je **Role** pole sa používa na zadanie predvolených hodnôt cien. |
    | Subdodávateľská zmluva | Ak riadok denníka predstavuje subdodávateľskú kapacitu alebo subdodávateľské náklady alebo materiály, vyberte príslušnú subdodávku. | Keď sa zaznamenajú riadky nákladového denníka, vybratá subdodávka určí cenník, ktorý sa použije na zadanie štandardných jednotkových nákladov. |
    | Subdodávateľská linka | Ak riadok denníka predstavuje subdodávateľskú kapacitu alebo náklady alebo materiál subdodávok, vyberte príslušný riadok subdodávky. | Keď sa zaznamenajú riadky nákladového denníka, vybraná subdodávateľská linka zabezpečí, že výpočty dostupnej kapacity na linke subdodávok budú správne vypočítané. |
    | Metóda výpočtu sumy | Štandardne je toto pole nastavené na **Vynásobte množstvo cenou**. Pri použití tejto metódy sa suma vypočíta ako *množstvo* ×*cena*. Ďalšou podporovanou metódou je **Pevná cena**. Pri použití tohto spôsobu sa cena nastaví na sumu a množstvo sa pri výpočte nepoužije. | |
    | Plán jednotiek a jednotka | Plán jednotiek a jednotka spolu identifikujú jednotku množstva. | Kombinácia jednotky a kategórie transakcie sa používa na zadanie štandardných cien pre výdavky. V predvolenej konfigurácii Project Operations sa kombinácia jednotky, role a jednotky zdrojov používa na zadanie predvolených cien za čas. Ak máte vlastnú konfiguráciu na zadávanie predvolených cien, použije sa spolu s jednotkou. Kombinácia produktu a jednotky sa používa na zadanie predvolených cien materiálov. |
    | Množstvo | Zadajte množstvo. | |
    | Cena | Ak pri vytváraní riadku denníka ponecháte cenu prázdnu, na zadanie predvolených cien sa použijú príslušné hodnoty v závislosti od triedy transakcie. Ak je pri vytváraní riadku denníka zadaná cena, použije sa táto cena. | |
    | Daň | Zadajte ľubovoľnú sumu dane. | V závislosti od zadanej sumy dane sa rozšírená suma vypočíta ako *Suma* + *daň*. |

## <a name="confirm-an-entry-journal"></a>Potvrďte vstupný denník

Po zadaní všetkých riadkov denníka vo vstupnom denníku môžete denník potvrdiť. Tento proces zaznamená každý riadok denníka ako skutočné údaje o príslušných projektoch.

Po potvrdení denníka ho už nemôžete upravovať ani žiadny z jeho riadkov.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Skutočné hodnoty vytvorené potvrdením denníka zápisu

Existuje niekoľko kľúčových rozdielov medzi skutočnými hodnotami, ktoré sa vytvárajú potvrdením denníka zápisu, a skutočnými hodnotami, ktoré sa vytvárajú počas schvaľovania denníkov spotreby času, nákladov a materiálu a potvrdenia faktúr v rámci projektových operácií:

- Vstupné denníky nepoužívajú transakčné spojenia na prepojenie skutočných nákladov so skutočnými nevyfakturovanými predajmi. Skutočné údaje, ktoré sa vytvoria pri schválení protokolov spotreby času, nákladov a materiálu, vždy používajú transakčné pripojenia na prepojenie skutočných nákladov a nevyúčtovaných predajov.
- Vstupné denníky nepoužívajú počiatky transakcií na prepojenie skutočných nákladov a skutočných nevyfakturovaných tržieb s akýmkoľvek pôvodným záznamom. Skutočné hodnoty, ktoré sa vytvoria pri schvaľovaní denníkov spotreby času, nákladov a materiálu, vždy používajú pôvod transakcií na prepojenie skutočných nákladov a nevyfakturovaných predajov s pôvodným záznamom času.
- Keď sa fakturujú skutočné nevyfakturované tržby, ktoré sú vytvorené potvrdením Vstupného denníka, skutočné vyúčtované tržby, ktoré sa vytvoria počas potvrdenia faktúry, sú prepojené so skutočnými nevyfakturovanými predajmi, podobným spôsobom ako skutočné nevyfakturované tržby, ktoré sa vytvoria, keď čas, Výdavok a Záznamy o použití materiálu sú schválené.
- Riadky vstupného denníka, ktoré sú vytvorené pre čas, ktorý je zadaný medziorganizačnými zdrojmi, nespôsobujú skutočné hodnoty **Jednotkové náklady na zdroje** a **Predaj Interorg** typy, ktoré sa majú vytvárať automaticky. Tieto skutočné hodnoty musia byť vytvorené ručne. Toto správanie sa líši od správania pre časové položky, ktoré sú zaznamenané medziorganizačnými zdrojmi. V takom prípade, keď je čas schválený, aplikácia automaticky vytvorí aktuálne informácie **náklady** typ na projekte a skutočných **Jednotkové náklady na zdroje** a **Predaj Interorg** typy na oddelení, ktoré vlastní zamestnanec. Potom použije transakčné spojenia na prepojenie týchto skutočností a počiatkov transakcií na ich prepojenie s pôvodným časovým záznamom.
- Keď sú vstupné denníky potvrdené, vytvárajú aktuálne údaje. Opravné denníky však nemožno použiť na opravu týchto skutočností. Toto správanie sa líši od správania pre skutočné údaje, ktoré sa vytvárajú pri schvaľovaní protokolov o použití času, nákladov a materiálu. V takom prípade vám aplikácia umožňuje použiť denníky opráv na opravu skutočností, aby sa opravili prípadné chyby, za predpokladu, že tieto skutočnosti ešte neboli vyfakturované. Ak už boli vyfakturované, stále môžete opraviť skutočnú skutočnosť, ak spracujete celý kredit tejto skutočnosti zákazníkovi.

> [!NOTE]
> Vstupné denníky nevynucujú prísne predvolené pravidlá. Preto používajte tieto vstupné denníky čo najmenej a buďte opatrní a opatrní, aby ste sa uistili, že vo svojom systéme nevytvoríte poškodené finančné údaje. Vždy, keď je to možné, použite na vytváranie skutočných údajov denníky času, nákladov a použitia materiálu, nastavenie míľnikov a záloh na projektových zmluvách a proces potvrdenia faktúry za projekt namiesto denníkov.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
