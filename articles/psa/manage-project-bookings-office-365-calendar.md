---
title: Riaďte projekty a rezervácie vo vašom Office 365 kalendári
description: Ako riadiť projekty a rezervácie vo vašom Office 365 kalendári
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b38affbfc8d339ac1a2093391286ea4c095207be8de2e8eeca558e6fcc5bcc07
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985453"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Spravujte projekty a rezervácie vo svojom kalendári (Project Service)

> [!Note]
> ZASTARANÉ: Táto funkcia bola zastaraná a už nie je k dispozícii.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Zobraziť osobné stretnutia, priradenia práce na projekte rezervácie a objednávky prác Field Service pomocou kalendára [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Všetko na jednom mieste, je ľahké riadiť váš deň. Stretnutia, plánované činnosti, rezervácie a úlohy sú k dispozícii v kalendári služby [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Ak používate [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], môžete tiež zadať vlastné plánované činnosti v zobrazení zadania času Project Service. To umožňuje projektu a zdroj manažéri vedieť o svojej dostupnosti pre projekty. Tiež vám ušetrí čas, pretože nemusíte dvakrát zadávať info o vašich osobných plánovaných činnostiach. Môžete jednoducho importovať vaše osobné plánované činnosti z kalendára do zobrazenia zadávania času Project Service.  
  
 Kalendár bude synchronizovať projektu a rezervácie pracovnej objednávky od dneška počas nasledujúcich štyroch týždňoch. Toto nastavenie nie je možné zmeniť.  
  
 Synchronizácia je podporovaná iba jednosmerne z PSA do vášho kalendára služieb [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. Môžete synchronizovať v opačnom poradí. 
  
 Ak sa chcete naučiť používať kalendára služieb [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], pozrite [Kalendár programu Outlook na webe pre podnikanie](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)  
  
## <a name="setup"></a>Inštalácia  
 Pred zobrazením a správou kalendára [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] budete musieť nastaviť niekoľko vecí.  
  
- Musíte mať poverenia globálneho správcu [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] alebo systémového správcu.  
  
- Váš správca bude musieť nakonfigurovať profil e-mailového servera a každý používateľ bude musieť nakonfigurovať svoju schránku. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Nastavenie spracovania e-mailov pomocou synchronizácie na strane servera](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Zapnutie synchronizácie pre vašu organizáciu (úloha správcu)  
  
1.  V hlavnej ponuke kliknite na **Nastavenia** > **Správa**.  
  
2.  Kliknite na položku **Nastavenia systému**.  
  
3.  Kliknite na kartu **Synchronizácia**.  
  
4.  Pod **Vyberte, či chcete povoliť synchronizáciu rezervácie zdrojov s Outlookom** označte **Synchronizovať rezervácie zdrojov s Outlookom**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Zapnutie synchronizácie profilu užívateľa (užívateľ úloha)  
  
1.  Kliknite na tlačidlo **Nastavenia**  v pravom hornom rohu obrazovky.  
  
2.  Kliknite na **Možnosti**.  
  
3.  Kliknite na kartu **Synchronizácia**.  
  
4.  V **Synchronizovať rezervácie zdrojov s Outlookom** označte **Synchronizovať rezervácie zdrojov s Outlookom**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importovať vlastné plánované činnosti (užívateľ úloha)  
 Môžete importovať vaše osobné plánované činnosti z kalendára do zobrazenia zadávania Project Service Automation.  
  
1. Otvorte kalendár [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] a kliknite na tlačidlo **Import údajov**.  
  
2. Na obrazovke filtre, vyberte **plánované činnosti z výmeny** a potom kliknite na tlačidlo **použiť**.  
  
3. Systém bude ťahať plánované činnosti do zobrazení času vstupu ako navrhovaných položiek z aktuálneho týždňa. Pridať položky na ďalší týždeň, kliknite **predchádzajúce** alebo **ďalšie**.  
  
4. Vyberte plánovanú činnosť, ktorú chcete pridať do Project Service Automation čas položka Zobraziť.  
  
5. Vo vyskakovacom okne **čas vstupu** vyberte príslušné možnosti previesť plánovanej činnosti na zobrazenie vstupu času Project Service Automation.  
  
6. Kliknite na tlačidlo **Uložiť**.  
  
### <a name="see-also"></a>Pozrite si tiež:  
 [Príručka časom, nákladmi a spoluprácou](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]