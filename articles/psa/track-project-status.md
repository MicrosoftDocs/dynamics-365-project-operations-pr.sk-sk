---
title: Sledovať stavu projektu
description: Ako na sledovanie stavu projektu v Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e9c8b594d468016264d0b4d9745597a35f55e50e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149607"
---
# <a name="track-a-projects-status-project-service"></a>Sledovanie stavu projektu (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Použite [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] na sledovanie pokroku projektu klienta.  

Počas procesu sa fázy projektu aktualizujú vzhľadom na priebeh:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Nové**    | Po vytvorení projektu sa fáza nastaví na **Nové**. Ak ste vytvorili projekt zo šablóny, v tejto fáze projektu môže mať plán, odhady a tím údajov. V opačnom prípade bude náčrt projektu a musíte ručne zadajte zvyšku komponentov projektu. |
|  **Ponuka**   |      Po spojení projektu a cenovej ponuky alebo jeho vytvorení z cenovej ponuky sa fáza projektu nastaví na **Cenová ponuka** a aktualizujú sa aj odhadovaný dátum začatia a ukončenia. Keď projekt je vo fáze cenová ponuka, podrobnosti cenovej ponuky sa zobrazia na karte **Predaj** stránky **projektu**.      |
|   **Plánovať**   |                                     Ak sa cenová ponuka priradená k projektu využije a proces sa dostane do fázy kontraktu, stav projektu sa aktualizuje na **Plán**. Podrobnosti zmluvy sa zobrazia na karte **Predaj** stránky **Projekt**.                                      |
| **Hotovo** |                    Po dokončení prác na projekte môžete jeho fázu prehodiť na **Dokončené**. Fáza dokončenia projektu predpokladá, že je práca hotová na 100 %, no projekt zostáva otvorený až do času, kým sa nezaznamenajú záznamy nákladov.                     |
|  **Zavrieť**   |           Keď všetky transakcie boli zaznamenané na projekte a už sa nemusí čakať na žiadny záznam, môžete manuálne nastaviť fázu **Zatvorený**. Ak je stav projektu **Zatvorený**, nemôžete doň zadávať žiadne ďalšie transakcie a projekt prechádza do stavu len na čítanie.           |

## <a name="to-track-a-projects-status"></a>Sledovanie stavu projektu  

1.  Prejdite na **Project Service > Projekty**.  

2.  Kliknite na projekt, na ktorom chcete pracovať.  

3.  Na paneli v hornej časti obrazovky zvoľte šípku ukazujúcu nadol vedľa názvu projektu a potom kliknite na **Sledovanie projektu**.  

4.  Vyberte **Sledovanie úsilia** alebo **sledovanie nákladov** v rozbaľovacom zozname nad zoznamom úloh.  

5.  Dvakrát kliknite na akúkoľvek úlohu, čím ju upravíte. Tiež môžete premiestniť alebo meniť veľkosť pruhy Ganttovho grafu na zmenu času a postupu úlohy.  

### <a name="see-also"></a>Pozrite si tiež:  
 [Príručka projektového manažéra](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]