---
title: Riadky subdodávateľskej zmluvy pre produkty
description: Táto téma vysvetľuje, ako zaznamenávať riadky subdodávateľskej zmluvy pre výrobky a používať rôzne polia na zaznamenávanie nákupov produktov od dodávateľov.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323705"
---
# <a name="subcontract-lines-for-products"></a>Riadky subdodávateľskej zmluvy pre produkty

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Subdodávateľská zmluva v Dynamics 365 Project Operations môže mať pre produkty riadok subdodávateľskej zmluvy. Tieto riadky umožňujú projektovému manažérovi nakupovať produkty od dodávateľov, ktoré potom môžu použiť pri projektových úlohách.

Vykonajte nasledujúce kroky na vytvorenie riadku subdodávateľskej zmluvy pre produkty v Project Operations.

1. Na navigačnej stránke vyberte položku **Subdodávateľské zmluvy** a potom otvorte subdodávateľskú zmluvu, s ktorou chcete pracovať. 
2. Na karte **Riadky subdodávateľskej zmluvy** vyberte **+ Nový** a vytvorte nový riadok subdodávateľskej zmluvy.
3. Na stránke **Rýchle vytvorenie** v poli **Trieda transakcie** vyberte **Materiál** a zadajte alebo vyberte požadované informácie o poli. 
4. Vyberte položku **Uložiť**.

Nasledujúca tabuľka poskytuje informácie o poliach na stránke **Podrobnosti riadka subdodávateľskej zmluvy** a stránke **Rýchle vytvorenie**, pretože sú relevantné pre nákup produktov.

| Pole | Popis |
| ----- | ----------- |
| Meno | Názov riadku subdodávateľskej zmluvy. |
| Popis | Stručný popis produktov, ktoré sa objednávajú na riadku subdodávateľskej zmluvy. |
| Typ riadka | Táto hodnota poľa je predvolene nastavená na **Založené na množstve**. |
| Spôsob fakturácie |  Spôsob fakturácie riadka subdodávateľskej zmluvy. Pre metódy fakturácie s pevnou cenou je k dispozícii plán faktúr založený na medzníkoch. |
| Trieda transakcie | Táto hodnota poľa je predvolene nastavená na **Čas**. Ak chcete vytvoriť riadky subdodávateľských zmlúv na nákup produktov, v poli **Trieda transakcie** vyberte **Materiál**. Tento výber naznačuje, že riadok subdodávateľskej zmluvy sa používa na zaznamenanie nákupu produktov, ktoré sa majú použiť v projektoch. |
| Vyberte produkt | Vyberte, či je kupovaný produkt vedený v katalógu produktov alebo ide o pridaný produkt. |
| Produkt | Vyberte aktívny produkt z katalógu. Toto pole je k dispozícii iba vtedy, ak je možnosť **Vyberte produkt** nastavená na **Existujúci**. |
| Pridaný produkt | Zadajte názov pridaného produktu. Toto pole je k dispozícii iba vtedy, ak je možnosť **Vyberte produkt** nastavená na **Pridaný**.  |
| Požadovaný dátum doručenia | Vyberte požadovaný dátum dodania produktov. Tento dátum sa používa aj na výber cenníka projektu z cenníkov projektov pripojených k subdodávateľskej zmluve. Náklady na produkt na riadku subdodávateľskej zmluvy sa potom predvolene odvíjajú od tohto cenníka. |
| Zmluvný dátum doručenia | Vyberte dátum, kedy sú výrobky zmluvne dohodnuté na doručenie.  |
| Objednané množstvo | Zadajte množstvo produktu, ktorý ste kúpili u predajcu. Ak vedúci projektu prečerpá toto množstvo, zobrazí sa upozornenie. |
| Skupina jednotiek | Táto hodnota je predvolená iba pre katalógové produkty. Kedy je súčasne vybrané **Produkt** a **Požadovaný termín dodania**, systém vyberie príslušný cenník na základe dátumu dodania. Na zodpovedajúci produkt sa dopytujú súvisiace položky v cenníku. Hodnoty jednotky a jednotkovej skupiny sú predvolené z nastavenia v zázname položky v cenníku. |
| Jednotka | Táto hodnota je predvolene nastavená pre jednotku v zázname položky v cenníku. Podľa potreby to môžete zmeniť na inú jednotku. Kombinácia produktu a jednotky sa používa na predvolenie jednotkovej ceny na riadku subdodávateľskej zmluvy pre existujúce katalógové produkty. |
| Jednotková cena | Jednotková cena sa predvolene používa kombináciou produktu a jednotky z položiek v cenníku súvisiacich s cenníkom projektu, ktorý je použiteľný pre požadovaný dátum dodania riadku subdodávateľskej zmluvy.  |
| Medzisúčet | Toto pole iba na čítanie sa vypočíta ako množstvo × jednotková cena, ak majú obe polia zadané hodnoty. Ak buď je niektoré z polí **Množstvo** alebo **Jednotková cena** prázdne, môžete hodnotu zadať ručne.  |
| Daň z predaja | Zadajte hodnotu dane z predaja. |
| Celková čiastka | Toto vypočítané pole ukazuje celkovú sumu riadka subdodávateľskej zmluvy po zahrnutí daní. Hodnota v tomto poli sa vypočíta ako medzisúčet + daň. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
