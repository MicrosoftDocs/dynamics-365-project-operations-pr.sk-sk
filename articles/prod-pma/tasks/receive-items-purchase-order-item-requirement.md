---
title: Príjem položiek z nákupnej objednávky z požiadaviek na položku
description: Táto téma vysvetľuje, ako prijímať položky na nákupnej objednávke z požiadavky na položku.
author: Yowelle
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
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2083516ff929113fd6db377acfe5aeb104666dd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288247"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Príjem položiek z nákupnej objednávky z požiadaviek na položku

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]