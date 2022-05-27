---
title: Podrobnosti hlavičky pre faktúry dodávateľa
description: Táto téma vysvetľuje funkcie poskytované v hlavičke faktúry dodávateľa v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17be106d5486358ff0bbf011af3da26a4c85a274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575599"
---
# <a name="header-details-for-vendor-invoices"></a>Podrobnosti hlavičky pre faktúry dodávateľa

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma vysvetľuje funkcie poskytované v hlavičke faktúry dodávateľa v Microsoft Dynamics 365 Project Operations.

Ako projektoví manažéri plánujú a realizujú projekty, môžu zamestnávať subdodávateľov a nakupovať produkty a služby od predajcov. Počas realizácie projektu vznikajú náklady na služby, materiály a kategórie nákladov, ktoré sa obstarávajú na základe subdodávok s dodávateľmi. Dodávatelia fakturujú tieto náklady projektom vytvorením dodávateľských faktúr.

Nasledujúca tabuľka poskytuje informácie o poliach v hlavičkách dodávateľských faktúr v projektových operáciách.

| Pole | Description | Funkčný vplyv |
| --- | --- | --- |
| Name | Názov faktúry dodávateľa. | Vo všetkých rozbaľovacích zoznamoch faktúry dodávateľa je názov faktúry dodávateľa uvedený v prvom stĺpci, aby vám pomohol identifikovať faktúru dodávateľa. Štandardne, keď je faktúra dodávateľa vytvorená zo subdodávky, **názov** pole dodávateľskej faktúry je nastavené na hodnotu, ktorá pozostáva z názvu subdodávky plus aktuálneho dátumu. |
| Description | Stručný popis služieb a produktov, ktoré sú fakturované na faktúre dodávateľa. | None |
| Dodávateľ | Názov spoločnosti, ktorá fakturuje produkty a služby. Táto spoločnosť by mala byť záznamom o účte, ktorý má typ vzťahu **Predajca** alebo **dodávateľa**. | <p>Na základe vybraného dodávateľa sa do nasledujúcich polí automaticky zadajú predvolené hodnoty:</p><ul><li>Mena</li><li>Cenníky</li><li>Platobné podmienky</li><li>Platobná adresa</li></ul> |
| Subdodávateľská zmluva | Odkaz na subdodávku pre faktúru dodávateľa. | <p>Na základe vybranej subdodávky sa predvolené hodnoty automaticky zadajú do nasledujúcich polí:</p><ul><li>Mena</li><li>Cenníky</li><li>Platobné podmienky</li><li>Platobná adresa</li></ul><p>Subdodávka, ktorá je vybratá v hlavičke faktúry dodávateľa, sa štandardne zadáva do riadkov faktúry dodávateľa a nemožno ju tam zmeniť.</p> |
| Dátum fakturácie | Dátum pre skutočné náklady, ktorý sa vytvorí po potvrdení faktúry dodávateľa. | Dátum faktúry sa používa aj na výber správneho nákupného cenníka buď z cenníkov, ktoré sú priložené k súvisiacemu predajcovi, alebo z parametrov projektu. |
| Dôvod stavu | Stav faktúry dodávateľa. | <p>Stav určuje, kde sa faktúra dodávateľa nachádza v obchodnom procese a či ju možno upraviť. Tu sú niektoré z dostupných hodnôt:</p><ul><li>**Návrh** – Faktúru dodávateľa je možné upraviť.</li><li>**Potvrdené** – Faktúra dodávateľa bola overená a potvrdená. Faktúry dodávateľa v tomto stave nie je možné upravovať ani mazať.</li><li>**V procese** – Faktúra dodávateľa sa kontroluje. Faktúry dodávateľa v tomto stave je možné upravovať, ale nie je možné ich vymazať.</li><li>**Zrušené** – Faktúra dodávateľa bola stornovaná. Faktúry dodávateľa v tomto stave nie je možné upravovať ani mazať.</li></ul> |
| Mena | Mena, v ktorej dodávateľ fakturuje produkty a služby na faktúre dodávateľa. | Na faktúre dodávateľa, ktorá odkazuje na subdodávku, je mena subdodávky štandardne zadaná ako mena faktúry dodávateľa. Na faktúre dodávateľa, ktorá neodkazuje na subdodávku, sa predvolená hodnota zadá zo záznamu účtu dodávateľa a možno ju zmeniť. Po uložení faktúry dodávateľa už nie je možné upravovať menu. |
| Zmluvná jednotka | Divízia spoločnosti, ktorá je zodpovedná za prijímanie služieb a/alebo produktov od predajcu. | None |
| Platobné podmienky | Platobné podmienky na faktúrach dodávateľa, ktoré sú vystavené. Predvolená hodnota je automaticky zadaná z účtu dodávateľa. | Platobné podmienky zo subdodávky sa skopírujú do všetkých faktúr dodávateľa, ktoré súvisia so subdodávkou. Platobné podmienky možno aktualizovať, ak má faktúra dodávateľa stav **Návrh**. |
| Platobná adresa | Adresa dodávateľa, ktorému musia byť platby zaslané. Predvolená hodnota je automaticky zadaná z účtu dodávateľa. | Platobná adresa zo subdodávky sa skopíruje ako platobná adresa do všetkých faktúr dodávateľa, ktoré sú pre danú subdodávku vytvorené. Platobnú adresu je možné aktualizovať, ak má faktúra dodávateľa stav **Návrh**. |
| Medzisúčet | Ak faktúra dodávateľa nemá žiadne riadky, zadajte medzisúčet faktúry pred zdanením. Ak faktúra dodávateľa obsahuje riadky, toto pole je len na čítanie. V tomto prípade zobrazená suma predstavuje medzisúčet zo všetkých riadkov faktúry dodávateľa. | None |
| Celková daň | Ak faktúra dodávateľa nemá žiadne riadky, zadajte celkové dane v subdodávke. Ak faktúra dodávateľa obsahuje riadky, toto pole je len na čítanie. V tomto prípade je zobrazená suma súčtom súm dane zo všetkých riadkov na faktúre dodávateľa. | None |
| Celková suma | Toto vypočítané pole zobrazuje celkovú sumu faktúry dodávateľa po zahrnutí daní. | None |

> [!NOTE]
> Nasledujúce polia na faktúre dodávateľa nie je možné zmeniť po uložení faktúry dodávateľa: **Predajca**, **·**, **·**, **jednotka** a **Platobné podmienky**. Ak sú potrebné zmeny v týchto poliach na faktúre dodávateľa, musíte faktúru dodávateľa odstrániť a vytvoriť novú faktúru dodávateľa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
