---
title: Nastavenie cenníka predaja
description: Táto téma poskytuje informácie o cenníkoch predaja pre naceňovanie projektov.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896480"
---
# <a name="sales-price-list-setup"></a>Nastavenie cenníka predaja

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
