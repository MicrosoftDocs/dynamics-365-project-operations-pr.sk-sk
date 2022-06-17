---
title: Vytvorenie projektového tímu
description: Tento článok poskytuje informácie o tom, ako vytvoriť a spravovať projektové tímy.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df9df8b3ee9b42a33c6031c78ff3673cad47bfe6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927347"
---
# <a name="create-a-project-team"></a>Vytvorenie projektového tímu

[!include [banner](../includes/banner.md)]

Ak chcete použiť roly, ktoré boli predtým v projekte nastavené, musí projektový manažér priradiť tieto roly k projektu. K projektu je možné priradiť viac rolí. Aby sa predišlo zámene, sú tieto roly počas rezervácie automaticky označené. Ak napr. projektový manažér vyžaduje troch softvérových inžinierov, tri roly softvérového inžiniera, ktoré majú označenie **softvérový inžinier 1**, **softvérový inžinier 2** a **softvérový inžinier 3** sa generujú automaticky. Ak boli pre danú rolu predtým nastavené vlastnosti, použijú sa ako filter počas hľadania zdroja. Podľa potreby je možné pridať ďalšie vlastnosti, aby sa hľadanie ešte vylepšilo.

Nastavenia zobrazenia je možné tiež prispôsobiť, aby sa získal lepší prehľad o dostupnosti zdrojov. K dispozícii sú možnosti zobrazenia hodinovej, dennej, týždennej, mesačnej, štvrťročnej a ročnej dostupnosti. K dispozícii je tiež možnosť zobraziť dostupnú a zostávajúcu kapacitu zdrojov. Táto možnosť je užitočná na správu času, keď odhadujete dostupný čas na aktivity alebo dostupnosť zdrojov.

Projektový manažér môže na stránke zvoliť rolu a potom, ak je k dispozícii zdroj, ktorý vyhovuje požiadavke, vybrať rezerváciu zdroja na vyplnenie roly. Upozorňujeme, že v tomto okamihu fázy plánovania nie je potrebné rezervovať zdroje. Pri vytváraní štruktúry WBS môžete roly nahradiť personálnymi zdrojmi pre projekt. Ak sú roly nahradené personálnymi zdrojmi v štruktúre WBS, nastavenie zdrojov automaticky aktualizuje zoznam a plánovanie projektového tímu.

[![Zoznam projektového tímu, ktorý zahŕňa roly aj skutočné zdroje.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektový manažér má rôzne možnosti rezervácie zdroja pre projekt, ako napr. **Zostávajúca kapacita**, **Plná kapacita**, **Percento kapacity** a **Uveďte hodiny**. Tieto možnosti rezervácie je možné kedykoľvek zrušiť, ak sa zmení priradenie zdrojov. Podporované sú dva typy rezervácií:

- **Pevná rezervácia** – Rezervácia zdroja bola schválená a bolo potvrdené, že bude pracovať na zákazke po stanovenú dobu.
- **Predbežná rezervácia** – Rezervácia zdroja bola predbežne nastavené na prácu na zákazke po stanovenú dobu.

Nasledujúci postup vysvetľuje, ako vytvoriť projektový tím.

## <a name="create-a-project-team"></a>Vytvorenie projektového tímu

1. Na stránke so zoznamom **Všetky projekty** vyberte projekt a potom vyberte **Upraviť**.
2. Na karte **Projektový tím a plánovanie** v poli **Naplánujte dátum ukončenia** zadajte do poľa dátum začatia plánu plus jeden mesiac. Napríklad, ak je dátum začatia plánu 24. júna 2017 (24. 6. 2017), zadajte **24/07/2017**.
3. Stlačte možnosť **Pridať**.
4. V table **Pridať do projektu roly** v poli **Rola** vyberte **Senior projektový manažér**.
5. Vyberte **Požadované kompetencie**.
6. Na stránke **Vybrať vlastnosti** sú predvolene vybrané vlastnosti, ktoré ste predtým nastavili pre rolu Senior projektového manažéra. Vyberte položku **OK**.
7. Na stránke **Pridajte do projektu roly** v poli **Počet zdrojov** zadajte **1**.
8. V poli **Zdroje** vyhľadávanie zobrazuje všetky zdroje, ktoré majú požadované kompetencie. Vyberte **Daniel Goldschmidt** a potom **Vytvoriť**.
9. Na stránke **Projekt** vyberte položku **Pridať**.
10. V table **Pridať do projektu roly** v poli **Rola** vyberte **Člen tímu**. V poli **Počet zdrojov** zadajte **5**.
11. Stlačte možnosť **Vytvoriť**.
12. Na stránke **Projekty** vyberte **Vyplniť zdroj**.

## <a name="monitor-project-teams"></a>Monitorovanie projektových tímov
1. Na stránke **Všetky projekty** vyberte prepojenie **ID projektu** pre projekt **Fáza 2 inovácie XYZ**.
2. Na rýchlej karte **Projektový tím a plánovanie** skontrolujte správnosť zdrojov projektu, ktoré sú uvedené.


[!INCLUDE[footer-include](../includes/footer-banner.md)]