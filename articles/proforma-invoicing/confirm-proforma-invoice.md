---
title: Potvrdenie faktúry pro forma
description: Táto téma poskytuje informácie o potvrdení proforma faktúry.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287887"
---
# <a name="confirm-a-proforma-invoice"></a>Potvrdenie faktúry pro forma

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Po potvrdení zálohovej faktúry sa stav projektovej faktúry aktualizuje na **Potvrdená**. Po potvrdení bude faktúra iba na čítanie. Odteraz bude možné faktúru opraviť, iba ak dôjde k opravám alebo kreditom iniciovaným zákazníkom alebo ak bude označená ako zaplatená.

Nasledujúca tabuľka obsahuje zoznam skutočných hodnôt vytvorených systémom. Tieto skutočné hodnoty sa vytvoria, keď sa vykonajú určité operácie s konceptom faktúry projektu pred jej potvrdením.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Scenár</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Skutočné hodnoty vytvorené po potvrdení</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturácia časovej transakcie bez akýchkoľvek úprav konceptu faktúry.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturovaný obrat predaja pre hodiny a sumu pri pôvodnom schválení času.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Vyfakturovaná skutočná hodnota predaja pre hodiny a sumu pri pôvodnom schválení času.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturácia časovej transakcie, ktorá bola upravená tak, aby sa znížilo množstvo.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturovaný obrat predaja pre hodiny a sumu pri pôvodnom schválení času.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je neúčtovateľná na zostávajúce hodiny a čiastku po odpočítaní opravených hodnôt v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturácia časovej transakcie, ktorá bola upravená tak, aby sa zvýšilo množstvo.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturovaný obrat predaja pre hodiny a sumu pri pôvodnom schválení času.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturácia transakcie výdavkov bez akýchkoľvek úprav konceptu faktúry.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturovaný obrat predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Vyfakturovaná skutočná hodnota predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturácia výdavkovej transakcie, ktorá bola upravená tak, aby sa znížilo množstvo.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturovaný obrat predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je neúčtovateľná na zostávajúce množstvo a čiastku po odpočítaní opravených hodnôt v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturácia výdavkovej transakcie, ktorá bola upravená tak, aby sa zvýšilo množstvo.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturovaný obrat predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturácia poplatku.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturovaný obrat predaja pre sumu poplatkov pri pôvodnom zázname v účtovnom denníku.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Vyfakturovaná skutočná hodnota predaja pre množstvo a sumu pri pôvodnom zázname poplatkov v účtovnom denníku.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturácia medzníka.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Vyfakturovaná skutočná hodnota predaja pre sumu medzníka pre pôvodný medzník v riadku zmluvy projektu.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]