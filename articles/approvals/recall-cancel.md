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

Člen projektového tímu, ktorý odošle záznam o čase, výdavkoch alebo spotrebe materiálu, môže tento záznam po schválení odvolať. Proces stiahnutia má dva hlavné kroky:

1. Odosielateľ požaduje stiahnutie.
2. Schvaľovateľ schváli žiadosť o stiahnutie.

## <a name="request-a-recall"></a>Požiadať o stiahnutie

Ak chcete požiadať o stiahnutie schválených záznamov o čase, výdavkoch alebo spotrebe materiálu, postupujte podľa týchto krokov.

1. Postupujte podľa jedného z týchto krokov v závislosti od typu záznamu, ktorý chcete vyvolať:

    - Časové záznamy nájdete na **projekty** \> **Moja práca** \> **Vstup času** a vyberte všetky časové záznamy pre konkrétnu kombináciu projektu a úlohy. Prípadne v mriežke vyberte jednotlivé bunky pre čas v určitom dátume konkrétneho projektu.
    - Pre položky výdavkov prejdite na **projekty** \> **Moja práca** \> **Výdavky** a vyberte riadok pre položku výdavkov, ktorú chcete vyvolať.
    - Pre položky spotreby materiálu prejdite na **projekty** \> **Moja práca** \> **Denník spotreby materiálu** a vyberte riadok pre záznam spotreby materiálu, ktorý chcete vyvolať.

2. Vyberte položku **Odvolať**. Zobrazí sa dialógové okno s potvrdením. Ak už boli vybraté položky času, nákladov alebo spotreby materiálu schválené, zobrazí sa výzva na zadanie dôvodu stiahnutia.
3. Zadajte dôvod stiahnutia a potom vyberte **OK**, čím potvrdíte operáciu. Systém odošle osobe, ktorá schválila položky, žiadosť o schválenie odvolania.

> [!IMPORTANT]
> Nemôžete vytvoriť požiadavku na stiahnutie pre schválený záznam o čase, výdavkoch alebo spotrebe materiálu, ktorý už bol fakturovaný zákazníkovi. Ak to skúsite, dostanete správu, že záznam o čase, výdavkoch alebo spotrebe materiálu nie je možné vyvolať, pretože už bol vyfakturovaný. V takom prípade môžete požiadať o zrušenie zápisu len vtedy, ak sa opravná faktúra použije na vystavenie celého dobropisu alebo vrátenie peňazí zákazníkovi na pôvodnej faktúre.

## <a name="approve-or-reject-a-recall-request"></a>Schválenie alebo odmietnutie žiadosti o stiahnutie

Ak chcete schváliť alebo zamietnuť žiadosť o stiahnutie, postupujte podľa týchto krokov.

1. Prejdite na **projekty** \> **moja práca** \> **schválenia**.
2. Na stránke zoznamu **Schválenia** zmeňte zobrazenie na **Žiadosti o odvolanie na schválenie**. Zobrazí sa zoznam predložených žiadostí o stiahnutie.
3. Vyberte jednu alebo viac položiek a potom vyberte položku **Schváliť** alebo **Odmietnuť**.
4. Ak ste vybrali možnosť **Schváliť**, zobrazí sa upozorňujúce hlásenie, ktoré vysvetľuje vplyv schválenia. Stlačením možnosti **OK** potvrďte operáciu. Žiadosť o odvolanie bola schválená.

    -alebo-

    Ak ste vybrali **Odmietnuť**, žiadosť o odvolanie sa zamietne.

> [!IMPORTANT]
> Keď je stiahnutie schválené, rovnako ako keď je vyžiadané, systém skontroluje akúkoľvek fakturačnú aktivitu v položkách času, nákladov alebo spotreby materiálu. Ak už bol záznam vyfakturovaný alebo ak je na návrhu faktúry, schvaľovateľ dostane chybové hlásenie, že čas alebo výdavok nemožno schváliť na stiahnutie, pretože už boli vyfakturované. Schvaľovateľ môže v tomto prípade odvolanie schváliť len v prípade, ak sa opravná faktúra použije na vystavenie celého dobropisu alebo vrátenie peňazí zákazníkovi na pôvodnej faktúre.

## <a name="impact-of-a-recall-request"></a>Vplyv žiadosti o stiahnutie

Ak sa schválenie odmietne, existuje prevádzkový dopad aj finančný dopad.

### <a name="operational-impact"></a>Prevádzkový vplyv

Ak je žiadosť o odvolanie schválená, záznam o schválení je označený ako **Zamietnutý**. Stav záznamu sa zmení na buď **Vrátený** alebo **Odmietnuté**, v závislosti od toho, či ide o časový záznam alebo o výdavok či spotrebu materiálu.

Člen projektového tímu môže prezerať položky, upravovať a potom znova odosielať položky alebo úplne vymazávať položky.

Ak sa žiadosť o odvolanie zamietne, stav položky zostane **Schválený** a položku nie je možné upraviť členom projektového tímu alebo schvaľovateľa projektu.

### <a name="financial-impact"></a>Finančný vplyv

Ak dôjde k schváleniu žiadosti o odvolanie, zodpovedajúce skutočné hodnoty nákladov a predaja sa aktualizujú nasledujúcim spôsobom:

- Pole **Stav úpravy** sa aktualizuje na **Upravené**.
- Pole **Stav fakturácie** sa aktualizuje na **Zrušené**.

Ďalšie, storno položky sú vytvorené v tabuľke skutočné údaje. Ak chcete vytvoriť storno položky, systém skopíruje hodnoty polí z pôvodných skutočných hodnôt. Iba hodnoty, ktoré nie sú skopírované, sú hodnoty množstva. Tieto hodnoty sa namiesto toho obrátili. Obrátené skutočné hodnoty sú vytvorené pre skutočné hodnoty **nákladov**, aj pre **nefakturovaných predajov**. Pole **Stav úpravy** na vrátených skutočných hodnotách je nastavené na **Neupraviteľné** a pole **Stav fakturácie** je nastavené na **Zrušené**. V dôsledku týchto zmien sa zaznamenané výdavky a backlog príjmov na projekte nebudú viac vzťahovať na sumy, ktoré tieto skutočné hodnoty predstavujú.

Ak sa žiadosť o odvolanie zamietne, neexistuje žiadny finančný vplyv na projekt.

## <a name="changes-to-time-entry-records"></a>Zmeny záznamov zadania času

Nasledujúca ilustrácia zobrazuje zmeny, ktoré sa vyskytnú pri schválených časových záznamoch a zodpovedajúce záznamy o schválení, keď sú odvolané.

![Prechody stavu vstupu času.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Zmeny v evidencii nákladov a spotreby materiálu

Nasledujúca ilustrácia zobrazuje zmeny, ktoré sa vyskytnú pri schválených záznamoch o výdavkoch a spotrebe materiálu a zodpovedajúcich záznamoch o schválení pri ich stiahnutí.

![Prechody stavu zadania nákladov.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
