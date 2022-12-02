---
title: Vytvorenie faktúr dodávateľov
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
# <a name="create-vendor-invoices"></a>Vytvorenie faktúr dodávateľov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Ak chcete používať funkcie popísané v tomto článku, musíte povoliť funkciu **Povoliť spracovanie skutočných hodnôt subdodávok pomocou Project Operations pre scenáre založené na zdrojoch** v pracovnom priestore **Správa funkcií**.

Fakturácia dodávateľov v Microsoft Dynamics 365 Project Operations môže byť použitá na evidenciu nákladov z dodávok služieb a/alebo materiálov na projekte, ktoré sú dokončené dodávateľmi.

Keď sú služby a/alebo materiály zadané dodávateľovi ako subdodávka, subdodávka predstavuje zmluvnú dohodu s týmto dodávateľom. Keď dodávateľ dodáva služby alebo keď sa materiály prijímajú a používajú na projektové úlohy, náklady sa zaznamenávajú do projektu. Dodávateľ potom pravidelne posiela faktúry. Tieto faktúry sú overené a spárované s nákladmi, ktoré sú zaznamenané v projekte. Po dokončení procesu overovania je faktúra dodávateľa potvrdená a uvoľnená na platbu.

## <a name="scenarios-for-use"></a>Scenáre použitia

Faktúry dodávateľa v Project Operations možno použiť na podporu dvoch odlišných scenárov:

- Zákazníci využívajú všetky možnosti subdodávok.
- Zákazníci nevyužívajú všetky možnosti subdodávok, ale chcú mať jednotný pohľad na náklady na projekty v rámci Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Zákazníci využívajú všetky možnosti subdodávok

Možnosti faktúr dodávateľa poskytujú spôsob, ako overiť záznamy času, spotreby materiálu a nákladov, ktoré odkazujú na subdodávateľské komponenty, a priradiť ich k riadkom faktúry dodávateľa. Tento proces možno použiť na overenie presnosti riadkov faktúry dodávateľa. Po dokončení procesu overovania a potvrdení faktúry dodávateľa systém stornuje skutočné údaje, ktoré boli zaznamenané v schválených protokoloch času, nákladov a použitia materiálu, a potom vytvorí nové skutočné náklady pomocou riadkov faktúry dodávateľa.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Zákazníci nevyužívajú všetky možnosti subdodávok, ale chcú mať jednotný pohľad na náklady na projekty v rámci Project Operations

Ak sledujete proces subdodávateľských zmlúv v systéme tretej strany, môžete zaznamenať náklady z tohto systému tretej strany do Project Operations vytvorením faktúr dodávateľa, ktoré neodkazujú na subdodávateľské zmluvy. Vaši projektoví manažéri tak môžu mať jednotný pohľad na všetky náklady na daný projekt.

## <a name="create-vendor-invoices-in-project-operations"></a>Vytvorenie faktúr dodávateľa v Project Operations

Faktúry dodávateľa sa vytvárajú v Dynamics 365 Finance pomocou modulu **Záväzky**. Nemôžete vytvárať faktúry dodávateľa priamo v Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Nastavenie overenia faktúry dodávateľa

Ak je faktúra dodávateľa určená na subdodávku v Dataverse, musíte povoliť parameter **Vyžaduje sa manuálne overenie zo strany PM**. Nastavenie voľby určuje, či sa má faktúra dodávateľa automaticky potvrdiť v Dataverse alebo či vyžaduje manuálne potvrdenie. Hlavička každej faktúry dodávateľa projektu obsahuje možnosť s rovnakým názvom. Štandardne je možnosť v hlavičke všetkých faktúr dodávateľa projektu nastavená na hodnotu, ktorú ste tu nastavili. Hodnotu však môžete podľa potreby aktualizovať v hlavičke jednotlivých faktúr dodávateľa.

Ak je možnosť nastavená na **Áno**, faktúra dodávateľa, ktorá je vytvorená vo Finance a synchronizovaná s Dataverse má stav **Koncept**. Faktúra musí byť následne skontrolovaná a overená projektovým manažérom a potvrdená pred jej spracovaním a zaúčtovaním na konkrétne projektové a účtovné účty vo Finance.

Ak je možnosť nastavená na **Nie**, faktúra dodávateľa sa automaticky potvrdí. Nevyžadujú sa žiadne ďalšie akcie.

Ak chcete nastaviť overovanie faktúr dodávateľov, postupujte podľa týchto krokov.

1. Vo Finance prejdite na **Projektové riadenie a účtovníctvo** \> **Nastaviť** \> **Parametre projektového riadenia a účtovníctva**.
1. Na karte **Finančné** nastavte možnosť **Vyžaduje sa manuálne overenie zo strany PM** na **Áno**, ak firemná politika vyžaduje overenie faktúr subdodávateľov. Ak sa nevyžaduje overenie projektovým manažérom v Dataverse, ponechajte možnosť nastavenú na **Nie** Štandardne sa nastavenie použije na stránku **Čakajúca faktúra dodávateľa**.

> [!NOTE]
> Faktúry dodávateľa, ktoré sú vytvorené pre subdodávky v Dataverse, možno správne spracovať iba vtedy, ak je možnosť **Vyžaduje sa manuálne overenie zo strany PM** nastavená na **Áno**. Skutočné náklady na čas, materiál a výdavky, ktoré vytvoria subdodávatelia, môže projektový manažér manuálne priradiť k riadkom faktúry dodávateľa, iba ak je táto možnosť nastavená na **Áno**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Založenie účtu integrácie obstarávania pre faktúry dodávateľov

Keď sa faktúra dodávateľa zaúčtuje vo Finance pre Project Operations – integrované prostredie (nie na sklade), finančné údaje sa zaúčtujú na účet integrácie obstarávania. Systém generuje skutočné hodnoty v Dataverse za zaúčtovanú faktúru. Tieto skutočné hodnoty sa zaúčtujú do Finance pomocou denníka integrácie projektu. Zaúčtovaním do denníka integrácie projektu sa zaúčtujú skutočné náklady a zruší sa účet integrácie obstarávania.

Ak chcete vytvoriť účet integrácie obstarávania pre faktúry dodávateľov, postupujte podľa týchto krokov.

1. Vo Finance prejdite na **Projektové riadenie a účtovníctvo** \> **Nastaviť** \> **Parametre projektového riadenia a účtovníctva**.
1. Na karte **Project operations v Dynamics 365 customer engagement** vyberte **Materiály** \> **Účet integrácie obstarávania**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Vytváranie a účtovanie faktúr subdodávateľov

Keď účtovník záväzkov dostane faktúru od subdodávateľa, vo Finance sa vytvorí nová faktúra.

1. Vo Finance prejdite na **Záväzky** \> **Faktúry** \> **Čakajúce faktúry dodávateľa**.
1. Na **table akcií** vyberte **Nový** na vytvorenie faktúry dodávateľa.
1. Na hlavičke faktúry v poli **Účet faktúry** vyberte **Subdodávateľ**.
1. Vyberte dátum faktúry.
1. Na karte **Hlavička** nastavte **Vyžaduje sa manuálne overenie zo strany PM** na **Áno**. Predvolené nastavenie tejto možnosti pochádza zo stránky **Parametre projektového riadenia a účtovníctva**. Dá sa však zmeniť na úrovni faktúry dodávateľa.
1. Na karte FastTab **Riadok faktúry** vyberte **Pridať riadok** na vytvorenie riadku faktúry dodávateľa.
1. Vyberte kategóriu obstarávania, ktorá bola vytvorená pre riadky subdodávok, a zadajte jednotkovú cenu, mernú jednotku a množstvo.
1. V časti Riadky faktúry dodávateľa na karte **Projekt** vyberte projekt, s ktorým subdodávateľ zdieľa faktúru subdodávateľa.
1. Vyberte kategóriu projektu. Môže byť akéhokoľvek typu – **Položka**, **Výdavok**, **Materiály** alebo **Hodiny**.
1. Rolu vyberte iba vtedy, ak je vybratá kategória projektu typu **Hodina**.
1. Vyberte **Zaúčtovať** na zaúčtovanie dodávateľskej faktúry.

Prípadne môžete vytvoriť dodávateľskú faktúru tak, že prejdete na **Záväzky** \> **Faktúry** \> **Otvoriť faktúry dodávateľa** a vyberiete možnosť **Nový**.

Keď je faktúra dodávateľa zaúčtovaná, bude dostupná v Dataverse na overenie a spracovanie projektovým manažérom.

## <a name="vendor-invoice-processing-in-dataverse"></a>Spracovanie faktúr dodávateľa v Dataverse

Vo faktúre dodávateľa, ktorá je vytvorená v Dataverse, niektoré hodnoty polí pochádzajú z faktúry dodávateľa, ktorá je zaznamenaná vo Finance. Ostatné hodnoty sú predvolené hodnoty, ktoré pochádzajú zo subdodávky.

Nasledujúce polia a súvisiace záznamy sa skopírujú zo subdodávateľskej zmluvy do hlavičky faktúry dodávateľa:

- Mena
- Zmluvná jednotka
- Platobné podmienky

V riadkoch faktúry dodávateľa používa Project Operations nasledujúce hodnoty polí na zadanie predvolenej subdodávky a odkazu na riadok subdodávateľskej zmluvy:

- Trieda transakcie
- Rola
- Kategória transakcie
- Polia produktu
- Project
- Úloha

> [!NOTE]
> Riadky subdodávateľskej zmluvy s pevnou cenou nie sú podporované v Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
