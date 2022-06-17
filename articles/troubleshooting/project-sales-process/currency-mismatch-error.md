---
title: Chyba nesúladu meny
description: Tento článok poskytuje informácie o riešení problémov s chybou nesúladu meny, ktorá sa vyskytuje pri ukladaní konkrétnych typov záznamov.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914743"
---
# <a name="currency-mismatch-error"></a>Chyba nesúladu meny 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Keď uložíte projekt, zmluvu, cenovú ponuku alebo rezervovateľný zdroj, môže sa zobraziť chyba, **Vlastná mena spoločnosti sa nezhoduje s menou zmluvnej jednotky. Ak chcete pokračovať, vyberte inú vlastnú spoločnosť alebo zmluvnú jednotku**. Je to preto, že existuje nesúlad meny medzi menou zmluvnej jednotky pre záznam a menou vlastníckej spoločnosti.


## <a name="resolution"></a>Povinné

Ak chcete tento problém obísť, postupujte takto:
- Pre tento záznam overte menu zmluvnej jednotky. Menu môžete zobraziť otvorením záznamu organizačnej jednotky a overením hodnoty na **generál** kartu v **mena** lúka.
- Overte menu vlastnej spoločnosti. Menu môžete zobraziť tak, že prejdete na **Súvisiace** > **účtovné knihy** vo firemnom zázname. Dvakrát kliknite na záznam hlavnej knihy, ktorý je priradený k spoločnosti, a overte hodnotu na **generál** kartu v **Účtovná mena** lúka.

Ak sa mena nastavená v zmluvnej jednotke a zázname hlavnej knihy nezhodujú, pri ukladaní záznamu upravte konfiguráciu alebo vyberte iné hodnoty. Systém vyžaduje, aby sa tieto záznamy zhodovali, aby sa zabezpečil správny medzipodnikový fakturačný tok. Ďalšie informácie o medzipodnikových konfiguráciách nájdete v časti [Vytvorte medzipodnikové transakcie](../../project-accounting/create-intercompany-transactions.md).

Ak záznam spoločnosti nemá priradený záznam hlavnej knihy, znamená to, že pri nastavovaní prostredia chýba konfigurácia. Konfiguráciu musí opraviť správca systému. Správca systému musí ísť na **Konfigurácie s duálnym zápisom** a zastaviť a reštartovať **Mapa s dvojitým zápisom do účtovných kníh** s počiatočnou synchronizáciou tejto mapy a jej predpokladmi. Ďalšie informácie nájdete v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../../environment/resource-dual-write-maps.md).
