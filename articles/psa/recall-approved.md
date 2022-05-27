---
title: Odvolanie schváleného času a položiek výdavkov
description: Táto téma poskytuje informácie o zrušení predtým schváleného času projektu alebo nákladov transakcie.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 457aebb00851a1db3e4aa1068f6a825759b8f2e3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578819"
---
# <a name="recall-approved-time-or-expense-entries"></a>Odvolanie schváleného času a položiek výdavkov

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Člen projektového tímu alebo iná osoba, ktorá odošle čas alebo výdavok, môže pripomenúť, že čas alebo náklad po jeho schválení. Proces na vyvolanie schváleného času alebo výdavku má dva kroky:

1. Odosielateľ požaduje stiahnutie.
2. Schvaľovateľ schvaľuje stiahnutie.

## <a name="request-a-recall"></a>Požiadať o stiahnutie

Tieto kroky použite na vyžiadanie stiahnutia schváleného zadania času alebo výdavkov.

1. Pre položky času, prejdite na **Projekty** \> **Moja práca** \> **Zadanie času**.

    -alebo-

    Pre položky výdavkov, prejdite na **Projekty** \> **Moja práca** \> **Výdavky**.

2. V prípade položiek času vyberte všetky položky času pre konkrétnu kombináciu projektu a úlohy. Prípadne v mriežke vyberte jednotlivé bunky pre čas v určitom dátume konkrétneho projektu.

    -alebo-

    Pre položky výdavkov vyberte riadok pre položku výdavku na vyvolanie.

3. Vyberte položku **Odvolať**. Zobrazí sa dialógové okno s potvrdením. Ak boli vybraté položky času a výdavkov už schválené, zobrazí sa výzva na zadanie dôvodu stiahnutia.
4. Zadajte dôvod stiahnutia a potom vyberte **OK**, čím potvrdíte operáciu. Systém odošle osobe, ktorá schválila položky, žiadosť o schválenie odvolania.

> [!NOTE]
> Aj keď možno odvolať záznamy schváleného času a výdavkov, po vyfakturovaní schváleného času alebo výdavku zákazníkovi už nemožno požiadavku o stiahnutie vytvoriť. Používateľ, ktorý sa pokúsi vytvoriť žiadosť o stiahnutie dostane správu, ktorá uvádza, že čas alebo výdavky nemožno stiahnuť, pretože už boli fakturované.

## <a name="approve-or-reject-a-recall-request"></a>Schválenie alebo odmietnutie žiadosti o stiahnutie

Ak chcete schváliť alebo zamietnuť žiadosť o stiahnutie, postupujte podľa týchto krokov.

1. Prejdite na **projekty** \> **moja práca** \> **schválenia**.
2. Na stránke zoznamu **Schválenia** zmeňte zobrazenie na **Žiadosti o odvolanie na schválenie**. Zobrazí sa zoznam predložených žiadostí o stiahnutie.
3. Vyberte jednu alebo viac položiek a potom vyberte položku **Schváliť** alebo **Odmietnuť**.
4. Ak ste vybrali možnosť **Schváliť**, zobrazí sa upozorňujúce hlásenie, ktoré vysvetľuje vplyv schválenia. Stlačením možnosti **OK** potvrďte operáciu. Žiadosť o odvolanie bola schválená.

    -alebo-

    Ak ste vybrali **Odmietnuť**, žiadosť o odvolanie sa zamietne.

> [!NOTE]
> Ako pri požadovaní stiahnutia skontroluje po schválení stiahnutia systém akúkoľvek aktivitu fakturácie v záznamoch času či výdavkov. Ak bola položka už fakturovaná, alebo ak je v návrhu faktúry, schvaľovateľovi sa zobrazí chybové hlásenie, ktoré uvádza, že čas alebo výdavky nemôžu byť schválené na stiahnutie, pretože to bolo už fakturované.

## <a name="impact-of-a-recall-request"></a>Vplyv žiadosti o stiahnutie

Ak sa schválenie odmietne, existuje prevádzkový dopad aj finančný dopad.

### <a name="operational-impact"></a>Prevádzkový vplyv

Ak je žiadosť o odvolanie schválená, záznam o schválení je označený ako **Zamietnutý**. Stav položky sa zmení na **Vrátený** alebo **Zamietnutý** v závislosti od toho, či ide o časovú položku alebo položku výdavkov.

Člen projektového tímu môže zobraziť položky, upraviť ich a potom znova odoslať alebo odstrániť položky úplne.

Ak sa žiadosť o odvolanie zamietne, stav položky zostane **Schválený** a položku nie je možné upraviť členom projektového tímu alebo schvaľovateľa projektu.

### <a name="financial-impact"></a>Finančný vplyv

Ak dôjde k schváleniu žiadosti o odvolanie, zodpovedajúce skutočné hodnoty nákladov a predaja sa aktualizujú nasledujúcim spôsobom:

- Pole **Stav úpravy** sa aktualizuje na **Upravené**.
- Pole **Stav fakturácie** sa aktualizuje na **Zrušené**.

Ďalšie, storno položky sú vytvorené v tabuľke skutočné údaje. Ak chcete vytvoriť storno položky, systém skopíruje hodnoty polí z pôvodných skutočných hodnôt. Iba hodnoty, ktoré nie sú skopírované, sú hodnoty množstva. Tieto hodnoty sa namiesto toho obrátili. Obrátené skutočné hodnoty sú vytvorené pre skutočné hodnoty **nákladov**, aj pre **nefakturovaných predajov**. Pole **Stav úpravy** na vrátených skutočných hodnotách je nastavené na **Neupraviteľné** a pole **Stav fakturácie** je nastavené na **Zrušené**. V dôsledku týchto zmien sa zaznamenané výdavky a backlog príjmov na projekte nebudú viac vzťahovať na sumy, ktoré tieto skutočné hodnoty predstavujú.

Ak sa žiadosť o odvolanie zamietne, neexistuje žiadny finančný vplyv na projekt.

## <a name="changes-to-time-entry-records"></a>Zmeny záznamov zadania času

Nasledujúci obrázok zobrazuje zmeny, ktoré sa vyskytnú pri schválených časových položkách, keď sú stiahnuté.

![Prechody stavu Zadanie času.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Zmeny záznamov zadania výdavkov

Nasledujúci obrázok zobrazuje zmeny, ktoré sa vyskytnú pri schválených výdavkových položkách, keď sú stiahnuté.

![Prechody stavu Zadanie výdavku.](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
