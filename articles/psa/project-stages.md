---
title: Typy etapy projektu
description: Táto téma poskytuje informácie o etapách projektu.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7f893b5429dd61ae45ad9d536420c96b2f58605b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586869"
---
# <a name="project-stage-types"></a>Typy etapy projektu 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Etapy projektu slúžia na to, aby odrážali stav projektu, ktorý postupuje. Prispôsobenia sa dajú použiť na automatickú aktualizáciu etáp pomocou postupov obchodného procesu, Power Automate alebo rozšírení doplnkov.

Nasledujúce etapy sú definované v predvolenom BPF:

- Nová
- Ponuka
- Plánovať
- Doručiť
- Hotovo
- Zavrieť 

## <a name="new"></a>Nové

Po vytvorení projektu sa fáza projektu nastaví na **Nové**. Ak bol projekt vytvorený zo šablóny, môže mať údaje o pláne, odhadovaní a tímových údajoch. V opačnom prípade je to len obrys projektu a zostávajúce komponenty musia byť zadané.

## <a name="quote"></a>Cenová ponuka

Po spojení projektu a cenovej ponuky alebo jeho vytvorení z cenovej ponuky sa etapa projektu nastaví na **cenová ponuka** a odhadované dátumy začatia a ukončenia sú aktualizované. Keď je projekt vo fáze **cenovej ponuky**, podrobnosti cenovej ponuky sa zobrazia na karte **predaje** na stránke **entita projektu**.

## <a name="plan"></a>Plánovať

Ak vyhráte cenovú ponuku, ktorá je priradená k projektu a project je posunutý do fázy **zmluvy**, stav projektu sa aktualizuje na **plán**. Keď je projekt vo fáze **plánu**, podrobnosti zmluvy sa zobrazia na stránke **entita projektu**.

## <a name="deliver"></a>Doručiť

Keď je dokončený plán projektu, a ste pripravení na spustenie projektu, projektový manažér by mal aktualizovať fázu projektu na **dodať** aby ukázal, že projekt začal.

## <a name="complete"></a>Dokončené 

Keď je dokončená práca pre projekt, projektový manažér môže aktualizovať fázu na **dokončené**. Aktualizáciou fáze projektu na **dokončené**, projektový manažér naznačuje, že práca je 100-percentne dokončená, ale že projekt je stále otvorený tak, že všetky čakajúce časy alebo výdavkové položky môžu byť zaznamenané.

## <a name="close"></a>Zavrieť

Keď sú všetky transakcie zaznamenané pre projekt, projektový manažér môže aktualizovať fázu na **zatvorené**. V tomto momente nie je možné zaznamenať žiadne transakcie a projekt je nastavený iba na čítanie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
