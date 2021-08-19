---
title: Kľúčové pojmy v subdodávkach
description: Táto téma vysvetľuje niektoré kľúčové pojmy, ktoré sa vzťahujú na subdodávky v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01d2e57b99015c346be15e3504440c14cb9a54e24215c0b1c052c5112f4b940a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994295"
---
# <a name="key-concepts-in-subcontracting"></a>Kľúčové pojmy v subdodávkach

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma vysvetľuje niektoré kľúčové pojmy, ktoré by ste mali poznať, než začnete používať funkciu subdodávok v Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Zmluvná jednotka v subdodávke

Zmluvná jednotka predstavuje divíziu alebo prax, ktorá vlastní dodávku prípadného projektu. Zmluvnou jednotkou je tiež divízia, ktorá vstupuje do zmluvného vzťahu s dodávateľom.

## <a name="purchase-currency"></a>Mena nákupu

V Project Operations je menou nákupu mena, v ktorej je subdodávka vytvorená. Je to tiež mena, v ktorej sú zaznamenané náklady na subdodávateľa projektu. Mena nákupu sa môže líšiť od meny projektu a mena projektu sa môže naopak líšiť od meny predaja.

## <a name="billing-methods-on-subcontract-lines"></a>Spôsoby fakturácie na riadkoch subdodávateľskej zmluvy

Pre projekty zvyčajne existujú zmluvné modely založené na pevných poplatkoch a spotrebe. Project Operations podporuje tieto spôsoby fakturácie v kontexte predaja a nákupu. Pri nákupe fungujú spôsoby fakturácie nasledujúcim spôsobom:

- **Čas a materiál** – Keď riadok subdodávateľskej zmluvy používa spôsob fakturácie **Čas a materiál**, časové náklady sú zaznamenané na projekte, keď subdodávatelia na tomto projekte pracujú a zaznamenávajú čas. Tieto transakcie nákladov od subdodávateľov sa potom spárujú s riadkovými položkami na faktúrach dodávateľa. V tomto modeli môžu projektoví manažéri, ktorí používajú Project Operations, spájať a overovať riadky faktúry dodávateľa so zaznamenaným a schváleným časom subdodávateľa. Po dokončení overovania sa predchádzajúce skutočné náklady, ktoré boli zaznamenané po schválení, stornujú a v projekte sa vytvoria nové skutočné náklady, ktoré sú založené na faktúre dodávateľa.
- **Pevná cena** – V tomto modeli zmluvy založenom na fixných poplatkoch sú faktúry dodávateľov založené na pevných medzníkoch. Zdroje subdodávateľov však môžu hlásiť aj čas. Čas je potom skontrolovaný a schválený projektovým manažérom. Po schválení Project Operations vytvorí dočasné skutočné náklady na projekt. Potom, čo predajca odošle faktúru za medzník, môže projektový manažér porovnať predtým zaznamenané skutočné náklady s medzníkom. Po dokončení overovania sa skutočné náklady obrátia a zaznamenajú sa náklady založené na medzníkoch.

## <a name="project-price-lists-on-subcontracts"></a>Projektové cenníky v subdodávateľských zmluvách

Projektové cenníky sú cenníky, ktoré sa používajú na nastavenie nákupných cien pre čas, náklady a ďalšie komponenty súvisiace s projektom. Cenníkov môže byť viacero, pričom každý z nich môže mať v rámci Project Operations vlastnú subdodávateľskú zmluvu s účinnosťou od dátumu. Project Operations nepodporuje prekrývanie dátumov účinnosti v cenníkoch projektov pre subdodávateľskú zmluvu.

## <a name="transaction-classes-on-subcontracts"></a>Triedy transakcií v subdodávateľských zmluvách

Project Operations podporuje štyri typy tried transakcií:

- Čas
- Výdavok
- Materiál
- Poplatok

Náklady na nákup je možné odhadnúť a môžu byť vynaložené iba v triedach transakcií **Čas**, **Výdavky** a **Materiál**. **Poplatok** je trieda transakcie iba pre príjmy a nie je k dispozícii v obsahu nákupu.

## <a name="purchase-pricing-dimensions"></a>Cenové dimenzie nákupu

Cenové dimenzie vám umožňujú rozhodnúť, ktoré atribúty sa použijú na nastavenie nákupnej ceny a na predvolené hodnoty pre časové transakcie. Pokiaľ ide o nákup, Project Operations podporuje iba pevné súbory dimenzií pre nastavenie nákupných cien a predvolené hodnoty. Pri nastavovaní nákupnej ceny a predvolených hodnotách v riadkoch subdodávateľských zmlúv a časových transakciách subdodávateľských zmlúv ide o atribúty **Rola** a **Rezervovateľný zdroj**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]