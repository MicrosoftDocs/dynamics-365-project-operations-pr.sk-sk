---
title: Konfigurácia neskladovaných materiálov a čakajúcich faktúr dodávateľov
description: Táto téma vysvetľuje, ako povoliť neskladované materiály a čakajúce faktúry dodávateľa.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9b55d959228062fc3577cf7f12d8926f51e9791f98c73fdc4b78251312a8a77a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003250"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Konfigurácia neskladovaných materiálov a čakajúcich faktúr dodávateľov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

## <a name="minimum-version-requirement"></a>Minimálna požadovaná verzia:

Používanie neskladovaných materiálov a čakajúcich faktúr dodávateľa pre scenáre Dynamics 365 Project Operations, založené na zdrojoch/sklade, si vyžadujú nasledujúce verzie:

Riešenia Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 alebo vyššia
- Riešenie orchestrácie aplikácií s duálnym zápisom – 2.2.2.23 alebo vyššie

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) alebo vyššia. Uistite sa, že je vaše prostredie Finance aktuálne a všetky aktualizácie kvality sú použité tak, aby vyhovovali minimálnym požiadavkám na verziu.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Spustite mapy duálneho zápisu pre skladové materiály a integráciu faktúr dodávateľa

Táto časť poskytuje informácie o konkrétnych mapách požadovaných pre neskladované materiály a faktúry dodávateľov. Overte, či sú nevyhnutné mapy uvedené v téme [Zriadenie nového prostredia](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) spustené vo vašom prostredí.

1. Prejdite na stránku Lifecycle Services (LCS), prejdite na svoj projekt LCS a prejdite na stránku **Podrobnosti o prostredí**.
2. V časti **Informácie o prostredí Common Data Service** stlačte možnosť **Odkaz na CDS for Apps**. Po výbere odkazu budete presmerovaní na zoznam entít v mapovaní.
3. Skontrolujte, či sú spustené nasledujúce mapy. Ak nie sú spustené, spustite ich a nezabudnite zahrnúť všetky súvisiace mapové tabuľky.

    - Spoločnosť CDS vydala odlišné produkty (produkty)
    - Vendors v2 (msdyn_vendors)
    - Tabuľka Project Operations pre materiálové odhady (msdyn_estimatelines)
    - Entita exportu faktúr dodávateľa integrácie Project Operations (msdyn_projectvendorinvoices)
    - Riadok entity exportu faktúr projektu dodávateľa projektu Project Operations (msdyn_projectvendorinvoicelines)
    - Skutočné hodnoty integrácie Project Operations (msdyn_actuals). Uistite sa, že používate verziu mapy 1.0.0.14 alebo vyššiu. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy môžete aktivovať výberom možnosti **Verzia mapy tabuľky** a potom uložiť vybranú verziu.

Ak používate štandardné ukážkové údaje, možno budete musieť zastaviť a reštartovať nasledujúce mapy entít s počiatočnou synchronizáciou:
  - Platobné dni CDS V2 (msdyn_paymentdays)
  - Časový plán platieb (msdyn_paymentschedules)
  - Platobné podmienky (msdyn_paymentterms)
  - Skupiny dodávateľov (msdyn_vendorgroups)
  - Jednotky (uom)

> [!NOTE]
> Počiatočná synchronizácia pre skupiny a jednotky dodávateľov môže pre niekoľko záznamov v existujúcej ukážkovej množine údajov zlyhať. Zlyhania môžete ignorovať, pretože vám nezabránia používať ukážkové údaje v Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Konfigurácia predpokladov v Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Aktivujte pracovný postup a vytvorte účty založené na entite dodávateľa

Poskytuje riešenie orchestrácie duálneho zápisu [Dodávatelia zvládajú integráciu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Ako nevyhnutná podmienka pre túto funkciu musia byť údaje dodávateľa vytvorené v entite **Účty**. Aktivujte proces pracovného postupu so šablónami a vytvorte tak dodávateľov v tabuľke **Účty**, ako je opísané v časti [Prepínajte medzi návrhmi dodávateľov](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Nastaviť produkty tak, aby boli aktívne

Neskladované materiály musia byť nakonfigurované ako **Vydané výrobky** v nástroji Finance. Riešenie orchestrácia duálneho zápisu poskytuje riešenie pripravené na použitie [Integrácia vydaných produktov do katalógu výrobkov Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). V predvolenom nastavení sú produkty z Finance synchronizované do Dataverse v stave návrhu. Ak chcete produkt synchronizovať do aktívneho stavu, aby ho bolo možné priamo použiť v dokumentoch o použití materiálu alebo čakajúcich faktúrach dodávateľa, prejdite na **Systém** > **Správa** > **Správa systému** > **Systémové nastavenia** a na karte **Predaj** nastavte **Vytváranie produktov v aktívnom stave** na **Áno**.

## <a name="configure-prerequisites-in-finance"></a>Konfigurácia predpokladov v nástroji Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Povoľte kľúč funkcie pre čakajúce faktúry dodávateľa

Dokončením nasledujúcich krokov povoľte funkčnosť pridávania podrobností projektu do riadkov faktúr čakajúcich na dodávateľa.

1. V nástroji Finance prejdite na pracovný priestor **Správa funkcie**.
2. V zozname funkcií nájdite funkciu **Povoliť faktúry dodávateľa v Project Operations pre scenáre založené na zdrojoch/na sklade** a stlačte možnosť **Povoliť**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definujte skupiny kategórií a kategórie projektov pre položky

Nakonfigurujte pre skupinu aspoň jednu skupinu kategórií typu transakcie **Položka** a najmenej jedna kategória projektu využívajúca túto skupinu. Viac informácií nájdete v časti [Konfigurácia projektových kategórií](../project-accounting/configure-project-categories.md#category-groups).

Skontrolujte profily nákladov a výnosov projektu a nakonfigurujte nastavenie účtovania hlavnej knihy pre transakcie položiek. Viac informácií nájdete v časti [Konfigurácia účtovníctva pre fakturovateľné projekty](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Natavenie produktu zápisu

V časti Project Operations môžete zaznamenávať odhady materiálu a použitie pre katalógové produkty, ktoré sú nakonfigurované vo vydanom katalógu produktov, a pre produkty určené na zápis. Používanie produktov na zapisovanie vyžaduje jeden vydaný produkt, ktorý je na tento účel nakonfigurovaný v aplikácii Finance. Vykonajte nasledujúce kroky na konfiguráciu produktu určeného na zápis. Zopakujte tieto kroky pre každú právnickú entitu, ktorá používa Project Operations pre scenáre zdrojov a akcií, ktoré nie sú na sklade.

1. V nástroji Finance choďte na **Správa informácií o produkte** > **Produkty** > **Vydané výrobky** a vyberte **Nový**.
2. V poli **Typ produktu** stlačte možnosť **Položka** a v poli **Podtyp produktu** stlačte možnosť **Výrobok**.
3. Zadajte číslo produktu (WRITEIN) a názov produktu (produkt určený na zápis).
4. Vyberte skupinu modelu položky. Uistite sa, že vybratá skupina modelov položiek má pole **Zásady inventára pre skladový produkt** nastavené na **False**.
5. Vyberte hodnoty v poliach **Skupina položiek**, **Skupina dimenzií úložiska** a **Skupina dimenzií sledovania**. Použite **Rozmery skladu** len pre **Lokality** a v poli **Rozmery sledovania** stlačte možnosť **Žiadne**.
6. Vyberte hodnoty v poli **Inventarizačná jednotka**, **Nákupná jednotka** a **Jednotka predaja** a potom uložte zmeny.
7. Na karte **Plán** nastavte predvolené nastavenie poradia a na karte **Inventarizácia** môžete nastaviť predvolenú lokalitu a sklad.
8. Prejdite na **Projektové riadenie a účtovníctvo** > **Nastavenie** > **Parametre projektového riadenia a účtovníctva** a otvorte **Project Operations v Dynamics 365 Dataverse**. 
9. Na karte **Materiály** v poli **Produkt na zápis** vyberte produkt, ktorý ste vytvorili.
10. Vo vašom prostredí Dataverse na mape lokality otvorte entitu **Produkty** a vyhľadajte záznam produktu na zapísanie. 
11. Otvorte podrobnosti záznamu a nastavte stav produktu na **Vyradené**. Tento stav produktu bráni komukoľvek v náhodnom použití tohto záznamu priamo v odhadoch materiálu a dokumentoch o použití.

### <a name="set-up-a-procurement-integration-account"></a>Založte si účet integrácie obstarávania

Účet integrácie obstarávania sa používa ako zúčtovací účet pri účtovaní čakajúcej faktúry dodávateľa s riadkami priradenými k projektu.

Keď systém zaúčtuje čakajúcu faktúru dodávateľa, tento účet sa použije na sumu nákladov na projekt. Fakturačné údaje dodávateľa sú spracované v Dataverse a vytvorí sa zodpovedajúci skutočný projekt. Informácie zo skutočného projektu sa pridajú do denníka integrácie Project Operations. Keď zaúčtujete denník integrácie, suma sa vymaže z účtu integrácie obstarávania a zaznamená sa do nákladov na projekt.

1. Na nastavenie účtu integrácie obstarávania prejdite na **Projektové riadenie a účtovníctvo** > **Nastavenie** > **Parametre projektového riadenia a účtovníctva** a otvorte **Project Operations v Dynamics 365 Dataverse**. 
2. Prejdite na kartu **Materiály** a vyberte hodnotu v poli **Účet integrácie obstarávania**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Nastaviť predvolené hodnoty kategórie projektu pre položku

1. V nástroji Finance prejdite na **Projektové riadenie a účtovníctvo** > **Nastavenie** > **Parametre projektového riadenia a účtovníctva** a otvorte **Project Operations v Dynamics 365 Dataverse**. 
2. Na karte **Predvolené hodnoty kategórie projektu** vyberte hodnotu v poli **Položka**. Táto kategória projektu sa používa pre významné transakcie, ak kategória projektu nebola nastavená v zázname skutočností projektu.
