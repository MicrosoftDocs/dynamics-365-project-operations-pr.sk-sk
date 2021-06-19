---
title: Režimy plánovania
description: Táto téma poskytuje informácie o režimoch plánovania.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116726"
---
# <a name="scheduling-modes"></a>Režimy plánovania

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_


Dynamics 365 Project Operations poskytuje organizáciám možnosť definovať, ako riadia zmeny kľúčových premenných v úlohách v rámci štruktúry rozdelenia práce. Na základe konkrétnych potrieb organizácie môžu projektoví manažéri po vytvorení projektu vykonať zmeny v režime plánovania.

V Project Operations sú k dispozícii tri režimy plánovania:

  - Pevné trvanie (toto je predvolený režim)
  - Fixné úsilie (*Práca*)
  - Pevné jednotky

Hodnoty ovplyvnené definíciou konkrétneho režimu plánovania sú určené nasledujúcim vzorcom:

  Úsilie = Trvanie x Jednotky

Keď definujete režim plánovania projektu, nastavujete jednu z týchto hodnôt, ktorú potom nemožno zmeniť. Udržiavanie tejto hodnoty ako konštanty dáva tejto hodnote prioritu, ktorá upozorní systém, aby ju nezmenil, keď sa zmenia ďalšie dve hodnoty. Nasledujúca tabuľka poskytuje informácie o vplyvoch výberu konkrétneho režimu.

| **V tejto úlohe**             | **Ak revidujete jednotky**   | **Ak revidujete trvanie** | **Ak revidujete úsilie**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Úloha Pevné jednotky     | Prepočíta sa trvanie. | Prepočíta sa úsilie.    | Prepočíta sa trvanie. |
| Úloha Pevné úsilie    | Prepočíta sa trvanie. | Prepočítajú sa jednotky.    | Prepočíta sa trvanie. |
| Úloha Pevné trvanie  | Prepočíta sa úsilie.   | Prepočíta sa úsilie.    | Prepočítajú sa jednotky.   |

Ďalšie informácie o vplyvoch daného režimu nájdete v časti [Zmena typu úlohy a spresnenie plánovania](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). V téme sa termín **Práca** používa namiesto termínu **Úsilie**.

## <a name="change-the-organizations-scheduling-mode"></a>Zmeňte režim plánovania organizácie

Vykonaním nasledujúcich krokov definujete režim plánovania organizácie.

1. Prejdite na **Nastavenia** \> **Všeobecné** \> **Parametre** a potom vyberte parameter projektu. 
2. Na stránke **Parametre projektu** vyberte predvolený režim plánovania pre organizáciu a potom definujte schopnosť projektového manažéra prepísať nastavenie pri vytváraní nového projektu.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Zmeňte nastavenie režimu plánovania na projekte

Ak organizácia umožňuje projektovému manažérovi prepísať predvolený režim plánovania, môže projektový manažér vykonať túto zmenu pri vytváraní nového projektu. Po uložení projektu sa však režim plánovania nedá zmeniť.

## <a name="copied-projects"></a>Skopírované projekty

Pretože sa projekt vytvorí, keď sa vykoná akcia kopírovania projektu, správca projektu nemôže nastaviť režim plánovania. Cieľový projekt bude vždy predvolený do režimu definovaného na úrovni organizácie.

## <a name="copied-tasks"></a>Skopírované úlohy

Keď sa úloha skopíruje z jedného projektu do druhého, dedí úlohu v režime plánovania cieľového projektu.
