---
title: Deaktivácia cenníkov
description: Tento článok vysvetľuje, ako deaktivovať alebo odstrániť nepoužívané alebo staré cenníky.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 56bd498d2cb892bdf0c7514d0918e3873098b8d4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924403"
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
