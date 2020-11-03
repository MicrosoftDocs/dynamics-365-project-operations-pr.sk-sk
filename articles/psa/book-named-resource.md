---
title: Rezervujte pomenované zdroje zo zdrojových požiadaviek.
description: Táto téma poskytuje informácie o rezervácii pomenovaných zdrojov pre požiadavku na všeobecné zdroje.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 20e3a904bc33360b194c0c53e58430c80d1ff55f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084569"
---
# <a name="book-named-resources-from-resource-requirements"></a>Rezervujte pomenované zdroje zo zdrojových požiadaviek.

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Môžete rezervovať pomenovaný zdroj k výmene všeobecného zdroja, ktorý má zdrojovú požiadavku.

1. V Project Service Automation (PSA) na stránke **projekty** kliknite na kartu **Tím**.
2. Vyberte všeobecný zdroj, ktorý má zdrojovú požiadavku zo zoznamu a potom kliknite na položku **rezervovať**. Alebo otvorte zdrojovú požiadavku a potom kliknite na položku **rezervovať**.


![Rezervácia všeobecného člena tímu](media/RM-how-to-14.png)


3. Na stránke **asistent plánovania** vyberte pomenovaný zdroj, ktorý chcete rezervovať do projektového tímu, a potom kliknite na položku **rezervovať**.

![Rezervácia všeobecného člena tímu pomocou Asistenta plánovania](media/RM-how-to-15.png)

Po dokončení rezervácie a splnení pomenovaného zdroja sa všeobecný zdroj nahradí názvom zdroja.

![Pomenovaný člen tímu nahrádza všeobecného člena tímu](media/RM-how-to-16.png)

Priradenia v pláne sú tiež aktualizované s názvom zdroja.

![Pomenovaný člen tímu priradený k úlohám projektu](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Naplnenie všeobecného zdroja s viacerými pomenovaniami zdrojov
Splnenie požiadavky na všeobecný zdroj s viacerými pomenovanými zdrojmi je podobné priradením jediného pomenovaného zdroja. Napríklad, je tam úloha s trvaním päť dní a 120 hodín úsilia. Túto úlohu nie je možné dokončiť jedným zdrojom, ktorý pracuje s typickým osemhodinovým dňom počas päťdňového týždňa. 

![Úloha, ktorá potrebuje 120 hodín úsilia počas piatich dní](media/RM-how-to-21.png)

Požiadavka je 120 hodín inžinierstva robotiky počas piatich dní, čo je 24 hodín denne.

![Denná požiadavka](media/RM-how-to-22.png)

Toto je príklad, kedy sú potrebné viaceré pomenované zdroje na splnenie všeobecnej zdrojovej požiadavky. Budete musieť rezervovať viac zdrojov na splnenie požiadavky.

![Rezervácia viacerých zdrojov na splnenie požiadavky.](media/RM-how-to-23.png)

Hlavný rozdiel v tomto scenári je, že všeobecný zdroj zostáva priradený k tímovej úlohe a rezervované pomenované zdroje členov tímu nie sú priradené ako súčasť pozície. Projektový manažér môže priradiť prácu podľa zodpovedajúcich pomenovaných prostriedkov. Zobrazenie **odsúhlasenia** môže pomôcť projektovému manažérovi pri rozbití rezervácií naprieč viacerými zdrojmi na priradenie úlohy. To sa nerobí automaticky, pretože v každom scenári zložitejšie ako jednoduchý príklad vyššie, ako keď máte zväzok úloh, ktoré tvoria požiadavku, zámer, ako chce projektový manažér priradiť, je potrebné systémovo predpokladať. Vzhľadom k tomu, že systém nemôže pochopiť zámer, je pravdepodobné, že predpoklady budú iné, než je určené, a stane sa nesprávny alebo nepredvídateľný výsledok. Predvídateľný výsledok je, že všeobecný zdroj zostáva priradený, kým projektový manažér zámerne vytvorí úlohy, s pomocou zobrazenia **odsúhlasenia**.


