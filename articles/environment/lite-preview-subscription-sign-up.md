---
title: Registrácia na odber ukážky – čiastočná
description: Táto téma poskytuje informácie o tom, ako odoberať a nasadiť jednoduché nasadenie Project Operations – dohoda o fakturácii pro forma.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6f4360b7febab57b97df0776ef9148d2a38f16a7
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175910"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrácia na odber ukážky – čiastočná 

Táto téma vysvetľuje, ako sa prihlásiť na odber ponuky partnera ukážky a ako nasadiť jednoduché nasadenie Dynamics 365 Project Operations – dohodu o fakturácii pro forma.

> [!NOTE]
> Tento proces sa zmení v nadchádzajúcich vydaniach Project Operations.

## <a name="prerequisites"></a>Predpoklady

- Dostanete e-mail s pozvánkou na účasť v ukážke. O ukážku môžete požiadať na [webovej stránke Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Používateľ, ktorý nasadí ukážku, musí mať práva globálneho správcu nájomníka platformy Azure.
- Prečítajte si všetky zmluvné podmienky.

## <a name="subscribe"></a>Prihlásiť sa na odber

Keď dostanete schválenie [žiadosti o ukážku](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) dostanete e-mailom dve ponuky od spoločnosti Microsoft. Tieto ponuky vám umožňujú nasadiť ukážku Project Operations:

- Dynamics 365 Project Operations (CRM) – skúšobná verzia ukážky
- Office 365 Project Operations – skúšobná verzia ukážky

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

## <a name="assign-licenses"></a>Priradenie licencií

> [!IMPORTANT]
> Na dokončenie nasledujúcich krokov budete potrebovať prístup správcu k portálu Microsoft 365 vo vašej organizácii.


1. Prejdite do [Centrum pre správu Microsoft 365](https://portal.office.com/) na pridelenie licencií vašim používateľom.

![Stránka správcu centra spravovania](./media/14AdminPortal.png)

2. Na stránke **Aktívni používatelia** vyberte používateľov, ktorým chcete priradiť licenciu.

![Priradenie licencií](./media/15AssignLicenses.png)

3. Overte, či sú vybrané licencie **Ukážka Dynamics 365 Project Operations (CRM)** a **Office 365 Project Operations – ukážka**. 
4. Vyberte **Uložiť zmeny**.

## <a name="create-a-new-cds-environment"></a>Vytvorenie nového prostredia CDS

1. Poskytnite nové prostredie nasadenia Project Operations CDS podľa pokynov v téme [Model nasadenia CDS](lite-deployment.md). Keď vyberiete typ prostredia, nezabudnite použiť **Skúšobnú verziu (na základe predplatného)**.
![Nové prostredie](./media/19CreateEnvironment.png)

2. Vyberte nastavenie **Povoliť aplikácie Dynamics 365** a nechajte možnosť **Automaticky nasadiť tieto aplikácie** prázdnu.  
3. Výberom položky **Uložiť** vytvoríte prostredie.

![Pridať databázu](./media/20CreateEnvironment1.png)

4. Po vytvorení prostredia nainštalujte riešenie **Microsoft Dynamics 365 Project Operations**. 

![Inštalácia riešenia](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Nainštalujte ukážkové údaje konfigurácie a nastavenia CDS

Nainštalujte ukážkové údaje konfigurácie a nastavenia CDS podľa pokynov v téme [Použiť ukážkové údaje nastavenia a konfigurácie](lite-apply-demo-setup-config-data.md).
