---
title: Priradenie potvrdenia k výdavku pomocou optického rozpoznávania znakov (OCR)
description: Táto téma poskytuje informácie o spracovaní účteniek optickým rozpoznávaním znakov (OCR).
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55f63c8c092942b73a55c9d86d867bca600f42e5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124342"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>Priradenie potvrdenia k výdavku pomocou optického rozpoznávania znakov (OCR)

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Zadávanie výdavkov bolo vylepšený zavedením spracovaním účteniek optickým rozpoznávaním znakov (OCR). Táto funkcia je navrhnutá tak, aby zlepšila používateľskú skúsenosť pri vytváraní výkazov výdavkov.

## <a name="key-features"></a>Kľúčové funkcie

- Systém z účtenky vyberie meno obchodníka, dátum a celkovú sumu.
- Systém sa pokúsi priradiť nepripojené účtenky k nepripojeným transakciám výdavkov.
- Z účteniek môžete vytvoriť ručne zadané transakcie výdavkov.

## <a name="attach-receipts-to-an-expense-report"></a>Pripojenie účteniek k výkazu výdavkov

Ak chcete pri vytváraní výkazu výdavkov automaticky pripojiť účtenky, ktoré zahŕňajú transakcie kreditnou kartou, postupujte takto.

  1. Otvorte pracovný priestor **Správa výdavkov**.
  2. Na karte **Účtenky** overte, či existujú nepripojené účtenky. Môžete tiež nahrať účtenky na karte **Účtenky**.
  3. Na karte **Výdavky** overte, či existujú nepripojené výdavky. Spravidla tieto výdavky importuje správca výdavkov od vydavateľa kreditnej karty.
  4. Vyberte **Nový výkaz výdavkov**. Upozorňujeme, že pri vytváraní výkazu výdavkov môžete zahrnúť ako výdavky, tak aj účtenky. Ak pridáte výdavky aj účtenky, spustí sa automatické priraďovanie účteniek k výdavkom.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Vytvorenie alebo spárovanie účteniek s výkazom výdavkov
Ak chcete vytvoriť výdavok alebo spárovať výdavok z účtenky, postupujte takto.

  1. Vo výkaze výdavkov, na karte **Príjmy**, pripojte účtenku výberom možnosti **Pridať účtenky**.
  2. Pod nahraným obrázkom účtenky si všimnite možnosti **Vytvoriť** a **Spárovať**.

      - Vyberte **Vytvoriť** na vytvorenie ručne zadanej výdavkovej transakcie a vyplnenie hodnôt, ktoré sú načítané z účtenky.
      - Ak vyberiete **Spárovať**, systém sa pokúsi spárovať existujúci výdavok s účtenkou.

## <a name="installation"></a>Inštalácia

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

## <a name="frequently-asked-questions"></a>Najčastejšie otázky

**Používa spoločnosť Microsoft moje údaje pre svoje modely?**

Nie, spoločnosť Microsoft vytvorila všeobecný model strojového učenia pre svoju službu spracovania účteniek. Tento model nie je založený na účtenkách, ktoré nahráte.

**Kde je táto funkcia k dispozícii a kde sa spracúva?**

Momentálne sú podporované USA.

**Kam smerujú moje účtenky?**

Služba Finance kontaktuje Cognitive Services s cieľom získať údaje polí. Cognitive Services si počas spracovania ponechajú kópiu vašej účtenky až 24 hodín. Po dokončení spracovania Cognitive Services účtenku odstránia. Účtenky sú stále uložené v službe Finance.

Viac informácií nájdete v časti [Umožnite porozumieť účtenkám s novou funkciou rozpoznávania formulárov](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]