---
title: Prehľad sledovania projektu
description: Táto téma poskytuje informácie o tom, ako sledovať priebeh projektu a spotrebu nákladov.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907382"
---
# <a name="project-tracking-overview"></a>Prehľad sledovania projektu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Potreba sledovať pokrok v rozvrhu sa líši v závislosti od odvetvia. Niektoré odvetvia sledujú na komplexnej úrovni, pričom iné odvetvia sledujú na vyššej úrovni. Táto téma ukazuje, ako naplánovať, aby spĺňali požiadavky vašej organizácie.

## <a name="effort-tracking-view"></a>Zobrazenie sledovania úsilia

Zobrazenie **Sledovanie úsilia** sleduje priebeh úloh v pláne porovnaním skutočných hodín úsilia strávených nad úlohou s plánovanými hodinami úsilia úlohy. Dynamics 365 Project Operations používa nasledujúce vzorce na výpočet metriky sledovania:

- **Percento priebehu**: skutočné úsilie vynaložené k dnešnému dňu ÷ odhad pri dokončení (EAC) 
- **Odhad do dokončenia (ETC)**: plánované úsilie – skutočné úsilie vynaložené k dnešnému dňu 
- **Odhad pri dokončení**: zostávajúce úsilie + skutočné úsilie vynaložené k dnešnému dňu 
- **Odchýlka predpokladaného úsilia**: Plánované úsilie – Odhad pri dokončení

Project Operations ukazuje predpoklad variácie úsilia na úlohe. Ak je úroveň odhadu pri dokončení vyššia ako plánované úsilie, úloha sa plánuje trvať dlhšie, než bolo pôvodne naplánované a prekračuje plán. Ak je úroveň odhadu pri dokončení nižšia ako plánované úsilie, úloha sa plánuje trvať kratšie, než bolo pôvodne naplánované a predbieha plán.

## <a name="reprojecting-effort"></a>Opätovné predpokladanie úsilia

Projektoví manažéri často reviduje pôvodné odhady úlohy. Projektové opätovné predpoklady sú vnímaním odhadov projektovým manažérom vzhľadom na súčasný stav projektu. Neodporúčame však, aby projektoví manažéri menili základné hodnoty. Dôvodom je, že projektový základ predstavuje etablovaný zdroj pravdivých informácií pre plán projektu a odhad nákladov, čo odsúhlasili všetci účastníci projektu.

Existujú dva spôsoby, ktoré projektový manažér môže znovu predpokladať úsilie na úlohy:

- Prepísať predvolené ETC s novým odhadom skutočného zostávajúceho úsilia na úlohe. 
- Prepísať predvolené percento priebehu s novým odhadom skutočného priebehu úlohy.

Každý prístup spôsobí prepočítanie odhadu do dokončenia, odhadu pri dokončení, percenta pokroku a predpokladaného úsilia rozptylu úlohy. Odhad pri dokončení, odhad do dokončenia a percento pokroku na súhrnných úlohách sú tiež prepočítané a vytvárajú nový predpoklad variácie úsilia.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Opätovné predpokladanie úsilia na súhrnné úlohy

Úsilie o súhrnné úlohy alebo kontajnerové úlohy možno opätovne predpokladať. Bez ohľadu na to, či používateľ znova predpokladá projekty pomocou zostávajúceho úsilia alebo percenta pokroku na súhrnné úlohy, začne sa nasledovný súbor výpočtov:

- EAC, ETC a percento pokroku v úlohe sú vypočítané.
- Nové EAC sa rozdelí na podradené úlohy v rovnakom pomere ako bolo pri úlohe pôvodné EAC.
- Vypočíta sa nový odhad pri dokončení na samostatné úlohy až po listový uzol. 
- Dotknuté podradené úlohy až po listový uzol majú svoj odhad pri dokončení a percento progresu prepočítané na základe hodnoty odhadu pri dokončení. To má za následok nové predpoklady pre variáciu úsilia úlohy. 
- Vypočítajú sa súhrnné úlohy EAC až po koreňový uzol.

### <a name="cost-tracking-view"></a>Zobrazenie sledovania nákladov 

Zobrazenie **Sledovanie nákladov** porovnáva skutočné náklady, ktoré sa vynaložili na úlohu na plánované náklady na úlohu. 

> [!NOTE]
> Toto zobrazenie zobrazuje iba náklady na pracovnú silu a nezahŕňa náklady z odhadov výdavkov. Project Operations používa nasledujúce vzorce na výpočet metriky sledovania:

- **Percento spotrebovaných nákladov**: skutočné náklady vynaložené k dátumu ÷ odhad nákladov pri dokončení
- **Náklady na dokončenie (CTC)**: plánované náklady– skutočné náklady vynaložené k dnešnému dňu
- **Odhad pri dokončení**: Zostávajúce náklady + Doterajšie skutočné náklady
- **Predpokladaná odchýlka nákladov**: plánované náklady – odhad pri dokončení

Predpoklad variácie nákladov sa zobrazuje v úlohe. Ak EAC je viac ako plánované náklady, úloha plánuje stáť viac, než bolo pôvodne naplánované. Preto sa to vyvíja nad rozpočtom. Ak EAC je menej ako plánované náklady, úloha plánuje stáť menej, než bolo pôvodne naplánované. Preto sa to vyvíja pod rozpočtom.

## <a name="project-managers-reprojection-of-cost"></a>Opätovné predpokladanie nákladov zo strany projektového manažéra

Keď je snaha znova predpokladaná, dôjde k spotrebovaniu percenta nákladov CTC, EAC, a prepočítaniu predpokladanej variácie nákladov v zobrazení **Sledovanie nákladov**.

## <a name="project-status-summary"></a>Súhrn stavu projektu

Sledovanie údajov v zobrazení **Sledovanie úsilia** a **Sledovania nákladov** zobrazuje priebeh a spotrebu nákladov v koreňovom uzle projektu, súhrnných úlohách a úrovniach úloh listového uzla. Časť **Stav** na stránke **Projektová entita** zobrazuje súhrn stavov na projektovej úrovni.

## <a name="status-summary-fields"></a>Polia súhrnu stavu

Pole **Celkový stav projektu** je editovateľné pole, ktoré zobrazuje celkový stav projektu. Používa farebné kódovanie, ako je zelená, žltá a červená, na označenie rastúceho rizika. Pole **Poznámky** umožňuje správcovi projektu zadať konkrétne poznámky o stave. Pole **Stav aktualizovaný dňa** nie je možné upravovať a hodnota je časová pečiatka, ktorá indikuje, kedy bol stav naposledy aktualizovaný.

Polia **Výkonnosť plánu** a **Výkonnosť nákladov** sa nastavujú od dátumu sledovania. Keď plán a odchýlka nákladov pre koreňový uzol v zobrazení **Sledovanie úsilia** budú pozitívne, môžete nastaviť tieto polia na možnosť **Popredu**. Keď časový rozvrh a odchýlka nákladov pre koreňový uzol sú záporné, môžete ich nastaviť na možnosť **Pozadu**.
