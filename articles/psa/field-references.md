---
title: Pridanie vlastných polí do cenového nastavenia a transakčných entít
description: Táto téma poskytuje informácie o pridávaní vlastných polí k nastaveniu ceny a transakčných entít.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: af2256e77c3ceeee9638f57d971137df1658687b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148482"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a>Pridanie vlastných polí do cenového nastavenia a transakčných entít 

[!include [banner](../includes/psa-now-project-operations.md)]

Táto téma predpokladá, že ste dokončili postupy v téme, [vytvoriť vlastné polia a entity.](create-custom-fields-entities.md) Ak ste tieto postupy nedokončili, vráťte sa späť a dokončite ich a potom sa vráťte na túto tému. 

V tejto téme vám postupy úkážu, ako pridať požadované vlastné pole odkazy na entity a prvky používateľského rozhrania (UI), ako sú formuláre a zobrazenia.

## <a name="add-custom-pricing-dimension-fields"></a>Pridať vlastné polia dimenzie ocenenia 
Po vytvorení vlastných polí a entít je ďalším krokom, aby sa cenové nastavenie a transakčné entity dozvedeli o všetkých vlastných entitách alebo množínách možností vytvorením referenčných polí. V závislosti od toho, či zoznam dimenzií cien obsahuje množinu možností, dimenzie alebo dimenzie entity alebo oboje, postupujte iba podľa krokov v **dimenziách vlastného oceňovania založeného na množine možností** alebo **Vlastné cenové dimenzie založené na entite**, resp. oboje.

### <a name="option-set-based-custom-pricing-dimensions"></a>Vlastné cenové dimenzie založené na množine možností
Ak je vlastná cenová dimenzia založená na množine možností, pridajte ju ako pole ku kľúčovým entitám Project Service. V nasledujúcom postupe sa používajú **pracovné miesto zdroja** a **pracovné hodiny zdroja** ako dimenzie oceňovania na základe množiny možností. Tieto sa musia najprv pridať ako polia do cenových entít **cena roly** a **prirážka k cene roly**.

1. V aplikácii Project Service Automation (PSA) kliknite na **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **cenové dimenzie \<your organization name>**. 
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity > cena roly**.
3. Rozbaľte entitu **cena roly** a zvoľte možnosť **Polia**.
4. Kliknite na **nové**, ak chcete vytvoriť nové pole s názvom **pracovné miesto zdroja** s vyberte **množina možností** ako typ poľa. 
5. Vyberte položku **použiť existujúcu množinu možností**, vyberte množinu možností **pracovné miesto zdroja** a potom kliknite na tlačidlo **Uložiť**.
6. Opakujte kroky 1-5 na pridanie tohto poľa do entity **prirážka k cene roly**. 
7. Opakujte kroky 1-5 pre množinu možností **pracovné hodiny zdroja**.

> [!IMPORTANT]
> Keď pridáte pole do viacerých entít, použite rovnaký názov poľa vo všetkých entitách. 

> ![Pridanie miesta pracovného zdroja do ceny role](media/RWL-Field.png)

Vo fázach predaja a odhadovania projektu sú potrebné odhady pracovného úsilia na dokončenie **lokálnej** práce a práce **na mieste**, **pravidelné hodiny** a **nadčasové hodiny**  sa používajú na odhadnutie hodnoty cenovej ponuky/projektu. Polia **Pracovné miesto zdroja** a **Pracovná doba zdroja** sa pridajú k entitám odhadu, **Detaily riadka cenovej ponuky**, **Detaily riadka zmluvy**, **Projektová úloha**, **Člen projektového tímu** a **Riadok odhadu**.

1. V PSA kliknite na položku **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**. 
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity > detail riadka cenovej ponuky**.
3. Rozbaľte entitu **detail riadka cenovej ponuky** a vyberte položku **polia**.
4. Kliknite na **nové**, ak chcete vytvoriť nové pole s názvom **pracovné miesto zdroja** a vyberte **množina možností** ako typ poľa. 
5. Vyberte položku **použiť existujúcu množinu možností** a **pracovné miesto zdroja** a potom kliknite na tlačidlo **Uložiť**.
6. Opakujte kroky 1-5, ak chcete pridať toto pole do entít **Detaily riadka projektovej zmluvy**, **Projektová úloha**, **Člen projektového tímu** a **Riadok odhadu**.
7. Opakujte kroky 1-6 pre množinu možností **pracovné hodiny zdroja**. 

> ![Pridanie miesta pracovného zdroja do riadka odhadu](media/RWL-Default-Value.png)


Pre dodávku a fakturáciu, musí byť dokončená práca presne ocenená, aby sa dalo vybrať, či bola vykonaná **lokálne** alebo **na mieste**, a či bola dokončená počas **pravidelných hodín** alebo **nadčasu** na skutočné hodnoty projektu. Polia **miesto práce zdroja** a **pracovného času zdroja** by sa mali pridať do entít **časového záznamu**, **skutočných hodnôt**, **detailov riadku faktúry** a do **účtovného záznamu**.

1. V PSA kliknite na položku **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**.
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity > cena roly**.
3. Rozbaľte entitu **detail riadka cenovej ponuky** a vyberte položku **polia**.
4. Kliknite na **nové**, ak chcete vytvoriť nové pole s názvom **pracovné miesto zdroja** s vyberte **množina možností** ako typ poľa. 
5. Vyberte položku **použiť existujúcu množinu možností**, vyberte množinu možností **pracovné miesto zdroja** a potom kliknite na tlačidlo **Uložiť**.
6. Opakujte kroky 1-5, ak chcete pridať toto pole do entít **skutočných údajov**, **detailov riadka faktúry** a **záznamov v účtovnom denníku**.
7. Opakujte kroky 1-6 pre množinu možností **pracovné hodiny zdroja**. 

> ![Pridanie miesta práce zdroja do záznamu času](media/RWL-time-entry.png)

Tým sa dokončia zmeny schémy požadované pre vlastné dimenzie založené na množine možností.

## <a name="entity-based-custom-pricing-dimensions"></a>Vlastné cenové dimenzie založené na entite

Keď je entitou vlastná cenová dimenzia, pridáte vzťahy 1:N medzi entitou dimenzia a kľúčovými entitami Project Service. Pomocou štandardného nadpisu príklad zhora, je rozumné očakávať, že každý zamestnanec má priradený štandardný názov. SAs výsledok, budete potrebovať vzťah 1:N od štandardného titulu rezervovateľného zdroja alebo vzťah N:1, ak bol vytvorený z rezervovateľného zdroja na štandardný názov.

1. V PSA kliknite na položku **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**. 
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity > štandardný názov**.
3. Rozbaľte entitu **štandardného titulu** a vyberte položku **1:N vzťahy**.
4. Kliknite na **nové** ak chcete vytvoriť nový vzťah 1:N s názvom **štandardný názov rezervovateľného prostriedku**. Zadajte zostávajúce požadované informácie a kliknite na **Uložiť**.

> ![Pridanie štandardného titulu ako referenčného poľa do Rezervovateľného prostriedku](media/ST-BR.png)

Štandardný názov bude tiež potrebné pridať do entít oceňovania Project Service **ceny role** a **prirážky ceny role**. To je tiež dokončené pomocou 1:N vzťahov medzi entitami **štandardný názov** a **cena roly** a entitami **štandardný názov** a **prirážka k cene roly**.

1. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity > štandardný názov**.
2. Rozbaľte entitu **štandardného titulu** a vyberte položku **1:N vzťahy**.
3. Kliknite na **nové** ak chcete vytvoriť nový vzťah 1:N s názvom **štandardný názov ceny role**. Zadajte zostávajúce požadované informácie a kliknite na **Uložiť**.
4. Opakujte kroky 1-4 na vytvorenie vzťahov 1:N medzi entitami **štandardný názov** a **prirážka k cene roly**,

Vo fázach predaja a odhadu projektu, na ocenenie cenovej ponuky/projektu, sú odhady pracovného úsilia potrebné pre každý štandardný titul. To znamená, že sú potrebné vzťahy 1:N od štandardného titulu ku každej z týchto entít odhadu v Project Service: 

- **Podrobnosti o riadku cenovej ponuky**
- **Podrobnosti o riadku projektovej zmluvy**
- **Projektová úloha**
- **Člen projektového tímu**
- **Riadok odhadu**

5. Opakujte kroky 1-5, ak chcete vytvoriť vzťahy 1:N zo **štandardého titulu** do **detailu riadka cenovej ponuky**, **detailu riadka projektovej zmluvy**, **projektovej úlohy**, **člena projektového tímu** a **riadka odhadu**.

> ![Pridanie štandardného titulu ako referenčného poľa do riadka odhadu](media/ST-Estimate-Line.png)

V fázach dodania a fakturácie musí byť práca dokončená každým štandardným titulom presne ocenená na skutočné hodnoty projektu. To znamená, že musia byť 1:N vzťahy od **štandardného titulu** po **čas vstupu**, **skutočné hodnoty**, **detail riadka faktúry** a **riadok entity účtovného denníka**.

6. Opakujte kroky 1 - 6 na vytvorenie 1:N vzťahov od **štandardného titulu** po **čas vstupu**, **skutočné hodnoty**, **detail riadka faktúry** a **riadok entity účtovného denníka**.

> ![Pridanie štandardného titulu ako referenčného poľa do časového záznamu](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Nastavenie predvolenej hodnoty dimenzie pomocou funkcií priradenia platformy
Pre časový záznam,by bolo užitočné mať systémom predvolený štandardný názov na časový záznam z Rezervovateľného zdroja, ktorý zaznamenáva časový záznam. Použite nasledovný postup na pridanie priraďovacích polí na vzťah 1:N z **Rezervovateľného zdroja** na **časový záznam**.

1. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity > štandardný názov**.
2. Rozbaľte entitu **štandardného titulu** a vyberte položku **1:N vzťahy**.
3. Dvakrát kliknite na položku **Rezervovateľný zdroj na časový záznam**. Na stránke **vzťah** kliknite na položku **použiť priradenia polí**. 
4. Kliknite na **nové**, ak chcete vytvoriť nové priraďovanie polí medzi poľom **štandardný názov** v entite **rezervovateľného prostriedku** na pole odkazu **štandardný názov** v entite **časový záznam**. 

> ![Nastavenie priradenia polí na umožnenie predvolenia štandardného názvu z rezervovateľného zdroja na časový záznam](media/ST-Mapping2.png)


Tým sa dokončia zmeny schémy požadované pre vlastné dimenzie založené na entite.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Pridajte vlastné polia do formulárov, zobrazení a obchodných pravidiel

Potom, čo ste vykonali všetky požadované zmeny schémy, ďalším krokom je, urobiť polia viditeľné v UI pridaním polí do formulárov a zobrazení.

1. Otvorte formulár alebo zobrazenie. Na pravom navigačnom paneli vyberte pole a presuňte ho na plátno formulára. 
2. Ak upravujete zobrazenie, použite pravý navigačný panel, kliknite na položku **pridať polia** a v dialógovom okne **zoznam polí** vyberte polia, ktoré potrebujete, a kliknite na **OK**.

Nasledujúca tabuľka je komplexný zoznam out-of-box formulárov a zobrazení, uvedených podľa entity, ktoré budú musieť byť aktualizované novými poľami. Ak máte vo vašich prispôsobeniach týchto entít ďalšie zobrazenia alebo formuláre, pridajte do nich aj nové polia.

| Entita Project Service        | Formuláre, ktoré potrebujú nové pole   |Zobrazenia, ktoré potrebujú nové pole      |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena roly|• Informácia |• Ceny kategórií aktívnych zdrojov<br> • Priradené zobrazenie cien kategórií zdrojov|
|  Prirážka k cene roly|Informácia|• Aktívna prirážka k cene roly<br>• Priradené zobrazenie prirážok k cenám rol|
|  Podrobnosti o riadku cenovej ponuky|• Informácie o projekte<br>• Rýchle vytvorenie projektu|• Podrobnosti o riadku aktívnej cenovej ponuky<br>• Kombinované podrobnosti o riadku cenovej ponuky<br>• Priradené zobrazenie podrobností o riadku cenovej ponuky|
|  Podrobnosti o riadku projektovej zmluvy|• Informácie o projekte<br>• Rýchle vytvorenie projektu|• Kombinované podrobnosti riadka zmluvy<br>• Aktívne podrobnosti o riadku zmluvy<br>• Priradené zobrazenie podrobností riadka zmluvy|
|  Projektová úloha|Informácia<br>• Nový formulár||
|  Člen projektového tímu|Informácia<br>• Nový formulár|• Aktívni členovia projektového tímu<br>• Členovia projektového tímu<br>• Priradené zobrazenie členov projektového tímu|
|  Zadanie času|Informácia<br>• Vytvoriť zadanie času|• Moje zadania času podľa dátumu<br>• Moje zadania času na tento týždeň<br>• Zadania času na schválenie|
|  Záznam v účtovnom denníku|Informácia<br>• Rýchle vytvorenie|• Aktívne záznamy v účtovnom denníku<br>• Priradené zobrazenie záznamov v účtovnom denníku|
|  Podrobnosti o riadku faktúry|Informácia<br>• Rýchle vytvorenie|• Aktívne podrobnosti o riadku faktúry<br>• Fakturovateľné transakcie faktúr<br>• Bezplatné transakcie faktúr<br>• Priradené zobrazenie podrobností o riadku faktúry<br>• Nefakturovateľná transakcia faktúry|
|  Skutočná hodnota|• Informácia<br>• Aktívne skutočné hodnoty|• Priradené zobrazenie skutočných hodnôt|

Vlastné polia môže byť tiež potrebné pridať do obchodných pravidiel v závislosti na tom, čo ste definovali. Jeden out-of-box príklad je pre obchodné pravidlo **Editability časového záznamu na základe stavu.** Toto pravidlo definuje, ktoré polia je potrebné uzamknúť, keď je časový záznam v stave, ktorý nie je možné upravovať, ako je napríklad **schválený**. Pridajte polia do tohto obchodného pravidla tak, aby boli polia zamknuté pre úpravy, keď je časový záznam v stave inom ako **koncept** alebo **vrátený.**


[!INCLUDE[footer-include](../includes/footer-banner.md)]