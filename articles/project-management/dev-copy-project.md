---
title: Vytváranie šablóny projektu pomocou funkcie kopírovania projektu
description: Tento článok poskytuje informácie o tom, ako vytvoriť šablóny projektu pomocou vlastnej akcie Kopírovať projekt.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923851"
---
# <a name="develop-project-templates-with-copy-project"></a>Vytváranie šablóny projektu pomocou funkcie kopírovania projektu

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations podporuje schopnosť kopírovať projekt a vrátiť všetky priradenia späť k všeobecným zdrojom, ktoré zastupujú danú rolu. Zákazníci môžu pomocou tejto funkcie zostaviť základné šablóny projektu.

Keď vyberiete **Kopírovať projekt**, aktualizuje sa stav cieľového projektu. Použite **Dôvod stavu** na určenie, kedy je akcia kopírovania dokončená. Výberom možnosti **Kopírovať projekt** sa aktualizuje aj počiatočný dátum projektu na aktuálny počiatočný dátum, ak sa v entite cieľového projektu nezistí žiadny cieľový dátum.

## <a name="copy-project-custom-action"></a>Vlastná akcia kopírovania projektu

### <a name="name"></a>Name 

msdyn\_ CopyProjectV3

### <a name="input-parameters"></a>Vstupné parametre

Existujú tri vstupné parametre:

- **ReplaceNamedResources** alebo **ClearTeamsAndAssignments** – Nastavte iba jednu z možností. Nenastavujte oboje.

    - **\{"ReplaceNamedResources": true\}** – Predvolené správanie pre operácie projektu. Všetky pomenované zdroje sú nahradené všeobecnými zdrojmi.
    - **\{"ClearTeamsAndAssignments": pravda\}** – Predvolené správanie pre Project for the Web. Všetky úlohy a členovia tímu sú odstránené.

- **Zdrojový projekt** – Odkaz na entitu zdrojového projektu, z ktorého sa má kopírovať. Tento parameter nemôže byť nulový.
- **Cieľ** – Odkaz na entitu cieľového projektu, do ktorého sa má kopírovať. Tento parameter nemôže byť nulový.

Nasledujúca tabuľka poskytuje súhrn troch parametrov.

| Parameter                | Type             | Hodnota                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **Pravda** alebo **Nepravdivé** |
| ClearTeamsAndAssignments | Boolean          | **Pravda** alebo **Nepravdivé** |
| SourceProject            | Odkaz na entitu | Zdrojový projekt    |
| Target                   | Odkaz na entitu | Cieľový projekt    |

Ďalšie predvolené hodnoty akcií nájdete v časti [Použite akcie webového rozhrania API](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Validácie

Vykonajú sa nasledujúce overenia.

1. Null kontroluje a získava zdrojové a cieľové projekty, aby potvrdil existenciu oboch projektov v organizácii.
2. Systém overí, či je cieľový projekt platný na kopírovanie, overením nasledujúcich podmienok:

    - Neexistuje žiadna predchádzajúca aktivita na projekte (vrátane výberu **Úlohy** kartu) a projekt sa vytvorí nanovo.
    - Neexistuje žiadna predchádzajúca kópia, v tomto projekte nebol požadovaný žiadny import a projekt nemá a **Nepodarilo sa** postavenie.

3. Operácia nie je volaná pomocou HTTP.

## <a name="specify-fields-to-copy"></a>Zadajte polia, ktoré chcete kopírovať

Po vyvolaní akcie bude funkcia **Kopírovať projekt** prehľadávať zobrazenie projektu **Kopírovať stĺpce projektu** na určenie, ktoré polia sa majú kopírovať pri kopírovaní projektu.

### <a name="example"></a>Príklad

Nasledujúci príklad ukazuje, ako zavolať na **CopyProjectV3** vlastná akcia s **removeNamedResources** súbor parametrov.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
