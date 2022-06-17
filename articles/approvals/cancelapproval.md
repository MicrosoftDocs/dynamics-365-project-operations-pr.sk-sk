---
title: Zrušte schválenie predtým schválených záznamov
description: Tento článok vysvetľuje, ako môže projektový manažér zrušiť schválenie predtým schválených záznamov o čase, výdavkoch alebo spotrebe materiálu.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930475"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Zrušte schválenie predtým schválených záznamov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Projektový manažér alebo schvaľovateľ, ktorý predtým schválil položky času, nákladov alebo spotreby materiálu, môže zrušiť schválenie týchto položiek. 

Ak chcete zrušiť schválenie predtým schváleného záznamu o čase, výdavkoch alebo spotrebe materiálu, postupujte podľa týchto krokov.

1. Prejdite na **projekty** \> **moja práca** \> **schválenia**.
2. The **Schválenia** stránka so zoznamom zobrazuje všetky časové záznamy, ktoré čakajú na schválenie. Zmeňte zobrazenie na **Moje predchádzajúce schválenia**.
3. Vyberte schválenie času, výdavkov alebo materiálu, ktoré chcete zrušiť. Potom na paneli akcií vyberte **Zrušiť schválenie**.
4. V okne s potvrdením, ktoré sa zobrazí, vyberte **OK** na potvrdenie operácie.

> [!IMPORTANT]
> Nemôžete zrušiť schválenie predtým schváleného záznamu o čase, výdavkoch a spotrebe materiálu, ktorý už bol zákazníkovi fakturovaný. Ak to skúsite, dostanete správu, že schválenie nie je možné zrušiť, pretože už bolo vyfakturované. V tomto prípade môžete odsúhlasenie zrušiť iba v prípade, že opravná faktúra je použitá na vystavenie celého dobropisu alebo vrátenie peňazí zákazníkovi na pôvodnej faktúre.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Vplyv zrušenia schválenia predtým schváleného zápisu

Ak sa schválenie zruší, existuje prevádzkový dopad aj finančný dopad.

### <a name="operational-impact"></a>Prevádzkový vplyv

Ak je schválenie zápisu zrušené, záznam o schválení je označený ako **Predložené**. Stav záznamu sa zmení na **Predložené**. V tejto fáze môže člen projektového tímu odvolať položku bez odoslania žiadosti o stiahnutie.

Schvaľovateľ môže zmeniť **Fakturovateľné množstvo** a **Typ fakturácie** hodnoty a potom schválte záznam ešte raz.

### <a name="financial-impact"></a>Finančný vplyv

Ak je schválenie záznamu zrušené, zodpovedajúce skutočné náklady a tržby sa aktualizujú nasledujúcim spôsobom:

- Pole **Stav úpravy** sa aktualizuje na **Upravené**.
- Pole **Stav fakturácie** sa aktualizuje na **Zrušené**.

Ďalšie, storno položky sú vytvorené v tabuľke skutočné údaje. Ak chcete vytvoriť storno položky, systém skopíruje hodnoty polí z pôvodných skutočných hodnôt. Iba hodnoty, ktoré nie sú skopírované, sú hodnoty množstva. Tieto hodnoty sa namiesto toho obrátili. Obrátené skutočné hodnoty sú vytvorené pre skutočné hodnoty **nákladov**, aj pre **nefakturovaných predajov**. Pole **Stav úpravy** na vrátených skutočných hodnotách je nastavené na **Neupraviteľné** a pole **Stav fakturácie** je nastavené na **Zrušené**. V dôsledku týchto zmien sa zaznamenané výdavky a backlog príjmov na projekte nebudú viac vzťahovať na sumy, ktoré tieto skutočné hodnoty predstavujú.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
