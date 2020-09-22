---
title: Príjem položiek z nákupnej objednávky z požiadaviek na položku
description: Táto téma vysvetľuje, ako prijímať položky na nákupnej objednávke z požiadavky na položku.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755521"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Príjem položiek z nákupnej objednávky z požiadaviek na položku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Táto téma vysvetľuje, ako prijímať položky na nákupnej objednávke z požiadavky na položku.

Použitím požiadavky na položku namiesto transakcie s položkou môžete naplánovať dodanie tesne pred skutočným použitím položky, vytvoriť objednávku, zahrnúť položku do rámca obchodnej zmluvy a zahrnúť požiadavku na položku do plánovania výroby. 

Táto úloha používa množinu údajov USSI.

1. Na navigačnej table prejdite do **Moduly > Projektové riadenie a účtovníctvo > Projekty > Všetky projekty**.
2. V zozname vyberte odkaz v požadovanom riadku.
3. Na table Akcia vyberte možnosť **Plán**.
4. Vyberte **Požiadavky na položku**.
5. Vyberte **Nové**.
6. V novom riadku zadajte alebo vyberte hodnotu v poli **Číslo položky**.
7. V poli **Množstvo** zadajte číslo.
8. Vyberte položku **Uložiť**.
9. Na table Akcia vyberte možnosť **Správa**.
10. Vyberte **Funkcie**.
11. Vyberte **Vytvorenie nákupnej objednávky**.
12. Vyberte začiarkavacie políčko **Zahrnúť všetko**.
13. V poli **Účet predajcu** zadajte alebo vyberte hodnotu.
14. Vyberte položku **OK**.
15. Na navigačnej table prejdite do **Moduly > Záväzky > Nákupné objednávky > Všetky nákupné objednávky**.
16. V zozname vyberte odkaz v požadovanom riadku.
17. Na table Akcia vyberte možnosť **Kúpiť**.
18. Vyberte položku **Potvrdiť**.
19. Na table Akcia vyberte možnosť **Prijať**.
20. Vyberte **Príjem produktu**.
21. V poli **Príjem produktu** zadajte hodnotu.
22. Vyberte položku **OK**.

