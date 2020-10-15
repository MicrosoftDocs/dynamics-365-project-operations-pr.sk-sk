---
title: Použitie ukážkových údajov nastavenia a konfigurácie
description: Táto téma poskytuje informácie o tom, ako použiť ukážkové údaje nastavenia a konfigurácie pre Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949067"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Použitie ukážkových údajov nastavenia a konfigurácie pre jednoduché nasadenie Project Operations – dohoda o fakturácii pro forma

_**Jednoduché nasadenie – dohoda o fakturácii pro forma_

1. Stiahnite si [Balík hlavných údajov](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Prejdite do priečinka *ProjOpsDemoDataSetupAndMaster – integrovaný CMT* a spustite spustiteľný súbor, *DataMigrationUtility*.
3. Na strane 1 Common Data Service Sprievodcu migráciou konfigurácie (CMT) vyberte **Import údajov** a potom vyberte **Pokračovať**.

![Migrácia konfigurácie](./media/1ConfigurationMigration.png)

4. Na strane 2 Sprievodcu CMT vyberte **Office 365** ako **Typ nasadenia**.
5. Vyberte možnosť **Zobraziť zoznam dostupných organizácií** a začiarkavacie políčka **Zobraziť rozšírené**.
6. Vyberte oblasť svojho nájomníka, zadajte svoje poverenia a potom vyberte **Prihlásiť sa**.

![Prihlásenie do konfigurácie](./media/2ConfigurationSignin.png)

7. Na strane 3 zo zoznamu Organizácie v časti Nájomník vyberte, do ktorej organizácie chcete importovať ukážkové údaje, a potom vyberte **Prihlásiť sa**.
8. Na strane 4 vyberte súbor zip, *MasterAndSetupData* z rozbaleného priečinka *ProjOpsDemoDataSetupAndMaster – integrovaný CMT*.

![Súbor Zip](./media/3ZipFile.png)

![Výber súboru](./media/4SelectAFile.png)

9. Po výbere súboru zip vyberte **Import údajov**.

![Importovať údaje](./media/5ImportData.png)

10. Import bude trvať približne dve až desať minút v závislosti od rýchlosti vašej siete. Po dokončení ukončite sprievodcu CMT. 
11. Skontrolujte údaje svojej organizácie v nasledujúcich 20 entitách:

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
- Podrobnosti o frekvencii faktúr
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
