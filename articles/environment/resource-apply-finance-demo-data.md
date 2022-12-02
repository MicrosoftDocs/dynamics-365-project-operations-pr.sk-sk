---
title: Použitie ukážkových údajov v prostredí na cloudovom hostiteľskom systéme Finance
description: Tento článok vysvetľuje, ako aplikovať ukážkové údaje z Project Operations do prostredia na cloudovom hostiteľskom systéme Dynamics 365 Finance.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 793b1a01f3bf692bb9f4c2d9abad9a44b110544a
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029916"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Použitie ukážkových údajov v prostredí na cloudovom hostiteľskom systéme Finance

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

> [!IMPORTANT]
> Tento článok sa týka iba systému Microsoft Dynamics 365 Finance verzie 10.0.13 a je možné ho používať iba v prostredí hosťovanom v cloude. Kroky v tomto článku vykonajte **PRED** použitím aktualizácií prostredia týkajúcich sa kvality.

1. Vo svojom projekte LCS otvorte stránku **Podrobnosti o prostredí**. Pamätajte na to, že obsahuje podrobnosti potrebné na pripojenie k prostrediu pomocou protokolu RDP (Remote Desktop Protocol).

![Podrobnosti o prostredí.](./media/1EnvironmentDetails.png)

Prvou súpravou zvýraznených poverení sú poverenia pre lokálny účet a obsahujú hypertextový odkaz na pripojenie k vzdialenej ploche. Poverenia zahŕňajú používateľské meno a heslo správcu prostredia. Druhá súprava poverení sa používa na prihlásenie na server SQL v tomto prostredí.

2. Pripojte sa k vzdialenej ploche pomocou hypertextového odkazu v časti **Lokálne účty** a použite **Poverenia lokálneho účtu** na overenie.
3. Prejdite do časti **Internetové informačné služby** > **Fondy aplikácií** > **AOSService** a zastavte službu. V tomto okamihu zastavíte službu, aby ste mohli pokračovať v nahradzovaní databázy SQL.

![Zastavenie AOS.](./media/2StopAOS.png)

4. Prejdite na **Služby** a zastavte nasledujúce dve položky:

- Microsoft Dynamics 365 Unified Operations: Služba dávkovej správy
- Microsoft Dynamics 365 Unified Operations: Platforma na import a export údajov

![Zastavenie služieb.](./media/3StopServices.png)

5. Otvorte Microsoft SQL Server Management Studio. Prihláste sa pomocou poverení servera SQL a použite meno používateľa axdbadmin a heslo zo stránky **Podrobnosti prostredia** LCS.

![SQL Server Management Studio.](./media/4SSMS.png)

6. V Prieskumníkovi objektov, **Databázy** a nájdite **AXDB**. Databázu nahradíte novou databázou, ktorá sa nachádza v časti [Centrum sťahovania](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Skopírujte súbor zip do virtuálneho počítača, ku ktorému ste vzdialene pripojení, a rozbaľte obsah súboru zip.
8. V programe SQL Server Management Studio kliknite pravým tlačidlom myši na **AxDB** a potom vyberte **Úlohy** > **Obnoviť** > **Databáza**.

![Obnovenie databázy.](./media/5RestoreDatabase.png)

9. Vyberte **Zdrojové zariadenie** a prejdite na súbor rozbalený zo súboru zip, ktorý ste skopírovali.

![Zdrojové zariadenia.](./media/6SourceDevice.png)

10. Vyberte **Možnosti** a potom vyberte **Prepísať existujúcu databázu** a **Zatvoriť existujúce pripojenia k cieľovej databáze**. 
11. Vyberte položku **OK**.

![Obnovenie nastavení.](./media/7RestoreSetting.png)

Dostanete potvrdenie, že obnovenie AXDB bolo úspešné. Po prijatí tohto potvrdenia môžete zavrieť SQL Services Management Studio.

12. Prejdite späť do časti **Internetové informačné služby** > **Fondy aplikácií** > **AOSService** a spustite AOSService.
13. Prejdite do časti **Služby** a spustite dve služby, ktoré ste zastavili predtým.

14. Vyhľadajte nástroj AdminUserProvisioning na tomto virtuálnom počítači. Prejdite na K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Spustite súbor .ext pomocou svojej adresy používateľa v poli **E-mailová adresa**. 
16. Stlačte možnosť **Odoslať**.

![Poskytovanie používateľa správcu.](./media/8AdminUserProvisioning.png)

Dokončenie trvá pár minút. Mali by ste dostať potvrdzujúce hlásenie, že správca bol úspešne aktualizovaný.

17. Nakoniec spustite príkazový riadok ako správca a vykonajte iisreset

![Resetovanie IIS.](./media/9IISReset.png)

18. Ukončite reláciu vzdialenej plochy a pomocou stránky **Podrobnosti o prostredí** LCS sa prihláste do prostredia a uistite sa, že funguje podľa očakávaní.

![Funance a operácie.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]