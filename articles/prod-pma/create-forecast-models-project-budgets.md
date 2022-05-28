---
title: Vytvorenie modelov prognóz pre rozpočty projektov
description: Táto téma popisuje, ako vytvoriť model prognózy pre zostávajúce rozpočty.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 992dd74524ae6a7c329612a125d60bebfcbe7dd2
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683649"
---
# <a name="create-forecast-models-for-project-budgets"></a>Vytvorenie modelov prognóz pre rozpočty projektov 

[!include [banner](../includes/banner.md)]

Táto téma popisuje, ako vytvoriť model prognózy pre zostávajúce rozpočty. Projekt, ktorý podlieha kontrole rozpočtu, používa dva typy rozpočtov: pôvodný a zvyšný. Pri vytváraní rozpočtu projektu musíte určiť pôvodný a zostávajúci model prognózy rozpočtu, ktoré boli vytvorené na stránke **Modely prognóz**. Rozpočty projektu založené na zadaných modeloch sa vytvárajú pri potvrdení projektového rozpočtu.

> [!NOTE]
> Model prognózy, ktorý sa používa na kontrolu rozpočtu, nemôže mať podmodel alebo ho nemožno použiť ako podmodel.

1. Vyberte **Projektové riadenie a účtovníctvo** > **Nastavenie** > **Prognózy**  > **Modely prognóz**.
2. Vyberte možnosť **Nový** a vytvorte nový model prognózy a potom zadajte číslo ID a názov nového modelu. 
3. Nastavte možnosť **Zastavené** na **Áno**, čím zabránite akýmkoľvek zmenám v riadkoch prognózy pre model prognózy. 
4. Ak by riadky prognózy, s ktorými je model spojený, mali generovať prognózy peňažných tokov v hlavnej účtovnej knihe, nastavte možnosť **Zahrnúť do prognóz peňažného toku** na **Áno**. 
5. Ak chcete ako dátum fakturácie použiť dátum projektu, nastavte možnosť **Prognóza dátumu faktúry** na **Áno**. 
6. V poli **Typ rozpočtu** vyberte jeden z nasledujúcich typov modelov:

   - **Pôvodný rozpočet**: Použite pôvodné sumy rozpočtu, ktoré sú potvrdené pri vytvorení a schválení pôvodného rozpočtu.
   - **Zostávajúci rozpočet**: Použite zostávajúce sumy rozpočtu počas realizácie projektu. Zostatky v tomto modeli prognózy sa znižujú o skutočné transakcie a zvyšujú alebo znižujú sa revíziami rozpočtu.
   - **Preniesť**: Použite sumy preneseného rozpočtu pre projekt. Prenos je voliteľný proces, pomocou ktorého je možné preniesť nevyužité sumy rozpočtu z jedného fiškálneho roka na druhý.

7. Podľa potreby nastavte nasledujúce možnosti:

   - Povoľte možnosť **Prognóza dátumu faktúry**, ak chcete ako dátum faktúry použiť dátum projektu.
   - Povoľte možnosť **Prognóza s WIP** pre prognózu na základe prebiehajúcej práce (WIP), a potom vyberte typ WIP. 
   - Môžete ponechať predvolené nastavenie **Typ rozpočtu** ako **Žiadny** alebo zadajte nový typ. Po zmene záznamu nie je možné zmeniť typ rozpočtu.     
    > [!NOTE]
    > Ak zmeníte predvolený typ rozpočtu, pre aktualizácie nebudú k dispozícii žiadne ďalšie možnosti a tento model prognózy nebudete môcť znova použiť. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]