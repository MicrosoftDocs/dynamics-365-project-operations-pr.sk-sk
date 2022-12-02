---
title: Zrušenie schválenia predtým schválených zadaní
description: Tento článok vysvetľuje, ako môže projektový manažér zrušiť schválenie predtým schválených zadaní času, výdavkov alebo spotreby materiálu.
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
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Zrušenie schválenia predtým schválených zadaní

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Projektový manažér alebo schvaľovateľ, ktorý predtým schválil zadania času, výdavkov alebo použitia materiálov, môže svoje schválenie týchto zadaní zrušiť. 

Ak chcete zrušiť schválenie predtým schváleného zadania času, výdavkov alebo použitia materiálov.

1. Prejdite na **projekty** \> **moja práca** \> **schválenia**.
2. Stránka so zoznamom **schválení** zobrazuje všetky časové zadania, ktoré čakajú na schválenie. Zmeňte zobrazenie na **Moje predchádzajúce schválenia**.
3. Vyberte schválenie času, výdavkov alebo materiálu, ktoré chcete zrušiť. Na table Akcia následne vyberte **Zrušiť schválenie**.
4. V zobrazenom potvrdzujúcom hlásení vyberte položku **OK** na potvrdenie úkonu.

> [!IMPORTANT]
> Nemôžete zrušiť schválenie predtým schváleného zadania času, výdavkov alebo použitia materiálu, ktoré už boli fakturované zákazníkovi. Ak sa o to pokúsite, zobrazí sa správa, ktorá uvádza, že schválenie nie je možné zrušiť, pretože už bolo fakturované. V takom prípade môžete zrušiť schválenie iba vtedy, ak sa opravná faktúra použije na vystavenie plného dobropisu alebo vrátenie peňazí zákazníkovi na pôvodnej faktúre.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Vplyv zrušenia schválenia na predtým schválené zadanie

Ak sa schválenie zruší, existuje prevádzkový dopad aj finančný dopad.

### <a name="operational-impact"></a>Prevádzkový vplyv

Ak je schválenie zadania zrušené, záznam o schválení je označený ako **Odoslané**. Stav záznamu sa zmení na **Odoslané**. V tejto etape môže člen projektového tímu stiahnuť zadanie bez odoslania žiadosti o stiahnutie.

Schvaľovateľ môže zmeniť hodnoty **Fakturovateľné množstvo** a **Typ fakturácie** a potom schváliť zadanie ešte raz.

### <a name="financial-impact"></a>Finančný vplyv

Ak bude schválenie zadania zrušené, zodpovedajúce skutočné hodnoty nákladov a predaja sa aktualizujú nasledujúcim spôsobom:

- Pole **Stav úpravy** sa aktualizuje na **Upravené**.
- Pole **Stav fakturácie** sa aktualizuje na **Zrušené**.

Ďalšie, storno položky sú vytvorené v tabuľke skutočné údaje. Ak chcete vytvoriť storno položky, systém skopíruje hodnoty polí z pôvodných skutočných hodnôt. Iba hodnoty, ktoré nie sú skopírované, sú hodnoty množstva. Tieto hodnoty sa namiesto toho obrátili. Obrátené skutočné hodnoty sú vytvorené pre skutočné hodnoty **nákladov**, aj pre **nefakturovaných predajov**. Pole **Stav úpravy** na vrátených skutočných hodnotách je nastavené na **Neupraviteľné** a pole **Stav fakturácie** je nastavené na **Zrušené**. V dôsledku týchto zmien sa zaznamenané výdavky a backlog príjmov na projekte nebudú viac vzťahovať na sumy, ktoré tieto skutočné hodnoty predstavujú.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
