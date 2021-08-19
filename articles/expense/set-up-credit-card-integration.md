---
title: Nastavenie integrácie kreditnej karty
description: Táto téma vysvetľuje, ako pracovať s transakciami kreditnej karty spojenými s výdavkami.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51c364dff41d856e493581e1b87fd29571f641c70e7233bdebb910efbc64b983
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996230"
---
# <a name="set-up-credit-card-integration"></a>Nastavenie integrácie kreditnej karty

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Transakcie s kreditnými kartami súvisiace s výdavkami je možné nastaviť tak, aby sa automaticky importovali podľa opakujúceho sa harmonogramu. Alternatívne je možné transakcie importovať manuálne podľa potreby. Transakcie kreditnou kartou sa importujú prostredníctvom dátovej entity transakcie kreditnou kartou.

## <a name="import-credit-card-transactions"></a>Import transakcií kreditnou kartou

Pri importovaní transakcií kreditnou kartou postupujte takto:

1. Na stránke **Transakcie kreditnou kartou** vyberte **Importovať transakcie**. Ak správu údajov otvárate prvýkrát, systém musí najskôr aktualizovať zoznam dátových entít.
2. V poli **Názov** zadajte jedinečný popis úlohy importu.
3. V poli **Formát zdrojových údajov** vyberte formát súboru, ktorý obsahuje transakcie kreditnej karty na import.
4. Vyberte **Nahrať** a potom vyhľadajte a vyberte súbor, ktorý chcete importovať.
5. Po nahraní súboru overte mapovanie súboru transakcií kreditnou kartou a stĺpcov dátovej entity transakcií kreditnou kartou výberom prepojenia **Zobraziť mapu** na dlaždici. Ak sa vyskytujú chyby spárovania, alebo ak musíte zmeniť spárovanie, vykonajte zmeny spárovania buď z karty **Vizualizácia spárovania** alebo karty **Podrobnosti spárovania**.
6. Ak chcete automatizovať transakcie kreditnou kartou, vyberte **Vytvoriť opakujúcu sa dátovú úlohu**. Potom môžete nastaviť opakovanie, ktoré definuje, ako často sa majú transakcie kreditnou kartou importovať. Po dokončení vyberte **OK**.
7. Ak chcete vybratý súbor importovať teraz, vyberte **Import**.
8. Ak sa počas importu vyskytnú chyby, môžete si prezrieť protokol vykonávania alebo údaje o postupe, aby ste videli chyby, ktoré musíte opraviť, aby ste zabezpečili úspešný import.

> [!NOTE]
> Ak potrebujete importovať viac ako jeden formát súboru, musíte vytvoriť samostatné úlohy importu pre každý typ formátu.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Zmena priradenia transakcií kreditnou kartou pre ukončených zamestnancov

Po ukončení záznamu zamestnanca je účet zamestnanca služby Active Directory Domain Services (AD DS) deaktivovaný. Môžu však existovať aktívne transakcie s kreditnými kartami, ktoré sa musia stále zaúčtovať a uhradiť. Na stránke **Transakcie kreditnou kartou** môžete zamestnanca znova priradiť k akejkoľvek transakcii kreditnou kartou, kde bol priradený zamestnanec prepustený.

Vyberte jednu alebo viac transakcií kreditnou kartou a potom vyberte **Opätovné pridelenie transakcií**. Potom môžete vybrať iného zamestnanca, ktorému chcete priradiť transakcie kreditnou kartou. Po opätovnom priradení transakcií kreditnou kartou ich možno vybrať pre výkaz výdavkov a zaplatiť obvyklým spôsobom na úhradu výkazu výdavkov.

## <a name="delete-credit-card-transactions"></a>Odstránenie transakcií kreditnou kartou 

Niekedy po importovaní transakcií kreditnou kartou môže byť potrebné niektoré transakcie vymazať. Môže to byť preto, že transakcie sú duplikáty, alebo preto, že údaje nemusia byť presné. Správcovia môžu používať funkciu **„Odstrániť transakcie kreditnou kartou“** na výber a odstránenie transakcií kreditnou kartou, ktoré **nie sú pripojené** k výkazu výdavkov. 

1. Prejdite na **Periodické úlohy** > **Odstránenie transakcií kreditnou kartou**.
2. Vyberte **Filtrovať** a poskytnite informácie na identifikáciu záznamov, ktoré sa majú zahrnúť.
3. Stlačením možnosti **OK** vymažte záznamy. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
