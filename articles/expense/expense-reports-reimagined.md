---
title: Prepracované výkazy výdavkov
description: Táto téma vysvetľuje prepracované a zmenené prostredie na zadávanie výkazov výdavkov.
author: suvaidya
manager: AnnBe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aaa7dd24915982cf137b5959f2f4c244b9c1e012
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499735"
---
# <a name="expense-reports-reimagined"></a>Prepracované výkazy výdavkov

Prebudovalo sa zadávanie výkazov výdavkov, aby sa zjednodušil postup a znížil čas potrebný na dokončenie výkazu. Ďalej sú uvedené hlavné komponenty nového prostredia s výdavkami:

- Nový pracovný priestor na správu výdavkov, ktorý vám umožní prístup k výdavkom vášho delegáta.
- Nové prostredie párovania príjmových dokladov, ktoré lepšie zobrazuje príjmové doklady na úrovni hlavičky a zjednodušuje proces pripájania príjmových dokladov k riadkom výdavkov.
- Nová mriežka iba na čítanie, ktorá umožňuje zobraziť oveľa viac riadkov výdavkov a ďalších stĺpcov údajov. Teraz môžete vidieť všetky rozpísané a rozdelené riadky spolu s ich hlavnými nákladmi.
- Zjednodušená tabla na úpravu výdavkov.
- Prepracované hlásenia o chybách, varovaniach a politike, ktoré poskytujú správny kontext a porozumenie problému a spôsobu jeho riešenia. Odstránili sme niekoľko hlásení, ktoré sa zobrazovali skôr, ako používatelia mohli dokončiť svoje úlohy a vyriešiť problémy.
- Nová stránka s určením povinných polí, voliteľných polí a polí, ktoré by nemali byť zahrnuté. Táto stránka pomáha znižovať počet polí, ktoré je potrebné nastaviť.
- Nový vzhľad a dojem pre výkazy výdavkov, takže výkazy už viac nevyzerajú, akoby boli určené pre účtovné osoby.

Nové prostredie zapnete pomocou pracovného priestoru **Správa funkcií** na zapnutie funkcie **Prepracované výkazy výdavkov**. Po zapnutí tejto funkcie prebehnú nasledujúce akcie:

- Existujúci pracovný priestor výdavkov sa nahradí novým pracovným priestorom.
- Pridá sa nové položka ponuky pre viditeľnosť poľa výdavkov.
- Nebudú odstránené žiadne existujúce položky ponuky pre výkazy výdavkov (existujúca stránka) alebo polia výkazu výdavkov.
- Pracovné postupy a akékoľvek schválenia vás stále dovedú na stránku s existujúcimi výkazmi výdavkov.

## <a name="getting-started-video-for-new-users"></a>Úvodné video pre nových používateľov

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Video [Prostredie výdavkov v Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (zobrazené vyššie) je súčasťou [zoznamu na prehrávanie Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), ktorý je k dispozícii na YouTube.

## <a name="new-features"></a>Nové funkcie

| Nová funkcia | Popis |
|---|----|
| Viditeľnosť poľa výdavkov | Nová stránka s nastaveniami umožňuje určiť, ktoré polia majú byť pre organizáciu zakázané, ktoré polia by sa mali vyžadovať a ktoré polia sa odporúčajú. |
| Povinné polia | Nová jednoduchá konfigurácia umožňuje vykonať niektoré požadované polia bez toho, aby ste museli používať rámec politiky. |
| Voliteľné polia | Bola pridaná druhá stránka pre voliteľné polia. Týmto spôsobom sa zamestnanci nebudú cítiť, akoby museli nastavovať polia, ale polia sú stále ľahko dostupné. |
| Pridávanie nepriložených potvrdení | Schopnosť pridať nepripojené potvrdenia k výkazu výdavkov je viditeľnejšia z pracovného priestoru a z výkazu výdavkov. |
| Zlepšené zasielanie správ | Riadky výdavkov, ktoré obsahujú varovania alebo chyby, sú lepšie viditeľné. |
| Zníženie počtu správ na paneli správ| Počet správ Infolog sa znížil a bolo vyvinuté úsilie, aby sa v mnohých prípadoch zabránilo zobrazovaniu duplicitných správ. |
| Zoskupené bežné akcie | Rozhranie bolo sprehľadnené pridaním nového tlačidla akcií pre väčšinu bežných akcií na úrovni riadkov a pridaním tlačidla elipsy (...) pre hlavičku a ďalšie menej časté akcie. |
| Nový pracovný priestor na zlepšenie viditeľnosti | Nový pracovný priestor zjednocuje funkcie a odkazy, ktoré umožňujú používateľom presun do rôznych oblastí. |
| Pridávanie existujúcich výdavkov a príjmov pri vytváraní výdavkov | Pri vytváraní výkazov výdavkov môžete pridať všetky výdavky alebo vybrať nepripojené výdavky. Nepripojené výdavky sú výdavky, ktoré boli importované z informačného kanála podnikovej kreditnej karty, alebo výdavky, ktoré boli vytvorené manuálne používateľom, ale neboli priložené k výkazu výdavkov.|
| Kalkulačka výmenných kurzov | Bola pridaná kalkulačka výmenných kurzov, ktorá umožňuje vypočítať výmenný kurz pre hotovostné transakcie s viacerými menami. |
| Ukladanie a pridávanie nových riadkov výdavkov | Tlačidlá **Uložiť** a **Nový** sú k dispozícii pri zadávaní nových výdavkov, aby vám pomohli rýchlo zadať riadky výdavkov. |
| Lepšia viditeľnosť rozdelených a rozpísaných riadkov | Rozpísané položky a rozdelené riadky sa pridávajú priamo do zoznamu výdavkov, aby sa zvýšila viditeľnosť a aby ste mohli ľahko určiť, či nedošlo k chybám. |
| Zobrazenie potvrdení počas rozpisu | Počas rozpisu je možné zobraziť potvrdenia. |
| Výber zálohy v hotovosti | Vyberte jednu alebo viac záloh v hotovosti na uskutočnenie transakcie s jedným výdavkom. |
| Zostatok zálohy v hotovosti | Skontrolujte zostatok zálohy v hotovosti v reálnom čase, keď vytvoríte záznam výdavkov v porovnaní so schválenými a vyplatenými zálohami v hotovosti. |

Počiatočné vydanie je zamerané na scenáre zadávania výdavkov. Akýkoľvek scenár kontroly alebo schválenia výkazu výdavkov bude naďalej používať existujúcu stránku zadávania výdavkov.

V prepracovanom pracovnom priestore pre výdavky nie sú podporované nasledujúce funkcie:

- Integrácia cestovnej žiadanky
- Zadávanie výdavkov na diéty
- Dočasná podpora schvaľovateľa
- Zobrazovanie histórie pracovných postupov


[!INCLUDE[footer-include](../includes/footer-banner.md)]
