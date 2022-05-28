---
title: Nakúpte neskladovaný materiál alebo kategórie obstarávania pomocou čakajúcej faktúry dodávateľa
description: Táto téma vysvetľuje, ako zaznamenávať čakajúce faktúry dodávateľa.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612676"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Nakúpte neskladovaný materiál alebo kategórie obstarávania pomocou čakajúcej faktúry dodávateľa

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Keďže spoločnosť obstaráva neskladový materiál alebo kategórie obstarávania pre projekt, náklady môžu byť okamžite zaúčtované oproti projektu. 

Spoločnosť Contoso Robotics USA napríklad vykonáva projekt obnovy zariadenia a potrebuje softvérové licencie. Tieto licencie sú obstarávané od dodávateľa tretej strany.  Pomocou Dynamics 365 Finance účtovník zaznamená čakajúci doklad faktúry dodávateľa a pripíše náklady na licenciu priamo k projektu obnovy zariadenia. 

> [!IMPORTANT]
> Pred použitím funkcií popísaných v tejto téme si prečítajte a vykonajte požadované konfigurácie. Ďalšie informácie nájdete v časti [Povoliť neskladované materiály a čakajúce faktúry dodávateľa](configure-materials-nonstocked.md) a [Použite kategórie obstarávania s projektovými nákupnými objednávkami a čakajúcimi faktúrami dodávateľa](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Zaúčtujte faktúru dodávateľa čakajúcu na projekt 

Faktúry čakajúcich dodávateľov možno zaznamenať na stránke **Čakajúce faktúry dodávateľa** (**Záväzky** > **Faktúry** > **Čakajúce faktúry dodávateľa**). Ak chcete zaúčtovať nespracovanú faktúru dodávateľa súvisiacej s projektom, postupujte takto:

1. Ísť do **Splatné účty** > **faktúry** a vyberte **Nový**. 
1. V **Fakturačný účet** vyberte dodávateľa a potom v poli **číslo** zadajte identifikáciu faktúry dodávateľa.
1. Pridajte riadok do faktúry dodávateľa a potom do **Číslo položky** vyberte neskladovú položku, ktorá bola zakúpená od dodávateľa. Prípadne v **Kategória obstarávania** vyberte kategóriu obstarávania, ktorá bola zakúpená od dodávateľa.   
1. Pridajte zakúpené množstvo. Systém vyplní jednotkovú cenu na základe konfigurácie ceny nenaskladnenej položky. 
1. Celkovú sumu a ďalšie požadované podrobnosti overte na riadku.
1. V detailoch linky, na **Projekt** vyberte ID projektu, do ktorého bude táto položka zaznamenaná.
1. Voliteľné: Vyberte číslo aktivity a aktualizujte kategóriu projektu a vlastnosť čiary.
1. Zaúčtujte čakajúcu faktúru dodávateľa. Pri zaúčtovaní faktúry systém zaznamená nasledujúce informácie:
    
    - Suma zostatku dodávateľa.
    - Suma dane z predaja.
    - Náklady oproti projektu sa zaznamenajú na účet integrácie obstarávania.
    - Transakcia skutočných nákladov projektu v Dataverse.  Táto transakcia sa ďalej spracováva pomocou [denníka integrácie Project Operations](../project-accounting/project-operations-integration-journal.md). Zaúčtovaním tohto denníka sa suma presunie z účtu integrácie obstarávania do účtu nákladov na projekt. 
    - Nákupy, ktoré sú fakturované zákazníkovi projektu pomocou metódy účtovania času a materiálu. Navyše sa vytvoria nevyfakturované predajné transakcie pre nákupy v Dataverse. Cenník produktov v Dataverse sa používa pre predajné ceny a sumy pre nevyfakturované predajné transakcie.
