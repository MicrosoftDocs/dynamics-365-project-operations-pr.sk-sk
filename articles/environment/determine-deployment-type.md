---
title: Určenie typu nasadenia
description: Táto téma poskytuje informácie, ktoré vám pomôžu určiť správny typ nasadenia Project operations pre vašu spoločnosť.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 280578b2710a0bccd1973b51b062fef7a2997780
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584155"
---
# <a name="determine-your-deployment-type"></a>Určenie typu nasadenia

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

> [!IMPORTANT]
> Po zakúpení licencie začnite tu, aby ste určili najlepší model nasadenia aplikácie Dynamics 365 Project Operations pomocou [riadeného postupu inštalácie](https://aka.ms/provisionprojectoperations).
> Po dokončení postupu riadenej inštalácie budete presmerovaní na správny portál na riadenie, aby ste dokončili inštaláciu. Dokončite inštaláciu podľa podrobností nasadenia.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Existujúci zákazníci systému Dynamics používajú Dynamics 365 Project Service Automation
Project Operations obsahuje funkcie dodávané s Project Service Automation. Pre týchto zákazníkov bude vydaný aktualizačný postup v 1. vlne vydaní na rok 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Existujúci zákazníci Dynamics 365 Finance využívajúci riadenie projektov a účtovníctvo 

Existujúci zákazníci aplikácie Financie, ktorí používajú funkciu Projektový manažment a účtovníctvo, ju môžu naďalej používať tak, ako je. Pozrite si [Project Operations pre scenáre využívajúce skladované materiály/výrobné objednávky](#pma).


## <a name="deployment-regions"></a>Oblasti nasadenia
Informácie o tom, ktoré oblasti podporujú nasadenie aplikácie Project Operations, nájdete v [správe Geografická dostupnosť pre Dynamics 365 a Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Vyberte položku **Zobraziť zostavu** a rozbalením ponuky **Dynamics 365 > Prevádzkové aplikácie >Dynamics 365 Project Operations** zobrazíte podporované regióny.

## <a name="deployment-types"></a>Typy nasadenia
Project Operations podporuje viac možností nasadenia, aby zodpovedali vašim požiadavkám. Či už ste novým alebo existujúcim zákazníkom Dynamics 365, Project Operations môže podporiť vaše potreby.

Náš [Dotazník o nasadení](https://aka.ms/provisionprojectoperations) vám pomôže určiť správne nasadenie. Výsledky vás prevedú jedným z nasledujúcich typov nasadenia:

- [Čiastočné nasadenie – dohoda o fakturácii pro forma](#lite)
- [Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek](#integrated)
- [Project Operations pre scenáre využívajúce skladované materiály/výrobné objednávky](#pma)

Project Operations podporuje scenáre využívajúce skladované materiály/výrobné objednávky a neskladové scenáre/scenáre založené na zdrojoch v rovnakom prostredí prostredníctvom konfigurácií na úrovni právnických osôb. Spoločnosť Contoso môže napríklad využiť možnosti skladovaných materiálov/výrobných objednávok vo svojom výrobnom závode v USA (právnická entita = Contoso Manufacturing United States). Spoločnosť Contoso môže využívať možnosti neskladovaných položiek/zdrojov vo svojom servisnom stredisku Contoso Robotics Arms vo Veľkej Británii (právnická entita = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Jednoduché nasadenie – dohoda o fakturácii pro forma

Jednoduché nasadenie zahŕňa nasledujúce možnosti:

- Proces predaja pre projekty, ktoré rozširujú možnosti aplikácie Dynamics 365 Sales
- Plánovanie projektu pomocou programu Microsoft Project for the Web
- Viacrozmerné ceny
- Jednotná správa zdrojov
- Sledovanie času
- Základné výdavky
- Fakturácia pro forma pre kontrolu a úpravy projektového manažéra 

#### <a name="deployment-steps"></a>Postup nasadenia
Určte najlepší model nasadenia Project Operations pomocou [Dotazníka o nasadení](https://aka.ms/provisionprojectoperations).

Toto nasadenie je popísané v časti [Registrácia na odber ukážky](lite-preview-subscription-sign-up.md) a [Zriadenie nového prostredia](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek
Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek zahŕňa nasledujúce možnosti:
 
- Proces predaja pre projekty, ktoré rozširujú aplikáciu Dynamics 365 Sales
- Plánovanie projektu pomocou programu Microsoft Project for the Web
- Viacrozmerné ceny
- Jednotná správa zdrojov
- Sledovanie času
- Základné výdavky
- Úplný výdavok
- Potvrdenie autorizácie vrátenia tovaru
- Fakturácia pro forma a fakturácia orientovaná na zákazníka 
- Priznanie výnosov pre projekty

#### <a name="deployment-steps"></a>Postup nasadenia
Určte najlepší model nasadenia Project Operations pomocou [Dotazníka o nasadení](https://aka.ms/provisionprojectoperations).

Toto nasadenie je popísané v časti [Registrácia na odber ukážky](resource-sign-up-preview-subscription.md) a [Zriadenie nového prostredia](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations pre scenáre využívajúce skladované materiály/výrobné objednávky

- Plánovanie projektu pomocou štruktúry WBS
- Správa zdrojov
- Sledovanie času
- Úplný výdavok
- Potvrdenie autorizácie vrátenia tovaru
- Úplné účtovanie
- Priznanie výnosov
- Výrobné zákazky
- Podpora skladovaných materiálov s inventárom

#### <a name="deployment-steps"></a>Postup nasadenia
Určte najlepší model nasadenia Project Operations pomocou [Dotazníka o nasadení](https://aka.ms/provisionprojectoperations).

Toto nasadenie je popísané v časti [Registrácia na odber ukážky](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) a [Zriadenie nového prostredia](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]