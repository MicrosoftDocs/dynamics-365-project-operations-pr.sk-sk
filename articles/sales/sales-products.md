---
title: Produkty
description: Táto téma obsahuje informácie o katalógu produktov, ktorý môžete použiť na poskytovanie informácií zákazníkom o produktoch a cenách, ktoré ponúka vaša organizácia.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 085b7e4d9274f8c8d94d7a84109cfa782acf3dbb9241bfd25ecb8c2f329e1bb8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986870"
---
# <a name="products"></a>Produkty

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Výrobky sú základom vášho podnikania. Katalóg produktov v Dynamics 365 Sales Professional je zbierka produktov a informácií o ich cenách. Uľahčite obchodným zástupcom rýchle zvýšenie predaja vytvorením katalógu produktov.

## <a name="add-a-product"></a>Pridanie produktu

1.  Uistite sa, že máte funkciu Sales Manager Professional alebo System Administrator, aby ste mohli pridávať produkty do systému Dynamics 365 Sales Professional.
2.  V mape lokality v časti **Nastavenie** stlačte možnosť **Produkty**.
3.  Vyberte **Pridať produkt** a vyplňte nasledujúce informácie:

    -  **Názov**
    -  **Kód Product ID**
    -  **Nadradený**: Zvoľte si nadradený rad pre produkt. Ak vytvárate podradený produkt v rade produktov, názov nadradeného radu produktov sa vyplní sem. Túto možnosť nemožno zmeniť po uložení záznamu.
    -  **Platné od**/**Platné do**: Definujte obdobie, počas ktorého bude produkt platný po výbere dátumu **Platné od** a **Platné do**.
    -  **Jednotková skupina**: vyberte skupinu jednotiek. Jednotková skupina je zbierka rôznych jednotiek, v ktorých sa produkt predáva, a určuje spôsob zoskupovania jednotlivých položiek do väčších množstiev. Ak napríklad pridávate semená ako produkt, môžete vytvoriť skupinu jednotiek s názvom „Semená” a definovať jeho primárnu jednotku ako „balík”.
    -  **Predvolená jednotka**: Vyberte najbežnejšiu jednotku, v ktorej sa bude produkt predávať. Jednotky predstavujú množstvá alebo hodnoty, v ktorých sa produkty predávajú. Ak napríklad pridávate ako produkt semená, môžete ich predávať po balíčkoch, krabiciach či paletách. Každý z nich sa stáva jednotky produktu. Ak semená sú väčšinou predávajú v balení, vyberte to ako jednotku.
    -  **Predvolený cenník**: Ak ide o nový produkt, toto pole je len na čítanie. Pred výberom predvoleného cenníka musíte vyplniť všetky povinné polia a potom uložiť záznam. Hoci sa nevyžaduje predvolený cenník, po uložení záznamu produktu je rozumné nastaviť predvolený cenník pre každý produkt. Ak záznam zákazníka neobsahuje cenník, Sales tak bude môcť pomocou predvoleného cenníka vytvárať ponuky, objednávky a faktúry.
    -  **Počet desatinných miest**: Zadajte celé číslo medzi 0 a 5. Ak produkt nie je možné rozdeliť na čiastkové množstvá, zadajte hodnotu 0. Presnosť poľa **Množstvo** v cenovej ponuke, objednávke alebo zázname produktu faktúry sa overí porovnaním s hodnotou v tomto poli v prípade, že produkt nemá priradený cenník.
    -  **Subjekt**: Priradí tento produkt môžete k subjektu. Subjekty môžete použiť na kategorizáciu produktov a filtrovanie zostáv.

4.  Vyberte položku **Uložiť**.
5.  Na karte **Ďalšie podrobnosti** v sekcii **Položky cenníka** vyberte položku **Ďalšie príkazy** a potom vyberte **Pridať novú položku cenníka**.
7.  Na karte **Ďalšie podrobnosti** v časti **Vzťah produktu** vyberte ikonu **Ďalšie príkazy** a potom vyberte **Pridať nový vzťah produktu**.
8.  Vo formulári **Nový vzťah produktu** zadajte nasledovné podrobnosti a na paneli príkazov stlačte možnosť **Uložiť a zavrieť**:

    -   **Súvisiaci produkt**: Vyberte produkt, ktorý chcete pridať ako súvisiaci produkt do existujúce záznamu produktu, na ktorom pracujete.
    -   **Typ vzťahu predaja**: Vyberte, či chcete pridať produkt ako up-sell, cross-sell, príslušenstvo, alebo náhradný produkt.
    -   **Smer**: Vyberte, či vzťah medzi výrobkami bude jednosmerný alebo obojsmerný. Keď vyberiete jednosmerný, produkt, ktorý ste vybrali v **Súvisiacom produkte** sa zobrazí ako odporúčanie pre existujúci produkt, ale nie naopak.

9.  Na formulári Produkt vyberte položku **Uložiť**.

## <a name="import-products"></a>Importovať produkty

Môžete použiť šablóny importu na privedenie hromadných údajov o produkte do Dynamics 365 Sales.

## <a name="revise-a-product"></a>Skontrolovať produkt

Majte inventár produktov aktualizovaný podľa potreby rýchlou kontrolou, a publikovaním informácií tak, že váš obchodní zástupcovia môžete vidieť posledné zmeny v inventári produktov.

1.  Skontrolujte, či máte jednu z nasledujúcich rol zabezpečenia alebo rovnocenné povolenia: správca systému, prispôsobovač systému, obchodný manažér, viceprezident pre predaj, viceprezident pre marketing alebo generálny riaditeľ.
2.  Na mape lokality vyberte **Produkty**.
3.  Otvorte aktívny produkt, ktorý chcete zmeniť, a na paneli príkazov kliknite na možnosť **Revidovať**.
4.  V dialógovom okne **Potvrdiť revidovanie** vyberte možnosť **Potvrdiť**. To zmení stav výrobku do **V rámci revízie**.
5.  Po vykonaní zmien na paneli s príkazmi vyberte položku **Publikovať**.

    > [!TIP]
    > Ak chcete vrátiť zmeny a pokračovať s poslednou aktívnou verziou produktu, vyberte položku **Vrátiť**. Tieto zmeny stavu výrobok vrátia produkt späť do stavu **Aktívny**.

## <a name="clone-a-product"></a>Klonovanie produktu 

Keď vytvárate nový produkt, ušetrite čas klonovaním existujúceho. Tým sa vytvorí kópia pôvodného záznamu so všetkými detailmi okrem názvu a identifikátora.

1.  Skontrolujte, či máte jednu z nasledujúcich rol zabezpečenia alebo rovnocenné povolenia: správca systému, prispôsobovač systému, obchodný manažér, viceprezident pre predaj, viceprezident pre marketing alebo generálny riaditeľ.
2.  Na mape lokality vyberte **Produkty**.
3.  Vyberte záznam skupiny produktov, produktu alebo balíka, ktorý chcete klonovať, a v príkazovom riadku kliknite na možnosť **Klonovať**. Zobrazí sa dialógové okno s potvrdením.
4.  Vyberte položku **Potvrdiť**.

Nový produkt záznamu sa otvorí s rovnakými detailmi ako ten pôvodný, okrem názvu a identifikátora.

## <a name="retire-a-product"></a>Vyradenie produktu 

Ak vaša organizácia už výrobok nepredáva, vyraďte ho tak, aby výrobok už nebol dostupný pre vašich obchodných zástupcov.

1.  Skontrolujte, či máte rolu zabezpečenia na úrovni správcu systému alebo manažéra Sales Professional alebo rovnocenné povolenia.
2.  Na mape lokality vyberte **Produkty**.
3.  Otvorte aktívny produkt, ktorý chcete vyradiť, a na paneli príkazov kliknite na možnosť **Vyradiť**.
4.  V dialógovom okne **Potvrdenie vyradenia** vyberte možnosť **Potvrdiť**.


## <a name="delete-a-product"></a>Odstránenie produktu

Na zastavenie predaja výrobku ho odstráňte.

> [!IMPORTANT]
> Odstránený záznam nemožno obnoviť.

1.  Skontrolujte, či máte rolu zabezpečenia na úrovni správcu systému alebo manažéra Sales Professional alebo rovnocenné povolenia.
2.  Na mape lokality vyberte **Produkty**.
3.  Vyberte záznam skupiny produktov, produktu alebo balíka, ktorý chcete odstrániť, a v príkazovom riadku kliknite na možnosť **Odstrániť**.
4.  V dialógovom okne **Potvrdenie odstránenia** vyberte možnosť **Pokračovať**.
 
 ## <a name="quantity-factors-for-products"></a>Množstvo faktorov pre výrobky

Faktorov kvantity podporujú predaj produktov založených na predplatnom. V prípade produktov založených na predplatnom sa množstvo v riadku cenovej ponuky alebo projektu vyjadrí ako počet používateľských mesiacov.

Zvyčajne je cena predplatného softvéru uložená v katalógu ako cena za používateľa mesačne. Avšak, môžete použiť iné časové popisy. Počas predajného procesu je cena v riadku cenovej ponuky zvyčajne cena za používateľa, za mesiac, ktorá bola dohodnutá a zľavnená agentom predaja IT. Každý obchod má iný počet užívateľov a iný počet predplatných mesiacov. Množstvo, ktoré sa používa na výpočet čiastky riadka cenovej ponuky, je produktom počtu používateľov a počtu mesiacov predplatného.

Faktory kvantity sa spoliehajú na atribúty produktov. Keď nakonfigurujete špecifické vlastnosti produktu, môžete označiť podmnožinu týchto vlastností alebo všetky vlastnosti ako faktory kvantity.

Systém overuje, že iba číselné vlastnosti alebo vlastnosti produktu, ktoré majú číselný typ údajov, sú označené ako faktory kvantity. Ak je produkt, na ktorý sú nakonfigurované množstevné faktory, pridaný do riadka cenovej ponuky, pole **množstvo** v riadku cenovej ponuky sa stáva poľom iba na čítanie. Po zadaní hodnôt pre vlastnosti produktu, ktoré sú faktory kvantity, sa vypočíta množstvo riadka cenovej ponuky.

Napríklad ak existujú nasledujúce vlastnosti: 

- **Počet používateľov**: Počet používateľov 
- **Počet mesiacov**: Počet mesiacov predplatného
- **Produkt SKU** 

Vlastnosti **Počet používateľov** a **Počet mesiacov** môžu byť označené ako faktory kvantity úpravou vlastnosti produktového riadku. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]