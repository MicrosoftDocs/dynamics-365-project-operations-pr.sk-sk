---
title: Koncepty jedinečné pre cenové ponuky založené na projekte
description: Tento článok poskytuje informácie o ponukách projektov v spoločnosti Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824347"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Koncepty jedinečné pre cenové ponuky založené na projekte

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Skôr ako začnete používať ponuky projektov v Microsoft Dynamics 365 Project Operations, mali by ste poznať nasledujúce kľúčové pojmy.

## <a name="owning-company"></a>Vlastniaca spoločnosť

Vlastník zastupuje právnickú osobu, ktorá vlastní dodávku projektu. Zákazník na cenovej ponuke by mal byť platným zákazníkom v danej právnickej osobe vo finančných a prevádzkových aplikáciách. Mena vlastníckej spoločnosti a mena zmluvnej jednotky, ktorá je vybraná na základe projektovej ponuky, sa musia zhodovať.

## <a name="contracting-unit"></a>Zmluvná jednotka

Zmluvná jednotka predstavuje divíziu alebo prax, ktorá vlastní dodávku projektu. Pre každú zmluvnú jednotku môžete nastaviť náklady na zdroj. Keď zadáte náklady na zdroje pre zdroj v zmluvnej jednotke, môžete nastaviť rôzne nákladové sadzby pre zdroje, od ktorých si zmluvná jednotka požičiava, alebo pre iné divízie alebo postupy v podniku. Tieto nákladové sadzby sa označujú ako transferové ceny, požičiavanie zdrojov alebo výmenné ceny. Keď nastavujete náklady na požičiavanie zdrojov z iných divízií, môžete nastaviť nákladové sadzby v mene divízie požičiavania.

## <a name="cost-currency"></a>Mena nákladov

Nákladová mena v projektových operáciách je mena, v ktorej sa náklady vykazujú. Táto mena je odvodená od meny, ktorá je pripojená k poľu **Zmluvná jednotka** v ponuke, zmluve a projekte. Náklady na projekt môžu byť zaznamenané v akejkoľvek mene. Existuje však prevod meny z meny, v ktorej boli náklady zaznamenané, do meny nákladov projektu.

Keďže výmenné kurzy na platforme Dataverse  nemôžu byť platné podľa dátumu, celkové sumy nákladov na obrazovke sa môžu časom zmeniť, ak aktualizujete výmenné kurzy. Náklady, ktoré sú zaznamenané v databáze, však zostávajú nezmenené, pretože sumy sú uložené v mene, v ktorej boli vynaložené.

## <a name="sales-currency"></a>Mena predaja

Mena predaja v projektových operáciách je mena, v ktorej sa zaznamenávajú a zobrazujú odhadované a skutočné sumy predaja. Je to tiež mena, v ktorej je zákazníkovi fakturovaná transakcia. Pre cenovú ponuku projektu je predvolená predajná mena nastavená zo záznamu zákazníka alebo účtu a možno ju zmeniť pri vytvorení ponuky. Mena predaja sa však po uložení cenovej ponuky nedá zmeniť. Predvolené cenníky produktov a projektov sú nastavené na základe predajnej meny ponuky.

Na rozdiel od nákladov sa hodnoty predaja môžu zaznamenávať **iba** v mene predaja.

## <a name="billing-method"></a>Spôsob fakturácie

Projekty majú zvyčajne modely zmlúv s pevným poplatkom a na základe spotreby. V projektových operáciách je zmluvný model projektu reprezentovaný metódou fakturácie. Spôsob účtovania má dve hodnoty: čas a materiál a pevnú cenu.

- **Čas a materiál** – Model kontraktov založený na spotrebe, kde sú všetky vynaložené náklady podložené príslušnými výnosmi. Keď odhadnete alebo vzniknú ďalšie náklady, zvýši sa aj zodpovedajúci odhadovaný a skutočný predaj. Môžete určiť nepresahujúce limity riadkov cenových ponúk, ktoré majú tento spôsob fakturácie. Týmto spôsobom môžete obmedziť skutočné príjmy. Neprekročenie limitov neovplyvňuje odhadovaný výnos.
- **Pevná cena** – model kontraktu s pevným poplatkom, kde hodnoty predaja sú nezávislé od vynaložených nákladov. Hodnota predaja je nemenná a nemení sa podľa vašich odhadov ani nespôsobuje vyššie náklady.

## <a name="project-price-lists"></a>Projektové cenníky

Projektové cenníky sú cenníky, ktoré sa používajú na zadanie predvolených cien, nie nákladových sadzieb, pre čas, náklady a iné komponenty súvisiace s projektom. Cenníkov môže byť viac a každý zoznam môže mať svoju vlastnú dátumovú účinnosť pre každú cenovú ponuku projektu. Projektové operácie nepodporujú účinnosť prekrývajúcich sa dátumov pre cenníky projektov.

## <a name="product-price-lists"></a>Cenníky produktov

Cenníky produktov sú cenníky, ktoré sa používajú na zadanie predvolených cien, nie nákladových sadzieb, pre produktové rady v cenovej ponuke. Pre jednu cenovú ponuku existuje iba jeden cenník produktov.

## <a name="transaction-classes"></a>Triedy transakcií

Project Operations podporuje štyri typy tried transakcií:

- Čas
- Výdavok
- Materiál
- Poplatok

Hodnoty nákladov a predaja možno odhadnúť a vynaložiť na **Čas**, **Výdavky** a **Materiál** triedy transakcií. **Poplatok** je trieda transakcií iba s výnosmi.

## <a name="work-entities-and-billing-entities"></a>Pracovné entity a fakturačné entity

Projekty a úlohy sú entity, ktoré predstavujú prácu. Riadky cenovej ponuky a Riadky zmluvy sú entity, ktoré predstavujú fakturáciu. Rôzne pracovné entity môžete prepojiť s možnosťami fakturácie tak, že ich priradíte k riadkom ponuky alebo k riadkom zmluvy.

## <a name="multi-customer-deals"></a>Dohody s viacerými zákazníkmi

K dohodám s viacerými zákazníkmi dochádza vtedy, keď na faktúru pripadá viac ako jeden zákazník. Tu je niekoľko typických príkladov:

- **Spoločnosti výrobcov originálneho vybavenia (OEM) a ich partneri** – Partneri a predajcovia predávajú produkt, ktorý zahŕňa služby s pridanou hodnotou. Počas obchodu so zákazníkom OEM zvyčajne ponúka financovanie časti projektu.
- **Projekty verejného sektora** – Viaceré oddelenia miestnej samosprávy súhlasia s financovaním projektu a sú fakturované podľa vopred dohodnutého rozdelenia. Napríklad školský obvod a úrad mesta alebo vládnej organizácie súhlasia s financovaním stavby kúpaliska.

## <a name="invoice-schedules"></a>Plány faktúry

Plány faktúr sú špecifické pre každý riadok cenovej ponuky a sú voliteľné. Plány faktúr sa vytvárajú na základe konkrétnych dátumov začiatku a konca a frekvencie faktúr. Používajú sa vo fáze zmluvy, keď je nakonfigurovaný proces automatického vytvárania faktúr. Počas fázy cenovej ponuky sú rozvrhy faktúr voliteľné. Ak sa vytvoria počas fázy cenovej ponuky, skopírujú sa do projektovej zmluvy, ktorá sa vytvorí po získaní ponuky na projekt.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Rozdiely od cenových ponúk Dynamics 365 Sales

Cenové ponuky Project Operations sú postavené na ponukách Dynamics 365 Sales. Mali by ste si však uvedomiť niekoľko dôležitých rozdielov vo funkčnosti:

- Cenové ponuky Project Operations majú dva rôzne typy riadkov: jeden pre projekty a jeden pre produkty.
- Cenové ponuky Project Operations majú svoju vlastnú stránku a prvky používateľského rozhrania (UI), obchodné pravidlá, obchodnú logiku v zásuvných moduloch a skripty na strane klienta, ktoré ich odlišujú od predajných ponúk.
- V Predaji môžete k jednej predajnej ponuke pripojiť viacero objednávok. V prevádzke projektu môžete k cenovej ponuke projektu pripojiť iba jednu projektovú zmluvu.
- Keď vyhráte cenovú ponuku, súvisiaca príležitosť môže zostať otvorená. Po víťaznej projektovej cenovej ponuke sa uzavrie súvisiaca príležitosť.
- Predajná ponuka nezahŕňa niektoré polia a koncepty, ktoré zahŕňa ponuka projektu. Polia zahŕňajú **zmluvnú jednotku**, **Account Manager** a **faktúra na kontaktné meno**.
- Predajné ponuky a ponuky projektov sú identifikované podľa poľa množina možností–based **Typ** . Pre cenovú ponuku predaja je hodnota tohto poľa **Na základe položky**. Pre cenovú ponuku projektu je hodnota **Na základe práce**.

Kvôli týmto rozdielom neodporúčame, aby ste zamieňali ponuky Predajné a Projektové operácie.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
