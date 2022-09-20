---
title: Inovujte z Automatizácie projektových služieb na Projektové operácie
description: Tento článok poskytuje prehľad procesu inovácie Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.openlocfilehash: 43ea29aeafb62f3ecd69b316f2c0a5b791707da5
ms.sourcegitcommit: bc21fbe8547534d2644269f873eb05d509840f23
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446055"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Inovujte z Automatizácie projektových služieb na Projektové operácie

S potešením oznamujeme prvú z troch fáz inovácie Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Project Operations. Tento článok poskytuje prehľad pre zákazníkov, ktorí sa vydávajú na túto vzrušujúcu cestu. Budúce články budú obsahovať úvahy vývojárov a podrobnosti o vylepšeniach funkcií. Poskytnú vám nielen pokyny, ktoré vám pomôžu pripraviť sa na inováciu na Project Operations, ale tiež vysvetlia, čo môžete očakávať po inovácii.

Program poskytovania aktualizácie bude rozdelený do troch fáz.

| Inovovať doručenie | 1. fáza (január 2022) | 2. fáza (november 2022) | 3. fáza (aprílová vlna 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Žiadna závislosť od štruktúry rozpisu prác (WBS) pre projekty | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS v rámci aktuálne podporovaných limitov projektových operácií | | :heavy_check_mark: | :heavy_check_mark: |
| WBS mimo aktuálne podporovaných limitov Project Operations, vrátane podpory pre desktopového klienta Project | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Aktualizujte funkcie procesu 

V rámci procesu inovácie sme do mapy lokality pridali denníky inovácie, aby správcovia mohli jednoduchšie diagnostikovať zlyhania. Okrem nového rozhrania budú pridané nové overovacie pravidlá na zabezpečenie integrity údajov po inovácii. Do procesu inovácie budú pridané nasledujúce overenia.

| Validácie | 1. fáza (január 2022) | 2. fáza (november 2022) | 3. fáza  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS bude overený proti bežným porušeniam integrity údajov (napríklad priradenia zdrojov, ktoré sú spojené s rovnakou nadradenou úlohou, ale majú rôzne nadradené projekty). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bude overený voči [známe limity Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bude overený voči známym limitom desktopového klienta Project. | |  | :heavy_check_mark: |
| Rezervovateľné zdroje a projektové kalendáre budú hodnotené podľa bežných nekompatibilných výnimiek z pravidiel kalendára. | | :heavy_check_mark: | :heavy_check_mark: |

Vo fáze 2 budú zákazníci, ktorí inovujú na Project Operations, upgradované svoje existujúce projekty na prostredie určené len na čítanie pre plánovanie projektov. V tomto prostredí len na čítanie bude v sledovacej mriežke viditeľný úplný WBS. Ak chcete upraviť WBS, projektoví manažéri môžu vybrať **Konvertovať** na hlavnej **Projekty** stránku. Proces na pozadí potom aktualizuje projekt tak, aby podporoval novú skúsenosť s plánovaním projektu z Project for the Web. Táto fáza je vhodná pre zákazníkov, ktorí majú projekty, ktoré do nej zapadajú [známe limity Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Vo fáze 3 bude pridaná podpora pre desktopového klienta Project v prospech zákazníkov, ktorí chcú naďalej upravovať svoje projekty z tejto aplikácie. Ak sa však existujúce projekty skonvertujú na nové prostredie Project for the Web, prístup k doplnku bude zakázaný pre každý skonvertovaný projekt.

## <a name="prerequisites"></a>Požiadavky

Aby bol zákazník oprávnený na inováciu fázy 1, musí spĺňať nasledujúce kritériá:

- Cieľové prostredie nesmie obsahovať žiadne záznamy v **msdyn_projecttask** subjekt.
- Platné licencie Project Operations musia byť priradené všetkým aktívnym používateľom zákazníka. 
- Zákazník musí overiť proces inovácie aspoň v jednom neprodukčnom prostredí, ktoré má reprezentatívny súbor údajov, ktorý je zosúladený s produkčnými údajmi.
- Cieľové prostredie musí byť aktualizované na Project Service Automation Update Release 41 (3.10.62.162) alebo novšie.

Predpoklady pre fázu 2 a fázu 3 budú aktualizované, keď sa budú blížiť všeobecné dátumy dostupnosti.

## <a name="licensing"></a>Licencovanie

Ak máte aktívne licencie pre Project Service Automation, môžete nainštalovať a používať Project Operations, ktorý zahŕňa všetky možnosti Project Service Automation a ďalšie. Týmto spôsobom môžete otestovať schopnosti projektových operácií, zatiaľ čo budete pokračovať v používaní Project Service Automation vo výrobe. Po vypršaní platnosti licencií Project Service Automation budete musieť prejsť na Project Operations. Keď plánujete tento prechod, musíte počítať so skutočnosťou, že licencia Project Operations nezahŕňa licenciu Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Testovanie a refaktorovanie prispôsobení

Ako východiskový bod importujte všetky prispôsobenia do čistého prostredia Project Operations (Lite), aby ste potvrdili, že import je úspešný a že obchodné operácie sa správajú podľa očakávania.

Tu je niekoľko vecí, na ktoré si treba dať pozor:

- Import môže zlyhať z dôvodu chýbajúcich závislostí. Inými slovami, referenčné polia prispôsobení alebo iné komponenty, ktoré boli odstránené v Project Operations. V takom prípade odstráňte tieto závislosti z vývojového prostredia.
- Ak vaše nespravované a spravované riešenia obsahujú komponenty, ktoré nie sú prispôsobené, odstráňte tieto komponenty z riešenia. Napríklad, keď prispôsobíte **Projekt** entity, pridajte do svojho riešenia iba hlavičku entity. Nepridávajte všetky polia. Ak ste už predtým pridali všetky podkomponenty, možno budete musieť manuálne vytvoriť nové riešenie a pridať doň relevantné komponenty.
- Formuláre a zobrazenia sa nemusia zobrazovať podľa očakávania. Za určitých okolností, ak ste prispôsobili niektorý z vopred pripravených formulárov alebo zobrazení, prispôsobenia môžu brániť novým aktualizáciám v prevádzke projektu, aby nadobudli účinnosť. Ak chcete identifikovať tieto problémy, odporúčame vám vykonať súbežnú kontrolu čistej inštalácie Project Operations a inštalácie Project Operations, ktorá zahŕňa vaše prispôsobenia. Porovnajte najčastejšie používané formuláre vo vašej firme, aby ste sa uistili, že vaša verzia formulára má stále zmysel a nechýba jej niečo z čistej verzie formulára. Vykonajte rovnaký typ kontroly vedľa seba pre všetky zobrazenia, ktoré ste si prispôsobili.
- Obchodná logika môže zlyhať pri spustení. Pretože odkazy na polia vo vašich zásuvných moduloch nie sú v čase importu overené, obchodná logika môže zlyhať z dôvodu odkazov na polia, ktoré už neexistujú, a môže sa zobraziť chybové hlásenie podobné nasledujúcemu príkladu: "'Project' entita neobsahuje atribút s Name = 'msdyn_plannedhours' a NameMapping = 'Logické'." V tomto prípade upravte svoje prispôsobenia tak, aby používali nové polia. Ak v logike doplnku používate automaticky generované triedy proxy a odkazy na silné typy, zvážte regeneráciu týchto proxy z čistej inštalácie. Týmto spôsobom môžete ľahko identifikovať všetky miesta, kde vaše doplnky závisia od zastaraných polí.

Po aktualizácii prispôsobení, aby ste mohli čisto importovať operácie projektu, prejdite na ďalšie kroky.

## <a name="end-to-end-testing-in-development-environments"></a>End-to-end testovanie vo vývojových prostrediach

### <a name="initiate-upgrade"></a>Spustite inováciu 

1. V Power Platform centrum spravovania, nájdite a vyberte svoje prostredie. Potom v aplikáciách vyhľadajte a vyberte **Dynamics 365 Project Operations**.
2. Vyberte **Inštalácia** na spustenie inovácie. The Power Platform admin center zobrazí túto inštaláciu ako novú inštaláciu. Zistí sa však prítomnosť staršej verzie Project Service Automation a existujúca inštalácia bude inovovaná.

    Po dokončení inovácie by prostredie malo ukázať, že Project Operations je nainštalovaný a že Project Service Automation nie je nainštalovaný.

    > [!NOTE]
    > V závislosti od množstva údajov v prostredí môže aktualizácia trvať niekoľko hodín. Hlavný tím, ktorý spravuje inováciu, by mal podľa toho naplánovať a spustiť inováciu počas mimopracovných hodín. V niektorých prípadoch, ak je objem dát veľký, upgrade by mal byť spustený cez víkend. Rozhodnutie o plánovaní by malo byť založené na výsledkoch testovania v nižších prostrediach.

3. Podľa potreby inovujte vlastné riešenia. V tomto bode nasaďte všetky zmeny, ktoré ste vykonali vo svojich prispôsobeniach v [Testovanie a refaktorovanie prispôsobení](#testing-and-refactoring-customizations) časti tohto článku.
4. Ísť do **nastavenie** \> **Riešenia** a vyberte možnosť odinštalovať **Zastarané komponenty projektových operácií** Riešenie.

    Toto riešenie je dočasné riešenie, ktoré uchováva existujúci dátový model a komponenty, ktoré sú prítomné počas inovácie. Odstránením tohto riešenia odstránite všetky polia a komponenty, ktoré sa už nepoužívajú. Týmto spôsobom pomáhate zjednodušiť rozhranie a zjednodušiť integráciu a rozšírenie.
    
### <a name="validate-common-scenarios"></a>Overte bežné scenáre

Pri overovaní vašich konkrétnych prispôsobení vám odporúčame, aby ste si prezreli aj obchodné procesy, ktoré sú podporované v rámci aplikácií. Tieto obchodné procesy zahŕňajú, ale nie sú obmedzené na, vytváranie predajných entít, ako sú cenové ponuky a zmluvy, a vytváranie projektov, ktoré zahŕňajú WBS a schvaľovanie skutočností.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Hlavné zmeny medzi automatizáciou projektových služieb a prevádzkou projektu

Táto časť poskytuje súhrn hlavných zmien, ktoré môžete očakávať medzi Project Service Automation a Project Operations.

### <a name="project-planning"></a>Plánovanie projektu

Možnosti plánovania projektu v Project Operations sa už nespoliehajú na kombináciu logiky na strane klienta a logiky na strane servera. Namiesto toho Project Operations používa Project for the Web ako nástroj plánovania. Táto zmena v možnostiach plánovania umožňuje niekoľko nových funkcií, ako sú Board a Ganttov pohľad, plánovanie založené na zdrojoch, [položky kontrolného zoznamu úloh](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) a režimy plánovania projektu. Nové možnosti plánovania podporuje aj bohatá sada nových [aplikačné programové rozhrania (API)](../project-management/schedule-api-preview.md). Tieto rozhrania API majú pomôcť zabezpečiť, aby žiadna programová operácia na vytváranie, aktualizáciu alebo odstraňovanie entity vo WBS nepoškodila vypočítané polia v pláne.

## <a name="billing-and-pricing"></a>Fakturácia a tvorba cien

V rámci pokračujúcich investícií do prevádzky projektu je k dispozícii niekoľko nových možností v oblasti fakturácie a tvorby cien. Tu sú niektoré príklady:

- [Evidovanie spotreby materiálu na projektoch a projektových úlohách](../material/material-usage-log.md)
- [Manažment subdodávok](../pro/subcontracting/managing-subcontracts-overview.md)
- [Zálohy a zmluvy založené na preddavkoch](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Stav neprekročenia zmluvy a overenia](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Účtovanie podľa úloh

## <a name="frequently-asked-questions"></a>Najčastejšie otázky

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Ktoré typy nasadení sú v súčasnosti podporované na inováciu?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Projektové operácie Lite Deployment                        | Podporované               |
| Dynamics 365 Finance Projektový manažment a účtovníctvo | Projektové operácie Lite Deployment                        | Momentálne nie je podporované |
| Finančný projektový manažment a účtovníctvo              | Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek     | Momentálne nie je podporované |
| Automatizácia projektových služieb 3.x                         | Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek     | Momentálne nie je podporované |
| Projekt pre web (vyhradené prostredie)            | Projektové operácie Lite Deployment                        | Momentálne nie je podporované |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Ako môžem nainštalovať Project Operations predtým, ako budú k dispozícii nástroje inovácie?

Existujú dve možnosti inštalácie Project Operations predtým, ako bude k dispozícii nástroj inovácie:

- Poskytnutie nového prostredia.
- Operácie projektu nasaďte samostatne v akejkoľvek predajnej organizácii, kde nie je prítomná automatizácia projektových služieb.

> [!NOTE]
> Ak je Project Service Automation nainštalovaný v organizácii, ale nebol používaný, je možné ho odinštalovať. Po úplnom odstránení Project Service Automation sa Project Operations môže nainštalovať v tej istej organizácii.
