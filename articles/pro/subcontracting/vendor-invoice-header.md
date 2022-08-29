---
title: Podrobnosti hlavičky pre faktúry dodávateľov
description: Tento článok vysvetľuje funkcie, ktoré sú uvedené v hlavičke faktúry dodávateľa v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261702"
---
# <a name="header-details-for-vendor-invoices"></a>Podrobnosti hlavičky pre faktúry dodávateľov

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok vysvetľuje funkcie, ktoré sú uvedené v hlavičke faktúry dodávateľa v Microsoft Dynamics 365 Project Operations.

Ako projektoví manažéri plánujú a realizujú projekty, môžu zamestnávať subdodávateľov a nakupovať produkty a služby od predajcov. Počas realizácie projektu vznikajú náklady na služby, materiály a kategórie nákladov, ktoré sa obstarávajú na základe subdodávok s dodávateľmi. Dodávatelia fakturujú tieto náklady projektom vytvorením faktúr dodávateľa.

Nasledujúca tabuľka poskytuje informácie o poliach v hlavičkách dodávateľských faktúr v Project Operations.

| Pole | Description | Funkčný vplyv |
| --- | --- | --- |
| Name | Názov faktúry dodávateľa. | Vo všetkých rozbaľovacích zoznamoch faktúry dodávateľa je názov faktúry dodávateľa uvedený v prvom stĺpci, aby vám pomohol identifikovať faktúru dodávateľa. Štandardne, keď je faktúra dodávateľa vytvorená zo subdodávky, **názov** pole dodávateľskej faktúry je nastavené na hodnotu, ktorá pozostáva z názvu subdodávky plus aktuálneho dátumu. |
| Description | Stručný popis služieb a produktov, ktoré sú fakturované na faktúre dodávateľa. | None |
| Dodávateľ | Názov spoločnosti, ktorá fakturuje produkty a služby. Táto spoločnosť by mala byť záznamom o účte, ktorý má typ vzťahu **Predajca** alebo **dodávateľa**. | <p>Na základe vybraného dodávateľa sa do nasledujúcich polí automaticky zadajú predvolené hodnoty:</p><ul><li>Mena</li><li>Cenníky</li><li>Platobné podmienky</li><li>Platobná adresa</li></ul> |
| Subdodávateľská zmluva | Odkaz na subdodávku pre faktúru dodávateľa. | <p>Na základe vybranej subdodávky sa predvolené hodnoty automaticky zadajú do nasledujúcich polí:</p><ul><li>Mena</li><li>Cenníky</li><li>Platobné podmienky</li><li>Platobná adresa</li></ul><p>Subdodávka, ktorá je vybratá v hlavičke faktúry dodávateľa, sa štandardne zadáva do riadkov faktúry dodávateľa a nemožno ju tam zmeniť.</p> |
| Dátum fakturácie | Dátum skutočných nákladov, ktorý sa vytvorí po potvrdení faktúry dodávateľa. | Dátum faktúry sa používa aj na výber správneho nákupného cenníka buď z cenníkov, ktoré sú priložené k súvisiacemu predajcovi, alebo z parametrov projektu. |
| Dôvod stavu | Stav faktúry dodávateľa. | <p>Stav určuje, kde sa faktúra dodávateľa nachádza v obchodnom procese a či ju možno upraviť. Tu sú niektoré z dostupných hodnôt:</p><ul><li>**Návrh** – Faktúru dodávateľa je možné upraviť.</li><li>**Potvrdené** – Faktúra dodávateľa bola overená a potvrdená. Faktúry dodávateľa v tomto stave nie je možné upraviť ani odstrániť.</li><li>**V procese** – Faktúra dodávateľa sa kontroluje. Faktúry dodávateľa v tomto stave je možné upravovať, ale nie je možné ich vymazať.</li><li>**Zrušené** – Faktúra dodávateľa bola stornovaná. Faktúry dodávateľa v tomto stave nie je možné upraviť ani odstrániť.</li></ul> |
| Mena | Mena, v ktorej dodávateľ fakturuje produkty a služby na faktúre dodávateľa. | Na faktúre dodávateľa, ktorá odkazuje na subdodávku, je mena subdodávky štandardne zadaná ako mena faktúry dodávateľa. Na faktúre dodávateľa, ktorá neodkazuje na subdodávku, sa predvolená hodnota zadá zo záznamu účtu dodávateľa a možno ju zmeniť. Po uložení faktúry dodávateľa už nie je možné upravovať menu. |
| Zmluvná jednotka | Divízia spoločnosti, ktorá je zodpovedná za prijímanie služieb a/alebo produktov od predajcu. | None |
| Platobné podmienky | Platobné podmienky na faktúrach dodávateľa, ktoré sú vystavené. Predvolená hodnota je automaticky zadaná z účtu dodávateľa. | Platobné podmienky zo subdodávky sa skopírujú do všetkých faktúr dodávateľa, ktoré súvisia so subdodávkou. Platobné podmienky je možné aktualizovať, ak má faktúra dodávateľa stav **Návrh**. |
| Platobná adresa | Adresa dodávateľa, ktorému musia byť platby zaslané. Predvolená hodnota je automaticky zadaná z účtu dodávateľa. | Platobná adresa zo subdodávky sa skopíruje ako platobná adresa do všetkých faktúr dodávateľa, ktoré sú pre danú subdodávku vytvorené. Platobnú adresu je možné aktualizovať, ak má faktúra dodávateľa stav **Návrh**. |
| Medzisúčet | Ak faktúra dodávateľa nemá žiadne riadky, zadajte medzisúčet faktúry pred zdanením. Ak faktúra dodávateľa obsahuje riadky, toto pole je len na čítanie. V tomto prípade zobrazená suma predstavuje medzisúčet zo všetkých riadkov faktúry dodávateľa. | None |
| Celková daň | Ak faktúra dodávateľa nemá žiadne riadky, zadajte celkové dane v subdodávke. Ak faktúra dodávateľa obsahuje riadky, toto pole je len na čítanie. V tomto prípade je zobrazená suma súčtom súm dane zo všetkých riadkov na faktúre dodávateľa. | None |
| Celková suma | Toto vypočítané pole zobrazuje celkovú sumu faktúry dodávateľa po zahrnutí daní. | None |

> [!NOTE]
> Nasledujúce polia na faktúre dodávateľa nie je možné zmeniť po uložení faktúry dodávateľa: **Predajca**, **·**, **·**, **jednotka**, a **Platobné podmienky**. Ak sú potrebné zmeny v týchto poliach na faktúre dodávateľa, musíte faktúru dodávateľa odstrániť a vytvoriť novú faktúru dodávateľa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
