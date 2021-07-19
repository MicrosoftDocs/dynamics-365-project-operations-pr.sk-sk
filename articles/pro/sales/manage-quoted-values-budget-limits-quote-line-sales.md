---
title: Prehľad riadkov cenových ponúk založených na projekte
description: Táto téma poskytuje informácie o používaní riadkov cenových ponúk založených na projekte pre projektovú úlohu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369890"
---
# <a name="project-based-quote-lines-overview"></a>Prehľad riadkov cenových ponúk založených na projekte 

_**Vzťahuje sa na:** Čiastočné nasadenie – dohoda o fakturácii pro forma, Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Riadky cenových ponúk založených na projekte sú navrhnuté tak, aby pomohli odhadnúť projektovú úlohu na zákazke. Štruktúra riadku cenovej ponuky založenej na projekte sa pre odhady projektu rozširuje o tieto koncepty:

- Spôsob fakturácie
- Mapovanie projektov a úloh
- Zahrnuté triedy transakcií
- Limit, ktorý sa nesmie prekročiť
- Nastavenie účtovateľnosti
- Odhad pomocou podrobností o riadku cenovej ponuky
- Zákazníci v riadkoch cenovej ponuky

Nasledujúca tabuľka poskytuje informácie o poliach na karte **Všeobecné** v riadku cenovej ponuky na základe projektu. Tieto polia pomáhajú vytvoriť základ pre podrobný a prízemných odhad projektovej úlohy.

| **Pole** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- |
| Meno | Názov riadka cenovej ponuky, ktorý vám pomôže identifikovať diskrétnu zložku cenovej ponuky, ktorá sa odhaduje. | Skopírované do riadku zmluvy o projekte, ktorý je vytvorený z tohto riadku cenovej ponuky po získaní ponuky. |
| Spôsob fakturácie | Pri cenovej ponuke vytvorenej z príležitosti sa táto hodnota skopíruje z príslušného poľa na riadka príležitosti. Toto pole obsahuje dva hlavné modely uzatvárania zmlúv podporované v aplikácii Dynamics 365 Project Operations:</br>- Pevná cena</br>- Čas a materiál.| Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná. |
| Project | Toto voliteľné pole použite na identifikáciu projektu, ktorý sa použije na vykonanie práce na tejto zákazke. Keď je projekt mapovaný na riadok cenovej ponuky, pomáha to pri nastavovaní účtovateľných úloh a tiež pri uvádzaní odhadu založeného na projekte k riadku cenovej ponuky ako podrobnosti o riadku cenovej ponuky. Ak projekt nie je mapovaný na riadok cenovej ponuky založenej na projekte, odhad by sa mal vytvoriť manuálne vytvorením podrobností o každom riadku cenovej ponuky. | Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.|
| Zahrnuté úlohy | Označuje, či sa tento riadok cenovej ponuky používa pre všetky alebo niektoré projektové úlohy vybratého projektu. Toto pole má nasledujúce možné hodnoty:</br>- Všetky projektové úlohy</br>- Iba vybraté projektové úlohy</br>Prázdna hodnota v tomto poli je ekvivalentná s možnosťou **Všetky projektové úlohy**. | Keď je na stránke projektu vybrané **Iba vybraté projektové úlohy**, karta **Nastavenie fakturácie úloh** vám umožňuje vybrať konkrétne úlohy a priradiť ich k tomuto riadku cenovej ponuky. Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná. |
| Zahrnúť čas | Hodnota **Áno**/**Nie** označuje, či budú časové transakcie alebo pracovné náklady na vybranom projekte zahrnuté do odhadu na tomto riadku cenovej ponuky. Hodnota **Nie** označuje, že časové transakcie alebo náklady na prácu nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky. Hodnota **Áno** označuje, že časové transakcie alebo náklady na prácu budú zahrnuté do odhadu v tomto riadku cenovej ponuky. | Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná. |
| Zahrnúť výdavok | Hodnota **Áno**/**Nie** označuje, či budú výdavkové náklady na vybranom projekte zahrnuté do odhadu na tomto riadku cenovej ponuky. Hodnota **Nie** označuje, že výdavkové náklady nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky. Hodnota **Áno** označuje, že výdavkové náklady budú zahrnuté do odhadu v tomto riadku cenovej ponuky. | Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná. |
| Zahrnúť materiál | Hodnota **Áno**/**Nie** označuje, či budú materiálové náklady na vybranom projekte zahrnuté do odhadu na tomto riadku cenovej ponuky. Hodnota **Nie** označuje, že materiálové náklady nebudú zahrnuté do odhadu na tomto riadku cenovej ponuky. Hodnota **Áno** označuje, že materiálové náklady budú zahrnuté do odhadu na tomto riadku cenovej ponuky. | Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná. |
| Zahrnúť poplatok | Hodnota **Áno**/**Nie** označuje, či budú poplatky na vybranom projekte zahrnuté do odhadu na tomto riadku cenovej ponuky. Hodnota **Nie** označuje, že poplatky nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky. Hodnota **Áno** označuje, že poplatky budú zahrnuté do odhadu v tomto riadku cenovej ponuky. | Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná. |
| Čiastka ponuky | Toto je suma, ktorá bude zákazníkovi ponúknutá za všetku predpokladanú prácu v tomto riadku cenovej ponuky. Pri cenovej ponuke vytvorenej z príležitosti sa táto hodnota skopíruje z poľa **Rozpočet zákazníka** na riadka príležitosti. Ak riadok cenovej ponuky založený na projekte obsahuje podrobnosti o riadku, toto pole je uzamknuté pre úpravy a je zhrnuté z čiastky v podrobnostiach riadka cenovej ponuky. | Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná. |
| Odhad dane | Toto je upraviteľné pole, kde môže používateľ pridať odhadovanú sumu dane pre riadok cenovej ponuky. Ak riadok cenovej ponuky založený na projekte obsahuje podrobnosti o riadku, toto pole je uzamknuté pre úpravy a je zhrnuté z čiastky daní v podrobnostiach riadka cenovej ponuky. | Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná. |
| Čiastka ponuky po zdanení | Toto pole predstavuje čiastku riadka cenovej ponuky po zdanení a je iba na čítanie. Čiastka v tomto poli sa počíta ako *Ponúknutá čiastka + daň*. | Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná. |
| Limit, ktorý sa nesmie prekročiť | Toto pole je upraviteľné a je k dispozícii iba pre riadky ponúk založené na projekte, ktoré majú spôsob účtovania **Čas a materiál**. | Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná. |
| Rozpočet zákazníka | Toto pole je upraviteľné a skopíruje sa z príslušného poľa v riadku príležitosti, ak bola cenová ponuka vytvorená z príležitosti. | Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Pravidlá overenia pre polia na karte Všeobecné v riadkoch cenových ponúk založených na projekte

**Pravidlo 1**: Ak je pole **Zahrnuté úlohy** prázdne alebo ak je nastavené na **Všetky projektové úlohy**, projekt je zahrnutý v riadku cenovej ponuky.

**Pravidlo 2**: Ak je pole **Zahrnuté úlohy** prázdne alebo ak je nastavené na **Všetky projektové úlohy**, projekt a určitú triedu transakcií je možné zahrnúť iba do jedného riadka cenovej ponuky založenej na projekte cenovej ponuky.

**Pravidlo 3**: Ak je pole **Zahrnuté úlohy** nastavené na **Iba vybrané projektové úlohy**, projekt a určitú triedu transakcií je možné zahrnúť do viacerých riadkov cenovej ponuky založenej na projekte cenovej ponuky.

**Pravidlo 4**: Ak má príležitosť viacero cenových ponúk, môžu existovať riadky cenových ponúk z rôznych cenových ponúk, ktoré všetky odkazujú na ten istý projekt a zahŕňajú rovnakú triedu transakcií.

**Pravidlo 5**: Ak cenové ponuky nepatria do rovnakej príležitosti, nemôžu obsahovať rovnakú triedu projektu a transakcie.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Príležitosť</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Ponuka</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Riadok cenovej ponuky</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Zahrnuté úlohy</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Zahrnúť čas</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Zahrnúť výdavok</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Zahrnúť materiál</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Zahrnúť</strong>
                </p>
                <p>
                    <strong>Poplatok</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Platný/neplatný</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Dôvod</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
Áno </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Porušenie pravidla č. 2. Čas, náklady a poplatky za projekt P1 sú zahrnuté v riadkoch cenových ponúk QL1 a QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
Áno </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Porušenie pravidla č. 2. Čas, materiál a poplatky za projekt P1 sú zahrnuté v riadkoch cenových ponúk QL1 a QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
Áno </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Platné </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Čas, materiál a poplatky za projekt P1 sú zahrnuté v QL1 <br>
Výdavky na projekt P1 sú zahrnuté v QL2 <br>
Žiadne prekrývanie toho, čo je obsiahnuté v každom riadku cenovej ponuky, a preto je platné.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Áno </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Iba vybraté úlohy </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
Áno </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Porušenie pravidla č. 2 </p>
                <p>
Q1 zahŕňa čas, materiál, výdavky a poplatky za podmnožinu úloh v projekte P1 </p>
                <p>
QL2 zahŕňa čas, výdavky a poplatky za celý projekt P1, a preto sa prekrýva s tým, čo je zahrnuté v Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
Áno </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Iba vybraté úlohy </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
Áno </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Platné </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Podľa pravidla č. 3 </p>
                <p>
Q1 zahŕňa čas, materiál, výdavky a poplatky za podmnožinu úloh v projekte P1.
                </p>
                <p>
QL2 zahŕňa čas, materiál, výdavky a poplatky za podmnožinu úloh v projekte P1.
                </p>
                <p>
Jediná ďalšie overenie je okolo podmnožiny úloh na QL1, ktorá sa líši od podmnožiny úloh QL2, aby sa zabezpečilo, že nedôjde k ich prekrývaniu. Vykonáva sa prostredníctvom systému, keď sú priradené úlohy.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Iba vybraté úlohy </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
Áno </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Všetky projektové alebo prázdne </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
Áno </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Platné </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Podľa pravidla č. 5 sú Q1 a Q2 dve cenové ponuky tej istej príležitosti, takže obidve môžu odhadnúť rovnaké komponenty projektu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Š2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Všetky projektové alebo prázdne </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
Áno </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Všetky projektové alebo prázdne </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
Áno </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Podľa pravidla č. 4 sú Q1 a Q2 dve cenové ponuky rôznych príležitostí, takže obidve nemôžu odhadnúť rovnaké komponenty toho istého projektu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Všetky projektové alebo prázdne </p>
            </td>
            <td width="45" valign="top">
                <p>
Áno </p>
            </td>
            <td width="46" valign="top">
                <p>
Áno </p>
            </td>
            <td width="43" valign="top">
                <p>
Áno </p>
            </td>
            <td width="41" valign="top">
                <p>
Áno </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
