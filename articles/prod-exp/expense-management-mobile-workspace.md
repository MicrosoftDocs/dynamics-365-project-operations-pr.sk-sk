---
title: Správa výdavkov pomocou mobilného pracovného priestoru
description: Táto téma poskytuje informácie o mobilnom pracovnom priestore na spravovanie výdavkov. Tento pracovný priestor umožňuje používateľom zaznamenať a nahrať účtenku, aby ju mohli neskôr pripojiť k výkazu výdavkov. Používatelia môžu tiež rýchlo vytvoriť riadok výdavkov pomocou priloženej účtenky a vytvárať a spravovať svoje výkazy výdavkov.
author: suvaidya
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2d257ced3dadb320c501bfd5f64dcd8f21c1a4d3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272047"
---
# <a name="expense-management-mobile-workspace"></a>Správa výdavkov pomocou mobilného pracovného priestoru

Táto téma poskytuje informácie o mobilnom pracovnom priestore **Spravovanie výdavkov**. Tento pracovný priestor umožňuje používateľom zaznamenať a nahrať účtenku, aby ju mohli neskôr pripojiť k výkazu výdavkov. Používatelia môžu tiež rýchlo vytvoriť riadok výdavkov pomocou priloženej účtenky a vytvárať a spravovať svoje výkazy výdavkov. Schvaľovatelia môžu navyše používať mobilný pracovný priestor **Správa výdavkov** na prezeranie výkazy výdavkov, ktoré sú im priradené, a tieto výkazy výdavkov buď schváliť, alebo odmietnuť.


Tento mobilný pracovný priestor je určený na použitie s mobilnou aplikáciou Dynamics 365 Unified Ops.


## <a name="overview"></a>Prehľad

Mnoho organizácií vyžaduje, aby bola k výkazu o cestovných alebo obchodných výdavkoch, ktorý zamestnanec predloží na preplatenie, priložená kópia účtenky. Mobilný pracovný priestor **Správa výdavkov** umožňuje používateľom rýchlo vytvoriť riadky s novými výdavkami na mobilnom zariadení podľa vlastného výberu pomocou priloženej fotografie účtenky. Používatelia môžu tiež nasnímať fotografiu účtenky a neskôr ju priložiť k výkazu výdavkov. Zamestnanci môžu tiež vytvárať a spravovať svoje výkazy výdavkov a potom ich pomocou mobilného zariadenia odosielať na schválenie a úhradu.


Mobilný pracovný priestor **Správa výdavkov** konkrétne umožňuje používateľom vykonávať tieto úlohy:

- Odfoťte príjmový doklad a nahrajte ho na Dynamics 365 Finance. Túto fotografiu môžete neskôr priložiť k výkazu výdavkov.
- Nahrajte súbor ako zaznamenanú účtenku. Tento súbor potom môžete neskôr priložiť k výkazu výdavkov.
- Vytvoriť nový riadok výdavkom pomocou priloženej účtenky. Potom môžete riadkovú položku pridať do výkazu výdavkov neskôr a odoslať ju na schválenie a na preplatenie.

Môžete používať aj tieto funkcie:

- Vytvoriť nový výkaz výdavkov.
- Pripojiť transakcie kreditnou kartou a ďalšie predtým vytvorené výdavky k výkazu výdavkov.
- Vytvoriť nové výdavky pre výkaz výdavkov.
- K výkazu výdavkov pripojiť účtenku o výdavku, a to buď odfotením účtenky alebo nahraním súboru ako nasnímanej účtenky.
- V závislosti od politiky výdavkov spoločnosti môžete k výdavku pridať zoznam hostí.
- V závislosti od politiky výdavkov spoločnosti môžete výdavky rozpísať.
- Predložiť výkaz výdavkov na schválenie a úhradu.
- Schváliť alebo odmietnuť výkazy výdavkov, pre ktoré ste prideleným schvaľovateľom.

## <a name="prerequisites"></a>Predpoklady
Požiadavky sa môžu líšiť v závislosti od verzie, ktorá bola nasadená vo vašej organizácii.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Predpoklady, ak používate Dynamics 365 Finance 
Ak bola pre vašu organizáciu nasadená služba Finance, správca systému musí zverejniť mobilný pracovný priestor **Správa výdavkov**. Pokyny nájdete v časti [Zverejnenie mobilných pracovných priestorov](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Nevyhnutné predpoklady, ak používate verziu 1611 s aktualizáciou platformy 3 alebo novšou
Ak bola pre vašu organizáciu nasadená verzia 1611 s aktualizáciou platformy 3 alebo novšou, musí správca systému splniť nasledujúce nevyhnutné predpoklady. 

<table>
<thead>
<tr class="header">
<th>Predpoklady</th>
<th>Rola</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementácia KB 4019015.</td>
<td>Správca systému</td>
<td>KB 4019015 je aktualizácia X++ alebo oprava metaúdajov, ktorá obsahuje mobilný pracovný priestor <strong>Správa výdavkov</strong>. Ak chcete implementovať KB 4019015, musí váš správca systému postupovať podľa týchto krokov.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Prevziať si rýchlu opravu metadát z Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Nainštalovať rýchlu opravu metadát</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Vytvorte balík s možnosťou nasadenia,</a> ktorý obsahuje modely <strong>ApplicationSuite</strong> a <strong>ExpenseMobile</strong>, a potom nahrajte balík s možnosťou nasadenia do LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Použiť nasaditeľný balík</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Zverejnite mobilný pracovný priestor <strong>Správa výdavkov</strong>.</td>
<td>Správca systému</td>
<td>Pozrite si <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Zverejnenie mobilného pracovného priestoru</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Stiahnite a nainštalujte si mobilnú aplikáciu Dynamics 365 for Operations
Stiahnite a nainštalujte si mobilnú aplikáciu Dynamics 365 Unified Ops:

- [Pre telefóny Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Pre telefóny iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prihlásenie sa do mobilnej aplikácie
1. Spustite aplikáciu na mobilnom zariadení.
2. Zadajte svoju adresu URL pre Dynamics 365.
4. Pri prvom prihlásení sa zobrazí výzva na zadanie používateľského mena a hesla. Zadajte svoje prihlasovacie údaje.
5. Po prihlásení sa zobrazia dostupné pracovné priestory pre vašu spoločnosť. Upozorňujeme, že ak váš správca systému zverejní nový pracovný priestor neskôr, budete musieť aktualizovať zoznam mobilných pracovných priestorov.


[![Obnovenie potiahnutím](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Zaznamenajte účtenku pomocou mobilného pracovného priestoru Správa výdavkov

1. Na svojom mobilnom zariadení otvorte pracovný priestor **Správa výdavkov**.
2. Vyberte **Zaznamenať účtenku**.
3. Vyberte **Vyfotografovať** alebo **Vybrať obrázok**.
4. Vykonajte jeden z týchto krokov:

    - Ak ste vybrali **Vyfotografovať**, nasledujte tieto kroky:

        1. Dostali ste sa k fotoaparátu svojho mobilného zariadenia, aby ste mohli účtenku odfotiť. Po odfotografovaní vyberte možnosť **OK** na prijatie fotografie.
        2. Voliteľné: Zadajte názov fotografie a poznámky.

    - Ak ste vybrali **Vybrať obrázok**, nasledujte tieto kroky:

        1. Vyberte obrázok zo zoznamu.
        2. Voliteľné: Zadajte názov obrázku a poznámky.

5. Vyberte **Hotovo**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Rýchlo zadajte výdavky pomocou mobilného pracovného priestoru Správa výdavkov
1. Na svojom mobilnom zariadení otvorte pracovný priestor **Správa výdavkov**.
2. Vyberte **Rýchle zadanie výdavku**.
3. Vyberte kategóriu výdavku. Zobrazí sa zoznam kategórií výdavkov, ktorú sú načítané vo vašej aplikácii na použitie v režime offline. Predvolene sa načíta 50 položiek, ale vývojár môže toto číslo zmeniť. Ďalšie informácie nájdu vývojári v tíme [Mobilná platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ak vaša kategória nie je v zozname, vyberte **Vyhľadávanie** a vyhľadajte ju online. Vyhľadávajte podľa kategórie výdavkov alebo prepnite na vyhľadávanie podľa typu výdavkov.
4. Zadajte dátum transakcie výdavku.
5. Voliteľné: Zadajte obchodníka výdavku.
6. Zadajte sumu výdavku.
7. Vyberte menu výdavku. Zobrazí sa zoznam kódov mien, ktorú sú načítané vo vašej aplikácii na použitie v režime offline. Predvolene sa načíta 400 mien, vývojár však môže tento počet zmeniť. Ďalšie informácie nájdu vývojári v tíme [Mobilná platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ak vaša mena nie je v zozname, vyberte **Vyhľadávanie** a vyhľadajte ju online. Vyhľadávajte podľa meny alebo prepnite na vyhľadávanie podľa názvu.
8. Vyberte **Vyfotografovať** alebo **Vybrať obrázok**.
9. Vykonajte jeden z týchto krokov:

    - Ak ste vybrali možnosť **Vyfotografovať**, dostanete sa k fotoaparátu svojho mobilného zariadenia, aby ste mohli účtenku odfotiť. Po odfotografovaní vyberte možnosť **OK** na prijatie fotografie.
    - Ak ste vybrali **Vybrať obrázok**, vyberte obrázok zo zoznamu.

10. Vyberte **Hotovo**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Schválenie výkazu výdavkov pomocou mobilného pracovného priestoru Správa výdavkov (ak používate aktualizáciu z júla 2017)
1. Na svojom mobilnom zariadení otvorte pracovný priestor **Správa výdavkov**.
2. **Schvaľovanie výdavkov** zobrazuje počet výkazov výdavkov, ktoré sú vám pridelené na schválenie. Tento počet sa aktualizuje každých približne 30 minút. Vyberte **Schvaľovanie výdavkov**.

    Zobrazí sa zoznam výkazov výdavkov, ktoré sú vám pridelené na schválenie.
    
3. Vyberte výkaz výdavkov, aby ste zobrazili podrobnosti o výdavku.
4. Vyberte výdavok, aby ste zobrazili podrobnosti o výdavku. Informácie, ktoré sa zobrazujú pri výdavku, zahŕňajú všetky podrobnosti o účtenke, hosťovi a položkách.
5. Späť na stránke **Výkaz výdavkov** vyberte, či chcete schváliť alebo odmietnuť výkaz výdavkov.
6. Zadajte akékoľvek komentáre k schvaľovacej akcii.
7. Vyberte **Hotovo**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Vytvorenie nového výkazu výdavkov a jeho odoslanie na schválenie pomocou mobilného pracovného priestoru Správa výdavkov (ak používate aktualizáciu z júla 2017)
1. Na svojom mobilnom zariadení otvorte pracovný priestor **Správa výdavkov**.
2. Vyberte **Zadanie výdavku**.
3. Vyberte **Nový výkaz** alebo vyberte existujúci výkaz výdavkov v zozname.
4. Pre nové výkazy výdavkov zadajte účel a všetky ďalšie dostupné informácie. Tieto informácie sa líšia v závislosti od toho, ako je pre vašu spoločnosť nakonfigurované spravovanie výdavkov.
5. Vyberte **Hotovo**.
6. Ak chcete pridať existujúce výdavky, napríklad transakcie kreditnou kartou, do výkazu výdavkov, vyberte **Pripojiť**.
7. V zozname vyberte jeden alebo viac výdavkov.
8. Vyberte **Hotovo**.
9. Ak chcete do výkazu výdavkov pridať nový výdavok, vyberte **Nový výdavok**.
10. Vyberte kategóriu výdavku. Zobrazí sa zoznam kategórií výdavkov, ktorú sú načítané vo vašej aplikácii na použitie v režime offline. Predvolene sa načíta 50 položiek, ale vývojár môže toto číslo zmeniť. Ďalšie informácie nájdu vývojári v tíme [Mobilná platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ak vaša kategória nie je v zozname, vyberte **Vyhľadávanie** a vyhľadajte ju online. Vyhľadávajte podľa kategórie výdavkov alebo prepnite na vyhľadávanie podľa typu výdavkov.
11. Voliteľné: Zadajte obchodníka výdavku.
12. Zadajte dátum transakcie výdavku.
13. Zadajte sumu výdavku.
14. Vyberte menu výdavku. Zobrazí sa zoznam kódov mien, ktorú sú načítané vo vašej aplikácii na použitie v režime offline. Predvolene sa načíta 400 mien, vývojár však môže tento počet zmeniť. Ďalšie informácie nájdu vývojári v tíme [Mobilná platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ak vaša mena nie je v zozname, vyberte **Vyhľadávanie** a vyhľadajte ju online. Vyhľadávajte podľa meny alebo prepnite na vyhľadávanie podľa názvu.
15. Vyberte **Hotovo**.
16. Ak chcete k výdavku pridať ďalšie podrobnosti, vyberte **Pridať ďalšie podrobnosti**. Polia, ktoré sú k dispozícii, závisia od konfigurácie správy výdavkov pre vašu spoločnosť.
17. Ak politika spoločnosti vyžaduje účtenku pre výdavok, vyberte **Účtenky** a potom postupujte podľa týchto krokov:

    1. Vyberte **Zaznamenať účtenku** alebo **Priložiť účtenku**.
    2. Vykonajte jeden z týchto krokov:

        - Ak ste vybrali **Zaznamenať účtenku**, nasledujte tieto kroky:

            1. Vyberte **Vyfotografovať** alebo **Vybrať obrázok**.
            2. Vykonajte jeden z týchto krokov:

                - Ak ste vybrali **Vyfotografovať**, nasledujte tieto kroky:

                    1. Dostali ste sa k fotoaparátu svojho mobilného zariadenia, aby ste mohli účtenku odfotiť. Po odfotografovaní vyberte možnosť **OK** na prijatie fotografie.
                    2. Voliteľné: Zadajte názov fotografie a poznámky.

                - Ak ste vybrali **Vybrať obrázok**, nasledujte tieto kroky:

                    1. Vyberte obrázok zo zoznamu.
                    2. Voliteľné: Zadajte názov obrázku a poznámky.

            3.  Vyberte **Hotovo**.

        - Ak ste vybrali **Pripojiť účtenku**, nasledujte tieto kroky:

            1.  V zozname vyberte jeden alebo viac obrázkov.
            2.  Vyberte **Hotovo**.

    3. Vyberte tlačidlo **Späť** pre návrat k podrobnostiam o výdavku.

18. Ak politika spoločnosti vyžaduje hostí pre výdavok, vyberte **Hostia** a potom postupujte podľa týchto krokov:

    1. Vyberte **Hosť**, **Predošlí hostia** alebo **Spolupracovníci**.
    2. Vykonajte jeden z týchto krokov:

        - Ak ste vybrali **Hosť**, nasledujte tieto kroky:

            1. Zadajte meno hosťa.
            2. Voliteľné: Zadajte organizáciu alebo krajinu hosťa.
            3. Voliteľné: Zadajte titul hosťa.
            4. Vyberte **Hotovo**.

        - Ak ste vybrali **Predchádzajúci hostia**, nasledujte tieto kroky:

            1. V zozname vyberte jedného alebo viacerých predchádzajúcich hostí. Zobrazí sa zoznam predchádzajúcich hostí, ktorých ste pridali do predchádzajúcich výkazov výdavkov, ktoré sú načítané vo vašej aplikácii na offline použitie. Predvolene sa načíta 50 položiek, ale vývojár môže toto číslo zmeniť. Ďalšie informácie nájdu vývojári v tíme [Mobilná platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ak váš predchádzajúci hosť nie je v zozname, vyberte **Vyhľadávanie** a vyhľadajte ho online. Vyhľadávajte podľa mena alebo prepnite na vyhľadávanie podľa organizácie, krajiny alebo titulu.
            2. Vyberte **Hotovo**.

        - Ak ste vybrali **Spolupracovníci**, nasledujte tieto kroky:

            1. V zozname vyberte jedného alebo viacerých spolupracovníkov. Zobrazí sa zoznam spolupracovníkov, ktorí sú načítaní vo vašej aplikácii na použitie v režime offline. Predvolene sa načíta 50 položiek, ale vývojár môže toto číslo zmeniť. Ďalšie informácie nájdu vývojári v tíme [Mobilná platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ak váš spolupracovník nie je v zozname, vyberte **Vyhľadávanie** a vyhľadajte ho online. Vyhľadávajte podľa mena alebo prepnite na vyhľadávanie podľa spoločnosti alebo titulu.
            2. Vyberte **Hotovo**.

    3. Vyberte tlačidlo **Späť** pre návrat k podrobnostiam o výdavku.

19. Ak politika spoločnosti vyžaduje rozpis výdavkov, vyberte **Rozpísať** a potom postupujte podľa týchto krokov:

    1. Vyberte prvý dátum, ktorý chcete rozpísať.
    2. Vyberte položku **Pridať rozpis**.
    3. Vyberte podkategóriu pre rozpis výdavku. Zobrazí sa zoznam podkategórií výdavkov, ktoré sú načítané vo vašej aplikácii na použitie v režime offline. Predvolene sa načíta 50 položiek, ale vývojár môže toto číslo zmeniť. Ďalšie informácie nájdu vývojári v tíme [Mobilná platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Ak vaša podkategória nie je v zozname, vyberte **Vyhľadávanie** a vyhľadajte ju online. Hľadajte podľa názvu podkategórie výdavkov.
    4. Zadajte čiastku transakcie pre rozpis.
    5. Ak je to potrebné, upravte dátum transakcie.
    6. Vyberte **Hotovo**.
    7. Opakujte predchádzajúce kroky, kým nedokončíte pridávanie kompletného rozpisu pre vybraný dátum.
    8. Pre ďalšie dni môžete zvoliť **Kopírovať na ďalší deň** a skopírovať položky do nasledujúceho dňa. Prípadne môžete zvoliť dátum na rozpis a potom pridať rozpis ako pri prvom dátume.
    9. Po dokončení rozpisu výdavkov vyberte tlačidlo **Späť** pre návrat k podrobnostiam o výdavku.

20. Vyberte tlačidlo **Späť** pre návrat na stránku **Výkaz výdavkov**.
21. Predchádzajúce kroky opakujte, kým nedokončíte pridávanie všetkých výdavkov.
22. Stlačte možnosť **Odoslať**.
23. Zadajte akékoľvek komentáre pre schvaľovateľa.
24. Vyberte **Hotovo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]