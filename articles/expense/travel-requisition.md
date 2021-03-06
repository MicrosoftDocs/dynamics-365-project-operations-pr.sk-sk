---
title: Cestovné žiadanky
description: Táto téma poskytuje informácie o cestovných žiadankách.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906328"
---
# <a name="travel-requisitions"></a>Cestovné žiadanky

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

V cestovnej žiadanke je uvedený zoznam výdavkov, ktoré vzniknú pri cestovaní. Cestovná žiadanka sa predkladá na kontrolu a môže sa použiť na autorizáciu výdavkov.

Môže sa od vás vyžadovať predloženie cestovnej žiadanky ešte predtým, ako vám vzniknú akékoľvek výdavky, ktoré sa účtujú organizácii. Táto požiadavka platí bez ohľadu na to, či účtujete výdavky na firemnú kreditnú kartu, míňate hotovosť, ktorú ste dostali z hotovostnej zálohy, alebo či vám vzniknú hotovostné výdavky, ktoré vám organizácia uhradí.

Cestovné žiadanky a politiky možno použiť na pomoc s riadením výdavkov organizácie. Napríklad, ak vaša organizácia pracuje na projekte s pevnou cenou, ktorý vyžaduje cestovanie, cestovné náklady členov projektového tímu musia zodpovedať rozpočtu projektu. Požadovaním schválenia cestovných výdavkov pred ich vznikom môže organizácia pomôcť zabezpečiť, aby projekt zostal v rámci rozpočtu.

## <a name="configuration"></a>Konfigurácia 

Cestovné žiadanky je možné nakonfigurovať ako „povinné“ povolením parametra „Predbežná autorizácia cesty je povinná“ v parametroch správy výdavkov. 

## <a name="create-and-submit-a-travel-requisition"></a>Vytvorenie a odoslanie cestovnej žiadanky

1. Prejdite do časti **Moje výdavky: cestovné žiadanky** a vyberte **Nová cestovná žiadanka**.
2. Zadajte účel a cieľ žiadanky.
3. V poli **Popis cesty** zadajte ďalšie informácie. 
4. Pre každý z očakávaných výdavkov, napríklad za letenku, stravu alebo prenájom auta, vytvorte riadkovú položku výdavkov. Uveďte predpokladaný dátum, odhadovanú sumu a menu pre každý výdavok. 
5. Po dokončení pridávania očakávaných výdavkov vyberte možnosť **Uložiť**.
6. Keď ste pripravení na odoslanie cestovnej žiadanky, zvoľte **Pracovný tok** > **Odoslať**.

Schválené cestovné žiadanky si môžete pozrieť v časti **Moje výdavky: cestovné žiadanky**. 

## <a name="view-available-travel-requisitions"></a>Zobrazenie dostupných cestovných žiadaniek

Všetky svoje cestovné žiadanky si môžete pozrieť v časti **Moje výdavky: cestovné žiadanky**.

## <a name="approve-travel-requisitions"></a>Schválenie cestovných žiadaniek

Vyberte cestovnú žiadanku, ktorú chcete schváliť, a potom vyberte **Pracovný postup** > **Schváliť**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Odošlite výkaz výdavkov pomocou svojej schválenej cestovnej žiadanky

1. Vytvorte nový výkaz výdavkov a v hlavičke výkazu výdavkov a zo zoznamu schválených cestovných žiadaniek vyberte **Mapovať na cestovnú žiadanku**.
2. Pole **Suma cestovnej žiadanky** sa automaticky aktualizuje v hlavičke výkazu výdavkov.
3. Pridajte všetky výdavky spojené s cestou. Ak je povolené pole **Predbežne schválené** aktualizuje sa zosúladená a schválená suma pre konkrétnu kategóriu výdavkov.

> [!NOTE]
> Keď mapujete výkaz výdavkov na schválenú cestovnú žiadanku, suma transakcie nemôže byť vyššia ako schválená suma. 
