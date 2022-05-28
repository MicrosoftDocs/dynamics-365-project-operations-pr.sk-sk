---
title: Organizačné jednotky
description: Táto téma popisuje koncepciu organizačných jednotiek a vysvetľuje, ako vytvoriť a udržiavať organizačné jednotky v Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 9a8c503dc6286f40c80ed9b7a8a04974ff7e50b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581395"
---
# <a name="organizational-units-overview"></a>Prehľad organizačných jednotiek

V Microsofte Dynamics 365 Project Operations, an *organizačná jednotka* je osobitná skupina alebo divízia v spoločnosti poskytujúcej profesionálne služby, ktorá využíva fakturovateľné zdroje s nákladovými sadzbami.

V prípade spoločností poskytujúcich profesionálne služby, ktoré využívajú technické zdroje v rôznych oblastiach praxe alebo obchodných línií, sa náklady na obsadenie úlohy môžu líšiť v závislosti od oblasti praxe alebo obchodnej línie, v ktorej je úloha obsadzovaná. V tomto scenári koncept organizačných jednotiek pomáha tým, že poskytuje spôsob, ako zoskupiť skupinu fakturovateľných rolí v divízii spoločnosti, ktorá má pre tieto roly odlišnú štruktúru nákladov.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Koncepcia organizačných jednotiek v projektových operáciách

V projektových operáciách má organizačná jednotka špecifickú menu a špecifické cenníky nákladov.

Menou organizačnej jednotky je primárna mena, ktorá sa používa na sledovanie nákladov.

Na každú organizačnú jednotku je možné priložiť jeden alebo viacero cenníkov obstarávacích cien. Project Operations kladie nasledujúce obmedzenia na cenníky, ktoré môžu byť pripojené k organizačnej jednotke:

- Cenníky musia byť v mene organizačnej zložky.
- Cenníky musia byť nákladové cenníky.

Entita Zdroj navyše obsahuje atribút pre organizačnú jednotku. Každý zdroj môže byť priradený k jednej organizačnej jednotke.

### <a name="roles-of-organizational-units"></a>Roly organizačných jednotiek

Organizačná jednotka zohráva v prevádzke projektu dve úlohy:

- **Contracting unit** – Organizačná jednotka, ktorá zastupuje skupinu spoločností alebo divízie, ktorá je primárne zodpovedná za získanie predaja a riadenie poskytovania práce a služieb zákazníkovi. Zmluvná jednotka je definovaná poľom **Contracting Unit** v sekcii hlavičky na stránkach **Opportunity**, **Quote**, **Project Contract** a **Project**.
- **Resourcing unit** – Organizačná jednotka, ku ktorej zdroj patrí alebo je priradený. Táto organizačná jednotka môže poskytnúť svoje zdroje pre niektoré roly na výkazy práce (SOWs) a projekty, ktoré sú vo vlastníctve zmluvnej jednotky.

![Zmluvné jednotky a zdrojové jednotky.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Organizačná jednotka FAQ

Tu sú uvedené odpovede na niekoľko z najčastejších otázok o organizačných jednotkách.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Ako súvisí entita Organizačná jednotka v Projektových operáciách s entitou Organizácia, ktorá už existuje v Dynamics 365?

Entita Organizácia v Dynamics 365 predstavuje názov globálnej inštancie Dynamics 365. Tento názov je zvyčajne názov globálneho podniku.

Entita organizačnej jednotky reprezentuje skupinu alebo divíziu v globálnom podniku. Táto skupina alebo divízia má množinu rolí a cenník nákladov pre tieto roly a tieto roly a cenník sa odlišujú od rolí a cenníka iných skupín alebo divízií v podniku.

Po nainštalovaní Project Operations sa na základe organizácie vytvorí predvolená organizačná jednotka. Všetky existujúce prostriedky sú priradené k predvolenej organizačnej jednotke. Ak sa do Dynamics 365 importujú nejakí noví používatelia alebo zdroje služby Active Directory, proces importu používateľov ich priradí k predvolenej organizačnej jednotke v Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Ako sa líši entita organizačnej jednotky od entity obchodnej jednotky?

V Dynamics 365, entita Obchodnej Jednotky je zabezpečená konštrukcia. Priradenie používateľa k účtovnej jednotke určuje entity a záznamy entity, ku ktorým má používateľ prístup. Určuje tiež povolenia (Create, Read, Write, Delete, Append, Append To, Assign alebo Share), ktoré má používateľ pre tieto záznamy entity.

Entita Organizačnej jednotky predstavuje skupinu spoločností alebo divízie, ktorá má odlišné nákladové sadzby pre zamestnancov, ktorým sú priradené. Priradenie prostriedku k organizačnej jednotke určuje zdrojové náklady na angažovanosť projektu.

Keď implementujete Dynamics 365, optimalizujte povolenia zabezpečenia pre hierarchiu obchodných jednotiek a priraďovanie používateľov k obchodným jednotkám. Priraďte všetkých používateľov, ktorí musia zvyčajne pristupovať k rovnakej množine záznamov na rovnakú obchodnú jednotku. Organizačná jednotka nemá žiadny vplyv na bezpečnostné oprávnenie alebo prístup.

**Príklad, ktorý ukazuje jeden potenciálny rozdiel v modelovaní organizačných jednotiek a obchodných jednotiek**

Blaho, Ltd. má prosperujúce technologické postupy spoločnosti Microsoft. Erik a Viktória sú obaja C\# vývojári, ale Viktória je v Spojených štátoch, zatiaľ čo Erik je v Indii. Väčšina projektov si vyžaduje zdroje z Contoso Indie a Contoso USA a Prakash a Tricia vyžadujú rovnakú úroveň bezpečnostného prístupu k projektom v tejto praktickej oblasti. Avšak, náklady na vývojárov z Blaho India sa výrazne líšia od nákladov na vývojárov z Blaho USA.

Tu je optimálny spôsob, ako navrhnúť pre tento scenár pomocou Dynamics 365 a Project Operations.

1. Vytvorte technologickú prax spoločnosti Microsoft ako obchodnú jednotku a priraďte ju spoločnosti Erik a Viktória. Týmto spôsobom pomôžete zabezpečiť, aby obaja zamestnanci mali rovnakú úroveň zabezpečenia prístupu ku všetkým projektom v danej oblasti praxe. Obaja budú môcť kontrolovať priebeh a hlásiť čas, výdavky, spotrebu materiálu a aktualizácie úloh.
2. Vytvorte dve organizačné jednotky, ktoré pomôžu zabezpečiť, aby sa náklady na projekt správne odrážali.
3. Spojte Triciu s Contoso USA a Prakash s Contoso Indiou.
4. Priraďte príslušné zoznamy nákladových cenníkov obom organizačným jednotkám. Týmto spôsobom pomôžete zabezpečiť, aby náklady zaznamenané v projekte pre Prakash a Tricia presne odrážali rozdiel v nákladoch medzi Contoso USA a Contoso Indiou.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Sú organizačné jednotky súvisiace s predajnými územiami v Dynamics 365?

Neexistuje žiadne združenie alebo vzťah medzi oblasťami predaja a organizačnými jednotkami. Územie predaja je zvyčajne zemepisnou oblasťou, kde dochádza k predaju. Cenník nákladov môže byť priradený k jednotlivým oblastiam predaja.

Organizačná jednotka je interná skupina alebo divízia v spoločnosti, ktorá sleduje náklady na množinu rolí, ktoré predáva iným divíziám alebo externým zákazníkom.

**Príklad, ktorý ukazuje jeden potenciálny rozdiel v modelovaní organizačných jednotiek a predajných území**

Blaho, Ltd. má dve vývojové centrá: Blaho USA a Blaho India. Náklady na zdroje sa medzi týmito dvoma vývojovými centrami značne líšia. Contoso predáva svoje služby informačných technológií (IT) na mnohých medzinárodných trhoch, ako sú Latinská Amerika, Severná Amerika, Ázia a Tichomorie, západná Európa a Stredný východ. Fakturačné sadzby pre rovnaké projektové role sa môžu značne líšiť v týchto trhoch. Blaho USA a Blaho India by mali byť nastavené ako organizačné jednotky a každá organizačná jednotka by mala mať svoj vlastný cenník nákladov. Ázia-Tichomorie, Latinská Amerika, Severná Amerika, Západná Európa a Stredný Východ by mali byť stanovené ako oblasti predaja a každá oblasť predaja by mala mať svoj vlastný predajný cenník.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Prečo existuje obmedzenie asociácie cenníkov s organizačnými jednotkami?

Predajné ceny sú zvyčajne jedinečné pre geografické oblasti alebo trhy, kde sa služby predávajú. Interné divízie spoločnosti nemajú zvyčajne svoje vlastné predajné ceny pre rovnaký typ služieb. Avšak, vnútorné divízie majú rôzne náklady na predaný tovar (COGS), v závislosti na zručnostiach ľudí, ktorých zamestnávajú a pracovné podmienky v regióne, kde pôsobia. Keďže organizačné jednotky sú modelované ako interné divízie spoločnosti, môžu mať len cenníky nákladov.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Prečo nemôžeme priradiť predajné cenníky k organizačným jednotkám?

V projektových operáciách môžu byť predajné cenníky priradené k zákazníkom a predajným územiam. Transakčné entity ako Opportunity, Quote, Project Contract a Project používajú predajné cenníky, ktoré sú pripojené k zákazníckemu účtu alebo predajnému územiu, na určenie fakturačných sadzieb a potenciálnych výnosov pre projektové zapojenie.

Cenníky nákladov sú priradené k organizačným jednotkám. Transakčné entity ako Opportunity, Quote, Project Contract a Project používajú cenníky nákladov, ktoré sú pripojené k zmluvnej jednotke, na určenie nákladov na projekt.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Sú organizačné jednotky v prevádzke projektu hierarchické?

Nie. V aktuálnom vydaní Project Operations nie sú organizačné jednotky hierarchické. Preto nemôžete vykonávať nasledujúce úlohy:

- Nakonfigurujte vzor na zadávanie predvolených nákladových cien, ktorý prechádza hierarchiou nahor.
- Vykazujte výnosy alebo náklady, ktoré sú zhrnuté na rôznych úrovniach hierarchie organizačných jednotiek.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Sme veľká nadnárodná firma, ktorá má komplexnú, viacúrovňovú hierarchiu nákladových stredísk, divízií a fakturačných kancelárií. Ako najlepšie využiť koncept organizačných jednotiek v aktuálnej verzii Project Operations?

Keď máte zložitú hierarchiu nákladových stredísk, divízií, fakturačných kancelárií atď., nastavte koncové uzly tejto hierarchie ako samostatné organizačné jednotky.

Nasledujúci príklad ukazuje typickú hierarchiu.

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

Ak sa vaša hierarchia podobá tomuto príkladu, musíte ju nastaviť ako plochý zoznam, ako je znázornené tu:

- Blaho India - SAP Practice - Technical Consultants
- Blaho India - SAP Practice - Functional Consultants
- Blaho India - Microsoft Technology Practice Functional Consultants
- Blaho India - Microsoft Technology Practice Functional Consultants
- Blaho US - SAP Practice - Technical Consultants
- Blaho US - SAP Practice - Functional Consultants
- Blaho US - Microsoft Technology Practice - Technical Consultants
- Blaho US - Microsoft Technology Practice - Functional Consultants

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Sme malá profesionálna spoločnosť so službami, ktorá funguje len ako jedna divízia. Ako najlepšie využiť koncept organizačných jednotiek v aktuálnej verzii Project Operations?

Ak vaša spoločnosť pracuje ako jedna jednotka, ktorá má jeden cenník nákladov, nemusíte nastaviť žiadne organizačné jednotky. Inštalácia Project Operations vytvorí jednu predvolenú organizačnú jednotku, ktorá má rovnaký názov ako organizácia. Predvolene, sú všetci užívatelia priradený k tejto organizačnej jednotke. Vždy, keď systém vyžaduje, aby bola vybratá organizačná jednotka, táto organizačná jednotka je predvolene vybratá.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Keď sa projekt vytvorí z riadka cenovej ponuky alebo riadku zmluvy, predvolená zmluvná jednotka pochádza z cenovej ponuky alebo projektovej zmluvy. Aká je predvolená zmluvná jednotka, ak je projekt vytvorený pred predajnými subjektmi, ako je ponuka alebo projektová zmluva?

Keď je projekt vytvorený samostatne, predvolená zmluvná jednotka projektu je založená na používateľovi, ktorý ho vytvorí. Tento používateľ je tiež predvoleným projektovým manažérom. Ak je projekt priradený k predajnej entite, ako je cenová ponuka alebo projektová zmluva, zmluvná jednotka projektu je namiesto toho založená na predajnej entite. V tomto prípade môžu byť prepočítané odhady projektu, pretože cenník nákladov sa používa na výpočet odhadu nákladov zmeny, ak sa zmení zmluvná jednotka. Predajný cenník sa používa na výpočet odhadov predaja, ktoré sa zmenia tak, aby boli synchronizované s projektovým cenníkom ponuky.

The **zmluvná jednotka** a **mena** polia projektu sú uzamknuté na úpravu, pretože musia byť synchronizované s hodnotami predajnej entity (cenová ponuka alebo projektová zmluva), ku ktorej je projekt namapovaný.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Vytvárajte a udržiavajte organizačné jednotky v Project Operations

Ak chcete vytvoriť organizačnú jednotku v Project Operations, postupujte podľa týchto krokov.

1. Ísť do **nastavenie \> Organizačné jednotky**.
2. Vyberte **Nové**.
3. V **generál** oblasť, v **názov** zadajte názov organizačnej jednotky. Potom nastavte ostatné polia podľa potreby.
4. Vyberte **Uložiť** vytvorte záznam, aby ste ho mohli ďalej upravovať.
5. Pod **Cenníky nákladov**, vyberte znamienko plus (**+**) pridať cenník. Môžete pridať iba cenníky, ktoré majú **náklady** kontext tu.
6. V **názov** vyberte pole **Vyhľadávanie** a vyberte cenník, ktorý chcete organizačnej jednotke sprístupniť. Pokračujte v pridávaní cenníkov podľa potreby.
7. Po dokončení pridávania cenníkov vyberte **Uložiť** v pravom dolnom rohu stránky.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
