---
title: Odhadnite tržby a náklady projektu, keď rezervovateľný zdroj plní pre projekt viac rolí
description: Táto téma poskytuje informácie o spôsobe používania dimenzie cien na podporu cien a nákladov pre zdroj, ktorý v projekte plní viac rolí.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5b2b57f5268a92168952b6da5123886df70cd4e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013280"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Odhadnite tržby a náklady projektu, keď rezervovateľný zdroj plní pre projekt viac rolí 

[!include [banner](../includes/psa-now-project-operations.md)]

Projektové spoločnosti často potrebujú jeden zdroj, ktorý by v projekte vykonával viac rolí. Cena a náklady každej z týchto rolí by mohli byť odlišné, čo znamená, že čas, ktorý bude mať rovnaký zdroj v rámci projektu, by mohol nadobudnúť odlišný finančný odhad v závislosti od vyúčtovania a sadzieb nákladov pre každú z rolí. Project Service Automation umožňuje nastavenie hodnôt v zázname člena tímu pre pomenovaný zdroj a umožňuje rozličné prepisovanie jednotlivých úloh, ku ktorým je člen tímu priradený.

Nasledujúci príklad vysvetľuje, ako jednoduché prepísanie tejto hodnoty umožňuje, aby mal zdroj viac rolí v projekte s rôznymi nákladmi a fakturačnými sadzbami.

## <a name="create-tasks"></a>Vytvorenie úloh
Vytvorte dve projektové úlohy po 40 hodín, úlohu A a úlohu B. Vyberte úlohu A ako predchodcu úlohy B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Nastavte rolu a organizačnú jednotku všeobecného člena projektového tímu

1. Na stránke **Plán** vyberte riadok **Úloha** úlohu A. 
2. V poli **Zdroje** vyberte položku **Vytvoriť** z rozbaľovacieho zoznamu.
3. Na stránke **Rýchle vytvorenie člena tímu** zadajte atribúty všeobecného člena tímu, ktorý môže vykonávať túto úlohu.
4. Vyberte príslušnú rolu a organizačnú jednotku a potom vyberte položku **Uložiť a zavrieť**. Vytvorí sa všeobecný člen tímu a priradí sa k tejto úlohe. 

Zopakujte tieto kroky pre úlohu B a uistite sa, že rola a organizačná jednotka člena generického tímu vytvoreného pre úlohu B je iná ako úloha A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Nastavte rolu a organizačnú jednotku projektovej úlohy

1. Po vytvorení úlohy A vyberte úlohu a potom vyberte položku **Upraviť úlohu**.
2. Na stránke **Podrobnosti úlohy** stránku nájdite polia **Rola** a **Organizačná jednotka**, pridajte hodnoty, ktoré sa požadujú od zdroja, ktorý by vykonal túto úlohu. 

  > [!NOTE]
  > Ak dokončujete tieto scenáre pomocou ukážkových údajov z Project Service Automation, vyberte rolu **Vedúci konzultant** pre rolu a organizačnú jednotku **Fabrikam US**.

3. Vyberte úlohu B a potom vyberte **Upraviť úlohu**.
4. Na stránke **Podrobnosti úlohy** stránku nájdite polia **Rola** a **Organizačná jednotka**, pridajte hodnoty, ktoré sa požadujú od zdroja, ktorý by vykonal túto úlohu. Uistite sa, že hodnoty v poliach **Rola** a **Organizačná jednotka** sa líšia pre úlohu B od hodnôt pre úlohu A. 

  > [!NOTE]
  > Ak dokončujete tieto scenáre pomocou ukážkových údajov z Project Service Automation, vyberte rolu **Sieťový technik** pre rolu a organizačnú jednotku **Fabrikam US**.

5. Uložte a zatvorte stránku **Podrobnosti úlohy**. 

## <a name="team-member-and-estimates-behavior"></a>Člen tímu a správanie odhadov 

1. Na stránke **Podrobnosti úlohy** v časti **Člen tímu** vyberte dvoch všeobecných členov tímu a potom vyberte položku **Generovať požiadavky**. 
2. Vyberte riadok člena tímu pre položku **Vedúci konzultant** a potom vyberte položku **Rezervovať**. Otvorí sa tabuľa s rozvrhom a rezervuje sa zdroj na základe tejto požiadavky.
3. Vyberte riadok člena tímu pre položku **Sieťový technik** a potom vyberte položku **Rezervovať**. Otvorí sa tabuľa s rozvrhom a rezervuje sa rovnaký zdroj na základe tejto požiadavky.

### <a name="team-member-grid"></a>Mriežka Člen tímu 
Na mriežke **Člen tímu** si všimnite, že dva všeobecné záznamy členov tímu sú odstránené a jeden zdroj bol nahradený. Pre tento zdroj existuje jedna množina hodnôt, ktorá ukazuje predvolenú množinu hodnôt pre polia **Rola** a **Organizačná jednotka**.
Keď rozbalíte riadok záznamu daného člena tímu, uvidíte v zázname člena tímu odlišné priradenia pre obe tieto úlohy. Každý riadok priradenia má hodnoty špecifické pre položky **Rola** a **Organizačná jednotka**. 

### <a name="estimates-grid"></a>Mriežka Odhady 
Keď prejdete na mriežku **Odhady**, všimnete si, že obidve priradenia toho istého zdroja majú rozdielnu cenu.
Cena za priradenie zdroja v úlohe A sa stanoví pomocou hodnoty atribútu **Rola** položky **Vedúci konzultant**. Cena za priradenie rovnakého zdroja v úlohe B sa stanoví pomocou hodnoty atribútu **Rola** položky **Sieťový technik**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]