---
title: Naplánujte zdroje pre projekt
description: Ako naplánovať zdroje pre projekt v Project Service
author: JohnPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: f3b7ea1a2b81b86bedc85b77689145ba5afb579d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583143"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Plánovanie zdrojov projektu (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Môžete skontrolovať dostupnosť na získanie celkový prehľad o spôsobe využitia vašich zdrojov, alebo môžete filtrovať zobrazenie podľa zručností, tímu, umiestnenia a ďalších možností.  
  
Tabuľa plánovania ukazuje zoznam zdrojov a ich dostupnosti. Vyberte režim zobrazenia zobraziť dostupnosť podľa **hodinami**, **deň**, **týždeň**, alebo **mesiac**.  
  
Predtým, ako použijete tabulu plánovania, je dôležité ju nastaviť. Ďalšie informácie si prečítajte v časti [Konfigurácia tabule plánovania (Field Service alebo Project Service Automation)](/dynamics365/field-service/configure-schedule-board).
  
Ak používate staršiu verziu, pre dostupnosť zdrojov pozrite [Zobraziť dostupnosť zdroja](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Na použitie funkcie tabule plánovanie, geografického označovania a služieb určovania polohy si budete musieť zapnúť mapy.  
> 
> 1. V hlavnej ponuke kliknite na tlačidlo **Plánovanie zdrojov** > **Správa**.  
> 2. Kliknite na **Parametre plánovania**.  
> 3. Otvorte záznam a prejdite nadol do sekcie **Resource Scheduling Optimization**.  
> 4. V poli **Pripojiť k mapám** zvoľte možnosť **Áno**.  
> 5. Odsúhlaste podmienky a uložte záznam.  
> 6. V hlavnej ponuke zvoľte možnosť **Project Service** > **Tabuľa plánovania**. Existuje niekoľko spôsobov, ako odtiaľto manuálne naplánovať rezerváciu požiadavky: Vyberte spôsob, ktorý vám vyhovuje.
  
## <a name="find-available-resources"></a>Vyhľadanie dostupných zdrojov

1.  V zozname **Požiadavka rezervácie** kliknite pravým tlačidlom myši na neplánovanú rezervácia a vyberte jednu z nasledujúcich možností:  
  
- Vybrať **nájsť dostupnosť - súčasné zdroje** nájsť dostupné zdroje v zozname zdrojov na palube plán.  
- Vybrať **nájsť dostupnosť - všetky zdroje** a nájdite dostupné zdroje spomedzi zdrojov v systéme.  
   > [!NOTE]
   >  Ak tak urobíte, pri filtorch sa zobrazia možnosti pre zvolení požiadavky rezervácie.  
  
2. Keď vidíte dostupnej zásuvky kliknite pravým tlačidlom myši na časový úsek na palube rozvrh a vyberte **Rezervovať tu**. Alebo drag and drop rezervácia požiadavka dostupného časového úseku.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Rezervujte si prostriedok pomocou denného zobrazenia a zistite, kedy je málo rezervovaný
  
1.  Na tabule plánovania, kliknite na tlačidlo **Režim zobrazenia** a vyberte **Dni**.  
  
    V zobrazení mriežky sa zobrazuje koľko hodín prostriedok je rezervované denne a ktoré dni je voľný.  
  
2.  Kliknite na názov prostriedku, ktorý chcete rezervovať, a potom kliknite na **Rezervovať**.  
  
3.  V dialógovom okne **Rezervácie zdrojov (vytvorenie)** vyberte projekt, ktorému chcete rezervovať prostriedok spolu s rezervácia metóda a časmi začatia a ukončenia.  
  
4.  Po skončení vyberte položku **Rezervovať**.  
  
## <a name="view-to-the-schedule-board"></a>Zobrazenie tabule plánovania
  
1.  Vyberte si nenaplánovanú požiadavku rezervácie zo zoznamu v spodnej časti.  
  
2.  Presuňte požiadavky rezervácie na dostupné zdroje a čas na tabuli plánovania.  
  
3.  Po skončení vyberte položku **Rezervovať**.  
  
### <a name="additional-resources"></a>Ďalšie zdroje  
 [Príručka správcu zdrojov](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
