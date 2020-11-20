---
title: Výnosy a náklady projektu
description: Táto téma poskytuje informácie o odhadovaní projektových nákladov a výnosov.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 282950c0ee21f430a2f20b21128830891c76c84a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127987"
---
# <a name="project-costs-and-revenue"></a>Výnosy a náklady projektu

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Odhady projektu poskytujú finančné náhľady pre prácu, ktorá sa odhaduje a plánuje v pláne projektu. Na karte **odhady** na stránke **projekty** sa zobrazuje vplyv nákladov a výnosov práce, ktorú plánujete. Poskytuje tiež informácie o mnohých preddefinovaných rozmeroch. 

> ![Karta odhadov](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Náklady a predajná hodnota projektu

Cenníky stanovujú cenu a sadzby fakturácie pre roly v projekte. Na základe rolí, priradených k názvu pozície a pomenovaného zdroja priradeného k úlohe, môžete určiť vplyv práce na náklady a výnosy. Ak existujú úlohy, ktoré nemajú žiadne priradenia (všeobecné alebo pomenované), nemôžete získať odhady nákladov alebo predaja. Hodnoty nákladov a predaja zohľadňujú dátum definovaný v cenníkoch.

### <a name="default-cost-price"></a>Predvolený cenník nákladov  

Každý projekt patrí do organizácie. Táto organizácia sa zobrazuje v poli **zmluvná jednotka** projektu. Cenník, ktorý je priradený k zmluvnej jednotke, sa používa na určenie obstarávacej ceny jednotky. Na určenie správnej obstarávacej ceny rolí pre dátumu definovaný v odhadovom riadku, kombináciu role, jednotky a organizačnej jednotky v cenníku nákladov. 

Aby sa mohli vypočítať ich obstarávacie ceny, všetky úlohy musia byť priradené k zdroju. Akékoľvek nepriradené úlohy budú mať obstarávaciu cenu 0,00.

Ak kombinácia roly, jednotky a organizačnej jednotky nevráti obstarávaciu cenu z cenníka zmluvnej jednotky, systém túto jednotku ignoruje. Namiesto toho vyhľadá kombináciu len roly a organizačnej jednotky. Ak sa zistí obstarávacia cena, prepočítavacie koeficienty sa použijú na jej konvertovanie na jednotku, ktorú ste vybrali v riadku odhadu.

Ak kombinácia roly a organizačnej jednotky nevráti obstarávaciu cenu z cenníka, systém túto jednotku ignoruje. Namiesto toho vyhľadá kombináciu roly a jednotky na nastavenie predvolenej ceny (po použití akejkoľvek konverzie).

Ak systém nenájde cenu pre rolu, potom bude obstarávacia cena nastavená na predvolenú hodnotu **0.00** riadku odhadu. Všetky hodnoty nákladov v riadkoch odhadov projektových nákladov sú zaznamenané v mene zmluvnej jednotky.

> [!NOTE]
> Predvolene, Microsoft Dynamics 365 ukladá hodnoty nákladov vo vašej základnej mene. Čiastky nákladov, ktoré sú uvedené na karte **odhady**, sú však v mene zmluvnej jednotky.  

### <a name="default-sales-price"></a>Predvolené predajné ceny 

Predajný cenník je určený buď predajnou entitou, ku ktorej je projekt pripojený, alebo zákazníkom projektu. Keď je predajná entita, ako napríklad príležitosť, cenová ponuka alebo zmluva, priradená k projektu, predajná cena entity predaja je určená cenníkom priradeným k cenovej ponuke alebo zmluve. Ak má cenová ponuka alebo zmluva vlastný cenník, ako predvolený predajný cenník pre odhady projektu je použitý tento predajný cenník. Ak neexistuje žiadna súvislosť s predajnými entitami, predvolený predajný cenník z parametrov sa použije ako predvolený predajný cenník projektu, ktorý je zhodný s menou zákazníka, ktorá je definovaná v projekte.

Každý riadok odhadu má zdrojovú jednotku, ktorá je spojená s ním. Zdrojová jednotka udáva organizačnú jednotku, z ktorej sú rezervované zdroje na dokončenie úlohy. Ak chcete určiť predajnú cenu priradených rolí, vyhľadajte kombináciu roly, jednotky a zdrojovej jednotky v predajnom cenníku. Ak nie sú k dispozícii žiadne priradenia k úlohe, predajná cena úlohy je 0,00.

Ak kombinácia roly, jednotky a zdrojovej jednotky nevráti predajnú cenu z predajného cenníka, systém túto jednotku ignoruje. Namiesto toho vyhľadá kombináciu len roly a zdrojovej jednotky. Ak sa nájde predajná cena, prepočítavacie koeficienty sa použijú na jej konvertovanie na jednotku, ktorú ste vybrali v riadku odhadu predaja. 

Ak kombinácia roly a zdrojovej jednotky nevráti predajnú cenu z predajného cenníka, systém túto zdrojovú jednotku ignoruje. Namiesto toho vyhľadá kombináciu roly a jednotky na nastavenie predvolenej ceny (po použití akejkoľvek konverzie).

Ak systém nenájde cenu pre rolu, potom bude predajná cena nastavená na predvolenú hodnotu **0.00** v riadku odhadu.

Karta **odhady** má zobrazenie mriežky, ktoré zobrazuje riadky odhadu. Mriežka obsahuje stĺpce pre jednotku, celkovú obstarávaciu cenu a celkovú predajnú cenu, ako je znázornené na nasledujúcom obrázku. 

> ![Zobrazenie mriežky na karte odhady](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Odhady času postupne zobrazenie projektu

Časovo delený pohľad na odhady projektov zobrazuje odhad údajov zo zobrazenia mriežky na časovej osi v časovej mierke, ktorú vyberiete. V predvolenom nastavení sa odhad údajov otáča na rozmer **rola**.

> ![Časovo delený pohľad na odhady projektu](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Pridelenie odhadu úsilia založené na režime úloh

V zobrazení časového rozloženia rozdeľte celkové úsilie, ktoré je odhadnuté pre úlohu pridelením určitých hodín úsilia na jednotku času vo vybranej časovej mierke. Režim úlohy určuje, ako sa rozdeľuje úsilie počas trvania úlohy. Dva druhy pridelenia sú **pravidelné** a **založené na pracovnej dobe**.

### <a name="work-hours-based-allocation"></a>Pridelenie založené na pracovnej dobe
 
V režime automatického plánovania úloh sa denné predvolené hodiny pre zdroje úlohy nastavujú v plnej pracovnej čase. Toto správanie platí pri prideľovaní úsilia rozdelením naprieč trvaním úloh aj v časovo delenom zobrazení. Napríklad ak odhadnete, že úlohu splní jeden zdroj v časovej mierke **deň**, snaha pridelená za deň nepresiahne počet pracovných hodín za deň stanovený v kalendári projektu. Preto pridelenie úsilia vždy zabezpečí, že zdroje sú odhadnuté tak, aby sa využívali počas celého dňa.

### <a name="even-allocation"></a>Pravidelné pridelenie

V manuálne naplánovanom režime úloh sa pracovné hodiny z kalendára projektu nepoužívajú. Namiesto toho, sa plán úlohy zakladá na vstupoch používateľa. Pre tieto úlohy nemá úsilie pridelené na jednotku času zvolenej časovej mierky žiadne limitujúce faktory. Celkové úsilie na úlohu je rovnako rozdelené a pridelené pre každú jednotku času vo zvolenej časovej mierke. Preto, režim úlohy, ktorý je definovaný na úlohe určujúcej rozdelenie úsilia, alebo pridelení úsilia k časovej jednotky v časovo rozdelených odhadoch.

## <a name="grouping-and-time-phasing-options"></a>Zoskupenie a možnosti fázovania času

Časovo rozdelené zobrazenie ukazuje rozdelenie úsilia, nákladové a predajné odhady na denných, týždenných, mesačných alebo ročných základoch. V predvolenom nastavení sa odhad údajov otáča na rozmer **rola**. Môžete však použiť možnosť **zoskupiť podľa** kontingenčného ovládacieho prvku na dve ďalšie dimenzie: **Kategória** a **zdroj.**

V zobrazení mriežky, aj v časovo delenom zobrazení môžete vybrať, ktoré polia sa zobrazia. Súčty pre každý časový blok sú zobrazené v spodnej časti projektu. Ukazujú celkové odhadované úsilie, náklady a predaje za deň, týždeň, mesiac alebo rok. Predvolená obstarávacia cena a predajná cena sú dátumovo-efektívne. Inými slovami, sa zmenia pre každý zdroj, na základe časovo delených zobrazení, ktoré ste vybrali.

## <a name="expense-estimates"></a>Odhady nákladov

Tlačidlo **pridať nový odhad výdavkov** v zobrazení mriežky umožňuje zaznamenať všetky výdavky, ktoré vznikli v projekte, ale ktoré priamo nesúvisia s prácou. Môžete zaznamenať odhady výdavkov pre konkrétnu úlohu alebo pre celý projekt. Vyberte kategórie výdavkov a predbežný dátum, kedy očakávate, že vzniknú náklady. Ak majú súvisiace cenníky nákladov a predajné cenníky predvolené ceny, (alebo sú definované percentá pre kategórie výdavkov), sú automaticky zadané do riadka odhadu keď sa vyskytne priradenie.
