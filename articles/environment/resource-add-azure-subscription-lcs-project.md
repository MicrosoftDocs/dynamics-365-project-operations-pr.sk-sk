---
title: Pridanie predplatného služieb Azure do projektu LCS
description: Táto téma poskytuje informácie o tom, ako pripojiť vaše predplatné služieb Azure k projektu LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e741f35f9b229d2897cec06054d91ae620397228
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175820"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Pridanie predplatného služieb Azure do projektu LCS

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Prostredia hosťované v cloude musia byť nasadené pomocou existujúceho predplatného služieb Azure. Táto téma vysvetľuje, ako pripojiť vaše existujúce predplatné služieb Azure k projektu LCS. 

## <a name="grant-admin-consent"></a>Udelenie súhlasu správcu

1. V projekte LCS v časti **Prostredia** vyberte **Nastavenia Microsoft Azure**.

![Nastavenia aplikácie Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Na stránke **Nastavenia projektu** na karte **Konektory Azure** vyberte **Povoliť**. Potom bude možné nasadiť prostredia do tohto projektu.

![Konektory Azure](./media/2AzureConnectors.png)

3. Znova vyberte **Povoliť** na poskytnutie súhlasu správcu.

![Udelenie súhlasu správcu](./media/3GrantAdminConsent.png)

4. Prijmite žiadosť o povolenie.

![Prijmite žiadosť o povolenie](./media/4AcceptPermissionRequest.png)

Autorizácia je teraz hotová. 

![Autorizácia bola úspešná](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Poskytnite službe Dynamics Deployment Services prístup k vášmu predplatnému služieb Azure

1. Prejdite do ponuky [Fakturácia Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) a zvoľte svoje predplatné. Aby mohla služba Dynamics Deployment Services nasadiť prostredia, musí mať prístup k tomuto predplatnému.

![Podrobnosti o predplatnom služieb Azure](./media/6AzureSubscription.png)

2. Na navigačnej table vyberte **Kontrola prístupu (IAM)** a potom vyberte **Pridať priradenie roly**.
3. V posúvači na pravej strane vyberte **Rola prispievateľa** a v uvedenom zozname vyhľadajte a vyberte **Dynamics Deployment Services**. 
4. Vyberte položku **Uložiť**.

![Prístup k predplatnému](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Pridajte konektor predplatného do projektu LCS

1. Vo projekte LCS na stránke **Nastavenia Microsoft Azure** vyberte **Pridať** na pridanie nového konektora.
2. Zadajte svoje ID predplatného Azure. Svoje ID predplatného Azure nájdete na [portáli Azure](https://ms.portal.azure.com/) v časti **Nastavenia** v ľavom dolnom rohu obrazovky.
3. V poli **Nakonfigurovať použitie Azure Resource Manager** vyberte **Áno**.
4. Uistite sa, že sa predplatné Azure AAD Tenant Domain zhoduje s predplatným Azure s vlastníctvom domény, ktoré používate, a vyberte **Ďalej**.
5. Na obrazovke **Nastaviť Microsoft Azure** zvoľte **Ďalej** na potvrdenie. Ak sa vám na tejto obrazovke zobrazí chyba, vráťte sa do sekcie [Poskytnúť službe Dynamics Deployment Services prístup k predplatnému Azure](#provide) v tejto téme a uistite sa, že ste dokončili všetky kroky.
6. Stiahnite si certifikát Azure Management do lokálneho priečinka vo vašom počítači a potom ho nahrajte na portál Azure Management Portal prechodom do časti **Nastavenia** > **Certifikáty pre správu**. Tento certifikát umožní spoločnosti LCS komunikovať s Azure vo vašom mene. Tento krok môžete preskočiť, ak má váš používateľ prístup k predplatnému.
7. Vyberte **Ďalej**.
8. Vyberte oblasť Azure, do ktorého chcete vykonať nasadenie a vyberte údajové centrum, ktoré je blízko miesta, kde plánujete tento systém používať.
9.  Vyberte možnosť **Pripojiť**.

Úspešne ste pripojili svoje predplatné služieb Azure. Teraz môžete nasadiť prostredia Dynamics 365 Finance hosťované na cloude.


