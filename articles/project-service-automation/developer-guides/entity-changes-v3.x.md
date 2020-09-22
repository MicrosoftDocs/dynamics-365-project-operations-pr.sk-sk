---
title: Entita, ovládací prvok a zmeny používateľského rozhrania (Project Service Automation 3.x)
description: Táto téma popisuje zmeny riešení pre Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9f8828c6-541c-4945-8c99-5785118e191d
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 56aa0bb8272b886bcd15dadd0f74fff3bc43e26b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755615"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Entita, ovládací prvok a zmeny používateľského rozhrania (Project Service Automation 3.x)
Pri vydaní Microsoft Dynamics Project Service Automation (PSA) 3.x sa vykonali mnohé zmeny entít, ovládacích prvkov, zobrazení a používateľského rozhrania. Táto téma poskytuje informácie o týchto verziách dôležitých zmenách:

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Vzťahy nadradený-podradený pre predajný doklad, riadok predajného dokladu, podrobné entity riadkov predajného dokladu
Vo verziách Dynamics 365 Project Service Automation (PSA) vydaného pred verziou 3,0, niektoré vzťahy medzi predajnými dokladmi, riadkami predajného dokladu a podrobnými entitami riadkov predajného dokladu boli už implementované prostredníctvom reťazca polia, ktoré by malo držať reťazové zastúpenie GUID súvisiacej entity. To bolo kvôli platforme obmedzení, ktoré vyžadujú významný vlastný kód na serveri a klientské strany riešenia, aby tieto vzťahy fungovali podobne ako typické Dynamics CRM vzťahy entity a aby sa reťazec polí správal ako vyhľadávacie polia.

PSA 3,0 bolo aktualizované na využitie novej entity vzťahu medzi predajným dokladom a riadkom predajného dokladu.

Keďže vyhľadávacie polia sa teraz môžu použiť na označenie odkazov na entity, polia, ktoré držali hodnotu reťazca identifikátora GUID súvisiacej entity v predchádzajúcich verziách, už nie sú potrebné, a preto boli zastarané. Vlastný klient a vedľajší serverový kód, ktorý spracováva vzťahy definované staršími verziami reťazcami polí, bol tiež zastaraný.

### <a name="entity-schema-changes"></a>Zmeny schémy entity
Nasledujúca tabuľka poskytuje zoznam jedna k jednej zastaraných reťazcov polí a nové vyhľadávacie polia pre entity. 

 Entita |   Zastarané pole (reťazec) | Nové pole (Vyhľadávanie)
--- | --- | ---
Podrobnosti o faktúre (Fakturačný riadok) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (skutočná hodnota) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Rozpis faktúr v riadku projektovej zmluvy) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Míľnik riadka projektovej zmluvy) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (fakt) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (detail riadka faktúry) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (záznam v účtovnom denníku) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Riadok zdrojovej kategórie v projektovej zmluve) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (detail riadka projektovej zmluvy) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (riadok kategórie transakcie v projektovej zmluve) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (riadok klasifikácie transakcie v projektovej zmluve) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Riadok cenovej ponuky plánu fakturácie) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Riadok cenovej ponuky zdrojovej kategórie) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (míľnik riadka cenovej ponuky) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (detail riadku cenovej ponuky) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Riadok cenovej ponuky transakčnej kategórie) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (riadok cenovej ponuky klasifikácie transakcie) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (riadok objednávky) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Zastarané vlastné zobrazenia a ovládacie prvky
Nasledujúce vlastné zobrazenia a ovládacie prvky a ich súvisiace artefakty boli zastarané.

- Zobrazenie účtovateľnosti.
- Vlastné ovládacie prvky mriežky na zobrazenie podrobností riadka cenovej ponuky na stránke **projektové informácie** pre riadok cenovej ponuky.
- Vlastné ovládacie prvky mriežky na zobrazenie podrobností riadka projektovej zmluvy na stránke **projektové informácie** pre riadok predajnej objednávky.

> [!NOTE]
> Úplný zoznam zastarané zdroje, pozri [zastarané webové prostriedky v Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Modul aplikácie zjednoteného klientskeho rozhrania
So zavedením modulov aplikácie zjednoteného klientsého rozhrania (UCI) boli položky mapy lokality PSA odstránené zo systému.  
Funkčnosť súvisiaca s prepínaním formulárov pre príležitosť, cenovú ponuku, objednávku, faktúru bola zastaraná, pretože už nie je potrebná, pretože modul aplikácie UCI obsahuje iba PSA verzie formulárov.  

Nasledujúce webové prostriedky boli zastarané:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Úplný zoznam zastaraných zdrojov, pozri [zastarané webové prostriedky v Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).


