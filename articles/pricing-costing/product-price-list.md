---
title: Cenníky produktov
description: Táto téma poskytuje informácie o cenníkoch v katalógových cenách používaných pre projektové cenové ponuky a zmluvy.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 02d274725983e50adc35a4cae1ac60c35be346a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004955"
---
# <a name="product-price-lists"></a>Cenníky produktov

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

 V Project Operations **Cenníky produktov** a súvisiace entity položiek cenníka podporujú funkciu určovania cien produktov na základe riadkov produktových cenových ponúk a zmlúv. Pri produktoch použitých v projektoch sa používajú záznamy položiek v cenníku pre cenníky projektov. 

Produkty by mali byť nastavené tak, aby mali predvolené náklady a cenníky v katalógu produktov. Ak chcete konfigurovať predvolené náklady a cenník, použite cenník, štandardné náklady a obstarávaciu cenu. Predvolený cenník sa používa v riadku cenovej ponuky alebo v riadku projektovej zmluvy iba vtedy, keď systém nemôže nájsť riadok cenníka pre daný produkt v cenovom zozname produktov pre cenovú ponuku alebo projektovú zmluvu.

Nákladová cena riadkov katalógu produktov sa môže zmeniť medzi cenovými ponukami. Táto schopnosť je dôležitá, pretože ak nechcete presne sledovať náklady, nemôžete určiť prevádzkové zisky na projektových angažmánoch. Predvolene sú štandardné náklady na produkt použíté ako obstarávacia cena. Predvolená cena však môže byť aktualizovaná v riadku cenovej ponuky, ak je pre túto cenovú ponuku odlišná cena.

## <a name="price-list-items"></a>Položky v cenníku

Produkty z katalógu produktov môžete pridať do rôznych cenníkov. Riadky cenníka pre produkty vždy odkazujú na konkrétnu jednotku. Ceny za produkt na položkách cenníka možno konfigurovať ako čiastku meny. Alternatívne môže byť nakonfigurovaný ako funkcia cenník, aktuálna cena, alebo štandardná cena.

Funkcia určovania cien podporuje rôzne možnosti zaokrúhľovania, keď sú ceny produktov nakonfigurované ako funkcia cenníka, štandardných nákladov alebo aktuálnych cien. Okrem užívania viacerých cenových metód a možností zaokrúhľovania môžete priradiť zoznamy zliav k položkám cenníka. 

 
## <a name="default-product-price-list"></a>Predvolený cenník produktov.
Každý záznam zákazníka má **predvolené pole cenníka**, kde môžete zadať cenník, ktorý zodpovedá mene zákazníka. V tomto poli sa automaticky nezadá predvolená hodnota. Ak existuje vlastná cenová zmluva s konkrétnym zákazníkom, môžete použiť toto pole na priradenie cenníka k danému zákazníkovi.

Príležitosti, cenová ponuka a pEntityrojektové zmluvy používajú nasledovný príkaz na zadanie predvolených cenníkov produktov. Rovnaká objednávka sa používa pre projektové cenníky.

1.  Ponuka
2.  Príležitosť
3.  Zákazník
4.  Globálne nastavenia 

V predvolenom nastavení obsahuje pole **produkt** v riadku cenovej ponuky všetky aktívne produkty v cenníkoch produktov cenovej ponuky. Ak bol produkt inaktivovaný, alebo ak ide o koncept produktu, nie je uvedený v zozname, a to ani v prípade, že je v cenníku. 

Riadky katalógu produktov sa pridajú ako riadky faktúry na prvej faktúre vytvorenej pre projektovú zmluvu. V návrhu faktúry možno tieto riadky faktúry odstrániť. V takom prípade sa riadky zobrazia na nasledujúcej faktúre, až kým nebudú fakturované, alebo kým sa faktúra neodošle zákazníkovi. Nie je možné fakturovať čiastočné množstvo riadka faktúry produktu. Po fakturácii riadkov produktov z projektovej zmluvy sa vytvoria skutočné hodnoty. Tieto skutočné hodnoty však nie sú prepojené s entitou súvisiaceho projektu. Inými slovami, riadky projektových zmlúv na základe produktu sú nezávislé od akýchkoľvek projektových použití. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
