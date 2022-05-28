---
title: Konfigurácia fakturovateľných súčastí riadka zmluvy založenej na projekte
description: Táto téma poskytuje informácie o tom, ako pridávať účtovateľné zložky do riadkov zmluvy v Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c02228c5b75afdc825ffbf0ada9ca57001a173ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593217"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurácia fakturovateľných súčastí riadka zmluvy založenej na projekte

_**Vzťahuje sa na:** Čiastočné nasadenie – dohoda o fakturácii pro forma, Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Riadok zmluvy na základe projektu obsahuje *zahrnuté* zložky a *účtovateľné* zložky.

Zahrnuté zložky sú zložky, ktoré sa vzťahujú na:

  - Spôsob fakturácie a rozdelenie zákazníkov
  - Limity, ktoré sa nesmú prekročiť 
  - Nastavenia frekvencie faktúr definované v riadku zmluvy na základe projektu

Podskupinu zahrnutých zložiek možno označiť ako účtovateľnú pomocou poľa **Typ fakturácie**. Pole **Typ fakturácie** je súpravou volieb, ktoré môžu obsahovať nasledujúce hodnoty v kontexte riadka zmluvy:

  - Účtovateľné
  - Neúčtovateľné

Účtovateľné zložky možno definovať pre úlohy, roly a kategórie transakcií.

Účtovateľnosť je definovaná na úlohách pre riadok zmluvy projektu a vzťahuje sa na všetky triedy transakcií zahrnuté v riadku. Ak je pole **Zahrnúť úlohy** v riadku zmluvy prázdne alebo nastavené na **Celý projekt**, karta **Účtovateľné úlohy** nebude k dispozícii.

Účtovateľnosť definovaná pre roly pre riadok zmluvy projektu sa vzťahuje iba na triedu transakcie **Čas**. Ak je pole **Zahrnúť čas** v riadku zmluvy nastavené na **Nie**, karta **Účtovateľné roly** nebude k dispozícii.

Účtovateľnosť definovaná pre kategórie transakcií pre riadok zmluvy projektu sa vzťahuje iba na triedu transakcie **Výdavok**. Ak je pole **Zahrnúť výdavky** nastavené na **Nie**, karta **Účtovateľné kategórie** nebude k dispozícii.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Aktualizácia úlohy projektu ako účtovateľnej alebo neúčtovateľnej

Projektová úloha môže byť účtovateľná alebo neúčtovateľná v konkrétnom riadku zmluvy, čo umožňuje nasledujúce nastavenie:

Ak zahŕňa riadok zmluvy založený na projekte **Čas** a určitú úlohu, **T1** je k nej pridružená ako účtovateľná. Ak existuje druhý riadok zmluvy, ktorý obsahuje **Výdavky**, môžete úlohu T1 v riadku zmluvy priradiť ako neúčtovateľnú. Výsledkom je, že všetok čas zaznamenaný pri úlohe je účtovateľný a všetky výdavky nie sú neúčtovateľné.

Typ fakturácie úlohy je možné nakonfigurovať na karte **Fakturovateľné úlohy** riadka zmluvy aktualizáciou poľa **Typ fakturácie** na vedľajšej mriežke úlohy riadkov zmluvy. Prípadne môžete aktualizovať pole **Typ fakturácie** vo vedľajšej mriežke nastavenia fakturácie úloh projektu, ktoré zobrazuje riadky zmluvy spojené s úlohou.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Aktualizácia roly ako účtovateľnej alebo neúčtovateľnej

Rola môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku zmluvy.

Typ fakturácie role je možné nakonfigurovať na karte **Účtovateľné role** v riadku zmluvy. Ak to chcete urobiť, aktualizujte pole **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné roly**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Aktualizácia kategórie transakcie ako účtovateľnej alebo neúčtovateľnej

Kategória transakcie môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku zmluvy.

Typ fakturácie transakcie je možné nakonfigurovať na karte **Účtovateľné kategórie** v riadku zmluvy na základe projektu. Ak to chcete urobiť, aktualizujte pole **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné kategórie**.

### <a name="resolve-chargeability"></a>Vyriešenie účtovateľnosti

Odhad alebo skutočná hodnota vytvorené pre čas sa považuje za účtovateľné iba v nasledujúcich prípadoch:

   - **Čas** je uvedený na riadku zmluvy.
   - **Rola** je nakonfigurovaná ako účtovateľná na riadku zmluvy.
   - **Zahrnuté úlohy** sú nastavené na **Vybrané úlohy** na riadku zmluvy.
 
 Ak sú tieto tri veci pravdivé, úloha je nakonfigurovaná ako účtovateľná. 

Odhad alebo skutočná hodnota vytvorené pre výdavky sa považujú za účtovateľné iba v nasledujúcich prípadoch:

   - **Výdavok** je uvedený na riadku zmluvy
   - **Kategória transakcie** je nakonfigurovaná ako účtovateľná na riadku zmluvy
   - **Zahrnuté úlohy** sú nastavené na **Vybraná úloha** na riadku zmluvy.
  
 Ak sú tieto tri veci pravdivé, **Úloha** je nakonfigurovaná ako účtovateľná. 

Odhad alebo skutočná hodnota vytvorené pre materiál sa považujú za účtovateľné iba v nasledujúcich prípadoch:

   - **Materiály** sú uvedené na riadku zmluvy
   - **Zahrnuté úlohy** sú nastavené na **Vybrané úlohy** na riadku zmluvy

Ak sú tieto dve veci pravdivé, **Úloha** je nakonfigurovaná ako účtovateľná. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Zahrnie čas</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Zahrnie výdavok</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Zahŕňa materiály</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Zahrnuté úlohy</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Rola</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategória</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Úloha</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Dopad účtovateľnosti</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Áno </p>
            </td>
            <td width="78" valign="top">
                <p>
Áno </p>
            </td>
            <td width="63" valign="top">
                <p>
Áno </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="70" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie je možné nastaviť </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: <strong>Účtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty výdavku: <strong>Účtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty materiálu: <strong>Účtovateľné</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Áno </p>
            </td>
            <td width="78" valign="top">
                <p>
Áno </p>
            </td>
            <td width="63" valign="top">
                <p>
Áno </p>
            </td>
            <td width="75" valign="top">
                <p>
Iba vybraté úlohy </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="70" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: <strong>Účtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty výdavku: <strong>Účtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty materiálu: <strong>Účtovateľné</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Áno </p>
            </td>
            <td width="78" valign="top">
                <p>
Áno </p>
            </td>
            <td width="63" valign="top">
                <p>
Áno </p>
            </td>
            <td width="75" valign="top">
                <p>
Iba vybraté úlohy </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovateľné</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné </p>
                <p>
Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Áno </p>
            </td>
            <td width="78" valign="top">
                <p>
Áno </p>
            </td>
            <td width="63" valign="top">
                <p>
Áno </p>
            </td>
            <td width="75" valign="top">
                <p>
Iba vybraté úlohy </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="70" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovateľné</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty materiálu: <strong>Neúčtovateľné</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Áno </p>
            </td>
            <td width="78" valign="top">
                <p>
Áno </p>
            </td>
            <td width="63" valign="top">
                <p>
Áno </p>
            </td>
            <td width="75" valign="top">
                <p>
Iba vybraté úlohy </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovateľné</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovateľné</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty materiálu: <strong>Neúčtovateľné</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Áno </p>
            </td>
            <td width="78" valign="top">
                <p>
Áno </p>
            </td>
            <td width="63" valign="top">
                <p>
Áno </p>
            </td>
            <td width="75" valign="top">
                <p>
Iba vybraté úlohy </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovateľné</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Neúčtovateľné</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Áno </p>
            </td>
            <td width="63" valign="top">
                <p>
Áno </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie je možné nastaviť </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Účtovateľné</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie je možné nastaviť </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: <strong>Nedostupné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné </p>
                <p>
Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Áno </p>
            </td>
            <td width="63" valign="top">
                <p>
Áno </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie je možné nastaviť </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Neúčtovateľné</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie je možné nastaviť </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: <strong>Nedostupné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Áno </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Áno </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="70" valign="top">
                <p>
Nie je možné nastaviť </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie je možné nastaviť </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: Účtovateľné </p>
                <p>
Typ fakturácie skutočnej hodnoty výdavku:<strong> Nedostupné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Áno </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Áno </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovateľné</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Nie je možné nastaviť </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie je možné nastaviť </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty výdavku:<strong> Nedostupné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Áno </p>
            </td>
            <td width="78" valign="top">
                <p>
Áno </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="70" valign="top">
                <p>
Účtovateľné </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie je možné nastaviť </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: Účtovateľné </p>
                <p>
Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné </p>
                <p>
Typ fakturácie skutočnej hodnoty materiálu: <strong>Nedostupné</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Áno </p>
            </td>
            <td width="78" valign="top">
                <p>
Áno </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovateľné</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Neúčtovateľné</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nie je možné nastaviť </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </p>
                <p>
Typ fakturácie skutočnej hodnoty materiálu: <strong>Nedostupné</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
