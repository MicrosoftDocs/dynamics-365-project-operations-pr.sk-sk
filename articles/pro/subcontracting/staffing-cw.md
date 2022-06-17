---
title: Personálne zabezpečenie projektu zmluvnými pracovníkmi a kapacitou na základe subdodávateľskej zmluvy
description: Tento článok vysvetľuje, ako možno zabezpečiť personálne požiadavky projektu pomocou zmluvných pracovníkov alebo subdodávateľských kapacít v spoločnosti Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 173e1c20d2d046ee2120ec178e51d4868b70847d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922103"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Personálne zabezpečenie projektu zmluvnými pracovníkmi a kapacitou na základe subdodávateľskej zmluvy

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Členovia generického projektového tímu môžu byť obsadení zamestnancami alebo zmluvnými pracovníkmi. Pri obsadzovaní projektu zmluvnými pracovníkmi môžete obmedziť svoje personálne možnosti na konkrétnych zmluvných pracovníkov, ktorí sú priradení k subdodávke. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Hľadajte požiadavky na personálne zdroje so zmluvnými pracovníkmi, ktorí patria do konkrétnej subdodávateľskej linky

Ak chcete vyhľadať a požiadať o personálne zdroje so zmluvnými pracovníkmi, ktorí patria do konkrétnej subdodávateľskej linky, postupujte takto:

1. Vytvorte člena všeobecného projektového tímu, ktorý odkazuje na subdodávku a líniu subdodávok.
2. Vygenerujte požiadavku na zdroj pre tohto všeobecného člena projektového tímu pomocou **Vygenerovať požiadavku** na podmriežke členov projektového tímu.
3. Vyberte riadok člena tímu a potom vyberte **Kniha** tlačidlo na vedľajšej mriežke. 
4. Tým sa otvorí tabuľa plánovania s kontextom požiadaviek. Spolu s ďalšími atribútmi, ako sú dátumy, rola a polia organizačnej jednotky, sa filtre tabule plánovania automaticky vyplnia aj poliami dodávateľa, subdodávky a subdodávky z požiadavky na zdroj.
5. Systém vyhľadá zdroje, ktoré spĺňajú kritériá filtra, a zobrazí ich zoznam. 
6. Vyberte jeden z filtrovaných zdrojov a rezervujte zdroj pre požiadavku. 
7. Vytvorí sa člen projektového tímu a aktualizuje sa referencie subdodávok a subdodávok. Ísť do **Odhady projektov** a vyberte **Aktualizujte ceny** zobrazíte aktualizované náklady na priradenie zdrojov. 

> [!NOTE]
> Aktualizácia člena projektového tímu s odkazom na subdodávku a linku subdodávky nemusí byť vždy možná počas rezervácie, ak je zdroj priradený k viacerým subdodávateľským líniám. Ak systém nedokáže aktualizovať člena projektového tímu pomocou subdodávky a riadku subdodávky, otvorte záznam člena projektového tímu a manuálne aktualizujte tieto polia, aby odhad finančných nákladov presne odrážal náklady subdodávateľa.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Vyhľadávanie a požiadavky na personálne zdroje s ktorýmkoľvek zmluvným pracovníkom

Ak chcete vyhľadať a požiadať o personálne zdroje s ktorýmkoľvek zmluvným pracovníkom, postupujte takto:

1. Vytvorte člena všeobecného projektového tímu.
2. Vygenerujte požiadavku na zdroj pre tohto všeobecného člena projektového tímu pomocou **Vygenerovať požiadavku** na podmriežke členov projektového tímu.
3. Vyberte riadok člena tímu a potom vyberte **Kniha** tlačidlo na vedľajšej mriežke. 
4. Tým sa otvorí tabuľa plánovania s kontextom požiadaviek. Spolu s ďalšími atribútmi, ako sú dátumy, rola a polia organizačnej jednotky, sa filtre tabule plánovania automaticky vyplnia aj poliami dodávateľa, subdodávky a subdodávky z požiadavky na zdroj. Pretože požiadavka nemala vyplnené žiadne hodnoty subdodávok alebo subdodávok, tieto atribúty budú na table filtra prázdne.
5. Systém vyhľadá zdroje, ktoré spĺňajú kritériá filtra, a zobrazí ich zoznam.
6. Aktualizujte **Typ pracovníka** na paneli filtra **Pracovník na dohodu** obmedziť vyhľadávanie na zmluvných pracovníkov. Aktualizovať **Predajca** na table filtra a vyberte dodávateľa, aby ste vyhľadávanie obmedzili tak, aby zobrazovali iba zmluvných pracovníkov, ktorí patria ku konkrétnej dodávateľskej spoločnosti.
7. Vyberte zmluvného pracovníka zo zoznamu a rezervujte zdroj pre požiadavku.
8. Vytvorí sa člen projektového tímu. Člen projektového tímu však nie je aktualizovaný so žiadnou subdodávkou alebo subdodávateľskou líniou, a preto sa priradenie zdrojov nebude účtovať podľa ceny subdodávok. Manuálne aktualizujte člena projektového tímu riadkom subdodávky a prejdite na **Odhady projektov** a vyberte **Aktualizujte ceny** zobrazíte aktualizované náklady na priradenie zdrojov.

> [!NOTE]
> Členovia projektového tímu, ktorí majú **Typ pracovníka** ako **Pracovník na dohodu** ale nemajú referenciu na subdodávku sú označené ako **Neplatné** na **Členovia projektového tímu** mriežka. Ak existujú nejakí členovia projektového tímu s týmto stavom, otvorte záznam člena projektového tímu a manuálne aktualizujte polia subdodávok a riadkov subdodávok tak, aby odhad finančných nákladov presne odrážal náklady subdodávateľa na **Odhady** tab. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
