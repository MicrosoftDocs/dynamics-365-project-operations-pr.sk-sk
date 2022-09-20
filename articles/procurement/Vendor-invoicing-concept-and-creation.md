---
title: Vytvárajte faktúry dodávateľa
description: Tento článok popisuje koncepciu dodávateľských faktúr a vysvetľuje, ako ich vytvoriť v Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475484"
---
# <a name="create-vendor-invoices"></a>Vytvárajte faktúry dodávateľa

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Ak chcete používať funkcie popísané v tomto článku, musíte povoliť **Povoľte spracovanie skutočného stavu subdodávok pomocou projektových operácií pre scenáre založené na zdrojoch** funkcia v **Správa funkcií** pracovnom priestore.

Fakturácia dodávateľa v spoločnosti Microsoft Dynamics 365 Project Operations môžu byť použité na evidenciu nákladov z dodávok služieb a/alebo materiálov na projekte, ktorý je dokončený dodávateľmi.

Keď sú služby a/alebo materiály zadané dodávateľovi ako subdodávka, subdodávka predstavuje zmluvnú dohodu s týmto dodávateľom. Keď dodávateľ dodáva služby alebo keď sa materiály prijímajú a používajú na projektové úlohy, náklady sa zaznamenávajú do projektu. Dodávateľ potom pravidelne posiela faktúry. Tieto faktúry sú overené a spárované s nákladmi, ktoré sú zaznamenané v projekte. Po dokončení procesu overovania je faktúra dodávateľa potvrdená a uvoľnená na platbu.

## <a name="scenarios-for-use"></a>Scenáre na použitie

Faktúry dodávateľa v projektových operáciách možno použiť na podporu dvoch odlišných scenárov:

- Zákazníci využívajú všetky možnosti subdodávok.
- Zákazníci nevyužívajú úplné skúsenosti so subdodávateľmi, ale chcú mať jednotný pohľad na náklady na projekty v rámci projektových operácií.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Zákazníci využívajú všetky možnosti subdodávok

Skúsenosti s faktúrami dodávateľa poskytujú spôsob, ako overiť záznamy času, spotreby materiálu a nákladových záznamov, ktoré odkazujú na subdodávateľské komponenty, a priradiť ich k riadkom faktúry dodávateľa. Tento proces možno použiť na overenie presnosti riadkov faktúry dodávateľa. Po dokončení procesu overovania a potvrdení faktúry dodávateľa systém stornuje skutočnosti, ktoré boli zaznamenané v schválených protokoloch času, nákladov a použitia materiálu, a potom vytvorí nové skutočné náklady pomocou riadkov faktúry dodávateľa.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Zákazníci nevyužívajú úplné skúsenosti so subdodávateľmi, ale chcú mať jednotný pohľad na náklady na projekty v projektových operáciách

Ak sledujete proces subdodávok v systéme tretej strany, môžete zaznamenať náklady z tohto systému tretej strany do projektových operácií vytvorením faktúr dodávateľa, ktoré neodkazujú na subdodávky. Vaši projektoví manažéri tak môžu mať jednotný pohľad na všetky náklady na daný projekt.

## <a name="create-vendor-invoices-in-project-operations"></a>Vytvorte faktúry dodávateľa v Project Operations

Faktúry dodávateľa sa vytvárajú v Dynamics 365 Finance pomocou **Splatné účty** modul. Faktúry dodávateľa nemôžete vytvárať priamo v Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Nastavte overenie faktúry dodávateľa

Ak je faktúra dodávateľa určená na subdodávku v Dataverse, musíte povoliť **Vyžaduje sa manuálne overenie PM** parameter. Nastavenie voľby určuje, či sa má faktúra dodávateľa automaticky potvrdiť v Dataverse alebo či vyžaduje manuálne potvrdenie. Hlavička každej faktúry dodávateľa projektu obsahuje možnosť s rovnakým názvom. Štandardne je možnosť v hlavičke všetkých faktúr dodávateľa projektu nastavená na hodnotu, ktorú ste tu nastavili. Hodnotu však môžete podľa potreby aktualizovať v hlavičke jednotlivých faktúr dodávateľa.

Ak je možnosť nastavená na **Áno**, faktúra dodávateľa, ktorá je vytvorená v Financie a synchronizovaná s Dataverse má **Návrh** postavenie. Faktúra musí byť následne overená a overená projektovým manažérom a potvrdená pred jej spracovaním a zaúčtovaním na konkrétne projektové a účtovné účty vo financiách.

Ak je možnosť nastavená na **Nie**, faktúra dodávateľa sa automaticky potvrdí. Nevyžadujú sa žiadne ďalšie kroky.

Ak chcete nastaviť overenie faktúry dodávateľa, postupujte podľa týchto krokov.

1. V časti Financie prejdite na **Projektový manažment a účtovníctvo** \> **Nastaviť** \> **Projektový manažment a účtovné parametre**.
1. Na **Finančné** kartu, nastavte **Vyžaduje sa manuálne overenie PM** možnosť **Áno** ak firemná politika vyžaduje overenie faktúr subdodávateľov. Ak sa nevyžaduje overenie projektovým manažérom v Dataverse, ponechajte množina možností na **Nie**. Štandardne sa nastavenie použije na **Čakajúca faktúra dodávateľa** stránku.

> [!NOTE]
> Faktúry dodávateľa, ktoré sú vytvorené pre subdodávky v Dataverse možno správne spracovať iba vtedy, ak **Vyžaduje sa manuálne overenie PM** možnosť je nastavená na **Áno**. Skutočné náklady na čas, materiál a náklady, ktoré vytvoria subdodávatelia, môže projektový manažér manuálne priradiť k riadkom faktúry dodávateľa, iba ak je táto možnosť nastavená na **Áno**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Nastavte účet integrácie obstarávania pre faktúry dodávateľa

Keď sa faktúra dodávateľa zaúčtuje v časti Financie pre projektové operácie – integrované prostredie (nie na sklade), finančné údaje sa zaúčtujú na účet integrácie obstarávania. Systém generuje aktuálne informácie v Dataverse za zaúčtovanú faktúru. Tieto skutočnosti sa zaúčtujú do Financie pomocou denníka integrácie projektu. Účtovanie denníka integrácie projektu zaúčtuje skutočné náklady a stornuje účet integrácie obstarávania.

Ak chcete nastaviť účet integrácie obstarávania pre faktúry dodávateľa, postupujte podľa týchto krokov.

1. V časti Financie prejdite na **Projektový manažment a účtovníctvo** \> **Nastaviť** \> **Projektový manažment a účtovné parametre**.
1. Na **Operácie projektu pri zapájaní zákazníkov Dynamics 365** kartu, vyberte **Materiály** \> **Účet integrácie obstarávania**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Vytvárajte a odosielajte faktúry dodávateľa subdodávateľov

Keď účtovník dostane faktúru od subdodávateľa, v Financie sa vytvorí nová faktúra.

1. V časti Financie prejdite na **Záväzky** \> **faktúry** \> **Čakajúce faktúry dodávateľa**.
1. Na **Panel akcií**, vyberte **Nový** na vytvorenie faktúry dodávateľa.
1. V hlavičke faktúry v **Fakturačný účet** pole, vyberte **Subdodávateľ**.
1. Vyberte dátum faktúry.
1. Na **Hlavička** kartu, nastavte **Vyžaduje sa manuálne overenie PM** možnosť **Áno**. Predvolené nastavenie tejto možnosti pochádza z **Projektový manažment a účtovné parametre** stránku. Dá sa však zmeniť na úrovni faktúry dodávateľa.
1. Na **Fakturačný riadok** FastTab, vyberte **Pridať riadok** na vytvorenie riadku faktúry dodávateľa.
1. Vyberte kategóriu obstarávania, ktorá bola vytvorená pre riadky subdodávok, a zadajte jednotkovú cenu, mernú jednotku a množstvo.
1. V časti Riadky faktúr dodávateľa na **Projekt** vyberte projekt, s ktorým subdodávateľ zdieľa faktúru za subdodávateľ.
1. Vyberte kategóriu projektu. Môže byť akéhokoľvek typu **Položka**, **·**, **·**, alebo **hodiny**.
1. Rolu vyberte iba vtedy, ak je vybratá kategória projektu **hodina** typu.
1. Vyberte **Príspevok** zaúčtovať faktúru dodávateľa.

Prípadne môžete vytvoriť faktúru dodávateľa tak, že prejdete na **Splatné účty** \> **faktúry** \> **Otvoriť faktúry dodávateľa** a výber **Nový**.

Keď je faktúra dodávateľa zaúčtovaná, bude dostupná v Dataverse na overenie a spracovanie projektovým manažérom.

## <a name="vendor-invoice-processing-in-dataverse"></a>Spracovanie faktúry dodávateľa v Dataverse

Vo faktúre dodávateľa, ktorá je vytvorená v Dataverse, niektoré hodnoty polí pochádzajú z faktúry dodávateľa, ktorá je zaznamenaná vo financiách. Ostatné hodnoty sú predvolené hodnoty, ktoré pochádzajú zo subdodávky.

Nasledujúce polia a súvisiace záznamy sa skopírujú zo subdodávky do hlavičky faktúry dodávateľa:

- Mena
- Zmluvná jednotka
- Platobné podmienky

V riadkoch faktúry dodávateľa používa Project Operations nasledujúce hodnoty polí na zadanie predvolenej subdodávky a odkazu na riadok subdodávky:

- Trieda transakcie
- Rola
- Kategória transakcie
- Polia produktov
- Project
- Úloha

> [!NOTE]
> Riadky subdodávok s pevnou cenou nie sú podporované v prevádzke projektu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
