---
title: Pridanie požadovaných vlastných polí do entít nastavenia cien a transakcií
description: Táto téma poskytuje informácie o tom, ako pridať požadované odkazy na vlastné pole do entít a do formulárov a zobrazení.
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
ms.openlocfilehash: 36c95913cc72e293c3015e1b9d3055aac476eebb4cf7d7993741d3cb61de0e13
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006186"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Pridanie požadovaných vlastných polí do entít nastavenia cien a transakcií

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma predpokladá, že ste dokončili postupy v téme [Vytvorenie vlastných polí a entít, ktoré sa budú používať ako cenové dimenzie](create-custom-fields-entities-pricing-dimensions.md). Ak ste tieto postupy nedokončili, vráťte sa späť a dokončite ich a potom sa vráťte na túto tému. 

V tejto téme vám postupy úkážu, ako pridať požadované vlastné pole odkazy na entity a prvky používateľského rozhrania (UI), ako sú formuláre a zobrazenia.

## <a name="add-custom-pricing-dimension-fields"></a>Pridať vlastné polia dimenzie ocenenia 
Po vytvorení vlastných polí a entít je ďalším krokom, aby sa cenové nastavenie a transakčné entity dozvedeli o všetkých vlastných entitách alebo množínách možností vytvorením referenčných polí. V závislosti od toho, či zoznam dimenzií cien obsahuje množinu možností, dimenzie alebo dimenzie entity alebo oboje, postupujte iba podľa krokov v **dimenziách vlastného oceňovania založeného na množine možností** alebo **Vlastné cenové dimenzie založené na entite**, resp. oboje.

### <a name="option-set-based-custom-pricing-dimensions"></a>Vlastné cenové dimenzie založené na množine možností
Ak je vlastná cenová dimenzia založená na množine možností, pridajte ju ako pole ku kľúčovým entitám. V nasledujúcom postupe sa používajú **pracovné miesto zdroja** a **pracovné hodiny zdroja** ako dimenzie oceňovania na základe množiny možností. Tieto sa musia najprv pridať ako polia do cenových entít **cena roly** a **prirážka k cene roly**.

1. V časti Project Operations vyberte **Nastavenia** > **Riešenia** a dvakrát kliknite na **Dimenzie cien \<your organization name>**. 
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity > cena roly**.
3. Rozbaľte entitu **cena roly** a zvoľte možnosť **Polia**.
4. Vyberte **Nové**, ak chcete vytvoriť nové pole s názvom **Pracovné miesto zdroja** a vyberte **Množina možností** ako typ poľa. 
5. Vyberte položku **Použiť existujúcu množinu možností**, vyberte množinu možností **Pracovné miesto zdroja** a potom vyberte **Uložiť**.
6. Opakujte kroky 1-5 na pridanie tohto poľa do entity **prirážka k cene roly**. 
7. Opakujte kroky 1-5 pre množinu možností **pracovné hodiny zdroja**.

> [!IMPORTANT]
> Keď pridáte pole do viacerých entít, použite rovnaký názov poľa vo všetkých entitách. 

> ![Pridanie miesta pracovného zdroja do ceny roly.](media/RWL-Field.png)

Vo fázach predaja a odhadovania projektu sú potrebné odhady pracovného úsilia na dokončenie **lokálnej** práce a práce **na mieste**, **pravidelné hodiny** a **nadčasové hodiny**  sa používajú na odhadnutie hodnoty cenovej ponuky/projektu. Polia **pracovného miesta zdroja** a **pracovné hodiny zdroja** sa pridajú k entitám odhadu, **detaily riadka cenovej ponuky**, **detaily riadka zmluvy**, **člen projektového tímu** a **riadok odhadu**.

1. V časti Project Operations vyberte **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**. 
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity > detail riadka cenovej ponuky**.
3. Rozbaľte entitu **detail riadka cenovej ponuky** a vyberte položku **polia**.
4. Vyberte **Nové**, ak chcete vytvoriť nové pole s názvom **Pracovné miesto zdroja** a vyberte typ poľa **Množina možností**. 
5. Vyberte položku **Použiť existujúcu množinu možností** a **Pracovné miesto zdroja** a potom vyberte **Uložiť**.
6. Opakujte kroky 1-5, ak chcete pridať toto pole do **detailov riadka projektovej zmluvy**, **člena projektového tímu** a entity **riadok odhadu**.
7. Opakujte kroky 1-6 pre množinu možností **pracovné hodiny zdroja**. 

> ![Pridanie miesta pracovného zdroja do riadka odhadu.](media/RWL-Default-Value.png)

Pre dodávku a fakturáciu, musí byť dokončená práca presne ocenená, aby sa dalo vybrať, či bola vykonaná **lokálne** alebo **na mieste**, a či bola dokončená počas **pravidelných hodín** alebo **nadčasu** na skutočné hodnoty projektu. Polia **miesto práce zdroja** a **pracovného času zdroja** by sa mali pridať do entít **časového záznamu**, **skutočných hodnôt**, **detailov riadku faktúry** a do **účtovného záznamu**.

1. Vyberte **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**.
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity > cena roly**.
3. Rozbaľte entitu **detail riadka cenovej ponuky** a vyberte položku **polia**.
4. Vyberte **Nové**, ak chcete vytvoriť nové pole s názvom **Pracovné miesto zdroja** a vyberte **Množina možností** ako typ poľa. 
5. Vyberte položku **Použiť existujúcu množinu možností**, vyberte množinu možností **Pracovné miesto zdroja** a potom vyberte **Uložiť**.
6. Opakujte kroky 1-5, ak chcete pridať toto pole do entít **skutočných údajov**, **detailov riadka faktúry** a **záznamov v účtovnom denníku**.
7. Opakujte kroky 1-6 pre množinu možností **pracovné hodiny zdroja**. 

> ![Pridanie miesta práce zdroja do záznamu času.](media/RWL-time-entry.png)

Tým sa dokončia zmeny schémy požadované pre vlastné dimenzie založené na množine možností.

## <a name="entity-based-custom-pricing-dimensions"></a>Vlastné cenové dimenzie založené na entite

Keď je entitou vlastná cenová dimenzia, pridáte vzťahy 1:N medzi entitou dimenzie a kľúčovými entitami. Pomocou štandardného nadpisu príklad zhora, je rozumné očakávať, že každý zamestnanec má priradený štandardný názov. SAs výsledok, budete potrebovať vzťah 1:N od štandardného titulu rezervovateľného zdroja alebo vzťah N:1, ak bol vytvorený z rezervovateľného zdroja na štandardný názov.

1. V časti Project Operations vyberte **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**. 
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity > štandardný názov**.
3. Rozbaľte entitu **štandardného titulu** a vyberte položku **1:N vzťahy**.
4. Vyberte **Nové**, ak chcete vytvoriť nový vzťah 1:N s názvom **Štandardný názov rezervovateľného zdroja**. Zadajte zostávajúce požadované informácie a následne vyberte **Uložiť**.

> ![Pridanie štandardného titulu ako referenčného poľa do Rezervovateľného zdroja.](media/ST-BR.png)

Štandardný názov bude tiež potrebné pridať do entít oceňovania **Cena roly** a **Prirážky k cene roly**. To je tiež dokončené pomocou 1:N vzťahov medzi entitami **štandardný názov** a **cena roly** a entitami **štandardný názov** a **prirážka k cene roly**.

1. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity > štandardný názov**.
2. Rozbaľte entitu **štandardného titulu** a vyberte položku **1:N vzťahy**.
3. Vyberte **Nové**, ak chcete vytvoriť nový vzťah 1:N s názvom **Štandardný názov ceny roly**. Zadajte zostávajúce požadované informácie a následne vyberte **Uložiť**.
4. Opakujte kroky 1-4 na vytvorenie vzťahov 1:N medzi entitami **štandardný názov** a **prirážka k cene roly**,

Vo fázach predaja a odhadu projektu, na ocenenie cenovej ponuky/projektu, sú odhady pracovného úsilia potrebné pre každý štandardný titul. To znamená, že sú potrebné vzťahy 1:N so štandardného názvu ku každej z týchto entít odhadu: 

- **Podrobnosti o riadku cenovej ponuky**
- **Podrobnosti o riadku projektovej zmluvy**
- **Člen projektového tímu**
- **Riadok odhadu**

5. Opakujte kroky 1-5, ak chcete vytvoriť vzťahy 1:N zo **štandardého titulu** do **detailu riadka cenovej ponuky**, **detailu riadka projektovej zmluvy**, **člena projektového tímu** a **riadka odhadu**.

> ![Pridanie štandardného titulu ako referenčného poľa do riadka odhadu.](media/ST-Estimate-Line.png)

  V fázach dodania a fakturácie musí byť práca dokončená každým štandardným titulom presne ocenená na skutočné hodnoty projektu. To znamená, že musia byť 1:N vzťahy od **štandardného titulu** po **čas vstupu**, **skutočné hodnoty**, **detail riadka faktúry** a **riadok entity účtovného denníka**.

6. Opakujte kroky 1 - 6 na vytvorenie 1:N vzťahov od **štandardného titulu** po **čas vstupu**, **skutočné hodnoty**, **detail riadka faktúry** a **riadok entity účtovného denníka**.

> ![Pridanie štandardného titulu ako referenčného poľa do časového záznamu.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Nastavenie predvolenej hodnoty dimenzie pomocou funkcií priradenia platformy
Pre časový záznam,by bolo užitočné mať systémom predvolený štandardný názov na časový záznam z Rezervovateľného zdroja, ktorý zaznamenáva časový záznam. Použite nasledovný postup na pridanie priraďovacích polí na vzťah 1:N z **Rezervovateľného zdroja** na **časový záznam**.

1. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity > štandardný názov**.
2. Rozbaľte entitu **štandardného titulu** a vyberte položku **1:N vzťahy**.
3. Dvakrát kliknite na položku **Rezervovateľný zdroj na časový záznam**. Na stránke **Vzťah** vyberte **Použiť párovanie polí**. 
4. Vyberte **Nové**, ak chcete vytvoriť nové párovanie polí medzi poľom **Štandardný názov** v entite **Rezervovateľný zdroj** a referenčným poľom **Štandardný názov** v entite **Časový záznam**. 

> ![Nastavenie priradenia polí na umožnenie predvolenia štandardného názvu z rezervovateľného zdroja na časový záznam.](media/ST-Mapping2.png)

Tým sa dokončia zmeny schémy požadované pre vlastné dimenzie založené na entite.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Pridajte vlastné polia do formulárov, zobrazení a obchodných pravidiel

Potom, čo ste vykonali všetky požadované zmeny schémy, ďalším krokom je, urobiť polia viditeľné v UI pridaním polí do formulárov a zobrazení.

1. Otvorte formulár alebo zobrazenie. Na pravom navigačnom paneli vyberte pole a presuňte ho na plátno formulára. 
2. Ak upravujete zobrazenie, použite pravú navigačnú tablu, vyberte **Pridať polia** a v dialógovom okne **Zoznam polí** vyberte polia, ktoré potrebujete, a vyberte **OK**.

Nasledujúca tabuľka je komplexný zoznam out-of-box formulárov a zobrazení, uvedených podľa entity, ktoré budú musieť byť aktualizované novými poľami. Ak máte vo vašich prispôsobeniach týchto entít ďalšie zobrazenia alebo formuláre, pridajte do nich aj nové polia.

| Entity        | Formuláre, ktoré potrebujú nové pole   |Zobrazenia, ktoré potrebujú nové pole      |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena roly|• Informácia |• Ceny kategórií aktívnych zdrojov<br> • Priradené zobrazenie cien kategórií zdrojov|
|  Prirážka k cene roly|Informácia|• Aktívna prirážka k cene roly<br>• Priradené zobrazenie prirážok k cenám rol|
|  Podrobnosti o riadku cenovej ponuky|• Informácie o projekte<br>• Rýchle vytvorenie projektu|• Podrobnosti o riadku aktívnej cenovej ponuky<br>• Kombinované podrobnosti o riadku cenovej ponuky<br>• Priradené zobrazenie podrobností o riadku cenovej ponuky|
|  Podrobnosti o riadku projektovej zmluvy|• Informácie o projekte<br>• Rýchle vytvorenie projektu|• Kombinované podrobnosti riadka zmluvy<br>• Aktívne podrobnosti o riadku zmluvy<br>• Priradené zobrazenie podrobností riadka zmluvy|
|  Člen projektového tímu|• Informácia<br>• Nový formulár|• Aktívni členovia projektového tímu<br>• Členovia projektového tímu<br>• Priradené zobrazenie členov projektového tímu|
|  Zadanie času|Informácia<br>• Vytvoriť zadanie času|• Moje zadania času podľa dátumu<br>• Moje zadania času na tento týždeň<br>• Zadania času na schválenie|
|  Záznam v účtovnom denníku|Informácia<br>• Rýchle vytvorenie|• Aktívne záznamy v účtovnom denníku<br>• Priradené zobrazenie záznamov v účtovnom denníku|
|  Podrobnosti o riadku faktúry|Informácia<br>• Rýchle vytvorenie|• Aktívne podrobnosti o riadku faktúry<br>• Fakturovateľné transakcie faktúr<br>• Bezplatné transakcie faktúr<br>• Priradené zobrazenie podrobností o riadku faktúry<br>• Nefakturovateľná transakcia faktúry|
|  Skutočná hodnota|• Informácia<br>• Aktívne skutočné hodnoty|• Priradené zobrazenie skutočných hodnôt|

Vlastné polia môže byť tiež potrebné pridať do obchodných pravidiel v závislosti na tom, čo ste definovali. Jeden out-of-box príklad je pre obchodné pravidlo **Editability časového záznamu na základe stavu.** Toto pravidlo definuje, ktoré polia je potrebné uzamknúť, keď je časový záznam v stave, ktorý nie je možné upravovať, ako je napríklad **schválený**. Pridajte polia do tohto obchodného pravidla tak, aby boli polia zamknuté pre úpravy, keď je časový záznam v stave inom ako **koncept** alebo **vrátený.**


[!INCLUDE[footer-include](../includes/footer-banner.md)]