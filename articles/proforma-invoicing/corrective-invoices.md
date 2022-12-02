---
title: Opravné projektové faktúry
description: Tento článok poskytuje informácie o tom, ako vytvárať a potvrdzovať opravné projektové faktúry v Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eecaf3dedeab5ff72d12808eb3144f9161313009
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931119"
---
# <a name="corrective-project-based-invoices"></a>Opravné projektové faktúry

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Potvrdenú projektovú faktúru je možné podľa dohody so zákazníkom a projektovým manažérom opraviť tak, že sa spracujú zmeny alebo pripíšu kredity.

Ak chcete vykonať úpravy potvrdenej faktúry, otvorte potvrdenú faktúru a vyberte **Opraviť túto faktúru**. 

> [!NOTE]
> Tento výber nie je k dispozícii, pokiaľ nie je potvrdená projektová faktúra alebo pokiaľ projektové faktúry neobsahujú zálohy alebo zadržané prostriedky alebo porovnanie záloh alebo zadržaných prostriedkov.

Z potvrdenej faktúry sa vytvorí nový koncept faktúry. Všetky podrobnosti o riadku faktúry z predtým potvrdenej faktúry sa skopírujú do nového konceptu. Ďalej sú uvedené niektoré kľúčové body pre podrobnosti o riadkoch v novej opravenej faktúre, ktorým je potrebné porozumieť:

- Všetky množstvá sa aktualizujú na nulu. Dynamics 365 Project Operations predpokladá, že všetky fakturované položky sú úplne pripísané. V prípade potreby môžete tieto množstvá manuálne aktualizovať, aby odrážali množstvo, ktoré sa fakturuje, a nie množstvo, ktoré sa pripisuje. Na základe zadaného množstva aplikácia vypočíta pripísané množstvo. Táto suma sa odráža v skutočnostiach, ktoré sa vytvárajú pri potvrdení opravenej faktúry. Ak robíte zmeny v sume dane, musíte zadať správnu sumu dane, a nie sumu dane, ktorá sa pripisuje.
- Opravy medzníkov sa vždy spracúvajú ako úplné kredity.


> [!IMPORTANT]
> Pre podrobnosti riadka faktúry, ktoré sú opravami ďalších už fakturovaných poplatkov, je pole **Oprava** nastavené na **Áno**. Pre faktúry, ktoré majú opravené podrobnosti riadka faktúry, je pole **Obsahuje opravy** nastavené na **Áno**.

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
Tento scenár nie je podporovaný.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
