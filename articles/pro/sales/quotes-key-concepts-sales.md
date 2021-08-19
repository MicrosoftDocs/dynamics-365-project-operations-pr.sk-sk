---
title: Cenové ponuky – Kľúčové koncepty – čiastočné
description: Táto téma poskytuje informácie o používaní projektových cenových ponúk v Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 279e7dd47d3d61b02227b307a5833ca0bac66f4a774b5ff23cb69aac417e2f0e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009460"
---
# <a name="concepts-unique-to-project-quotes"></a>Koncepty jedinečné pre projektové cenové ponuky

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_


Nasledujú kľúčové koncepty, ktoré si musíte uvedomiť predtým, ako začnete používať cenové ponuky projektu v Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Zmluvná jednotka

Zmluvná jednotka predstavuje divíziu alebo prax, ktorá vlastní dodávku projektu. Pre každú zmluvnú jednotku môžete nastaviť náklady na zdroj. Keď zadáte náklady na zdroj pre zdroj v zmluvnej jednotke, budete tiež môcť nastaviť rôzne nákladové sadzby pre zdroje, z ktorej čerpá táto zmluvná jednotka alebo inú divíziu alebo postup v rámci podniku. Vzťahujú sa na prevodné ceny, čerpanie zdroja alebo výmenné ceny. Keď nastavujete náklady na čerpanie zdrojov z iných divízií, môžete si zvoliť aj nastavenie týchto sadzieb nákladov v mene požičiavajúcej divízie.

## <a name="cost-currency"></a>Mena nákladov

Mena nákladov v Project Operations je mena, v ktorej sa vykazujú náklady. Táto mena je odvodená od meny pripojenej k poľu **Zmluvná jednotka** pre cenovú ponuku, zmluvu a projekt. Náklady je možné prihlásiť v akejkoľvek mene oproti projektu. Existuje však prevod meny z meny, v ktorej boli zaznamenané náklady, do meny nákladov na projekt.

Keďže výmenné kurzy v platforme CDS nemôžu byť účinné, celkové ceny na obrazovke sa môžu časom meniť, ak aktualizujete výmenné menové kurzy. Náklady zaznamenané v databáze však zostávajú nezmenené, pretože sumy sa ukladajú v mene, v ktorej sa započítali.

## <a name="sales-currency"></a>Mena predaja

Mena predaja v rámci Project Operations je mena, v ktorej sú zaznamenané a zobrazené odhadované a skutočné sumy predaja. Je to tiež mena, v ktorej je zákazníkovi vystavená faktúra pre obchod. V projektovej cenovej ponuke je predvolená mena predaja zo záznamu zákazníka alebo obchodného vzťahu a pri vytvorení cenovej ponuky je možné ju zmeniť. Po uložení cenovej ponuky nie je možné zmeniť menu predaja. Cenníky produktov a projektov sú predvolene založené na predajnej mene cenovej ponuky.

Na rozdiel od nákladov je možné hodnoty predaja zaznamenať iba v mene predaja.

## <a name="billing-method"></a>Spôsob fakturácie

Projekty majú zvyčajne zmluvné modely založené na pevných poplatkoch a spotrebe. Je zastúpené v Project Operations ako **Spôsob fakturácie** a má dve hodnoty, čas a materiál a pevnú cenu.

- **Čas a materiál:** Toto je zmluvný model založený na spotrebe, kde sú všetky vzniknuté náklady kryté zodpovedajúcimi výnosmi. Keď odhadnete alebo vzniknú ďalšie náklady, zvýši sa aj zodpovedajúci odhadovaný a skutočný predaj. Môžete určiť nepresahujúce limity riadkov cenových ponúk, ktoré majú tento spôsob fakturácie. Tým sa zhora ohraničí skutočný výnos. Nepresahujúce limity neovplyvnia odhadované výnosy.
- **Pevná cena:** Toto je model zmluvy s pevným poplatkom, ktorý naznačuje, že hodnoty predaja budú nezávislé od vzniknutých nákladov. Hodnota predaja je nemenná a nemení sa podľa vašich odhadov ani nespôsobuje vyššie náklady.

## <a name="project-price-lists"></a>Projektové cenníky

Cenníky projektu sú cenníky, ktoré sa používajú pri predvolených cenách, nie pri cenových sadzbách, čase, výdavkoch a ďalších komponentoch súvisiacich s projektom. Cenníkov môže byť viac a každý zoznam môže mať svoju vlastnú dátumovú účinnosť pre každú cenovú ponuku projektu. Prekrývajúci sa dátum účinnosti v projektových cenníkoch nie je podporovaný v Project Operations.

## <a name="product-price-lists"></a>Cenníky produktov

Cenníky produktov sú cenníky, ktoré sa používajú pri predvolených cenách, nie pri cenových sadzbách, pre riadky v cenovej ponuke založené na produkte. Pre jednu cenovú ponuku je k dispozícii iba jeden cenník produktov.

## <a name="transaction-classes"></a>Triedy transakcií

Project Operations podporuje štyri typy tried transakcií:

- Čas
- Výdavok
- Materiál
- Poplatok

Hodnoty nákladov a predajov možno odhadnúť a môžu vzniknúť v triedach transakcií Čas, Výdavky a Materiál. Poplatok je triedou transakcií iba s výnosmi.

## <a name="work-entities-and-billing-entities"></a>Pracovné entity a fakturačné entity

Entity, ktoré zastupujú prácu, sú Projekty a Úlohy. Entity, ktoré zastupujú fakturáciu, sú riadky cenovej ponuky a riadky zmluvy. Rôzne pracovné entity môžete prepojiť s možnosťami fakturácie tak, že ich priradíte k riadkom cenovej ponuky alebo zmluvy.

## <a name="multi-customer-deals"></a>Dohody s viacerými zákazníkmi

K dohodám s viacerými zákazníkmi dochádza, keď sa má fakturovať viac ako jeden zákazník. Medzi bežné príklady patrí:

- **Podniky OEM a ich partneri:** Partneri a predajcovia predávajú produkt so službami s pridanou hodnotou. Toto je zvyčajne scenár, keď počas konkrétnej dohody so zákazníkom ponúka výrobca OEM financovanie časti projektu. 

- **Projekty verejného sektora:** Viaceré oddelenia miestnej vládnej organizácie súhlasia s financovaním projektu a fakturujú sa podľa vopred dohodnutého rozdelenia. Napríklad školský obvod a úrad mesta alebo vládnej organizácie súhlasia s financovaním stavby kúpaliska.

## <a name="invoice-schedules"></a>Plány faktúry

Plány faktúr sú špecifické pre každý riadok cenovej ponuky a tiež sú voliteľné. Plány faktúr sa vytvárajú na základe určitých dátumov začatia a ukončenia a frekvencie faktúr. Plány faktúr sa používajú v etape zmluvy, keď je nakonfigurovaný proces automatického vytvárania faktúr. V etape cenovej ponuky sú plány voliteľné. Keď sa vytvárajú plány faktúr v etape **Cenová ponuka**, skopírujú sa do zmluvy projektu, ktorá sa vytvorí po získaní cenovej ponuky projektu.

## <a name="changes-from-dynamics-365-sales-quote"></a>Zmeny oproti cenovej ponuke Dynamics 365 Sales:

Cenové ponuky Project Operations sú postavené na cenových ponukách Dynamics 365 Sales. Mali by ste si však uvedomiť niekoľko dôležitých rozdielov vo funkčnosti:

- Akcie **Revidovať** a **Aktivovať** nie sú podporované.
- Cenové ponuky v Project Operations majú dva rôzne typy riadkov. Jeden je pre projekty a druhý pre produkty.
- Cenové ponuky v Project Operations majú svoj vlastný formulár a prvky používateľského rozhrania, obchodné pravidlá, obchodnú logiku v doplnkoch a skripty na strane klienta, vďaka ktorým sú oproti cenovým ponukám v Sales jedinečné.

Z týchto dôvodov sa neodporúča používať striedavo cenové ponuky v Sales a cenové ponuky v Project Operations.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
