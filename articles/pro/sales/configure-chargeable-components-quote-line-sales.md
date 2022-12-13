---
title: Nakonfigurujte spoplatnené komponenty na riadkoch projektovej ponuky
description: Tento článok poskytuje informácie o nastavení účtovateľných a neúčtovateľných zložiek v riadku cenovej ponuky založenej na projekte.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1e454278a1c5c24ac346c537c778b25448d9ea03
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825537"
---
# <a name="configure-chargeable-components-on-project-quote-lines"></a>Nakonfigurujte spoplatnené komponenty na riadkoch projektovej ponuky

_**Vzťahuje sa na:** Čiastočné nasadenie – dohoda o fakturácii pro forma, Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Riadok cenovej ponuky na základe projektu má koncept *zahrnutej* zložky a *účtovateľnej* zložky.

Zahrnuté komponenty sa vzťahujú na:

  - Spôsob fakturácie a rozdelenie zákazníkov
  - Limity, ktoré sa nesmú prekročiť 
  - Nastavenia frekvencie faktúr definované v riadku cenovej ponuky na základe projektu

Podskupinu zahrnutých zložiek možno označiť ako účtovateľnú pomocou poľa **Typ fakturácie**. Pole **Typ fakturácie** je súpravou volieb, ktoré môžu obsahovať nasledujúce hodnoty v kontexte riadka cenovej ponuky:

  - Účtovateľné
  - Neúčtovateľné

Účtovateľné zložky možno definovať pre úlohy, roly a kategórie transakcií.

Účtovateľnosť je definovaná na úlohách pre riadok cenovej ponuky a vzťahuje sa na všetky triedy transakcií zahrnuté v tomto riadku. Ak je pole **Zahrnúť úlohy** nastavené na **Celý projekt** alebo je ponechané prázdne, karta **Účtovateľné úlohy** nebude k dispozícii.

Účtovateľnosť je definovaná pre riadok cenovej ponuky a vzťahuje sa iba na triedu transakcie **Čas**. Ak je pole **Zahrnúť čas** nastavené na **Nie** v riadku cenovej ponuky projektu, karta **Účtovateľné roly** nebude k dispozícii.

Účtovateľnosť je definovaná pre kategórie transakcií pre riadok cenovej ponuky sa vzťahuje iba na triedu transakcie **Výdavok**. Ak je pole **Zahrnúť výdavky** nastavené na **Nie** v riadku cenovej ponuky projektu, karta **Účtovateľné kategórie** nebude k dispozícii.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Aktualizácia úlohy projektu, ktorá má byť účtovateľná alebo neúčtovateľná

Projektová úloha môže byť účtovateľná alebo neúčtovateľná v kontexte špecifického riadku cenovej ponuky na základe projektu, čo umožňuje nasledujúce nastavenie.

Ak riadok cenovej ponuky založený na projekte obsahuje **Čas** a úlohu **T1**, úloha je priradená k riadku cenovej ponuky ako účtovateľná. Ak existuje druhý riadok cenovej ponuky, ktorý obsahuje **Výdavky**, môžete úlohu **T1** v riadku cenovej ponuky priradiť ako neúčtovateľnú. Výsledkom je, že všetok čas zaznamenaný pri úlohe je účtovateľný a všetky výdavky zaznamenané pre úlohu nie sú neúčtovateľné.

Typ fakturácie úlohy je možné nakonfigurovať na karte **Fakturovateľné úlohy** riadku cenovej ponuky založenej na projekte aktualizáciou poľa **Typ fakturácie** na vedľajšej mriežke **Úlohy riadkov cenovej ponuky**. Prípadne môžete aktualizovať typ fakturácie pre projektovú úlohu v poli **Typ fakturácie** vo vedľajšej mriežke v nastavení fakturácie úloh projektu, ktoré zobrazuje riadky cenovej ponuky spojené s úlohou.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aktualizácia roly, ktorá má byť účtovateľná alebo neúčtovateľná

Rola môže byť účtovateľná alebo neúčtovateľná v kontexte konkrétneho riadka cenovej ponuky založenej na projekte.

Typ fakturácie roly je možné nakonfigurovať na karte **Fakturovateľné roly** riadku cenovej ponuky aktualizáciou poľa **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné roly**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aktualizácia kategórie transakcie, ktorá má byť účtovateľná alebo neúčtovateľná

Kategória transakcie môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku cenovej ponuky.

Typ fakturácie transakcie je možné nakonfigurovať na karte **Fakturovateľné kategórie** riadku cenovej ponuky aktualizáciou poľa **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné kategórie**.

### <a name="resolve-chargeability"></a>Vyriešenie účtovateľnosti
Odhad alebo skutočná hodnota vytvorené pre čas sa budú považovať za účtovateľné iba v nasledujúcich prípadoch:

   - **Čas** je uvedený na riadku cenovej ponuky.
   - **Rola** je nakonfigurovaná ako účtovateľná na riadku cenovej ponuky.
   - **Zahrnuté úlohy** sú nastavené na možnosť **Vybrané úlohy** na riadku cenovej ponuky. 

Ak sú tieto tri veci pravdivé, **Úloha** je tiež nakonfigurovaná ako účtovateľná. 

Odhad alebo skutočná hodnota vytvorené pre výdavky sa považujú za účtovateľné iba v nasledujúcich prípadoch: 

   - **Výdavok** je uvedený na riadku cenovej ponuky.
   - **Kategória transakcie** je nakonfigurovaná ako účtovateľná na riadku cenovej ponuky.
   - **Zahrnuté úlohy** sú nastavené na možnosť **Vybrané úlohy** na riadku cenovej ponuky.

Ak sú tieto tri veci pravdivé, **Úloha** je tiež nakonfigurovaná ako účtovateľná. 

Odhad alebo skutočná hodnota vytvorené pre materiál sa budú považovať za účtovateľné iba v nasledujúcich prípadoch:

   - **Materiál** je uvedený na riadku cenovej ponuky.
   - **Zahrnuté úlohy** sú nastavené na možnosť **Vybrané úlohy** na riadku cenovej ponuky.

Ak sú tieto dve veci pravdivé, **Úloha** by mala byť tiež nakonfigurovaná ako účtovateľná. 


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
Nedá sa nastaviť </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: Účtovateľné </p>
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
Účtovateľné </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturácia skutočnej hodnoty času: Účtovateľné </p>
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
Nedá sa nastaviť </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Účtovateľné</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nedá sa nastaviť </p>
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
Nedá sa nastaviť </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Neúčtovateľné</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nedá sa nastaviť </p>
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
Nedá sa nastaviť </p>
            </td>
            <td width="65" valign="top">
                <p>
Nedá sa nastaviť </p>
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
Nedá sa nastaviť </p>
            </td>
            <td width="65" valign="top">
                <p>
Nedá sa nastaviť </p>
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
Nedá sa nastaviť </p>
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
Nedá sa nastaviť </p>
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
