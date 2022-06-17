---
title: Mena
description: Tento článok poskytuje informácie o tom, ako pridať a odstrániť typy mien v prevádzke projektu.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0fbfd1039fe0a7401376bb8c27b118297fdc87f5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921551"
---
# <a name="currency"></a>Mena

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_



Meny určujú ceny za produkty, ktoré obsahuje produktový katalóg , a náklady na transakcie, ako sú napríklad objednávky. Ak sa vaši zákazníci nachádzajú naprieč geografickými oblasťami, pridajte si ich meny, aby bolo možné spravovať transakcie. Pridajte meny, ktoré sú najvhodnejšie pre vaše súčasné a budúce podnikateľské potreby.  

> [!NOTE]
> Ak je vašim prostredím prostredie Common Data Service, ste v centre spravovania Power Platform a vyberiete stránku **Meny** (**Prostredia** > [vyberte prostredie]> **Nastavenia** > **Firemné** > **Meny**), stránka bude prázdna. Dôvodom je, že nastavenie meny nie je podporované v prostrediach služby Common Data Service.

## <a name="add-a-currency"></a>Pridanie meny  
Pred začatím tohto postupu skontrolujte, či vaša rola zabezpečenia obsahuje oprávnenia správcu systému. 

1. V centre spravovania Power Platform vyberte prostredie. 
2. Vyberte **Nastavenia** > **Firemné**.
3. Vyberte **Meny**.  
4. Vyberte **Nové**.  
5. Vyplňte informácie podľa potreby.  


   |          Pole          |                                                                                                                                                                                                                                                                                                                                                                            Opis                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Typ meny**    | - **Systém** – Túto možnosť vyberte, ak chcete používať meny dostupné v aplikáciách s podporou modelov v rámci Dynamics 365. Ak chcete hľadať menu, vyberte **Vyhľadávanie**. Keď vyberiete kód meny **názov meny** a **Symbol meny** sa pridajú k vybratej mene automaticky.<br />- **Vlastné** – Túto možnosť vyberte, ak chcete pridať menu, ktorá nie je dostupná v aplikáciách s podporou modelov v rámci Dynamics 365. V tomto prípade musíte manuálne zadať hodnoty pre **kód meny**, **presnosť meny**, **názov meny**, **Symbol meny**, a **Konverzia meny**. |
   |    **Kód meny**    |                                                                                                                                                                                                                                                                                                                                            Skrátený tvar meny. Napríklad **USD** pre americký dolár.                                                                                                                                                                                                                                                                                                                                            |
   | **Presnosť meny**  |                                                                                                                                                                                  Zadajte počet desatinných miest, ktoré chcete použiť pre túto menu.  Môžete pridať hodnotu medzi 0 a 4. **Poznámka:**  Ak ste nastavili hodnotu presnosti v dialógovom okne **Nastavenie systému**, táto hodnota sa zobrazí tu.                                                                                                                                                                                  |
   |    **Názov meny**    |                                                                                                                                                                                                                                         Ak ste vybrali kód meny zo zoznamu dostupných mien v aplikáciách s podporou modelov v rámci Dynamics 365, tu sa zobrazí názov meny pre vybratý kód. Ak ste vybrali **vlastné** ako typ meny, zadajte názov meny.                                                                                                                                                                                                                                          |
   |   **Symbol meny**   |                                                                                                                                                                                                                                                                      Ak ste vybrali kód meny zo zoznamu dostupných mien, tu sa zobrazí symbol zvolenej meny. Ak ste vybrali **vlastné** ako typ meny, zadajte symbol novej meny.                                                                                                                                                                                                                                                                       |
   | **Konverzia meny** |                                                                                                                                                                                                                                     Zadajte hodnotu vybratej meny z hľadiska jedného amerického dolára. Ide o sumu akou sa vybratá mena konvertuje na základnú menu. **Dôležité:**  Nezabudnite túto hodnotu často aktualizovať, aby ste zabránili nepresným výpočtom v transakciách.                                                                                                                                                                                                                                      |


6. Keď skončíte, na paneli s príkazmi vyberte **Uložiť** alebo **Uložiť a Zavrieť**.  

   > [!TIP]
   >  Ak chcete menu upraviť, vyberte menu a potom zadajte alebo vyberte nové hodnoty.  

## <a name="delete-a-currency"></a>Odstráňte menu  

1. V centre spravovania Power Platform vyberte prostredie. 
2. Vyberte **Nastavenia** > **Firemné**.
3. Vyberte **Meny**.  
4. Zo zobrazeného zoznamu mien si vyberte tú, ktorú chcete vymazať.  
5. Vyberte **Odstrániť**.  
6. Potvrďte vymazanie.  

> [!IMPORTANT]
>  Nemôžete vymazať meny, ktoré využívajú iné záznamy. Možno ich len deaktivovať. Deaktiváciou záznamov meny sa neodstránia informácie o mene uložené v existujúcich záznamoch, ako sú napríklad príležitosti alebo objednávky. Avšak, nebudete môcť vybrať deaktivovanú menu pre nové transakcie.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]