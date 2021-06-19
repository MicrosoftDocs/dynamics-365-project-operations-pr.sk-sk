---
title: Odhadnite tržby a náklady projektu, keď rezervovateľný zdroj plní v projekte viac rolí
description: Táto téma vysvetľuje, ako používať dimenzie cien na podporu odhadov cien a nákladov pre zdroj, ktorý v projekte plní viac rolí.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7ef9765b7db1c6650fb0599bf5fb4b4b6304be69
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013685"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Odhadnite tržby a náklady projektu, keď rezervovateľný zdroj plní v projekte viac rolí 

_**Vzťahuje sa na:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma, Project Operations pre scenáre založené na zdrojoch/výrobe_ 

Projektové spoločnosti často potrebujú jeden zdroj, ktorý by v projekte plnil viac rolí. Cena a výdavky na každú rolu môžu byť iné. To znamená, že čas toho istého zdroja na projekte môže získať iný finančný odhad v závislosti od vyúčtovania a nákladov na jednotlivé roly. Môžete nastaviť hodnoty v zázname člena tímu pre pomenovaný zdroj s rôznymi prepísanými hodnotami pre každú z úloh, ku ktorým je člen tímu priradený.

Nasledujúci príklad vás prevedie tým, ako jednoduché prepísanie hodnoty umožňuje zdroju mať viac rolí v projekte s rôznymi cenami a fakturačnými sadzbami.

## <a name="create-tasks"></a>Vytvorenie úloh
Ak chcete vytvoriť úlohy, musíte pridať úlohy, ako aj súhrnné úlohy. Potom musíte úlohu priradiť skôr, ako pridáte trvanie úlohy. 

### <a name="add-tasks-and-summary-tasks"></a>Pridanie úloh a súhrnných úloh
Ak chcete pridať úlohu, postupujte podľa nasledujúcich krokov.

1. Prejdite na **Projekty** a otvorte projekt, do ktorého chcete pridať úlohy.
2. Vyberte **Pridať novú úlohu**. Pomenujte úlohu a stlačte **Enter**.
3. Zadajte názov ďalšej úlohy a stlačte **Enter**. Toto opakujte, kým nebudete mať úplný zoznam úloh.
3. Ak chcete odsadiť úlohy pod **Zhrnutím** úloh, vyberte tri zvislé bodky vedľa názvu úlohy a potom vyberte **Vytvoriť vedľajšiu úlohu**. 

  > [!TIP]
  > Ak chcete vybrať viac ako jednu úlohu, vyberte úlohu, stlačte a podržte **Ctrl** a potom vyberte inú úlohu.
  >
  > Môžete si tiež vybrať **Zvýšiť úroveň vedľajšej úlohy**, ak chcete presunúť úlohy zo **Zhrnutia** úloh.

### <a name="assign-tasks"></a>Priradenie úloh

Ak priradiť úlohy, postupujte podľa nasledujúcich krokov.

1. V stĺpci **Priradené:** pre úlohu vyberte ikonu osoby.
2. Vyberte člena tímu zo zoznamu alebo zadajte text a vyhľadajte meno.

### <a name="add-task-duration-and-columns"></a>Pridanie trvania úlohy a stĺpcov

Často je najjednoduchšie začať s výstavbou projektu s dĺžkou trvania. Ak chcete pridať trvanie úlohy, postupujte podľa nasledujúcich krokov.

1. V stĺpci **Trvanie** pre úlohu zadajte počet dní, ktoré si myslíte, že bude trvať splnenie úlohy. Ak chcete použiť inú časovú jednotku, zadajte číslo a slovo **hodín**, **týždňov** alebo **mesiacov**.
2. Ak chcete, aby sa vaša úloha zobrazovala ako míľnik v tvare diamantu v zobrazení **Časová os**, v stĺpci **Trvanie** zadajte **0 dní**.
3. Stlačte **Enter** a prejdite na pole **Trvanie** nasledujúcej úlohy a pokračujte v zadávaní trvania.

  > [!NOTE]
  > Pre súhrnné úlohy nemôžete zadať trvanie.

Do svojho projektu môžete pridať stĺpce, ktoré poskytnú ďalšie podrobnosti. Vykonáte to výberom položky **Pridať stĺpec**. 

Ďalšie informácie sa dozviete v časti [Vytvorenie projektu](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Nastavenie roly a organizačnej jednotky pre všeobecného člena projektového tímu
Vykonaním nasledujúcich krokov nastavíte rolu a organizačnú jednotku pre všeobecného člena tímu.

1. Na stránke **Úlohy** vyberte riadok **Úloha** pre **Úlohu A**. 
2. V časti **Priradené používateľovi** vyberte **Pridanie všeobecných zdrojov**. Týmto sa otvorí stránka **Rýchle vytvorenie člena tímu**.
3. Na stránke **Rýchle vytvorenie člena tímu** zadajte atribúty všeobecného člena tímu, ktorý môže vykonávať túto úlohu.
4. Vyberte príslušnú rolu a organizačnú jednotku a potom vyberte položku **Uložiť a zavrieť**. Vytvorí sa všeobecný člen tímu a priradí sa k tejto úlohe. 
5. Opakujte kroky 1 – 4 pre **Úlohu B**. Avšak **Úloha B** musí mať pre všeobecného člena tímu pridelenú inú rolu a organizačnú jednotku ako **Úloha A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Nastavenie roly a organizačnej jednotky pre projektovú úlohu
Vykonaním nasledujúcich krokov nastavíte rolu a organizačnú jednotku pre úlohu.

1. Potom, čo vytvoríte **Úlohu A**, vyberte úlohu a potom vyberte ikonu **i** na otvorenie tably **Podrobnosti úlohy**. 
2. Na table **Podrobnosti úlohy** prejdite nadol a výberom možnosti **Zobraziť podrobnosti** otvoríte stránku **Podrobnosti úlohy**.
3. Na stránke **Podrobnosti úlohy** v rámci položiek **Rola** a **Organizačná jednotka**, pridajte hodnoty, ktoré sú potrebné na vykonanie tejto úlohy pre zdroj. 

  > [!NOTE]
  > Ak dokončíte tento scenár pomocou ukážkových údajov Project Operations, vyberte **Vedúci konzultant** pre rolu a **Fabrikam USA** ako organizačnú zložku.

4. Vyberte **Úloha B** a potom vyberte úlohu.
5. Výberom ikony **i** sa otvorí tabla **Podrobnosti úlohy**. 
6. Na table **Podrobnosti úlohy** prejdite nadol a výberom možnosti **Zobraziť podrobnosti** otvoríte stránku **Podrobnosti úlohy**.
7. Na stránke **Podrobnosti úlohy** v rámci položiek **Rola** a **Organizačná jednotka** pridajte hodnoty, ktoré sú potrebné, aby zdroj mohol túto úlohu vykonať. Hodnoty v poliach **Rola** a **Organizačná jednotka** pre **Úlohu B** musia byť iné ako pre **Úlohu A**. 

  > [!NOTE]
  > Ak dokončíte tento scenár pomocou ukážkových údajov Project Operations, vyberte **Sieťový technik** pre rolu a **Fabrikam USA** ako organizačnú zložku.

8. Uložte a zatvorte stránku **Podrobnosti úlohy**. 

## <a name="team-member-and-estimates-behavior"></a>Člen tímu a správanie odhadov 
Aby ste pochopili správanie mriežky **Člen tímu** a odhadov, vykonajte nasledujúce kroky.

1. V mriežke **Člen tímu** vyberte dvoch všeobecných členov tímu a potom vyberte **Generovať požiadavky**. Tým sa vygenerujú požiadavky zdrojov. 
2. Vyberte riadok člena tímu pre položku **Vedúci konzultant** a potom vyberte položku **Rezervovať**. Otvorí sa tabuľa plánovania so zoznamom zdrojov. Vyberte zdroj a potom vyberte **Rezervovať** na rezerváciu zdroja podľa tejto požiadavky.
3. Vyberte riadok člena tímu pre položku **Sieťový technik** a potom vyberte položku **Rezervovať**. Otvorí sa tabuľa plánovania so zoznamom zdrojov. Vyberte rovnaký zdroj ako vyššie a potom vyberte **Rezervovať** na rezerváciu zdroja podľa tejto požiadavky.

### <a name="team-member-grid"></a>Mriežka Člen tímu 

Na mriežke **Člen tímu** sa odstránia dva záznamy všeobecných členov tímu a nahradia sa iba jedným zdrojom. Pre tento zdroj existuje jedna množina hodnôt, ktoré sú predvolenou množinou hodnôt pre **Rolu** a **Organizačnú jednotku**.

Keď rozbalíte riadok pre tento záznam člena tímu, uvidíte v zázname člena tímu odlišné priradenia pre obe úlohy. Každý riadok priradenia má hodnoty špecifické pre položky **Rola** a **Organizačná jednotka**. 

### <a name="estimates-grid"></a>Mriežka Odhady 

Na mriežke **Odhady** sú obidve priradenia toho istého zdroja ocenené rozdielne. Cena za priradenie zdroja v **úlohe A** sa stanoví pomocou hodnoty atribútu **Rola** položky **Vedúci konzultant**. Cena za priradenie rovnakého zdroja v **úlohe B** sa stanoví pomocou hodnoty atribútu **Rola** položky **Sieťový technik**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]