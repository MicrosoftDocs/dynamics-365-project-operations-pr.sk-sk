---
title: Vytvorenie a potvrdenie účtovných denníkov opráv
description: Tento článok poskytuje informácie o tom, ako vytvoriť a potvrdiť účtovný denník opráv.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928083"
---
# <a name="create-and-confirm-correction-journals"></a>Vytvorenie a potvrdenie účtovných denníkov opráv

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Príležitostne môže byť nesprávne zadaný údaj o čase alebo výdavkoch. Napríklad poradca môže zvoliť nesprávny dátum pri vytváraní časového záznamu alebo môže vybrať nesprávny projekt pri zadávaní výdavkov. Ak konzultant nemôže vykonať aktualizácie predložených záznamov, back-end správca môže priamo opraviť skutočné hodnoty pre projekt.

## <a name="correct-approved-time-entries"></a>Opravte schválené časové záznamy     

Ak chcete opraviť jednorazové alebo viacnásobné zadania projektu, vykonajte nasledujúce kroky.

1. V oblasti **Sales** zvoľte možnosť **Transakcie** a potom stlačte možnosť **Schválený čas**. 

2. V zozname **Schválený čas** vyhľadajte a vyberte jeden alebo viac schválených záznamov času, ktoré chcete opraviť. Pomocou filtra môžete vyhľadať súvisiace položky. Môžete napríklad filtrovať ID projektu a vybrať všetky schválené časové záznamy s týmto ID projektu.

3. Zvoľte možnosť **Opraviť záznamy**. Automaticky sa vytvorí nový denník korekcií s priradeným typom **Oprava času**. Vybraté položky sa pridajú do denníka. 

4. Na stránke **Nový denník** zadajte **Trvanie** svojho denníka korekcií a potom stlačte kartu **Opravy zadaní času**.  

5. V časti **Nové hodnoty pre zadania času** aktualizujte v prípade potreby polia so správnymi informáciami. Napríklad môžete zmeniť priradený projekt alebo rezervovateľný zdroj.

6. Stlačte možnosť **Ukážka**. V dialógovom okne stlačte možnosť **OK**. Na karte **Záznamy v účtovnom denníku** si môžete zobraziť zoznam pôvodných skutočností, ktoré súvisia s vybratými časovými položkami, ktoré boli zmenené, a opravené zodpovedajúce riadky, ktoré boli vytvorené. Ak je potrebné vykonať ďalšie opravy, opakujte kroky 5 a 6. 

    > [!NOTE]
    > Všetky opravené skutočnosti budú mať rovnaké hodnoty, aké ste vybrali v sekcii **Nové hodnoty pre zadania času**.

7. Ak sa opravy zobrazia podľa očakávania, vyberte položku **Potvrdiť**. V dialógovom okne stlačte možnosť **OK**.

8. Vráťte sa do oblasti **Sales**, zvoľte možnosť **Projekty** a potom otvorte projekt, pre ktoré ste práve aktualizovali časové záznamy. 

9. Na stránke **Projekty** na karte **Skutočné údaje** si zobrazte vykonané zmeny. 

    > [!NOTE]
    > Ak karta **Skutočné údaje** nie je viditeľná, zvoľte možnosť **Súvisiace** > **Skutočné údaje**.  

10. V zozname **Priradené zobrazenie skutočných hodnôt** môžete vidieť, že pôvodné časové záznamy, ktoré boli zvrátené, sú stále uvedené, ako aj zodpovedajúce opravené časové položky. 

 
## <a name="correct-approved-expense-entries"></a>Opravte schválené záznamy výdavkov

Ak chcete opraviť jednu alebo viac položiek výdavkov, vykonajte nasledujúce kroky. 

1. V oblasti **Sales** v ľavej navigačnej table v časti **Transakcie** zvoľte možnosť **Schválené výdavky**.

2. V zozname **Schválené výdavky** zvoľte projekt, ktorý chcete opraviť, a potom stlačte možnosť **Opraviť záznamy**. Automaticky sa vytvorí nový denník korekcií s priradeným typom **Oprava výdavku**. 

3. Na stránke **Nový denník** zadajte **Opis** opravy a na karte **Oprava výdavku** v sekcii **Nové hodnoty pre výdavky** zvoľte dátové polia, ktoré chcete pri vybratých riadkoch nákladov opraviť. Napríklad môžete priradiť náklady inému **Projektu** alebo opraviť **Kategória výdavku**, **Dátum výdavku** alebo **Rezervovateľný zdroj**.

4. Stlačte možnosť **Ukážka**. V dialógovom okne stlačte možnosť **OK**. 

5. Skontrolujte opravy na karte **Záznamy v účtovnom denníku**. Môžete si zobraziť zoznam pôvodných skutočností, ktoré súvisia s vybratými výdavkovými položkami, ktoré boli zmenené, a opravené zodpovedajúce riadky, ktoré boli vytvorené.

6. Ak sú opravené hodnoty podľa očakávania, vyberte položku **Potvrdiť**. V dialógovom okne stlačte možnosť **OK**. Ak sa hodnoty nezobrazujú podľa očakávania, vyberte položku **Zrušiť**, čím sa vrátite do zoznamu **Schválené výdavky**. Opakujte kroky 2 až 5. 

7. Po potvrdení účtovného denníka opráv prejdite späť na projekt alebo projekty, ktoré ste aktualizovali, aby ste si prezreli zmeny.

8. Na stránke projektu na karte **Skutočné hodnoty** skontrolujte zoznam **Priradené zobrazenie skutočných hodnôt**. Uvádzajú sa pôvodné záznamy a opravené položky.


## <a name="correct-approved-material-usage-logs"></a>Opravte schválené denníky používania materiálu

Ak chcete opraviť jednu alebo viac položiek denníka použitia materiálu, vykonajte nasledujúce kroky.

1. V oblasti **Predaj** v ľavej navigačnej table v časti **Transakcie** zvoľte možnosť **Skutočné hodnoty**.

2. V zozname **Skutočné hodnoty** použite stĺpcové filtre na výber triedy transakcie **Materiál**,aby sa zobrazili len skutočné hodnoty pre materiály. Na ďalšie obmedzenie zobrazených skutočných hodnôt použite iné filtre stĺpcov. Keď nájdete požadovanú množinu skutočných hodnôt, vyberte skutočné hodnoty a potom vyberte **Opraviť záznamy**. Automaticky sa vytvorí nový denník opráv s priradeným typom **Oprava materiálu**.

3. Na stránke **Nový denník** v poli **Popis** zadajte popis denníka opráv. Potom na karte **Oprava materiálu** v sekcii **Nové hodnoty pre materiály** vyberte údajové polia, ktoré chcete opraviť pre vybrané riadky materiálov. Môžete napríklad priradiť materiál k inému projektu alebo opraviť produkt, dátum materiálu alebo subdodávateľskú zmluvu.

4. Stlačte možnosť **Ukážka**. V dialógovom okne potom kliknite na **OK**.

5. Na karte **Záznamy v účtovnom denníku** skontrolujte opravy. Môžete zobraziť zoznam pôvodných skutočných hodnôt, ktoré súvisia s vybratými položkami materiálov, ktoré boli zmenené, a opravené zodpovedajúce riadky, ktoré boli vytvorené.

6. Ak sú opravené hodnoty podľa očakávania, vyberte položku **Potvrdiť**. V dialógovom okne potom kliknite na **OK**. Ak hodnoty nie sú podľa očakávania, vyberte položku **Zrušiť**, čím sa vrátite do zoznamu **Skutočné hodnoty**. Potom opakujte kroky 2 až 5.

7. Po potvrdení účtovného denníka opráv prejdite späť na projekt alebo projekty, ktoré ste aktualizovali, aby ste si prezreli zmeny.

8. Na stránke projektu na karte **Skutočné hodnoty** skontrolujte zoznam **Priradené zobrazenie skutočných hodnôt**. Uvádzajú sa pôvodné záznamy a opravené položky.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
