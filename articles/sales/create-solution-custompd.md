---
title: Vytvorenie riešenia pre vlastné cenové dimenzie
description: Tento článok poskytuje informácie o vytváraní riešení pre vlastné cenové dimenzie.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cd7fedaa7bece16e99131bcc0faff3ce547580e8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915157"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Vytvorenie riešenia pre vlastné cenové dimenzie

 _**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_ 

>[!IMPORTANT]
>Všetky zmeny vlastných cenových dimenzií by mali byť v samostatnom riešení. Tento dôležitý najlepší postup poskytuje flexibilitu pri aktualizácii alebo odstraňovaní zmien podľa potreby, pomôže pri opätovnom použití vašej práce a uľahčuje portovanie týchto zmien na iné inštancie. Po vykonaní požadovaných zmien exportujte toto riešenie ako **spravované** riešenie a importujte ho do iných inštancií na opätovné použitie.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Vytvorenie riešenia pre vlastné cenové dimenzie

1.  Vyberte položku **Nastavenia** > **Riešenia** a potom vyberte položku **Nové**.
2.  Pomenujte riešenie ako *Cenové dimenzie \<your organization name\>*.
3. Zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.

  ![Vytvorenie vlastného riešenia pre cenové dimenzie.](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Pridajte všetky požadované entity a súvisiace súčasti do riešenia Cenové dimenzie

Pridajte do svojho cenového riešenia nasledujúce entity Project Service, aby ste mohli urobiť dôležité zmeny schémy v cenovom riešení. Po dokončení tohto postupu entity rozpoznajú nové cenové dimenzie.

1.  Vyberte **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **<*názov vašej organizácie*> cenové dimenzie**.
2.  V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Pridať existujúce** > **Entity**.
3.  V dialógovom okne **súčasti riešenia** vyberte nasledujúce entity:
 
   - **Skutočnosť**
   - **Rezervovateľný zdroj**
   - **Riadok odhadu**
   - **Projektová úloha**
   - **Podrobnosti o riadku faktúry**
   - **Záznam v účtovnom denníku**
   - **Podrobnosti o riadku projektovej zmluvy**
   - **Člen projektového tímu**
   - **Podrobnosti o riadku cenovej ponuky**
   - **Prirážka k cene roly**
   - **Cena roly**
   - **Zadanie času**
 
   ![Pridanie existujúcich entít do vlastného riešenia cenovej dimenzie.](./media/Existing-entities-to-PD-solution.png)
 
 4. Pre každú entitu skontrolujte pridávané komponenty a konečný zoznam aktív entity pre každú entitu. 

   >[!NOTE]
   > Zahrňte všetky formuláre a zobrazenia pre každú vybranú entitu.

  ![Pridané entity.](./media/solution-component-selection.png)


5.  Po zobrazení výzvy na zahrnutie akýchkoľvek závislých entít pre vybrané entity vyberte **Nie, nezahŕňať požadované komponenty.**

    ![Vrátane závislých entít.](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]