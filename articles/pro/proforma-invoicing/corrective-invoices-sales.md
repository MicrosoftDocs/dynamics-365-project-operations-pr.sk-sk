---
title: Opravné projektové faktúry
description: Tento článok poskytuje informácie o tom, ako vytvoriť a potvrdiť opravné faktúry v prevádzke projektu.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3e8e10d69368f4704ec6121106fbfd35394dc441
ms.sourcegitcommit: 95dacb0e74fa8970f56fdb1cbaa915d3fbec6e0f
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/17/2022
ms.locfileid: "9023678"
---
# <a name="corrective-project-invoices"></a>Opravné projektové faktúry

_**Vzťahuje sa na:** Čiastočné nasadenie – dohoda o fakturácii pro forma, Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Potvrdenú projektovú faktúru je možné podľa dohody so zákazníkom a projektovým manažérom opraviť tak, že sa spracujú zmeny alebo pripíšu kredity.

Ak chcete vykonať úpravy potvrdenej faktúry, otvorte potvrdenú faktúru a vyberte **Opraviť túto faktúru**. 

> [!NOTE]
> Tento výber nie je k dispozícii, pokiaľ nie je potvrdená projektová faktúra.

Z potvrdenej faktúry sa vytvorí nový koncept faktúry. Všetky podrobnosti o riadku faktúry z predtým potvrdenej faktúry sa skopírujú do nového konceptu. Ďalej sú uvedené niektoré kľúčové body pre podrobnosti o riadkoch v novej opravenej faktúre, ktorým je potrebné porozumieť:

- Všetky množstvá sa aktualizujú na nulu. Aplikácia predpokladá, že všetky fakturované položky sú úplne pripísané. V prípade potreby môžete tieto množstvá manuálne aktualizovať, aby odrážali množstvo, ktoré sa fakturuje, a nie množstvo, ktoré sa pripisuje. Na základe zadaného množstva aplikácia vypočíta pripísané množstvo. Táto suma sa odráža v skutočnostiach, ktoré sa vytvárajú pri potvrdení opravenej faktúry. Ak robíte zmeny v sume dane, musíte zadať správnu sumu dane, a nie sumu dane, ktorá sa pripisuje.
- Predtým potvrdené riadky zmlúv založené na produkte sa nekopírujú. Spracovanie opráv vo projektovej faktúre založenej na produkte nie je podporované.
- Opravy medzníkov sa vždy spracúvajú ako úplné kredity.
- Ak bola zákazníkovi fakturovaná nesprávna suma, sumy preddavku alebo zálohy je možné opraviť.
- Odsúhlasenia preddavkov a záloh je možné opraviť, ak bola použitá nesprávna suma na odsúhlasenie oproti nákladom na predtým potvrdenej faktúre.

> [!IMPORTANT]
> Podrobnosti o riadku faktúry, ktoré sú opravami ďalších už fakturovaných nákladov, majú pole **Oprava** nastavené na **Áno**. Faktúry, ktoré majú opravené podrobnosti o riadku faktúry, majú pole s názvom **Obsahuje opravy**, ktoré je tiež nastavené na **Áno**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Skutočné hodnoty vytvorené po potvrdení opravnej faktúry

V nasledujúcej tabuľke sú uvedené skutočné hodnoty, ktoré sa vytvoria pri potvrdení opravnej faktúry.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenár</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Skutočné hodnoty vytvorené po potvrdení</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Potvrdenie opravy fakturovaného preddavku alebo zálohy.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturovaný obrat predaja preddavku alebo zálohy, ktorý bol vytvorený na odsúhlasenie. Táto suma je kladná, pretože má zrušiť zápornú hodnotu, ktorá sa vytvorila pri fakturácii preddavku alebo zálohy.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Storno skutočnej hodnoty fakturovaného predaja sa vytvorí pre sumu preddavku alebo zálohy na stornovanie pôvodného fakturovaného predaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový opravený fakturovaný predaj sa vytvorí pre opravenú sumu v riadku opravenej faktúry založenej na preddavku alebo zálohe.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Skutočná hodnota nevyfakturovaného predaja so zápornou sumou v opravenom riadku faktúry založenej na preddavku alebo zálohe, ktorý sa má použiť na odsúhlasenie.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Potvrdenie o oprave predtým odsúhlaseného preddavku alebo zálohy.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturovaný obrat predaja preddavku alebo zálohy, ktorý bol vytvorený na odsúhlasenie. Táto suma je kladná a má zrušiť zápornú hodnotu, ktorá sa vytvorila pri predchádzajúcom odsúhlasení.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Skutočná hodnota stornovaného fakturovaného predaja pre sumu na predchádzajúcej faktúre.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový opravený fakturovaný predaj pre opravenú sumu preddavku, ktorý sa použije v opravenej faktúre.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Skutočná hodnota nevyfakturovaného predaja so zápornou sumou v opravenom zostávajúcom preddavku alebo zálohe, ktorý sa má použiť na odsúhlasenie v ďalších faktúrach.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturácia plného kreditu z predtým fakturovanej časovej transakcie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storno vyfakturovaného predaja pre hodiny a sumu v riadku s podrobnosťami pôvodnej faktúry pre čas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja pre hodiny a sumu v riadku s podrobnosťami pôvodnej faktúry pre čas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturácia čiastočného kreditu pre časovú transakciu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storno vyfakturovaného predaja pre hodiny a vyfakturovanú sumu v riadku s podrobnosťami pôvodnej faktúry pre čas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, jeho zrušenie a ekvivalentná skutočná hodnota fakturovaného predaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná pre zostávajúce hodiny a sumu po odpočítaní opravených hodnôt v podrobnostiach o riadku faktúry.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturácia plného kreditu z predtým fakturovanej výdavkovej transakcie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storno vyfakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre výdavok.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre výdavok.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturácia čiastočného kreditu z predtým fakturovanej výdavkovej transakcie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storno vyfakturovaného predaja pre fakturované množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre výdavok.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach opraveného riadka faktúry, jeho zrušenie a ekvivalentná skutočná hodnota fakturovaného predaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná pre zostávajúce množstvo a sumu po odpočítaní opravených hodnôt v podrobnostiach o riadku faktúry.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturácia celého kreditu predtým fakturovanej transakcie materiálu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Fakturované storno predaja pre množstvo a sumu na pôvodnom riadku faktúry s podrobnosťami za materiál.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja pre množstvo a sumu na pôvodnom riadku faktúry s podrobnosťami za materiál.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturácia čiastočného kreditu pri transakcii materiálu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Fakturované storno predaja pre množstvo a sumu fakturovanú na pôvodnom riadku faktúry s podrobnosťami za materiál.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná za množstvo a sumu na upravenom detaile riadku faktúry, jej storno a ekvivalentná skutočná hodnota fakturovaného predaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná pre zostávajúce množstvo a sumu po odpočítaní opravených hodnôt v podrobnostiach o riadku faktúry.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturácia plného kreditu z predtým fakturovanej poplatkovej transakcie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storno vyfakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre poplatok.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre poplatok.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturácia čiastočného kreditu z predtým fakturovanej poplatkovej transakcie.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storno vyfakturovaného predaja pre množstvo a fakturovanú sumu v riadku s podrobnosťami pôvodnej faktúry pre poplatok.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného opravného riadka faktúry, jeho zrušenie a ekvivalentná skutočná hodnota fakturovaného predaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturácia plného kreditu z predtým fakturovaného medzníka.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storno vyfakturovaného predaja pre sumu v riadku s podrobnosťami pôvodnej faktúry pre medzník.
                </p>
                <p>
Stav faktúry medzníka sa aktualizuje z <b>Bola uverejnená faktúra pre zákazníka</b> na <b>Pripravené na fakturáciu</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturácia čiastočného kreditu z predtým fakturovaného medzníka.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nepodporované </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Kredity a opravy predtým fakturovaného riadku zmluvy založenej na projekte.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nepodporované </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
