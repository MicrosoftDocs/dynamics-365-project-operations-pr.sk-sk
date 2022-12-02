---
title: Vytvorenie a potvrdenie účtovných denníkov zadaní
description: Tento článok poskytuje informácie o tom, ako vytvoriť a potvrdiť Účtovné denníky vstupov v Microsoft Dynamics 365 Project Operations.
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

Účtovné denníky vstupov používate na zaznamenávanie skutočných údajov priamo v Microsoft Dynamics 365 Project Operations. Keď používate Účtovné denníky vstupov, nemusíte zadávať denníky času, výdavkov a použitia materiálu do Project Operations.

Jeden Účtovný denník vstupov vám umožňuje vytvoriť viacero záznamov v účtovnom denníku. Keď je záznam potvrdený, záznam v účtovnom denníku vstupov zaznamená skutočnú hodnotu pre nasledujúce podrobnosti:

- Náklady alebo výnosy v závislosti od zvoleného typu transakcie.
- Vybranú triedu transakcie. Dostupné triedy sú **Čas**, **Výdavok**, **Materiál**, **Preddavok**, **Míľnik** a **Daň**.
- Projekt a/alebo úloha, ktorá je vybratá v zázname v účtovnom denníku.

Ak chcete vytvoriť Účtovný denník vstupov v Project Operations, postupujte podľa týchto krokov.

1. Prejdite do **Predaj** \> **Transakcie** \> **Denníky**.
2. Na stránke so zoznamom **Účtovné denníky vstupov** vyberte na table Akcia **Nový** na vytvorenie denníka.
3. Na stránke **Nový denník** v poli **Popis** zadajte popis denníka.
4. Uistite sa, že pole **Typ denníka** je nastavené na **Vstup** a potom vyberte **Uložiť**. Po uložení nového Účtovného denníka vstupov by sa mala na stránke denníka zobraziť karta **Záznamy v účtovnom denníku**.
5. Na karte **Záznamy v účtovnom denníku** vyberte na paneli s nástrojmi nad mriežkou **Nový** na vytvorenie položky záznamu v účtovnom denníku vstupov.
6. V dialógovom okne **Rýchle vytvorenie** na vytvorenie položky záznamu v účtovnom denníku vstupov nastavte polia podľa popisu v nasledujúcej tabuľke.

    | Pole | Description | Funkčný vplyv |
    | --- | --- | --- |
    | Trieda transakcie | Záznam v účtovnom denníku možno klasifikovať do jednej zo šiestich tried transakcií: **Čas**, **Výdavok**, **Materiál**, **Záloha**, **Míľnik** alebo **Daň**. | Trieda transakcie **Daň** transakcií sa už v Project Operations nepoužíva. <br> Ak vytvoríte a triedu transakcie **Daň**, nebude spracovaná pri fakturácii ani vo výpočtoch nákladov alebo výnosov. **Míľnik** je triedou transakcie iba s výnosmi. <br>Trieda transakcie **Záloha** predstavuje preddavok, ktorý bol prijatý od zákazníka. Vždy by mal byť vytvorený ako pár záznamov v účtovnom denníku predaja a nevyfakturovaného predaja. |
    | Typ transakcie | Typy transakcií **Náklady**, **Predaj medzi organizáciami** a **Zdrojová jednotková cena** by sa mali používať na zaznamenávanie nákladov.<br> Typy transakcií **Nevyfakturovaný predaj** a **Fakturovaný predaj** by sa mali používať na zaznamenávanie výnosov. | Trieda transakcie **Záloha** funguje iba s typmi transakcií **Nevyfakturovaný predaj** a **Fakturovaný predaj**.<br> Trieda transakcie **Míľnik** funguje iba s typom transakcie **Fakturovaný predaj**. <br>Typy transakcií **Predaj medzi organizáciami** a **Zdrojová jednotková cena** sú použiteľné len pre triedu transakcií **Čas** a tieto sú dostupné len pre Denníky vstupov v scenári nasadenia Lite a nie pri nasadzovaní Project Operations v scenároch Zdroj/Neskladové materiály. |
    | Vyberte produkt | Keď je vybratá trieda transakcie **Materiál**, toto pole vám umožňuje určiť, či materiálová transakcia, pre ktorú vytvárate záznam v účtovnom denníku, je existujúci produkt alebo produkt nezahrnutý do katalógu. | Ak vyberiete **Produkt nezahrnutý do katalógu**, môžete zadať názov produktu. |
    | Produkt | Odkaz na produkt z katalógu. | |
    | Description | Popis záznamu v účtovnom denníku, ktorý uľahčuje jeho identifikáciu. | Pre záznamy v účtovnom denníku nevyfakturovaného predaja sa hodnota použije ako popis pri vytváraní podrobností riadku faktúry. |
    | Externý opis | Opis záznamu v účtovnom denníku, ktorý možno použiť na zdieľanie s externými účastníkmi projektu. | Pre záznamy v účtovnom denníku nevyfakturovaného predaja sa hodnota použije ako externý popis pri vytváraní podrobností riadku faktúry. Môže sa objaviť aj na faktúre, ktorá je zaslaná zákazníkovi. |
    | Typ fakturácie | Hodnota, ktorá označuje, či sa záznam v účtovnom denníku bude počítať ako spoplatnená, doplnková alebo neúčtovateľná súčasť projektu. | V typickom postupe je typ fakturácie odvodený od dohodnutých podmienok, ktoré sú nastavené v zmluve. Keď však zaznamenáte záznam v účtovnom denníku, môžete do tohto poľa zadať hodnotu. |
    | Dátum dokumentu | Použite dátum, kedy sa transakcia uskutočnila. | |
    | Počiatočný dátum | Použite dátum, kedy sa transakcia uskutočnila. | Toto pole sa používa na porovnanie s dátumom vytvorenia faktúry za transakcie typu **Nevyfakturovaný predaj**. Toto porovnanie vám pomôže rozhodnúť sa, či je transakcia s dátumom v budúcnosti alebo s dátumom v minulosti. Na faktúru budú pridané iba transakcie s dátumom v minulosti. |
    | Konečný dátum | Použite dátum, kedy sa transakcia uskutočnila. | |
    | Dátum účtovnej uzávierky | Použite dátum, kedy bude účtovný dopad zaznamenaný. | |
    | Zákazník v riadku zmluvy | Ak má riadok zmluvy iba jedného zákazníka, toto pole je štandardne nastavené na zákazníka v riadku zmluvy, keď sa záznam v účtovnom denníku uloží. Ak má riadok zmluvy viacerých zákazníkov, vyberte správneho zákazníka na riadku zmluvy. | Ak systém nedokáže určiť zákazníka v riadku zmluvy v zázname v účtovnom denníku a ak je prázdny v skutočnej hodnote typu **Nevyfakturovaný predaj**, ktorý je vytvorený zo záznamu v účtovnom denníku, skutočná hodnota nebude fakturovaná. |
    | Project | Vyberte projekt, do ktorého chcete zaznamenať skutočnú hodnotu. | Na základe zvoleného projektu, triedy transakcie a úlohy sa systém pokúsi určiť zmluvu, riadok zmluvy alebo zákazníka na riadku zmluvy. |
    | Úloha | Vyberte úlohu, do ktorej chcete zaznamenať skutočnú hodnotu. | Ak ste počas nastavovania zmluvy priradili úlohy k riadkom zmluvy, systém použije vybratú úlohu spolu s triedou projektu a transakcie na určenie zmluvy, riadku zmluvy a zákazníka na riadku zmluvy. |
    | Kategória transakcie | Vyberte kategóriu transakcie, do ktorej chcete zaznamenať skutočnú hodnotu. | Pre výdavky určuje vybratá kategória transakcie predvolenú cenu, ktorá sa zadá do záznamu v účtovnom denníku pri jeho uložení. |
    | Rola | Toto pole je relevantné pre časové záznamy v účtovnom denníku. Vyberte rolu zdroja, ktorý strávil čas na projekte a/alebo úlohe. | Ak pre časové záznamy v účtovnom denníku použijete prednastavenú konfiguráciu na zadanie predvolených nákladov na zdroje a sadzieb fakturácie, zvolená rola sa použije spolu s jednotkou zdrojov na určenie predvolenej ceny, ktorá sa zadá do záznamu v účtovnom denníku pri jeho uložení. Ak na zadávanie predvolených cien používate vlastnú konfiguráciu, mali by ste túto konfiguráciu skontrolovať a zistiť, či sa pole **Rola** používa na zadanie predvolených hodnôt cien. |
    | Subdodávateľská zmluva | Ak záznam v účtovnom denníku predstavuje subdodávateľskú kapacitu alebo subdodávateľské náklady alebo materiály, vyberte príslušnú subdodávku. | Keď sa zaznamenajú nákladové záznamy v účtovnom denníku, vybratá subdodávka určí cenník, ktorý sa použije na zadanie štandardných jednotkových nákladov. |
    | Riadok subdodávateľskej zmluvy | Ak záznam v účtovnom denníku predstavuje subdodávateľskú kapacitu alebo subdodávateľské náklady alebo materiály, vyberte príslušný riadok subdodávateľskej zmluvy. | Keď sa zaznamenajú nákladové riadky subdodávateľskej zmluvy, vybraný riadok subdodávateľskej zmluvy zabezpečí, že výpočty dostupnej kapacity na riadku subdodávateľskej zmluvy budú správne vypočítané. |
    | Metóda výpočtu sumy | Toto pole je nastavené štandardne na **Vynásobenie množstva cenou**. Pri použití tejto metódy sa suma vypočíta ako *Množstvo* × *Cena*. Ďalšou podporovanou metódou je **Pevná cena**. Pri použití tejto metódy sa cena nastaví na sumu a množstvo sa pri výpočte nepoužije. | |
    | Plán jednotky a Jednotka | Plán jednotky a jednotka spolu identifikujú jednotku množstva. | Kombinácia jednotky a kategórie transakcie sa používa na zadávanie predvolených cien pre výdavky. V predvolenej konfigurácii Project Operations sa kombinácia jednotky, roly a jednotky zdrojov používa na zadanie predvolených cien za čas. Ak máte vlastnú konfiguráciu na zadávanie predvolených cien, použije sa spolu s jednotkou. Kombinácia produktu a jednotky sa použije na zadávanie predvolených cien materiálov. |
    | Množstvo | Zadajte množstvo. | |
    | Cena | Ak pri vytváraní záznamu v účtovnom denníku ponecháte cenu prázdnu, príslušné hodnoty sa použijú na zadanie predvolených cien v závislosti od triedy transakcie. Ak je pri vytváraní záznamu v účtovnom denníku zadaná cena, použije sa táto cena. | |
    | Daň | Zadajte ľubovoľnú sumu dane. | V závislosti od zadanej sumy dane sa rozšírená suma vypočíta ako *Suma* + *Daň*. |

## <a name="confirm-an-entry-journal"></a>Potvrďte Účtovný denník vstupov

Po zadaní všetkých záznamov v účtovnom denníku v Účtovnom denníku vstupov môžete účtovný denník potvrdiť. Tento proces zaznamená každý záznam v účtovnom denníku ako skutočné údaje o príslušných projektoch.

Po potvrdení účtovného denníka ho už nemôžete upravovať ani upravovať žiadny z jeho riadkov.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Skutočné hodnoty vytvorené potvrdením Účtovného denníka vstupov

Existuje niekoľko kľúčových rozdielov medzi skutočnými hodnotami, ktoré sa vytvárajú potvrdením Účtovného denníka vstupov a skutočnými hodnotami, ktoré sa vytvárajú počas schvaľovania denníkov spotreby času, nákladov a materiálu a potvrdenia faktúr v rámci Project Operations:

- Účtovné denníky vstupov nepoužívajú transakčné spojenia na prepojenie skutočných nákladov so skutočnými nevyfakturovanými predajmi. Skutočné hodnoty, ktoré sa vytvoria pri schvaľovaní denníkov spotreby času, nákladov a materiálu, vždy používajú transakčné pripojenia na prepojenie skutočných nákladov a nevyúčtovaných predajov.
- Účtovné denníky vstupov nepoužívajú počiatky transakcii na prepojenie skutočných nákladov a skutočných skutočných nevyfakturovaných predajov s akýmkoľvek pôvodným záznamom. Skutočné hodnoty, ktoré sa vytvoria pri schvaľovaní denníkov spotreby času, nákladov a materiálu, vždy používajú počiatky transakcií na nákladov s skutočných nevyúčtovaných predajov s pôvodnou časovou položkou.
- Keď sa fakturujú skutočné nevyfakturované predaje, ktoré sú vytvorené potvrdením Účtovného denníka vstupov, skutočné vyfakturované predaje, ktoré sa vytvoria počas potvrdenia faktúry, sú prepojené so skutočnými nevyfakturovanými predajmi podobným spôsobom, ako skutočné nevyfakturované predaje, ktoré sa vytvoria pri schválení denníkov času, výdavkov a použitia materiálu.
- Záznamy v účtovnom denníku, ktoré sú vytvorené pre čas, ktorý je zadaný medziorganizačnými zdrojmi, nespôsobujú automatické vytvorenie skutočných hodnôt typov **Zdrojová jednotková cena** a **Predaj medzi organizáciami**. Tieto skutočné hodnoty musia byť vytvorené manuálne. Toto správanie sa líši od správania pre časové položky, ktoré sú zaznamenané medziorganizačnými zdrojmi. V takom prípade, keď je čas schválený, aplikácia automaticky vytvorí skutočné hodnoty typu **Náklady** v projekte a skutočné hodnoty typov **Zdrojová jednotková cena** a **Medziorganizačný predaj** na vlastnom oddelení zamestnanca. Potom použije transakčné spojenia na prepojenie týchto skutočných hodnôt a počiatkov transakcií na ich prepojenie s počiatočným časovým záznamom.
- Keď sú Účtovné denníky vstupov potvrdené, vytvárajú aktuálne hodnoty. Opravné účtovné denníky však nemožno použiť na opravu týchto skutočných hodnôt. Toto správanie sa líši od správania pre skutočné hodnoty, ktoré sa vytvárajú pri schvaľovaní denníkov používania času, nákladov a materiálu. V takom prípade vám aplikácia umožňuje použiť Opravné účtovné denníky na opravu skutočných hodnôt, aby sa opravili prípadné chyby, za predpokladu, že tieto skutočné hodnoty ešte neboli vyfakturované. Ak už boli vyfakturované, stále môžete opraviť skutočnú hodnotu, ak vystavíte úplný dobropis tejto skutočnej hodnoty zákazníkovi.

> [!NOTE]
> Účtovné denníky vstupov nevynucujú prísne predvolené pravidlá. Preto používajte tieto Účtové denníky vstupov čo najmenej a buďte opatrní, aby ste sa uistili, že vo svojom systéme nevytvoríte poškodené finančné údaje. Vždy, keď je to možné, použite na vytváranie skutočných hodnôt denníky času, nákladov a použitia materiálu, nastavenie míľnikov a záloh na projektových zmluvách a proces potvrdenia faktúry za projekt namiesto Účtovných denníkov vstupov.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
