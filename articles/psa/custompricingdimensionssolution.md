---
title: Vytváranie vlastných riešení pre cenové dimenzie
description: Táto téma vysvetľuje, ako vytvoriť vlastné riešenie pri vytváraní vlastných cenových dimenzií.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 4dea80d8e4645675d3e89e846532ca7c0f292faa328c45938941c50dc15486fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995285"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Vytváranie vlastných riešení pre cenové dimenzie

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Všetky zmeny vlastných cenových dimenzií by mali byť v samostatnom riešení. Táto dôležitá najlepšia prax poskytuje flexibilitu v budúcnosti na aktualizáciu alebo odstránenie zmien podľa potreby, pomôže pri opätovnom použití vašej práce a uľahčuje port týchto zmien na inú inštanciu. Potom, čo vykonáte všetky požadované zmeny, exportujte toto riešenie ako **spravované riešenie** a importujte ho do iných inštancií na opätovné použitie nastavení cien.

1. Vyberte položku **Nastavenia** > **Riešenia** a potom vyberte položku **Nové**. 
2. Pomenujte riešenie, **dimenzie cien \<your organization name>**, zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.

> ![Vytvorenie vlastného riešenia pre cenové dimenzie.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Pridajte všetky požadované entity a súvisiace súčasti do riešenia Cenové dimenzie
Budete musieť pridať nasledujúce entity služby Project Service na vaše cenové riešenie. Dokončite kroky v tomto postupe tak, aby sa niektoré dôležité zmeny schémy v cenovom riešení tak, že entity sa dozvedia o nových cenových dimenziách.

1. Vyberte **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**. 
2. V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Pridať existujúce** > **Entity**.
3. V dialógovom okne **súčasti riešenia** vyberte nasledujúce entity:

- Skutočnosť
- Rezervovateľný zdroj
- Riadok odhadu
- Projektová úloha
- Podrobnosti o riadku faktúry
- Záznam v účtovnom denníku
- Podrobnosti o riadku projektovej zmluvy
- Člen projektového tímu
- Podrobnosti o riadku cenovej ponuky
- Prirážka k cene roly
- Cena roly 
- Zadanie času 

> ![Pridanie existujúcich entít do riešenia cenových dimenzií.](media/Existing-entities-to-PD-solution.png)

> ![Výber súčastí riešenia.](media/Dimension-Components.png)

> [!NOTE]
> Nezabudnite zahrnúť všetky formuláre a zobrazenia pre každú vybranú entitu.

4. Keď sa zobrazí výzva na zahrnutie všetkých závislých entít pre entity vybraté vyššie, vyberte položku **Nie**.

> ![Nezahrnúť súvisiace súčasti.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]