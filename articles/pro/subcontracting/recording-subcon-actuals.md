---
title: Evidencia času, výdavkov a použitia materiálu pre súčasti v rámci subdodávateľskej zmluvy
description: Tento článok vysvetľuje, ako spoločnosť Microsoft sleduje čas, výdavky a spotrebu materiálu zaznamenanú v projektoch zo subdodávateľských komponentov Dynamics 365 Project Operations.
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
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Evidencia času, nákladov a spotreby materiálu na projektoch pre subdodávateľské komponenty

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok vysvetľuje, ako spoločnosť Microsoft sleduje čas, výdavky a spotrebu materiálu zaznamenanú v projektoch zo subdodávateľských komponentov Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Náklady na čas subdodávateľa na projektoch
V projektových operáciách môžu zmluvní pracovníci zaznamenávať čas na projektoch podobným spôsobom ako zamestnanci. Pri zadávaní času na projektoch a/alebo projektových úlohách si zmluvný pracovník môže vybrať konkrétnu subdodávku a subdodávku.

Keď sa schváli čas predložený zmluvnými pracovníkmi, náklady na projekt sa zaznamenajú pomocou sadzby jednotkových nákladov, ktorá je nastavená pre zdroj zmluvného pracovníka v **Ceny rolí** časti kúpnej cenníka na subdodávke.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Kalkulácia nákladov na subdodávky na projekty
Pri zadávaní výdavkov vynaložených na projekty môžete vybrať subdodávku a riadok subdodávok na zázname výdavkov. 

Keď sa tento záznam o výdavkoch odošle a schváli, výdavkové náklady sa zaznamenajú v projekte na základe jednotkových nákladov, ktoré sú nastavené pre danú kategóriu transakcií v **Ceny kategórií** časti kúpnej cenníka na subdodávke.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Kalkulácia subdodávateľských materiálov na projektoch
Pri zadávaní spotreby materiálu na projektoch si môžete vybrať subdodávku a riadok subdodávok v protokole spotreby materiálu. Keď sa odošle a schváli protokol spotreby materiálu, materiálové náklady sa zaznamenajú v projekte na základe jednotkových nákladov, ktoré sú nastavené pre daný produkt v **Položky cenníka** časti cenníka subdodávok.

Spotrebu materiálu je možné zaznamenať aj pri zapísaných produktoch na projektoch. Tento typ použitia materiálu môže byť tiež spojený so subdodávkou a subdodávateľskou linkou. Pri zaznamenávaní spotreby materiálu pre produkty na zápis musíte zadať jednotkovú cenu produktu na zápis. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
