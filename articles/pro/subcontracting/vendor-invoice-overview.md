---
title: Fakturácia dodávateľov – koncept a tvorba
description: Tento článok popisuje koncepciu dodávateľských faktúr, scenáre použitia a spôsob vytvárania dodávateľských faktúr v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911477"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Fakturácia dodávateľov – koncept a tvorba

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Fakturácia dodávateľa v spoločnosti Microsoft Dynamics 365 Project Operations možno použiť na evidenciu nákladov na dodávky služieb a/alebo materiálov na projekte dodávateľmi.

Keď sú služby a/alebo materiály zadané dodávateľovi ako subdodávka, subdodávka predstavuje zmluvnú dohodu s týmto dodávateľom. Keď dodávateľ dodáva služby alebo sa materiály prijímajú a používajú na projektové úlohy, náklady sa zaznamenávajú do projektu. Dodávateľ pravidelne posiela faktúry, ktoré sú overené a spárované s nákladmi, ktoré sú zaznamenané v projekte. Po dokončení procesu overovania je faktúra dodávateľa potvrdená a uvoľnená na platbu.

## <a name="scenarios-for-use"></a>Scenáre na použitie

Faktúry dodávateľa v projektových operáciách možno použiť na podporu dvoch odlišných scenárov.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Zákazníci využívajú všetky subdodávateľské skúsenosti

Skúsenosti s faktúrami dodávateľa poskytujú spôsob, ako overiť a spárovať záznamy času, spotreby materiálu a nákladových záznamov, ktoré odkazujú na subdodávateľské komponenty s riadkami faktúr dodávateľa. Tento proces možno použiť na overenie presnosti riadkov faktúry dodávateľa. Po dokončení procesu overovania a potvrdení faktúry dodávateľa aplikácia stornuje skutočnosti, ktoré boli zaznamenané v schválených protokoloch času, nákladov a spotreby materiálu, a vytvorí nové skutočné náklady pomocou riadkov faktúry dodávateľa.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Zákazníci nevyužívajú úplné skúsenosti so subdodávateľmi, ale chcú mať jednotný pohľad na náklady na projekty v projektových operáciách

Ak sledujete proces subdodávok v systéme tretej strany, môžete zaznamenať náklady z tohto systému tretej strany do projektových operácií vytvorením faktúr dodávateľa, ktoré neodkazujú na subdodávky. Vaši projektoví manažéri tak môžu mať jednotný pohľad na všetky náklady na daný projekt.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Vytváranie dodávateľských faktúr v projektových operáciách

Faktúry dodávateľa je možné vytvárať dvoma spôsobmi:

- Na stránke zoznamu faktúr dodávateľa alebo na stránke podrobností pre jednu faktúru dodávateľa
- Zo stránky so zoznamom subdodávok alebo zo stránky s podrobnosťami pre jednu subdodávku

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Vytvorenie zo stránky zoznamu faktúr dodávateľa alebo zo stránky podrobností

1. Ísť do **Nákup** \> **Dodávateľské faktúry**.
2. Na stránke zoznamu faktúr dodávateľa alebo na stránke podrobností pre jednu faktúru dodávateľa vyberte **Nový** na vytvorenie novej faktúry dodávateľa.

Faktúry dodávateľa, ktoré sú vytvorené týmto spôsobom, môžu tiež odkazovať na subdodávku.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Vytvorenie zo stránky so zoznamom subdodávok alebo zo stránky s podrobnosťami

1. Ísť do **Nákup** \> **Subdodávky**.
2. Vyberte jednu alebo viacero subdodávok.
3. Na stránke so zoznamom subdodávok alebo na stránke podrobností pre jednu subdodávku vyberte **Vytvorte faktúru dodávateľa** na vytvorenie novej faktúry dodávateľa.

Nová faktúra dodávateľa v **Návrh** stav sa vytvorí pre každú subdodávku, ktorú ste vybrali.

Faktúry dodávateľa, ktoré vytvoríte týmto spôsobom, vždy odkazujú na subdodávku v hlavičke faktúry dodávateľa. Každý riadok v subdodávke, ktorý má spôsob fakturácie času a materiálu, spôsobí vytvorenie riadku na faktúre dodávateľa. Každý riadok v subdodávke, ktorý má spôsob fakturácie s pevnou cenou, spôsobí vytvorenie riadka na faktúre dodávateľa pre každý míľnik v riadku subdodávky, ktorý má stav **Pripravené na fakturáciu**.

Nasledujúce polia a súvisiace záznamy sa skopírujú zo subdodávky do hlavičky faktúry dodávateľa:

- Predajca.
- Súvisiace cenníky budú skopírované na faktúru dodávateľa ako cenníky.
- Mena.
- Zmluvná jednotka.
- Platobné podmienky.

Pre riadky subdodávok Čas a materiál budú nasledujúce polia a súvisiace záznamy skopírované z riadku subdodávok do riadku faktúry dodávateľa:

- Referencie subdodávok a subdodávateľských liniek
- Trieda transakcie
- Rola
- Kategória transakcie
- Polia produktov
- Project
- Úloha
- Rezervovateľný zdroj

Pre riadky subdodávok s pevnou cenou sa skopírujú nasledujúce polia z riadku subdodávok a míľnika riadku subdodávok do riadku faktúry dodávateľa:

- Referencie subdodávok a subdodávateľských liniek.
- Transakčná trieda. V predvolenom nastavení bude hodnota **Míľnik**.
- Názov a čiastka míľnika sa skopírujú zo súvisiaceho míľnika subdodávky.
- Používateľ si bude môcť vybrať projekt a úlohu v riadku faktúry dodávateľa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
