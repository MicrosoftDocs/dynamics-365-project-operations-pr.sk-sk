---
title: Správa stavu, ktorý sa nesmie prekročiť, a overení
description: Táto téma poskytuje informácie o kontrolách neprekročenia limitu vykonávaných v aplikácii Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130012"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Správa stavu, ktorý sa nesmie prekročiť, a overení 

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

## <a name="not-to-exceed-on-approvals"></a>Nesmie byť prekročené pri schválení

Po zadaní záznamu o čase alebo výdaji sa vytvorí záznam o schválení. Ak je schválenie fakturovateľné a mapuje sa na časový a materiálny riadok zmluvy, systém vykoná overovaciu kontrolu neprekročenia na nasledujúcich úrovniach:

  - Kontrola proti limitu stanovenému pre zákazníka v riadku projektovej zmluvy
  - Kontrola proti limitu stanovenému v riadku zmluvy
  - Kontrola proti limitu stanovenému pre zákazníka
  - Kontrola proti limitu stanovenému v zmluve

Kontroly na každej úrovni zahŕňajú zabezpečenie toho, aby suma hodnoty predaja pri tomto schválení neporušila neprekročiteľný limit na tejto úrovni po zohľadnení množstva už zaznamenaných nevybavených fakturácií a sumy fakturovanej k dnešnému dňu na tejto úrovni.

Ak kontrola prejde, udelí sa schváleniu stav overenia **Úspech**.

Ak kontrola zlyhá, udelí sa schváleniu stav overenia **Neúspešné**. Podrobnosti overenia, ktoré sa nesmie prekročiť, budú informovať používateľa, na ktorej úrovni sa overenie nepodarilo.

Ak sa zadaný záznam o čase alebo výdavku považuje za nefakturovateľný, stav overenia, ktorý sa nesmie prekročiť, sa nastaví na **Nepoužiteľné** s podrobnosťou overenia rovnou **Nevzťahuje sa**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Neprekročiteľné pri nefakturovaných skutočných predajoch

Po schválení zadania času alebo výdaja sa vytvoria záznamy o skutočných nákladoch a nevyfakturovaných skutočných predajoch. Ak je vytváraná skutočná hodnota nefakturovaného predaja fakturovateľná a mapuje sa na časový a materiálny riadok zmluvy, aplikácia vykoná overovaciu kontrolu neprekročenia na nasledujúcich úrovniach:

  - Kontrola proti limitu stanovenému pre zákazníka riadka projektovej zmluvy
  - Kontrola proti limitu stanovenému v riadku zmluvy
  - Kontrola proti limitu stanovenému pre zákazníka
  - Kontrola proti limitu stanovenému v zmluve

Kontroly na každej úrovni zaistia, aby suma hodnoty predaja pri skutočnej hodnote neporušila neprekročiteľný limit na tejto úrovni po zohľadnení množstva už zaznamenaných nevybavených fakturácií a sumy fakturovanej k dnešnému dňu na tejto úrovni.

Ak kontrola prejde, skutočná hodnota nefakturovaného predaja bude mať stav, ktorý sa nesmie prekročiť **Zaviazaný**.

Ak kontrola zlyhá, skutočná hodnota nefakturovaného predaja bude mať stav, ktorý sa nesmie prekročiť **Neúspešné**. Podrobnosti overenia informujú používateľa, na ktorej úrovni sa overenie nepodarilo.

Keď sa skutočný nevyfakturovaný predaj považuje za nefakturovateľný alebo bezplatný, ak na žiadnej zo štyroch úrovní nie je nastavený limit, ktorý sa nesmie prekročiť, alebo ak je vytváranou skutočnou hodnotou Náklad, Preddavok, Zdrojová jednotka alebo Predaj v rámci organizácie, polia **Stav, ktorý sa nesmie prekročiť** a **Podrobnosti overenia, ktoré sa nesmú prekročiť** musia byť nastavené na **Nepoužiteľné**.

## <a name="reset-the-not-to-exceed-status"></a>Zresetovanie stavu, ktorý sa nesmie prekročiť

Môžete vykonať hromadný reset stavu, ktorý sa nesmie prekročiť. To umožňuje projektovým manažérom upraviť overenie, ktoré sa nesmie prekročiť, aby uprednostnili fakturáciu jedného konkrétneho súboru práce, času alebo výdavkov pred ostatnými, ktoré sú už viazané z dostupnej sumy, ktorá sa nesmie prekročiť.

Po zresetovaní stavu, ktorý sa nesmie prekročiť, v nefakturovaných skutočných predajoch, sa viazaná suma zníži. Projektový manažér môže vybrať iný súbor práce, času alebo výdavkov, ktoré predtým zlyhali pri overení, ktoré sa nesmie prekročiť, a prehodnotiť ich. So znížením pridelenej sumy tieto skutočné hodnoty teraz prejdú overením. To pomáha projektovému manažérovi uplatňovať väčší vplyv a kontrolu nad fakturovateľnými transakciami za dané obdobie.

Ak chcete resetovať stav, ktorý sa nesmie prekročiť, vyberte jednu alebo viac skutočných hodnôt zo zobrazenia **Backlog pre fakturáciu času a materiálu** alebo **Skutočné hodnoty** a potom vyberte **Resetovať stav, ktorý sa nesmie prekročiť**.

Stav, ktorý sa nesmie prekročiť, sa obnoví na **Nehodnotené** pri všetkých relevantných vybratých skutočných hodnotách. Skutočné hodnoty, ktoré majú obnovený stav, ktorý sa nesmie prekročiť, sú nefakturované skutočné predaje, ktoré ešte nie sú vyfakturované, nie na koncepte faktúry, a sú označené ako účtovateľné. Všetky ďalšie vybrané skutočné hodnoty sú ignorované.

## <a name="reevaluate-not-to-exceed-status"></a>Prehodnotenie stavu, ktorý sa nesmie prekročiť

Môžete vykonať hromadné prehodnotenie stavu, ktorý sa nesmie prekročiť. Prehodnotenie stavu, ktorý sa nesmie prekročiť, je užitočné v týchto prípadoch:

  - U zákazníka došlo k opätovnému prerokovaniu limitov, ktoré sa nesmú prekročiť, so zákazníkom a bude potrebné prehodnotiť skutočné hodnoty.
  - Projektový manažér chce doladiť backlog fakturácie nevyfakturovaných predajov uprednostnením jedného diela pred druhým.

Ak chcete prehodnotiť stav, ktorý sa nesmie prekročiť, vyberte jednu alebo viac skutočných hodnôt zo zobrazenia **Backlog pre fakturáciu času a materiálu** alebo **Skutočné hodnoty** a potom vyberte **Prehodnotiť stav, ktorý sa nesmie prekročiť**.

Všetky príslušné vybrané skutočné hodnoty s limitom, ktorý sa nesmie prekročiť, sa vyhodnotia oproti nastaveniu limitu, ktorý sa nesmie prekročiť. Skutočné hodnoty, ktoré sú relevantné pre opätovné prehodnotenie stavu, ktorý sa nesmie prekročiť, sú nefakturované skutočné predaje, ktoré nie sú vyfakturované, nie na koncepte faktúry, a sú označené ako účtovateľné. Akékoľvek ďalšie príslušné vybraté skutočné hodnoty.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]