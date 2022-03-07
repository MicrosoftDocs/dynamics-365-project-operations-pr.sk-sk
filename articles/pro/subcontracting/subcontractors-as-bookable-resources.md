---
title: Nastavenie subdodávateľov ako rezervovateľné zdroje
description: Táto téma vysvetľuje, ako nastaviť a udržiavať zdroje subdodávateľov, ktoré sú vytvorené z používateľov a kontaktov v systéme, aby ich bolo možné priradiť k subdodávateľským zmluvám v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c765e3c423e440f092c92f9bab75304914b0609447f1dc1c014f98801561b7a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994205"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Nastavenie subdodávateľov ako rezervovateľné zdroje

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Ak chcete nastaviť subdodávateľov ako rezervovateľné zdroje v Microsoft Dynamics 365 Project Operations, postupujte podľa týchto krokov.

1. Prejdite do **Projekt** \> **Zdroje** a vyberte položku **Nový**.
2. Na stránke **Nový rezervovateľný zdroj** v poli **Typ zdroja** vyberte jednu z nasledujúcich možností:

    - **Používateľ** – Tento typ zdroja zvoľte, ak subdodávateľ musí pristupovať k Project Operations, aby zadal čas alebo náklady. Ak vyberiete **Používateľ**, subdodávateľ vyžaduje na prístup do systému platnú licenciu.
    - **Kontakt** alebo **Obchodný vzťah** – Vyberte jeden z týchto typov zdrojov, ak subdodávateľ nevyžaduje prístup k Project Operations, ale musí byť k dispozícii na zadávanie priradení alebo rezervácií projektov. Žiadny z týchto typov zdrojov neposkytuje prístup do systému. Vyberte **Obchodný vzťah** na reprezentáciu spoločnosti dodávateľa ako rezervovateľný zdroj. Vyberte **Kontakt** na reprezentáciu jednotlivých zamestnancov dodávateľa.

3. V závislosti od typu zdroja, ktorý ste vybrali, sa zobrazí výzva na výber zodpovedajúceho záznamu o používateľovi, obchodnom vzťahu alebo kontakte.
4. V poli **Typ pracovníka** vyberte „Zmluvný pracovník“ a nastavte subdodávateľa ako rezervovateľný zdroj.

    > [!NOTE]
    > Ak necháte pole **Typ pracovníka** prázdne, rezervovateľný zdroj bude považovaný za zamestnanca.

5. Ak ste vybrali ako typ pracovníka **Zmluvný pracovník**, vyberte dodávateľa, pre ktorého zdroj pracuje.
6. Vyberte časové pásmo zdroja a potom vyberte **Uložiť**. Ak chcete priradiť šablónu pracovnej doby k rezervovateľnému zdroju, môžete vybrať **Nastaviť kalendár** na stránke so zoznamom **Rezervovateľný zdroj**.

Aby bol rezervovateľný zdroj priradený k riadku subdodávateľskej zmluvy, musí splniť tieto podmienky:

- Rezervovateľný zdroj musí byť zmluvný pracovník.
- Rezervovateľný zdroj typu zdroja **Kontakt** typ zdroja musí byť priradený k dodávateľskému obchodnému vzťahu ako kontakt. Rezervovateľný zdroj typu zdroja **Používateľ** typ zdroja nemusí byť priradený k dodávateľskému obchodnému vzťahu ako kontakt.
- Hodnota poľa **Dodávateľ** pre rezervovateľný zdroj sa musí zhodovať s hodnotou poľa **Dodávateľ** pre subdodávateľskú zmluvu.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Aktualizujte typ mapovania pracovníkov a dodávateľov pre rezervovateľné zdroje

Pole **Typ pracovníka** pre rezervovateľný zdroj určuje, či je rezervovateľným zdrojom zmluvný pracovník alebo zamestnanec. Pole **Dodávateľ** definuje dodávateľský obchodný vzťah, ku ktorému je rezervovateľný zdroj priradený. Priradením rezervovateľného zdroja k dodávateľovi ako kontaktu uvádzate, že kontakt je zamestnancom spoločnosti dodávateľa.

Ak polia **Typ pracovníka** a **Dodávateľ** pre rezervovateľný zdroj sa zmenia, zmeny ovplyvnia všetky budúce overenia nových záznamov, ktoré rezervovateľný zdroj vytvorí, napríklad časové záznamy. Tieto zmeny však nespôsobia neplatnosť existujúcich záznamov.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
