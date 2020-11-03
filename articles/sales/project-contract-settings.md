---
title: Nastavenia projektovej zmluvy
description: Táto téma poskytuje informácie o poliach, ktoré majú vplyv na riadky zmluvy, a informácie o zmluve, ktoré sú zhrnuté vo všetkých riadkových položkách.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c11d6e76b551e0d2cde8ff514d1a0ddd989d07b9
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088103"
---
# <a name="project-contract-settings"></a>Nastavenia projektovej zmluvy

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma poskytuje informácie o poliach, ktoré sa vzťahujú na celú zmluvu o projekte vrátane nastavení, ktoré majú vplyv na všetky riadky zmluvy. Zahrnuté sú aj informácie o zmluve, ktoré sú zhrnuté vo všetkých riadkových položkách a slúžia na zvýšenie KPI projektovej zmluvy.

V nasledujúcej tabuľke sú uvedené polia zmluvy o projekte, ktoré sú jedinečné pre Dynamics 365 Project Operations alebo majú niektoré dôležité zmeny v porovnaní s predajnými objednávkami v Dynamics 365 Sales.

| Pole | Miesto | Relevantnosť, účel a pokyny | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| Zadať | Karta **Súhrn** (skrytá) | Ide o pole množiny možností s nasledovnými možnosťami:</br>- **Založené na práci** (k dispozícii iba vtedy, keď je nainštalovaný Project Operations)</br>- **Založené na položke** (k dispozícii iba vtedy, keď sú nainštalované Project Operations a Sales)</br>- **Služba založená na údržbe** (k dispozícii, keď je nainštalovaná služba Dynamics 365 Field Service) | V časti Project Operations je hodnota tohto poľa predvolená na **Založené na práci** a klasifikuje zmluvu ako zmluvu na základe projektu. Zmluva by mala byť založená na projekte, aby umožnila všetky rozšírenia a funkcie špecifické pre projekt. |
| Vlastniaca spoločnosť | Karta **Súhrn** | Právnická osoba, ktorá bude zodpovedať za náklady a výnosy, ktoré vzniknú z tohto projektu alebo z projektov súvisiacich s touto projektovou zmluvou. Po vytvorení zmluvy z cenovej ponuky sa toto pole skopíruje z príslušného poľa v zázname cenovej ponuky. | Vlastnená spoločnosť je rovnaká ako koncept právnickej osoby v module **Projektové riadenie a účtovníctvo** v Project Operations. Všetky náklady a výnosy z tohto projektu sa zaúčtujú v hlavnej účtovnej knihe vlastniacej spoločnosti. |
| Zákazník | Karta **Súhrn** | Referencia na záznam zákazníka spoločnosti zákazníka alebo obchodného vzťahu. Po vytvorení zmluvy z cenovej ponuky sa toto pole skopíruje z príslušného poľa v zázname cenovej ponuky. | Mena v cenovej zmluve projektu je predvolene založená na mene zákazníka. Menu je možné pred uložením zmluvy zmeniť. |
| Manažér obchodného vzťahu | Karta **Súhrn** | Meno manažéra obchodného vzťahu pre túto dohodu. Po vytvorení zmluvy z cenovej ponuky sa toto pole skopíruje z príslušného poľa v zázname cenovej ponuky. | Manažér obchodného vzťahu je zodpovedný za riadenie vzťahov so zákazníkom po dokončení tohto projektu. Na základe rezervovateľného záznamu zdroja naviazaného na manažéra obchodného vzťahu je v zmluvnej jednotke predvolená zmluva projektu. |
| Zmluvná jednotka | Karta **Súhrn** | Organizačná jednotka zodpovedná za realizáciu projektov spojených s touto zmluvou. Po vytvorení zmluvy z cenovej ponuky sa toto pole skopíruje z príslušného poľa v zázname cenovej ponuky. | Zmluvnou jednotkou je divízia spoločnosti, ktorá realizuje projekty. Každá zmluvná jednotka má menu, ktorá sa používa na vykazovanie odhadovaných a skutočných nákladov vzniknutých počas projektu. |
| Cenník produktov | Karta **Súhrn** | Toto je cenník, ktorý sa používa na predvolené ceny v riadkoch zmluvy. Rozbaľovací zoznam možností pre toto pole zobrazuje zoznam cenníkov, kde sa mena cenníka zhoduje s menou v zmluve. Po vytvorení zmluvy z cenovej ponuky sa toto pole skopíruje z príslušného poľa v zázname cenovej ponuky. Na projektovej  zmluve je toto pole predvolené zo záznamu obchodného vzťahu, ale je možné ho zmeniť. | Pre toto pole neexistuje žiadna následná relevancia. |
| Mena | Karta **Súhrn** | Mena použitá na hlásenie hodnoty tejto dohody a mena, v ktorej bude zákazníkovi fakturovaná. Po vytvorení zmluvy z cenovej ponuky sa toto pole skopíruje z príslušného poľa v zázname cenovej ponuky. Na projektovej zmluve je toto pole predvolené zo záznamu obchodného vzťahu, ale je možné ho zmeniť. | Po uložení zmluvy už toto pole nie je možné upravovať. Toto pole sa používa na predvolenie cenníkov produktov a projektov v zmluve. Mena v zmluve sa používa na zhodu s menou v cenníku. |
| Limit, ktorý sa nesmie prekročiť | Karta **Súhrn** | Toto pole naznačuje vyjednaný horný limit konečnej hodnoty, s ktorou zákazník v prípade tejto dohody súhlasí. | Horný limit sa hodnotí počas vykonávania a je použiteľný vo všetkých riadkových položkách a projektoch spojených s touto dohodou. |
| Požadovaný dátum doručenia | Karta **Súhrn** | Po vytvorení zmluvy z cenovej ponuky projektu sa toto pole skopíruje z príslušného poľa v zázname cenovej ponuky projektu. | Tento dátum sa používa ako konečný dátum na generovanie plánov faktúr. |

Nasledujúce KPI sú k dispozícii na karte **Plnenie zmluvy** projektovej zmluvy.

| Pole | Miesto | Relevantnosť, účel a pokyny |
| --- | --- | --- |
| Hodnota zmluvy | Celková zmluva | Celková hodnota projektovej zmluvy. |
| Fakturovaná suma | Celková zmluva | Súčet súm na všetkých faktúrach oproti tejto zmluve. |
| Vynaložené náklady | Celková zmluva | Súčet všetkých skutočných nákladov zaznamenaných vo všetkých projektoch, ktoré sú priradené k zmluve. |
| Hrubá marža | Celková zmluva | Fakturovaná suma - náklady vzniknuté do dátumu/fakturovaná suma |
| Očakávaná marža | Celková zmluva | (Hodnota zmluvy - Odhadované náklady)/Hodnota zákazky Odhadované náklady = Súčet všetkých odhadovaných nákladov na všetky projekty priradené k zmluve.|
| Hodnota zmluvy | Riadky založené na projekte | Hodnota riadku zmluvy. |
| Fakturovaná suma | Riadky založené na projekte | Pre riadok zmluvy s pevnou cenou: Súčet súm na všetkých skutočných míľnikoch fakturovaného predaja oproti tomuto riadku zmluvy na rôznych faktúrach vytvorených pre túto zmluvu. Pre riadok zmluvy času a materiálu: Súčet súm na všetkých skutočných fakturovateľného predaja oproti tomuto riadku zmluvy na rôznych faktúrach vytvorených pre túto zmluvu. |
| Vynaložené náklady | Riadky založené na projekte | Súčet všetkých skutočných nákladov zaznamenaných vo všetkých projektoch, ktoré sú priradené k zmluve. |
| Hrubá marža | Riadky založené na projekte | (Fakturovaná suma - náklady vzniknuté do dátumu)/fakturovaná suma |
| Očakávaná marža | Riadky založené na projekte | (Suma riadku zmluvy v základnej mene - Odhadované náklady na riadok zmluvy v základnej mene)/Výška riadku zmluvy v základnej mene |
| Vynaložené náklady | Detail riadka na základe projektu | Čas: Súčet čiastok na časové náklady pre túto rolu v projekte, ktorá je priradená k riadku zmluvy. Výdavky: Súčet čiastok na všetky výdavky pre túto kategóriu v projekte, ktorá je priradená k riadku zmluvy. |
| Zaznamenané množstvo | Detail riadka na základe projektu | Čas: Všetky časové údaje o skutočných časových nákladoch pre rolu v projekte, ktorá je priradená k tomuto riadku zmluvy. Výdavky: Všetky množstvá pre túto kategóriu výdavkov pre skutočnú hodnotu výdavkov v projekte, ktorý je priradený k tomuto riadku zmluvy. |
| Fakturovaná suma | Detail riadka na základe projektu | Pre riadok zmluvy s pevnou cenou zostáva toto pole na úrovni podrobností prázdne a zobrazuje sa iba na úrovni riadku zmluvy. Pre časový a materiálny riadok kontaktu sa výpočty dokončujú na úrovni podrobností. Podrobnosti zobrazujú súčet sumy na všetkých fakturovaných riadkoch výnosov oproti tomuto riadku zmluvy, ktoré sú spoplatnené. |
| Fakturované množstvo | Detail riadka na základe projektu | Pre riadok zmluvy s pevnou cenou zostáva toto pole na úrovni podrobností prázdne a zobrazuje sa iba na úrovni riadku zmluvy. Pre časový a materiálny riadok kontaktu sa výpočty dokončujú na úrovni podrobností pre čas a výdavky. Čas: Súčet hodín na všetkých fakturovaných riadkoch výnosov pre túto rolu oproti tomuto riadku zmluvy, ktoré sú spoplatnené. Výdavky: Všetky množstvá pre túto kategóriu výdavkov pre skutočnú hodnotu výdavkov v projekte, ktorý je priradený k tomuto riadku zmluvy. |
| Hodnota zmluvy | Riadky založené na produkte | Hodnota riadka zmluvy tohto produktového riadka zmluvy. |
| Fakturovaná suma | Riadky založené na produkte | Súčet súm na všetkých riadkoch faktúr oproti tomuto riadku zmluvy o produkte na rôznych faktúrach, ktoré sú vytvorené pre túto zmluvu. |
| Vynaložené náklady | Riadky založené na produkte | Súčet všetkých skutočných nákladov zaznamenaných v riadku zmluvy na základe produktu. |
| Hrubá marža | Riadky založené na projekte | Fakturovaná suma - náklady vzniknuté do dátumu/fakturovaná suma |
| Očakávaná marža | Riadky založené na produkte | (Hodnota riadku zmluvy - Odhadované náklady na riadok zmluvy)/Hodnota riadku zmluvy |
