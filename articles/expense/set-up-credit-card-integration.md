---
title: Nastavenie integrácie kreditnej karty
description: Táto téma vysvetľuje, ako importovať a udržiavať transakcie kreditnými kartami súvisiace s výdavkami.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120877"
---
# <a name="set-up-credit-card-integration"></a>Nastavenie integrácie kreditnej karty

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Transakcie s kreditnými kartami súvisiace s výdavkami je možné nastaviť tak, aby sa automaticky importovali podľa opakujúceho sa harmonogramu. Alternatívne je možné transakcie importovať manuálne podľa potreby. Transakcie kreditnými kartami sa importujú prostredníctvom dátovej entity Transakcie kreditnou kartou.

## <a name="import-credit-card-transactions"></a>Import transakcií kreditnou kartou

1. Na stránke **Transakcie kreditnou kartou** vyberte **Importovať transakcie**. Ak správu údajov otvárate prvýkrát, systém musí najskôr aktualizovať zoznam dátových entít.
2. Do poľa **Názov** zadajte jedinečný popis úlohy importu.
3. V poli **Formát zdrojových údajov** vyberte formát súboru, ktorý obsahuje transakcie kreditnej karty na import.
4. Vyberte **Nahrať** a potom vyhľadajte a vyberte súbor, ktorý chcete importovať.
5. Po nahraní súboru overte spárovanie súboru transakcií s kreditnými kartami a stĺpcov dátovej entity Transakcie s kreditnými kartami výberom prepojenia **Zobraziť mapu** na dlaždici. Ak sa vyskytujú chyby spárovania, alebo ak musíte zmeniť spárovanie, vykonajte zmeny spárovania buď z karty **Vizualizácia spárovania** alebo karty **Podrobnosti spárovania**.
6. Ak chcete automatizovať transakcie kreditnou kartou, vyberte **Vytvoriť opakujúcu sa dátovú úlohu**. Potom môžete nastaviť opakovanie, ktoré definuje, ako často sa majú transakcie kreditnou kartou importovať. Po dokončení vyberte **OK**.
7. Ak chcete vybratý súbor importovať teraz, vyberte **Import**.
8. Ak sa počas importu vyskytnú chyby, môžete si prezrieť protokol vykonávania alebo údaje o postupe, aby ste videli chyby, ktoré musíte opraviť, aby ste zaručili úspešný import.

> [!NOTE]
> Ak musíte importovať viac ako jeden formát súboru, musíte vytvoriť samostatné úlohy importu pre každý typ formátu.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Zmena priradenia transakcií kreditnou kartou pre ukončených zamestnancov

Po ukončení záznamu zamestnanca je účet zamestnanca služby Active Directory Domain Services (AD DS) deaktivovaný. Môžu však existovať aktívne transakcie s kreditnými kartami, ktoré sa musia stále zaúčtovať a uhradiť. Zo stránky **Transakcie kreditnou kartou** môžete zamestnanca znova priradiť k akejkoľvek transakcii kreditnou kartou, kde bol ukončený pridružený zamestnanec.

Vyberte jednu alebo viac transakcií kreditnou kartou a potom vyberte **Opätovné pridelenie transakcií**. Potom môžete vybrať iného zamestnanca, ktorému chcete priradiť transakcie kreditnou kartou. Po opätovnom priradení transakcií kreditnou kartou ich možno vybrať pre výkaz výdavkov a zaplatiť obvyklým spôsobom na úhradu výkazu výdavkov.


[!INCLUDE[footer-include](../includes/footer-banner.md)]