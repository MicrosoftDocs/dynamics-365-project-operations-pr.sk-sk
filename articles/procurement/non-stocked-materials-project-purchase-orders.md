---
title: Objednávanie neskladovaných materiálov pre projekt pomocou nákupných objednávok projektu
description: Tento článok vysvetľuje, ako si môžete objednať neskladové materiály pre projekt pomocou projektových objednávok.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929831"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Objednajte si kategórie obstarávania alebo neskladové materiály pre projekt pomocou projektových objednávok

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Oddelenie obstarávania vo vašej organizácii môže použiť [nákupné objednávky](/dynamics365/supply-chain/procurement/purchase-order-overview) na sledovanie objednávok tovaru a služieb. Objednávky pre kategórie obstarávania alebo neskladové materiály možno priradiť k projektu. Fakturácia týchto nákupných objednávok zaúčtuje náklady oproti projektu.

## <a name="prerequisites"></a>Predpoklady
Vykonajte nasledujúce kroky, aby ste povolili funkciu projektových objednávok.

1. V Dynamics 365 Finance prejdite na **Správa funkcií** pracovnom priestore.
2. V zozname funkcií vyhľadajte a vyberte funkciu, **Povoliť nákupné objednávky projektov v projektových operáciách pre scenáre založené na zdrojoch/nie na sklade**.
3. Vyberte položku **Povoliť**.
4. Nakonfigurujte materiály, ktoré nie sú na sklade, a faktúry čakajúce na dodávateľa, ako je popísané v [Konfigurácia neskladovaných materiálov a čakajúcich faktúr dodávateľov](configure-materials-nonstocked.md).
5. Nakonfigurujte kategórie obstarávania podľa popisu v [Použite kategórie obstarávania s projektovými nákupnými objednávkami a čakajúcimi faktúrami dodávateľa](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Vytvorte nákupnú objednávku projektu zo zoznamu objednávok projektu

1. Vo časti Finance prejdite na **Projektový manažment a účtovníctvo** > **Projekty** > **Všetky projekty** a vyberte projekt.
2. Na table akcií na karte **Spravovať** v skupine **Nový** vyberte **Úloha položky** > **Nákupná objednávka**.
3. Na stránke **Vytvoriť nákupnú objednávku** vyberte dodávateľa, u ktorého chcete zadať objednávku, zadajte podľa potreby ďalšie informácie a potom vyberte **OK**.
4. Na stránke **Nákupná objednávka** v mriežke **Riadky nákupných objednávok** vyberte **Pridať riadok**.
5. Zadajte číslo položky alebo kategóriu obstarávania, množstvo, jednotku, jednotkovú cenu a ďalšie informácie podľa potreby.

    > [!NOTE]
    > S objednávkami projektu je možné použiť iba kategórie obstarávania, neskladované položky a služby. Skladové položky nie sú podporované.

6. Pokračujte v pridávaní položiek alebo kategórií obstarávania podľa potreby a potvrďte nákupnú objednávku.

    Príjmy za tovar a služby je možné zaznamenať vytvorením a zaúčtovaním potvrdenia o produkte.

    > [!NOTE]
    > Príjmy z produktu sa nezaznamenávajú do skutočných nákladov na projekt v Microsoft Dataverse a nemajú vplyv na podzáložku projektu.

    Potom, čo predajca odošle faktúru za položky a služby na nákupnej objednávke, oddelenie obstarávania môže vygenerovať faktúru pre nákupnú objednávku tak, že prejdete na **Faktúra** > **Generovať** > **Faktúra** na table akcií. Ďalšie informácie o čakajúcich faktúrach dodávateľa nájdete v časti [Zakúpenie neskladovaného materiálu pomocou nespracovanej faktúry dodávateľa](pending-vendor-invoices.md).
