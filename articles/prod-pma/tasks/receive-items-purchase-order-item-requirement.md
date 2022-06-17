---
title: Príjem položiek z nákupnej objednávky z požiadaviek na položku
description: Tento článok vysvetľuje, ako získať položky na nákupnú objednávku z požiadavky na položku.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbe15fac325ad00bdd2f2fc6ddf3ae15df45271
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929555"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Príjem položiek z nákupnej objednávky z požiadaviek na položku

[!include [banner](../../includes/banner.md)]

Tento článok vysvetľuje, ako získať položky na nákupnú objednávku z požiadavky na položku.

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