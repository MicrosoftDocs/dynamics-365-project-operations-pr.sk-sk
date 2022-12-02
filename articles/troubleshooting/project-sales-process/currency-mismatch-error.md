---
title: Chyba nezhody mien
description: Tento článok poskytuje informácie o riešení problémov s chybou nezhody mien, ktorá sa vyskytuje pri ukladaní konkrétnych typov záznamov.
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
# <a name="currency-mismatch-error"></a>Chyba nezhody mien 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Pri ukladaní projektu, zmluvy, ponuky alebo rezervovateľného zdroja sa môže vyskytnúť chyba **Mena vlastniacej spoločnosti sa nezhoduje s menou zmluvnej jednotky. Ak chcete pokračovať, vyberte inú vlastniacu spoločnosť alebo zmluvnú jednotku**. Dôvodom je nesúlad meny medzi menou zmluvnej jednotky pre záznam a menou vlastniacej spoločnosti.


## <a name="resolution"></a>Povinné

Ak chcete vyriešiť tento problém, vykonajte nasledujúce:
- Pre tento záznam overte menu zmluvnej jednotky. Menu môžete zobraziť otvorením záznamu organizačnej jednotky a overením hodnoty na karte **Všeobecné** v poli **Mena**.
- Overte menu vlastniacej spoločnosti. Ak chcete zobraziť menu, prejdite na stránku **Súvisiace** > **Registre** vo firemnom zázname. Dvakrát kliknite na záznam registra, ktorý je priradený k spoločnosti, a overte hodnotu na karte **Všeobecné** v poli **Účtovná mena**.

Ak sa mena nastavená v zmluvnej jednotke a zázname registra nezhodujú, pri ukladaní záznamu upravte konfiguráciu alebo vyberte iné hodnoty. Systém vyžaduje, aby sa tieto záznamy zhodovali, aby sa zabezpečil správny medzipodnikový fakturačný tok. Ďalšie informácie o medzipodnikových konfiguráciách nájdete v časti [Vytváranie medzipodnikových transakcií](../../project-accounting/create-intercompany-transactions.md).

Ak záznam spoločnosti nemá priradený záznam registra, znamená to, že pri nastavovaní prostredia chýba konfigurácia. Konfiguráciu musí opraviť správca systému. Správca systému musí ísť do ponuky **Konfigurácie s duálnym zápisom** a zastaviť a reštartovať funkciu **Mapa duálneho zápisu do registra** s počiatočnou synchronizáciou tejto mapy a jej predpokladov. Ďalšie informácie nájdete v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../../environment/resource-dual-write-maps.md).
