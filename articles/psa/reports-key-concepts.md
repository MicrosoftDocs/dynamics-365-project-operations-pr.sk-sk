---
title: Kľúčové koncepty
description: Táto téma obsahuje prepojenia na kľúčové koncepty pre riadenie zdrojov v Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 75b2d2c520cc48eb59c266289ca2bdc1288f2920
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147762"
---
# <a name="key-concepts"></a>Kľúčové koncepty

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nasledujúca tabuľka definuje kľúčové koncepty, ktoré sa používajú v aplikácii Dynamics 365 Project Service Automation.

| Koncept                    | Definícia |
|----------------------------|------------|
| Člen projektového tímu        | Ako súčasť projektového tímu môže byť členom projektového tímu pomenovaný zdroj, ktorý má rezervácie, pomenovaný zdroj, ktorý nemá rezervácie, alebo všeobecný zdroj. Všeobecné zdroje nemajú rezervácie, sú miestne pre projekt, a nemajú kapacitné obmedzenia naprieč projektmi. |
| Projektové generické zdroje   | Zástupný symbol prostriedku, ktorý vám umožní vytvoriť tím a zamestnanca projektového plánu bez toho, aby ste museli poznať pomenovaný prostriedok. Kalendár projektu sa používa ako kalendár všeobecného prostriedku. Všeobecné zdroje môžu byť pridané do projektového tímu a priradené k úlohám. |
| Rezervované hodiny               | Hodiny prostriedku sú ťažko rezervované proti projektu, ktorý pomáha zaručiť dokončenie projektovej práce. Rezervované hodiny sú spotrebované z celkovej kapacity zdroja. Rezervácie sú proti iba pomenované zdroje, nie proti všeobecným zdrojom. |
| Priradené hodiny             | Hodiny prostriedkov sú priradené k úlohám v pláne projektu. Priradenia môžu byť proti buď pomenovaným zdrojom, alebo všeobecným zdrojom. Úlohy môžu byť nezávislé od rezervácií. |
| Požadované hodiny             | Požadovaná kapacita, ktorá ešte nie je splnená zo strany pomenovaného prostriedku. Požadované hodiny sú relevantné len pre generických členov tímu, ktorí vygenerovali požiadavky na zdroje. |
| Dopyt                     | Aktuálna a prichádzajúca pracovná záťaž. V Project Service Automation dopyt sa zobrazuje ako zdroj požiadavky alebo požiadavky na zdroje. |
| Požiadavka na zdroj       | Entita, ktorá sa používa na zachytenie požadovaných hodín, začiatočného a koncového dátumu, zručnosti, geografie a iných cenových dimenzií pre požadované zdroje. Požiadavky na zdroje sú buď generované z členov projektového tímu, alebo jednotlivo vytvorené. |
| Žiadosť o zdroj           | Entita, ktorá sa používa ako „obálka” na predstavenie požiadavky zdroja, ktorý je potrebné splniť zo strany manažéra zdroja. |
| Predvolená rola zdroja      | Rola, pod ktorou je prostriedok zoskupený do výpočtu využitia. Predpokladá sa, že zdroj má požadované zručnosti pre rolu a spĺňa cieľové využitie tejto úlohy. |
| Organizačná jednotka zdroja | Organizačná jednotka, ktorá má priradený zdroj. |
| Kontúry                    | Úloha, požiadavka alebo doba priradenia, pretože sú rozdelené do dennej distribúcie. Napríklad, päťdňová, 40-hodinový úloha môže byť kontúrovaná do ôsmich hodín denne počas piatich dní. |
| Zobrazenie Vyrovnanie        | Zobrazenie zobrazuje rezervácie a všetky priradenia pre každého člena projektového tímu. Toto zobrazenie umožňuje projektovým manažérom nájsť nesúlad medzi rezerváciami a priradeniami a prijať nápravné opatrenia, ak nastane akýkoľvek nesúlad. |
| Pracovná doba                 | Entita, ktorá sa používa na identifikáciu kapacity zdroja a pracovných a nepracovných hodín. Táto entita sa označuje aj ako kalendár zdrojov. |
