---
title: Nastavenie integrácie kreditnej karty
description: Tento článok vysvetľuje, ako pracovať s transakciami kreditnými kartami súvisiacimi s výdavkami.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4d32754548af67bdd5b9f7345f6363bd6193b36d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924514"
---
# <a name="set-up-credit-card-integration"></a>Nastavenie integrácie kreditnej karty

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Transakcie s kreditnými kartami súvisiace s výdavkami je možné nastaviť tak, aby sa automaticky importovali podľa opakujúceho sa harmonogramu. Alternatívne je možné transakcie importovať manuálne podľa potreby. Transakcie kreditnou kartou sa importujú prostredníctvom dátovej entity transakcie kreditnou kartou.

## <a name="import-credit-card-transactions"></a>Import transakcií kreditnou kartou

Pri importovaní transakcií kreditnou kartou postupujte takto:

1. Na stránke **Transakcie kreditnou kartou** vyberte **Importovať transakcie**. Ak otvárate správu údajov prvýkrát, systém musí aktualizovať zoznam entít údajov, aby ste mohli pokračovať.
2. V poli **Názov** zadajte jedinečný popis úlohy importu.
3. V poli **Formát zdrojových údajov** vyberte formát súboru, ktorý obsahuje transakcie kreditnej karty na import.
4. Vyberte **Nahrať** a potom vyhľadajte a vyberte súbor, ktorý chcete importovať.
5. Po nahraní súboru overte mapovanie súboru transakcií kreditnou kartou a stĺpcov dátovej entity transakcií kreditnou kartou výberom prepojenia **Zobraziť mapu** na dlaždici. Ak sa vyskytujú chyby spárovania, alebo ak musíte zmeniť spárovanie, vykonajte zmeny spárovania buď z karty **Vizualizácia spárovania** alebo karty **Podrobnosti spárovania**.
6. Ak chcete automatizovať transakcie kreditnou kartou, vyberte **Vytvoriť opakujúcu sa dátovú úlohu**. Potom môžete nastaviť opakovanie, ktoré definuje, ako často sa majú transakcie kreditnou kartou importovať. Po dokončení vyberte **OK**
7. Ak chcete vybratý súbor importovať teraz, vyberte **Import**.
8. Ak sa počas importu vyskytnú chyby, môžete si prezrieť protokol vykonávania alebo údaje o postupe, aby ste videli chyby, ktoré musíte opraviť, aby ste zabezpečili úspešný import.

> [!NOTE]
> Ak potrebujete importovať viac ako jeden formát súboru, musíte vytvoriť samostatné úlohy importu pre každý typ formátu.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Zmena priradenia transakcií kreditnou kartou pre ukončených zamestnancov

Po ukončení záznamu o zamestnancovi je účet zamestnanca Active Directory Domain Services (AD DS) zakázaný. Môžu však existovať aktívne transakcie s kreditnými kartami, ktoré sa musia stále zaúčtovať a uhradiť. Na stránke **Transakcie kreditnou kartou** môžete zamestnanca znova priradiť k akejkoľvek transakcii kreditnou kartou, kde bol priradený zamestnanec prepustený.

Vyberte jednu alebo viac transakcií kreditnou kartou a potom vyberte **Opätovné pridelenie transakcií**. Potom môžete vybrať iného zamestnanca, ktorému chcete priradiť transakcie kreditnou kartou. Po opätovnom priradení transakcií kreditnou kartou ich možno vybrať pre výkaz výdavkov a zaplatiť obvyklým spôsobom na úhradu výkazu výdavkov.

## <a name="delete-credit-card-transactions"></a>Odstránenie transakcií kreditnou kartou 

Niekedy po importovaní transakcií kreditnou kartou môže byť potrebné niektoré transakcie vymazať. Môže to byť spôsobené tým, že transakcie sú duplicitné alebo preto, že údaje nie sú presné. Správcovia môžu používať funkciu **„Odstrániť transakcie kreditnou kartou“** na výber a odstránenie transakcií kreditnou kartou, ktoré **nie sú pripojené** k výkazu výdavkov. 

1. Prejdite na **Periodické úlohy** > **Odstránenie transakcií kreditnou kartou**.
2. Vyberte **Filtrovať** a poskytnite informácie na identifikáciu záznamov, ktoré sa majú zahrnúť.
3. Stlačením možnosti **OK** vymažte záznamy. 

## <a name="storing-credit-card-numbers"></a>Ukladanie čísel kreditných kariet

Na ukladanie čísel kreditných kariet sú k dispozícii tri možnosti. Čísla kreditných kariet sú uložené na **Parametre riadenia výdavkov** stránku.

- **Zabráňte zadávaniu čísla karty** – Čísla kreditných kariet sa neukladajú.
- **Čísla hash kariet (uložte posledné štyri číslice)** – Posledné štyri číslice čísel kreditných kariet sú uložené v zašifrovanom formáte.
- **Uložte čísla kariet** – Čísla kreditných kariet sú uložené v nezašifrovanom formáte. Táto možnosť nie je v súlade so štandardom zabezpečenia údajov (DSS) odvetvia platobných kariet (PCI). Preto, aby bola organizácia v súlade s predpismi PCI DSS, správcovia organizácií by sa mali rozhodnúť buď neukladať čísla kreditných kariet, alebo ukladať čísla hash kariet.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
