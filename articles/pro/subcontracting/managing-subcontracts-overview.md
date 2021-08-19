---
title: Správa subdodávateľských zmlúv v aplikácii Project Operations
description: Táto téma prináša prehľad celého procesu správy subdodávateľských zmlúv v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994250"
---
# <a name="subcontract-management-in-project-operations"></a>Správa subdodávateľských zmlúv v aplikácii Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Subdodávateľské zmluvy v Microsoft Dynamics 365 Project Operations podporujú nasledujúci tok obchodného procesu.

![Postup procesu subdodávateľských zmlúv](../media/SubcontractingProcessFlow.png)

Tu je podrobný popis procesu subdodávateľských zmlúv.

1. Projektový manažér vytvorí subdodávateľskú zmluvu s dodávateľom. Pre subdodávateľskú zmluvu sa štandardne používajú cenníky, ktoré sú pripojené k záznamu dodávateľa. Dodávateľský obchodný vzťah má typ vzťahu **Dodávateľ** alebo **Poskytovateľ**.
2. Projektový manažér môže všetky nákupy podrobne rozpísať ako riadkové položky v subdodávateľskej zmluve. Riadky subdodávateľskej zmluvy môžu byť pre čas, náklady alebo produkty. Trieda transakcie, ktorá je vybratá na každom riadku subdodávateľskej zmluvy, určuje, na čo je daný riadok určený.
3. Account manažér dodávateľa a projektový manažér môžu iterovať prostredníctvom subdodávateľskej zmluvy. Ceny možno upravovať v nákupných cenníkoch, ktoré sú pripojené k subdodávateľskej zmluve.
4. V tomto bode alebo neskôr v procese, ak je riadok subdodávateľskej zmluvy určený pre čas, account manažér dodávateľa spojí kontakty s každým riadkom subdodávateľskej zmluvy. Toto priradenie poskytuje informácie projektovému manažérovi, ktorý pracuje na subdodávateľskej zmluve. Keď je kontakt priradený k riadku subdodávateľskej zmluvy, systém automaticky vytvorí rezervovateľný zdroj z kontaktu, ak rezervovateľný zdroj ešte neexistuje.
5. Spôsob fakturácie na každom riadku subdodávateľskej zmluvy môže byť **Pevná cena** alebo **Čas a materiál**. V prípade riadkov subdodávateľských zmlúv s pevnou cenou môžete nastaviť plán faktúr založený na medzníkoch.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
