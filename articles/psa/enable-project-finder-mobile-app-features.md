---
title: Zapnutie funkcie aplikácie Project Finder Mobile
description: Ako zapnúť funkcie aplikácie Project Finder Mobile pre Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084371"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Zapnutie funkcií aplikácie Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

V telefóne môžete použiť zdroje Project Finder Mobile s [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] na vyhľadanie nových projektov a aktualizáciu ich súborov schopností.  
  
 Aplikácia je dostupná pre telefóny [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] a [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Musíte nastaviť niekoľko možností v parametroch nastavenia vašej organizačnej jednotky, ktoré používateľom umožnia zobrazovať požiadavky na zdroje projektov a aktualizovať si svoje zručnosti.  
  
> [!NOTE]
>  Aplikácia Project Finder Mobile funguje len s [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (nie s lokálnymi inštaláciami).  
  
1. Prejdite na **Project Service > Parametre.**  
  
2. Kliknite na parametre nastavenia, ktoré chcete použiť na spustenie funkcií aplikácie Project Finder Mobile  
  
3. V oblasti **všeobecné** nastavte **Požiadavky zdrojov viditeľné pre zdroje** na **Áno**.  
  
4. Nastavte možnosť **Povoliť aktualizáciu zručností podľa zdroja** na **Áno**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Toto je globálne nastavenie. Projektoví manažéri môžu nastaviť, či bude viditeľný individuálny projekt na stránke **projektového tímu** projektu.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-mailové oznámenia  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] posiela e-maily týkajúce sa prostriedkov žiadostí nasledovným príjemcom v nasledujúcich časoch:  
  
|Príjemca|Udalosť|  
|---------------|-----------|  
|Projektový manažér|-   Keď sa zdroj cez aplikáciu Project Finder Mobile zaregistruje do projektu.|  
|Zdroj|-   Keď práca na projekte, do ktorého sa zdroj zaregistroval, už bola dokončená iným zdrojom.<br />-   Keď sa schváli alebo zamietne ich žiadosť o schválenie zručností.<br />-   Keď sa schváli alebo zamietne ich žiadosť o registráciu do projektu.|  
  
## <a name="privacy-notice"></a>Oznámenie o ochrane osobných údajov  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Pozrite si tiež  
 [Nastavenie prostriedkov](../psa/set-up-resources.md)
