---
title: Riadky faktúry dodávateľa pre míľniky
description: Táto téma vysvetľuje, ako vytvoriť riadky faktúry dodávateľa pre míľniky v subdodávke.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590641"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Riadky faktúry dodávateľa pre míľniky

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Faktúra dodávateľa v spoločnosti Microsoft Dynamics 365 Project Operations môže mať riadky faktúry dodávateľa pre míľniky, ktoré sú definované na riadku subdodávok. Projektoví manažéri môžu použiť riadky faktúry dodávateľa pre míľniky na zaznamenanie nákladov na služby, ktoré sú obstarané ako náklady založené na míľnikoch, ktoré vznikajú v súvislosti so službami alebo produktmi, ktoré sú obstarané pre projekt.

Riadky faktúry dodávateľa pre míľniky musia vždy odkazovať na riadok subdodávky, ktorý má spôsob fakturácie s pevnou cenou. Keď riadok faktúry dodávateľa pre míľniky odkazuje na riadok subdodávok, projektoví manažéri budú môcť porovnať a overiť základné náklady na čas, výdavky alebo materiály, ktoré odkazujú na daný riadok subdodávky, s míľnikom, ktorý fakturuje dodávateľ.

Nasledujúca tabuľka poskytuje informácie o poliach v riadkoch faktúry dodávateľa pre míľniky.

| Pole | Description | Funkčný vplyv |
| --- | --- | --- |
| Name | Názov riadku faktúry dodávateľa na uľahčenie identifikácie. | Tento názov sa zobrazí ako prvý stĺpec vo všetkých vyhľadávaniach, ktoré sú založené na riadkoch faktúry dodávateľa. |
| Description | Stručný popis služieb, ktoré sú fakturované dodávateľom v riadku faktúry dodávateľa. | None |
| Subdodávateľská zmluva | Subdodávateľská zmluva, na základe ktorej boli služby pôvodne objednané. | Keď je pre faktúru dodávateľa vybratá subdodávka, všetky riadky na faktúre dodávateľa zdedia tento výber. Faktúra dodávateľa nemôže obsahovať riadky faktúry dodávateľa, ktoré odkazujú na rôzne subdodávky. |
| Subdodávateľská linka | Subdodávateľská linka, na ktorej boli služby objednané. Zoznam riadkov subdodávok, ktoré je možné vybrať, je obmedzený na riadky vo vybranej subdodávke. | Keď sa v riadku faktúry dodávateľa pre míľniky vyberie riadok subdodávok, **Role** a **Kategória transakcie** polia a polia súvisiace s produktom sú irelevantné a nie sú dostupné. The **množstvo**, **a** **Skupina jednotiek** polia tiež nie sú relevantné pre riadky faktúry dodávateľa založené na míľnikoch. |
| Dátum transakcie | Dátum, kedy budú skutočné náklady riadku faktúry dodávateľa zaznamenané v projekte. | None |
| Trieda transakcie | Vyberte **Míľnik** na zaznamenanie faktúry dodávateľa za dokončený míľnik, ktorý bol definovaný na riadku subdodávok. | None |
| Medzník | Vyberte míľnik, ktorý je definovaný v príslušnom riadku subdodávky, ktorý je označený ako **Pripravené na fakturáciu**. | Míľniky subdodávateľskej linky, ktoré majú stav **Pripravené na fakturáciu** možno vybrať na riadku faktúry dodávateľa. |
| Project | Názov projektu, na ktorý sa použili fakturované služby. | Toto pole je povinné a nemôže zostať prázdne. |
| Úloha | Názov projektovej úlohy, na ktorú boli použité služby, ktoré sú fakturované. Toto pole je dostupné len vtedy, ak je vybratý projekt. Výber projektovej úlohy je voliteľný. | Ak toto pole ponecháte prázdne, projektový manažér môže priradiť riadok faktúry dodávateľa k triede transakcií v príslušnom riadku subdodávok, ktorý je zaznamenaný v ktorejkoľvek úlohe projektu. Ak riadok faktúry dodávateľa neodkazuje na riadok subdodávky a toto pole zostane prázdne, skutočné náklady vytvorené riadkom faktúry dodávateľa nebudú prepojené so žiadnymi skutočnými nevyfakturovanými predajmi. V tomto prípade, ak je nastavená fakturácia na základe úloh, nemusí byť možné náklady fakturovať koncovému zákazníkovi. |
| Suma medzníka | Zadajte hodnotu míľnika, ktorý je definovaný na riadku subdodávky, ktorý je pripravený na fakturáciu. | None |
| Daň z predaja | Zadajte sumu dane z predaja. | None |
| Celková suma | Celková suma riadku faktúry dodávateľa vrátane daní. Toto pole sa vypočíta ako *Míľniková čiastka* + *Daň z predaja*. | None |

> [!NOTE]
> Keď sa vytvorí riadok faktúry dodávateľa, ktorý odkazuje na míľnik v riadku subdodávok, stav míľnika subdodávok sa aktualizuje na **Faktúra dodávateľa bola vytvorená**. Potom, keď je táto faktúra dodávateľa potvrdená, stav míľnika riadku subdodávok sa aktualizuje na **Faktúra dodávateľa potvrdená**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
