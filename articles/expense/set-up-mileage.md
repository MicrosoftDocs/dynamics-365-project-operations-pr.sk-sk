---
title: Nastavenie najazdených kilometrov pomocou úrovní najazdených kilometrov
description: Tento článok poskytuje informácie o sadzbách najazdených kilometrov a úrovniach počtu najazdených kilometrov.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 03ca18c8fef6228f2ba553ebe50447beda5a857c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930153"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Nastavenie najazdených kilometrov pomocou úrovní najazdených kilometrov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Keď sa vykáže výdavok a zvolená kategória výdavku je **Najazdené kilometre**, suma za túto položku výdavku sa počíta podľa *sadzby za najazdené kilometre*. Táto suma sa určuje pomocou definovaných úrovní najazdených kilometrov alebo, ak nie sú stanovené úrovne najazdených kilometrov, podľa štandardnej sadzby za najazdené kilometre. 

Úrovne najazdených kilometrov môžete nastaviť v časti **Správa výdavkov** > **Nastavenie** > **Všeobecné** > **Kategórie výdavkov** > **Najazdené kilometre** > **Nastavenie kategórie**.

Ak vaša organizácia po inovácii na verziu 10.0.18 používa kategóriu výdavkov na najazdené kilometre, zvážte aktiváciu funkcie najazdených kilometrov po skontrolovaní dizajnových zmien uvedených nižšie. 

Nový dizajn úrovní najazdených kilometrov má vplyv na to, ako sa spracúva hodnota v poli **Množstvo**. Pred vydaním verzie 10.0.18 sa hodnota v poli **Množstvo** považovala za spodnú hranicu. Keď nahromadená hodnota prekročila túto hranicu, použila sa zodpovedajúca sadzba.  Od verzie 10.0.18 sa hodnota v poli **Množstvo** považuje za hornú hranicu. Zodpovedajúca sadzba sa použije, keď je počet najazdených kilometrov menší ako hodnota v poli **Množstvo**.  Nový model pre úrovne najazdených kilometrov pomáha dosahovať konzistentnosť naprieč rôznymi úrovňami najazdených kilometrov a lepšiu použiteľnosť.   

Všetky schválené výkazy o výdavkoch sa počas účtovania prepočítajú podľa nového vzoru.

## <a name="example"></a>Príklad
 
### <a name="before-version-10018"></a>Pred verziou 10.0.18
S dvoma úrovňami najazdených kilometrov predstavuje spodný limit najazdených kilometrov pole **Množstvo** na každej úrovni. V súčasnosti má prvá úroveň hodnotu nula (0) a sadzbu 0,45 a druhá úroveň má hodnotu 1 000 a sadzbu 0,25. Ak nahromadené míle alebo kilometre prekročia hodnotu uvedenú v poli, použije sa príslušná sadzba. Ak neexistuje žiadny riadok s nulovým množstvom, systém použije sadzbu za najazdené kilometre, ktorá je definovaná vo výkaze o výdavkoch. 
 
Ak zamestnanec predloží výkaz o výdavkoch s 1500 míľami, dva riadky najazdených kilometrov v zaúčtovanom výkaze o výdavkoch budú: 1000 (sadzba 0,45) + 500 (sadzba 0,25) = 575,00.

### <a name="after-version-10018"></a>Po verzii 10.0.18
Vo verzii 10.0.18 predstavuje horný limit úrovne pole **Množstvo** na každej úrovni. V súčasnosti má prvá úroveň hodnotu 999 a sadzbu 0,45 a druhá úroveň má hodnotu 999999999,00 a sadzbu 0,25. Ak nahromadené míle alebo kilometre prekročia hodnotu uvedenú v poli **Množstvo**, použije sa príslušná sadzba. Ak dôjde k prekročeniu všetkých horných hraníc, systém použije sadzbu za najazdené kilometre, ktorá je definovaná vo výkaze o výdavkoch. 
 
Ak chcete správne vypočítať ten istý scenár, musíte zmeniť nastavenie úrovne. Pole **Množstvo** na prvej úrovni má hodnotu 999,00 a na druhej úrovni má hodnotu 999999999,00. Ak zamestnanec prekročí celkové množstvo najazdených míľ alebo kilometrov na prvej úrovni, systém použije sadzbu za najazdené kilometre, ktorá je definovaná vo výkaze o výdavkoch. 
  
Ak zamestnanec predloží výkaz o výdavkoch s 1500 míľami, dva riadky najazdených kilometrov v zaúčtovanom výkaze o výdavkoch budú: 1000 (sadzba 0,45) + 500 (sadzba 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Povoľte funkciu výpočtu najazdených kilometrov pre viac úrovní najazdených kilometrov s rovnakou sadzbou

Funkcia **Výpočet najazdených kilometrov pre viac úrovní najazdených kilometrov s rovnakou sadzbou** zlepší výpočet sadzby za najazdené kilometre. Ak chcete povoliť túto funkciu, vykonajte nasledujúce kroky.

1. Prejdite do časti **Pracovné priestory** > **Správa funkcií**. 
2. V zozname vyhľadajte a vyberte možnosť **Výpočet najazdených kilometrov pre viac úrovní najazdených kilometrov s rovnakou sadzbou** a potom vyberte možnosť **Povoliť teraz**.

Po povolení tejto funkcie obnovte úrovne najazdených kilometrov tak, aby správne odzrkadľovali hodnotu v poli **Množstvo**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
