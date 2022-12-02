---
title: Zaúčtovanie výkazov výdavkov
description: Tento článok vysvetľuje, ako účtovať výkazy výdavkov.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524889"
---
# <a name="post-expense-reports"></a>Zaúčtovanie výkazov výdavkov

Po schválení a preložení výkazu výdavkov do finančného denníka je možné ho zaúčtovať. Pri zaúčtovaní výkazu výdavkov sa identifikujú výdavky, ktoré sú oprávnené na vrátenie dane z pridanej hodnoty (DPH). Úloha overovania a vrátenia platieb DPH je pridelená zamestnancovi, ktorý je zodpovedný za overenie výkazu výdavkov.

Ak sú náklady na správu o výdavkoch účtované inej spoločnosti ako spoločnosti, ktorá zamestnáva zamestnanca, musíte overiť spoločnosť, ktorá tieto náklady dlhuje ako aj spoločnosť, ktorej dlhuje náklady. Napríklad zamestnanec, ktorý predložil výkaz výdavkov, pracuje pre spoločnosť DAT, ale výdavky účtoval spoločnosti DIR. V takom prípade je DAT spoločnosť, ktorej dlhuje výdavok, a DIR je spoločnosť, ktorej je výdavok dlžný. Po overení týchto riadkov denníka môžete zaúčtovať riadky výdavkov do účtovnej knihy.

Ak chcete zaúčtovať výkaz výdavkov, na stránke **Schválené výkazy výdavkov** vyberte výkaz výdavkov a potom na table akcií vyberte **Príspevok**.

Môžete tiež zaúčtovať všetky výkazy výdavkov v zozname súčasne. Vyberte všetky výkazy výdavkov a potom vyberte **Príspevok**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Povoľte funkciu Schopnosť účtovať výdavkový záväzok v mene dodávateľa pre spôsob úhrady v hotovosti

Funkcia **Schopnosť účtovať výdavkový záväzok v mene dodávateľa pre spôsob úhrady v hotovosti** umožňuje zaúčtovať výkazy výdavkov v mene dodávateľa pre spôsob úhrady v hotovosti.

V súčasnosti, keď predkladáte hotovostné výdavky, výkazy výdavkov sa účtujú v účtovnej mene. Z dôvodu prevodu sumy medzi menou transakcie, účtovnou menou a menou dodávateľa sa dodávateľom zaplatí nesprávna suma, ak dátum transakcie výdavku a skutočný dátum platby majú rozdielne výmenné kurzy.

Táto funkcia zabezpečí, že zostatok dodávateľa bude zaznamenaný v mene dodávateľa pri zaúčtovaní výkazu výdavkov.

1. Prejdite do časti **Pracovné priestory** \> **Správa funkcií**.
2. V zozname vyhľadajte a vyberte **Schopnosť zaúčtovať výdavkový záväzok v mene dodávateľa pre spôsob úhrady v hotovosti** a potom vyberte **Povoliť teraz**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
