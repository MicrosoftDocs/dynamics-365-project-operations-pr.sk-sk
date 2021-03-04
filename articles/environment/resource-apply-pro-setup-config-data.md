---
title: Nastavenie a použitie konfiguračných údajov v Common Data Service
description: Táto téma poskytuje informácie o nastavení a použití konfiguračných údajov v Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642247"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Nastavenie a použitie konfiguračných údajov v Common Data Service 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Predpoklady

Skôr ako začnete konfigurovať údaje v Common Data Service (CDS), musia byť splnené nasledujúce predpoklady:

1.  Nasadenie prostredia CDS a prostredia Dynamics 365 Finance pre Project Operations.
2.  Informácie o právnickej osobe z Dynamics 365 Finance sa zdieľajú s prostredím CDS. To znamená, že entita **Spoločnosť** v CDS má tieto firemné záznamy:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Inštalácia údajov pre nastavenie a konfiguráciu

1. Stiahnite, odblokujte a rozbaľte súbor [Balík údajov nastavenia a konfigurácie](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Prejdite do rozbaleného priečinka a spustite spustiteľný súbor *DataMigrationUtility*.
3. Na strane 1 Common Data Service Sprievodcu migráciou konfigurácie (CMT) vyberte **Import údajov** a potom vyberte **Pokračovať**.

![Migrácia konfigurácie](./media/1ConfigurationMigration.png)

4. Na strane 2 Sprievodcu CMT vyberte **Microsoft 365** ako **Typ nasadenia**.
5. Vyberte možnosť **Zobraziť zoznam dostupných organizácií** a začiarkavacie políčka **Zobraziť rozšírené**.
6. Vyberte oblasť svojho nájomníka, zadajte svoje poverenia a vyberte **Prihlásiť sa**.

![Prihlásenie do konfigurácie](./media/2ConfigurationSignin.png)

7. Na strane 3 zo zoznamu Organizácie v časti Nájomník vyberte, do organizáciu, do ktorej chcete importovať ukážkové údaje, a vyberte **Prihlásiť sa**.
8. Na strane 4 vyberte súbor zip *SampleSetupAndConfigData* z rozbaleného priečinka.

![Výber súboru ZIP](./media/3ZipFile.png)

![Výber súboru](./media/4SelectAFile.png)

9. Po výbere súboru zip vyberte **Import údajov**.

![Import údajov](./media/5ImportData.png)

10. Import bude trvať približne dve až desať minút v závislosti od rýchlosti vašej siete. Po dokončení importovania ukončite sprievodcu CMT. 
11. Skontrolujte údaje svojej organizácie v nasledujúcich 19 entitách:

  - Mena
  - Organizačná jednotka
  - Kontakt
  - Daňová skupina
  - Skupina zákazníkov
  - Jednotka
  - Skupina jednotiek
  - Cenník
  - Cenník parametrov projektu
  - Frekvencia faktúr
  - Kategória rezervovateľného zdroja
  - Kategória transakcie
  - Kategória výdavku
  - Cena roly
  - Cena kategórie transakcie
  - Charakteristika
  - Rezervovateľný zdroj
  - Priradenie kategórie rezervovateľného zdroja
  - Charakteristika rezervovateľného zdroja

![Dokončenie importu](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Aktualizujte konfigurácie Project Operations

1. Prejdite do prostredia CE. Nájdete ho po otvorení [Power Platform Centrum spravovania](https://admin.powerplatform.microsoft.com/environments) a výberom prostredia a potom výberom **Otvorené prostredie**. 

![Otvorenie prostredia](./media/7OpenEnvironment.png)

2. Prejdite do **Projekty** > **Zdroje** a potom vyberte **Nový** na vytvorenie rezervovateľného zdroja pre vášho používateľa.

![Rezervovateľné zdroje](./media/8BookableResources.png)

3. Na karte **Všeobecné** vyberte svojho správcu. Skontrolujte, či sa časové pásmo zhoduje s tým, v ktorom sa nachádzate. 

![Nový rezervovateľný zdroj](./media/9NewBookableResource.png)

4. Na karte **Plánovanie** v poli **Spoločnosť** vyberte spoločnosť **USPM** a potom vyberte **Uložiť**. 

![Karta Plánovanie](./media/10SchedulingTab.png)

5. Stlačte kartu **Pracovný čas**.  

![Pracovné hodiny](./media/11WorkHours.png)

6. Dvakrát kliknite na ľubovoľnú hodnotu v kalendári a vyberte **Upraviť** > **Všetky udalosti v rade**. 

![Pracovný kalendár](./media/12WorkCalendar.png)

7. Zmeňte pracovný čas na osemhodinový (8) pracovný deň, víkendy označte ako dni pracovného pokoja a uistite sa, že časové pásmo zodpovedá tomu vášmu. 
8. Vyberte položku **Uložiť a zavrieť**.

![Aktualizovanie kalendára](./media/13UpdateCalendar.png)

9. Prejdite do **Nastavenia** > **Šablóny kalendára** a vyberte **Nová**.
 
 ![Šablóny kalendárov](./media/14CalendarTemplates.png)
 
 10. Zadajte názov, vyberte zdroj šablóny, ktorú ste vytvorili, a potom vyberte **Uložiť**. 
 
 ![Uloženie šablóny kalendára](./media/15SaveCalendarTemplate.png)
 
 11. Prejdite do **Parametre** a dvakrát kliknite na záznam. 
 
 ![Parametre projektu](./media/16ProjectParameters.png)
 
12. Aktualizujte nasledujúce polia:

 - **Predvolená spoločnosť**: USPM
 - **Predvolená organizačná jednotka**: Contoso Robotics Global
 - **Frekvencia faktúr**: Siedmy a posledný deň
 - **Šablóna pracovného času**: Zmena na šablónu, ktorú ste vytvorili.

13. Vyberte položku **Uložiť**. 

![Aktualizované parametre projektu](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]