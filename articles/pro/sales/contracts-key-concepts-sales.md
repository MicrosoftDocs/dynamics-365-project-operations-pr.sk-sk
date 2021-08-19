---
title: Projektové zmluvy – Kľúčové koncepty – čiastočné
description: Táto téma poskytuje informácie o kľúčových konceptoch projektových zmlúv.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a797a4fef6276f6ed008b0e58eed4c7480ba3492bcc166a362d4ff2816acf777
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991460"
---
# <a name="concepts-unique-to-project-contracts"></a>Koncepty jedinečné pre projektové zmluvy

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Táto téma poskytuje kľúčové koncepty, ktoré si musíte uvedomiť predtým, ako začnete používať projektové zmluvy v Dynamics 365 Project Operations:

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

## <a name="product-price-lists"></a>Cenníky produktov

Cenníky produktov sa používajú pri predvolených cenách, nie pri cenových sadzbách, pre riadky v zmluve založenej na produkte. Pre jednu zmluvu je k dispozícii iba jeden cenník produktov.

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

Dohody s viacerými zákazníkmi majú viac ako jedného zákazníka na fakturovanie dohody. Bežné príklady zahrňujú:

- Podniky OEM a ich partneri: Partneri a ďalší predajcovia predávajú produkt s niektorými službami s pridanou hodnotou, ktoré zvyčajne zahŕňajú konkrétny obchod so zákazníkom. OEM ponúka na financovanie časť projektu. 

- Projekty verejného sektora: Viaceré oddelenia miestnej vládnej organizácie súhlasia s financovaním projektu a fakturujú sa podľa vopred dohodnutého rozdelenia. Napríklad školský obvod a vládna organizácia súhlasia s financovaním stavby kúpaliska.

## <a name="invoice-schedules"></a>Plány faktúry

Plány faktúr sú špecifické pre každý riadok zmluvy a sú potrebné na fungovanie automatickej fakturácie. Plány faktúr sa vytvárajú na základe určitých dátumov začatia a ukončenia a frekvencie faktúr. Plány sa používajú v etape zmluvy, keď je nakonfigurovaný proces automatického vytvárania faktúr. Keď sa projektová zmluva vytvorí z cenovej ponuky, plán faktúr sa skopíruje do projektovej zmluvy z cenovej ponuky.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Zmeny oproti zmluve Dynamics 365 Sales

Zmluvy v Project Operations sú postavené na zmluvách v Dynamics 365 Sales. Mali by ste si však uvedomiť niekoľko dôležitých odchýlok a rozdielov vo funkčnosti:

- Zmluvy v Project Operations majú dva rôzne typy prepojení, jedno pre projekty a druhé pre produkty.
- Zmluvy v Project Operations majú svoj vlastný formulár a prvky používateľského rozhrania, obchodné pravidlá, obchodnú logiku v doplnkoch a skripty na strane klienta, vďaka ktorým sú oproti zmluvám v Sales jedinečné.

Z týchto dôvodov by ste nemali používať vymeniteľne predajnú zmluvu a projektovú zmluvu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
