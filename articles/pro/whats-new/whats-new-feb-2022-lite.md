---
title: Čo je nové vo februári 2022 – nasadenie aplikácie Project Operations Lite
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii v nasadení Project Operations Lite, vydanie z februára 2022.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922839"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Čo je nové vo februári 2022 – nasadenie aplikácie Project Operations Lite

_Platí pre: Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.28.0.120

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

Od tohto vydania môžete do jedného projektu pridať až 300 členov tímu. Predtým bol limit na počet členov tímu 150. Ďalšie informácie nájdete v dokumente [Limity projektu](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Aktualizácie kvality

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2497369 | Oprava materiálu musí nasledovať hodnotu dátumu v parametroch **Oprava**. |
| Fakturácia a tvorba cien | 2498697 | Vylepšená konfigurácia zabezpečenia pre **Odvolanie zadania času**. |
| Fakturácia a tvorba cien | 2517455 | Akcia **Obnovenie transakcie v riadku faktúry** nesmie byť povolená na spustenie akcie viackrát súčasne pre tú istú faktúru. |
| Fakturácia a tvorba cien | 2517465 | Akcia **Deaktivácia podrobností o riadku faktúry** je zablokovaná, pretože nie je podporovaná. |
| Fakturácia a tvorba cien | 2556660 | Opravené kontroly dátumu účinnosti, ktoré sa vykonávajú v cenníku, ktorý je priložený k záznamu parametrov projektu. |
| Správa príležitostí | 2369202 | Opravená obchodná logika, ktorá overuje, že cenníky, ktoré majú prekrývajúce sa dátumy účinnosti, možno pripojiť k tej istej zmluve o projekte. |
| Správa príležitostí | 2385965 | Opravené správanie na karte **Zákazníci** na stránke **Projektová zmluva** pri výbere možnosti **Uložiť a zavrieť**. |
