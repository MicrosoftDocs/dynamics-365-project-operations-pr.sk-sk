---
title: Etapy projektu
description: Táto téma poskytuje informácie o etapách projektu.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755560"
---
# <a name="project-stages"></a>Etapy projektu 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Etapy projektu sa aktualizujú, aby odrážali stav projektu, ktorý prebieha. Predvolený tok obchodného procesu automaticky aktualizuje niektoré etapy projektu, zatiaľ čo iné sú manuálne aktualizované projektovým manažérom. 

Nasledujúce etapy sú definované v predvolenom BPF:

- Nové
- Cenová ponuka
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
