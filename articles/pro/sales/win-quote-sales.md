---
title: Uzavretie projektových cenových ponúk
description: Tento článok poskytuje informácie o uzatváraní cenovej ponuky v Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4335fa5467640af840c0f68a648c9b8a6864d834
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826195"
---
# <a name="close-project-quotes"></a>Uzavretie projektových cenových ponúk

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Cenovú ponuku projektu je možné uzavrieť ako Získaná alebo Nevyužitá. Koncept cenovej ponuky je možné uzavrieť, pretože operácie Aktivovať a Upraviť pre cenovú ponuku nie sú v Microsoft Dynamics 365 Project Operations podporované.

## <a name="close-a-quote-as-won"></a>Uzavretie cenovej ponuky ako Získaná

Keď uzavriete ponuku projektu ako Získaná, stav sa nastaví na Uzavretá a dôvod stavu je Získaná. Po uzavretí budú cenové ponuky projektu iba na čítanie a vytvorí sa koncept projektovej zmluvy so všetkými informáciami o cenovej ponuke. Pretože uzavretú cenovú ponuku nie je možné znovu otvoriť, vaše zmeny sa potvrdia v potvrdzovacom dialógovom okne.

Ak je cenová ponuka pripojená k príležitosti, akékoľvek ďalšie projektové ponuky týkajúce sa príležitosti sa automaticky uzavrú ako nezískané.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finančný dopad uzavretia cenovej ponuky nastavenej ako Získaná

Ak v projekte existujú časové údaje, zatiaľ čo je ešte pripojený k návrhu cenovej ponuky, zaznamenajú sa iba náklady na čas alebo výdavky. Po uzavretí cenovej ponuky ako získanej bude aplikácia refaktorovať náklady obrátením starších skutočných nákladov a opätovným vytvorením nových skutočných nákladov. Aplikácia spracuje tieto skutočné náklady na základe metódy fakturácie súvisiacej s riadkom zmluvy projektu. Ak sa skutočné náklady odvolávajú na časový a materiálny riadok zmluvy, zodpovedajúce nevyúčtované predajné skutočnosti sa vytvoria, keď sa ponuka uzavrie a vytvorí sa projektová zmluva. Ak sa skutočná cena odvoláva na riadok zmluvy so stanovenou cenou, aplikácia zastaví spracovanie skutočných nákladov, ktoré sú založené na pravidlách rozdeleného fakturovania pre zákazníkov projektovej zmluvy.

## <a name="closing-a-quote-as-lost"></a>Uzavretie citátu ako strateného

Keď uzavriete ponuku projektu ako Nevyužitá, stav sa nastaví na Uzavretá a dôvod stavu je Nevyužitá. Uzavretie cenovej ponuky spôsobí, že ponuka projektu bude iba na čítanie. Keďže uzavretú cenovú ponuku nie je možné znovu otvoriť, tak pred zatvorením cenovej ponuky musíte svoje zmeny potvrdiť v dialógovom okne.

Ak projektová cenová ponuka, ktorá je uzavretá ako Nezískaná, odkazuje na projekt v ktoromkoľvek z jeho riadkov, tento projekt sa tiež označí ako Zatvorený. Všetky rezervácie zdrojov od daného dňa budú zrušené.

> [!NOTE]
> V rámci Project Operations uzavretie ponuky ako Získaná or Nevyužitá nebude mať vplyv na tento stav príležitosti, ktorá zostane otvorená, kým sa manuálne neuzavrie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
