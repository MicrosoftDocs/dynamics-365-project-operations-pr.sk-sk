---
title: Spracovanie potvrdenia výdavkov
description: Táto téma poskytuje informácie o spracovaní účteniek optickým rozpoznávaním znakov (OCR). Táto funkcia je navrhnutá tak, aby zlepšila používateľskú skúsenosť pri vytváraní výkazov výdavkov v Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993525"
---
# <a name="expense-receipt-processing"></a>Spracovanie potvrdenia výdavkov

Zadávanie výdavkov bolo vylepšený zavedením spracovaním účteniek optickým rozpoznávaním znakov (OCR). Táto funkcia je navrhnutá tak, aby zlepšila používateľskú skúsenosť pri vytváraní výkazov výdavkov.

## <a name="key-features"></a>Kľúčové funkcie

- Z účtenky sa vyberie meno obchodníka, dátum a celková suma.
- Funkcia sa pokúsi priradiť nepripojené účtenky k nepripojeným transakciám výdavkov.
- Z účteniek môžu používatelia vytvoriť ručne zadané transakcie výdavkov.

## <a name="usage-examples"></a>Príklady použitia

Ak chcete pri vytváraní výkazu výdavkov automaticky pripojiť účtenky, ktoré zahŕňajú transakcie kreditnou kartou, postupujte nasledovne:

  1. Otvorte pracovný priestor **Správa výdavkov**.
  2. Na karte **Účtenky** overte, či existujú nepripojené účtenky. Môžete tiež nahrať účtenky na karte **Účtenky**.
  3. Na karte **Výdavky** overte, či existujú nepripojené výdavky. Spravidla tieto výdavky importuje správca výdavkov od vydavateľa kreditnej karty.
  4. Vyberte **Nový výkaz výdavkov**. Upozorňujeme, že pri vytváraní výkazu výdavkov môžete zahrnúť ako výdavky, tak aj účtenky. Ak pridáte výdavky aj účtenky, spustí sa automatické priraďovanie účteniek k výdavkom.

Ak chcete vytvoriť výdavok alebo spárovať výdavok z účtenky, postupujte nasledovne:

  1. Vo výkaze výdavkov, na karte **Príjmy**, pripojte účtenku výberom možnosti **Pridať účtenky**.
  2. Pod nahraným obrázkom účtenky si všimnite možnosti **Vytvoriť** a **Spárovať**.

      - Vyberte **Vytvoriť** na vytvorenie ručne zadanej výdavkovej transakcie a vyplnenie hodnôt, ktoré sú načítané z účtenky.
      - Ak vyberiete **Spárovať**, systém sa pokúsi spárovať existujúci výdavok s účtenkou.

## <a name="installation"></a>Inštalácia

Táto funkcia funguje v kombinácii s funkciou **Prepracované výkazy výdavkov**, ktorá pomáha zjednodušiť skúsenosti s výdavkami. Táto funkcia je k dispozícii iba pre prostredia Tier 2+, ktorými sú Sandbox a Production.

Ak chcete používať tieto pokročilé možnosti výdavkov, nainštalujte si doplnok Služba riadenia výdavkov pre Microsoft Dynamics 365 Finance a zapnite funkcie vo vašej inštancii. V Microsoft Dynamics Lifecycle Services (LCS) môžete pristupovať k doplnku z vášho projektu.

1. Prihláste sa do LCS a otvorte požadované prostredie.
2. Prejdite do časti **Všetky podrobnosti**.
3. Vyberte **Údržba** alebo prejdite nadol na rýchlu kartu **Doplnky prostredia**.
4. Vyberte **Nainštalovať nový doplnok**.
5. Vyberte **Služba riadenia výdavkov**.
6. Postupujte podľa inštalačnej príručky a vyjadrite súhlas s obchodnými podmienkami.
7. Vyberte **Nainštalovať**.

V pracovnom priestore **Správa funkcií** zapnite nasledujúce funkcie:

- Prepracované výkazy výdavkov
- Automatické párovanie a vytváranie výdavkov z účtenky

Po zapnutí týchto funkcií prebehnú nasledujúce akcie:

- Existujúci pracovný priestor **Riadenie výdavkov** sa nahradí novým pracovným priestorom.
- Pridá sa nové položka ponuky pre viditeľnosť poľa výdavkov.
- Stále môžete otvoriť predchádzajúcu stránku **Výkazy výdavkov** tak, že prejdete na **Správa výdavkov> Moje výdavky > Výkazy výdavkov**.
- Pracovné postupy a akékoľvek schválenia vás stále dovedú na stránku s existujúcimi výkazmi výdavkov.
- Účtenky budú spracované prostredníctvom Microsoft Azure Cognitive Services a metadáta budú extrahované a pridané.
- Je pridaná možnosť, ktorá vám umožní vytvoriť výkaz výdavkov, ktorý obsahuje spárované nepriradené účtenky.
- Možnosť, ktorá sa pridáva do výkazov výdavkov, vám umožňuje vytvoriť výdavkový riadok z účtenky alebo sa pokúsiť spárovať existujúcu účtenku s existujúcim výdavkovým riadkom.

Ďalšie informácie o funkcii nového zobrazenia prehľadov výdavkov nájdete v časti [Prepracované výkazy výdavkov](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Najčastejšie otázky

**Používa spoločnosť Microsoft moje údaje pre svoje modely?**

Nie, spoločnosť Microsoft vytvorila všeobecný model strojového učenia pre svoju službu spracovania účteniek. Tento model nie je založený na účtenkách, ktoré nahráte.

**Kde je táto funkcia k dispozícii a kde sa spracúva?**

Momentálne sú podporované USA.

**Kam smerujú moje účtenky?**

Služba Finance kontaktuje Cognitive Services s cieľom získať údaje polí. Cognitive Services si počas spracovania ponechajú kópiu vašej účtenky až 24 hodín. Po dokončení spracovania Cognitive Services účtenku odstránia. Účtenky sú stále uložené v službe Finance.

Viac informácií nájdete v časti [Umožnite porozumieť účtenkám s novou funkciou rozpoznávania formulárov](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]