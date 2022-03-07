---
title: Zobrazuje riadky cenovej ponuky založené na produkte.
description: Táto téma poskytuje informácie o riadkoch cenovej ponuky založenej na produkte.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: 3cc2e8788ea699b57ef75903ec3771f2e66fe867a9b8b6328a55b484eb13ede4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008605"
---
# <a name="product-based-quote-lines"></a>Zobrazuje riadky cenovej ponuky založené na produkte.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Môžete vytvoriť riadky cenových ponúk v Dynamics 365 Project Service Automation. Riadky cenových ponúk založené na produkte môžu byť riadky "Write-in" alebo môžu byť položkami z katalógu produktov.

## <a name="product-catalog"></a>Katalóg produktov

Produkty v katalógu produktov Dynamics 365 majú predvolenú jednotku a jednotkovú skupinu. Ak niekoľko produktov zdieľa rovnakú množinu atribútov, môžete vytvoriť produktovú rodinu, ktorá má tiež tieto atribúty. Všetky produkty v jednej produktovej rodine zdedia rovnakú množinu atribútov.

Spoločnosť napríklad predáva licencie na predplatné pre celý rad softvéru. Všetky predplatné softvéry májú nasledujúce dva atribúty:

- Počet používateľov 
- Trvanie predplatného (v mesiacoch)

Dobrým spôsobom, ako zachovať tento typ katalógu, je vytvorenie produktovej rodiny, ktorá je pomenovaná **predplatným softvérom**, a ktorá má **počet používateľov** a **trvanie predplatného** ako atribúty. Potom môžete pridať jednotlivé produkty, ako je napríklad **Dynamics 365 Sales** alebo **Dynamics 365 Field Service** do **predplatenej softvérovej** rodiny produktov.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Pridanie položiek katalógu produktov do projektovej ponuky

Projektová ponuka a strany projektovej zmluvy majú sekcie pre dva typy riadkov: riadky založené na projekte a založené na produkte. Pre riadky založené na produkte sa Dynamics 365 používa na pridávanie položiek z katalógu produktov do cenovej ponuky. Rozbaľovací zoznam v riadku cenovej ponuky alebo projektovej zmluvy obsahuje všetky produkty a jednotky v cenníku produktov, ktorý je priložený k cenovej ponuke alebo projektovej zmluve. Môžete tiež pridať produkty, ktoré nie sú súčasťou cenovej ponuky cenníka produktov.

Okrem toho môžete vybrať produkty z iných cenníkov, alebo môžete vybrať produkty priamo z katalógu produktov. Keď vyberiete produkty priamo z katalógu produktov, na získanie predajnej ceny produktu sa použije predvolený cenník daného produktu. Ak predvolený cenník nie je nastavený, cena je nastavená na hodnotu 0 (nula).

Ak je riadok cenovej ponuky založený na katalógu produktov, predajnú cenu môžete prepísať priamo v riadku cenovej ponuky. Všimnite si, že riadok cenovej ponuky v Dynamics 365 má **cenové** pole. K dispozícii sú dve hodnoty:

- Prepíšte cenu  
- Použite predvolenú hodnotu

Ak nastavíte toto pole na **prepísať ceny**, Dynamics 365 nenastaví predvolenú cenu. Musíte zadať cenu produktu v riadku cenovej ponuky. Ak nastavíte toto pole na **používať predvolené nastavenia**, Dynamics 365 použije predvolenú predajnú cenu a uzamkne pole, aby sa zabránilo úpravám.

Po nainštalovaní PSA sa predvolené predajné ceny zapisujú do riadkov na základe produktov v cenovej ponuke. Pole **ceny** sa potom nastaví na **prepísanie cien**, aby ste mohli upraviť predvolenú cenu v riadkoch cenovej ponuky.

> ![Nastavte prepisovanie cien.](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Množstvo faktorov pre výrobky

PSA používa množstvo faktorov na podporu predaja produktov založených na predplatnom. V prípade produktov založených na predplatnom sa množstvo v riadku cenovej ponuky alebo projektu vyjadrí ako počet používateľských mesiacov.

Zvyčajne je cena predplatného softvéru uložená v katalógu ako cena za používateľa mesačne. Avšak, môžete použiť iné časové popisy. Počas predajného procesu je cena v riadku cenovej ponuky zvyčajne cena za používateľa, za mesiac, ktorá bola dohodnutá a zľavnená agentom predaja IT. Každý obchod má iný počet užívateľov a iný počet predplatných mesiacov. Množstvo, ktoré sa používa na výpočet čiastky riadka cenovej ponuky, je produktom počtu používateľov a počtu mesiacov predplatného.

Na podporu tohto druhu predaja, PSA predstavil koncept kvantity faktorov. Množstvo faktorov sa spolieha na atribúty v Dynamics 365. Keď nakonfigurujete špecifické vlastnosti produktu, PSA vám umožní označiť podmnožinu týchto vlastností alebo všetky vlastnosti ako množstevné faktory.

PSA overuje, že iba číselné vlastnosti alebo vlastnosti produktu, ktoré majú číselný typ údajov, sú označené ako množstevné faktory. Ak je produkt, na ktorý sú nakonfigurované množstevné faktory, pridaný do riadka cenovej ponuky, pole **množstvo** v riadku cenovej ponuky sa stáva poľom iba na čítanie. Po zadaní hodnôt pre vlastnosti produktu, ktoré sú množstevné faktory, PSA vypočíta množstvo riadka cenovej ponuky.

Napríklad, Dynamics 365 môže mať nasledujúce vlastnosti: 

- **No of users** - Počet používateľov 
- **NO of Months** - Počet mesiacov predplatného
- **Produkt SKU** 

Vlastnosti **No of Users** a **No of Months** môžu byť označené ako množstevné faktory úpravou vlastnosti produktového riadka. 

> ![Označovanie No of Users a No of Months ako kvalitatívne faktory.](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]