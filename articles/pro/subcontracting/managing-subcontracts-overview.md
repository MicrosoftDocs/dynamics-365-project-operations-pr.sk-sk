---
title: Správa subdodávateľských zmlúv v aplikácii Project Operations
description: Tento článok poskytuje prehľad o komplexnom procese riadenia subdodávok zvyčajne v organizáciách založených na projekte.
author: rumant
ms.date: 09/14/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b2e4518f77b2099f9818ea56623be9efb20b01f4
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522345"
---
# <a name="subcontract-management-in-project-operations"></a>Správa subdodávateľských zmlúv v aplikácii Project Operations


_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok poskytuje prehľad o komplexnom procese riadenia subdodávok v projektových organizáciách. Subdodávky služieb sa spravidla riadia tokom obchodného procesu, ktorý je znázornený na nasledujúcom diagrame.

![Postup procesu subdodávateľských zmlúv](../media/SubcontractingProcessFlow.png)

Nasledujúci zoznam obsahuje podrobný popis procesu subdodávateľských zmlúv.

1. Projektový manažér vytvorí subdodávateľskú zmluvu s dodávateľom. Pre subdodávateľskú zmluvu sa štandardne používajú cenníky, ktoré sú pripojené k záznamu dodávateľa. Dodávateľský obchodný vzťah má typ vzťahu **Dodávateľ** alebo **Poskytovateľ**.
2. Projektový manažér môže všetky nákupy podrobne rozpísať ako riadkové položky v subdodávateľskej zmluve. Riadky subdodávateľskej zmluvy môžu byť pre čas, náklady alebo produkty. Trieda transakcie riadka subdodávateľskej zmluvy určuje, na čo je daný riadok určený.
3. Account manažér dodávateľa a projektový manažér môžu iterovať prostredníctvom subdodávateľskej zmluvy. Ceny možno upravovať v nákupných cenníkoch, ktoré sú pripojené k subdodávateľskej zmluve.
4. V tomto bode alebo neskôr v procese, ak je riadok subdodávateľskej zmluvy určený pre čas, account manažér dodávateľa spojí kontakty dodávateľa s každým riadkom subdodávateľskej zmluvy. Toto priradenie poskytuje informácie projektovému manažérovi, ktorý pracuje na subdodávateľskej zmluve. Keď je kontakt dodávateľa priradený k riadku subdodávateľskej zmluvy, systém automaticky vytvorí rezervovateľný zdroj z kontaktu, ak rezervovateľný zdroj ešte neexistuje.
5. Spôsob fakturácie na každom riadku subdodávateľskej zmluvy môže byť **Pevná cena** alebo **Čas a materiál**. V prípade riadkov subdodávateľských zmlúv s pevnou cenou sa nastaví plán faktúr založený na medzníkoch.
6.  Po nastavení subdodávateľskej zmluvy a dokončení vyjednávania sa potvrdí. Potvrdené subdodávateľské zmluvy nie je možné upravovať, ale ak dôjde k zmenám, je možné subdodávateľskú zmluvu „znova otvoriť pre úpravy“, ktorá nastaví stav zo stavu **Potvrdené** späť na **Koncept** a vyjednávanie je možné znova otvoriť. 
7.  Pri vytváraní generického člena tímu v projekte môže byť člen tímu priradený k riadku subdodávateľskej zmluvy. To naznačuje potrebu obsadiť generického člena tímu kapacitou subdodávateľa.
8.  Menovaní členovia tímu môžu byť buď vytvorení priamo na projekte, alebo vytvorení ich rezerváciou pomocou prostredia plánovania zdrojov. Ak je menovaný člen projektového tímu zmluvný pracovník, je možné to priradiť k riadku subdodávateľskej zmluvy. Tým sa zníži dostupná kapacita riadku subdodávateľskej zmluvy.
9.  Zdroje subdodávateľa môžu zaznamenávať čas, výdavky a využitie materiálu pri projektoch a projektových úlohách a potom ich odoslať na schválenie. U zamestnancov je to podobné. Pri zaznamenávaní času môže zmluvný pracovník vybrať konkrétnu subdodávateľskú zmluvu alebo riadok subdodávateľskej zmluvy.
10. Po schválení bude čas schválený subdodávateľmi zaznamenávať skutočné náklady na projekt na základe kúpnej ceny zmluvného pracovníka alebo roly, ktorú má v projekte.
11. Faktúry dodávateľa a položky v riadku faktúry dodávateľa môžu byť v systéme zaznamenané pre prácu vykonanú zdrojmi dodávateľa alebo produkty dodané dodávateľom. Riadky faktúry dodávateľa musia byť špecifické pre projekt a pre triedu transakcií čas, náklady, produkt/materiál, medzník alebo poplatok. Voliteľne môžu riadky faktúry dodávateľa odkazovať na riadok subdodávateľskej zmluvy.
12. Systém automaticky priradí všetky skutočné náklady, ktoré zodpovedajú riadku subdodávateľskej zmluvy a projektu, k faktúre dodávateľa. To uľahčí trojcestný proces párovania a overenia.
13. Projektový manažér potom môže skontrolovať automaticky spárované skutočné údaje o projekte, odstrániť alebo pridať ďalšie skutočné náklady na projekt a dokončiť proces overenia.
14. Dokončením procesu overenia na všetkých riadkoch bude faktúra dodávateľa označená ako **Pripravená na platbu**. V tejto etape je možné faktúru a riadky dodávateľa preniesť do systému účtovníctva alebo záväzkov na spracovanie platby dodávateľovi. Predtým zaznamenané náklady projektu budú stornované a skutočné náklady z riadku faktúry dodávateľa budú zaznamenané do projektu.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Riadky subdodávateľskej zmluvy založené na množstve a riadky subdodávateľskej zmluvy založené na práci

Riadok subdodávateľskej zmluvy môže byť založený na množstve alebo na práci. 

Keď je riadok subdodávateľskej zmluvy **založený na množstve**, množstvo nakupované na riadku subdodávateľskej zmluvy za čas, výdavok alebo materiál možno použiť na akýkoľvek projekt.

Keď je riadok subdodávateľskej zmluvy **založený na práci**, riadok subdodávateľskej zmluvy sa mapuje na súbor prác reprezentovaný uzlom v pláne projektu. Hodnota riadka subdodávateľskej zmluvy je súčtom všetkých komponentov, ktoré sú potrebné na dodanie tohto diela. Tieto sú modelované ako podrobnosti riadka subdodávateľskej zmluvy a môžu to byť kolekcie času, nákladov alebo materiálov. V prípade riadka subdodávateľskej zmluvy založenej na práci je riadok subdodávateľskej zmluvy taktiež vyhradený jednému projektu. Tieto typy subdodávok nie sú v súčasnosti podporované prevádzkou projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

