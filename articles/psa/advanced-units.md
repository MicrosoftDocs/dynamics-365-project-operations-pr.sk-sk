---
title: Jednotkové skupiny a jednotky
description: Tento článok poskytuje informácie o skupinách a jednotkách jednotiek.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ed413cc927901308a111263dbad1a59af8fce620
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933419"
---
# <a name="unit-groups-and-units"></a>Jednotkové skupiny a jednotky

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Jednotkové skupiny a jednotky sú základnými entitami v Microsoft Dynamics 365. Jednotka je jediná merná jednotka a viacero jednotiek je možné zoskupiť do skupín jednotiek. Jednotková skupina sa niekedy označuje ako jednotkový plán v používateľskom rozhraní Dynamics 365 (UI). 

Tu je niekoľko príkladov jednotiek a jednotkových skupín:
 
- **Unit group**: Vzdialenosť 
    - **Units**: Míle, Kilometer, a tak ďalej.
- **Unit group**: Čas
    - **Units**: Hodina, deň, týždeň, a tak ďalej. 

Keď nastavíte viacero jednotiek v jednotkovej skupine, musíte nastaviť tiež konverzný faktor medzi nimi určovaním prvej jednotky, ktorú nastavíte ako predvolenú alebo primárnu jednotku pre jednotkovú skupinu. 

Na príklad, ak v jednotkovej skupine **Time** nastavíte **Hour** ako prvú jednotku, systém určí **Hour** ako predvolenú jednotku. Ak je ďalšia jednotka, ktorú nastavíte, **Day**, musíte nastaviť konverzný faktor **Day** na **Hour**. Ak potom pridáte **Week** ako tretiu jednotku, musíte nastaviť konverzný faktor pre **Week**, pokiaľ ide o **Day** alebo **Hour**. 

Nasledujúci obrázok zobrazuje príklad nastavenia pre jednotku **Day**, kde pole **Quantity** zobrazuje počet hodín, ktoré sú v dni a **Week**, kde pole **Quantity** zobrazuje počet dní, ktoré sú v týždni.

> ![Jednotková skupina: informačná stránka.](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Používanie jednotiek a jednotkových skupín

Dynamics 365 Project Service Automation používa jednotky a jednotkové skupiny na spracovanie odhadov a položiek pre výdavky aj čas. 

V prípade výdavkov má každá kategória výdavkov predvolenú jednotkovú skupinu a jednotku. Tieto hodnoty sa zadajú ako predvolené hodnoty položiek cenníka pre kategórie výdavkov. 

Napríklad máte kategóriu výdavku ktorá sa nazýva **Mileage**. Má jednotkovú skupinu, ktorá je pomenovaná **Distance** a predvolenú jednotku, ktorá sa nazýva **Mile**. Ak nastavíte **Distance** jednotkovú skupinu tak, aby mala dve jednotky (**Mile** a **Kilometer**), môžete nastaviť dve ceny pre kategóriu **Mileage** v jednom cenníku: cena za míľu a cena za kilometer.

| Kategória výdavku  | Jednotková skupina  | Jednotka      | Spôsob oceňovania  | Cena za jednotku  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Cestovné           | Vzdialenosť      | Míľa      | Cena za jednotku    | 10 USD            |
| Cestovné           | Vzdialenosť      | Kilometer | Cena za jednotku    |  6 USD            |

Keď zadáte výdavky na projekte, systém určuje cenu prostredníctvom kombinácie kategórie a jednotky na výdavku. 

| Popis výdavku        | Kategória výdavku  | Jednotka  | Množstvo  | Jednotková cena   |
|----------------------------|---------------------|-------|-----------|----------------|
| Jazda ku klientovi | Cestovné             | Míľa  | 10        | 10 USD         |

Pre čas, má každá hlavička cenníka pole **Default Time Unit**. Hodnota sa nastaví pri vytváraní hlavičky cenníka. Táto jednotka sa potom použije na nastavenie všetkých cien založených na roli v tomto cenníku.

Odhadované riadky pre pole **Time on Quote** možno vyjadriť v ktorejkoľvek časovej jednotke. Avšak, odhadované riadky na projektoch a časových záznamoch v projektoch však môže používať len **Hour** jednotku času. Ak jednotka v zázname času alebo riadok odhadu nezodpovedá jednotke v riadku cenníka pre túto rolu, systém skonvertuje cenu na jednotky, ktoré sú definované v projektovom odhade alebo v skutočnej transakcii projektu.

Nasledujúci príklad ukazuje, ako PSA používa jednotkové skupiny, jednotky a konverzné faktory.
- Jednotky

   - **Unit group**: Čas 
   - **Units**: Hodina 
    
    - **Day** - Konverzný faktor: 8 hodín       
    - **Week** - Konverzný faktor: 40 hodín  
        
- Nastavenie cenníka v Projekte A:

    - **Name**: UK predajné ceny 2016 
    - **Default time unit**: Deň 
    - **Mena**: GBP

| Rola      | Jednotková skupina | Jednotka | Organizačná jednotka | Cena   |
|-----------|------------|------|---------------------|---------|
| Vývojár | Time       | Day  | Blaho UK          | 800 GBP |

### <a name="time-entry"></a>Zadanie času

Nasledujúca tabuľka zobrazuje výslednú transakciu na strane predaja vytvorenú spoločnosťou PSA pre trojhodinový projekt.


| Projekt   | Úloha    | Rola      | Množstvo | Jednotka  | Jednotková cena | Suma nevyfakturovaného predaja |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projekt A | Navrhnúť  | Vývojár | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>FAQ časových jednotiek

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Konvertuje PSA na rôzne jednotky v prípade výdavkov?
Nie. Konverzia jednotky funguje len pre čas. Pre výdavky, ak systém nemôže nájsť cenu pre kombináciu výdavkovej kategórie a jednotky, cena je nastavená na 0,00 predvolene.

### <a name="why-does-psa-convert-time-units"></a>Prečo PSA konvertuje časové jednotky?
V niektorých krajinách alebo regiónoch existuje zákonná požiadavka, aby sa fakturačné sadzby stanovili v dňoch. Cenové vyjednávanie a poskytovanie zliav počas cyklu cenovej ponuky sa vykonáva pomocou dennej sadzby pre každú fakturovateľnú rolu. Harmonogram odhadu a záznam času sa vykonáva v hodinách. Na podporu tohto rozdielu v časových jednotkách, PSA konvertuje časové jednotky.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Je možné zmeniť časové jednotky na odhady projektu?
Nie. Odhad plánu je momentálne obmedzený na hodiny a nedá sa zmeniť.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Môžu byť jednotky a jednotkové skupiny upravené, vymazané a pridané?
Áno. S výnimkou **Time** jednotkových skupín a **Hour** jednotky je možné všetky jednotky odstrániť alebo upraviť a pridať nové jednotky. V PSA nie je možné **Time** jednotkovú skupinu a **Hour** jednotku odstrániť. Avšak môžu byť aktualizované s preloženým textom pre pole **Name**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
