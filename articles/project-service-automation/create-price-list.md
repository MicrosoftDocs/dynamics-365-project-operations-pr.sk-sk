---
title: Vytvorenie cenníka
description: Ako na vytvorenie cenníka v Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755675"
---
# <a name="create-a-price-list-project-service"></a>Vytvorenie cenníka (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Cenníky poskytujú šablónu správcom účtu, ktorú môžu použiť na vytvorenie cenových ponúk a projektov a tiež na stanovenie nákladov na projekt. Ponúkajú zoznam položiek úloh a nákladov a cenu za každú z nich. Môžete vytvoriť viaceré cenníky, aby ste mohli zachovať samostatné štruktúry cien pre rôzne regióny, kde produkty predávate alebo rôzne predajné kanály. Je to dobrý nápad vytvoriť najmenej jeden cenník pre každú menu, v ktorej plánujete účtovať zákazníkov.  
  
Na vytvorenie finančného odhadu pre vykonanú prácu sa uistite, že každý projekt má zoznam sprievodných nákladov a predajných cien. Nastavte predvolené náklady a predajný cenník, ktoré sa vzťahujú na všetky projekty vytvorené vo vašej organizácii.  
  
Cenníky sa spoliehajú na úlohy a kategórie výdavkov, takže pred vytvorením cenníka, uistite sa, že ste už nakonfigurovali úlohy a náklady kategórie, ktoré chcete použiť pri vytváraní cenníku.  
  
1.  Prejdite na **Project Service > Cenníky**.  
  
2.  Kliknite na položku **Nový**.  
  
3.  V časti **Kontext** zvoľte, či je tento cenník pre **Náklady**, **Nákup** alebo **Predaj**.  
  
4.  V poli **Názov** zadajte názov cenníka.  
  
5.  V poli **Mena** zvoľte menu, ktorú použijete pri fakturácii a nákladoch.  
  
6.  V poli **Časová jednotka** stanovte časové obdobie, na ktoré sa vzťahuje cena. Môže ísť o deň alebo hodinu.  
  
7.  Podľa potreby vyplňte **Dátum začatia**, **Dátum skončenia** a **Popis**.  
  
8.  Kliknite na tlačidlo **Uložiť** a vytvorte záznam, aby ste mohli pokračovať v jeho úprave.  
  
9. Ak chcete pridať cenu roly do cenníka, kliknite na možnosť **+** v časti **Ceny rolí**.  
  
10. V table **Cena roly** vyplňte podrobnosti a potom kliknite na **Uložiť**. Pokračujte v pridávaní cien rolí podľa potreby. Keď budete hotoví, kliknite na **Uložiť** v pravom spodnom rohu obrazovky.  
  
11. Ak chcete pridať cenu kategórie výdavkov do cenníka, kliknite na možnosť **+** v časti **Ceny kategórií**.  
  
12. V table **Cena kategórie transakcie** vyplňte podrobnosti a potom kliknite na **Uložiť**. Pokračujte v pridávaní cien kategórií podľa potreby. Keď budete hotoví, kliknite na **Uložiť** v pravom spodnom rohu obrazovky.  
  
13. Ak chcete pridať položky do cenníka, kliknite na **+** v časti **Položky v cenníku**.  
  
14. V table **Položky v cenníku** vyplňte podrobnosti a potom kliknite na **Uložiť**. Pokračujte v pridávaní položiek cenníka podľa potreby. Keď budete hotoví, kliknite na **Uložiť** v pravom spodnom rohu obrazovky.  
  
15. Ak chcete pridať územný vzťah k cenníku, kliknite na **+** v časti **Územné vzťahy**.  
  
16. V okne **Nové pripojenie** vyplňte podrobnosti a potom kliknite na **Uložiť**. Podľa potreby pokračujte v pridávaní územných vzťahov. Keď budete hotoví, kliknite na **Uložiť** v pravom spodnom rohu obrazovky.  
  
### <a name="see-also"></a>Pozrite si tiež:  
 [Konfigurácia Project Service Automation](../project-service/configure.md)
