---
title: Proces plánovania konverzie projektu z automatizácie projektových služieb na projektové operácie
description: Tento článok poskytuje prehľad zmien funkcií pre Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642588"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Proces plánovania konverzie projektu z automatizácie projektových služieb na projektové operácie

Po úspešnej inovácii projektu z Microsoft Dynamics 365 Project Service Automation 3.X až Dynamics 365 Project Operations Lite, úprava projektových úloh v štruktúre rozpisu úloh siete (WBS) nie je možná. Zákazníci si budú môcť prezrieť WBS v sledovacej mriežke, kde boli pridané nové polia, aby poskytli všetky podrobnosti, ktoré súvisia s úlohou. Pre projekty, kde sa vyžadujú úpravy WBS, môžete selektívne previesť vhodné projekty do nového projektu pre webové plánovanie.

## <a name="project-conversion-process"></a>Proces konverzie projektu

Ak chcete konvertovať projekt, postupujte podľa týchto krokov.

1. Otvorte hlavnú stránku projektu a vyberte **Konvertovať** na paneli akcií.
1. V okne s potvrdením vyberte **OK** na spustenie konverzie projektu. Vyskytnú sa tieto akcie:

    1. Panel správ, ktorý sa zobrazí na hlavnej stránke projektu, uvádza: „Plán projektu sa konvertuje. Nemôžete robiť zmeny v projekte, kým sa konverzia nedokončí."
    1. Budete presmerovaní na zoznam projektov.

    Po dokončení konverzie projektu sa vykonajú nasledujúce akcie:

    1. Pridelený projektový manažér dostane upozornenie na pravej strane aplikácie.
    1. Lišta správ, ktorá uvádza, že prebieha konverzia, sa odstráni.
    1. The **Rozvrh** karta zobrazuje nové prostredie plánovania s Project for the web. Každý používateľ, ktorý má príslušné licencie a roly zabezpečenia, môže upravovať WBS.
    1. The **Nástroj plánovania** pole sa aktualizuje na **Projekt pre web**.
    1. The **Konvertovať** tlačidlo sa odstráni z podokna akcií.

> [!IMPORTANT]
> Hromadná konverzia projektov nie je povolená. Akýkoľvek pokus o aktualizáciu veľkého množstva projektov súčasne bude obmedzený. Toto obmedzenie pomáha zabezpečiť vysoký výkon pre všetkých zákazníkov.

## <a name="manual-tasks-vs-automatic-tasks"></a>Manuálne úlohy vs. automatické úlohy

Keď je prostredie inovované z Project Service Automation na Project Operations, všetky úlohy vo WBS sa považujú za automaticky naplánované. Koncept manuálne naplánovaných úloh nie je dostupný v Projecte pre web. Môžete však definovať preferované správanie plánovania pre svoje projekty pomocou [režim plánovania](/project-management/scheduling-modes.md) pri vytváraní nových projektov.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Obmedzené operácie pre projekty pred konverziou

Táto časť popisuje funkčné rozdiely, ktoré môžete očakávať, keď projekty neboli konvertované.

### <a name="copy-project"></a>Kopírovať projekt

The **Kopírovať** prevádzka je podporovaná len na konvertovaných projektoch. Inovované projekty nie je možné pred konverziou skopírovať.

### <a name="move-project"></a>Presunúť projekt

Zmena dátumu začiatku projektu úmerne neposunie začiatok úloh, pokiaľ nebol projekt skonvertovaný.

## <a name="frequently-asked-questions"></a>Najčastejšie otázky

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Aké sú rozdiely medzi konvertovanými projektmi a novými projektmi, ktoré sa vytvoria po dokončení inovácie?

Pre projekty, ktoré sa konvertujú po inovácii prostredia, sa nastaví príznak, ktorý prikáže plánu rešpektovať iba kalendár projektu. Toto správanie sa zhoduje so správaním v Project Service Automation. Príznak však nebude nastavený pre nové projekty, ktoré sa vytvoria po inovácii. Preto bude plán rešpektovať pracovný čas zdrojov, keď sú priradené k úlohe.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Čo mám robiť, ak sa môj projekt nepodarí konvertovať?

Ak sa váš projekt nepodarí konvertovať, prvým krokom je skontrolovať protokoly chýb, aby ste identifikovali všetky bežné problémy, ktoré súvisia s vaším WBS. Ak protokoly neuvádzajú konkrétnu chybu, v súvislosti s ktorou môžete podniknúť kroky, kontaktujte zákaznícku podporu, aby sa váš prípad mohol ďalej posúdiť.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Ako sa v Project for the web rieši zatváranie podnikov?

Project for the web nerešpektuje obchodné uzávery, ktoré podnik definuje na úrovni organizácie. Bude však rešpektovať iné typy voľných dní, ktoré sú definované v danej šablóne pracovného času.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Aké sú obmedzenia Project for the web?

Pozri [Vytvorte štruktúru rozpisu práce: Obmedzenia projektu](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Môžem očakávať zmeny v mojich odhadoch nákladov a predaja?

V zriedkavých prípadoch, keď sa obrysy priradenia zdrojov prepočítavajú alebo keď spadajú do inej hranice dátumu ako zdrojový projekt, môžete vidieť rozdiely v predaji a odhadoch nákladov. V rámci procesu inovácie sa od zákazníkov očakáva, že otestujú reprezentatívnu vzorovú sadu projektov, aby pochopili prípadné zmeny harmonogramu.
