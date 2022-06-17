---
title: Novinky v rámci skoršieho prístupu v 2. vlne vydaní na rok 2021 – čiastočné nasadenie Project Operations
description: Tento článok poskytuje informácie o funkciách dostupných vo verzii 2021 s predčasným prístupom zjednodušeného nasadenia Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924127"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Novinky v rámci skoršieho prístupu v 2. vlne vydaní na rok 2021 – čiastočné nasadenie Project Operations

_Platí pre: Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok sa vzťahuje na nasledujúce Dynamics 365 Project Operations komponenty a verzie:

  - Project Operations v prostredí Dataverse verzie 4.23.0.4

Vydanie sa použije iba vtedy, ak je prostredie [zaregistrované do skoršieho prístupu](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

[Správa subdodávateľských zmlúv](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) – Táto funkcia poskytuje lepšiu viditeľnosť a kontrolu nad všetkými aspektmi práce na projekte. Ukážka správy subdodávateľských zmlúv obsahuje nasledujúce možnosti:

  - Projektový manažér môže vytvoriť subdodávateľskú zmluvu s dodávateľom. Pre subdodávateľskú zmluvu sa štandardne používajú cenníky, ktoré sú pripojené k záznamu dodávateľa. Dodávateľský obchodný vzťah má typ vzťahu **Dodávateľ** alebo **Poskytovateľ**.
  - Projektový manažér môže všetky nákupy podrobne rozpísať ako riadkové položky v subdodávateľskej zmluve. Riadky subdodávateľskej zmluvy môžu byť pre čas, náklady alebo produkty. Trieda transakcie riadka subdodávateľskej zmluvy určuje, na čo je daný riadok určený.
  - Account manažér dodávateľa a projektový manažér môžu iterovať prostredníctvom subdodávateľskej zmluvy. Ceny možno upravovať v nákupných cenníkoch, ktoré sú pripojené k subdodávateľskej zmluve.
  - Počas tohto procesu, ak je riadok subdodávateľskej zmluvy určený pre čas, account manažér dodávateľa môže spojiť kontakty dodávateľa s každým riadkom subdodávateľskej zmluvy. Toto priradenie poskytuje informácie projektovému manažérovi, ktorý pracuje na subdodávateľskej zmluve. Keď je kontakt dodávateľa priradený k riadku subdodávateľskej zmluvy, systém automaticky vytvorí rezervovateľný zdroj z kontaktu, ak rezervovateľný zdroj ešte neexistuje.
  - Spôsob fakturácie na každom riadku subdodávateľskej zmluvy môže byť Pevná cena alebo Čas a materiál. V prípade riadkov subdodávateľských zmlúv s pevnou cenou sa nastaví plán faktúr založený na medzníkoch.
