---
title: Zakúpenie neskladovaných materiálov alebo kategórie obstarávania použitím čakajúcej faktúry dodávateľa
description: Tento článok vysvetľuje, ako zaznamenávať čakajúce faktúry dodávateľa.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922011"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Zakúpenie neskladovaných materiálov alebo kategórie obstarávania použitím čakajúcej faktúry dodávateľa

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Keďže spoločnosť obstaráva pre projekt neskladované materiály alebo kategórie obstarávania, náklady je možné okamžite zaznamenať oproti projektu. 

Spoločnosť Contoso Robotics USA napríklad vykonáva projekt obnovy zariadenia a potrebuje softvérové licencie. Tieto licencie sú obstarávané od dodávateľa tretej strany.  Použitím Dynamics 365 Finance referent pre záväzky zaúčtuje dokument čakajúcej faktúry dodávateľa a pripíše náklady na licenciu priamo oproti projektu obnovy zariadenia. 

> [!IMPORTANT]
> Pred použitím funkcií popísaných v tomto článku si prečítajte a vykonajte požadované konfigurácie. Viac informácií nájdete v časti [Povoliť neskladované materiály a čakajúce faktúry dodávateľa](configure-materials-nonstocked.md) a [Použitie kategórií obstarávania s nákupnými objednávkami projektu a čakajúcimi faktúrami dodávateľa](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Zaúčtujte faktúru dodávateľa čakajúcu na projekt 

Faktúry čakajúcich dodávateľov možno zaznamenať na stránke **Čakajúce faktúry dodávateľa** (**Záväzky** > **Faktúry** > **Čakajúce faktúry dodávateľa**). Ak chcete zaúčtovať nespracovanú faktúru dodávateľa súvisiacej s projektom, postupujte takto:

1. Prejdite na **Záväzky** > **Faktúry** a vyberte **Nový**. 
1. V poli **Účet faktúry** vyberte dodávateľa a následne v poli **Číslo** zadajte identifikáciu faktúry dodávateľa.
1. Pridajte riadok k faktúre dodávateľa a následne do poľa **Číslo položky** vyberte neskladovú položku, ktorá bola zakúpená od dodávateľa. Prípadne v poli **Kategória obstarávania** vyberte kategóriu obstarávania, ktorá bola zakúpená od dodávateľa.   
1. Pridajte zakúpené množstvo. Systém vyplní jednotkovú cenu na základe konfigurácie ceny položky, ktorá nie je na sklade. 
1. Celkovú sumu a ďalšie požadované podrobnosti overte na riadku.
1. Na riadku podrobnosti na karte **Projekt** vyberte ID projektu, do ktorého sa táto položka zaznamená.
1. Voliteľne: Vyberte číslo aktivity a aktualizujte kategóriu projektu a vlastnosť riadka.
1. Zaúčtujte čakajúcu faktúru dodávateľa. Po zaúčtovaní faktúry systém zaznamená nasledujúce informácie:
    
    - Suma zostatku dodávateľa.
    - Suma dane z predaja.
    - Náklady oproti projektu sa zaznamenajú na účet integrácie obstarávania.
    - Transakcia skutočných nákladov projektu v Dataverse.  Táto transakcia sa ďalej spracováva pomocou [denníka integrácie Project Operations](../project-accounting/project-operations-integration-journal.md). Zaúčtovaním tohto denníka sa suma presunie z účtu integrácie obstarávania do účtu nákladov na projekt. 
    - Nákupy, ktoré sú fakturované zákazníkovi projektu pomocou metódy účtovania času a materiálu. Navyše sa vytvoria nevyfakturované predajné transakcie pre nákupy v Dataverse. Cenník produktov v Dataverse sa používa pre predajné ceny a sumy pre nevyfakturované predajné transakcie.
