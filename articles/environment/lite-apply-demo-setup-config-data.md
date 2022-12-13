---
title: Použitie ukážkových údajov nastavenia a konfigurácie – čiastočné
description: Tento článok poskytuje informácie o tom, ako použiť ukážkové údaje nastavenia a konfigurácie pre Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811045"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Použitie ukážkových údajov nastavenia a konfigurácie pre Project Operations – čiastočné 

_**Jednoduché nasadenie – dohoda o fakturácii pro forma_



## <a name="prerequisites"></a>Požiadavky

Pred začatím konfigurácie musíte mať zriadené prostredie Dataverse pre Dynamics 365 Project Operations.


## <a name="instructions"></a>Pokyny

1. Stiahnite si  [Inštalačný dátový balík](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Prejdite do priečinka *ProjOpsSampleSetupData - iba CMT s CE* a spustite spustiteľný súbor *DataMigrationUtility*.
1. Na strane 1 Common Data Service Sprievodcu migráciou konfigurácie (CMT) vyberte **Import údajov** a potom vyberte **Pokračovať**.

    ![Migrácia konfigurácie.](./media/1ConfigurationMigration.png)

1. Na strane 2 Sprievodcu CMT vyberte **Microsoft 365** ako **Typ nasadenia**.
1. Vyberte možnosť **Zobraziť zoznam dostupných organizácií** a začiarkavacie políčka **Zobraziť rozšírené**.
1. Vyberte oblasť svojho nájomníka, zadajte svoje poverenia a potom vyberte **Prihlásiť sa**.

   ![Prihlásenie do konfigurácie.](./media/2ConfigurationSignin.png)

1. Na strane 3 zo zoznamu Organizácie v časti Nájomník vyberte, do ktorej organizácie chcete importovať ukážkové údaje, a potom vyberte **Prihlásiť sa**.
1. Na strane 4 vyberte súbor .zip *SampleSetupAndConfigData* z rozbaleného priečinka *ProjOpsSampleSetupData - iba CMT s CE*.

   ![Súbor Zip.](./media/3ZipFile.png)

   ![Vybrať súbor.](./media/4SelectAFile.png)

1. Po výbere súboru zip vyberte **Import údajov**.

   ![Import údajov.](./media/5ImportData.png)

1. Import bude trvať približne dve až desať minút v závislosti od rýchlosti vašej siete. Po dokončení ukončite sprievodcu CMT. 
1. Skontrolujte údaje svojej organizácie v nasledujúcich 18 entitách:

    -   Mena
    -   Konto
    -   Organizačná jednotka
    -   Kontakt
    -   Jednotka
    -   Skupina jednotiek
    -   Cenník
    -   Cenník parametrov projektu 
    -   Frekvencia faktúr
    -   Kategória rezervovateľného zdroja
    -   Kategória transakcie
    -   Kategória výdavku
    -   Cena roly
    -   Cena kategórie transakcie
    -   Charakteristika
    -   Rezervovateľný zdroj
    -   Priradenie kategórie rezervovateľného zdroja
    -   Charakteristika rezervovateľného zdroja

    ![Dokončenie importu.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
