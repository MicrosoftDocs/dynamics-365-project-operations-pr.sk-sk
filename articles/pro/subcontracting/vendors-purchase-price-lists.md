---
title: Správa cenníka dodávateľa a nákupu v Project Operations
description: Táto téma poskytuje informácie, ktoré vám pomôžu vytvoriť a udržiavať údaje o dodávateľoch a cenníky nákupov pre subdodávateľov.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994160"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Správa cenníka dodávateľa a nákupu v Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

## <a name="vendors-in-project-operations"></a>Dodávatelia v Project Operations

V Microsoft Dynamics 365 Project Operations majú dodávateľské obchodné vzťahy typ vzťahu **Dodávateľ** alebo **Poskytovateľ**. Ako dodávateľa v rámci subdodávateľskej zmluvy môžete vybrať iba záznam obchodného vzťahu, ktorý má jeden z týchto typov vzťahov.

K záznamu dodávateľa môžete priradiť jeden alebo viac nákupných cenníkov. Každý nákupný cenník, ktorý je spojený so záznamom dodávateľa, by však mal mať odlišnú účinnosť podľa dátumu. Project Operations nepodporuje prekrývanie účinnosti podľa dátumu v nákupných cenníkoch.

Nasledujúce polia a koncepty v zázname dodávateľa sa predvolene používajú pre akúkoľvek subdodávateľskú zmluvu, ktorá je vytvorená pre dodávateľa:

- Platobné podmienky
- Kontakt platiteľa
- Primárny kontakt

    > [!NOTE]
    > V predvolenom nastavení sa ako account manažér dodávateľa subdodávky použije primárny kontakt dodávateľa.

- Mena
- Aktuálne nákupné cenníky

## <a name="purchase-price-lists-in-project-operations"></a>Nákupné cenníky v Project Operations

Cenník, kde je pole **Kontext** nastavené na **Nákup** sa považuje za nákupný cenník. Nákupné cenníky je možné definovať tak, aby predstavovali katalóg nákupných sadzieb pre čas, náklady a materiál. Nákupné cenníky sa podobajú cenníkom obstarávacích cien a predajným cenníkom v Project Operations. Nasledujúce koncepty sa vzťahujú na nákupné cenníky rovnakým spôsobom, akým sa vzťahujú na cenníky obstarávacích cien a predajné cenníky:

- **Účinnosť podľa dátumu** – Nákupné cenníky majú účinnosť podľa dátumu. Účinnosť podľa dátumu je reprezentovaná poľami počiatočného a konečného dátumu v každom cenníku. Čas medzi počiatočným a koncovým dátumom je obdobím účinnosti.
- **Mena** – Mena v hlavičke cenníka sa používa ako mena, v ktorej sú nákupné ceny vyjadrené pre prácu, kategórie výdavkov a výrobky v katalógu.
- **Predvolená časová jednotka** – Predvolená časová jednotka vyjadruje ceny práce pre nákupy. Pole časovej jednotky v cenníku slúži iba na poskytnutie predvolenej hodnoty. Túto hodnotu je možné zmeniť v jednotlivých riadkov Cena roly.

Nákupné cenníky je možné pripojiť k záznamom dodávateľov ako priradenia, ktoré sú známe ako cenníky projektov. Tieto cenníky sa používajú na zadávanie predvolených cien v riadkoch subdodávateľských zmlúv. Keď je k záznamu dodávateľa pripojených viac nákupných cenníkov, predvolene sa pre subdodávateľské zmluvy, ktoré sú vytvorené pre dodávateľa, použije najaktuálnejší cenník. Iba cenníky, kde je pole **Kontext** nastavené na **Nákup** je možné pripojiť k záznamom dodávateľov.

### <a name="subcontract-specific-purchase-price-lists"></a>Nákupné cenníky špecifické pre subdodávateľov

Nákupné cenníky je tiež možné pripojiť k subdodávateľským zmluvám ako priradenia, ktoré sú známe ako cenníky projektov. Tieto cenníky sa používajú na zadávanie predvolených cien v riadkoch subdodávateľských zmlúv. Keď je k subdodávateľskej zmluve priložených viac nákupných cenníkov, každý z nich musí mať rozdielnu dátumovú účinnosť. Project Operations nepodporuje nákupné cenníky, ktoré majú prekrývajúcu sa dátumovú účinnosť. Iba cenníky, kde je pole **Kontext** nastavené na **Nákup** je možné pripojiť k subdodávateľským zmluvám.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
