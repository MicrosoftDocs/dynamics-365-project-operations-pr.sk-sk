---
title: Nastavenie šablón nákladov
description: Táto téma poskytuje informácie o tom, ako vytvoriť a používať šablóny nákladov v Project Operations.
author: sigitac
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 786b2b9b140f82d406044c2ed05761d7f46ee9e0
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642742"
---
# <a name="set-up-cost-templates"></a>Nastavenie šablón nákladov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_


Táto téma poskytuje informácie o tom, ako vytvoriť a používať šablóny nákladov v Project Operations. Šablóna nákladov určuje:

- Kategórie projektu pre prognózy a skutočné transakcie, ktoré sa majú zahrnúť do percenta výpočtu dokončenia projektu. Hodnota percenta dokončenia sa potom použije na výpočet výšky vykázaného výnosu.
- Či je možné percento dokončenia zmeniť, ak sa počíta automaticky.
- Či sa percento dokončenia počíta na základe súm alebo jednotiek.

## <a name="cost-template-example"></a>Príklad šablóny nákladov

Pracujete na projekte webových stránok pre zákazníka, v rámci ktorého si účtujete paušálny poplatok 10 000 USD. Predpokladáte, že dokončenie projektu bude trvať 100 hodín (5 000 USD). Predpovedáte tiež dve letenky a štyri noci v hoteli na cesty k zákazníkovi (1 800 USD). Výsledkom sú celkové predpokladané náklady 6 800 USD.

Keď na konci mesiaca spustíte proces rozpoznávania výnosov s pevnou cenou a vytvoríte odhad, zistíte, že ste na projekte odpracovali 35 hodín. To ešte nezahŕňa lety ani náklady na hotel. Tiež ste nechali asistenta vykonať päť hodín prieskumu projektu za cenu 100 USD, ktorý ste neplánovali.

Pri výpočte hodnoty percenta dokončenia pre tento projekt máte na výber z nasledujúcich možností:

- Chcete zahrnúť všetky náklady (hodiny a výdavky) alebo iba hodiny?
- Chcete zahrnúť všetky hodiny alebo iba plánované hodiny?
- Chcete vypočítať percento dokončenia na základe dolárových nákladov plánovaných hodín (5 000 USD) alebo iba na základe počtu hodín (100)?

Vaše odpovede na tieto otázky určujú možnosti, ktoré nastavíte v šablóne nákladov, a kategórie, ktoré vyberiete v riadkoch šablón nákladov.

Nasledujúca tabuľka ilustruje výsledky rôznych metód výpočtu hodnoty percenta úplnosti pre tento scenár.

| Dokončenie na základe | Dolárové náklady alebo jednotky | Dokončené (v percentách) | Výpočet |
| --- | --- | --- | --- |
| Všetky hodiny, bez výdavkov | Dolárové náklady | 37 % 35 × 50 USD + 100 USD = 1 850 USD 1 850 USD/5 000 USD |
| Všetky hodiny, bez výdavkov | Jednotky | 40 % | 40 hodín/100 hodín (vrátane piatich neplánovaných hodín) |
| Plánované hodiny, bez výdavkov | Dolárové náklady alebo jednotka | 35 % | 35/100 hodín alebo 35 × 50 USD/5 000 |
| Všetky hodiny a výdavky | Dolárové náklady | 27,2 % | 1 850 USD/6 800 USD+ |

Rozhodnutie, aký prístup zvoliť pri tvorbe šablóny nákladov, môže závisieť od niekoľkých úvah:

- Ak do šablóny nákladov zahrniete neplánované hodiny, riskujete, že sa projekt splní na 100 percent pred dokončením. Je to tak preto, lebo skutočné hodiny budú väčšie ako plánované hodiny. Ak použijete niektorú z prvých dvoch metód uvedených v tabuľke, mali by ste zmeniť plán (predpokladané jednotky), keď zistíte odchýlky. V takom prípade by ste pripočítali alebo odpočítali hodiny na základe svojich vedomostí o tom, čo je potrebné na dokončenie projektu. Ak bude realizácia projektu trvať ďalších 65 hodín, do plánu by ste pridali päť hodín, spolu teda 105 hodín. Ak viete, že váš asistent vykoná ďalších päť hodín výskumu, celkový súčet bude 110 hodín.
- Ak použijete tretiu metódu uvedenú v tabuľke, aktualizovali by ste iba plánované hodiny pre svoj čas, aby bol výpočet percentuálneho dokončenia presný. Keď sa zaregistrujú neplánované hodiny, vaša ziskovosť sa zmení, ale zostanete na známej trajektórii percentuálneho dokončenia.
- Ak použijete štvrtú metódu uvedenú v tabuľke, existuje riziko, že výdavky sa vyskytnú v nepravidelných časoch a nemusia sa prejaviť v postupe dokončenia. Preto, ak sú zahrnuté aj výdavky, môžu spôsobiť, že vaše percento dokončenia bude kolísať viac, ako je žiaduce. Napríklad preto, že ste ešte neleteli, bolo vaše percento dokončenia 27 percent namiesto 35 percent alebo 37 percent, ak ste mali výpočet založiť iba na čase. Keby ste podnikli jednu cestu na dve noci a presne predpovedali svoje letové a hotelové náklady, percento dokončenia by bolo 40,4 % (1850 USD za prácu a 900 USD za výdavky = 2750 USD/6800 USD = 40,4 %). Preto by vznik nákladov iba na jednu cestu lietadlom zmenil percento dokončenia z 27 na 40 %.

## <a name="create-cost-templates"></a>Vytvorenie šablón nákladov
Ak chcete vytvoriť šablóny nákladov, postupujte podľa týchto krokov:

1. Ak chcete pristupovať k šablónam nákladov, v prostredí Dynamics 365 Finance prejdite do **Projektový manažment a účtovníctvo** > **Nastavenie** > **Odhady** > **Šablóna nákladov**.
2. Ak chcete vytvoriť novú šablónu nákladov, zvoľte položku **Nová**. Zadajte názov a popis.
3. Uveďte identifikátor nákladového riadka pre každý typ transakcie.
4. Vyberte predvolenú metódu dokončenia:

  - **Automaticky**: Percento dokončenia sa pre projekt počíta automaticky. Výslednú hodnotu nemožno zmeniť.
  - **Ručne**: Percento dokončenia sa pre projekt počíta ručne. Výslednú hodnotu možno zmeniť.

  > [!NOTE]
  > Pre manuálne výpočty sa percento dokončenia udržuje v položke **Ručný výpočet** na karte **Všeobecné** na stránke **Odhad**.

5. V časti **Dokončenie na základe** vyberte jednu z nasledujúcich hodnôt:

  - **Čiastka**: Čiastka v účtovnej mene počíta percento dokončenia.
  - **Jednotka**: Množstvo počíta percento dokončenia.
  - **Priamka**: Systém vypočítava percento dokončenia na proporcionálnom základe pomocou dátumov začatia a ukončenia projektu na určenie dĺžky projektu.

6. Vyberte **Nákladové riadky** na kontrolu nákladových riadkov šablóny nákladov. Pre každý typ transakcie je potrebný aspoň jeden nákladový riadok. Môžete však vytvoriť viac nákladových liniek pre rovnaké typy transakcií a nastaviť pre tieto riadky požadované atribúty.
7. Na karte **Kategórie** vyberte kategórie projektu, ktoré sa majú zahrnúť do riadku šablón nákladov.
8. Na karte **Všeobecné** vyberte, či bude tento riadok zahrnutý do percenta výpočtu dokončenia.
9. Vyberte metódu nákladov na dokončenie, ktorá sa má použiť pri výpočte percenta dokončenia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]