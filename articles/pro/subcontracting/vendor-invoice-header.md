---
title: Podrobnosti hlavičky pre faktúry dodávateľov
description: Tento článok vysvetľuje funkcie, ktoré sú k dispozícii v hlavičke faktúry dodávateľa v Microsoft Dynamics 365 Project Operations.
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

Tento článok vysvetľuje funkcie, ktoré sú k dispozícii v hlavičke faktúry dodávateľa v Microsoft Dynamics 365 Project Operations.

Keďže projektový manažér plánuje a realizuje projekty, môže zamestnávať subdodávateľov a nakupovať výrobky a služby od dodávateľov. Počas realizácie projektu vznikajú náklady na kategórie služieb, materiálov a nákladov, ktoré sa obstarávajú na základe subdodávateľských zmlúv s dodávateľmi. Dodávatelia fakturujú tieto náklady projektom vytvorením faktúr dodávateľa.

Nasledujúca tabuľka poskytuje informácie o poliach v hlavičkách faktúr dodávateľa v Project Operations.

| Pole | Description | Funkčný vplyv |
| --- | --- | --- |
| Name | Názov faktúry dodávateľa. | Vo všetkých rozbaľovacích zoznamoch faktúr dodávateľa je v prvom stĺpci uvedený názov faktúry dodávateľa, ktorý vám pomôže identifikovať faktúru dodávateľa. Štandardne, keď je faktúra dodávateľa vytvorená zo subdodávateľskej zmluvy, pole **Názov** faktúry dodávateľa je nastavené na hodnotu, ktorá pozostáva z názvu subdodávateľskej zmluvy plus aktuálneho dátumu. |
| Description | Stručný opis služieb a produktov, ktoré sú fakturované na riadku faktúre dodávateľa. | None |
| Dodávateľ | Názov spoločnosti, ktorá fakturuje výrobky a služby. Táto spoločnosť by mala byť obchodným vzťahom, ktorý má typ vzťahu **Dodávateľ** alebo **Poskytovateľ**. | <p>Na základe vybraného dodávateľa sa automaticky zadajú predvolené hodnoty v nasledujúcich poliach:</p><ul><li>Mena</li><li>Cenníky</li><li>Platobné podmienky</li><li>Platobná adresa</li></ul> |
| Subdodávateľská zmluva | Odkaz na subdodávateľskú zmluvu pre faktúru dodávateľa. | <p>Na základe vybranej subdodávateľskej zmluvy sa automaticky zadajú predvolené hodnoty v nasledujúcich poliach:</p><ul><li>Mena</li><li>Cenníky</li><li>Platobné podmienky</li><li>Platobná adresa</li></ul><p>Subdodávateľská zmluva, ktorá je vybratá v hlavičke faktúry dodávateľa, sa štandardne zadáva do riadkov faktúry dodávateľa a nemožno ju tam zmeniť.</p> |
| Dátum faktúry | Dátum skutočných hodnôt nákladov, ktorý sa vytvorí po potvrdení faktúry dodávateľa. | Dátum faktúry sa tiež používa na výber správneho nákupného cenníka buď z cenníkov, ktoré sú pripojené k príslušnému dodávateľovi, alebo z parametrov projektu. |
| Dôvod stavu | Stav faktúry dodávateľa. | <p>Stav určuje, kde faktúra dodávateľa v obchodnom procese nachádza a či ju možno upravovať. Tu sú niektoré z dostupných hodnôt:</p><ul><li>**Koncept** – Faktúru dodávateľa je možné upraviť.</li><li>**Potvrdené** – Faktúra dodávateľa bola overená a potvrdená. Faktúra dodávateľa v tomto stave sa nedá upravovať ani odstrániť.</li><li>**V procese** – Faktúra dodávateľa sa kontroluje. Faktúry dodávateľov v tomto stave sa dajú upravovať, ale nedajú sa odstrániť.</li><li>**Zrušené** – Faktúra dodávateľa bola zrušená. Faktúra dodávateľa v tomto stave sa nedá upravovať ani odstrániť.</li></ul> |
| Mena | Mena, v ktorej dodávateľ fakturuje produkty a služby na faktúre dodávateľa. | Na faktúre dodávateľa, ktorá odkazuje na subdodávateľskú zmluvu, je mena subdodávateľskej zmluvy štandardne zadaná ako mena faktúry dodávateľa. Na faktúre dodávateľa, ktorá neodkazuje na subdodávateľskú zmluvu, sa predvolená hodnota zadá zo záznamu obchodného vzťahu dodávateľa a možno ju zmeniť. Po uložení faktúry dodávateľa už nie je možné upravovať menu. |
| Zmluvná jednotka | Divízia spoločnosti, ktorá je zodpovedná za prijímanie služieb a/alebo produktov od predajcu. | None |
| Platobné podmienky | Platobné podmienky na faktúrach dodávateľa, ktoré sú vystavené. Predvolená hodnota je automaticky zadaná z účtu dodávateľa. | Platobné podmienky zo subdodávateľskej zmluvy sa skopírujú do všetkých faktúr dodávateľov, ktoré súvisia so subdodávateľskou zmluvou. Platobné podmienky je možné aktualizovať, ak má faktúra dodávateľa stav **Koncept**. |
| Platobná adresa | Adresa dodávateľa, ktorému musia byť platby zaslané. Predvolená hodnota je automaticky zadaná z účtu dodávateľa. | Platobná adresa zo subdodávateľskej zmluvy sa skopíruje ako platobná adresa do všetkých faktúr dodávateľov, ktoré sú pre subdodávateľskú zmluvu vytvorené. Platobnú adresu je možné aktualizovať, ak má faktúra dodávateľa stav **Koncept**. |
| Medzisúčet | Ak faktúra dodávateľa nemá riadky, zadajte medzisúčet faktúry pred zdanením. Ak má faktúra dodávateľa riadky, toto pole je len na čítanie. V tomto prípade je suma, ktorá je zobrazená, je medzisúčtom zo všetkých riadkov na faktúre dodávateľa. | None |
| Celková daň | Ak faktúra dodávateľa nemá riadky, zadajte celkové dane na subdodávateľskej zmluve. Ak má faktúra dodávateľa riadky, toto pole je len na čítanie. V tomto prípade je suma, ktorá je zobrazená, je celkovým súčtom daní zo všetkých riadkov na faktúre dodávateľa. | None |
| Celková čiastka | Toto vypočítané pole ukazuje celkovú sumu faktúry dodávateľa po zahrnutí daní. | None |

> [!NOTE]
> Nasledujúce polia na faktúre dodávateľa nie je možné zmeniť po uložení faktúry dodávateľa: **Predajca**, **Subdodávateľská zmluva**, **Mena**, **Zmluvná jednotka** a **Platobné podmienky**. Ak sú potrebné zmeny v týchto poliach na faktúre dodávateľa, musíte faktúru dodávateľa odstrániť a vytvoriť novú faktúru dodávateľa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
