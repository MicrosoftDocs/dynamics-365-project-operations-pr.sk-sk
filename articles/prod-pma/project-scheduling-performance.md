---
title: Výkon plánovania projektového zdroja
description: Tento článok poskytuje informácie o tom, ako zlepšiť výkon plánovania prostriedkov pre veľký počet projektov.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 072476d43fb3b3d4f96480ec2d3dc5f9db28e501
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921919"
---
# <a name="project-resource-scheduling-performance"></a>Výkon plánovania projektového zdroja

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Problémy s výkonom súvisiace s plánovaním zdrojov môžu nastať, keď počet projektov dosiahne tisíce. Na zlepšenie výkonu plánovania prostriedkov je k dispozícii funkcia, ktorá používateľom umožňuje skrátiť čas potrebný na spustenie formulára dostupnosti prostriedkov. Týmto sa konkrétne odstráni proces synchronizácie súhrnnej kapacity zdrojov a použije sa **ResProjectResource** tabuľka na urýchlenie vyhľadávania zdrojov. Všimnite si, že tabuľka **ResRollup** sa už nebude používať.

> [!IMPORTANT]
> Ak existuje závislosť buď od procesu synchronizácie súhrnnej kapacity zdrojov, alebo od **ResProjectResource** nepoužívajte túto funkciu.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Povoliť vylepšenie výkonu plánovania zdrojov
Ak chcete povoliť vylepšenie výkonu plánovania prostriedkov, vykonajte nasledujúce kroky.

1. Prejdite do **Správa funkcií** > **Všetky** a v zozname funkcií vyhľadajte možnosť **Povoliť funkciu vylepšenia výkonu plánovania zdrojov projektu**.
2. Vyberte položku **Povoliť teraz**.

> [!NOTE]
> Ak nenájdete funkciu v zozname, stlačte možnosť **Skontrolovať aktualizácie** a obnovte zoznam.

3. Obnovte prehľadávač a potom prejdite na **Projektové riadenie a účtovníctvo** > **Periodické** > **Zdroje projektu** > **Synchronizujte kapacitu kalendárov zdrojov vo všetkých spoločnostiach**.
4. Nastavte **Odstrániť existujúce záznamy o kapacite** na **Áno** na odstránenie predchádzajúcich údajov. Ak chcete generovať prírastkové údaje, nastavte ich na **Nie**.
5. V poli **Kód obdobia** vyberte obdobie, v ktorom sa majú údaje generovať. Ak vyberiete kód obdobia, nie je potrebné definovať počiatočný a konečný dátum.
6. Ak ponecháte pole **Kód obdobia** prázdne, vyberte konkrétne dátumy začatia a ukončenia na generovanie údajov.
7. Vyberte položku **OK**.

 > [!NOTE]
 > Toto bude distribuovať všeobecné údaje do tabuľky **ResCalendarCapacity** naprieč všetkými spoločnosťami vo vašom prostredí, takže dávkovú prácu je potrebné spustiť iba v jednej právnickej osobe. Údaje v tejto dávkovej úlohe sú potrebné na výpočet kapacity prostriedkov prostredníctvom súvisiaceho kalendára.

8. Prejdite do **Projektové riadenie a účtovníctvo** > **Periodické** > **Zdroje projektu** > **Naplňte zdroje projektu vo všetkých spoločnostiach** a potom vyberte **OK**. Toto je skript na aktualizáciu údajov pre všeobecné údaje v tabuľkách **ResProjectResource**, **ResCalendarDateTimeRange** a **ResEffectiveDateTimeRange**. Hodnoty pre pole **PSAPRojSchedRole.RootActivity** sa tiež aktualizujú. Ak to nie je spustené, dostanete varovanie, keď sa pokúsite vykonať operácie plánovania prostriedkov.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Vypnutie vylepšenia výkonu plánovania zdrojov

1. Prejdite do **Správa funkcií** > **Všetky** a v zozname funkcií vyhľadajte možnosť **Povoliť funkciu vylepšenia výkonu plánovania zdrojov projektu**.
2. Vyberte funkciu a potom stlačte tlačidlo **Zakázať**.
3. Obnovte prehliadač.
4. Prejdite na **Projektové riadenie a účtovníctvo** > **Pravidelne** > **Synchronizácia kapacity** > **Synchronizácia súhrnov kapacity zdroja**.
5. Na stránke **Synchronizácia súhrnnej kapacity** nastavte **Odstrániť existujúce záznamy o kapacite** na **Áno** na odstránenie predchádzajúcich údajov. Ak chcete generovať prírastkové údaje, nastavte ich na **Nie**.
6. V poli **Kód obdobia** vyberte obdobie, v ktorom sa majú údaje generovať. Ak vyberiete kód obdobia, nie je potrebné definovať počiatočný a konečný dátum.
7. Ak ponecháte pole **Kód obdobia** prázdne, vyberte konkrétne dátumy začatia a ukončenia na generovanie údajov.
8. Vyberte položku **OK**.

> [!NOTE]
> Toto bude distribuovať všeobecné údaje do tabuľky **ResRollup** naprieč všetkými spoločnosťami vo vašom prostredí, takže dávkovú prácu je potrebné spustiť iba v jednej právnickej osobe. Táto hromadná úloha je potrebná pre všetky zobrazenia **Dostupnosť zdrojov**. Ak táto dávková úloha nie je spustená, údaje **ResRollup** sa budú generovať za chodu, čo môže chvíľu trvať.


[!INCLUDE[footer-include](../includes/footer-banner.md)]