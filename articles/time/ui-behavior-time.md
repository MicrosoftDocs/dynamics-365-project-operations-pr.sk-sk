---
title: Správanie používateľského rozhrania pri zadávaní času
description: Táto téma poskytuje informácie o správaní používateľského rozhrania pri zadávaní času.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8719e2f9ee4867f17ed75142eca2115f61e37999
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124522"
---
# <a name="time-entry-ui-behavior"></a>Správanie používateľského rozhrania pri zadávaní času

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_


Mriežka **Zadanie týždenného času** je vlastný ovládací prvok, ktorý má dve časti, **Dimenzie** a **Trvanie**.

## <a name="dimensions"></a>Dimenzie
Časti **Dimenzie** zobrazujú dimenzie, proti ktorým možno zadávať čas. Nasledujúce dimenzie sú predpripravené:

  - Project
  - Projektová úloha
  - Rola
  - Typ
  - Stav zadania

Časť **Dimenzia** neumožňuje riadkové úpravy. Táto časť je podporovaná zobrazením, ktoré umožňuje pridať vlastné polia do mriežky týždennej časovej položky.

## <a name="duration"></a>Trvanie:
V časti trvanie sa zobrazujú dni v týždni ako hlavičky stĺpcov. Táto časť umožňuje riadkové úpravy. Po vytvorení riadka zadania času, ktorý má príslušné dimenzie, môžu používatelia rýchlo zadávať množstvo času, ktoré strávili v týchto dimenziách.

## <a name="create-a-new-time-entry"></a>Vytvorenie nového časového záznamu

1. V mriežke na zadanie času vyberte **Nový**. 
2. V dialógovom okne **Rýchle vytvorenie zadania času** vyberte dátum zadania času.
3. Zadajte údaje pre dimenzie **Projekt**, **Projektová úloha**, **Rola** a **Trvanie**. Tieto informácie by mali byť pridané v minútach, hodinách alebo dňoch zadaním **h**, **m** alebo **d** spolu s číslom. 
4. Zadajte popis zadania a všetky komentáre, ktoré sa dajú externe zdieľať, pokiaľ ide o zadanie času. 

Po uložení záznamu sa zadané hodnoty zobrazia v sekcii **Dimenzie**. Informácie zadané v poli **Trvanie** sa zobrazia v dátume, pre ktorý bol vytvorený záznam času.

Vyhľadávacie polia sú podporované systémovými zobrazeniami. Ak napríklad používateľ prejde do projektu, pole **Projektová úloha** sa predvolene nastaví na zobrazenie **Kopírovať**. Ak chcete vytvoriť časové položky pre úlohy, ktoré nie sú priradené používateľovi, kliknite v dialógovom okne na možnosť **Zmeniť zobrazenie** na vyhľadávanie a stlačte možnosť **Všetky aktívne projektové úlohy**.

## <a name="edit-a-time-entry"></a>Úprava zadania času 
Podrobnosti z niektorých polí na stránke časovej položky, ako napríklad **Popis** a **Externé poznámky** sa nezobrazujú v mriežke týždenného vstupu. Namiesto toho sa v bunkách **Trvanie**, ktoré majú tieto ďalšie podrobnosti, objaví malý trojuholníkový indikátor. 

1. Ak chcete upraviť časový záznam, vyberte v časovom zázname bunku, ktorú chcete aktualizovať.
2. Vyberte možnosť **Upraviť podrobnosti** na aktualizovanie údajov v table **Hlavný formulár zadaní času**. 

## <a name="copy-a-time-entry-row"></a>Kopírovanie riadku zadania času
Po vytvorení riadka môžete zvoliť možnosť **Kopírovať riadok** a skopírovať celý riadok do nového riadka. Po skopírovaní riadka týmto spôsobom sa skopírujú aj dimenzie a trvania. Môžete tiež vybrať možnosť **Upraviť riadok** a aktualizovať hodnoty dimenzie a trvania v sekcii **Trvanie**.

## <a name="open-a-time-entry-behavior"></a>Správanie otvorenia časovej položky
Na podporu optimálneho a rýchleho zadávania v najvýraznejších poliach sa v mriežke týždenného vstupu zobrazuje podmnožina vybratých dimenzií a časových trvaní. Ak chcete zobraziť všetky podrobnosti o jedinom časovom zápise, v časti **Upraviť zadanie** stlačte položku **Otvoriť**.

## <a name="submit-a-time-entry"></a>Odoslať zadanie času
Môžete odoslať jednorazovú položku alebo skupinu časových položiek výberom bloku buniek alebo celým časovým riadkom a následným výberom možnosti **Odoslať**. Odoslané časové položky sa zobrazia ako položky, ktoré čakajú na schválenie na stránke **Schválenie** schvaľovateľov. Po úspešnom odovzdaní záznamov ich nemožno upravovať.

## <a name="recall-a-time-entry"></a>Odvolať zadanie času
Môžete si pripomenúť položky, ktoré ste odoslali. Môžete si pripomenúť, jediný čas vstupu, blok času položky, alebo celý rad časových položiek. Odvolané zadania času je možné upravovať.

## <a name="time-entry-status"></a>Stav zadania času

- **Koncept**: Nové položky času sa automaticky priradia k stavu **Koncept**. Odstránia sa len časové položky, ktoré majú stav **Koncept**.
- **Odoslané**: Keď je odoslaná časová položka, stav sa aktualizuje na **Odoslané**. 
- **Schválené**: Keď je odoslaná časová položka schválená, stav sa aktualizuje na **Schválené**. 
- **Vrátené**: Ak je položka času zamietnutá, stav sa aktualizuje na **Vrátené** a položka bude k dispozícii na opravu a opätovné odoslanie. 

## <a name="view-rejection-comments"></a>Zobraziť komentáre k zamietnutiu
Ak schvaľovateľ zamietne časovú položku, môže pridať poznámky, ktoré pomôžu prostriedku pochopiť dôvod zamietnutia. Ak chcete zobraziť komentáre odmietnutia pre časovú položku, vyberte položku **Otvoriť položku**. Pripomienky k zamietnutiu sa zobrazia na časovej osi. Používateľ môže odpovedať na komentáre o odmietnutí skôr, ako znova odošle položku.

## <a name="copy-week"></a>Kopírovať týždeň
Po vytvorení niekoľkých časových záznamov môžu používatelia vytvoriť viac časových záznamov súčasne.

1. Vo formulári **Zadania času** vyberte **Kopírovať týždeň** na hromadné vytvorenie ďalších časových záznamov. 
2. V dialógovom okne **Kopírovať** v časti **Obdobie od** použite polia **Počiatočný dátum** a **Koncový dátum** na definovanie rozsahu dátumov, z ktorého sa majú kopírovať časové položky. 
3. V časti **Obdobie do** v poli **Počiatočný dátum** zadajte dátum vytvorenia položiek času. 
4. Vyberte **Skopírovať**. Pre dátum zadaný v časti **Obdobie do** sa vytvorí kópia časových položiek pre zodpovedajúci deň v týždni v položke **Obdobie od**. Napríklad, pondelkový čas vstup z minulého týždňa bude skopírovaný do pondelka pre týždeň uvedený v položke **Obdobie do**.

## <a name="import"></a>Import
Rovnaký základný proces sa používa na import z rezervácií, úloh a výmen. Môžete určiť rozsah dátumov, z ktorého sa importujú rezervácie, a potom explicitne vybrať rezervácie, ktoré sa majú skopírovať do konceptu zadaní času. 
