---
title: Import a udržiavanie transakcií kreditnou kartou
description: Táto téma vysvetľuje, ako importovať a udržiavať transakcie kreditnými kartami súvisiace s výdavkami. Tieto transakcie je možné nastaviť tak, aby sa automaticky importovali podľa opakujúceho sa plánu, alebo podľa potreby je možné ich manuálne importovať.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084517"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Import a udržiavanie transakcií kreditnou kartou

[!include [banner](../includes/banner.md)]

Transakcie s kreditnými kartami súvisiace s výdavkami je možné nastaviť tak, aby sa automaticky importovali podľa opakujúceho sa harmonogramu. Alternatívne je možné transakcie importovať manuálne podľa potreby. Transakcie kreditnými kartami sa importujú prostredníctvom dátovej entity Transakcie kreditnou kartou.

Ďalšie informácie o entitách údajov nájdete v časti [Entity údajov](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

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
