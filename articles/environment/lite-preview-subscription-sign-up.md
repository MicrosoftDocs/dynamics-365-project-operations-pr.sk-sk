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
ms.openlocfilehash: 44edf2613ea4b26dadbd9edc47c784c488c577de
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290063"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrácia na odber ukážky – čiastočná 

Táto téma vysvetľuje, ako sa prihlásiť na odber ponuky verzie Preview partnera a čiastočne nasadiť Dynamics 365 Project Operations – dohoda o fakturácii pro forma.

> [!NOTE]
> Tento proces sa zmení v nadchádzajúcich vydaniach Project Operations.

## <a name="prerequisites"></a>Predpoklady

- Dostanete e-mail s pozvánkou na účasť v ukážke. O ukážku môžete požiadať na [webovej stránke Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Používateľ, ktorý nasadí ukážku, musí mať práva globálneho správcu nájomníka platformy Azure.
- Prečítajte si všetky zmluvné podmienky.

## <a name="subscribe"></a>Prihlásiť sa na odber

Keď dostanete schválenie [žiadosti o ukážku](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) dostanete e-mailom dve ponuky od spoločnosti Microsoft. Tieto ponuky vám umožňujú nasadiť ukážku Project Operations:

- Dynamics 365 Project Operations (CRM) – Skúšobná verzia
- Office 365 Project Operations – skúšobná verzia ukážky

> [!IMPORTANT]
> Túto úlohu musí vykonať iba jedna osoba, správca nájomníka v organizácii. Ak nie ste predplatiteľom tohto vydania, počkajte, kým nebude zaregistrovaná vaša organizácia a kým dostanete svoje prihlasovacie údaje.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – Skúšobná verzia 

Skôr ako začnete, uistite sa, že ste prihlásený do prehliadača s pracovným účtom používateľa v nájomníkovi, kde chcete zobraziť ukážku Project Operations.

1. Uplatnite prvý kód ponuky, **Dynamics 365 Project Operations (CRM) – Skúšobná verzia** vložením riadka s adresou URL prehliadača.

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

3. Overte si, či sú vybrané licencie **Verzia Preview aplikácie Dynamics 365 Project Operations (CRM)** a **Office 365 Project Operations – verzia Preview**. 
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]