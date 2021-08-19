---
title: Vytvorenie opravných projektových faktúr
description: Táto téma poskytuje informácie o opravných faktúrach v Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cde82bb3c5777458a63a44a131af284e6ed5d7532de6aacbb5eb860c1fcddebd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006219"
---
# <a name="create-corrective-project-based-invoices"></a>Vytvorenie opravných projektových faktúr 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Potvrdenú projektovú faktúru je možné podľa dohody so zákazníkom a projektovým manažérom opraviť tak, že sa spracujú zmeny alebo pripíšu kredity.

Ak chcete vykonať úpravy potvrdenej faktúry, otvorte potvrdenú faktúru a vyberte **Opraviť túto faktúru**. 

> [!NOTE]
> Tento výber nie je k dispozícii, pokiaľ nie je potvrdená projektová faktúra.

Z potvrdenej faktúry sa vytvorí nový koncept faktúry. Všetky podrobnosti o riadku faktúry z predtým potvrdenej faktúry sa skopírujú do nového konceptu. Nasleduje niekoľko kľúčových bodov, ktoré vám pomôžu lepšie porozumieť podrobnostiam riadkov v novej opravenej faktúre:

- Všetky množstvá sa aktualizujú na nulu. Toto predpokladá, že všetky fakturované položky sú úplne pripísané. V prípade potreby môžete tieto množstvá manuálne aktualizovať, aby odrážali množstvo, ktoré sa fakturuje, a nie množstvo, ktoré sa pripisuje. Na základe zadaného množstva aplikácia vypočíta pripísané množstvo. Táto suma sa odráža v skutočnostiach, ktoré sa vytvárajú pri potvrdení opravenej faktúry. Ak robíte zmeny v sume dane, musíte zadať správnu sumu dane, a nie sumu dane, ktorá sa pripisuje.
- Opravy medzníkov sa vždy spracúvajú ako úplné kredity.
- Ak bola zákazníkovi fakturovaná nesprávna suma, sumy preddavku alebo zálohy je možné opraviť.
- Odsúhlasenia preddavkov a záloh je možné opraviť, ak bola použitá nesprávna suma na odsúhlasenie oproti nákladom na predtým potvrdenej faktúre.

> [!IMPORTANT]
> Detaily riadka faktúry, ktoré sú opravami ďalších už fakturovaných poplatkov, majú pole **Oprava** nastavené na **Áno**. Faktúry, ktoré majú opravené podrobnosti o riadku faktúry, majú pole s názvom **Obsahuje opravy**, ktoré je tiež nastavené na **Áno**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Skutočné hodnoty vytvorené po potvrdení opravnej faktúry

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
Stav faktúry medzníka sa aktualizuje z <b>Faktúra pre zákazníka bola zaúčtovaná</b> na <b>Pripravené na fakturáciu</b>.
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
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
