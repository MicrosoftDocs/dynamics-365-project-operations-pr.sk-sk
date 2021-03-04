---
title: Platba vopred v hotovosti
description: Táto téma poskytuje informácie o platbách vopred v hotovosti.
author: suvaidya
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 58864790720824cecad8ce1ff7ff0a335a42cc03
ms.sourcegitcommit: 7aa0b7fb22213d8baa2d69efece9a636d9f62493
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098903"
---
# <a name="cash-advance"></a>Platba vopred v hotovosti

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Platba vopred v hotovosti umožňuje zamestnancom požičať si od svojej spoločnosti peniaze skôr, ako im vzniknú akékoľvek výdavky. Keď je požadovaná platba vopred v hotovosti schválená a vyplatená, zamestnanec môže peniaze použiť na výdavky na podnikanie, ktoré mu pravdepodobne vzniknú. 

## <a name="create-and-submit-a-cash-advance-request"></a>Vytvorenie a predloženie žiadosti o platbu vopred v hotovosti
Ak chcete vytvoriť novú hotovostnú zálohu a odoslať žiadosť o hotovostnú zálohu, postupujte takto: 

1. V časti **Moje výdavky** vyberte **Hotovostné zálohy** > **Nová**. 
2. Na stránke **Nová žiadosť o platbu vopred v hotovosti** zadajte účel výdavkov a vyberte miesto, kde vzniknú náklady.
3. Zadajte požadovanú sumu a menu a potom vyberte **Uložiť**. 
4. Keď ste pripravení podať žiadosť o platbu vopred v hotovosti, na stránke **Žiadosť o platbu vopred v hotovosti** vyberte **Pracovný postup** > **Predložiť**.

## <a name="modify-a-cash-advance-request"></a>Upravenie žiadosti o platbu vopred v hotovosti

Ak žiadosť o platbu vopred v hotovosti nebola predložená na schválenie, môžete ju upraviť.

1. V časti **Moje výdavky: hotovostné zálohy** vyhľadajte a vyberte hotovostnú zálohu, ktorú chcete upraviť.
2. Vyberte **Upraviť** a vykonajte potrebné zmeny v žiadosti o platbu vopred v hotovosti. 
3. Vyberte položku **Uložiť a zavrieť**.


## <a name="view-cash-advance-requests"></a>Zobrazenie žiadostí o platbu vopred v hotovosti
V časti **Moje výdavky: platby vopred v hotovosti** môžete skontrolovať zoznam všetkých platieb vopred v hotovosti, ktoré sú v koncepte, predložené, kontrolované alebo vyplatené. 

## <a name="approve-cash-advance-requests"></a>Schválenie žiadostí o platbu vopred v hotovosti

Správcovia alebo používatelia nakonfigurovaní ako schvaľovatelia v pracovnom postupe budú môcť schvaľovať platby vopred v hotovosti, ktoré im boli predložené na kontrolu. 

1. Na schválenie platby vopred v hotovosti v časti **Spracovať platby vopred v hotovosti** vyberte **Platby vopred v hotovosti na moju kontrolu**.
2. Vyberte platbu vopred v hotovosti, ktorú chcete skontrolovať, a vyberte **Schváliť**.  

## <a name="pay-cash-advances"></a>Výplata platby vopred v hotovosti 
Nasledujúci postup zvyčajne vykonáva účtovník alebo používateľ s účtovníckymi povoleniami.

1. Ak chcete zaúčtovať schválené platby vopred v hotovosti, zvoľte **Schválené platby vopred v hotovosti** a potom vyberte **Platba a prevod**.  
2. Zadajte podrobnosti do denníka o platbách vopred v hotovosti a potom vyberte **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Predložte výkaz výdavkov oproti zaplatenej platbe vopred v hotovosti 

Keď vytvoríte a odošlete výkaz výdavkov pre hotovostnú zálohu, ktorú ste už dostali, výdavky sa automaticky upravia oproti danej zálohe. Ak je vaša platba vopred v hotovosti vyššia ako suma výdavkov, musíte zostatok vrátiť spoločnosti pomocou kategórie výdavkov **Vrátiť hotovosť**. Ak je hotovostná záloha zaplatená spoločnosťou nižšia ako suma, ktorú ste vynaložili, spoločnosť vám musí zostatok uhradiť. 

### <a name="example"></a>Príklad
Plánujete cestu zo Seattlu do New Yorku na konferenciu. Požiadavku na hotovostnú zálohu na 3000,00 USD vytvoríte na základe odhadovaných nákladov na konferenčný lístok, letenky, hotel, stravu a taxík. Platba vám nebude vyplatená, pokiaľ váš nadriadený neschváli túto žiadosť. Po schválení manažérom sa požadovaná platba vopred v hotovosti vyplatí na váš bankový účet v sume 3000,00 USD. Potom sa zúčastníte konferencie. Po dokončení cesty zistíte, že celkové výdavky boli iba 2790,00 USD. Vyberte **Hotovosť** v poli **Spôsob platby** a uveďte svoje výdavky v hodnote 2790,00 USD. Vaša predložená suma výdavkov sa automaticky upraví oproti platbe vopred v hotovosti 3000,00 USD, ktorá vám bola požičaná. Teraz dlžíte zostatok 210,00 USD (3000,00 - 2790,00), ktorý môžete spoločnosti vrátiť pomocou kategórie výdavkov **Vrátiť hotovosť**.

