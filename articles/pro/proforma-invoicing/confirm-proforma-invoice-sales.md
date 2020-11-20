---
title: Potvrdenie faktúry pro forma – čiastočné
description: Táto téma poskytuje informácie o potvrdzovaní zálohových faktúr v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176540"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Potvrdenie faktúry pro forma – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_


Po potvrdení zálohovej faktúry sa stav projektovej faktúry aktualizuje na **Potvrdená**. Po potvrdení bude faktúra iba na čítanie. Odteraz bude možné faktúru opraviť, iba ak dôjde k opravám alebo kreditom iniciovaným zákazníkom alebo ak bude faktúra označená ako zaplatená.

Nasledujúca tabuľka obsahuje zoznam skutočných hodnôt vytvorených systémom. Tieto skutočné hodnoty sa vytvoria, keď sa vykonajú určité operácie s konceptom faktúry projektu pred jej potvrdením.

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
Fakturácia zálohy alebo preddavku </p>
            </td>
            <td width="408" valign="top">
                <p>
Skutočná hodnota fakturovaného predaja typu <strong>Preddavok</strong> sa vytvára pre sumu na preddavku alebo na zálohe.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Skutočná hodnota nevyfakturovaného predaja so zápornou sumou preddavku alebo zálohy, ktorá sa má použiť na odsúhlasenie.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Po úplnom odsúhlasení preddavku alebo zálohy na faktúre.
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
Skutočná hodnota fakturovaného predaja pre sumu na tejto faktúre.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Po čiastočnom odsúhlasení preddavku alebo zálohy na faktúre.
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
Skutočná hodnota fakturovaného predaja pre sumu na tejto faktúre.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Negatívna skutočná hodnota nevyfakturovaného predaja zostávajúceho preddavku alebo suma zálohy, ktorá sa má použiť na odsúhlasenie na budúcich faktúrach.
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
Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty predaja a ekvivalentná skutočná hodnota fakturovaného predaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová skutočná hodnota nefakturovaného predaja, ktorá je neúčtovateľná na zostávajúce hodiny a čiastku po odpočítaní opravených hodnôt v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty predaja a ekvivalentná skutočná hodnota fakturovaného predaja.
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
Vyfakturovaná skutočná hodnota predaja pre množstvo a sumu pri pôvodnom schválení výdavkov </p>
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
Nová skutočná hodnota nefakturovaného predaja, ktorá je neúčtovateľná na zostávajúce množstvo a čiastku po odpočítaní opravených hodnôt v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalent skutočnej hodnoty fakturovaného predaja.
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
        <tr>
            <td width="216" valign="top">
                <p>
Účtovanie riadkov zmlúv založených na produkte.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Skutočná hodnota fakturovaného predaja pre riadok produktu s množstvom a sumou pochádzajúcou z riadka zmluvy založenej na produkte.
                </p>
            </td>
        </tr>
    </tbody>
</table>
