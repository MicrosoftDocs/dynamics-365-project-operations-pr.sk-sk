---
title: Organizačné jednotky
description: Tento článok popisuje koncepciu organizačných jednotiek a vysvetľuje, ako vytvoriť a udržiavať organizačné jednotky v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921643"
---
# <a name="organizational-units-overview"></a>Prehľad organizačných jednotiek

V Microsoft Dynamics 365 Project Operations je *organizačná jednotka* samostatná skupina alebo divízia v spoločnosti, ktorá poskytuje profesionálne služby, ktorá zamestnáva fakturovateľné zdroje, ktoré majú nákladové sadzby.

V spoločnostiach, ktoré poskytujú profesionálne služby, ktoré zamestnávajú technické zdroje v rôznych praktických oblastiach alebo obchodných odvetviach, sa náklady na obsadenie roly môžu líšiť v závislosti od oblasti alebo obchodného odvetvia, v ktorých sa rola obsadzuje. Koncept organizačných jednotiek pomáha v tomto scenári tým, že poskytuje spôsob, ako zoskupiť súbor fakturovateľných rolí v divízii spoločnosti, ktorá má odlišnú štruktúru nákladov pre tieto roly.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Koncepcia organizačných jednotiek v Project Operations

V Project Operations, má organizačná jednotka špecifickú menu a špecifické cenníky obstarávacích cien.

Menou organizačnej jednotky je primárna mena, ktorá sa používa na sledovanie nákladov.

Na každú organizačnú jednotku je možné priložiť jeden alebo viacero cenníkov obstarávacích cien. Project Operations kladie nasledujúce obmedzenia na cenníky, ktoré môžu byť pripojené k organizačnej jednotke:

- Cenníky musia byť v mene organizačnej jednotky.
- Cenníky musia byť v cenníkoch obstarávacích cien.

Okrem toho entita Zdroj obsahuje atribút pre organizačnú jednotku. Každý zdroj môže byť priradený k jednej organizačnej jednotke.

### <a name="roles-of-organizational-units"></a>Roly organizačných jednotiek

Organizačná jednotka hrá v Project Operations dve roly:

- **Contracting unit** – Organizačná jednotka, ktorá zastupuje skupinu spoločností alebo divízie, ktorá je primárne zodpovedná za získanie predaja a riadenie poskytovania práce a služieb zákazníkovi. Zmluvná jednotka je definovaná poľom **Contracting Unit** v sekcii hlavičky na stránkach **Opportunity**, **Quote**, **Project Contract** a **Project**.
- **Resourcing unit** – Organizačná jednotka, ku ktorej zdroj patrí alebo je priradený. Táto organizačná jednotka môže poskytnúť svoje zdroje pre niektoré roly na výkazy práce (SOWs) a projekty, ktoré sú vo vlastníctve zmluvnej jednotky.

![Zmluvné jednotky a zdrojové jednotky.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Najčastejšie otázky o organizačnej jednotke

Tu sú uvedené odpovede na niekoľko z najčastejších otázok o organizačných jednotkách.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Ako súvisí entita Organizačná jednotka v Project Operations s entitou Organizácia, ktorá už existuje v Dynamics 365?

Entita Organizácia v Dynamics 365 predstavuje názov globálnej inštancie Dynamics 365. Tento názov je zvyčajne názov globálneho podniku.

Entita organizačnej jednotky reprezentuje skupinu alebo divíziu v globálnom podniku. Táto skupina alebo divízia má množinu rolí a cenník nákladov pre tieto roly a tieto roly a cenník sa odlišujú od rolí a cenníka iných skupín alebo divízií v podniku.

Keď je nainštalovaný Project Operations, predvolená organizačná jednotka je vytvorená na základe organizácie. Všetky existujúce prostriedky sú priradené k predvolenej organizačnej jednotke. Ak sa importujú nejakí noví používatelia alebo zdroje Active Directory do Dynamics 365, proces importu používateľa ich priradí predvolenej organizačnej jednotke v Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Ako sa entita Organizačná jednotka odlišuje od entity Obchodná jednotka?

V Dynamics 365, entita Obchodnej Jednotky je zabezpečená konštrukcia. Priradenie používateľa k účtovnej jednotke určuje entity a záznamy entity, ku ktorým má používateľ prístup. Určuje tiež povolenia (Create, Read, Write, Delete, Append, Append To, Assign alebo Share), ktoré má používateľ pre tieto záznamy entity.

Entita Organizačnej jednotky predstavuje skupinu spoločností alebo divízie, ktorá má odlišné nákladové sadzby pre zamestnancov, ktorým sú priradené. Priradenie prostriedku k organizačnej jednotke určuje zdrojové náklady na angažovanosť projektu.

Keď implementujete Dynamics 365, optimalizujte povolenia zabezpečenia pre hierarchiu obchodných jednotiek a priraďovanie používateľov k obchodným jednotkám. Priraďte všetkých používateľov, ktorí musia zvyčajne pristupovať k rovnakej množine záznamov na rovnakú obchodnú jednotku. Organizačná jednotka nemá žiadny vplyv na bezpečnostné oprávnenie alebo prístup.

**Príklad, ktorý ukazuje jeden potenciálny rozdiel v modelovaní organizačných jednotiek a obchodných jednotiek**

Blaho, Ltd. má prosperujúce technologické postupy spoločnosti Microsoft. Erik a Viktória sú obaja C\# vývojári, ale Viktória je v Spojených štátoch, zatiaľ čo Erik je v Indii. Väčšina projektových záväzkov si vyžaduje zdroje od spoločnosti Contoso India a Contoso USA a Erik a Viktória si vyžadujú rovnakú úroveň prístupu k zabezpečeniu k projektom v tejto praktickej oblasti. Avšak, náklady na vývojárov z Blaho India sa výrazne líšia od nákladov na vývojárov z Blaho USA.

Tu je optimálny spôsob, ako navrhovať pre tento scenár pomocou Dynamics 365 a Project Operations.

1. Vytvorte technologickú prax spoločnosti Microsoft ako obchodnú jednotku a priraďte ju spoločnosti Erik a Viktória. Týmto spôsobom môžete pomôcť zaistiť, že obaja zamestnanci majú rovnakú úroveň prístupu k zabezpečeniu k akýmkoľvek projektom v tejto oblasti praxe. Obaja budú môcť kontrolovať priebeh a hlásiť čas, výdavky, spotrebu materiálov a aktualizácie úloh.
2. Vytvorte dve organizačné jednotky, ktoré pomôžu zabezpečiť správne zohľadnenie nákladov na projekt.
3. Pripojte Viktóriu ku Contoso USA a Erika ku Contoso India.
4. Priraďte príslušné zoznamy nákladových cenníkov obom organizačným jednotkám. Týmto spôsobom pomôžete zaručiť, že náklady, ktoré sú zaznamenané na projekte pre Erika a Viktóriu presne odrážajú rozdiel v nákladoch medzi Contoso USA a Contoso India.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Sú organizačné jednotky súvisiace s predajnými územiami v Dynamics 365?

Neexistuje žiadne združenie alebo vzťah medzi oblasťami predaja a organizačnými jednotkami. Územie predaja je zvyčajne zemepisnou oblasťou, kde dochádza k predaju. Cenník nákladov môže byť priradený k jednotlivým oblastiam predaja.

Organizačná jednotka je interná skupina alebo divízia v spoločnosti, ktorá sleduje náklady na množinu rolí, ktoré predáva iným divíziám alebo externým zákazníkom.

**Príklad, ktorý ukazuje jeden potenciálny rozdiel v modelovaní organizačných jednotiek a predajných území**

Blaho, Ltd. má dve vývojové centrá: Blaho USA a Blaho India. Náklady na zdroje sa výrazne líšia medzi týmito dvoma vývojovými centrami. Contoso predáva svoje IT služby na mnohých medzinárodných trhoch, ako sú Latinská Amerika, Severná Amerika, Ázia-Tichomorie, Západná Európa a Stredný Východ. Fakturačné sadzby pre rovnaké projektové role sa môžu značne líšiť v týchto trhoch. Blaho USA a Blaho India by mali byť nastavené ako organizačné jednotky a každá organizačná jednotka by mala mať svoj vlastný cenník nákladov. Ázia-Tichomorie, Latinská Amerika, Severná Amerika, Západná Európa a Stredný Východ by mali byť stanovené ako oblasti predaja a každá oblasť predaja by mala mať svoj vlastný predajný cenník.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Prečo existuje obmedzenie asociácie cenníkov s organizačnými jednotkami?

Predajné ceny sú zvyčajne jedinečné pre geografické oblasti alebo trhy, kde sa služby predávajú. Interné divízie spoločnosti nemajú zvyčajne svoje vlastné predajné ceny pre rovnaký typ služieb. Avšak, vnútorné divízie majú rôzne náklady na predaný tovar (COGS), v závislosti na zručnostiach ľudí, ktorých zamestnávajú a pracovné podmienky v regióne, kde pôsobia. Keďže organizačné jednotky sú modelované ako interné divízie spoločnosti, môžu mať len cenníky nákladov.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Prečo nemôžeme priradiť zoznamy predajných cenníkov k organizačným jednotkám?

V Project Operations môžu byť zoznamy predajných cien spojené so zákazníkmi a predajnými územiami. Transakčné entity, ako je Opportunity, Quote, Project Contract, a Project používajú predajné cenníky, ktoré sú pripojené ku kontu zákazníka alebo k oblasti predaja na určenie sadzieb fakturovania a potenciálnych výnosov na zapojenie v projekte.

Cenníky nákladov sú priradené k organizačným jednotkám. Transakčné entity ako Opportunity, Quote, Project Contract a Project používajú cenníky obstarávacích cien, ktoré sú pripojené k obstarávacej jednotke na určenie nákladov na zapojenie do projektu.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Sú organizačné jednotky hierarchické v Project Operations?

Nie. V súčasnom vydaní Project Operations, organizačné jednotky nie sú hierarchické. Preto napríklad môžete vykonať nasledovné úlohy:

- Nakonfigurovať vzor na zadávanie predvolených obstarávacích cien, ktoré budú prechádzať hierarchiou nahor.
- Nahlásiť výnosy alebo náklady na rôznych úrovniach hierarchie organizačnej jednotky.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Sme veľká nadnárodná firma s komplexnou, viacúrovňovou hierarchiou nákladových centier, divízií a fakturačných kancelárií. Ako môžeme najlepšie využiť koncept organizačných jednotiek v aktuálnej verzii Project Operations?

Ak máte komplexnú hierarchiu nákladových centier, divízií, fakturačných kancelárií a pod., nastavte listové uzly hierarchie ako odlišné organizačné jednotky.

Nasledujúci príklad znázorňuje typickú hierarchiu.

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

Ak je vaša hierarchia podobná tomuto príkladu, musíte ju nastaviť ako plochý zoznam, ako je to znázornené tu:

- Blaho India - SAP Practice - Technical Consultants
- Blaho India - SAP Practice - Functional Consultants
- Blaho India - Microsoft Technology Practice Functional Consultants
- Blaho India - Microsoft Technology Practice Functional Consultants
- Blaho US - SAP Practice - Technical Consultants
- Blaho US - SAP Practice - Functional Consultants
- Blaho US - Microsoft Technology Practice - Technical Consultants
- Blaho US - Microsoft Technology Practice - Functional Consultants

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Sme malá profesionálna spoločnosť so službami, ktorá funguje len ako jedna divízia. Ako môžeme najlepšie využiť koncept organizačných jednotiek v aktuálnej verzii Project Operations?

Ak vaša spoločnosť pracuje ako jedna jednotka, ktorá má jeden cenník nákladov, nemusíte nastaviť žiadne organizačné jednotky. Počas inštalácie Project Operations sa vytvorí jedna predvolená organizačná jednotka, ktorá má rovnaký názov ako organizácia. Predvolene, sú všetci užívatelia priradený k tejto organizačnej jednotke. Vždy, keď systém vyžaduje, aby bola vybratá organizačná jednotka, táto organizačná jednotka je predvolene vybratá.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Keď sa projekt vytvorí z riadka cenovej ponuky alebo riadku zmluvy, predvolená zmluvná jednotka pochádza z cenovej ponuky alebo projektovej zmluvy. Aká je predvolená zmluvná jednotka, ak je projekt vytvorený pred predajnými jednotkami, ako je napríklad Cenová ponuka alebo Projektová zmluva?

Keď je projekt vytvorený samostatne, predvolená zmluvná jednotka projektu je založená na používateľovi, ktorý ho vytvorí. Tento používateľ je tiež predvoleným projektovým manažérom. Ak je projekt priradený k predajnej entite, ako je napríklad cenová ponuka alebo projektová zmluva, zmluvná jednotka projektu je založená na predajnej entite. V tomto prípade môžu byť prepočítané odhady projektu, pretože cenník nákladov sa používa na výpočet odhadu nákladov zmeny, ak sa zmení zmluvná jednotka. Predajný cenník sa používa na výpočet odhadov predaja, ktoré sa zmenia tak, aby boli synchronizované s cenníkom projektu v cenovej ponuke.

Polia **Zmluvná jednotka** a **Mena** v projekte sú zamknuté pre úpravy, pretože musia byť synchronizované s hodnotami na predajnej entite (cenová ponuka alebo projektová zmluva), ku ktorej je projekt priradený.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Vytvárajte a udržiavajte organizačné jednotky v Project Operations

Ak chcete vytvoriť organizačnú jednotku v Project Operations, postupujte podľa týchto krokov.

1. Prejdite do **Nastavenia \> Organizačné jednotky**.
2. Vyberte **Nové**.
3. V oblasti **Všeobecné** v poli **Názov** zadajte názov organizačnej jednotky. Potom nastavte ostatné polia podľa potreby.
4. Vyberte **Uložiť** a vytvorte záznam, aby ste mohli pokračovať v jeho úprave.
5. Pod **Cenníky obstarávacej ceny** vyberte symbol plus (**+**), čím pridáte cenník. Môžete tu pridať iba cenníky, ktoré majú kontext **Cena**.
6. V poli **Názov** kliknite na tlačidlo **Search** a vyberte cenník, ktorý chcete sprístupniť pre organizačnú jednotku. Pokračujte v pridávaní cenníkov podľa potreby.
7. Po dokončení pridávania cenníkov vyberte ikonu **Uložiť** v pravom dolnom rohu stránky.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
