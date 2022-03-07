---
title: Prepracované výkazy výdavkov
description: Táto téma poskytuje informácie o prebudovanom a prepracovanom prostredí pre zadávanie výkazov výdavkov.
author: ryansandness
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: fa111917ffd3107413846dae67c56fd2495cfc1e1bc7362152138efd7bf3b869
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986105"
---
# <a name="redesigned-expense-reports"></a>Prepracované výkazy výdavkov

Zadanie výkazu výdavkov bolo prepracované tak, aby sa zjednodušil proces dokončenia výkazov výdavkov a aby sa skrátil potrebný čas. Ďalej sú uvedené hlavné komponenty nového prostredia s výdavkami:

- Nový pracovný priestor na správu výdavkov, ktorý vám umožní prístup k výdavkom vášho delegáta.
- Nové prostredie párovania príjmových dokladov, ktoré lepšie zobrazuje príjmové doklady na úrovni hlavičky a zjednodušuje proces pripájania príjmových dokladov k riadkom výdavkov.
- Nová mriežka iba na čítanie, ktorá umožňuje zobraziť oveľa viac riadkov výdavkov a ďalších stĺpcov údajov. Teraz môžete vidieť všetky rozpísané a rozdelené riadky spolu s ich hlavnými nákladmi.
- Zjednodušená tabla na úpravu výdavkov.
- Prepracované hlásenia o chybách, varovaniach a politike pomáhajú zaručiť, že máte správny kontext a že rozumiete problému a spôsobu jeho riešenia. Spoločnosť Microsoft odstránila mnoho hlásení, ktoré sa objavili skôr, ako mali používatelia možnosť dokončiť svoje úlohy a vyriešiť problémy, napríklad neúplnú správu rozpisu.
- Nová stránka s určením, ktoré polia požaduje vaša organizácia, ktoré polia sú voliteľné a ktoré polia by sa nemali zachytávať. Táto stránka pomôže znížiť počet polí, ktoré musia používatelia nastaviť.
- Nový vzhľad a dojem pre výkazy výdavkov, takže výkazy už viac nevyzerajú, akoby boli určené pre účtovné osoby.

Nové prostredie zapnete pomocou pracovného priestoru **Správa funkcií** na zapnutie funkcie **Prepracované výkazy výdavkov**. Po zapnutí tejto funkcie prebehnú nasledujúce akcie:

- Existujúci pracovný priestor výdavkov sa nahradí novým pracovným priestorom.
- Pridá sa nové položka ponuky pre viditeľnosť poľa výdavkov.
- Nebudú odstránené žiadne existujúce položky ponuky pre výkazy výdavkov (existujúca stránka) alebo polia výkazu výdavkov.
- Pracovné postupy a akékoľvek schválenia vás stále dovedú na stránku s existujúcimi výkazmi výdavkov.

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
| Pridávanie existujúcich výdavkov a príjmov pri vytváraní výdavkov | Pri vytváraní výkazov výdavkov môžete pridať všetky alebo vybrané výdavky a príjmy. |
| Kalkulačka výmenných kurzov | Bola pridaná kalkulačka výmenných kurzov, ktorá umožňuje vypočítať výmenný kurz pre hotovostné transakcie s viacerými menami. |
| Ukladanie a pridávanie nových riadkov výdavkov | Tlačidlá **Uložiť** a **Nový** sú k dispozícii pri zadávaní nových výdavkov, aby vám pomohli rýchlo zadať riadky výdavkov. |
| Lepšia viditeľnosť rozdelených a rozpísaných riadkov | Rozpísané položky a rozdelené riadky sa pridávajú priamo do zoznamu výdavkov, aby sa zvýšila viditeľnosť a aby ste mohli ľahko určiť, či nedošlo k chybám týkajúcich sa zásad alebo iným chybám. |
| Zobrazenie potvrdení počas rozpisu | Počas rozpisu je možné zobraziť potvrdenia. |

Počiatočné vydanie je zamerané na scenáre zadávania výdavkov. Akýkoľvek scenár kontroly alebo schválenia výkazu výdavkov bude naďalej používať existujúcu stránku zadávania výdavkov.

Nasledujúce funkcie sa nachádzajú na existujúcej stránke, zatiaľ sa však nenachádzajú na novej stránke. Tieto funkcie budú znovu zavedené v priebehu niekoľkých nasledujúcich vydaní:

- Schválenia
- Schválenie záväzkov a možnosť úpravy účtovníctva
- Viaceré body zadávania
- Integrácia cestovnej žiadanky
- Dátová entita pre viditeľnosť poľa výdavkov
- Zadanie výdavkov na diéty
- Pracovný postup na úrovni riadkov
- Dočasná podpora schvaľovateľa
- Rozšírené rozpisy


[!INCLUDE[footer-include](../includes/footer-banner.md)]