---
title: Fakturácia dodávateľov – koncept a tvorba
description: Tento článok popisuje koncepciu dodávateľských faktúr, scenárov používania a vysvetľuje, ako vytvoriť faktúry dodávateľov v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261963"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Fakturácia dodávateľov – koncept a tvorba

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Fakturácia dodávateľov v Microsoft Dynamics 365 Project Operations môže byť použitá na evidenciu nákladov z dodávok služieb a/alebo materiálov na projekte od dodávateľov.

Keď sú služby a/alebo materiály zadané dodávateľovi ako subdodávka, subdodávka predstavuje zmluvnú dohodu s týmto dodávateľom. Keď dodávateľ dodáva služby alebo keď sa materiály prijímajú a používajú na projektové úlohy, náklady sa zaznamenávajú do projektu. Dodávateľ pravidelne posiela faktúry, ktoré sú overené a spárované s nákladmi, ktoré sú zaznamenané v projekte. Po dokončení procesu overovania je faktúra dodávateľa potvrdená a uvoľnená na platbu.

## <a name="scenarios-for-use"></a>Scenáre použitia

Faktúry dodávateľa v Project Operations možno použiť na podporu dvoch odlišných scenárov.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Zákazníci využívajú všetky možnosti subdodávok

Možnosti faktúr dodávateľa poskytujú spôsob, ako overiť a spárovať záznamy času, spotreby materiálu a nákladov, ktoré odkazujú na subdodávateľské komponenty, s riadkami faktúry dodávateľa. Tento proces možno použiť na overenie presnosti riadkov faktúry dodávateľa. Po dokončení procesu overovania a potvrdení faktúry dodávateľa aplikácia stornuje skutočné údaje, ktoré boli zaznamenané v schválených protokoloch času, nákladov a použitia materiálu, a vytvorí nové skutočné náklady pomocou riadkov faktúry dodávateľa.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Zákazníci nevyužívajú všetky možnosti subdodávok, ale chcú mať jednotný pohľad na náklady na projekty v rámci Project Operations

Ak sledujete proces subdodávateľských zmlúv v systéme tretej strany, môžete zaznamenať náklady z tohto systému tretej strany do Project Operations vytvorením faktúr dodávateľa, ktoré neodkazujú na subdodávateľské zmluvy. Vaši projektoví manažéri tak môžu mať jednotný pohľad na všetky náklady na daný projekt.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Vytvorenie faktúr dodávateľa v Project Operations

Faktúry dodávateľov možno vytvoriť dvoma spôsobmi:

- Na stránke zoznamu faktúr dodávateľa alebo na stránke podrobností pre jednu faktúru dodávateľa
- Zo stránky so zoznamom subdodávateľských zmlúv alebo zo stránky s podrobnosťami pre jednu subdodávateľskú zmluvu

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Vytvorenie zo stránky zoznamu faktúr dodávateľa alebo zo stránky podrobností

1. Prejdite na **Nákup** \> **Dodávateľské faktúry**.
2. Na stránke zoznamu faktúr dodávateľa alebo na stránke podrobností pre jednu faktúru dodávateľa vyberte **Nová** na vytvorenie novej faktúry dodávateľa.

Faktúry dodávateľa, ktoré sú vytvorené týmto spôsobom, môžu tiež odkazovať na subdodávateľskú zmluvu.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Vytvorenie zo stránky zoznamu subdodávateľskej zmluvy alebo zo stránky podrobností

1. Prejdite na **Nákup** \> **Subdodávateľské zmluvy**.
2. Vyberte najmenej jednu subdodávateľskú zmluvu.
3. Na stránke zoznamu subdodávateľských zmlúv alebo na stránke podrobností pre jednu subdodávateľskú zmluvu vyberte **Vytvoriť faktúru dodávateľa** na vytvorenie novej faktúry dodávateľa.

Nová faktúra dodávateľa v stave **Koncept** sa vytvorí pre každú subdodávateľskú zmluvu, ktorú ste vybrali.

Faktúry dodávateľa, ktoré vytvoríte týmto spôsobom, vždy odkazujú na subdodávateľskú zmluvu v hlavičke faktúry dodávateľa. Každý riadok v subdodávateľskej zmluve, ktorý má spôsob fakturácie Čas a materiál, spôsobí vytvorenie riadku na faktúre dodávateľa. Každý riadok v subdodávateľskej zmluve, ktorý má spôsob fakturácie Pevná cena, spôsobí vytvorenie riadka na faktúre dodávateľa pre každý míľnik v riadku subdodávateľskej zmluvy, ktorý má stav **Pripravené na fakturáciu**.

Nasledujúce polia a súvisiace záznamy sa skopírujú zo subdodávateľskej zmluvy do hlavičky faktúry dodávateľa:

- Dodávateľ.
- Súvisiace cenníky budú skopírované do faktúry dodávateľa ako cenníky.
- Mena.
- Zmluvná jednotka.
- Platobné podmienky.

Pre riadky subdodávateľskej zmluvy Čas a materiál budú nasledujúce polia a súvisiace záznamy skopírované z riadku subdodávateľskej zmluvy do riadku faktúry dodávateľa:

- Referencie subdodávateľskej zmluvy a riadku subdodávateľskej zmluvy
- Trieda transakcie
- Rola
- Kategória transakcie
- Polia produktu
- Project
- Úloha
- Rezervovateľný zdroj

Pre riadky subdodávateľskej zmluvy Pevná cena budú nasledujúce polia skopírované z riadku subdodávateľskej zmluvy a medzníka riadku subdodávateľskej zmluvy do riadku faktúry dodávateľa:

- Referencie subdodávateľskej zmluvy a riadku subdodávateľskej zmluvy.
- Trieda transakcie. Predvolene bude hodnota **Medzník**.
- Názov a čiastka medzníka sa skopírujú zo súvisiaceho medzníka riadku subdodávateľskej zmluvy.
- Používateľ si bude môcť vybrať projekt a úlohu na riadku faktúry dodávateľa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
