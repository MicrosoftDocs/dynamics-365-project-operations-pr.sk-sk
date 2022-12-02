---
title: Externé plánovanie
description: Tento článok poskytuje informácie o externom plánovaní.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736995"
---
# <a name="external-scheduling"></a>Externé plánovanie

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Režim externého plánovania vám umožňuje natívne vytvárať, aktualizovať a odstraňovať entity, ktoré súvisia so štruktúrami rozdelenia práce (WBS), ale bez aktuálnych obmedzení, ktoré uplatňuje Microsoft Project for the Web. Poskytuje tiež obmedzené overenie. Tento režim by mali používať iba títo zákazníci:

- Zákazníci, ktorí majú nástroje potrebné na definovanie WBS mimo logiky plánovania, ktorú poskytuje Project Operations
- Zákazníci, ktorí musia spravovať hierarchiu plánov, závislosti alebo trvanie úlohy

> [!IMPORTANT]
> Údaje, ktoré nie sú správne zadané v entitách súvisiacich s WBS, sa nemusia vykresliť v mriežke zosúladenia zdrojov, mriežke odhadov, mriežke sledovania ani v mriežke priradenia zdrojov.

## <a name="configuration"></a>Configuration

Táto funkcia je predvolene povolená. Na predvolenej hlavnej stránke projektov sa však súvisiace pole predvolene nezobrazuje. Ak chcete povoliť pole, na Maker Portal otvorte hlavnú stránku entity projektu, vyberte pole **Nástroj na plánovanie** a potom zmeňte pole na **Predvolene viditeľné**. Ak nepoužívate predpripravenú hlavnú stránku projektu, upravte svoju existujúcu stránku a pridajte na ňu pole **Nástroj na plánovanie**.

## <a name="settings"></a>Nastavenie

Ak chcete použiť režim externého plánovania, musíte najprv vytvoriť nový projekt a vybrať plánovací nástroj **Externe naplánované** v rozbaľovacom zozname na hlavnej stránke projektu. Po nastavení tohto režimu pre projekt ho už nie je možné zmeniť.

## <a name="viewing-the-wbs"></a>Prezeranie WBS

Ak je projekt naplánovaný externe, prístup k Project for the Web je pre tento projekt obmedzený. Ak chcete zobraziť WBS, musíte prejsť na mriežku sledovania, kde je zobrazený úplný WBS.

## <a name="creating-and-editing-the-wbs"></a>Vytváranie a upravovanie zobrazení WBS

Ak je pre projekt povolené externé plánovanie, musíte definovať údaje pre všetky entity súvisiace so WBS vrátane úloh, členov tímu, priradení zdrojov a závislostí.

Nasledujúca ilustrácia zobrazuje dátový model pre plánovanie projektu.

![Dátový model plánovania projektu.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funkčné obmedzenia

Nasledujúce operácie nie sú povolené na externe naplánovaných projektoch.

### <a name="project-planning"></a>Plánovanie projektu

- **Kopírovať projekt** – Táto operácia sa v externe naplánovaných projektoch nepodporuje.
- **Presunúť projekt** – Zmeny dátumu začiatku projektu neposunú začiatok úloh ani priradenia zdrojov vo WBS.
- **Aktualizácia projektového manažéra** – Zmeny projektového manažéra na hlavnej stránke projektu nevytvoria automaticky nového člena projektového tímu, kým sa projekt neskonvertuje.
- **Aktualizácia šablóny pracovného času projektu** – Zmeny v šablóne pracovného času projektu neprepočítajú plán projektu.
- **Kontúry priradenia zdrojov** – Vytvorením priradení zdrojov sa automaticky neaktualizuje pole **mdyn\_PlannedWork**. Toto pole sa používa na ukladanie kontúr pre úsilie priraďovania zdrojov. Ak v mriežke priradenia zdrojov alebo v mriežke zosúladenia zdrojov zobrazíte časovo rozložené úsilie, musíte definovať platné kontúry priradenia zdrojov. Tieto kontúry musia byť správne naformátované, aby spúšťali výpočet kontúr nákladov aj kontúr predajných cien. Odporúčame vám vytvoriť testovací projekt, ktorý je naplánovaný pomocou Project for the Web, a potom skontrolovať súvisiace údaje, aby ste potvrdili požiadavky a formátovanie.

### <a name="resource-management"></a>Správa zdrojov

- **Plnenie všeobecných požiadaviek na zdroj** – Plnenie všeobecných požiadaviek na zdroj nie je podporované pre externe plánované projekty. Pokusy o splnenie aktívnych otvorených požiadaviek vytvoria nových členov projektového tímu, ale neodstránia generického člena tímu ani nenahradia generického člena tímu v žiadnych existujúcich priradeniach zdrojov.
- **Odstrániť člena tímu** – Odstránením člena tímu sa automaticky neodstránia priradenia zdrojov.

### <a name="quoting-and-contracting"></a>Vytváranie cenových ponúk a uzatváranie zmlúv

- **Importovanie podrobností o riadku cenovej ponuky a riadku zmluvy** – Keď sa z projektu importujú podrobnosti cenovej ponuky alebo riadku zmluvy, aplikácia bola testovaná tak, aby podporovala maximálne 500 úloh vo WBA na základe limitu 20 priradení na úlohu.

### <a name="actuals-and-invoicing"></a>Skutočné hodnoty a fakturácia

- Hoci neexistujú žiadne zmeny v existujúcich overeniach medzi WBS a finančnými transakciami, je dôležité, aby ste sa prispôsobili vopred pripravenému dátovému modelu, aby ste zabezpečili, že všetky následné transakcie prebehnú podľa očakávania.
