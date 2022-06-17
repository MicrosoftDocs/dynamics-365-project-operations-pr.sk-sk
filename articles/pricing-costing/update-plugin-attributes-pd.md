---
title: Aktualizácia atribútov doplnkov o nové cenové dimenzie
description: Tento článok poskytuje informácie o tom, ako aktualizovať atribúty doplnkov pre cenové dimenzie.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920033"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Aktualizácia atribútov doplnkov o nové cenové dimenzie

Tento článok poskytuje informácie o tom, ako aktualizovať atribúty doplnkov pre cenové dimenzie.

> [!NOTE]
> Tento článok sa vzťahuje len na funkcie ponuky a zmluvy v Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Požiadavky
Pred dokončením krokov v tomto článku musíte vykonať postupy v nasledujúcich článkoch:

  - [Vytvorenie vlastných polí a entít](create-custom-fields-entities-pricing-dimensions.md) 
  - [Pridanie vlastných polí do entít nastavenia cien a transakcií ](add-custom-fields-price-setup-transactional-entities.md)
  - [Nastavenie vlastných polí ako cenových dimenzií](set-up-custom-fields-pricing-dimensions.md). 
  
Ak ste tieto postupy nedokončili, dokončite ich a potom sa vráťte k tomuto článku.

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