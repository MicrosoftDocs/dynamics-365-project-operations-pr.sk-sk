---
title: Priebeh projektu a spotrebu nákladov
description: Táto téma poskytuje informácie o tom, ako sledovať priebeh projektu a spotrebu nákladov.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755644"
---
# <a name="project-progress-and-cost-consumption"></a>Priebeh projektu a spotrebu nákladov

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Potreba sledovať pokrok v rozvrhu sa líši v závislosti od odvetvia. Niektoré odvetvia sledujú na komplexnej úrovni, zatiaľ čo iné odvetvia sledujú na vyššej úrovni. Táto téma ukazuje, ako naplánovať, aby spĺňali požiadavky vašej organizácie.

## <a name="effort-tracking-view"></a>Zobrazenie sledovania úsilia

Zobrazenie **Sledovanie úsilia** zobrazuje pokrok úloh v pláne. Porovnáva skutočné strávené hodiny, ktoré boli strávené na úlohe, s plánovanými hodinami úsilia pre danú úlohu. PSA používa nasledujúce vzorce na výpočet metriky sledovania:

- Percento priebehu = skutočné úsilie vynaložené k dnešnému dňu ÷ plánované úsilie na úlohu 
- Odhad do dokončenia (ETC) = plánované úsilie – skutočné úsilie vynaložené k dnešnému dňu 
- Odhad pri dokončení (EAC) = zostávajúce úsilie + skutočné úsilie vynaložené k dnešnému dňu 
- Odchýlka predpokladaného úsilia = Plánované úsilie – EAC

PSA ukazuje predpoklad variácie úsilia na úlohe. Ak EAC je viac ako plánované úsilie, úloha sa plánuje trvať dlhšie, než bolo pôvodne naplánované. Preto je pozadu za plánom. Ak EAC je menej ako plánované úsilie, úloha sa plánuje trvať kratšie, než bolo pôvodne naplánované. Preto je popredu pred plánom.

## <a name="re-projecting-effort"></a>Opätovné predpokladanie úsilia

Je bežné, že projektový manažér reviduje pôvodné odhady úlohy. Projektové opätovné predpoklady sú vnímaním odhadov projektovým manažérom vzhľadom na súčasný stav projektu. Neodporúčame však, aby projektoví manažéri menili základné čísla, pretože projektový základ predstavuje etablovaný zdroj pravdivých informácií pre plán projektu a odhad nákladov, čo odsúhlasili všetci účastníci projektu.

Existujú dva spôsoby, ktoré projektový manažér môže znovu predpokladať úsilie na úlohy:

- Prepísať predvolené ETC s novým odhadom skutočného zostávajúceho úsilia na úlohe. 
- Prepísať predvolené percento priebehu s novým odhadom skutočného priebehu úlohy.

Každý z týchto prístupov spôsobuje prepočítanie úlohy ETC, EAC a percento pokroku a predpokladané úsilie rozptylu úlohy. EAC, ETC a percento pokroku na súhrnných úlohách sú tiež prepočítané a vytvárajú nový predpoklad variácie úsilia.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Opätovné predpokladanie úsilia na súhrnné úlohy

Úsilie o súhrnné úlohy alebo kontajnerové úlohy možno opätovne predpokladať. Bez ohľadu na to, či používateľ znova predpokladá projekty pomocou zostávajúceho úsilia alebo percenta pokroku na súhrnné úlohy, začne sa nasledovný súbor výpočtov:

- EAC, ETC a percento pokroku v úlohe sú vypočítané.
- Nové EAC sa rozdelí na podradené úlohy v rovnakom pomere ako bolo pri úlohe pôvodné EAC.
- Vypočíta sa nový odhad pri dokončení na samostatné úlohy až po listový uzol. 
- Dotknuté podradené úlohy až po listový uzol majú svoj odhad pri dokončení a percento progresu prepočítané na základe hodnoty odhadu pri dokončení. To má za následok nové predpoklady pre variáciu úsilia úlohy. 
- Vypočítajú sa súhrnné úlohy EAC až po koreňový uzol.

### <a name="cost-tracking-view"></a>Zobrazenie sledovania nákladov 

Zobrazenie **Sledovanie nákladov** porovnáva skutočné náklady, ktoré sa vynaložili na úlohu na plánované náklady na úlohu. 

> [!NOTE]
> Toto zobrazenie zobrazuje iba náklady na pracovnú silu a nezahŕňa náklady z odhadov výdavkov. 

PSA používa nasledujúce vzorce na výpočet metriky sledovania:

- Percento spotrebovaných nákladov = skutočné náklady vynaložené k dátumu ÷ plánované náklady na úlohu
- Náklady na dokončenie (CTC) = plánované náklady– skutočné náklady vynaložené k dnešnému dňu
- EAC = CTC + skutočné náklady vynaložené k dnešnému dňu
- Predpokladaná odchýlka nákladov = plánované náklady – EAC

Predpoklad variácie nákladov sa zobrazuje v úlohe. Ak EAC je viac ako plánované náklady, úloha plánuje stáť viac, než bolo pôvodne naplánované. Preto sa to vyvíja nad rozpočtom. Ak EAC je menej ako plánované náklady, úloha plánuje stáť menej, než bolo pôvodne naplánované. Preto sa to vyvíja pod rozpočtom.

## <a name="project-managers-re-projection-of-cost"></a>Opätovné predpokladanie nákladov zo strany projektového manažéra

Keď je snaha znova predpokladaná, dôjde k spotrebovaniu percenta nákladov CTC, EAC, a prepočítaniu predpokladanej variácie nákladov v zobrazení **Sledovanie nákladov**.

## <a name="project-status-summary"></a>Súhrn stavu projektu

Sledovanie údajov v zobrazení **Sledovanie úsilia** a **Sledovania nákladov** zobrazuje priebeh a spotrebu nákladov v koreňovom uzle projektu, súhrnných úlohách a úrovniach úloh listového uzla. Časť **Stav** na stránke **Projektová entita** zobrazuje súhrn stavov na projektovej úrovni.

## <a name="status-summary-fields"></a>Polia súhrnu stavu

Pole **Celkový stav projektu** je editovateľné pole, ktoré zobrazuje celkový stav projektu. Používa farebné kódovanie, ako je zelená, žltá a červená, na označenie rastúceho rizika. Pole **Poznámky** umožňuje správcovi projektu zadať konkrétne poznámky o stave. Pole **Stav aktualizovaný dňa** nie je možné upravovať a hodnota je časová pečiatka, ktorá indikuje, kedy bol stav naposledy aktualizovaný.

Polia **Výkonnosť plánu** a **Výkonnosť nákladov** sa nastavujú od dátumu sledovania. Keď plán a odchýlka nákladov pre koreňový uzol v zobrazení **Sledovanie úsilia** budú pozitívne, môžete nastaviť tieto polia na možnosť **Popredu**. Keď časový rozvrh a odchýlka nákladov pre koreňový uzol sú záporné, môžete ich nastaviť na možnosť **Pozadu**.
