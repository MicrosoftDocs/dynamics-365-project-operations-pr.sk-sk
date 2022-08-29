---
title: Riadky faktúr dodávateľov pre čas
description: Tento článok vysvetľuje, ako zaznamenať riadky faktúry dodávateľa pre časové náklady, ktoré vložili subdodávatelia.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262032"
---
# <a name="vendor-invoice-lines-for-time"></a>Riadky faktúr dodávateľov pre čas

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Faktúra dodávateľa v spoločnosti Microsoft Dynamics 365 Project Operations môže mať riadky faktúry dodávateľa za čas. Projektoví manažéri môžu použiť riadky faktúry dodávateľa pre čas na zaznamenanie nákladov na čas subdodávateľov na projektoch.

Riadky faktúry dodávateľa pre čas môžu alebo nemusia odkazovať na riadok subdodávky pre čas. Ak riadok faktúry dodávateľa pre čas odkazuje na subdodávku, projektoví manažéri budú môcť porovnať a overiť čas, ktorý je fakturovaný riadkom faktúry dodávateľa, s časom, ktorý zaznamenávajú subdodávatelia a schvaľujú projektoví manažéri na projekte.

Nasledujúca tabuľka poskytuje informácie o poliach na riadkoch faktúry dodávateľa pre čas.

| Pole | Description | Funkčný vplyv |
| --- | --- | --- |
| Name | Názov riadku faktúry dodávateľa na uľahčenie identifikácie. | Tento názov sa zobrazí ako prvý stĺpec vo všetkých vyhľadávaniach, ktoré sú založené na riadkoch faktúry dodávateľa. |
| Description | Stručný popis služieb, ktoré sú fakturované dodávateľom v riadku faktúry dodávateľa. | None |
| Subdodávateľská zmluva | Subdodávka, na základe ktorej boli služby pôvodne objednané. | Keď je pre faktúru dodávateľa vybratá subdodávka, všetky riadky na faktúre dodávateľa zdedia tento výber. Faktúra dodávateľa nemôže obsahovať riadky faktúry dodávateľa, ktoré odkazujú na rôzne subdodávky. |
| Subdodávateľská linka | Subdodávateľská linka, na ktorej boli služby objednané. Zoznam riadkov subdodávok, ktoré je možné vybrať, je obmedzený na riadky vo vybranej subdodávke. | Keď je v riadku faktúry dodávateľa vybratý riadok pre čas, predvolené hodnoty pre **Projekt**, **·**, a **Rezervovateľný zdroj** polia sa zadávajú z príslušných polí v riadku subdodávky. Ak má vybraný riadok subdodávky hodnoty v **Projekt**, **·**, a **Rezervovateľné** hodnoty zodpovedajúcich polí v riadku faktúry dodávateľa sa nemôžu líšiť od týchto hodnôt. |
| Dátum transakcie | Dátum, kedy budú skutočné náklady riadku faktúry dodávateľa zaznamenané v projekte. | None |
| Trieda transakcie | Predvolená hodnota je **Čas**. | Hodnota **Čas** označuje, že riadok faktúry dodávateľa sa používa na zaznamenanie čiastky faktúry za čas subdodávateľa. |
| Project | Názov projektu, na ktorý boli použité služby, ktoré sú fakturované. | Toto pole je povinné a nemôže zostať prázdne. |
| Úloha | Názov projektovej úlohy, na ktorú sa použili fakturované služby. Toto pole je dostupné len vtedy, ak je vybratý projekt. Výber projektovej úlohy je voliteľný. | Ak toto pole ponecháte prázdne, projektový manažér môže priradiť riadok faktúry dodávateľa k času, ktorý je zaznamenaný zdrojmi subdodávateľa pri akejkoľvek úlohe projektu. Ak riadok faktúry dodávateľa neodkazuje na riadok subdodávky a toto pole zostane prázdne, skutočné náklady vytvorené riadkom faktúry dodávateľa nebudú prepojené so žiadnymi skutočnými nevyfakturovanými predajmi. V tomto prípade, ak je nastavená fakturácia podľa úloh, nemusí byť možné náklady fakturovať koncovému zákazníkovi. |
| Rola | Úloha subdodávateľských zdrojov, ktorých čas sa fakturuje. | Toto pole určuje rolu, ktorú vykonávajú zdroje subdodávok, ktorých čas je fakturovaný na faktúre dodávateľa. |
| Rezervovateľný zdroj | Meno subdodávateľa, ktorého čas sa fakturuje. Výber rezervovateľného zdroja je voliteľný. | Ak toto pole ponecháte prázdne, projektový manažér môže priradiť riadok faktúry dodávateľa k času, ktorý je zaznamenaný ktorýmkoľvek zdrojom, ktorý patrí dodávateľovi v riadku faktúry dodávateľa. |
| Množstvo | Do riadku faktúry zadajte počet hodín, ktoré sú fakturované dodávateľom. |None |
| Jednotková skupina | Predvolená hodnota je **Skupina časových jednotiek** a nedá sa zmeniť. | None |
| Jednotka | Predvolená hodnota je základná jednotka hodín zo skupiny časových jednotiek. Túto hodnotu môžete zmeniť na nákup v akejkoľvek jednotke skupiny časových jednotiek, ako je deň alebo týždeň. | Kombinácia **Role** a **Jednotka** hodnoty sa použijú ako predvolená alebo vypočítaná hodnota pre **Jednotková cena** v riadku faktúry dodávateľa. |
| Jednotková cena | Predvolená jednotková cena používa kombináciu **Role** a **Jednotka** hodnoty z cenníka projektu, ktorý sa vzťahuje na dátum transakcie riadku faktúry dodávateľa. | Ak je cena pre príslušný projektový cenník nastavená v jednotke, ktorá sa líši od jednotky na riadku faktúry dodávateľa, systém použije na výpočet jednotkovej ceny konverziu jednotiek. |
| Medzisúčet | Toto pole len na čítanie sa vypočíta ako *Množstvo*&times;*Jednotková cena*, ak sú hodnoty zadané v oboch **Množstvo** pole a **Jednotková cena** lúka. Ak sú jedno alebo obe polia prázdne, môžete do tohto poľa zadať hodnotu. | None |
| Daň z predaja | Zadajte sumu dane z predaja. | None |
| Celková suma | Celková suma riadku faktúry dodávateľa vrátane daní. Toto pole sa vypočíta ako *Medzisúčet* + *Daň z predaja*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
