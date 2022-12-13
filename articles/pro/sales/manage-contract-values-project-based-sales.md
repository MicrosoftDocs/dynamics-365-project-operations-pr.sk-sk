---
title: Prehľad projektových zmlúv
description: Tento článok poskytuje informácie o práci s riadkami projektovej zmluvy v Project Operations.
author: rumant
ms.date: 10/28/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f5a529233692a39b0674417cd4ea225e40243086
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824646"
---
# <a name="project-contract-lines-overview"></a>Prehľad projektových zmlúv

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Riadky zmluvy založené na projekte v Dynamics 365 Project Operations sú navrhnuté tak, aby uchovávali odhad a fakturačné dohody pre konkrétne komponenty projektovej úlohy na zákazke. Štruktúra riadka zmluvy založeného na projekte sa rozširuje pre odhady projektu a scenáre fakturácie s týmito konceptmi:

- Spôsob fakturácie
- Mapovanie projektov a úloh
- Zahrnuté triedy transakcií
- Limit, ktorý sa nesmie prekročiť
- Nastavenie účtovateľnosti
- Odhady pomocou podrobností riadku zmluvy
- Zákazníci v riadku zmluvy

Nasledujúca tabuľka obsahuje polia na karte **Všeobecné** riadkov zmlúv založených na projektoch, ktoré pomáhajú pripraviť základ pre podrobný, základný odhad a fakturačné podmienky pre prácu na projekte.

| Pole | Popis | Nadväzujúci vplyv |
| --- | --- | --- |
| **Názov** | Názov riadku zmluvy. Toto identifikuje samostatnú zložku zmluvy, ktorá sa odhaduje. Pri projektovej zmluve vytvorenej z cenovej ponuky sa táto hodnota skopíruje z príslušnej hodnoty riadku cenovej ponuky založeného na projekte. | Názov skopírovaný na riadok projektovej faktúry, ktorý je vytvorený z tohto riadku zmluvy pri vytváraní faktúry. |
| **Spôsob fakturácie** | V prípade projektovej zmluvy vytvorenej z cenovej ponuky sa táto hodnota skopíruje z príslušného poľa v riadku cenovej ponuky. Toto je množina možností, ktorá predstavuje dva hlavné modely uzatvárania zmlúv podporované aplikáciou Project Operations:</br>- **Pevná cena**</br>- **Čas a materiál** | Skutočná transakcia bude spracovaná na základe spôsobu fakturácie odkazovaného riadka zmluvy. Ak má riadok zmluvy, na ktorý odkazuje skutočná hodnota, časovú a materiálovú metódu fakturácie, vytvoria sa skutočné záznamy o nákladoch a nevyfakturovaných predajoch. Ak má riadok zmluvy, na ktorý odkazuje skutočná hodnota, spôsob fakturácie s pevnou cenou, vytvorí sa iba skutočná hodnota nákladu. |
| **Project** | Toto pole sa používa na identifikáciu projektu, ktorý sa použije na vykonanie práce na tejto zákazke. | Táto hodnota sa použije v spojení s položkami **Zahrnuté úlohy** a **Zahrnuté triedy transakcií** na vyriešenie odkazu na riadok zmluvy v skutočnom alebo odhadovanom riadku zmluvy. |
| **Zahrnuté úlohy** | Označuje, či tento riadok zmluvy obsahuje všetky projektové úlohy pre vybratý projekt alebo iba podmnožinu úloh. Toto je množina možností, ktorá má nasledujúce možné hodnoty:</br>- **Všetky projektové úlohy**</br>- **Iba vybraté projektové úlohy**. Prázdna hodnota v tomto poli sa rovná výberu možnosti **Všetky projektové úlohy**. | Ak je vybraté **Iba vybrané úlohy**, môžete vybrať konkrétne úlohy a priradiť ich k tomuto riadku zmluvy na karte **Nastavenie fakturácie úloh** na stránke **Projekt**. Hodnota sa použije v spojení s triedami **Projekt** a **Zahrnuté transakcie** na vyriešenie odkazu na riadok zmluvy na záznamu riadka so skutočnou alebo odhadovanou hodnotou. |
| **Zahrnúť čas** | Hodnota **Áno**/**Nie** označuje, či budú časové transakcie alebo pracovné náklady na vybranom projekte zahrnuté v tomto riadku zmluvy. Hodnota **Nie** označuje, že na tomto riadku zmluvy nebudú zahrnuté časové transakcie ani náklady na prácu. Hodnota **Áno** naznačuje, že budú. | Táto hodnota sa používa v spojení s projektom na vyriešenie referencie riadka zmluvy na skutočnom alebo odhadovanom zázname riadka. |
| **Zahrnúť výdavok** | Hodnota **Áno**/**Nie** označuje, či budú výdavkové náklady na vybranom projekte zahrnuté do odhadu na tomto riadku zmluvy. Hodnota **Nie** označuje, že na tomto riadku zmluvy nebudú zahrnuté nákladové výdavky. Hodnota **Áno** naznačuje, že budú. | Táto hodnota sa používa v spojení s projektom na vyriešenie referencie riadka zmluvy na skutočnom alebo odhadovanom zázname riadka. |
| **Zahrnúť materiály** | Hodnota **Áno**/**Nie** označuje, či budú materiálové náklady na vybranom projekte zahrnuté do odhadu na tomto riadku zmluvy. Hodnota **Nie** označuje, že materiálové náklady nebudú zahrnuté do tohto riadka zmluvy. Hodnota **Áno** naznačuje, že budú. | Táto hodnota sa používa v spojení s projektom na vyriešenie referencie riadka zmluvy na skutočnom alebo odhadovanom zázname riadka. |
| **Zahrnúť poplatok** | Hodnota **Áno**/**Nie** označuje, či budú poplatky na vybranom projekte zahrnuté do odhadu na tomto riadku zmluvy. Hodnota **Nie** označuje, že na tomto riadku zmluvy nebudú zahrnuté poplatky. Hodnota **Áno** naznačuje, že budú. | Táto hodnota sa používa v spojení s projektom na vyriešenie referencie riadka zmluvy na skutočnom alebo odhadovanom zázname riadka. |
| **Zmluvná suma** | Na riadku zmluvy s pevnou cenou je táto suma dohodnutou hodnotou, ktorá bude zákazníkovi fakturovaná za všetky pracovné komponenty spojené s týmto riadkom zmluvy. Na riadku zmluvy s časom a materiálom je táto suma odhadovanou hodnotou toho, čo bude zákazníkovi fakturované za všetky pracovné komponenty spojené s týmto riadkom zmluvy. V prípade projektovej zmluvy vytvorenej z cenovej ponuky sa táto hodnota skopíruje z príslušného poľa v riadku cenovej ponuky. Ak má riadok zmluvy založený na projekte podrobnosti riadku, toto pole je uzamknuté pre úpravy a je zosumarizované z čiastky v podrobnostiach riadku zmluvy. | Ak má riadok zmluvy podrobnosti o riadku, je možné túto hodnotu upraviť zmenou čiastok v detaile riadku. Na riadku zmluvy s pevnou cenou sa táto hodnota používa na generovanie sumy pred zdanením v periodických medzníkoch na fakturovanie. |
| **Odhad dane** | Používateľ môže toto pole upraviť a do riadku zmluvy vložiť predpokladanú sumu dane. Ak má riadok zmluvy založený na projekte podrobnosti riadku, toto pole je uzamknuté pre úpravy a je zosumarizované z čiastky dane v podrobnostiach riadku zmluvy. | Ak má riadok zmluvy podrobnosti o riadku, je možné túto hodnotu upraviť zmenou čiastok dane v podrobnostiach riadka. Na riadku zmluvy s pevnou cenou sa táto hodnota používa na generovanie dane v periodických medzníkoch na fakturovanie. |
| **Zmluvná suma po zdanení** | Suma v riadku zmluvy po zdanení. Toto pole je iba na čítanie a počíta sa ako **Zmluvná suma + daň**. | Na riadku zmluvy s pevnou cenou sa táto hodnota používa na generovanie periodických medzníkoch na fakturovanie. |
| **Limit, ktorý sa nesmie prekročiť** | Používateľ môže toto pole upravovať a je k dispozícii iba na riadkoch zmlúv založených na projektoch, ktoré majú metódu fakturácie nastavenú ako čas a materiál. | Používateľ môže toto pole upraviť. Keď skutočný čas a materiál odkazuje na tento riadok zmluvy pre čas a materiál, suma na skutočnom sa vyhodnotí oproti limitu na riadku zmluvy, ktorý sa nesmie prekročiť. Toto hodnotenie sa dokončí po zaúčtovaní už vynaložených a pridelených súm. |
| **Rozpočet zákazníka** | Toto pole sa dá upravovať a kopíruje sa zo zodpovedajúceho poľa na riadku cenovej ponuky, ak zmluva bola vytvorená z cenovej ponuky. | Toto pole slúži iba na informačné účely a nemá žiadny následný význam. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Pravidlá overenia možností na karte Všeobecné v riadkoch zmlúv založených na projektoch

Pravidlo 1: Ak je pole **Zahrnuté úlohy** prázdne alebo nastavené na **Všetky projektové úlohy**, všetky úlohy projektu sú zahrnuté v riadku zmluvy.

Pravidlo 2: Keď je pole **Zahrnuté úlohy** prázdne alebo výslovne nastavené na **Všetky projektové úlohy**, projekt a určitú triedu transakcií možno zahrnúť iba do jedného riadka zmluvy založenej na projekte v rámci zmluvy.

Pravidlo 3: Keď je pole **Zahrnuté úlohy** nastavené na **Iba vybraté projektové úlohy**, projekt a určitú triedu transakcií možno zahrnúť do viacerých riadkov zmluvy založenej na projekte v rámci zmluvy.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Zmluva</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Riadok zmluvy</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Zahrnuté úlohy</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Zahrnúť čas</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Zahrnúť výdavok</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Zahrnúť materiály</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Zahrnúť</strong>
                </p>
                <p>
                    <strong>Poplatok</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Platný/neplatný</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Dôvod</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Porušenie pravidla č. 2. Čas, náklady, materiály a poplatky za projekt P1 sú zahrnuté v oboch riadkoch zmluvy CL1 a CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Porušenie pravidla č. 2. Čas, materiály a poplatky za projekt P1 sú zahrnuté v oboch riadkoch zmluvy CL1 a CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Platné </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Čas, materiály a poplatky za projekt P1 sú zahrnuté v CL1.
                </p>
                <ul>
                    <li>
Výdavky na projekt P1 sú zahrnuté v CL2.
                    </li>
                </ul>
                <p>
Žiadne prekrývanie toho, čo je obsiahnuté v každom riadku zmluvy, a preto je platné.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Iba vybraté úlohy </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Porušenie pravidla č. 2 </p>
                <p>
C1 zahŕňa čas, materiály, výdavky a poplatky za podmnožinu úloh v projekte P1.
                </p>
                <p>
CL2 zahŕňa čas, , materiály, výdavky a poplatky za celý projekt P1, a preto sa prekrýva s tým, čo je zahrnuté v C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prázdna </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Iba vybraté úlohy </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Platné </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Podľa pravidla č. 3 </p>
                <p>
C1 zahŕňa čas, výdavky, materiály a poplatky za podmnožinu úloh v projekte P1.
                </p>
                <p>
CL2 zahŕňa čas, výdavky, materiály a poplatky za podmnožinu úloh v projekte P1.
                </p>
                <p>
Jediné ďalšie overenie je okolo podmnožiny úloh na CL1, ktorá sa líši od podmnožiny úloh CL2, aby sa zabezpečilo, že tu nedôjde k prekrývaniu. Vykonáva sa prostredníctvom systému, keď sú priradené úlohy.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Iba vybraté úlohy </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="48" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
            <td width="42" valign="top">
                <p>
Áno </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
