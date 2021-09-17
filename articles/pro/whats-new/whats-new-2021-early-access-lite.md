---
title: Novinky v rámci skoršieho prístupu v 2. vlne vydaní na rok 2021 – čiastočné nasadenie Project Operations
description: Táto téma poskytuje informácie o funkciách, ktoré sú k dispozícii v rámci skoršieho prístupu k 2. vlne vydaní na rok 2021 Project Operations s čiastočným nasadením.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323930"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Novinky v rámci skoršieho prístupu v 2. vlne vydaní na rok 2021 – čiastočné nasadenie Project Operations

_Platí pre: Čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

  - Project Operations v prostredí Dataverse verzie 4.23.0.4

Vydanie sa použije iba vtedy, ak je prostredie [zaregistrované do skoršieho prístupu](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

[Správa subdodávateľských zmlúv](../subcontracting/subcontracting_EA_scope.md) – Táto funkcia poskytuje lepšiu viditeľnosť a kontrolu nad všetkými aspektmi práce na projekte. Ukážka správy subdodávateľských zmlúv obsahuje nasledujúce možnosti:

  - Projektový manažér môže vytvoriť subdodávateľskú zmluvu s dodávateľom. Pre subdodávateľskú zmluvu sa štandardne používajú cenníky, ktoré sú pripojené k záznamu dodávateľa. Dodávateľský obchodný vzťah má typ vzťahu **Dodávateľ** alebo **Poskytovateľ**.
  - Projektový manažér môže všetky nákupy podrobne rozpísať ako riadkové položky v subdodávateľskej zmluve. Riadky subdodávateľskej zmluvy môžu byť pre čas, náklady alebo produkty. Trieda transakcie riadka subdodávateľskej zmluvy určuje, na čo je daný riadok určený.
  - Account manažér dodávateľa a projektový manažér môžu iterovať prostredníctvom subdodávateľskej zmluvy. Ceny možno upravovať v nákupných cenníkoch, ktoré sú pripojené k subdodávateľskej zmluve.
  - Počas tohto procesu, ak je riadok subdodávateľskej zmluvy určený pre čas, account manažér dodávateľa môže spojiť kontakty dodávateľa s každým riadkom subdodávateľskej zmluvy. Toto priradenie poskytuje informácie projektovému manažérovi, ktorý pracuje na subdodávateľskej zmluve. Keď je kontakt dodávateľa priradený k riadku subdodávateľskej zmluvy, systém automaticky vytvorí rezervovateľný zdroj z kontaktu, ak rezervovateľný zdroj ešte neexistuje.
  - Spôsob fakturácie na každom riadku subdodávateľskej zmluvy môže byť Pevná cena alebo Čas a materiál. V prípade riadkov subdodávateľských zmlúv s pevnou cenou sa nastaví plán faktúr založený na medzníkoch.
