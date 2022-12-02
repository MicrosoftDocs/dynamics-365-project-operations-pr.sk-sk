---
title: Registrácia na odber ukážky – čiastočná
description: Tento článok poskytuje informácie o tom, ako odoberať a nasadiť nasadenie Project Operations lite – dohoda o fakturácii pro forma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410095"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrácia na odber ukážky – čiastočná 

Tento článok vysvetľuje, ako sa prihlásiť na odber skúšobnej ponuky a nasadenia Dynamics 365 Project Operations Lite – dohoda o proforma fakturácii.

> [!NOTE]
> Tento proces sa zmení v nadchádzajúcich vydaniach Project Operations.

## <a name="prerequisites"></a>Predpoklady
- Používateľ, ktorý nasadí ukážku, musí mať práva globálneho správcu nájomníka platformy Azure. Nájomníka si môžete vytvoriť počas prvého uplatnenia ponuky.

> [!IMPORTANT]
> Túto úlohu musí vykonať iba jedna osoba, správca nájomníka v organizácii. Ak nie ste predplatiteľom tohto vydania, počkajte, kým nebude zaregistrovaná vaša organizácia a kým dostanete svoje prihlasovacie údaje.
> 
> Skúšobné verzie sú u nájomcu jednorazové. Skúšobnú verziu môžete spustiť iba raz. Na účely skúšobného obdobia vám odporúčame vytvoriť nového nájomcu.

### <a name="dynamics-365-project-operations-trial"></a>Skúšobná verzia Dynamics 365 Project Operations 

Skôr ako začnete, uistite sa, že ste prihlásený do prehliadača s pracovným účtom používateľa v nájomníkovi, kde chcete zobraziť ukážku Project Operations.

1. Prejdite na [Skúšobná verzia Project Operations](https://aka.ms/try-po) a uplatnite si prvý ponukový kód **Dynamics 365 Project Operations**.
2. Potvrďte objednávku.

  Uvidíte, potvrdenie, že ponuka bola úspešne uplatnená.

## <a name="assign-licenses"></a>Priradenie licencií

> [!IMPORTANT]
> Na dokončenie nasledujúcich krokov budete potrebovať prístup správcu k Microsoft 365 vo vašej organizácii .


1. Choďte do [centra spravovania Microsoft 365](https://portal.office.com/) a priraďte licencie svojim používateľom.
2. Na stránke **Aktívni používatelia** vyberte používateľov, ktorým chcete priradiť licenciu.
3. Overte, či je vybratá licencia **Dynamics 365 Project Operations**. 
4. Vyberte **Uložiť zmeny**.

## <a name="create-a-new-dataverse-environment"></a>Vytvorenie nového prostredia Dataverse

1. Poskytnite nové prostredie nasadenia Project Operations Dataverse podľa pokynov v článku [Model nasadenia Dataverse](lite-deployment.md). Keď vyberiete typ prostredia, nezabudnite použiť **Skúšobnú verziu (na základe predplatného)**.

  ![Nové prostredie.](./media/19CreateEnvironment.png)

2. Vyberte nastavenie **Povoliť aplikácie Dynamics 365** a nechajte možnosť **Automaticky nasadiť tieto aplikácie** prázdnu.  
3. Výberom položky **Uložiť** vytvoríte prostredie.

  ![Pridajte databázu.](./media/20CreateEnvironment1.png)

4. Po vytvorení prostredia nainštalujte riešenie **Microsoft Dynamics 365 Project Operations**. 

![Nainštalujte riešenie.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Nastavenie ukážkových údajov

Nastavte ukážkové údaje podľa pokynov v článku [Použitie ukážkových údajov nastavenia a konfigurácie](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
