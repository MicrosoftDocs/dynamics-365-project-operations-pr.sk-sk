---
title: Projektové zmluvy – Kľúčové koncepty
description: Táto téma poskytuje informácie o kľúčových konceptoch projektových zmlúv v aplikácii Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa00bd5b4a1179f38d5dfb63a47b39eec69c6ecf
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642157"
---
# <a name="project-contracts---key-concepts"></a>Projektové zmluvy – Kľúčové koncepty

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Táto téma poskytuje kľúčové koncepty, ktoré si musíte uvedomiť predtým, ako začnete používať projektové zmluvy v Dynamics 365 Project Operations:

## <a name="owning-company"></a>Vlastniaca spoločnosť

Vlastniaca spoločnosť je právnická entita z modulu **Projektové riadenie a účtovníctvo** pre Project Operations z Dynamics 365 Finance. Vlastniaca spoločnosť predstavuje právnickú entitu, ktorá bude obchodným vzťahom pre náklady a výnosy, ktoré vzniknú z obchodu.

## <a name="contracting-unit"></a>Zmluvná jednotka

Zmluvná jednotka predstavuje divíziu alebo prax, ktorá vlastní dodávku projektu. Pre každú zmluvnú jednotku môžete nastaviť náklady na zdroj. Keď zadáte náklady na zdroj pre daný zdroj, budete môcť nastaviť aj rôzne nákladové sadzby pre zdroje. Táto zmluvná jednotka tieto zdroje čerpá od iných divízií alebo postupov v rámci podniku. Nákladové sadzby na zdroje sa vzťahujú na prevodné ceny, čerpanie zdroja alebo výmenné ceny. Keď nastavujete nákladové sadzby na čerpanie zdrojov z iných divízií, použite menu požičiavajúcej divízie.

## <a name="cost-currency"></a>Mena nákladov

Mena nákladov je mena, v ktorej sa náklady zobrazujú na obrazovke. Táto mena je odvodená od meny pripojenej k poľu **Zmluvná jednotka** pre zmluvu a projekt. Náklady je možné prihlásiť v akejkoľvek mene oproti projektu. Existuje však prevod meny z meny, v ktorej boli zaznamenané náklady, do meny nákladov na projekt pri zobrazení na obrazovke.

Keďže výmenné kurzy v platforme Common Data Service (CDS) nemôžu byť účinné k dátumu, celkové ceny na obrazovke sa môžu časom meniť, ak aktualizujete výmenné menové kurzy. Náklady zaznamenané v databáze však zostávajú nezmenené, pretože sumy sa ukladajú v mene, v ktorej sa započítali.

## <a name="sales-currency"></a>Mena predaja

Mena predaja v rámci Project Operations je mena, v ktorej sú zaznamenané a zobrazené odhadované a skutočné sumy predaja. Mena predaja je tiež mena, v ktorej je zákazníkovi vystavená faktúra pre obchod. V projektovej zmluve je predvolená mena predaja zo záznamu zákazníka alebo obchodného vzťahu a pri vytvorení zmluvy je možné ju zmeniť. Keď je zmluva vytvorená uzavretím cenovej ponuky pri jej získaní, mena v zmluve sa predvolene nastaví podľa meny v cenovej ponuke.

Keď vytvoríte projektovú zmluvu od začiatku, pole **Mena predaja** nie je možné upraviť. Cenníky produktov a projektov sú predvolene založené na tejto mene v zmluve.

Na rozdiel od nákladov je možné hodnoty predaja zaznamenať iba v mene predaja.

## <a name="billing-method"></a>Spôsob fakturácie

Spravidla existujú dva typy modelov uzatvárania zmlúv pre projekty, pevný poplatok a založené na spotrebe. Tieto modely sú v Project Operations zastúpené ako spôsoby fakturácie s dvoma možnými hodnotami:

- Čas a materiál: Zmluvný model založený na spotrebe, kde sú všetky vzniknuté náklady kryté zodpovedajúcimi výnosmi. Keď odhadnete alebo vzniknú ďalšie náklady, zvýši sa aj zodpovedajúci odhadovaný a skutočný predaj. Do riadkov zmluvy zadajte limity, ktoré sa nesmú prekročiť, ktoré majú tento spôsob fakturácie, ktorý obmedzuje skutočné výnosy. Nepresahujúce limity neovplyvnia odhadované výnosy.
- Pevná cena: Model zmluvy s pevným poplatkom, ktorý naznačuje, že hodnoty predaja budú nezávislé od vzniknutých nákladov. Hodnota predaja je nemenná a nemení sa podľa vašich odhadov ani nespôsobuje vyššie náklady.

## <a name="project-price-lists"></a>Projektové cenníky

Cenníky projektu sa používajú pri predvolených cenách, nie pri cenových sadzbách, čase, výdavkoch a ďalších komponentoch súvisiacich s projektom. Cenníkov môže byť viac. Každý cenník má svoju vlastnú účinnosť podľa dátumu pre každú projektovú zmluvu. Prekrývajúci sa dátum účinnosti v projektových cenníkoch nie je podporovaný v Project Operations.

Keď sa vytvorí projektová zmluva získaním ponuky projektu, skopírujú sa cenníky projektu s uvedením názvu a dátumu zmluvy. Kopírovanie týchto informácií predstavuje vlastné ceny pre komponenty projektu uvedené v tejto zmluve o projekte.

## <a name="transaction-classes"></a>Triedy transakcií

Project Operations podporuje štyri typy tried transakcií:

- Čas
- Výdavok
- Materiál
- Poplatok

Hodnoty nákladov a predajov možno odhadnúť a môžu vzniknúť v triedach transakcií Čas, Výdavky a Materiál. Poplatok je triedou transakcie iba s výnosmi.

## <a name="work-entities-and-billing-entities"></a>Pracovné entity a fakturačné entity

Entity, ktoré zastupujú prácu, sú projekty a úlohy. Entity, ktoré zastupujú aspekty fakturácie, sú riadky zmluvy. Rôzne pracovné entity môžete previazať s možnosťami fakturácie tak, že ich previažete s riadkami zmluvy.

## <a name="multi-customer-deals"></a>Dohody s viacerými zákazníkmi

Dohody s viacerými zákazníkmi majú viac ako jedného zákazníka na fakturovanie dohody. Medzi bežné príklady patrí:

- Podniky OEM a ich partneri: Partneri a ďalší predajcovia predávajú produkt s niektorými službami s pridanou hodnotou, ktoré zvyčajne zahŕňajú konkrétny obchod so zákazníkom. OEM ponúka na financovanie časť projektu. 

- Projekty verejného sektora: Viaceré oddelenia miestnej vládnej organizácie súhlasia s financovaním projektu a fakturujú sa podľa vopred dohodnutého rozdelenia. Napríklad školský obvod a vládna organizácia súhlasia s financovaním stavby kúpaliska.

## <a name="invoice-schedules"></a>Plány faktúry

Plány faktúr sú špecifické pre každý riadok zmluvy a sú potrebné na fungovanie automatickej fakturácie. Plány faktúr sa vytvárajú na základe určitých dátumov začatia a ukončenia a frekvencie faktúr. Plány sa používajú v etape zmluvy, keď je nakonfigurovaný proces automatického vytvárania faktúr. Keď sa projektová zmluva vytvorí z cenovej ponuky, plán faktúr sa skopíruje do projektovej zmluvy z cenovej ponuky.

## <a name="changes-from-dynamics-365-sales-orders"></a>Zmeny oproti objednávkam Dynamics 365 Sales

Zmluvy v Project Operations sú postavené na objednávkach v Dynamics 365 Sales. Existujú však dôležité odchýlky a rozdiely vo funkčnosti. Zmluvy majú svoj vlastný formulár a prvky používateľského rozhrania, obchodné pravidlá, obchodnú logiku v doplnkoch a skripty na strane klienta, vďaka ktorým sú oproti objednávkam jedinečné. Z týchto dôvodov nepoužívajte vymeniteľne predajnú objednávku a zmluvu Project Operations.
