---
title: Oceňovanie katalógu produktov
description: Táto téma poskytuje informácie o tom, ako funguje oceňovanie produktov v katalógu Dynamics 365 Project Service Automation (PSA).
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 59e05a55d41573b96785a2f41a7d5d822f6b515fb55edddea5ef1862b7694a1b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000190"
---
# <a name="product-catalog-pricing"></a>Oceňovanie katalógu produktov 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Cenníky a entity položiek cenníka podporujú oceňovanie katalógu produktov. Pre najväčšiu časť, sa táto funkcia používa pre linky založené na katalógu projektových cenových ponúk a projektových zmlúv.

Pre riadky založené na projekte, zmluva predstavuje dohodu po jej víťazstve. Keďže proces vyjednávania zvyčajne predchádza víťazstvu, ceny, ktoré sú pripojené k cenovej ponuke, sa vždy skopírujú ako sú do nového cenníka, priloženého k zmluve. Tento nový cenník nie je možné zmeniť mimo rozsahu zmluvy. Toto obmedzenie pomáha chrániť sadzbu karty, ktorá bola dohodnutá z akýchkoľvek cenových zmien, ktoré sa vyskytujú v hlavnom cenníku.

Produkty by mali byť nastavené tak, aby mali predvolené náklady a cenníky v katalógu produktov. Ak chcete konfigurovať predvolené náklady a cenník, musíte použiť cenu zoznamu, štandardnú cenu a aktuálnu cenu. Predvolený cenník sa používa v riadku cenovej ponuky alebo v riadku projektovej zmluvy iba vtedy, keď systém nemôže nájsť riadok cenníka pre daný produkt v cenovom zozname produktov pre cenovú ponuku alebo projektovú zmluvu.

Nákladová cena riadkov katalógu produktov sa môže zmeniť medzi cenovými ponukami. Táto schopnosť je dôležitá, pretože ak nechcete presne sledovať náklady, nemôžete určiť prevádzkové zisky na projektových angažmánoch. Predvolene sú štandardné náklady na produkt použíté ako obstarávacia cena. Predvolená cena však môže byť aktualizovaná v riadku cenovej ponuky, ak je pre túto cenovú ponuku odlišná cena.

## <a name="price-list-items"></a>Položky v cenníku

Produkty z katalógu produktov môžete pridať do rôznych cenníkov. Riadky cenníka pre produkty vždy odkazujú na konkrétnu jednotku. Ceny za produkt na položkách cenníka možno konfigurovať ako čiastku meny. Alternatívne môže byť nakonfigurovaný ako funkcia cenník, aktuálna cena, alebo štandardná cena.

PSA podporuje rôzne možnosti zaokrúhľovania, keď sú ceny nakonfigurované ako funkcia cenníka, štandardných nákladov alebo bežných nákladov. Okrem užívania viacerých cenových metód a možností zaokrúhľovania môžete priradiť zoznamy zliav k položkám cenníka. 

> ![Pridávanie produktov z katalógu produktov do rôznych cenníkov.](media/basic-guide-16.png)

Keď vytvoríte nový vlastný cenník pre cenovú ponuku výberom položky **vytvoriť vlastné ceny** na stránke **projektovej ponuky**, PSA vytvorí kópiu cenníka a pole **entita** v hlavičke nového cenníka je nastavené na **predajnú entitu**. Názov nového cenníka sa pripojí k názvu cenovej ponuky a časovej pečiatky. Môžete tiež použiť názov nového cenníka a názov cenovej ponuky vo vlastných pracovných postupoch na spustenie dodatočnej revízie a schválení cenových ponúk, ktoré používajú vlastné ceny.

 
## <a name="default-product-price-list"></a>Predvolený cenník produktov.
Každý záznam zákazníka má **predvolené pole cenníka**, kde môžete zadať cenník, ktorý zodpovedá mene zákazníka. V zariadení PSA sa v tomto poli automaticky nezadá predvolená hodnota. Ak existuje vlastná cenová zmluva s konkrétnym zákazníkom, môžete použiť toto pole na priradenie cenníka k danému zákazníkovi.

Príležitosti, cenová ponuka a pEntityrojektové zmluvy používajú nasledovný príkaz na zadanie predvolených cenníkov produktov. Rovnaká objednávka sa používa pre projektové cenníky.

1.  Cenová ponuka
2.  Príležitosť
3.  Zákazník
4.  Globálne nastavenia pre PSA

V predvolenom nastavení obsahuje pole **produkt** v riadku cenovej ponuky všetky aktívne produkty v cenníkoch produktov cenovej ponuky. Ak bol produkt inaktivovaný, alebo ak ide o koncept produktu, nie je uvedený v zozname, a to ani v prípade, že je v cenníku. 

Riadky katalógu produktov sa pridajú ako riadky faktúry na prvej faktúre vytvorenej pre projektovú zmluvu. V návrhu faktúry možno tieto riadky faktúry odstrániť. V takom prípade sa riadky zobrazia na nasledujúcej faktúre, až kým nebudú fakturované, alebo kým sa faktúra neodošle zákazníkovi. V PSA nie je možné fakturovať čiastočné množstvo riadka faktúry produktu. Po fakturácii riadkov produktov z projektovej zmluvy sa vytvoria skutočné hodnoty. Tieto skutočné hodnoty však nie sú prepojené s entitou súvisiaceho projektu. Inými slovami, riadky projektových zmlúv na základe produktu sú nezávislé od akýchkoľvek projektových použití. PSA nesleduje spotrebu materiálu na projektoch.


[!INCLUDE[footer-include](../includes/footer-banner.md)]