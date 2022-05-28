---
title: Registrácia na odber ukážky – čiastočná
description: Táto téma poskytuje informácie o tom, ako odoberať a nasadiť jednoduché nasadenie Project Operations – dohoda o fakturácii pro forma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3b06ac29e8021967490534d3aefc8b5ce733413b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588019"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrácia na odber ukážky – čiastočná 

Táto téma vysvetľuje, ako sa prihlásiť na odber skúšobnej ponuky a nasadenia Dynamics 365 Project Operations Lite – dohoda o proforma fakturácii.

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


1. Ísť do [Microsoft 365 centrum spravovania](https://portal.office.com/) na pridelenie licencií vašim používateľom.
2. Na stránke **Aktívni používatelia** vyberte používateľov, ktorým chcete priradiť licenciu.
3. Overte, či je vybratá licencia **Dynamics 365 Project Operations**. 
4. Vyberte **Uložiť zmeny**.

## <a name="create-a-new-dataverse-environment"></a>Vytvorenie nového prostredia Dataverse

1. Poskytnite nové prostredie nasadenia Project Operations Dataverse podľa pokynov v téme [Model nasadenia Dataverse](lite-deployment.md). Keď vyberiete typ prostredia, nezabudnite použiť **Skúšobnú verziu (na základe predplatného)**.

  ![Nové prostredie.](./media/19CreateEnvironment.png)

2. Vyberte nastavenie **Povoliť aplikácie Dynamics 365** a nechajte možnosť **Automaticky nasadiť tieto aplikácie** prázdnu.  
3. Výberom položky **Uložiť** vytvoríte prostredie.

  ![Pridajte databázu.](./media/20CreateEnvironment1.png)

4. Po vytvorení prostredia nainštalujte riešenie **Microsoft Dynamics 365 Project Operations**. 

![Nainštalujte riešenie.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Nainštalujte ukážkové údaje konfigurácie a nastavenia CDS

Nainštalujte ukážkové údaje konfigurácie a nastavenia CDS podľa pokynov v téme [Použiť ukážkové údaje nastavenia a konfigurácie](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
