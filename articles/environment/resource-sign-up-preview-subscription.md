---
title: Registrácia na odber ukážky Project Operations pre scenáre zdrojov/chýbajúcich zdrojov
description: Táto téma poskytuje informácie o tom, ako sa prihlásiť na odber a nasadiť Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dc3b353f19b915f645aed91dc2a8127117027034
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121147"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Registrácia na odber ukážky Project Operations pre scenáre zdrojov/chýbajúcich zdrojov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma vysvetľuje, ako sa prihlásiť na odber ukážky/ponuky partnera a nasadiť prostredie Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.

## <a name="prerequisites"></a>Predpoklady

- Dostanete e-mail s pozvánkou na účasť v ukážke. O ukážku môžete požiadať na [webovej stránke Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Používateľ, ktorý nasadí ukážku, musí mať práva globálneho správcu nájomníka platformy Azure.
- Nasadenie finančného prostredia vyžaduje platné predplatné služieb Azure, ktoré sa bude fakturovať za každé prostredie. Na začiatok môžete použiť existujúce predplatné svojich organizácií alebo použiť [skúšobnú verziu Azure](https://azure.microsoft.com/en-us/free/). Prostredie CDS bude počas obmedzeného obdobia 30 dní poskytovaný zadarmo.

## <a name="subscribe"></a>Prihlásiť sa na odber

Keď je vaše schválenie [žiadosti o ukážku](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) schválené, dostanete e-mailom tri ponuky od spoločnosti Microsoft. Tieto ponuky vám umožňujú nasadiť ukážku Project Operations:

- Dynamics 365 Project Operations (CRM) – skúšobná verzia ukážky
- Office 365 Project Operations – skúšobná verzia ukážky
- Dynamics 365 Finance – skúšobná verzia

> [!IMPORTANT]
> Túto úlohu musí vykonať iba jedna osoba, správca nájomníka v organizácii. Ak nie ste predplatiteľom tohto vydania, počkajte, kým nebude zaregistrovaná vaša organizácia a kým dostanete svoje prihlasovacie údaje.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – skúšobná verzia ukážky 

Skôr ako začnete, uistite sa, že ste prihlásený do prehliadača s pracovným účtom používateľa v nájomníkovi, kde chcete zobraziť ukážku Project Operations.

1. Uplatnenie prvého kódu ponuky, **Dynamics 365 Project Operations (CRM) – skúšobná verzia ukážky** vložením do adresy URL prehliadača.

![Uplatniť ponuku](./media/16RedeemFirstOfferNew.png)

2. Potvrďte objednávku.

![Potvrďte objednávku](./media/17ConfirmOrderNew.png)

Uvidíte, že ponuka potvrdenia bola úspešne uplatnená.

![Potvrdenie](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – skúšobná verzia ukážky

Zopakujte rovnaké kroky ako pri prvom kóde ponuky. Nezabudnite pridať druhý kód ponuky pomocou rovnakého používateľského účtu, aký bol použitý s prvým kódom ponuky.

### <a name="dynamics-365-finance-preview-trial"></a>Skúšobná verzia ukážky Dynamics 365 Finance

Rovnaké kroky zopakujte aj pri poslednej ponuke z uvítacieho e-mailu.

## <a name="assign-licenses"></a>Priradenie licencií

> [!IMPORTANT]
> Na dokončenie nasledujúcich krokov budete potrebovať prístup správcu k portálu Microsoft 365 vo vašej organizácii.

1. Prejdite do [Centrum pre správu Microsoft 365](https://portal.office.com/) na pridelenie licencií vašim používateľom.

![Stránka správcu centra spravovania](./media/14AdminPortal.png)

2. Na stránke **Aktívni používatelia** vyberte používateľov, ktorým chcete priradiť licenciu.

![Priradenie licencií](./media/15AssignLicenses.png)

3. Overte, či licencia **Ukážka Dynamics 365 Project Operations (CRM)** a **Ukážka Office 365 Project Operations** boli vybraté a stlačte možnosť **Uložiť zmeny**.

> [!NOTE]
> Ponuku na vyskúšanie služby Finance nie je potrebné priradiť používateľovi.

## <a name="start-a-new-project-in-lcs"></a>Začatie nového projektu v LCS

Vytvorte nový projekt LCS podľa popisu v téme [Začatie nového projektu v LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Pridanie predplatného služieb Azure do projektu LCS

Pri dokončení tejto úlohy postupujte podľa pokynov v téme [Pridanie predplatného služieb Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Nasadenie ukážky prostredia Finance s Project Operations pre scenáre zdrojov/chýbajúcich zdrojov

Postupujte podľa pokynov v téme [Zriadenie nového prostredia](resource-provision-new-environment.md) na dokončenie nasadenia. Použite typ nasadenia [ukážkové prostredie](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) pre ukážku. 

## <a name="install-cds-setup-and-configuration-data"></a>Inštalácia údajov CDS pre nastavenie a konfiguráciu

Nainštalujte údaje pre nastavenie a konfiguráciu CDS podľa popisu v téme [Nastavenie a použitie konfiguračných údajov v Common Data Service](resource-apply-pro-setup-config-data.md).
Tento krok dokončite až po nasadení ukážkového prostredia Finance a pripravení ukážkových údajov v FO.
