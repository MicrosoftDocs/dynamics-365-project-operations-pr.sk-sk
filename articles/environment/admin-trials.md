---
title: Registrácia do skúšobných verzií Project Operations
description: Tento článok poskytuje informácie o tom, ako nasadiť skúšobnú verziu Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 7db7ea6b3cffe6eb43ee0519bbaccfc9092c9311
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959694"
---
# <a name="sign-up-for-project-operations-trials"></a>Registrácia do skúšobných verzií Project Operations 

_**Vzťahuje sa na:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma, Project Operations pre scenáre založené na zdrojoch/výrobe_ 



Tento článok vysvetľuje, ako sa prihlásiť na odber ukážkovej ponuky partnera a nasadiť a Dynamics 365 Project Operations životné prostredie.

Vďaka novej skúšobnej verzii Project Operations môžete automaticky nasadiť ktorýkoľvek z troch podporovaných scenárov nasadenia vyplnením dotazníka, ktorý odporúča najlepší prístup k nasadeniu. Tento článok poskytuje informácie o tom, ako:

- Uplatnenie skúšobnej ponuky.
- Inicializácia poskytovania prostriedkov.
- Konfigurácia duálneho zápisu.
- Ďalšie informácie o Project Operations. 

Nasledujúca tabuľka uvádza podrobnosti o novej skúšobnej ponuke.

| **Položka ponuky**               | **Podrobnosti**                                  |
|------------------------------|----------------------------------------------|
| Typ ponuky                   | Tento typ ponuky je vedený správcom, takže na uplatnenie je potrebný správca nájomníka. |
| Použitie ponuky                    | Jednorazová na nájomníka                          |
| Trvanie ponuky               | 30 kalendárnych dní                             |
| Uplatnenia na nájomníka       | 1                                            |
| Prípona                    | 1 rozšírenie, 30 kalendárnych dní               |
| Počet skúšobných prostredí | 3                                            |


## <a name="admin-trial-details"></a>Podrobnosti o skúšobnej verzii správcu
Nasledujúca tabuľka uvádza podrobnosti o skúšobnej verzii a ich použitie pre každý typ nasadenia.

| **Položka**                      | **Lite**                                     | **Neskladové materiály** | **Skladové materiály** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| K dispozícii sú údaje o nastavení           | Áno                                          | Áno                       | Áno (USSI)            |
| Transakčné údaje            | No                                           | No                        | No                    |
| Čas poskytnutia prostriedkov v minútach  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Predpoklady
Ak chcete nasadiť skúšobné verziu Dynamics 365 Project Operations, sú potrebné nasledovné predpoklady.

- Registrácia do [Dynamics 365 Project Operations – skúšobná verzia Preview](https://www.aka.ms/try-po).
- Používateľ, ktorý nasadí ukážku, musí mať práva globálneho správcu nájomníka platformy Azure.

> [!IMPORTANT]
> Túto úlohu musí vykonať iba jedna osoba v organizácii, správca nájomníka. Ak nie ste predplatiteľom tohto vydania, počkajte, kým nebude zaregistrovaná vaša organizácia a kým dostanete svoje prihlasovacie údaje.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations – skúšobná verzia Preview 

Predtým ako začnete, prihláste sa do prehliadača pomocou používateľského pracovného konta v nájomníkovi, kde chcete zobraziť verziu Preview Project Operations.

1. Uplatnite prvý kód ponuky, **Dynamics 365 Project Operations – skúšobná verzia Preview** vložením riadka s adresou URL prehliadača.

    ![Uplatniť ponuku](./media/16RedeemFirstOfferNew.png)

2. Potvrďte objednávku.

    ![Potvrďte objednávku](./media/17ConfirmOrderNew.png)

  Uvidíte potvrdenie, že ponuka bola úspešne uplatnená.

   ![Potvrdenie](./media/18OrderConfirmationNew.png)

  Budete presmerovaní do [centra spravovania Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Dotazník a poskytovanie prostriedkov

1.  Prejdite do [centra spravovania Power Platform](https://admin.powerplatform.com/projectoperationstrial) a vyplňte dotazník.  
2.  Skontrolujte odporúčaný typ nasadenia a vyberte **Spustiť inštaláciu** na spustenie poskytovania prostriedkov.
3.  Skontrolujte podmienky a požiadavky a potom vyberte **Spustiť**.

   Po spustení poskytovania prostriedkov budete presmerovaní na zoznam prostredí v centre spravovania Power Platform. Počas poskytovania prostriedkov je stav vášho prostredia **PreparingInstance**.
 
  Keď je zriaďovanie dokončené, stav vášho prostredia je **Pripravený**. Zabezpečenie prostredia zahŕňa nasadenie demo údajov.
 
4.  Vyberte príslušný Microsoft Dataverse URL a adresy URL aplikácií Finance and Operations na overenie nasadenia.

## <a name="configuring-dual-write"></a>Konfigurácia duálneho zápisu
- Ak chcete nakonfigurovať roly zabezpečenia pre duálny zápis, pozrite si časť [Aktualizujte nastavenia zabezpečenia v Project Operations v Dataverse](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse).
- Ak chcete získať prístup ku konfigurácii duálneho zápisu, prejdite na inštanciu financií a operácií a potom prejdite na **Správa údajov** > **Dvojité písanie**.
- Ak chcete nakonfigurovať mapy s dvojitým zápisom, pozrite si časť [Spustite Project Operations mapy s dvojitým zápisom](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Priradenie licencií

Na dokončenie nasledujúcich krokov budete potrebovať prístup správcu k Microsoft 365 vo vašej organizácii .

1. Choďte na [Microsoft 365 centrum spravovania](https://portal.office.com/) na pridelenie licencií vašim používateľom.

   ![Stránka správcu centra spravovania](./media/14AdminPortal.png)

2. Na stránke **Aktívni používatelia** vyberte používateľov, ktorým chcete priradiť licenciu.

   ![Priradenie licencií](./media/15AssignLicenses.png)

3. Overte, či bola vybratá licencia **Dynamics 365 Project Operations verzia Preview** a potom vyberte **Uložiť zmeny**.

## <a name="additional-resources"></a>Ďalšie zdroje

Nasledujúce zdroje poskytujú užitočné rady na začiatku cesty s Project Operations:

- [Seriál videí – Prehľad Project Operations, podrobné preskúmanie funkcií a plán](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Určenie typu nasadenia](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Najčastejšie otázky

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Čo ak potrebujem ALM alebo ELM pre svoje prostredie aplikácií pre financie a operácie?

- Partnerov, ktorí vyžadujú úplné možnosti správy životného cyklu prostredia, nájdete v dokumente [Žiadosť o licenciu izolovaného priestoru partner](https://experience.dynamics.com/requestlicense), kde môžete preskúmať novú partnerskú ponuku. 
- Partnerov, ktorí hľadajú viac informácií o právach na interné použitie, nájdete v dokumente [Práva na interné použitie v cloude a softvérové výhody (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Môžem si skúšobnú dobu predĺžiť nad 30 dní?
Ak si chcete skúšobnú verziu predĺžiť, vykonajte nasledujúce kroky.

1. V **Microsoft 365 Admin Center**, ísť do **Fakturácia** > **Vaše produkty**.
2. Vyberte **Dynamics 365 Project Operations (CE) – skúšobná verzia Preview**.
3. Pod položkou **Dátum uplynutia platnosti** vyberte **Predĺžiť dátum**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Môžem inovovať z čiastočného nasadenia na nasadenie založené na zdrojoch/neskladovaných zdrojoch?
V súčasnej dobe neexistuje podpora na inováciu prostredia z čiastočného nasadenia na nasadenie založené na neskladovaných zdrojoch.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Môžem získať prístup k službám Lifecycle Services (LCS) pre svoje finančné prostredia?  
Nie. V prípade týchto skúšobných verzií je nasadenie riešené prostredníctvom centra spravovania Power Platform. Prístup do finančného prostredia je obmedzený.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Môžem si skúšobnú verziu nainštalovať do existujúceho prostredia?
Ak máte existujúce prostredie, bude vám dovolené nainštalovať čiastočné nasadenie do existujúceho predajného prostredia Dataverse z centra spravovania Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
