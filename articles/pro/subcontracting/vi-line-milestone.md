---
title: Riadky faktúr dodávateľov pre medzníky
description: Tento článok vysvetľuje, ako vytvoriť riadky faktúry dodávateľa pre medzníky v subdodávateľskej zmluve.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261048"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Riadky faktúr dodávateľov pre medzníky

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Faktúra dodávateľa v Microsoft Dynamics 365 Project Operations môže mať riadky faktúry dodávateľa pre medzníky, ktoré sú definované na riadku subdodávateľskej zmluvy. Projektoví manažéri môžu použiť riadky faktúry dodávateľa pre medzníky na zaznamenanie nákladov na služby, ktoré sú obstarané ako náklady založené na medzníkoch, ktoré sú vynaložené na služby alebo produkty, ktoré sú obstarané pre projekt.

Riadky faktúry dodávateľa pre medzníky musia vždy odkazovať na riadok subdodávateľskej zmluvy, ktorý používa spôsob fakturácie s pevnou cenou. Ak riadok faktúry dodávateľa pre medzníky odkazuje na riadok subdodávateľskej zmluvy, manažéri projektu budú môcť spárovať a overiť príslušné časové náklady, výdavky alebo materiál, ktoré odkazujú na riadok subdodávateľskej zmluvy, s medzníkom, ktorý fakturuje dodávateľ.

Nasledujúca tabuľka poskytuje informácie o poliach na riadku faktúry dodávateľa pre medzníky.

| Pole | Description | Funkčný vplyv |
| --- | --- | --- |
| Name | Názov riadka faktúry dodávateľa, ktorý má pomôcť s identifikáciou. | Tento názov sa zobrazí ako prvý stĺpec vo všetkých vyhľadávaniach, ktoré sú založené na riadkoch faktúr dodávateľov. |
| Description | Stručný opis služieb, ktoré dodávateľ fakturuje na riadku faktúry dodávateľa. | None |
| Subdodávateľská zmluva | Subdodávateľská zmluva, na základe ktorej boli služby pôvodne objednané. | Keď je pre faktúru dodávateľa vybratá subdodávateľská zmluva, všetky riadky na faktúre dodávateľa zdedia tento výber. Faktúra dodávateľa nemôže obsahovať riadky faktúry dodávateľa, ktoré odkazujú na rôzne subdodávateľské zmluvy. |
| Riadok subdodávateľskej zmluvy | Riadok subdodávateľskej zmluvy, na základe ktorého boli služby objednané. Zoznam riadkov subdodávateľských zmlúv, ktoré je možné vybrať, je obmedzený na riadky vo vybranej subdodávateľskej zmluve. | Keď sa v riadku faktúry dodávateľa pre medzníky vyberie riadok subdodávateľskej zmluvy, polia **Rola**, **Kategória transakcie** a polia súvisiace s produktom sú irelevantné a nie sú dostupné. Polia **Množstvo**, **Jednotka** a **Jednotková skupina** tiež nie sú relevantné pre riadky faktúry dodávateľa založené na medzníkoch. |
| Dátum transakcie | Dátum, kedy budú skutočné náklady riadku faktúry dodávateľa zaznamenané v projekte. | None |
| Trieda transakcie | Vyberte **Medzník** na zaznamenanie faktúry dodávateľa za dokončený medzník, ktorý bol definovaný na riadku subdodávateľskej zmluvy. | None |
| Medzník | Vyberte medzník, ktorý je definovaný v príslušnom riadku subdodávateľskej zmluvy, ktorý je označený ako **Pripravené na fakturáciu**. | Na riadku faktúry dodávateľa možno vybrať medzníky riadka subdodávateľskej zmluvy, ktoré majú stav **Pripravené na fakturáciu**. |
| Project | Názov projektu, v rámci ktorého boli fakturované služby použité. | Toto pole je povinné a nemôže ostať prázdne. |
| Úloha | Názov projektovej úlohy, v rámci ktorého boli fakturované služby použité. Toto pole je dostupné len vtedy, ak je vybratý projekt. Výber projektovej úlohy je voliteľný. | Ak toto pole ponecháte prázdne, projektový manažér môže spárovať riadok faktúry dodávateľa s triedou transakcií na príslušnom riadku subdodávateľskej zmluvy, ktorá je zaznamenaná na ľubovoľnej úlohe projektu. Ak riadok faktúry dodávateľa neodkazuje na riadok subdodávateľskej zmluvy a toto pole zostane prázdne, skutočné náklady vytvorené riadkom faktúry dodávateľa nebudú prepojené so žiadnymi skutočnými nevyfakturovanými predajmi. V tomto prípade, ak je nastavená fakturácia podľa úloh, nemusí byť možné náklady fakturovať koncovému zákazníkovi. |
| Suma medzníka | Zadajte hodnotu medzníka, ktorý je definovaný v príslušnom riadku subdodávateľskej zmluvy, ktorý je pripravený na fakturáciu. | None |
| Daň z predaja | Zadajte sumu dane z predaja. | None |
| Celková čiastka | Celková čiastka riadka faktúry dodávateľa vrátane daní. Toto pole sa počíta ako *Suma medzníka* + *Daň z predaja*. | None |

> [!NOTE]
> Keď sa vytvorí riadok faktúry dodávateľa, ktorý odkazuje na medzník v riadku subdodávateľskej zmluvy, stav medzníka subdodávateľskej zmluvy sa aktualizuje na **Faktúra dodávateľa bola vytvorená**. Potom, keď je táto faktúra dodávateľa potvrdená, stav medzníka riadku subdodávateľskej zmluvy sa aktualizuje na **Faktúra dodávateľa potvrdená**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
