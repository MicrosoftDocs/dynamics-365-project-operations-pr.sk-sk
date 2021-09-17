---
title: Podrobnosti hlavičky pre subdodávateľské zmluvy
description: Táto téma vysvetľuje funkcie uvedené v hlavičke subdodávateľskej zmluvy v Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323660"
---
# <a name="header-details-for-subcontracts"></a>Podrobnosti hlavičky pre subdodávateľské zmluvy

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma vysvetľuje funkcie uvedené v hlavičke subdodávateľskej zmluvy v Dynamics 365 Project Operations.

Keďže projektový manažér plánuje a realizuje projekty, môže zamestnávať subdodávateľov a nakupovať výrobky a služby od predajcov. Keď projektový manažér potrebuje kúpiť produkty alebo služby, môže vytvoriť subdodávateľskú zmluvu v Project Operations.

Ak chcete vytvoriť subdodávateľskú zmluvu, postupujte podľa nasledujúcich krokov.

1. Na navigačnej table vyberte položku **Subdodávateľské zmluvy** a na stránke **Subdodávateľská zmluva** vyberte **Nová**.
2. Zadajte zostávajúce požadované informácie a následne vyberte **Uložiť**.

    Nasledujúca tabuľka poskytuje informácie o poliach na stránke záhlavia subdodávateľskej zmluvy.

    | **Pole** | **Opis** |
    | --- | --- | 
    | Meno | Názov subdodávateľskej zmluvy. |
    | Popis | Stručný popis služieb a produktov, ktoré sa nakupujú v subdodávateľskej zmluve. |
    | Dodávateľ | Názov spoločnosti, od ktorej sa nakupujú produkty a služby. Záznam tohto obchodného vzťahu má typ vzťahu **Dodávateľ** alebo **Poskytovateľ**. |
    | Dátum subdodávateľskej zmluvy | Dátum vytvorenia subdodávateľskej zmluvy. |
    | Dôvod stavu | Stav subdodávateľskej zmluvy. |
    | Mena | Mena, v ktorej sa nakupujú produkty a služby. Hodnota v tomto poli je predvolene z obchodného vzťahu dodávateľa, ale je možné ju zmeniť. Cenníky projektov, ktoré sa používajú na oceňovanie produktov a služieb na subdodávateľskej zmluve, by mali byť v tejto mene. K subdodávateľskej zmluve nemožno priradiť cenníky v žiadnej inej mene. Náklady na produkty a služby vzniknuté v súvislosti s touto subdodávateľskou zmluvou budú zaúčtované do projektu v tejto mene. |
    | Zmluvná jednotka | Divízia spoločnosti, ktorá s predajcom uzatvára kúpnu zmluvu alebo subdodávateľskú zmluvu. |
    | Platobné podmienky | Platobné podmienky na faktúrach dodávateľa, ktoré sú vystavené na základe tejto subdodávateľskej zmluvy. Hodnota v tomto poli predvolene pochádza z zo záznamu obchodného vzťahu dodávateľa. |
    | Platobná adresa | Adresa, na ktorú sa odosielajú platby za faktúry dodávateľa. Hodnota v tomto poli predvolene pochádza z zo záznamu obchodného vzťahu dodávateľa. |
    | Fakturačné meno | Meno osoby alebo divízie v spoločnosti dodávateľa, ktorá bude odosielať faktúru. Hodnota v tomto poli pochádza predvolene zo záznamu obchodného vzťahu dodávateľa a bude použitá ako názov primárneho kontaktu na faktúrach dodávateľa vytvorených pre túto subdodávateľskú zmluvu. |
    | Zasielacia adresa | Adresa použitá na faktúrach od tohto dodávateľa. Hodnota v tomto poli predvolene pochádza z zo záznamu obchodného vzťahu dodávateľa. Táto adresa sa používa aj ako faktúra z adresy na faktúrach dodávateľov vytvorených pre túto subdodávateľskú zmluvu. |
    | Medzisúčet | Ak subdodávateľská zmluva nemá žiadne riadky, zadajte do tohto poľa hodnotu, ktorá označuje medzisúčet objednávky pred zdanením. Ak má subdodávateľská zmluva riadky, toto pole je len na čítanie. Zobrazená čiastka je medzisúčtom zo všetkých riadkov subdodávateľskej zmluvy. |
    | Daň celkom | Ak subdodávateľská zmluva nemá žiadne riadky, zadajte do tohto poľa hodnotu, ktorá označuje dane v tejto subdodávateľskej zmluve. Ak má subdodávateľská zmluva riadky, toto pole je len na čítanie. Zobrazená čiastka je súčtom čiastok dane zo všetkých riadkov subdodávateľskej zmluvy. |
    | Celková čiastka |  Toto vypočítané pole ukazuje celkovú sumu subdodávateľskej zmluvy po zahrnutí daní.  |
    | Dátum potvrdenia | Dátum potvrdenia subdodávateľskej zmluvy.  |
    | Požiadal používateľ | Hodnota v tomto poli je predvolene nastavená na meno používateľa, ktorý vytvára subdodávateľskú zmluvu. Túto hodnotu môže zmeniť tvorca subdodávateľskej zmluvy, aby označil osobu, v mene ktorej vytvára subdodávateľskú zmluvu.  |
    | Account manažér dodávateľa | Názov primárneho kontaktu obchodného vzťahu dodávateľa. Hodnota v tomto poli predvolene pochádza z zo záznamu obchodného vzťahu dodávateľa. Túto hodnotu poľa môže používateľ zmeniť tak, aby ako správcu obchodného vzťahu dodávateľa subdodávateľskej zmluvy vybral iný kontakt. Tento kontakt môže konfigurovať a odosielať e-mailové upozornenia a vyjednávania o cenách. |


