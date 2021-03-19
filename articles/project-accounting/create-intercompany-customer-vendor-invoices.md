---
title: Vytváranie medzipodnikových faktúr zákazníkov a dodávateľov
description: Táto téma poskytuje informácie o tom, ako vytvárať medzipodnikové faktúry zákazníkov a dodávateľov.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dd9aa1a4d167d556206a487e79983090b3f4592a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287482"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Vytváranie medzipodnikových faktúr zákazníkov a dodávateľov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Účtovník projektu v požičiavajúcej právnickej osobe vytvorí medzipodnikovú faktúru zákazníka za náklady na projekt, ktoré sa prevádzajú na požičiavajúcu si osobu. Po schválení a zaúčtovaní medzipodnikovej faktúry zákazníka pošle požičiavajúca právnická osoba medzipodnikovú faktúru požičiavajúcej si právnickej osobe.

Účtovník projektu pre požičiavajúcu právnickú osobu môže nastaviť dávkový proces na pravidelné generovanie medzipodnikových faktúr. Účtovník projektu špecifikuje kritériá, ako napríklad konkrétne projekty, na vytvorenie medzipodnikových faktúr v dávke.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Ručné vytvorenie medzipodnikovej faktúry zákazníka za projektové transakcie 

Tento postup použite na ručné vytvorenie medzipodnikovej faktúry zákazníka za projektové transakcie. Vyhľadajte hodiny, ktoré uviedli pracovníci na projektoch v požičiavajúcich si právnických osobách, a náklady, ktoré vznikli vašej právnickej osobe v mene požičiavajúcich si právnických osôb. Môžete vyhľadávať podľa názvu právnickej osoby, čísla zmluvy o projekte, čísla projektu, rozsahu dátumov alebo akejkoľvek kombinácie týchto možností. Vo výsledkoch vyhľadávania vyberte transakcie, ktoré sa majú pridať k medzipodnikovej faktúre.

1. V Dynamics 365 Finance prejdite do **Projektový manažment a účtovníctvo** > **Faktúry projektu** > **Medzipodnikové faktúry zákazníka**. Na stránke so zoznamom **Medzipodnikové faktúry zákazníka** na table akcií vyberte **Nový**.
2. Na stránke **Vytvoriť medzipodnikovú faktúru** v poli **Právnická osoba** si vyberte požičiavajúcu si právnickú osobu.
3. Voliteľné: Zadajte konkrétnu zmluvu o projekte a číslo projektu.
4. Zúžte vyhľadávanie výberom rozsahu dátumov. Zadajte konkrétne dátumy do polí **Dátum začiatku** a **Dátum ukončenia**. Vo výsledkoch vyhľadávania sa zobrazia iba medzipodnikové transakcie, ktoré sa zaúčtujú v tomto rozsahu dátumov.
5. Položku **Nastaviť pokročilý parameter záznamu v účtovnom denníku** nastavte na **Áno** a vyberte **Vyhľadať**.
6. Vo výsledkoch vyhľadávania vyberte transakcie, ktoré chcete zahrnúť do návrhu medzipodnikovej faktúry, a potom vyberte **OK**.
7. Na stránke **Medzipodniková faktúra zákazníka** sa zobrazia transakcie medzipodnikového projektu, ktoré ste vybrali z výsledkov vyhľadávania. Ak chcete upraviť transakcie pred odoslaním faktúry požičiavajúcej si právnickej osobe, postupujte takto:
  
    1. Otvorte stránku **Vytvoriť návrh faktúry**. Vyberte ďalšie medzipodnikové transakcie pre aktuálnu faktúru a potom vyberte **Pridať riadok**.
    2. Na odstránenie riadka ho vyberte a potom kliknite na položku **Odstrániť**.
    3. Prezerajte komentáre, dôvody, finančné dimenzie a ďalšie informácie o vybranom riadku na rýchlej karte **Riadky faktúr**.
    
8. Ak chcete zaúčtovať medzipodnikovú faktúru zákazníka, na table akcií vyberte **Zaúčtovať**.

> [!NOTE]
> Ak vaša organizácia vyžaduje, aby boli medzipodnikové faktúry skontrolované pred ich zaúčtovaním, správca systému môže nastaviť pracovný postup pre medzipodnikové faktúry. Ak pre medzipodnikové faktúry nie je nastavený pracovný postup, môžete zaúčtovať medzipodnikovú faktúru.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Vytvorenie dávkovej úlohy pre medzipodnikové faktúry

Môžete vytvoriť viac medzipodnikových faktúr súčasne pre všetky požičiavajúce si právnické osoby. Pomocou vyhľadávacej funkcie môžete napríklad vyhľadávať všetky transakcie, ktoré sú zaúčtované najatými pracovníkmi a súvisia s projektmi, ktoré riadia iné právnické osoby. Potom môžete pre každú požičiavajúcu si právnickú osobu vytvoriť medzipodnikovú faktúru za transakcie uvedené vo výsledkoch vyhľadávania.

1. Prejdite do **Projektový manažment a účtovníctvo** > **Pravidelné** > **Projektové faktúry** > **Vytvoriť medzipodnikové faktúry zákazníkov**.
2. Na stránke **Vytvoriť medzipodnikové faktúry zákazníkov** v poli **Spoločnosť** si vyberte právnickú osobu, ktorá bude fakturovať. Ak nevyberiete spoločnosť, všetky transakcie, ktoré vyhovujú kritériám vyhľadávania, sa zobrazia pre všetky požičiavajúce si právnické osoby.
3. V poli **Vytvoriť jednu faktúru za** vyberte, či chcete vytvoriť faktúru za medzipodnikové transakcie na základe projektu alebo na základe požičiavajúcej si právnickej osoby.
4. Voliteľné: Ak chcete vybrať konkrétny projekt a projektovú zmluvu, pre ktorú chcete vytvoriť medzipodnikové faktúry, kliknite na **Vybrať**. Na stránke **Dopyt** v poli **Kritérium** vyberte projektovú zmluvu, číslo projektu alebo obidve a potom vyberte **OK**.
5. Na karte **Dávka** nastavte dávkový proces na opakované vytváranie medzipodnikových faktúr. Viac informácií nájdete v článku [Odoslať úlohu hromadného spracovania z formulára](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Ak chcete zaúčtovať medzipodnikové faktúry, na table akcií vyberte **Zaúčtovať**.

> [!NOTE]
> Ak vaša organizácia vyžaduje, aby boli medzipodnikové faktúry skontrolované pred ich zaúčtovaním, správca systému môže nastaviť pracovný postup pre medzipodnikové faktúry. Ak pre medzipodnikové faktúry nie je nastavený pracovný postup, môžete zaúčtovať medzipodnikové faktúry.

## <a name="post-the-intercompany-vendor-invoice"></a>Zaúčtovanie medzipodnikovej faktúry dodávateľa

Účtovník projektu v požičiavajúcej si právnickej osobe môže pri zaúčtovaní príslušnej medzipodnikovej faktúry zákazníka skontrolovať nevybavené medzipodnikové faktúry dodávateľa. Vo aplikácii Finance prejdite v požičiavajúcej si právnickej osobe na **Záväzky** > **Faktúry** > **Čakajúca faktúra dodávateľa**. Čakajúce číslo faktúry sa bude zhodovať s číslom faktúry medzipodnikového zákazníka. Overte správnosť faktúry a potom faktúru zaúčtujte. Zaúčtovaním medzipodnikovej faktúry dodávateľa sa vytvorí vedľajšia účtovná kniha projektu a transakcia v hlavnej účtovnej knihe, ktorá odráža transakčné náklady v požičiavajúcej si právnickej osobe.


[!INCLUDE[footer-include](../includes/footer-banner.md)]