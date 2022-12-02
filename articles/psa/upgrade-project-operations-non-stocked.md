---
title: Inovácia z aplikácie Project Service Automation na Project Operations
description: Tento článok poskytuje prehľad procesu inovácie z Microsoft Dynamics 365 Project Service Automation na Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
ms.topic: article
ms.author: ruhercul
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736686"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Inovácia z aplikácie Project Service Automation na Project Operations

S potešením oznamujeme druhú z troch fáz inovácie z Microsoft Dynamics 365 Project Service Automation na Microsoft Dynamics 365 Project Operations. Tento článok poskytuje prehľad pre zákazníkov, ktorí sa vydávajú na túto vzrušujúcu cestu. 

Program poskytovania inovácie bude rozdelený do troch fáz.

| Inovovať doručenie | 1. fáza (január 2022) | 2. fáza (november 2022) | 3. fáza (aprílová vlna vydaní 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Žiadna závislosť od štruktúry rozdelenia práce (WBS) pre projekty | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS v rámci aktuálne podporovaných limitov Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| WBS mimo aktuálne podporovaných limitov Project Operations vrátane podpory pre Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funkcie procesu inovácie 

V rámci procesu inovácie sme do mapy lokality pridali denníky inovácie, aby mohli správcovia jednoduchšie diagnostikovať zlyhania. Okrem nového rozhrania budú pridané nové overovacie pravidlá na zabezpečenie integrity údajov po inovácii. Do procesu inovácie budú pridané nasledujúce overenia.

| Overenia | 1. fáza (január 2022) | 2. fáza (november 2022) | Fáza 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS bude overený proti bežným porušeniam integrity údajov (napríklad priradenia zdrojov, ktoré sú spojené s rovnakou nadradenou úlohou, ale majú rôzne nadradené projekty). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bude overený vzhľadom na [známe limity Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bude overený vzhľadom na známe limity Project Desktop Client. | |  | :heavy_check_mark: |
| Rezervovateľné zdroje a projektové kalendáre budú vyhodnotené voči bežným nekompatibilným výnimkám z pravidiel kalendára. | | :heavy_check_mark: | :heavy_check_mark: |

Vo fáze 2 budú zákazníkom, ktorí inovujú na Project Operations, inovované ich existujúce projekty na prostredie určené len na čítanie pre plánovanie projektov. V tomto prostredí len na čítanie bude v sledovacej mriežke viditeľná úplná štruktúra WBS. Ak chcete upraviť WBS, projektoví manažéri môžu vybrať [**Konvertovať**](/PSA-Upgrade-Project-Conversion.md) na hlavnej stránke projektu. Proces na pozadí potom aktualizuje projekt tak, aby podporoval nové prostredie plánovania projektov z Project for the Web. Táto fáza je vhodná pre zákazníkov, ktorí majú projekty, ktoré zapadajú do [známych limitov Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Vo fáze 3 bude pridaná podpora pre Project Desktop Client v prospech zákazníkov, ktorí chcú naďalej upravovať svoje projekty z tejto aplikácie. Ak sa však existujúce projekty skonvertujú na nové prostredie Project for the Web, prístup k doplnku bude zakázaný pre každý skonvertovaný projekt.

## <a name="prerequisites"></a>Požiadavky

Ak chcete získať nárok na inováciu fázy 1, musíte spĺňať nasledujúce kritériá:

- Cieľové prostredie nesmie obsahovať žiadne záznamy v entite **msdyn_projecttask**.
- Platné licencie Project Operations musia byť priradené všetkým aktívnym používateľom. 
- Proces aktualizácie musíte overiť aspoň v jednom neprodukčnom prostredí, ktoré obsahuje reprezentatívnu množinu údajov, ktorá je v súlade s vaším produkčným prostredím.
- Cieľové prostredie musí byť aktualizované na Project Service Automation Update Release 37 (V3.10.58.120) alebo novšie.

Ak chcete získať nárok na inováciu fázy 2, musíte spĺňať nasledujúce kritériá:

- Platné licencie Project Operations musia byť priradené všetkým aktívnym používateľom. 
- Proces aktualizácie musíte overiť aspoň v jednom neprodukčnom prostredí, ktoré obsahuje reprezentatívnu množinu údajov, ktorá je v súlade s vaším produkčným prostredím.
- Cieľové prostredie musí byť aktualizované na Project Service Automation Update Release 37 (V3.10.58.120) alebo novšie.
- Prostredia obsahujúce úlohy (msdyn_projecttask) sú podporované iba vtedy, ak je celkový počet úloh na projekt 500 alebo menej.

Predpoklady pre fázu 3 budú aktualizované, keď sa bude blížiť dátum všeobecnej dostupnosti.

## <a name="licensing"></a>Licencovanie

Ak máte aktívne licencie pre Project Service Automation, môžete nainštalovať a používať Project Operations, ktorý zahŕňa všetky kľúčové možnosti Project Service Automation a ďalšie. Týmto spôsobom môžete otestovať možnosti Project Operations, zatiaľ čo budete pokračovať v používaní Project Service Automation vo výrobe. Po vypršaní platnosti licencií Project Service Automation budete musieť prejsť na Project Operations. Keď plánujete tento prechod, musíte počítať so skutočnosťou, že licencia Project Operations nezahŕňa licenciu Project Service Automation. Zákazníci, ktorí majú scenáre, v ktorých nasadili Project Service Automation a potrebujú naďalej používať alebo zvyšovať svoje licencie pre PSA, kým plánujú prejsť na Project Operations, môžu požiadať o dočasné licencie PSA na základe zakúpených licencií Project Operations. Jedna licencia Project Service Automation bude vydaná pre jednu licenciu Project Operations. O dočasné licencie PSA môžete požiadať pomocou tohto odkazu: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Testovanie a refaktoring prispôsobení

Ako východiskový bod importujte všetky prispôsobenia do čistého prostredia Project Operations (Lite), aby ste potvrdili, že import je úspešný a že obchodné operácie sa správajú podľa očakávania.

Tu je niekoľko vecí, na ktoré si treba dať pozor:

- Import môže zlyhať z dôvodu chýbajúcich závislostí. Inými slovami, referenčné polia prispôsobení alebo iné komponenty, ktoré boli odstránené v Project Operations. V takom prípade odstráňte tieto závislosti z vývojového prostredia.
- Ak vaše nespravované a spravované riešenia obsahujú komponenty, ktoré nie sú prispôsobené, odstráňte tieto komponenty z riešenia. Napríklad, keď prispôsobíte entitu **Projekt**, pridajte do svojho riešenia iba hlavičku entity. Nepridávajte všetky polia. Ak ste už predtým pridali všetky vedľajšie súčasti, možno budete musieť manuálne vytvoriť nové riešenie a pridať doň relevantné súčasti.
- Formuláre a zobrazenia sa nemusia zobrazovať podľa očakávania. Za určitých okolností, ak ste prispôsobili niektorý z vopred pripravených formulárov alebo zobrazení, prispôsobenia môžu brániť novým aktualizáciám v Project Operations, aby nadobudli účinnosť. Ak chcete identifikovať tieto problémy, odporúčame vám vykonať súbežnú kontrolu čistej inštalácie Project Operations a inštalácie Project Operations, ktorá zahŕňa vaše prispôsobenia. Porovnajte najčastejšie používané formuláre vo vašej firme, aby ste sa uistili, že vaša verzia formulára má stále zmysel a nechýba jej niečo z čistej verzie formulára. Vykonajte rovnaký typ kontroly vedľa seba pre všetky zobrazenia, ktoré ste si prispôsobili.
- Obchodná logika môže zlyhať pri spustení. Pretože odkazy na polia vo vašich doplnkoch nie sú v čase importu overené, obchodná logika môže zlyhať z dôvodu odkazov na polia, ktoré už neexistujú, a môže sa zobraziť chybové hlásenie podobné nasledujúcemu príkladu: „Entita ‚Project‘ neobsahuje atribút s Name = ‚msdyn_plannedhours‘ a NameMapping = ‚Logical‘.“ V tomto prípade upravte svoje prispôsobenia tak, aby používali nové polia. Ak v logike doplnku používate automaticky generované triedy proxy a odkazy na silné typy, zvážte regeneráciu týchto proxy z čistej inštalácie. Týmto spôsobom môžete ľahko identifikovať všetky miesta, kde vaše doplnky závisia od zastaraných polí.

Po aktualizácii prispôsobení, aby ste mohli čisto importovať Project Operations, prejdite na ďalšie kroky.

## <a name="end-to-end-testing-in-development-environments"></a>Komplexné testovanie vo vývojových prostrediach

### <a name="initiate-upgrade"></a>Spustite inováciu 

1. V centra spravovania Power Platform nájdite prostredie a vyberte ho. Potom v aplikáciách vyhľadajte a vyberte **Dynamics 365 Project Operations**.
2. Vyberte **Nainštalovať** na spustenie inovácie. Centrum spravovania Power Platform zobrazí túto inštaláciu ako novú inštaláciu. Zistí sa však prítomnosť staršej verzie Project Service Automation a existujúca inštalácia bude inovovaná.

    Po dokončení inovácie by prostredie malo ukázať, že Project Operations je nainštalované a že Project Service Automation nie je nainštalované.

    V závislosti od množstva údajov v prostredí môže proces inovácie trvať niekoľko hodín. Hlavný tím, ktorý spravuje inováciu, by mal podľa toho naplánovať a spustiť inováciu mimo pracovných hodín. V niektorých prípadoch, ak je objem dát veľký, by mala byť inovácia spustená cez víkend. Rozhodnutie o plánovaní by malo byť založené na výsledkoch testovania v nižších prostrediach.

3. Podľa potreby inovujte vlastné riešenia. V tomto bode nasaďte všetky zmeny, ktoré ste vykonali vo svojich prispôsobeniach, v sekcii [Testovanie a refaktoring prispôsobení](#testing-and-refactoring-customizations) tohto článku.
4. Prejdite na **make.powerapps.com**, vyberte svoje prostredie z rozbaľovacej ponuky v pravom hornom rohu portálu, vyberte **Riešenia** z ponuky vľavo, vyberte riešenie **Zastarané komponenty Project Operations** a následne **Odinštalovať**.

    Toto riešenie je dočasné riešenie, ktoré uchováva existujúci dátový model a komponenty, ktoré sú prítomné počas inovácie. Odstránením tohto riešenia odstránite všetky polia a komponenty, ktoré sa už nepoužívajú. Týmto spôsobom pomáhate zjednodušiť rozhranie a zjednodušiť integráciu a rozšírenie.
    
### <a name="upgrade-to-project-operations-lite"></a>Inovácia na Project Operations Lite

Nasledujúce kroky popisujú proces inovácie a súvisiace protokolovanie chýb:

1. **Kontrola verzie PSA:** Ak chcete nainštalovať Project Operations, musíte mať V3.10.58.120 alebo vyšší.
1. **Predbežné overenie:** Keď správca iniciuje inováciu, systém spustí operáciu predbežného overenia na každej entite, ktorá je jadrom riešenia Project Operations. Tento krok overí, či sú všetky referencie entít platné, a zabezpečí, že údaje súvisiace s WBS sú v rámci publikovaných limitov Project for the Web.
1. **Inovácia metaúdajov:** Po úspešnom predbežnom overení systém iniciuje zmeny schémy a vytvorí riešenie so zastaranými komponentmi. Toto zastarané riešenie môžete odstrániť po dokončení všetkom požadovanom refaktoringu prispôsobení. Tento krok je najdlhšou časťou procesu inovácie a môže trvať až štyri hodiny.
1. **Inovácia údajov:** Po dokončení všetkých požadovaných zmien schémy v kroku inovácie metaúdajov sa vaše údaje migrujú do novej schémy a vykonajú sa všetky požadované predvolené nastavenia a prepočítanie.
1. **Aktualizácia modulu plánovania projektu:** Po úspešnej aktualizácii údajov sa karta **Plán** na hlavnej stránke je premenuje na **Úlohy**. Keď používateľ po inovácii vyberie túto kartu, bude presmerovaný na navigáciu do sledovacej mriežky, aby si mohol pozrieť verziu štruktúry WBS len na čítanie. Ak chcete upraviť štruktúru WBS, musíte spustiť [proces konverzie plánu](/PSA-Upgrade-Project-Conversion.md). Všetky projekty bez už existujúcej štruktúry WBS môžu využívať nové možnosti plánovania priamo, bez konverzie.
 
### <a name="validate-common-scenarios"></a>Overenie bežných scenárov

Pri overovaní vašich konkrétnych prispôsobení vám odporúčame, aby ste si prezreli aj obchodné procesy, ktoré sú podporované v rámci aplikácií. Tieto obchodné procesy zahŕňajú, okrem iného, vytváranie predajných entít, ako sú cenové ponuky a zmluvy, a vytváranie projektov, ktoré zahŕňajú štruktúry WBS a schvaľovanie skutočných hodnôt.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Hlavné zmenu medzi aplikáciami Project Service Automation a Project Operations

Táto časť poskytuje súhrn hlavných zmien, ktoré môžete očakávať medzi aplikáciami Project Service Automation a Project Operations.

### <a name="project-planning"></a>Plánovanie projektu

Možnosti plánovania projektu v Project Operations sa už nespoliehajú na kombináciu logiky na strane klienta a logiky na strane servera. Namiesto toho Project Operations používa Project for the Web ako nástroj plánovania. Táto zmena v možnostiach plánovania umožňuje niekoľko nových funkcií, ako sú zobrazenia tabule a Ganttovho diagramu, plánovanie založené na zdrojoch, [položky kontrolného zoznamu úloh](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) a režimy plánovania projektu. Nové možnosti plánovania podporuje aj bohatá množina nových [rozhraní na programovanie aplikácií (API)](../project-management/schedule-api-preview.md). Tieto rozhrania API majú pomôcť zabezpečiť, aby žiadna programová operácia na vytváranie, aktualizáciu alebo odstraňovanie entity v štruktúre WBS nepoškodila vypočítané polia v pláne.

### <a name="billing-and-pricing"></a>Fakturácia a tvorba cien

V rámci pokračujúcich investícií do Project Operations je k dispozícii niekoľko nových možností v oblasti fakturácie a tvorby cien. Tu sú niektoré príklady:

- [Zaznamenanie využitia materiálu na projektoch a projektových úlohách](../material/material-usage-log.md)
- [Správa subdodávateľských zmlúv](../pro/subcontracting/managing-subcontracts-overview.md)
- [Zálohy a zmluvy založené na preddavkoch](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Stav zmluvy, ktorý sa nesmie prekročiť, a overenia](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Fakturácia podľa úloh

### <a name="resource-management"></a>Správa zdrojov

Project Operations poskytuje voliteľnú podporu pre tabuľu Universal Resource Scheduling (URS) a asistenta plánovania. Toto nové prostredie bude povinné vo vlne vydaní z apríla 2023.

## <a name="frequently-asked-questions"></a>Najčastejšie otázky

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Ktoré typy nasadení sú v súčasnosti podporované na inováciu?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Nasadenie aplikácie Project Operations Lite                        | Podporované               |
| Dynamics 365 Finance Project Management a Accounting | Nasadenie aplikácie Project Operations Lite                        | Momentálne nie je podporované |
| Finance Project Management a Accounting              | Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek     | Momentálne nie je podporované |
| Project Service Automation 3.x                         | Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek     | Momentálne nie je podporované |
| Project for the Web (vyhradené prostredie)            | Nasadenie aplikácie Project Operations Lite                        | Momentálne nie je podporované |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Ako môžem nainštalovať Project Operations predtým, ako budú k dispozícii nástroje inovácie?

Existujú dve možnosti inštalácie Project Operations predtým, ako bude k dispozícii nástroj inovácie:

- Zriadenie nového prostredia.
- Project Operations nasaďte samostatne v akejkoľvek organizácii predaja, kde nie je prítomná Project Service Automation.

Ak je Project Service Automation nainštalovaný v organizácii, ale nebol používaný, je možné ho odinštalovať. Po úplnom odstránení Project Service Automation sa Project Operations môže nainštalovať v tej istej organizácii.
