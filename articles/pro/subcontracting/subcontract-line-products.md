---
title: Riadky subdodávateľskej zmluvy pre produkty
description: Táto téma vysvetľuje, ako zaznamenávať riadky subdodávateľskej zmluvy pre výrobky a používať rôzne polia na zaznamenávanie nákupov produktov od dodávateľov.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 71e4a48c3d29d7ea5b015f6c6797da60001fccff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579092"
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

| Pole | Popis | Funkčný vplyv|
| ----- | ----------- | ----------- |
| Meno | Názov riadka subdodávateľskej zmluvy, ktorý má pomôcť s identifikáciou. |Toto sa zobrazí ako prvý stĺpec vo všetkých vyhľadávaniach na základe riadkov subdodávateľských zmlúv.
| Popis | Stručný popis produktov, ktoré sa objednávajú na riadku subdodávateľskej zmluvy. | Nie je |
| Typ riadka | Toto pole má predvolenú hodnotu **Založené na množstve**. |Nie je |
| Spôsob fakturácie | Toto je množina možností, ktorý predstavuje dva hlavné zmluvné modely podporované zo strany Project Operations: **Pevná cena** a **Čas a materiál**. | Na základe zvoleného spôsobu fakturácie je pre riadky subdodávateľov s metódou fakturácie s pevnou cenou k dispozícii míľnik založený na faktúre. |
| Trieda transakcie |Toto pole má predvolenú hodnotu **Čas**. Ak chcete vytvárať riadky subdodávateľských zmlúv na nákup produktov, nastavte pole **Trieda transakcie** na **Materiál**.  | To naznačuje, že riadok zmluvy subdodávateľa sa používa na zaznamenávanie nákupu produktov, ktoré sa majú použiť na projektoch. |
| Vyberte produkt | Vyberte, či je kupovaný produkt vedený v katalógu produktov alebo ide o pridaný produkt. |Nie je |
| Produkt | Vyberte aktívny produkt z katalógu. Toto pole je k dispozícii iba vtedy, ak je možnosť **Vyberte produkt** nastavená na **Existujúci**. |Kombinácia **Výrobok** a **Jednotka** budú použité ako predvolené alebo vypočítané pre jednotkovú cenu pre riadok subdodávateľskej zmluvy.
| Pridaný produkt | Zadajte názov pridaného produktu. Toto pole je k dispozícii iba vtedy, ak je možnosť **Vyberte produkt** nastavená na **Pridaný**.  |Kúpna cena sa pri zapisovaných produktoch automaticky nevyplní.|
| Požadovaný dátum doručenia | Zadajte požadovaný dátum dodania produktov.| Tento dátum sa používa aj na výber cenníka projektu z cenníkov projektov pripojených k subdodávateľskej zmluve. Náklady na produkt na riadku subdodávateľskej zmluvy sa potom predvolene odvíjajú od tohto cenníka. |
| Zmluvný dátum doručenia | Zadajte dátum, kedy sú výrobky zmluvne dohodnuté na dodanie.  |Nie je|
| Objednané množstvo | Zadajte množstvo produktu, ktorý ste kúpili u predajcu.| Toto sa použije na zobrazenie upozornení, keď projektový manažér prečerpá z tohto množstva.|
| Skupina jednotiek | Táto hodnota je predvolená iba pre katalógové produkty. |Kedy je súčasne vybrané **Produkt** a **Požadovaný termín dodania**, systém vyberie príslušný cenník na základe dátumu dodania. Na zodpovedajúci produkt sa dopytujú súvisiace položky v cenníku. Hodnoty jednotky a jednotkovej skupiny sú predvolené z nastavenia v zázname položky v cenníku. |
| Jednotka | Táto hodnota je predvolene nastavená na jednotku nastavenú v zázname položky cenníka. Podľa potreby to môžete zmeniť na inú jednotku.| Kombinácia produktu a jednotky sa používa na predvolenie jednotkovej ceny na riadku subdodávateľskej zmluvy pre existujúce katalógové produkty. |
| Jednotková cena | Jednotková cena sa predvolene používa kombináciou produktu a jednotky z položiek v cenníku súvisiacich s cenníkom projektu, ktorý je použiteľný pre požadovaný dátum dodania riadku subdodávateľskej zmluvy.  |Nie je |
| Medzisúčet | Toto pole iba na čítanie sa vypočíta ako množstvo × jednotková cena, ak majú obe polia zadané hodnoty. Ak buď je niektoré z polí **Množstvo** alebo **Jednotková cena** prázdne, môžete hodnotu zadať ručne.  |Nie je |
| Daň z predaja | Zadajte hodnotu dane z predaja. |Nie je |
| Celková čiastka | Toto vypočítané pole ukazuje celkovú sumu riadka subdodávateľskej zmluvy po zahrnutí daní. Hodnota v tomto poli sa vypočíta ako medzisúčet + daň. |Nie je |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
