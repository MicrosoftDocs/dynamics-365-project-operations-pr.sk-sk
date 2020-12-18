---
title: model zabezpečenia,
description: Táto téma poskytuje informácie o modeli zabezpečenia v Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b01f3d88dd021895933bc863b762f019ae50eed6
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642922"
---
# <a name="security-model"></a>Model zabezpečenia

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations obsahuje jedinečný bezpečnostný model, ktorý umožňuje obchodný bezpečnostný model založený na rolách, ktorý spolupracuje so skupinami Microsoft Office. 


## <a name="security-roles"></a>Roly zabezpečenia
Medzi funkcie klientskeho rozhrania Project Operations patria nasledujúce roly:

| Rola                          | Popis                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Správca postupov              | Podporuje medziprojektové vykazovanie.                                                                                                            | Organizačná jednotka              |
| Schvaľovateľ projektu              | Schvaľuje čas a náklady spojené s projektom.                                                                                                                              | Organizačná jednotka |
| Správca fakturácie projektu | Vytvorí návrh faktúry.                                                                                                                                                 | Organizačná jednotka |
| Projektový manažér               | Vytvorí plán projektu a požiada o zdroje.                                                                                                                              | Organizačná jednotka |
| Projektový zdroj              | Členovia tímu, ktorých je možné rezervovať a nahlásiť čas.                                                                                                          | Organizačná jednotka|
| Správca zdrojov              | Všetky funkcie správy zdrojov, ako napríklad plnenie požiadaviek na zdroje a rezervácie, sú oddelené tak, aby podporovali hybridnú konfiguráciu projektového manažéra + manažéra zdrojov a jednu a centralizovanú rolu správcu zdrojov. | Organizačná jednotka |


Microsoft Project for the Web obsahuje nasledujúce roly:

| Rola           | Popis                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Používateľ projektu   | Spoločný používateľ projektu, ktorý je schopný vytvárať vlastné projekty a prezerať si všetky zdieľané projekty. | Používateľ   |
| Systém projektu | Úloha použitá v kontexte aplikácie. Zákazníci by nemali používať túto rolu systému.                                    | Globálne |

## <a name="security-enforcement"></a>Presadzovanie bezpečnosti
Akcie, ktoré sa vykonávajú na úrovni projektu, sa vykonávajú v kontexte prihláseného používateľa. To znamená, že na vytvorenie, otvorenie alebo odstránenie projektu sa vyžaduje, aby mal používateľ k dispozícii prístup do CDS. Prístup do CDS je možné poskytnúť prostredníctvom ktoréhokoľvek z možných mechanizmov zahrnutých do platformy. Napríklad, používateľ s väčším rozsahom môže mať prístup k projektu alebo ak bola vykonaná explicitná akcia zdieľania projektu, ktorá používateľovi umožňuje prístup.

Je dôležité, aby sa to vzalo do úvahy pri vytváraní projektov v Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Moderná skupinová spolupráca s Project Operations
Project for the Web a Project Operations podporujú moderné skupiny pre spoluprácu. Používatelia pridaní do projektu prostredníctvom skupiny môžu upravovať plán projektu.

Project for Web pridáva používateľov do skupiny automaticky po priradení.

Skupiny poskytujú povolenia na spoločnú prácu na projekte a podporné artefakty spolupráce. Nasledujúci diagram zobrazuje udalosti a zmeny stavu, ku ktorým dôjde počas procesu skupinového priradenia.

Project Operations nevytvára skupinu prostredníctvom implicitnej akcie a robí to iba prostredníctvom explicitnej akcie tlačiacich skupín.

Vyhľadávanie členov skupiny v dialógovom okne **Správa skupín** je obmedzené na tých, ktorí sú nastavení ako súčasť skupiny zabezpečenia prostredia. Ďalšie informácie nájdete v sekcii [Riadenie prístupu používateľov k prostrediam: skupiny zabezpečenia a licencie](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Skupinový režim](./media/groupsmode.png)

1. Projekt je vytváraný a vlastnený tvoriacim používateľom.
2. Vlastník projektu je aktualizovaný v tíme.
3. Tím vlastníka je namapovaný na zadanú alebo vytvorenú skupinu Office.
4. Pôvodný vlastník projektu je pridaný do skupiny Office.

## <a name="deployment-recommendation"></a>Odporúčanie pre nasadenie
S vývojom modelu skupinovej spolupráce Office bude pridaná funkčnosť, ktorá poskytne podrobnejšiu kontrolu v priebehu času. Zákazníkom, ktorí v súčasnosti nasadia Project Operations, sa odporúča, aby sa zamerali na tradičný model zabezpečenia Microsoft Dynamics 365.

Ďalšie informácie nájdete v sekcii [Zabezpečenie v Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Zabezpečenie Project Operations a Microsoft Dynamics 365 Finance
Project Operations zahŕňa tieto roly:

- Projektový manažér
- Projektový účtovník

Ďalšie informácie o zabezpečení vo Finance nájdete v časti [Zabezpečenie na základe roly](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


