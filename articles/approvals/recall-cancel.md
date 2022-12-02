---
title: Odvolanie predtým schválených zadaní
description: Tento článok vysvetľuje, ako môže člen projektového tímu požiadať o stiahnutie predtým predložených a schválených záznamov o čase, výdavkoch a použití materiálu a ako môže projektový manažér schváliť alebo zamietnuť žiadosti o stiahnutie.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930383"
---
# <a name="recall-previously-approved-entries"></a>Odvolanie predtým schválených zadaní

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Člen projektového tímu, ktorý odošle záznam o čase, výdavkoch alebo použití materiálu, môže stiahnuť tento záznam po jeho schválení. Proces stiahnutia zahŕňa dva hlavné kroky:

1. Odosielateľ požaduje stiahnutie.
2. Schvaľovateľ schvaľuje žiadosť o stiahnutie.

## <a name="request-a-recall"></a>Požiadať o stiahnutie

Tieto kroky použite na vyžiadanie stiahnutia schváleného zadania času, výdavkov alebo použitia materiálu.

1. Postupujte podľa jedného z týchto krokov v závislosti od typu záznamu, ktorý chcete stiahnuť:

    - V prípade položiek času prejdite do **Projekty** \> **Moja práca** \> **Zadanie času** a vyberte všetky položky času pre konkrétnu kombináciu projektu a úlohy. Prípadne v mriežke vyberte jednotlivé bunky pre čas v určitom dátume konkrétneho projektu.
    - Pre položky výdavkov Prejdite do **Projekty** \> **Moja práca** \> **Výdavky** a vyberte riadok pre položku výdavku na vyvolanie.
    - Pre položky použitia materiálu prejdite do **Projekty** \> **Moja práca** \> **Denník použitia materiálu** a vyberte riadok pre zadanie použitia materiálu, ktorý chcete stiahnuť.

2. Vyberte položku **Odvolať**. Zobrazí sa dialógové okno s potvrdením. Ak boli vybraté položky času, výdavkov alebo použitia materiálu už schválené, zobrazí sa výzva na zadanie dôvodu stiahnutia.
3. Zadajte dôvod stiahnutia a potom vyberte **OK**, čím potvrdíte operáciu. Systém odošle osobe, ktorá schválila položky, žiadosť o schválenie odvolania.

> [!IMPORTANT]
> Nemôžete vytvoriť požiadavku na stiahnutie pre schválený záznam o čase, výdavkoch alebo použitia materiálu, ktorý už bol fakturovaný zákazníkovi. Ak sa o to pokúsite, zobrazí sa správa, ktorá uvádza, že zadanie času, výdavku alebo použitia materiálu nemožno stiahnuť, pretože už boli fakturované. V takom prípade môžete požiadať o zrušenie zadania iba vtedy, ak sa opravná faktúra použije na vystavenie plného dobropisu alebo vrátenie peňazí zákazníkovi na pôvodnej faktúre.

## <a name="approve-or-reject-a-recall-request"></a>Schválenie alebo odmietnutie žiadosti o stiahnutie

Ak chcete schváliť alebo zamietnuť žiadosť o stiahnutie, postupujte podľa týchto krokov.

1. Prejdite na **projekty** \> **moja práca** \> **schválenia**.
2. Na stránke zoznamu **Schválenia** zmeňte zobrazenie na **Žiadosti o odvolanie na schválenie**. Zobrazí sa zoznam predložených žiadostí o stiahnutie.
3. Vyberte jednu alebo viac položiek a potom vyberte položku **Schváliť** alebo **Odmietnuť**.
4. Ak ste vybrali možnosť **Schváliť**, zobrazí sa upozorňujúce hlásenie, ktoré vysvetľuje vplyv schválenia. Stlačením možnosti **OK** potvrďte operáciu. Žiadosť o odvolanie bola schválená.

    -alebo-

    Ak ste vybrali **Odmietnuť**, žiadosť o odvolanie sa zamietne.

> [!IMPORTANT]
> Po schválení stiahnutia, rovnako ako pri jeho vyžiadaní, systém skontroluje, či sa v záznamoch o čase, výdavkoch alebo použití materiálu nenachádza nejaká fakturačná aktivita. Ak bola položka už fakturovaná, alebo ak je v návrhu faktúry, schvaľovateľovi sa zobrazí chybové hlásenie, ktoré uvádza, že čas alebo výdavky nemôžu byť schválené na stiahnutie, pretože to bolo už fakturované. V takom prípade môžete schvaľovateľ schváliť stiahnutie iba vtedy, ak sa opravná faktúra použije na vystavenie plného dobropisu alebo vrátenie peňazí zákazníkovi na pôvodnej faktúre.

## <a name="impact-of-a-recall-request"></a>Vplyv žiadosti o stiahnutie

Ak sa schválenie odmietne, existuje prevádzkový dopad aj finančný dopad.

### <a name="operational-impact"></a>Prevádzkový vplyv

Ak je žiadosť o odvolanie schválená, záznam o schválení je označený ako **Zamietnutý**. Stav položky sa zmení na **Vrátený** alebo **Zamietnutý** v závislosti od toho, či ide o časovú položku alebo položku výdavkov alebo použitia materiálu.

Člen projektového tímu môže zobraziť položky, upraviť ich a potom znova odoslať alebo položky úplne odstrániť.

Ak sa žiadosť o odvolanie zamietne, stav položky zostane **Schválený** a položku nie je možné upraviť členom projektového tímu alebo schvaľovateľa projektu.

### <a name="financial-impact"></a>Finančný vplyv

Ak dôjde k schváleniu žiadosti o odvolanie, zodpovedajúce skutočné hodnoty nákladov a predaja sa aktualizujú nasledujúcim spôsobom:

- Pole **Stav úpravy** sa aktualizuje na **Upravené**.
- Pole **Stav fakturácie** sa aktualizuje na **Zrušené**.

Ďalšie, storno položky sú vytvorené v tabuľke skutočné údaje. Ak chcete vytvoriť storno položky, systém skopíruje hodnoty polí z pôvodných skutočných hodnôt. Iba hodnoty, ktoré nie sú skopírované, sú hodnoty množstva. Tieto hodnoty sa namiesto toho obrátili. Obrátené skutočné hodnoty sú vytvorené pre skutočné hodnoty **nákladov**, aj pre **nefakturovaných predajov**. Pole **Stav úpravy** na vrátených skutočných hodnotách je nastavené na **Neupraviteľné** a pole **Stav fakturácie** je nastavené na **Zrušené**. V dôsledku týchto zmien sa zaznamenané výdavky a backlog príjmov na projekte nebudú viac vzťahovať na sumy, ktoré tieto skutočné hodnoty predstavujú.

Ak sa žiadosť o odvolanie zamietne, neexistuje žiadny finančný vplyv na projekt.

## <a name="changes-to-time-entry-records"></a>Zmeny záznamov zadania času

Nasledujúci obrázok zobrazuje zmeny, ktoré sa vyskytnú pri schválených časových položkách a zodpovedajúcich záznamoch schválenia, keď sú stiahnuté.

![Prechody stavu zadania času.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Zmeny záznamov zadania výdavkov a použitia materiálu

Nasledujúci obrázok zobrazuje zmeny, ktoré sa vyskytnú pri schválených položkách výdavkov a použitia materiálu a zodpovedajúcich záznamoch schválenia, keď sú stiahnuté.

![Prechody stavu zadania výdavku.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
