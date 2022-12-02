---
title: Evidencia času, výdavkov a použitia materiálu pre súčasti v rámci subdodávateľskej zmluvy
description: Tento článok vysvetľuje, ako Microsoft Dynamics 365 Project Operations sleduje čas, výdavky a spotrebu materiálu zaznamenanú v projektoch zo subdodávateľských súčastí.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522533"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Evidencia času, výdavkov a použitia materiálu v projektoch pre súčasti v rámci subdodávateľskej zmluvy

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok vysvetľuje, ako Microsoft Dynamics 365 Project Operations sleduje čas, výdavky a spotrebu materiálu zaznamenanú v projektoch zo subdodávateľských súčastí.

## <a name="costing-for-subcontractor-time-on-projects"></a>Náklady na čas subdodávateľa na projektoch
V Project Operations môžu zmluvní pracovníci zaznamenávať čas na projektoch podobným spôsobom ako zamestnanci. Pri zaznamenávaní času v projektoch a/alebo projektových úlohách môže zmluvný pracovník vybrať konkrétnu subdodávateľskú zmluvu alebo riadok subdodávateľskej zmluvy.

Keď sa schváli čas predložený zmluvnými pracovníkmi, náklady na projekt sa zaznamenajú pomocou sadzby jednotkových nákladov, ktorá je nastavená pre zdroj zmluvného pracovníka v sekcii **Ceny rolí** cenníka nákupu v subdodávateľskej zmluve.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Náklady na subdodávateľské výdavky na projekty
Pri zadávaní výdavkov vynaložených na projekty môžete vybrať subdodávateľskú zmluvu a riadok subdodávok v zázname výdavkov. 

Po predložení a schválení tohto záznamu výdavkov sa náklad na výdavok zaznamená v projekte na základe jednotkovej ceny, ktorá je nastavená pre danú kategóriu transakcie v sekcii **Ceny kategórií** nákupného cenníka v subdodávateľskej zmluve.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Náklady na subdodávateľské materiály na projekty
Pri zadávaní použitia materiálov na projekty môžete vybrať subdodávateľskú zmluvu a riadok subdodávok v denníku použitia materiálu. Po predložení a schválení denníka použitia materiálu sa náklady na materiál zaznamenajú do projektu na základe jednotkovej ceny, ktorá je pre tento produkt nastavená v časti **Položky cenníka** cenníka subdodávateľskej zmluvy.

Použitie materiálu je možné zaznamenať aj pri zapísaných produktoch na projektoch. Tento typ použitia materiálu môže byť tiež spojený so subdodávateľskou zmluvou a riadkom subdodávateľskej zmluvy. Pri zaznamenávaní použitia materiálu pre produkty nezahrnuté do katalógu musíte zadať jednotkovú cenu produktu nezahrnutého do katalógu. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
