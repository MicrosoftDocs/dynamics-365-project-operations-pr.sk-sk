---
title: Zakúpenie neskladovaných materiálov použitím čakajúcej faktúry dodávateľa
description: Táto téma vysvetľuje, ako zaznamenávať čakajúce faktúry dodávateľa.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e95f7dabe597968707fdd2dead40bfb93d7f1f95
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547308"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Zakúpenie neskladovaných materiálov použitím čakajúcej faktúry dodávateľa

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Keďže spoločnosť obstaráva pre projekt neskladované materiály, náklady je možné okamžite zaznamenať oproti projektu. 

Spoločnosť Contoso Robotics USA napríklad vykonáva projekt obnovy zariadenia a potrebuje softvérové licencie. Tieto licencie sú obstarávané od dodávateľa tretej strany.  Použitím Dynamics 365 Finance, referent pre účty zaúčtuje dokument faktúry čakajúceho dodávateľa a pripíše náklady na licenciu priamo oproti projektu obnovy zariadenia. 

> [!IMPORTANT]
> Pred použitím funkcií popísaných v tejto téme si prečítajte a vykonajte požadované konfigurácie. Viac informácií nájdete v časti [Povoliť neskladované materiály a čakajúce faktúry dodávateľa](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Zaúčtujte faktúru dodávateľa čakajúcu na projekt 

Faktúry čakajúcich dodávateľov možno zaznamenať na stránke **Čakajúce faktúry dodávateľa** (**Záväzky** > **Faktúry** > **Čakajúce faktúry dodávateľa**). Ak chcete zaúčtovať nespracovanú faktúru dodávateľa súvisiacej s projektom, postupujte takto:

1. Prejdite na **Záväzky** > **Faktúry** a stlačte možnosť **Nový**. 
2. V poli **Účet faktúry** vyberte dodávateľa a v poli **Číslo** do poľa zadajte identifikáciu faktúry dodávateľa.
3. Pridajte riadok k faktúre dodávateľa a do poľa **Číslo položky** vyberte skladovú položku zakúpenú od dodávateľa. 

    > [!NOTE]
    > Riadky faktúr dodávateľa, ktoré sú založené na kategórii obstarávania, sa proti projektu nedajú zaznamenať. 
    
5. Pridajte zakúpené množstvo. Systém vyplní jednotkovú cenu na základe konfigurácie ceny tovaru, ktorý nie je na sklade. 
6. Celkovú sumu a ďalšie požadované podrobnosti overte na riadku.
7. Na riadku podrobnosti na karte **Projekt** vyberte projekt, do ktorého sa táto položka zaznamená.
8. Voliteľne vyberte číslo aktivity a aktualizujte kategóriu projektu a vlastnosť riadka.
9. Zaúčtujte čakajúcu faktúru dodávateľa. Po zaúčtovaní faktúry systém zaznamená:
    
    - Suma zostatku dodávateľa.
    - Suma dane z predaja.
    - Náklady oproti projektu sa zaznamenajú na účet integrácie obstarávania.
    - Transakcia skutočných nákladov projektu v Dataverse.  Táto transakcia sa ďalej spracováva pomocou [denníka integrácie Project Operations](../project-accounting/project-operations-integration-journal.md). Zaúčtovaním tohto denníka sa suma presunie z účtu integrácie obstarávania do účtu nákladov na projekt. 
    - Nákupy, ktoré sú fakturované zákazníkovi projektu pomocou metódy účtovania času a materiálu. Navyše sa vytvoria nevyfakturované predajné transakcie pre nákupy v Dataverse. Cenník produktov v Dataverse sa používa pre predajné ceny a sumy pre nevyfakturované predajné transakcie.
