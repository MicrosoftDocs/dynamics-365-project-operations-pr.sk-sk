---
title: Nastavenie predajného cenníka
description: Táto téma poskytuje informácie o cenníkoch predaja pre naceňovanie projektov.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 712dedb6766ff36181e261a66f3af99469449574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004910"
---
# <a name="set-up-a-sales-price-list"></a>Nastavenie predajného cenníka

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

V prípade projektových ponúk a zmlúv má cenník projektu odlišný vzor prepísania ceny ako cenník produktov. V radku cenovej ponuky založenej na katalógu produktov, môžete prepísať cenu do rolí a kategórií priamo v riadku cenovej ponuky, pretože každý riadok cenovej ponuky poukazuje na presne jednu položku katalógu. V riadku cenovej ponuky založenej na projekte však nie je možné prepísať cenu na roly a kategórie priamo v riadku cenovej ponuky. Môžete použiť cenník projektu na prácu s dvoma odlišnými vzormi prepísania.

> [!NOTE]
> Odporúčame, že máte samostatný cenník pre vaše projektové zdroje a položky katalógu, kvôli rozdielom v správaní medzi oboma pri prepismi cenotvorby.

Každá z nasledujúcich entít môže mať jednu alebo viac priradených predajných cenníkov pre cenotvorbu projektu:

- Zákaznícke (konto) 
- Príležitosť 
- Cenová ponuka 
- Projektová zmluva

Združenie týchto entít s cenníkmi je indikované projektovými cenníkmi. Môžete priradiť jeden alebo viac cenníkov s entitami zákazníka, príležitosti, cenovej ponuky a projektovej predajnej zmluvy.

Predvolený zoznam projektových cenníkov nie je automaticky zadaný v zázname zákazníka. Zoznam projektových cenníkov však môžete manuálne priložiť k záznamu zákazníka. Avšak, mali by ste manuálne priložiť projektový cenník len vtedy, ak máte vlastnú cenovú dohodu so zákazníkom. 

Ak je zoznam projektových cenníkov pripojený k predajnej entite, overujú sa nasledujúce informácie:

- Cenník má kontext **Predaj**. 
- Mena zákazníka sa musí zhodovať s menou uvedenou v cenníku. 

Na projektovej zmluve sa používa nasledujúce poradie priority na automatické nastavenie súvisiacich projektových cenníkov:

1. Ponuka
2. Príležitosť
3. Zákazník 
4. Globálne nastavenia 

Ak je projektový cenník predvolene zadaný, systém overí, či mena zodpovedá mene zákazníka, a či predvolené cenníky, ktoré boli zadané, majú kontext **Predaj**.

Môžete priradiť viacero cenníkov s entitami zákazníka, príležitosti, cenovej ponuky a projektovej zmluvy. Táto funkcia podporuje predvolený dátum predvolené ceny pre dlho-bežiaci projekt zmluvy, kde môžete požadovať viac ako jeden cenník na účet pre cenové aktualizácie, ktoré nastanú z dôvodu inflácie. Ak však cenové zoznamy, ktoré priradíte k entite zákazník, príležitosť, cenová ponuka alebo zmluva o projekte, majú prekrývajúcu sa účinnosť dátumu, predvolené ceny môžu byť nesprávne. Preto by ste sa mali uistiť, že projektové cenníky, ktoré majú prekrývanie dátumovej efektívnosti nie sú spojené s týmito entitami.


[!INCLUDE[footer-include](../includes/footer-banner.md)]