---
title: Registrácia na odber ukážky Project Operations pre scenáre zdrojov/chýbajúcich zdrojov
description: Táto téma poskytuje informácie o tom, ako sa prihlásiť na odber a nasadiť Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949072"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Registrácia na odber ukážky Project Operations pre scenáre zdrojov/chýbajúcich zdrojov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma vysvetľuje, ako sa prihlásiť na odber ukážky/ponuky partnera a nasadiť prostredie Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.

## <a name="prerequisites"></a>Predpoklady

- Dostanete e-mail s pozvánkou na účasť v ukážke. O ukážku môžete požiadať na [webovej stránke Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Používateľ, ktorý nasadí ukážku, musí mať práva globálneho správcu nájomníka platformy Azure.
- Nasadenie finančného prostredia vyžaduje platné predplatné služieb Azure, ktoré sa bude fakturovať za každé prostredie. Na začiatok môžete použiť existujúce predplatné svojich organizácií alebo použiť [skúšobnú verziu Azure](https://azure.microsoft.com/en-us/free/). Prostredie CDS bude počas obmedzeného obdobia 30 dní poskytovaný zadarmo.

## <a name="subscribe"></a>Prihlásiť sa na odber

Keď je vaše schválenie [žiadosti o ukážku](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) schválené, dostanete e-mailom dve ponuky od spoločnosti Microsoft. Tieto ponuky vám umožňujú nasadiť ukážku Project Operations:

- Dynamics 365 Project Operations – skúšobná verzia ukážky
- Skúšobná verzia ukážky Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Túto úlohu musí vykonať iba jedna osoba, správca nájomníka v organizácii. Ak nie ste predplatiteľom tohto vydania, počkajte, kým nebude zaregistrovaná vaša organizácia a kým dostanete svoje prihlasovacie údaje.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – skúšobná verzia ukážky

1. Uplatnite prvú ponuku, **skúšobnú verziu Dynamics 365 Project Operations** s adresou URL uvedenou v uvítacom e-maile.

![Prvá ponuka](./media/1FirstOffer.png)

2. Skontrolujte, či ste prihlásený ako používateľ, ktorý patrí k organizácii, ktorá si predplatí službu.
3. Pokračujte v uplatnení ponuky. 
4. Vyberte **Áno, pridať do môjho účtu**.

![Uplatniť ponuku](./media/2RedeemFirstOffer.png)

![Potvrdiť ponuku](./media/3ConfirmFirstOffer.png)

![Ponuka uplatnená](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Skúšobná verzia ukážky Dynamics 365 Finance

Rovnaké kroky zopakujte aj pri druhej ponuke z uvítacieho e-mailu.

## <a name="assign-licenses"></a>Priradenie licencií

> [!IMPORTANT]
> Na dokončenie nasledujúcich krokov budete potrebovať prístup správcu k Office 365 vo vašej organizácii .

1. Prejdite na [Centrum pre správu Microsoft 365](https://portal.office.com/) na pridelenie licencií vašim používateľom.

![Portál na správu služieb Office](./media/5OfficeAdminPortal.png)

2. Na stránke **Aktívni používatelia** vyberte používateľov, ktorým chcete priradiť licenciu.

![Priradenie licencií](./media/6AssignLicenses.png)

3. Skontrolujte, či bola vybratá licencia Project Operations, a vyberte **Uložiť zmeny**. 

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

