---
title: Mobilný pracovný priestor Zadanie času projektu
description: Táto téma poskytuje informácie o mobilnom pracovnom priestore Zadanie času projektu. Tento pracovný priestor umožňuje používateľom zadať a uložiť čas oproti projektu pomocou mobilného zariadenia.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755598"
---
# <a name="project-time-entry-mobile-workspace"></a>Mobilný pracovný priestor Zadanie času projektu

[!include [banner](../includes/banner.md)]

Táto téma poskytuje informácie o mobilnom pracovnom priestore **Zadanie času projektu**. Tento pracovný priestor umožňuje používateľom zadať a uložiť čas oproti projektu pomocou mobilného zariadenia.

Tento mobilný pracovný priestor je určený na použitie s mobilnou aplikáciou Dynamics 365 Unified Ops. 

## <a name="overview"></a>Prehľad
V rámci svojej každodennej práce sú zdroje projektu často priamo na mieste alebo cestujú. Mobilný pracovný priestor **Zadanie času projektu** umožňuje používateľom zadať svoj fakturovateľný alebo nefakturovateľný čas oproti projektu na ľubovoľnom mobilnom zariadení. Preto môžu zdroje pre projekty zaznamenávať časové údaje kedykoľvek a kdekoľvek. Môžu tiež zobraziť časové záznamy, ktoré už boli zaznamenané. 

Konkrétne v mobilnom pracovnom priestore **Zadanie času projektu** môžu používatelia vykonávať tieto úlohy:

-   Pre ľubovoľný vybraný dátum zadať počet hodín, ktoré ste strávili konkrétnou úlohou.
-   Vyhľadať podľa názvu projektu alebo zákazníka, aby ste našli projekt, pre ktorý chcete zadať čas.
-   Zadať kategóriu a aktivitu za čas, ktorý ste strávili.
-   Zaznamenať čas pre projekt ako fakturovateľný alebo nefakturovateľný.
-   Voliteľne zadať akékoľvek externé a interné komentáre.

## <a name="prerequisites"></a>Predpoklady
Predpoklady sa líšia v závislosti od verzie Microsoft Dynamics 365, ktorý bol nasadený pre vašu organizáciu.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Predpoklady, ak používate Dynamics 365 Finance
Ak bola pre vašu organizáciu nasadená služba Finance, správca systému musí zverejniť mobilný pracovný priestor **Zadanie času projektu**. Pokyny nájdete v časti [Zverejnenie mobilného pracovného priestoru](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

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

<td>Implementácia KB 4018050.</td>
<td>Správca systému</td>
<td>KB 4018050 je aktualizácia X ++ alebo rýchla oprava metadát, ktorá obsahuje mobilný pracovný priestor <strong>Zadanie času projektu</strong>. Ak chcete implementovať KB 4018050, musí váš správca systému postupovať podľa týchto krokov.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Prevziať si rýchlu opravu metadát z Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Nainštalovať rýchlu opravu metadát</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Vytvoriť nasaditeľný balík,</a> ktorý obsahuje modely <strong>ApplicationSuite</strong> a <strong>ProjectMobile</strong>, a následne nahrať nasaditeľný balík do LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Použiť nasaditeľný balík</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Zverejnenie mobilného pracovného priestoru <strong>Project time entry</strong>.</td>
<td>Správca systému</td>
<td>Pozrite si <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Zverejnenie mobilného pracovného priestoru</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Stiahnite a nainštalujte mobilnú aplikáciu

Stiahnite a nainštalujte mobilnú aplikáciu Finance and Operations:

-   [Pre telefóny Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Pre telefóny iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prihlásenie sa do mobilnej aplikácie
1.  Spustite aplikáciu na mobilnom zariadení.
2.  Zadajte svoju adresu URL pre Dynamics 365.
3.  Pri prvom prihlásení sa zobrazí výzva na zadanie používateľského mena a hesla. Zadajte svoje prihlasovacie údaje.
4.  Po prihlásení sa zobrazia dostupné pracovné priestory pre vašu spoločnosť. Upozorňujeme, že ak váš správca systému zverejní nový pracovný priestor neskôr, budete musieť aktualizovať zoznam mobilných pracovných priestorov.

[![Obnovenie potiahnutím](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Zadanie času pomocou mobilného pracovného priestoru Zadanie času projektu
1.  Na svojom mobilnom zariadení vyberte pracovný priestor **Zadanie času projektu**.
2.  Vyberte **Zadanie času**. Zobrazia sa kalendárne dátumy aktuálneho týždňa.
3.  Pre vybraný dátum zvoľte **Akcie** &gt; **Nový vstup**.
4.  Zadajte počet hodín, ktoré chcete zaznamenať.
5.  Vyberte projekt pre zadanie času. Zoznam zobrazuje projekty, ktoré sa načítajú do vašej aplikácie na offline použitie. Predvolene sa načíta 50 položiek, ale vývojár môže toto číslo zmeniť. Ďalšie informácie získate v časti [Mobilná platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Ak váš projekt nie je v zozname, vyberte **Vyhľadávanie**. Vyhľadávajte podľa názvu alebo prepnite na vyhľadávanie podľa názvu projektu alebo zákazníka.
7.  Vyberte kategóriu. Zoznam zobrazí kategórie, ktoré sa načítajú do vašej aplikácie na offline použitie. Predvolene sa načíta 50 položiek, ale vývojár môže toto číslo zmeniť. Ďalšie informácie získate v časti [Mobilná platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Ak vaša kategória nie je v zozname, vyberte **Vyhľadávanie**. Vyhľadávajte podľa kategórie alebo prepnite na vyhľadávanie podľa názvu kategórie.
9.  Vyberte aktivitu. Zoznam zobrazí aktivity, ktoré sa načítajú do vašej aplikácie na offline použitie. Predvolene sa načíta 50 položiek, ale vývojár môže toto číslo zmeniť. Ďalšie informácie získate v časti [Mobilná platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Ak vaša aktivita nie je v zozname, vyberte **Vyhľadávanie**. Vyhľadávajte podľa čísla aktivity alebo prepnite na vyhľadávanie podľa účelu.

11. Vyberte vlastnosť riadka.
12. Voliteľne: Zadajte akékoľvek externé a interné komentáre.
13. Vyberte **Hotovo**.
