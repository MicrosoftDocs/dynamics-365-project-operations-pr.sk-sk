---
title: Etapy projektu
description: Táto téma poskytuje informácie o etapách projektu, ktoré sú dostupné v Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b11c67ebd21fdf423eeae2db8154f26787c2e64f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897965"
---
# <a name="project-stages"></a>Etapy projektu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Etapy projektu slúžia na to, aby odrážali stav projektu, ktorý postupuje. Prispôsobenia sa dajú použiť na automatickú aktualizáciu etáp pomocou postupov obchodného procesu, Power Automate alebo rozšírení doplnkov.

Nasledujúce etapy sú definované v predvolenom toku obchodného procesu:

- Nový
- Ponuka
- Plán
- Doručiť
- Hotovo
- Zatvoriť 

## <a name="new"></a>Nový

Po vytvorení projektu sa fáza projektu nastaví na **Nové**. Ak bol projekt vytvorený zo šablóny, môže mať údaje o pláne, odhadovaní a tímových údajoch. V opačnom prípade je to obrys projektu a zostávajúce komponenty musia byť zadané.

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

