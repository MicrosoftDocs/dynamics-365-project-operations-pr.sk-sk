---
title: Sledovanie úsilia na projekte
description: Táto téma poskytuje informácie o tom, ako sledovať úsilie na projekte a priebeh prác.
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3fdf7787f0144dace84852a0442406085bdc1639
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010895"
---
# <a name="project-effort-tracking"></a>Sledovanie úsilia na projekte

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Potreba sledovať pokrok v rozvrhu sa líši v závislosti od odvetvia. Niektoré odvetvia sledujú na komplexnej úrovni, pričom iné odvetvia sledujú na vyššej úrovni. Táto téma ukazuje, ako naplánovať, aby spĺňali požiadavky vašej organizácie.

## <a name="effort-tracking-view"></a>Zobrazenie sledovania úsilia

Zobrazenie **Sledovanie úsilia** sleduje priebeh úloh v pláne porovnaním skutočných hodín úsilia strávených nad úlohou s plánovanými hodinami úsilia úlohy. Dynamics 365 Project Operations používa nasledujúce vzorce na výpočet metriky sledovania:

- **Percento priebehu**: skutočné úsilie vynaložené k dnešnému dňu ÷ odhad pri dokončení (EAC) 
- **Zostávajúce úsilie**: Odhadované úsilie na dokončenie – Skutočné úsilie vynaložené k dnešnému dňu 
- **Odhad pri dokončení**: zostávajúce úsilie + skutočné úsilie vynaložené k dnešnému dňu 
- **Odchýlka predpokladaného úsilia**: Plánované úsilie – Odhad pri dokončení

Project Operations ukazuje predpoklad variácie úsilia na úlohe. Ak je úroveň odhadu pri dokončení vyššia ako plánované úsilie, úloha sa plánuje trvať dlhšie, než bolo pôvodne naplánované a prekračuje plán. Ak je úroveň odhadu pri dokončení nižšia ako plánované úsilie, úloha sa plánuje trvať kratšie, než bolo pôvodne naplánované a predbieha plán.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Preplánovanie úsilia na úlohy listových uzlov

Projektoví manažéri často reviduje pôvodné odhady úlohy. Projektové opätovné predpoklady sú vnímaním odhadov projektovým manažérom vzhľadom na súčasný stav projektu. Neodporúčame však, aby projektoví manažéri zmenili hodnoty plánovaného úsilia. Je to preto, že plánované úsilie projektu predstavuje zavedený zdroj pravdy pre harmonogram projektu a odhad nákladov, a všetci zainteresovaní účastníci projektu s ním súhlasili.

Manažér projektu môže preplánovať úsilie na úlohy aktualizáciou predvolenej hodnoty **Zostávajúce úsilie** novým odhadom úlohy. Táto aktualizácia spôsobuje prepočet odhadu úlohy po dokončení (EAC), percentuálneho pokroku a projektovanej odchýlky úsilia pri úlohe. Odhad pri dokončení, odhad do dokončenia a percento pokroku na súhrnných úlohách sú tiež prepočítané a vytvárajú nový predpoklad variácie úsilia.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Opätovné predpokladanie úsilia na súhrnné úlohy

Úsilie o súhrnné úlohy alebo kontajnerové úlohy možno opätovne predpokladať. Projektoví manažéri môžu aktualizovať zostávajúce úsilie týkajúce sa súhrnných úloh. Aktualizácia zostávajúceho úsilia spustí v aplikácii nasledujúcu skupinu výpočtov:

- EAC a percento pokroku v úlohe sú vypočítané.
- Nové EAC sa rozdelí na podradené úlohy v rovnakom pomere ako bolo pri úlohe pôvodné EAC.
- Vypočíta sa nový odhad pri dokončení na samostatné úlohy až po listový uzol. 
- Dotknuté podradené úlohy až po listový uzol majú svoje zostávajúce úsilie a percento progresu prepočítané na základe hodnoty odhadu pri dokončení. To má za následok nové predpoklady pre variáciu úsilia úlohy. 
- Vypočítajú sa súhrnné úlohy EAC až po koreňový uzol.


## <a name="project-status-summary"></a>Súhrn stavu projektu

Sledovanie údajov v zobrazení **Sledovanie úsilia** a **Sledovania nákladov** zobrazuje priebeh a spotrebu nákladov v koreňovom uzle projektu, súhrnných úlohách a úrovniach úloh listového uzla. Časť **Stav** na stránke **Projektová entita** zobrazuje súhrn stavov na projektovej úrovni.

## <a name="status-summary-fields"></a>Polia súhrnu stavu

Pole **Celkový stav projektu** je editovateľné pole, ktoré zobrazuje celkový stav projektu. Používa farebné kódovanie, ako je zelená, žltá a červená, na označenie rastúceho rizika. Pole **Poznámky** umožňuje správcovi projektu zadať konkrétne poznámky o stave. Pole **Stav aktualizovaný dňa** nie je možné upravovať a hodnota je časová pečiatka, ktorá indikuje, kedy bol stav naposledy aktualizovaný.

Polia **Výkonnosť plánu** a **Výkonnosť nákladov** sa nastavujú od dátumu sledovania. Keď plán a odchýlka nákladov pre koreňový uzol v zobrazení **Sledovanie úsilia** budú pozitívne, môžete nastaviť tieto polia na možnosť **Popredu**. Keď časový rozvrh a odchýlka nákladov pre koreňový uzol sú záporné, môžete ich nastaviť na možnosť **Pozadu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
