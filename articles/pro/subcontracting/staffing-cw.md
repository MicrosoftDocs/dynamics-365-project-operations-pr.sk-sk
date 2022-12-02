---
title: Personálne zabezpečenie projektu zmluvnými pracovníkmi a kapacitou na základe subdodávateľskej zmluvy
description: Tento článok vysvetľuje, ako možno zabezpečiť personálne požiadavky projektu pomocou zmluvných pracovníkov alebo subdodávateľských kapacít v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522455"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Personálne zabezpečenie projektu zmluvnými pracovníkmi a kapacitou na základe subdodávateľskej zmluvy

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Všeobecní členovia projektového tímu môžu byť obsadení zamestnancami alebo zmluvnými pracovníkmi. Pri personálnom obsadzovaní projektu zmluvnými pracovníkmi môžete obmedziť svoje personálne možnosti na konkrétnych zmluvných pracovníkov, ktorí sú priradení k riadku subdodávateľskej zmluvy. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Vyhľadanie požiadaviek na personálne zdroje so zmluvnými pracovníkmi, ktorí patria do konkrétneho riadka subdodávateľskej zmluvy

Ak chcete vyhľadať požiadavky na personálne zdroje a obsadiť ich zmluvnými pracovníkmi, ktorí patria do konkrétneho riadka subdodávateľskej zmluvy, postupujte podľa týchto krokov:

1. Vytvorte všeobecného člena projektového tímu, ktorý odkazuje na subdodávateľskú zmluvu a riadok subdodávateľskej zmluvy.
2. Vygenerujte požiadavku na zdroj pre tohto všeobecného člena projektového tímu pomocou tlačidla **Generovať požiadavku** na vedľajšej mriežke členov projektového tímu.
3. Vyberte riadok člena tímu a potom vyberte tlačidlo **Rezervovať** na vedľajšej mriežke. 
4. Tým sa otvorí Tabuľa plánovania s kontextom požiadaviek. Spolu s ďalšími atribútmi, ako sú dátumy, rola a polia organizačnej jednotky, sa filtre Tabule plánovania automaticky vyplnia aj poľami dodávateľa, subdodávateľskej zmluvy a riadka subdodávateľskej zmluvy z požiadavky na zdroj.
5. Systém vyhľadá zdroje, ktoré spĺňajú kritériá filtra, a uvedie ich. 
6. Vyberte jeden z filtrovaných zdrojov a rezervujte zdroj pre požiadavku. 
7. Vytvorí sa člen projektového tímu a aktualizujú sa odkazy na subdodávateľskú zmluvu a riadok subdodávateľskej zmluvy. Prejdite do **Odhady projektu** a vyberte **Aktualizovať ceny**, ak chcete zobraziť aktualizované náklady na priradenie zdrojov. 

> [!NOTE]
> Aktualizácia člena projektového tímu s odkazom na subdodávateľskú zmluvu a riadok subdodávateľskej zmluvy nemusí byť vždy možná počas rezervácie, ak je zdroj priradený k viacerým riadkom subdodávateľskej zmluvy. Ak systém nedokáže aktualizovať člena projektového tímu o subdodávateľskú zmluvu a riadok subdodávateľskej zmluvy, otvorte záznam člena projektového tímu a manuálne aktualizujte tieto polia, aby odhad finančných nákladov presne odrážal náklady subdodávateľa.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Vyhľadávanie požiadaviek na personálne zdroje a ich obsadenie zmluvným pracovníkom

Ak chcete vyhľadávať požiadavky na personálne zdroje a obsadiť ich zmluvným pracovníkom, postupujte podľa týchto krokov:

1. Vytvorte všeobecného člena projektového tímu.
2. Vygenerujte požiadavku na zdroj pre tohto všeobecného člena projektového tímu pomocou tlačidla **Generovať požiadavku** na vedľajšej mriežke členov projektového tímu.
3. Vyberte riadok člena tímu a potom vyberte tlačidlo **Rezervovať** na vedľajšej mriežke. 
4. Tým sa otvorí Tabuľa plánovania s kontextom požiadaviek. Spolu s ďalšími atribútmi, ako sú dátumy, rola a polia organizačnej jednotky, sa filtre Tabule plánovania automaticky vyplnia aj poľami dodávateľa, subdodávateľskej zmluvy a riadka subdodávateľskej zmluvy z požiadavky na zdroj. Pretože požiadavka nemala vyplnené žiadne hodnoty subdodávateľskej zmluvy alebo riadka subdodávateľskej zmluvy, tieto atribúty budú na table filtrov prázdne.
5. Systém vyhľadá zdroje, ktoré spĺňajú kritériá filtra, a uvedie ich.
6. Aktualizujte pole **Typ pracovníka** na table filtra na **Zmluvný pracovník**, aby ste obmedzili vyhľadávanie na zmluvných pracovníkov. Aktualizujte možnosť **Dodávateľ** na table filtra a vyberte dodávateľa, aby ste vyhľadávanie obmedzili tak, aby zobrazovalo iba zmluvných pracovníkov, ktorí patria ku konkrétnej dodávateľskej spoločnosti.
7. Vyberte zmluvného pracovníka zo zoznamu a rezervujte zdroj pre požiadavku.
8. Vytvorí sa člen projektového tímu. Člen projektového tímu však nie je aktualizovaný o žiadnu subdodávateľskú zmluvu ani riadok subdodávateľskej zmluvy, a preto priradenie zdrojov nebude účtované pomocou ceny subdodávok. Manuálne aktualizujte člena projektového tímu riadkom subdodávateľskej zmluvy, prejdite na **Odhady projektov** a vyberte **Aktualizovať ceny** na zobrazenie aktualizovaných nákladov na priradenie zdrojov.

> [!NOTE]
> Členovia projektového tímu, ktorí majú **Typ pracovníka** nastavený ako **Zmluvný pracovník**, ale nemajú referenciu na subdodávateľskú zmluvu označenú ako **Neplatné** na mriežke **Členovia projektového tímu**. Ak existujú členovia projektového tímu s týmto stavom, otvorte záznam člena projektového tímu a ručne aktualizujte polia subdodávateľská zmluva a riadok subdodávateľskej zmluvy tak, aby finančný odhad nákladov presne odrážal náklady subdodávateľa na karte **Odhady**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
