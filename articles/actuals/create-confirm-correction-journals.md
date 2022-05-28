---
title: Vytvorenie a potvrdenie účtovných denníkov opráv
description: Táto téma poskytuje informácie o tom, ako vytvoriť a potvrdiť účtovný denník opravy.
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
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582822"
---
# <a name="create-and-confirm-correction-journals"></a>Vytvorenie a potvrdenie účtovných denníkov opráv

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Občas môže byť nesprávne zadaný čas alebo výdavok. Konzultant môže napríklad vybrať nesprávny dátum pri vytváraní časového záznamu alebo môže vybrať nesprávny projekt, keď zadáva výdavok. Ak konzultant nemôže aktualizovať predložené záznamy, správca servera môže priamo opraviť skutočné skutočnosti pre projekt.

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

7. Po potvrdení denníka opráv sa vráťte k projektu alebo projektom, ktoré ste aktualizovali, aby ste videli svoje zmeny.

8. Na stránke projektu, na **Aktuálne** skontrolujte kartu **Aktuálne pridružené zobrazenie** zoznam. Uvádzajú sa pôvodné záznamy a opravené položky.


## <a name="correct-approved-material-usage-logs"></a>Opravte schválené protokoly používania materiálu

Vykonajte nasledujúce kroky na opravu jednej alebo viacerých položiek denníka použitia materiálu.

1. V **Predaj** v ľavom navigačnom paneli pod **Transakcie**, vyberte **Aktuálne**.

2. V **Aktuálne** pomocou stĺpcových filtrov vyberte **Materiál** trieda transakcie, takže sú zobrazené iba skutočné hodnoty pre materiály. Na ďalšie obmedzenie zobrazených skutočností použite iné filtre stĺpcov. Keď nájdete požadovanú množinu skutočných hodnôt, vyberte aktuálne hodnoty a potom vyberte **Správne zadania**. Automaticky sa vytvorí nový denník opráv a **Korekcia materiálu** je priradený typ.

3. Na **Nový denník** stránke, v **Popis** zadajte popis opravy. Potom na **Oprava materiálu** kartu, v **Nové hodnoty pre materiály** vyberte dátové polia, ktoré chcete opraviť pre vybrané materiálové rady. Môžete napríklad priradiť materiál k inému projektu alebo opraviť produkt, dátum materiálu alebo subdodávku.

4. Stlačte možnosť **Ukážka**. Potom v dialógovom okne vyberte **OK**.

5. Na **Riadky denníka** skontrolujte opravy. Môžete zobraziť zoznam pôvodných skutočností, ktoré súvisia s vybratými položkami materiálu, ktoré boli stornované, a opravenými zodpovedajúcimi riadkami, ktoré boli vytvorené.

6. Ak sú opravené hodnoty podľa očakávania, vyberte položku **Potvrdiť**. Potom v dialógovom okne vyberte **OK**. Ak hodnoty nie sú podľa očakávania, vyberte **Zrušiť** vrátiť sa do **Aktuálne** zoznam. Potom zopakujte kroky 2 až 5.

7. Po potvrdení denníka opráv sa vráťte k projektu alebo projektom, ktoré ste aktualizovali, aby ste videli svoje zmeny.

8. Na stránke projektu, na **Aktuálne** skontrolujte kartu **Aktuálne pridružené zobrazenie** zoznam. Uvádzajú sa pôvodné záznamy a opravené položky.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
