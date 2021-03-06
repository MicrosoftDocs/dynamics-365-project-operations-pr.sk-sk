---
title: Vrátenie DPH v správe výdavkov
description: Táto téma vysvetľuje, ako prijímať vrátené platby za oprávnené transakcie s daňou z pridanej hodnoty (DPH).
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 2c20e4a7fa9748e03bf1729fc2f7bdbfc2f292d1
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908584"
---
# <a name="vat-recovery-in-expense-management"></a>Vrátenie DPH v správe výdavkov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Aby spoločnosť alebo organizácia mohla dostávať vrátené platby za oprávnené transakcie s daňou z pridanej hodnoty (DPH), musí identifikovať, zhromažďovať, overovať a poskytovať presné informácie. Tento proces zahŕňa viac úloh a v závislosti od veľkosti vašej spoločnosti môže zahŕňať niekoľko zamestnancov alebo rolí.

Na vrátenie DPH v module **Správa výdavkov** musia byť splnené nasledujúce predpoklady:

- Je potrebné vytvoriť daňové kódy pre krajiny/regióny, ktoré sú priradené ku kategóriám výdavkov.
- Pre každý kód dane musí byť vytvorená skupina dane z predaja.
- Pre každú skupinu dane z predaja musí byť vytvorený kód dane z predaja.

Po splnení nevyhnutných predpokladov je potrebné vykonať nasledujúce kroky, aby ste mohli požiadať o vrátenie platby za transakcie s DPH.

1. V prehľade výdavkov zadajte daňové informácie o transakciách kreditnou kartou, aby ste identifikovali oprávnené vrátenia DPH.
2. Skontrolujte, či sú všetky daňové informácie úplné, a potom odošlite výkaz výdavkov.
3. Spracujte výdavky, ktoré sú oprávnené na medzinárodné vrátenie DPH.
4. Zašlite údaje o vrátení DPH dodávateľovi tretej strany na podanie medzinárodnej žiadosti o vrátenie.
5. Spracujte výdavky na tuzemské vrátenie DPH.

Nasledujúce časti poskytujú príklady, ktoré znázorňujú, ako zamestnanci spoločnosti Contoso vykonávajú každý krok.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Zadajte daňové informácie o transakciách kreditnou kartou, aby ste identifikovali oprávnené vrátenia DPH

Nancy, obchodná zástupkyňa spoločnosti Contoso, ktorá má sídlo v Spojených štátoch, sa nedávno vrátila z predajnej cesty do Veľkej Británie. Počas cesty Nancy vznikli nejaké osobné výdavky za jedlo, ktoré uhradila kreditnou kartou. Nancy musí teraz vytvoriť výkaz výdavkov na vyrovnanie výdavkov.

Keď Nancy zadá informácie do výkazu výdavkov, vyberie **Spojené kráľovstvo** v poli **Krajina/región** na stránke **Upraviť výkaz výdavkov**. Zoznam skupín dane z predaja je potom filtrovaný tak, že zobrazuje iba skupiny, ktoré sa vzťahujú na Spojené kráľovstvo. Nancy vyberie skupinu dane z predaja **Spojené kráľovstvo 001** a potom zo vyberie položku skupiny dane z predaja **Jedlá**. Potom Nancy pridá novú transakciu pre ubytovanie. Keďže pre ubytovanie v Spojenom kráľovstve existuje iba jedna skupina dane z predaja a jedna položka zo skupiny dane z predaja, tieto informácie sa automaticky vyplnia so výkazu výdavkov pre Nancy.

Podľa pravidiel spoločnosti Contoso musia mať všetky výdavky zodpovedajúci príjmový doklad. Preto keď Nancy uloží výkaz výdavkov, dostane správu s oznámením, že musí priložiť potvrdenie o každej transakcii, ktorú uviedla vo svojom výkaze výdavkov. Nancy overí, že k svojmu výkazu výdavkov pripojila digitálny obrázok každého potvrdenia o transakcii, a potom správu predloží na schválenie. Potom pošle papierové potvrdenky spracovateľskému tímu administratívneho oddelenia. Tento tím zašle údaje o vrátení DPH dodávateľovi tretej strany, ktorý podáva medzinárodné žiadosti o vrátenie DPH pre spoločnosť Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Overte daňové informácie a zaúčtujte výkaz výdavkov

Predtým ako môže April, ako koordinátorka záväzkov pre spoločnosť Contoso, uverejniť výkaz výdavkov, musí zadať všetky chýbajúce daňové informácie. Otvorí stránku **Podrobnosti o výkaze výdavkov** a zobrazí sa schválená správa o výdavkoch Nancy. April potom otvorí výkaz výdavkov s cieľom zobraziť podrobnosti o transakciách. Vidí, že Nancy pre jednu z transakcií nezadala skupinu dane z predaja. Pretože tieto informácie nie sú poskytnuté, April nemôže zaúčtovať výkaz výdavkov. Preto sa pozrie na stránku **Daňové konfigurácie** v správe výdavkov a nájde príslušnú položku zo skupiny dane z predaja pre krajinu/región a typ transakcie. April teraz môže zaúčtovať výkaz výdavkov do hlavnej účtovnej knihy.

Keď April zaúčtuje výkaz výdavkov, vytvorí sa pracovná položka s možnosťou vrátenia DPH. Táto pracovná položka je priradená členovi spracovateľského tímu administratívneho oddelenia. April dostane správu, ktorá potvrdzuje, že bolo zaúčtovanie úspešné. Táto správa tiež uvádza počet transakcií s DPH, ktoré boli identifikované na vrátenie.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Spracujte výdavky, ktoré sú oprávnené na medzinárodné vrátenie DPH

Arnie, člen spracovateľskému tímu administratívneho oddelenia spoločnosti Contoso, je zodpovedný za overenie, či sú všetky požadované informácie pre vrátenie DPH obsiahnuté vo výkazoch výdavkov. Otvorí stránku **Vrátenie dane z výdavkov** a vyberie výkaz výdavkov, ktorý odoslala Nancy. Arnie potom overí, či sú priložené všetky požadované potvrdenky a či bola zadaná správna skupina dane z predaja a kódy dane z predaja.

Keď Arnie dostane papierové potvrdenky od Nancy, overí ich oproti digitálnym potvrdenkám a potom zmení stav výkazu výdavkov na **Pripravené na vrátenie**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Údaje o vrátení DPH odošlite dodávateľovi tretej strany

Keď je Arnie pripravený odoslať údaje z výkazu výdavkov dodávateľovi tretej strany, ktorý bude podávať žiadosť o vrátenie DPH, otvorí stránku **Vrátenie dane z výdavkov**. Odfiltruje stránku tak, aby zobrazovala iba výkazy výdavkov, ktoré sú označené ako **Pripravené na vrátenie**. Arnie potom vyberie možnosť **Súbor** &gt; **Exportovať do programu Excel**. Informácie o DPH z výkazov výdavkov sa exportujú do hárka programu Microsoft Excel. Arnie predloží tento hárok dodávateľovi tretej strany a zahrnie správu s oznámením, že papierové potvrdenky boli odoslané kuriérom.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Spracujte výdavky pre tuzemské vrátenie DPH

Arnie musí overiť, či sú transakcie výkazu výdavkov oprávnené na vrátenie DPH a či sú k výkazom pripojené digitálne potvrdenky. Aby mohol Arnie začať spracúvať oprávnené výdavky na tuzemské vrátenie, otvorí stránku **Vrátenie dane z výdavkov** a vyberie výkaz výdavkov, ktorý sa má overiť. Skontroluje, či sú potvrdenky uvedené v mene spoločnosti a nie zamestnanca. (Pre vrátenie DPH musia byť potvrdenky uvedené v mene spoločnosti.) Arnie potom overí, či bola zadaná správna skupina dane z predaja a kódy dane z predaja.

Keď Arnie dostane papierové potvrdenky, zmení stav výkazu výdavkov na **Pripravené na vrátenie**. Potom môže podať žiadosť o vrátenie na príslušnom daňovom úrade. V tomto prípade je príslušným daňovým úradom v USA Internal Revenue Service (IRS).
