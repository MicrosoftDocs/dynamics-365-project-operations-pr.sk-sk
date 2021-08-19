---
title: Aktualizácia atribútov doplnkov o nové cenové dimenzie
description: Táto téma poskytuje informácie o aktualizácii atribútov doplnkov pre cenové dimenzie.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d57ec617d2c7b10a01a75e7eaa9ca2d646af3f6ee1d06d4e6fb228fc0533da27
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988355"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Aktualizácia atribútov doplnkov o nové cenové dimenzie

Táto téma poskytuje informácie o aktualizácii atribútov doplnkov pre cenové dimenzie.

> [!NOTE]
> Táto téma sa týka iba funkcií cenovej ponuky a zmluvy v Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Predpoklady
Pred vykonaním krokov v tejto téme musíte mať dokončené postupy v nasledujúcich témach:

  - [Vytvorenie vlastných polí a entít](create-custom-fields-entities-pricing-dimensions.md) 
  - [Pridanie vlastných polí do entít nastavenia cien a transakcií ](add-custom-fields-price-setup-transactional-entities.md)
  - [Nastavenie vlastných polí ako cenových dimenzií](set-up-custom-fields-pricing-dimensions.md). 
  
Ak ste tieto postupy nedokončili, dokončite ich a potom sa vráťte na túto tému.

## <a name="register-a-plug-in"></a>Registrácia doplnku
Keď sa na stránke **Riadok cenovej ponuky** pre riadok ponuky projektu vytvorí detail riadka cenovej ponuky, systém vytvorí dva riadky odhadu. Jeden riadok je pre stranu nákladov odhadu a druhý riadok pre stranu predaja. Toto je rovnaké pre riadky projektových zmlúv.

Keď vykonáte zmenu množstva alebo poľa na strane nákladov, táto zmena tiež vykoná na strane predaja. Je to možné, pretože doplnky PreOperation na Quotelinedetail a entity podrobností riadka zmluvy spájajú špecifické atribúty na strane nákladov so stranou predaja transakcie. Ak potrebujete vykonať zmeny v hodnotách cenových dimenzií na strane predaja aj na strane nákladov, je potrebné po vykonaní zmien v cenovej dimenzii znova zaregistrovať nasledujúce doplnky.

Toto sú doplnky na aktualizáciu a opätovnú registráciu:

- PreOperationContractLineDetailUpdate – **Aktualizuje msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Aktualizuje msdyn_quotelinetransaction**

Vykonaním nasledujúcich krokov aktualizujete a znova zaregistrujete doplnky.

1. Otvorte **PluginRegistrationTool** a pripojte sa k svojmu prostrediu Project Operations Dataverse.
2. Vyberte **Vyhľadávať** a zadajte niekoľko prvých písmen doplnku, ktorý sa má aktualizovať.
3. Po rozpoznaní doplnku ho označte a potom vyberte možnosť **Vybrať na hlavnom formulári**.
4. Vyberte krok **Aktualizovať msdyn_orderlinetransaction**, kliknite pravým tlačidlom myši a potom vyberte položku **Aktualizovať**.
5. Na dialógovej stránke **Aktualizovať** vyberte tri bodky (**...**) v atribútoch filtrovania.
6. Otvorí sa okno s atribútmi filtrovania, ktoré poskytuje zoznam všetkých atribútov v entite a cenových dimenzií. Začiarknite políčka pre atribúty cenových dimenzií.
7. Výberom tlačidla **OK** zatvoríte stránku a potom vyberte **Aktualizovať krok**.
8. Opakujte kroky 2 až 7 pre druhý doplnok **PreOperationQuoteLineDetail**. Pre tento doplnok budete musieť aktualizovať krok **Aktualizácia msdyn_quotelinetransaction**.
9. Zatvorte nástroj **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]