---
title: Splnenie všeobecných požiadaviek zdrojov
description: Táto téma poskytuje informácie o rezervácii pomenovaných zdrojov pre požiadavku na všeobecné zdroje.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897605"
---
# <a name="generic-resource-requirement-fulfillment"></a>Splnenie všeobecných požiadaviek zdrojov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Môžete rezervovať pomenovaný zdroj k výmene všeobecného zdroja, ktorý má zdrojovú požiadavku.

1. Na stránke **Projekty** vyberte kartu **Tím**.
2. Vyberte všeobecný zdroj, ktorý má zdrojovú požiadavku zo zoznamu a potom vyberte **Rezervovať**. Alebo otvorte zdrojovú požiadavku a potom vyberte **Rezervovať**.
3. Na stránke **Asistent plánovania** vyberte pomenovaný zdroj, ktorý chcete rezervovať do projektového tímu, a potom vyberte **Rezervovať**.

Po dokončení rezervácie a splnení pomenovaného zdroja sa všeobecný zdroj nahradí názvom zdroja.

Priradenia v pláne sú tiež aktualizované s názvom zdroja.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Naplnenie všeobecného zdroja s viacerými pomenovaniami zdrojov
Splnenie požiadavky na všeobecný zdroj s viacerými pomenovanými zdrojmi je podobné priradením jediného pomenovaného zdroja. Napríklad, je tam úloha s trvaním päť dní a 120 hodín úsilia. Túto úlohu nie je možné dokončiť jedným zdrojom, ktorý pracuje s typickým osemhodinovým dňom počas päťdňového týždňa. 

Požiadavka je 120 hodín inžinierstva robotiky počas piatich dní, čo je 24 hodín denne.

Toto je príklad, kedy sú potrebné viaceré pomenované zdroje na splnenie všeobecnej zdrojovej požiadavky. Budete musieť rezervovať viac zdrojov na splnenie požiadavky.

Hlavný rozdiel v tomto scenári je, že všeobecný zdroj zostáva priradený k tímovej úlohe a rezervované pomenované zdroje členov tímu nie sú priradené ako súčasť pozície. Projektový manažér môže priradiť prácu podľa zodpovedajúcich pomenovaných prostriedkov. Zobrazenie **odsúhlasenia** môže pomôcť projektovému manažérovi pri rozbití rezervácií naprieč viacerými zdrojmi na priradenie úlohy. To sa nerobí automaticky, pretože v každom scenári, ktorú je zložitejší ako jednoduchý príklad vyššie, ako napr. keď máte zväzok úloh, ktoré tvoria požiadavku alebo zámer, ako chce projektový manažér vykonať priradenie, je potrebné predpokladať systémovo. Vzhľadom k tomu, že systém nemôže pochopiť zámer, je pravdepodobné, že predpoklady budú iné, než je určené, a stane sa nesprávny alebo nepredvídateľný výsledok. Predvídateľný výsledok je, že všeobecný zdroj zostáva priradený, kým projektový manažér zámerne vytvorí úlohy, s pomocou zobrazenia **odsúhlasenia**.


