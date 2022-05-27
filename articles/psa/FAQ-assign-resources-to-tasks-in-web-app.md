---
title: Ako môžem priradiť rezervovateľný zdroj k úlohe vo webovej aplikácii
description: Prehľad spôsobov, ako môžete priradiť rezervovateľné zdroje.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 0aaf7f69fa8ae081a74fbc4f18014686f625661c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578865"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Ako priradiť prostriedok rezervovateľné úlohy vo webovej aplikácii (aplikácia Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Existujú dva spôsoby, ako priradiť prostriedok k úlohe v Project Service. Môžete rezervovať prostriedok ako člen tímu a potom ho priradiť k úlohe. Alebo môžete vytvoriť všeobecného člena tímu cez priradenie roly v úlohách, vytvoriť tím a následne splniť požiadavky na personál s pomenovaným zdrojom.

Upozorňujeme, že v prípade, ak chcete priradiť rezervovateľný zdroj k úlohe, rezervovateľný zdroj člena tímu musí mať dostatočne dostupné rezervácie. Stav rezervácie musí predstavovať typ potvrdenie Pevne rezervované a stav musí byť Potvrdené. Ak nie je k dispozícii dostatok rezervácií pre zdroj, Project Service odstráni priradenie a zobrazí nasledovné chybové hlásenie:

*Nie je možné priradiť prostriedok úlohe – nasledujúce zdroje nemajú dostatočný počet hodín zarezervovaný pre projekt*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervujte si prostriedok ako člen tímu a potom ho priradiť k úlohe.

S touto metódou pridať prostriedok do projektového tímu a potom priradiť úlohy na prostriedok v pláne projektu. Tu je, ako to urobiť:
1.  V mriežke člen tímu pridajte nového člena tímu stlačením možnosti **Nový**.
2.  Na obrazovke tím členských rýchle vytvorenie vyberte názov rezervovateľné prostriedku a nastaviť úlohu.
3.  Zvoľte dátumy **Od** a **Do**.

    > [!div class="mx-imgBorder"] 
    > ![Snímka obrazovky pridania člena tímu.](media/FAQ-Resources-to-Tasks2-1.png "Snímka obrazovky pridania člena tímu")
 
4.  Vyberte jednu z nasledujúcich metód prideľovania pre rezerváciu prostriedku:
    - **Plná kapacita** Táto metóda zarezervuje úplnú kapacitu zdroje pre stanovené dátumy od a do.
    - **Kapacita v percentách** zarezervuje zdroj pre percento kapacity zdroja pre stanovené dátumy od a do.
    - **Podľa rovnomerne rozmiestnených hodín** zarezervuje prostriedok pre stanovený počet hodín, ktoré rovnomerne rozdelí na dni v rámci stanovených dátumov od a do.
    - **Podľa hodín počiatočného vyťaženia** zarezervuje prostriedok pre stanovený počet hodín, v rámci počiatočného vyťaženia denných hodín v rámci stanovených dátumov od a do.

    Nestláčajte možnosť **Žiadne**, pretože sa tým zdroj pridá k tímu, no nevytvorí žiadne rezervácie, ktoré by využili kapacity zdroja.
5.  Vyberte **Uložiť**.

    Upozorňujeme, že hodiny rezervácie musia byť dostatočné na pokrytie hodín úsilia a rozsahov dátumov úlohy, ku ktorej tento zdroj priraďujete. Ak nie sú zosúladené, nemôžete priradiť zdroj k úlohe.

6.  Na štruktúre rozdelenia práce (WBS) úlohy kliknite na rozbaľovaciu ponuku bunky zdroja. Potom: 

    1. Stlačte možnosť **Pridať**.
    2. Stlačte rozbaľovaciu ponuku v časti **Zdroje** a potom označte člena tímu, ktorého ste pridali.
    3. Vyberte položku **OK**. Člen tímu je teraz priradený k úlohe.

    > [!div class="mx-imgBorder"] 
    > ![Snímka obrazovky pridania zdrojov pomocou WBS.](media/FAQ-Resources-to-Tasks2-2.png "Snímka obrazovky pridania zdrojov pomocou WBS")
 
Na mriežke člena tímu uvidíte súčet priradených hodín zdroja v časti Priradené hodiny. Hodnota bude menšia alebo rovná rezervovaným hodinám zdroja. 

> [!div class="mx-imgBorder"] 
> ![Snímka obrazovky priradených hodín pre zdroj.](media/FAQ-Resources-to-Tasks2-3.png "Snímka obrazovky priradených hodín pre zdroj")
 
V prípade, že úloha, ktorú sa pokúšate priradiť k zdroju začína po koncovom dátume rezervácie zdroja, zdroj sa v rozbaľovacej ponuke nezobrazí.

Všimnite si, že môžete priradiť prostriedok na viac hodín, než sú ich rezervované hodiny. Predpokladom je, aby zdroj ešte mal nepriradenú kapacitu. V tomto prípade bude zdroj len čiastočne priradený k svojim rezerváciám. Zostávajúce nepriradené hodiny úloh si môžete zobraziť pridaním stĺpca Počet hodín bez personálu k štruktúre rozdelenia práce.

Ak sú zdroje priradené k ich zarezervovaným hodinám (ich zarezervované hodiny sa rovnajú priradeným hodinám), zobrazí sa vám pri pokuse o priradenie ich budúcich akcií nasledovné chybové hlásenie:

*Nie je možné priradiť prostriedok úlohe – nasledujúce zdroje nemajú dostatočný počet hodín zarezervovaný pre projekt.*

Okrem toho predvolený správca členov projektového tímu ktorý sa pridáva do tímu pri vytváraní projektu je pridané bez spomínaného a nemožno priradiť ľubovoľnú úlohu. Nezobrazia sa v rozbaľovacej ponuke zdroja pre úlohy.

Ak chcete priradiť tento zdroj, musíte ich odstrániť z tímu a potom znova pridať metódu prideľovania, ktorá nebude mať príznak Žiadna. Dôvod ich pridania do tímu pri vytvorení projektu je ten, že projekt má predvolene aspoň jedného schvaľovateľa projektu.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Vytvorenie všeobecného člena tímu prostredníctvom priradenia roly k úlohám

Týmto spôsobom sa zaručí, že zdroje majú dosť rezervácie pre úlohy. Najprv vytvorte zástupný symbol alebo všeobecný zdroj, ktorý popisuje vlastnosti pomenovaného zdroja, ktorý chcete nakoniec priradiť k úlohám vytvorením tímu po priradení rol k úlohám. Tu je, ako to urobiť:

1. Na štruktúre rozdelenia práce označte úlohu.
2. V bunke zdroja zvoľte ikonu rozbaľovacej ponuky **Priradená rola**.
3. V rozbaľovacej ponuke stlačte možnosť **Rola** a vyberte si rolu pre všeobecný zdroj.
4. Vyberte položku **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Snímka obrazovky použitia WBS na pridanie zdroja.](media/FAQ-Resources-to-Tasks2-4.png "Snímka obrazovky použitia WBS na pridanie zdroja")
 
Po úspešnom dokončení rol priraďovania k úlohám vo WBS zvoľte možnosť **Generovať projektový tím**. Služba Project Service vytvorí minimálny počet všeobecných členov tímu na základe rol, zdrojových organizačných jednotiek a kalendára projektu sčítaním priradení úlohy.

> [!div class="mx-imgBorder"] 
> ![Snímka obrazovky generovania projektového tímu.](media/FAQ-Resources-to-Tasks2-5.png "Snímka obrazovky generovania projektového tímu")
 
Na mriežke členov tímu uvidíte zdroje všeobecného zdroja s rolou a názvom pozície. Ak sú dva zdroje potrebné pre rolu na dokončenie práce, funkcia všeobecného tímu vytvorí dvoch členov tímu a použije názov pozície, aby ich rozdelil.

> [!div class="mx-imgBorder"] 
> ![Snímka obrazovky pridania dvoch všeobecných zdrojov.](media/FAQ-Resources-to-Tasks2-6.png "Snímka obrazovky pridania dvoch všeobecných zdrojov")
 
Môžete si otvoriť záložné požiadavky zdroja pre všeobecného člena tímu stlačením odkazu v časti Požiadavka na zdroj.

> [!div class="mx-imgBorder"] 
> ![Snímka obrazovky otvorenia záložnej požiadavky na zdroj.](media/FAQ-Resources-to-Tasks2-7.png "Snímka obrazovky otvorenia záložnej požiadavky na zdroj")

Stlačte možnosť **Rezervovať** pre všeobecný zdroj a potom môžete použiť tabuľu plánovania na vyhľadanie a rezerváciu skutočného zdroja. Môžete tiež predložiť požiadavku na plnenie správcovi zdrojov stlačením možnosti **Odoslať žiadosť**.

Pri plnení všeobecného zdroja pomenovaným zdrojom sa všeobecný zdroj odstráni z tímu a priradenia úlohy pre všeobecný zdroj sa priradia k pomenovanému zdroju, ktorý vyplnil požiadavku na zdroj všeobecného zdroja.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
