---
title: Vytvorenie a potvrdenie účtovných denníkov opráv
description: Táto téma poskytuje informácie o tom, ako vytvoriť a potvrdiť účtovný denník opravy.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8ca35d1e66cbacaf65b7cd43493e3588f213788e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276952"
---
# <a name="create-and-confirm-correction-journals"></a>Vytvorenie a potvrdenie účtovných denníkov opráv

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Príležitostne môže byť nesprávne zadaný údaj o čase alebo výdavkoch. Napríklad poradca môže zvoliť nesprávny dátum pri vytváraní časového záznamu alebo môže transponovať čísla pri zadávaní výdavkov. Ak konzultant nemôže vykonať aktualizácie predložených záznamov, správca môže priamo opraviť záznam pre projekt.

Na dokončenie postupov v tejto téme budete potrebovať oprávnenia správcu.

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

Napríklad na nasledujúcej grafike sú dve riadkové položky s množstvom 8,00, ktorých debety sú uvedené v stĺpci Suma. Ďalej sú v stĺpci Suma dve riadkové položky s množstvom -8,00, ktoré zobrazujú pripísané sumy. Tieto korekcie znižujú množstvo na nulu.

 
## <a name="correct-approved-expense-entries"></a>Opravte schválené záznamy výdavkov

Ak chcete opraviť jednu alebo viac položiek výdavkov, vykonajte nasledujúce kroky. 

1. V oblasti **Sales** v ľavej navigačnej table v časti **Transakcie** zvoľte možnosť **Schválené výdavky**.

2. V zozname **Schválené výdavky** zvoľte projekt, ktorý chcete opraviť, a potom stlačte možnosť **Opraviť záznamy**. Automaticky sa vytvorí nový denník korekcií s priradeným typom **Oprava výdavku**. 

3. Na stránke **Nový denník** zadajte **Opis** opravy a na karte **Oprava výdavku** v sekcii **Nové hodnoty pre výdavky** zvoľte dátové polia, ktoré chcete pri vybratých riadkoch nákladov opraviť. Napríklad môžete priradiť náklady inému **Projektu** alebo opraviť **Kategória výdavku**, **Dátum výdavku** alebo **Rezervovateľný zdroj**.

4. Stlačte možnosť **Ukážka**. V dialógovom okne stlačte možnosť **OK**. 

5. Skontrolujte opravy na karte **Záznamy v účtovnom denníku**. Môžete si zobraziť zoznam pôvodných skutočností, ktoré súvisia s vybratými výdavkovými položkami, ktoré boli zmenené, a opravené zodpovedajúce riadky, ktoré boli vytvorené.

6. Ak sú opravené hodnoty podľa očakávania, vyberte položku **Potvrdiť**. V dialógovom okne stlačte možnosť **OK**. Ak sa hodnoty nezobrazujú podľa očakávania, vyberte položku **Zrušiť**, čím sa vrátite do zoznamu **Schválené výdavky**. Opakujte kroky 2 až 5. 

> [!NOTE]
> Opravené skutočné hodnoty budú mať rovnaké hodnoty, aké ste vybrali v sekcii **Nové hodnoty pre výdavky**.

7. Po potvrdení denníka opráv prejdite späť na projekt alebo projekty, ktoré ste aktualizovali, aby ste si prezreli zmeny.  

8. Na stránke projektu na karte **Skutočné hodnoty** skontrolujte **Priradené zobrazenie skutočných hodnôt**. Uvádzajú sa pôvodné záznamy a opravené položky. Nasledujúca grafika zobrazuje pôvodné sumy vstupných nákladov a zodpovedajúce opravené položky vstupných nákladov. 




[!INCLUDE[footer-include](../includes/footer-banner.md)]