---
title: Podrobnosti hlavičky pre subdodávateľské zmluvy
description: Táto téma vysvetľuje funkcie uvedené v hlavičke subdodávateľskej zmluvy v Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee863d31b45e7de962488fe804202ddfe580eb04
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501345"
---
# <a name="header-details-for-subcontracts"></a>Podrobnosti hlavičky pre subdodávateľské zmluvy

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma vysvetľuje funkcie uvedené v hlavičke subdodávateľskej zmluvy v Dynamics 365 Project Operations.

Keďže projektový manažér plánuje a realizuje projekty, môže zamestnávať subdodávateľov a nakupovať výrobky a služby od predajcov. Keď projektový manažér potrebuje kúpiť produkty alebo služby, môže vytvoriť subdodávateľskú zmluvu v Project Operations.

Ak chcete vytvoriť subdodávateľskú zmluvu, postupujte podľa nasledujúcich krokov.

1. Na navigačnej table vyberte položku **Subdodávateľské zmluvy** a na stránke **Subdodávateľská zmluva** vyberte **Nová**.
2. Zadajte zostávajúce požadované informácie a následne vyberte **Uložiť**.

    Nasledujúca tabuľka poskytuje informácie o poliach na stránke **záhlavia subdodávateľskej zmluvy**.

    | Pole | Popis |Funkčný vplyv |
    |---|------|---| 
    | Meno | Názov subdodávateľskej zmluvy. | Vo všetkých rozbaľovacích zoznamoch subdodávok je v prvom stĺpci uvedený názov subdodávky, ktorý vám pomôže identifikovať subdodávku. | 
    | Popis | Stručný popis služieb a produktov, ktoré sa nakupujú v subdodávateľskej zmluve. | Nie je |
    | Dodávateľ | Názov spoločnosti, od ktorej sa nakupujú produkty a služby. Záznam tohto obchodného vzťahu má typ vzťahu **Dodávateľ** alebo **Poskytovateľ**. | Na základe vybraného dodávateľa sa automaticky zadajú predvolené hodnoty pre nasledujúce polia:<br/> **• Mena**. </br> **• Cenníky** </br> **• Platobné podmienky**</br> **• Platobná adresa**</br> **• Zasielacia adresa**</br> **• Fakturačné meno** </br>**• Account manažér dodávateľa**|
    | Dátum subdodávateľskej zmluvy | Dátum vytvorenia subdodávky. | Dátum subdodávky sa používa na výber správneho nákupného cenníka buď z cenníkov, ktoré sú pripojené k príslušnému dodávateľovi, alebo z parametrov projektu. |
    | Dôvod stavu | Stav subdodávateľskej zmluvy. | Stav určuje, kde sa subdodávka v obchodnom procese nachádza a či ju možno upravovať. <br/>Hodnoty zahŕňajú:<br>• **Koncept**: Subdodávku je možné upraviť. Upravovať môžete iba subdodávky so stavom **Koncept**.<br/>• **Potvrdená**: Rokovanie s predajcom je dokončené a subdodávka je schválená na dodanie. <br/>• **Uzavretá**: Dodávka na subdodávateľskú zmluvu je dokončená.<br/>• **Zrušená**: Subdodávka bola zrušená a neplánuje sa žiadna dodávka.  | 
    | Mena | Mena, v ktorej sa nakupujú výrobky a služby. Predvolená hodnota je automaticky zadaná z účtu dodávateľa, ale je možné ju zmeniť. | Mena subkontraktu sa používa na výber nákupného cenníka buď z cenníkov, ktoré sú pripojené k príslušnému dodávateľovi, alebo z parametrov projektu. Cenníky v inej mene nemožno spájať so subdodávkou. Náklady na čas, výdavky a materiály, ktoré dodávateľské zdroje dodajú z tejto subdodávky, sú v projekte zaznamenané v tejto mene. Po uložení záznamu o subdodávke nie je možné zmeniť menu subdodávky.|
    | Zmluvná jednotka | Divízia spoločnosti, ktorá s predajcom uzatvára kúpnu zmluvu alebo subdodávateľskú zmluvu. | Nie je |
    | Platobné podmienky | Platobné podmienky na faktúrach dodávateľa, ktoré sú vystavené na základe tejto subdodávky. Predvolená hodnota je automaticky zadaná z účtu dodávateľa. | Platobné podmienky zo subdodávky sa skopírujú do všetkých faktúr dodávateľov, ktoré súvisia s touto subdodávkou. Platobné podmienky je možné aktualizovať, ak má subdodávka stav **Koncept**. | 
    | Platobná adresa | Adresa dodávateľa, ktorému musia byť platby zaslané. Predvolená hodnota je automaticky zadaná z účtu dodávateľa. | Platobná adresa zo subdodávky sa skopíruje ako platobná adresa do všetkých faktúr dodávateľov, ktoré sú pre túto subdodávku vytvorené. Platobnú adresu je možné aktualizovať, ak má subdodávka stav **Koncept**.|
    | Fakturačné meno | Meno osoby alebo divízie v spoločnosti dodávateľa, ktorá bude odosielať faktúru. Predvolená hodnota je automaticky zadaná z účtu dodávateľa. | Hodnota **Fakturačné meno** zo subdodávky sa skopírujú do všetkých faktúr dodávateľov, ktoré súvisia s touto subdodávkou. Toto pole je možné aktualizovať, ak má subdodávka stav **Koncept**.|
    | Fakturovať na adresu | Adresa, ktorá sa používa na faktúrach od dodávateľa. Predvolená hodnota je automaticky zadaná z účtu dodávateľa. | Táto adresa je adresa „faktúry od“ na faktúrach dodávateľov, ktoré boli vytvorené pre túto subdodávku. |
    | Medzisúčet | Ak subdodávka nemá riadky, zadajte medzisúčet objednávky pred zdanením. Ak má subdodávateľská zmluva riadky, toto pole je len na čítanie. Suma, ktorá je zobrazená, je medzisúčetom zo všetkých riadkov subdodávky. | Nie je |
    | Daň celkom | Ak subdodávka nemá riadky, zadajte celkovú hodnotu dane na tejto subdodávke. Ak má subdodávateľská zmluva riadky, toto pole je len na čítanie. Suma, ktorá je zobrazená, je súčtom čiastok daní zo všetkých riadkov subdodávky. | Nie je |
    | Celková čiastka | Toto vypočítané pole ukazuje celkovú sumu subdodávateľskej zmluvy po zahrnutí daní. | Nie je |
    | Dátum potvrdenia | Dátum potvrdenia subdodávateľskej zmluvy. | Nie je |
    | Požiadal používateľ | Štandardne je toto pole nastavené na meno používateľa, ktorý vytvára subdodávku. Tvorca subdodávky však môže hodnotu zmeniť tak, aby označil osobu, pre ktorú subdodávku vytvára. | Nie je |
    | Account manažér dodávateľa | Názov primárneho kontaktu obchodného vzťahu dodávateľa. Predvolená hodnota je automaticky zadaná z účtu dodávateľa. Ako správcu účtu dodávateľa subdodávky môžete vybrať iný kontakt. | Môžete nastaviť e-mailové upozornenia na upozornenie kontaktu na zmeny subdodávky v dôsledku vyjednávania o cene. |
