---
title: Registrácia na odber ukážky Project Operations pre scenáre zdrojov/chýbajúcich zdrojov
description: Táto téma poskytuje informácie o tom, ako sa prihlásiť na odber a nasadiť Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9094b6928c5c276a40166ef5d8cb0facb539685b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575829"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Registrácia na odber ukážky Project Operations pre scenáre zdrojov/chýbajúcich zdrojov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_



Táto téma vysvetľuje, ako sa prihlásiť na odber skúšobnej ponuky a nasadiť prostredie Project Operations pre scenáre založené na zdrojoch/také, ktoré nie sú na sklade.

## <a name="prerequisites"></a>Predpoklady
- Používateľ, ktorý nasadí ukážku, musí mať práva globálneho správcu nájomníka platformy Azure. Nájomníka si môžete vytvoriť počas prvého uplatnenia ponuky. 
- Nasadenie finančného prostredia vyžaduje platné predplatné služieb Azure, ktoré sa bude fakturovať za každé prostredie. Na začiatok môžete použiť existujúce predplatné svojich organizácií alebo použiť [skúšobnú verziu Azure](https://azure.microsoft.com/free/). Prostredie CDS bude počas obmedzeného obdobia 30 dní poskytovaný zadarmo.

> [!IMPORTANT]
> Túto úlohu musí vykonať iba jedna osoba, správca nájomníka v organizácii. Ak nie ste predplatiteľom tohto vydania, počkajte, kým nebude zaregistrovaná vaša organizácia a kým dostanete svoje prihlasovacie údaje.
> 
> Skúšobné verzie sú u nájomcu jednorazové. Skúšobnú verziu môžete spustiť iba raz. Na účely skúšobného obdobia vám odporúčame vytvoriť nového nájomcu.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - skúšobná verzia Preview 

Skôr ako začnete, uistite sa, že ste prihlásený do prehliadača s pracovným účtom používateľa v nájomníkovi, kde chcete zobraziť ukážku Project Operations.

1. Uplatnite prvý kód ponuky **Dynamics 365 Project Operations** tu [Skúšobná verzia Project Operations](https://aka.ms/try-po).
2. Potvrďte objednávku.

  Uvidíte, že ponuka potvrdenia bola úspešne uplatnená.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance ukážková skúšobná verzia

Prejdite do [Skúšobná verzia Preview Dynamics 365 for Finance](https://aka.ms/trypoche) a zopakujte kroky z predchádzajúcej časti s ponukou, prihláste sa do prostredia hosťovaného v cloude.  

## <a name="assign-licenses"></a>Priradenie licencií

> [!IMPORTANT]
> Na dokončenie nasledujúcich krokov budete potrebovať prístup správcu k Microsoft 365 vo vašej organizácii .

1. Ísť do [Microsoft 365 centrum spravovania](https://portal.office.com/) na pridelenie licencií vašim používateľom.

2. Na stránke **Aktívni používatelia** vyberte používateľov, ktorým chcete priradiť licenciu.

3. Overte, či bola vybratá licencia **Dynamics 365 Project Operations** a stlačte možnosť **Uložiť zmeny**.

> [!NOTE]
> Ponuku na vyskúšanie služby Finance nie je potrebné priradiť používateľovi.

## <a name="start-a-new-project-in-lcs"></a>Začatie nového projektu v LCS

Vytvorte nový projekt LCS podľa popisu v téme [Začatie nového projektu v LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Pridanie predplatného služieb Azure do projektu LCS

Pri dokončení tejto úlohy postupujte podľa pokynov v téme [Pridanie predplatného služieb Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Nasadenie ukážky prostredia Finance s Project Operations pre scenáre zdrojov/chýbajúcich zdrojov

Postupujte podľa pokynov v téme [Zriadenie nového prostredia](resource-provision-new-environment.md) na dokončenie nasadenia. Použite typ nasadenia [ukážkové prostredie](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) pre ukážku. 

## <a name="install-cds-setup-and-configuration-data"></a>Inštalácia údajov CDS pre nastavenie a konfiguráciu

Nainštalujte údaje pre nastavenie a konfiguráciu CDS podľa popisu v téme [Nastavenie a použitie konfiguračných údajov v Common Data Service](resource-apply-pro-setup-config-data.md).
Tento krok dokončite až po nasadení ukážkového prostredia Finance a pripravení ukážkových údajov.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
