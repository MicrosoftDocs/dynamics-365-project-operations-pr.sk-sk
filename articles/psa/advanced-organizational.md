---
title: Organizačné jednotky
description: Táto téma poskytuje informácie o organizačných jednotkách v Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 755eee6ab9993c72ff1db46e0993527ac0826bfe
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130642"
---
# <a name="organizational-units"></a>Organizačné jednotky 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, organizačná jednotka je odlišná skupina alebo divízia v profesionálnej spoločnosti služieb, ktorá zamestnáva fakturovateľné zdroje, ktoré majú nákladové zdroje.

V spoločnostiach profesionálnych služieb, ktoré zamestnávajú technické zdroje v rôznych praktických oblastiach alebo obchodných tratiach, náklady na vyplnenie úlohy v jednej praxi alebo obchodnej línii sa môžu líšiť od nákladov na vyplnenie úlohy v inej praxi alebo obchodnej linke. Koncept organizačné jednotky pomáha v tomto scenári tým, že poskytuje spôsob, ako zoskupiť súbor fakturovateľné role v divízii spoločnosti, ktorá má odlišnú štruktúru nákladov pre tieto roly.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Kľúčové atribúty a asociácie organizačných jednotiek

V PSA, má organizačná jednotka v PSA špecifickú menu a špecifické cenníky obstarávacích cien.

Menou organizačnej jednotky je primárna mena, ktorá sa používa na sledovanie nákladov.

Na každú organizačnú jednotku je možné priložiť jeden alebo viacero cenníkov obstarávacích cien. PSA kladie nasledujúce obmedzenia na cenníky, ktoré môžu byť pripojené k organizačnej jednotke:

- Cenníky musia byť v mene organizačnej jednotky
- Cenníky musia byť v cenníkoch obstarávacích cien

Okrem toho existuje atribút organizačnej jednotky zdrojovej entity. Každý zdroj môže byť priradený k jednej organizačnej jednotke.

## <a name="roles-of-organizational-units"></a>Roly organizačných jednotiek

Organizačná jednotka hrá dve roly v PSA:

- **Contracting unit** – Organizačná jednotka, ktorá zastupuje skupinu spoločností alebo divízie, ktorá je primárne zodpovedná za získanie predaja a riadenie poskytovania práce a služieb zákazníkovi. Zmluvná jednotka je definovaná poľom **Contracting Unit** v sekcii hlavičky na stránkach **Opportunity**, **Quote**, **Project Contract** a **Project**.
- **Resourcing unit** – Organizačná jednotka, ku ktorej zdroj patrí alebo je priradený. Táto organizačná jednotka môže poskytnúť svoje zdroje pre niektoré roly na výkazy práce (SOWs) a projekty, ktoré sú vo vlastníctve zmluvnej jednotky.

> ![Zmluvné jednotky a zdrojové jednotky](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Organizačná jednotka FAQs

Tu sú uvedené odpovede na niekoľko z najčastejších otázok o organizačných jednotkách.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Ako súvisí Organizačná Jednotka entity v PSA s Organizačnou entitou, ktorá už existuje v Dynamics 365?

Organizačná entita v Microsoft Dynamics 365 predstavuje názov globálnej inštancie Dynamics 365. Tento názov je zvyčajne názov globálneho podniku.

Entita organizačnej jednotky reprezentuje skupinu alebo divíziu v globálnom podniku. Táto skupina alebo divízia má množinu rolí a cenník nákladov pre tieto roly a tieto roly a cenník sa odlišujú od rolí a cenníka iných skupín alebo divízií v podniku.

Keď je nainštalovaný PSA, predvolená organizačná jednotka je vytvorená na základe organizácie. Všetky existujúce prostriedky sú priradené k predvolenej organizačnej jednotke. Ak sa importujú nejakí noví používatelia alebo zdroje Active Directory do Dynamics 365, proces importu používateľa ich priradí predvolenej organizačnej jednotke v PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Ako sa entita organizačnej jednotky odlišuje od entity obchodnej jednotky?

V Dynamics 365, entita Obchodnej Jednotky je zabezpečená konštrukcia. Priradenie používateľa k účtovnej jednotke určuje entity a záznamy entity, ku ktorým má používateľ prístup. Určuje tiež povolenia (Create, Read, Write, Delete, Append, Append To, Assign alebo Share), ktoré má používateľ pre tieto záznamy entity.

Entita Organizačnej jednotky predstavuje skupinu spoločností alebo divízie, ktorá má odlišné nákladové sadzby pre zamestnancov, ktorým sú priradené. Priradenie prostriedku k organizačnej jednotke určuje zdrojové náklady na angažovanosť projektu.

Keď implementujete Dynamics 365, optimalizujte povolenia zabezpečenia pre hierarchiu obchodných jednotiek a priraďovanie používateľov k obchodným jednotkám. Priraďte všetkých používateľov, ktorí musia zvyčajne pristupovať k rovnakej množine záznamov na rovnakú obchodnú jednotku. Organizačná jednotka nemá žiadny vplyv na bezpečnostné oprávnenie alebo prístup.

#### <a name="example-of-organizational-units-and-business-units"></a>Príklad organizačných jednotiek a obchodných jednotiek

Blaho, Ltd. má prosperujúce technologické postupy spoločnosti Microsoft. Erik a Viktória sú obaja C\# vývojári, ale Viktória je v Spojených štátoch, zatiaľ čo Erik je v Indii. Väčšina projektových záväzkov si vyžaduje zdroje od spoločnosti Blaho India a Blaho USA a Erik a Viktória si vyžadujú rovnakú úroveň prístupu k zabezpečeniu k projektom v tejto praktickej oblasti. Avšak, náklady na vývojárov z Blaho India sa výrazne líšia od nákladov na vývojárov z Blaho USA.

Tu je optimálny spôsob, ako navrhnúť pre tento scenár pomocou Dynamics 365 a PSA.

1. Vytvorte technologickú prax spoločnosti Microsoft ako obchodnú jednotku a priraďte ju spoločnosti Erik a Viktória. Týmto spôsobom môžete pomôcť zaručiť, že obaja zamestnanci majú rovnakú úroveň prístupu k zabezpečeniu k akýmkoľvek projektom v tejto oblasti praxe. Obaja budú môcť kontrolovať priebeh a hlásiť čas, výdavky a aktualizácie úloh. 
2. Vytvoriť dve organizačné jednotky, aby Hel zaručil, že náklady na projekt sú správne odrazené. 
3. Pridružiť Viktória s Blaho USA a pridružiť Erik s Blaho India.
4. Priraďte príslušné zoznamy nákladových cenníkov obom organizačným jednotkám. TIn týmto spôsobom, môžete pomôcť zaručiť, že náklady, ktoré sú zaznamenané na projekte pre Erik a Viktória presne odrážajú rozdiel v nákladoch medzi Blaho USA a Blaho India.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Sú organizačné jednotky súvisiace s predajnými územiami v Dynamics 365?

Neexistuje žiadne združenie alebo vzťah medzi oblasťami predaja a organizačnými jednotkami. Územie predaja je zvyčajne zemepisnou oblasťou, kde dochádza k predaju. Cenník nákladov môže byť priradený k jednotlivým oblastiam predaja.

Organizačná jednotka je interná skupina alebo divízia v spoločnosti, ktorá sleduje náklady na množinu rolí, ktoré predáva iným divíziám alebo externým zákazníkom.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Príklad organizačných jednotiek a oblastí predaja

Blaho, Ltd. má dve vývojové centrá: Blaho USA a Blaho India. Náklady na zdroje sa výrazne líšia medzi týmito dvoma rozvojovými centrami.

Blaho predáva svoje IT služby na mnohých medzinárodných trhoch, ako sú Latinská Amerika, Severná Amerika, Ázia-Tichomorie, Západná Európa a Stredný Východ. Fakturačné sadzby pre rovnaké projektové role sa môžu značne líšiť v týchto trhoch.

Blaho USA a Blaho India by mali byť nastavené ako organizačné jednotky a každá organizačná jednotka by mala mať svoj vlastný cenník nákladov. Ázia-Tichomorie, Latinská Amerika, Severná Amerika, Západná Európa a Stredný Východ by mali byť stanovené ako oblasti predaja a každá oblasť predaja by mala mať svoj vlastný predajný cenník.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Prečo existuje obmedzenie asociácie cenníkov s organizačnými jednotkami? 

Predajné ceny sú zvyčajne jedinečné pre geografické oblasti alebo trhy, kde sa služby predávajú. Interné divízie spoločnosti nemajú zvyčajne svoje vlastné predajné ceny pre rovnaký typ služieb. Avšak, vnútorné divízie majú rôzne náklady na predaný tovar (COGS), v závislosti na zručnostiach ľudí, ktorých zamestnávajú a pracovné podmienky v regióne, kde pôsobia. Keďže organizačné jednotky sú modelované ako interné divízie spoločnosti, môžu mať len cenníky nákladov.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Prečo nemôžeme priradiť zoznamy predajných cenníkov k organizačným jednotkám?

V PSA môžu byť zoznamy predajných cien spojené so zákazníkmi a predajnými územiami. Transakčné entity, ako je Opportunity, Quote, Project Contract, a Project používajú predajné cenníky, ktoré sú pripojené ku kontu zákazníka alebo k oblasti predaja na určenie sadzieb fakturovania a potenciálnych výnosov na projekte Engagement.

Cenníky nákladov sú priradené k organizačným jednotkám. Transakčné entity ako Opportunity, Quote, Project Contract a Project používajú cenníky nákladov, ktoré sú pripojené k obstarávacej jednotke na určenie nákladov na zapojenie projektu.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Sú organizačné jednotky hierarchické v PSA?

Nie. V súčasnom vydaní PSA, organizačné jednotky nie sú hierarchické. To znamená, že nemôžete:

- Nakonfigurujte vzor pre ceny nákladov, ktoré zlyhajú, ktoré prechádzajú hierarchiou. 
- Nahláste výnosy alebo náklady na rôznych úrovniach hierarchie organizačnej jednotky.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Sme veľká nadnárodná firma s komplexnou, viacúrovňovou hierarchiou nákladových centier, divízií a fakturačných kancelárií. Ako môžeme čo najlepšie využiť koncept organizačnej jednotky v tejto verzii aplikácie Project Service?

Ak máte komplexnú hierarchiu nákladových centier, divízií, fakturačných kancelárií atď., nastavte listové uzly hierarchie ako odlišné organizačné jednotky.
Nasledujúci príklad znázorňuje typickú hierarchiu:

**Blaho India**

  - SAP Prax 

    - Technické poradenstvo 
    - Funkčné poradenstvo 
    
  - Prax spoločnosti Microsoft Technology 

    - Technické poradenstvo
    - Funkčné poradenstvo 
    
**Contoso US**

 - SAP Prax 

    - Technické poradenstvo 
    - Funkčné poradenstvo 
    
 - Prax spoločnosti Microsoft Technology 

    - Technické poradenstvo 
    - Funkčné poradenstvo 
 
Ak je vaša hierarchia podobná, musíte ju nastaviť ako plochý zoznam, ako je to znázornené tu:
- Blaho India - SAP Practice - Technical Consultants 
- Blaho India - SAP Practice - Functional Consultants       
- Blaho India - Microsoft Technology Practice Functional Consultants 
- Blaho India - Microsoft Technology Practice Functional Consultants 
- Blaho US - SAP Practice - Technical Consultants  
- Blaho US - SAP Practice - Functional Consultants  
- Blaho US - Microsoft Technology Practice - Technical Consultants 
- Blaho US - Microsoft Technology Practice - Functional Consultants

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Sme malá profesionálna spoločnosť so službami, ktorá funguje len ako jedna divízia. Ako môžeme najlepšie využiť koncept organizačnej jednotky v aktuálnej verzii PSA?

Ak vaša spoločnosť pracuje ako jedna jednotka, ktorá má jeden cenník nákladov, nemusíte nastaviť žiadne organizačné jednotky. Počas inštalácie PSA, Dynamics 365 vytvorí jednu predvolenú organizačnú jednotku, ktorá má rovnaký názov ako organizácia. Predvolene, sú všetci užívatelia priradený k tejto organizačnej jednotke. Vždy, keď systém vyžaduje, aby bola vybratá organizačná jednotka, táto organizačná jednotka je predvolene vybratá.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Keď sa projekt vytvorí z riadka cenovej ponuky alebo riadku zmluvy, predvolená zmluvná jednotka pochádza z cenovej ponuky alebo projektovej zmluvy. Ak je projekt vytvorený pred predajnými entitami, ako je napríklad cenová ponuka alebo projektová zmluva, aká je predvolená zmluvná jednotka?

Keď je projekt vytvorený samostatne, predvolená zmluvná jednotka projektu je založená na používateľovi, ktorý ho vytvorí. Tento používateľ je tiež predvoleným projektovým manažérom. Ak je projekt priradený k predajnej entite, ako je napríklad cenová ponuka alebo projektová zmluva, zmluvná jednotka projektu je založená na predajnej entite. V tomto prípade môžu byť prepočítané odhady projektu, pretože cenník nákladov sa používa na výpočet odhadu nákladov zmeny, ak sa zmení zmluvná jednotka. Predajný cenník sa používa na výpočet odhadov predaja, ktoré sa zmenia tak, aby boli synchronizované s cenníkom projektu v cenovej ponuke.

Polia **Contracting Unit** a **Currency** v projekte sú zamknuté pre úpravy, pretože musia byť synchronizované s hodnotami na predajnej entite (cenová ponuka alebo projektová zmluva), ku ktorej je projekt priradený.
