---
title: Novinky v rámci skoršieho prístupu v 2. vlne vydaní na rok 2021 – čiastočné nasadenie Project Operations
description: Táto téma poskytuje informácie o funkciách, ktoré sú k dispozícii v rámci skoršieho prístupu k 2. vlne vydaní na rok 2021 Project Operations s čiastočným nasadením.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7b5f3528e4b4e615b8e7f24bfd3702746fd584c9
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723695"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Novinky v rámci skoršieho prístupu v 2. vlne vydaní na rok 2021 – čiastočné nasadenie Project Operations

_Platí pre: Čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

  - Project Operations v prostredí Dataverse verzie 4.23.0.4

Vydanie sa použije iba vtedy, ak je prostredie [zaregistrované do skoršieho prístupu](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

[Správa subdodávateľských zmlúv](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) – Táto funkcia poskytuje lepšiu viditeľnosť a kontrolu nad všetkými aspektmi práce na projekte. Ukážka správy subdodávateľských zmlúv obsahuje nasledujúce možnosti:

  - Projektový manažér môže vytvoriť subdodávateľskú zmluvu s dodávateľom. Pre subdodávateľskú zmluvu sa štandardne používajú cenníky, ktoré sú pripojené k záznamu dodávateľa. Dodávateľský obchodný vzťah má typ vzťahu **Dodávateľ** alebo **Poskytovateľ**.
  - Projektový manažér môže všetky nákupy podrobne rozpísať ako riadkové položky v subdodávateľskej zmluve. Riadky subdodávateľskej zmluvy môžu byť pre čas, náklady alebo produkty. Trieda transakcie riadka subdodávateľskej zmluvy určuje, na čo je daný riadok určený.
  - Account manažér dodávateľa a projektový manažér môžu iterovať prostredníctvom subdodávateľskej zmluvy. Ceny možno upravovať v nákupných cenníkoch, ktoré sú pripojené k subdodávateľskej zmluve.
  - Počas tohto procesu, ak je riadok subdodávateľskej zmluvy určený pre čas, account manažér dodávateľa môže spojiť kontakty dodávateľa s každým riadkom subdodávateľskej zmluvy. Toto priradenie poskytuje informácie projektovému manažérovi, ktorý pracuje na subdodávateľskej zmluve. Keď je kontakt dodávateľa priradený k riadku subdodávateľskej zmluvy, systém automaticky vytvorí rezervovateľný zdroj z kontaktu, ak rezervovateľný zdroj ešte neexistuje.
  - Spôsob fakturácie na každom riadku subdodávateľskej zmluvy môže byť Pevná cena alebo Čas a materiál. V prípade riadkov subdodávateľských zmlúv s pevnou cenou sa nastaví plán faktúr založený na medzníkoch.
