---
title: Časté otázky pre správu zdrojov
description: Táto téma obsahuje odpovede na často kladené otázky týkajúce sa správy zdrojov.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755637"
---
# <a name="resource-management-faq"></a>Časté otázky pre správu zdrojov

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Aký je rozdiel medzi členom tímu a požiadavkou na zdroje?

Člen projektového tímu môže byť priradený k úlohám, môže byť rezervovaný alebo prerezervovaný a nastavený ako schvaľovateľ. Požiadavka na zdroje môže existovať bez člena projektového tímu, ako koncept poznámky o dopyte. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Aký je rozdiel medzi navrhnutými a predbežne rezervovanými hodinami?

Navrhované hodiny a predbežne rezervované hodiny sa líšia vo viditeľnosti. Navrhované hodiny sú viditeľné len pre správcov zdrojov a projektového manažéra, ktorý inicioval dopyt pomocou požiadavky na zdroje. Predbežne rezervované hodiny sú viditeľné pre každého, kto má prístup k tabuli plánovania.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Ako môžem zobraziť predbežne rezervované hodiny pre zdroje v tíme?

Predbežné rezervácie možno uskutočniť pri rezervácii požiadavky o zdroj. Zdroje, ktoré sú predbežne rezervované v projektovom tíme, sa zobrazujú ako členovia tímu, ktorí majú predbežne rezervované hodiny. Zobrazia sa tiež na tabuli plánu.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Ako zmením požadované hodiny a počiatočný a koncový dátum pre zdroj (všeobecný alebo pomenovaný), ktorý som rezervoval?

Po rezerváciách zdrojov vyberte položku **Spravovanie rezervácií**, aby ste mohli vykonať požadované zmeny.

## <a name="what-resources-types-does-project-service-automation-support"></a>Aké typy prostriedkov podporuje Project Service Automation?

**Používateľ** a **Kontakt** sú jedinými typmi prostriedkov, ktoré sú podporované v Dynamics 365 Project Service Automation. Aj keď môžete vytvoriť iné typy zdrojov (napríklad **Zariadenie** a **Skupina**), nie je pre nich podporovaný žiadny prípad použitia end-to-end.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Aký je rozdiel medzi priradením a rezerváciou?

Priradenia sú priraďovanie zdrojov k projektovým úlohám v pláne projektu. Zdroje môžu byť buď skutočnými, alebo všeobecnými zdrojmi. Rezervácie sú pevné alebo predbežné alokácie zdrojov k projektu. Pevné rezervácie spotrebúvajú kapacitu zdroja. V ideálnom prípade sa pri reálnych zdrojoch musia rezervácie a priradenia zhodnúť, pretože sa nelíšia. Avšak, PSA nepresadzuje túto zmluvu. V zobrazení Vyrovnanie sa zobrazuje projektový manažér, v ktorom nesúhlasia rezervácie a priradenia.
