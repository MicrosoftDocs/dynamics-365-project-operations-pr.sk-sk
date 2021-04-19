---
title: Deaktivácia cenníkov
description: Táto téma vysvetľuje, ako deaktivovať alebo odstrániť nepoužívané alebo staré cenníky.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701972"
---
# <a name="deactivate-price-lists"></a>Deaktivácia cenníkov 

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Ak chcete odstrániť staré alebo nepoužívané cenníky z Dynamics 365 Project Operations, musíte vykonať dva kroky. 

1. Odstráňte alebo vymažte cenník z konkrétnych stránok.
2. Cenník deaktivujte alebo odstráňte z aktívnych cenníkov na stránke **Cenníky**.

>[!IMPORTANT]
> Na úplné odstránenie cenníka musíte dokončiť obidva kroky. Nestačí iba vykonanie kroku 2, ktorým je priame odstránenie alebo deaktivácia cenníka zo zobrazenia Aktívne cenníky. Musíte tiež odstrániť priradenie tohto cenníka zo všetkých miest uvedených v kroku 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Odstránenie cenníka z konkrétnych stránok
1. Ak chcete odstrániť cenník z Project Operations, choďte na nasledujúce stránky:  

      - Stránka **Parametre projektu** > karta **Cenníky**
      - Stránka **Organizačná jednotka** > mriežka **Cenníky**
      - Stránka **Obchodný vzťah** > mriežka **Projektové cenníky**
      - Stránka **Projektové cenové ponuky** > mriežka **Projektové cenníky**: Toto platí pre všetky aktívne projektové cenové ponuky.
      - Stránka **Projektové zmluvy** > mriežka **Projektové cenníky**: Toto platí pre všetky aktívne projektové zmluvy.

 2. Pre každú stránku musíte zvoliť cenník, ktorý chcete odstrániť, a potom zvoliť **Odstrániť**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Odstránenie alebo deaktivácia cenníka zo stránky Cenníky
 
1. Ak chcete odstrániť cenník z aktívnych cenníkov, prejdite na **Predaj** > **Zákazníci** > **Cenníky**. 
2. Vyberte cenník, ktorý chcete odstrániť, a potom vyberte **Odstrániť**. Ak sa na cenník odkazuje pri akýchkoľvek existujúcich transakciách, nebudete ho môcť vymazať. Ak k tomu dôjde, môžete cenník deaktivovať, aby sa nezobrazil v žiadnom zobrazení. 
3. Ak chcete cenník deaktivovať, znova vyberte cenník a potom vyberte možnosť **Deaktivovať**.   
