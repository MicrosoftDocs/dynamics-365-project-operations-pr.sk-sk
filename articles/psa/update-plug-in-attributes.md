---
title: Aktualizácia atribútov doplnkov na zahrnutie nových dimenzií cien
description: Táto téma poskytuje informácie o aktualizácii atribútov doplnkov pre dimenzie cien.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147087"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Aktualizácia atribútov doplnkov na zahrnutie nových dimenzií cien

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Ak nepoužívate program Project Service Automation (PSA) a funkcie uzatvárania zmlúv, môžete túto tému vynechať.

Pred začatím tejto témy sa predpokladá, že ste dokončili postupy v témach [Vytvorte vlastné polia a entity](create-custom-fields-entities.md), [Pridanie vlastných polí do cenového nastavenia a transakčných entít](field-references.md) a [Nastavenie vlastných polí ako dimenzií cien](set-up-pricing-dimensions.md). Ak ste tieto postupy nedokončili, vráťte sa späť a dokončite ich a potom sa vráťte na túto tému.

Keď sa vytvorí podrobnosti riadka cenovej ponuky na stránke **Riadok cenovej ponuky** pre riadok projektovej ponuky vytvorí detail riadka cenovej ponuky, systém vytvorí dva riadky odhadu v pozadí – jeden riadok pre stranu nákladov odhadu a jeden pre predajnú stranu. Toto je rovnaké pre riadky projektových zmlúv.

Keď vykonáte zmenu množstva alebo poľa na strane nákladov, táto zmena sa vyplní na strane predaja. Je to možné, pretože nasledujúce doplnky musia byť znovu registrované po zmene cenových dimenzií.

- PreOperationContractLineDetailUpdate - Aktualizácie **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Aktualizácie **msdyn_quotelinetransaction**.

Nasledujúce kroky vám vysvetlia proces registrácie doplnkov.

1. Otvorte **PluginRegistrationTool** a pripojte sa k online inštancii.
2. Vyberte položku **Hľadať** a vyhľadajte doplnok, ktorý chcete aktualizovať.

 ![Snímka obrazovky zo stromu vyhľadávania](media/PRT-1.png)

3. Po rozpoznaní doplnku ho označte a potom kliknite na možnosť **Vybrať na hlavnom formulári**.

4. Vyberte krok doplnku, ktorý chcete aktualizovať, kliknite pravým tlačidlom myši a potom vyberte položku **aktualizovať.**

 ![Snímka obrazovky doplnku určeného na aktualizáciu](media/PRT-2.png)
 
5. V okne aktualizácia kliknite na tri bodky (**...**) v atribútoch filtrovania.

 ![Snímka obrazovka z aktualizácie existujúceho kroku informácií konfigurácie](media/PRT-3.png)
 
6. Začiarknite políčka atribút ceny.

 ![Snímka obrazovka znázorňujúce označenie začiarkávacieho poľa atribútov ceny](media/PRT-4.png)

7. Kliknite na tlačidlo **OK** pre stránky a potom vyberte **Aktualizovať**.

 ![Snímka obrazovky zobrazujúca tlačidlo „Aktualizovať”](media/PRT-5.png)
 
8. Tento postup zopakujte pri druhom doplnku, **PreOperationQuoteLineDetail - Aktualizácia msdyn_quotelinetransaction**.

9. Zatvorte registračný nástroj doplnku.



[!INCLUDE[footer-include](../includes/footer-banner.md)]