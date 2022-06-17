---
title: Uzavretie cenovej ponuky – čiastočné
description: Tento článok poskytuje informácie o uzatvorení cenovej ponuky v Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e3a199843f379dc53d63372f91e8be2e1bcbf4e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916951"
---
# <a name="close-a-quote---lite"></a>Uzavretie cenovej ponuky – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Cenovú ponuku projektu je možné uzavrieť ako Získaná alebo Nevyužitá. Koncept cenovej ponuky je možné uzavrieť, pretože operácie Aktivovať a Upraviť pre cenovú ponuku nie sú v Microsoft Dynamics 365 Project Operations podporované.

## <a name="close-a-quote-as-won"></a>Uzavretie cenovej ponuky ako Získaná

Keď uzavriete ponuku projektu ako Získaná, stav sa nastaví na Uzavretá a dôvod stavu je Získaná. Po uzavretí budú cenové ponuky projektu iba na čítanie a vytvorí sa koncept projektovej zmluvy so všetkými informáciami o cenovej ponuke. Pretože uzavretú cenovú ponuku nie je možné znovu otvoriť, vaše zmeny sa potvrdia v potvrdzovacom dialógovom okne.

Ak je cenová ponuka pripojená k príležitosti, akékoľvek ďalšie projektové ponuky týkajúce sa príležitosti sa automaticky uzavrú ako nezískané.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finančný dopad uzavretia cenovej ponuky nastavenej ako Získaná

Ak v projekte existujú časové údaje, zatiaľ čo je ešte pripojený k návrhu cenovej ponuky, zaznamenajú sa iba náklady na čas alebo výdavky. Po uzavretí cenovej ponuky ako získanej bude aplikácia refaktorovať náklady obrátením starších skutočných nákladov a opätovným vytvorením nových skutočných nákladov. Aplikácia spracuje tieto skutočné náklady na základe metódy fakturácie súvisiacej s riadkom zmluvy projektu. Ak sa skutočné náklady odvolávajú na časový a materiálny riadok zmluvy, zodpovedajúce nevyúčtované predajné skutočnosti sa vytvoria, keď sa ponuka uzavrie a vytvorí sa projektová zmluva. Ak sa skutočná cena odvoláva na riadok zmluvy so stanovenou cenou, aplikácia zastaví spracovanie skutočných nákladov, ktoré sú založené na pravidlách rozdeleného fakturovania pre zákazníkov projektovej zmluvy.

## <a name="closing-a-quote-as-lost"></a>Uzavretie cenovej ponuky ako nevyužitej:

Keď uzavriete ponuku projektu ako Nevyužitá, stav sa nastaví na Uzavretá a dôvod stavu je Nevyužitá. Uzavretie cenovej ponuky spôsobí, že ponuka projektu bude iba na čítanie. Keďže uzavretú cenovú ponuku nie je možné znovu otvoriť, tak pred zatvorením cenovej ponuky musíte svoje zmeny potvrdiť v dialógovom okne.

Ak projektová cenová ponuka, ktorá je uzavretá ako Nezískaná, odkazuje na projekt v ktoromkoľvek z jeho riadkov, tento projekt sa tiež označí ako Zatvorený. Všetky rezervácie zdrojov od daného dňa budú zrušené.

> [!NOTE]
> V rámci Project Operations uzavretie ponuky ako Získaná or Nevyužitá nebude mať vplyv na tento stav príležitosti, ktorá zostane otvorená, kým sa manuálne neuzavrie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]