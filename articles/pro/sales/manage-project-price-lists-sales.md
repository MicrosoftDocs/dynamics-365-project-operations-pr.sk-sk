---
title: Správa projektových cenníkov v projektových cenových ponukách – čiastočné
description: Táto téma poskytuje informácie o práci s cenníkmi projektov v cenových ponukách. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ff830c63f7acf4cc23ac75d44afa9c3553b8724
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176000"
---
# <a name="manage-project-price-lists-on-project-quotes---lite"></a>Správa projektových cenníkov v projektových cenových ponukách – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Cenové ponuky projektu sú navrhnuté tak, aby podporovali cenníky s účinnosťou viacerých dátumov predaja. V Dynamics 365 Project Operations bola pridaná nová pridružená entita **Cenníky projektu**. Táto entita má vzťah 1 k mnohým pre cenovú ponuku projektu.

Cenníky projektu sa používajú na ocenenie časových a výdavkových transakcií projektu. Ak má cenová ponuka jeden alebo viac cenníkov projektu, tieto cenníky sa používajú na odhad ceny a času a výdavkov a skutočných hodnôt o projektoch, ktoré sú spojené s cenovou ponukou prostredníctvom riadka cenovej ponuky.

Ak v cenovej ponuke projektu nie sú uvedené žiadne cenníky projektu, zobrazí sa varovné hlásenie. V hlásení sa uvádza, že keďže neexistujú žiadne cenníky projektu, vaše odhadované a skutočné práce a náklady na projekt nebudú ocenené. Namiesto toho budú mať nulovú (0) cenu za predajné hodnoty.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Priradenie alebo oddelenie cenníka projektu od cenovej ponuky projektu

Ak chcete vytvoriť alebo zvoliť konkrétny cenník na odhadovanie prác a výdavkov na projekt, vykonajte nasledujúce kroky.

1. Na cenovej ponuke vyberte kartu **Cena projektu** a vo vedľajšej mriežke vyberte **+ Pridať nový cenník projektu**.
2. Na stránke Rýchle vytvorenie vyberte cenník. Rozbaľovací zoznam zobrazuje všetky cenníky, pre ktoré je nastavený kontext **Predaj** a mena sa zhoduje s menou v cenovej ponuke.
4. Zadajte popis priradenia cenníka k projektu a vyberte **Uložiť a zavrieť**.

Vytvorí sa priradenie cenníka projektu.

Tento proces môžete zopakovať, ak potrebujete k ponuke projektu priradiť viac ako jeden cenník projektu. Viac cenníkov projektu vytvorte, iba ak máte odlišné dátumy účinnosti pre každý z pridružených cenníkov projektu.

> [!NOTE]
> Project Operations nepodporuje účinnosť prekrývajúcich sa dátumov cenníkov projektu. Ak existuje viac cenníkov projektov pre transakciu s daným dátumom, cena tejto transakcie bude predvolene nastavená na nulu (0).
Ak chcete odstrániť priradenie cenníka projektu, vyberte cenník projektu a potom vyberte **Vymazať cenník pre cenovú ponuku projektu**. Cenník sa odstráni z projektových cenníkov pre cenovú ponuku, samotný cenník sa však nevymaže. Vymaže sa iba priradenie k cenovej ponuke.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Nastavenie predvolených cenníkov projektu pre cenovú ponuku

Cenové ponuky projektu je možné nastaviť predvolene v cenovej ponuke projektu. Toto nastavenie zaisťuje, že všetky ponuky vo vašej organizácii vždy začínajú štandardným cenníkom pre dané cenové obdobie.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Nastavenie predvoleného nastavenia organizácie pre cenníky projektov

1. Prejdite na **Nastavenia** > **Všeobecné** > **Parametre**.
2. Na stránke so zoznamom **Aktívne parametre** vyhľadajte záznam a dvojitým kliknutím ho otvorte. 
3. Na stránke **Parametre** vyberte kartu **Cenník**. Môžete vidieť, že sa zobrazí zoznam predvolených cenníkov. Toto je zoznam štandardných nákladových a predajných cenníkov. Ak tu budete mať priradený predajný cenník pre každú menu, v ktorej predávate, zabezpečíte, aby bol tento predajný cenník predvolený pri každej ponuke, ktorú vytvoríte pre zákazníkov, ktorí obchodujú v tejto mene.

### <a name="set-up-customer-specific-project-price-lists"></a>Stanovenie cenníkov projektov špecifických pre zákazníka

Cenníky projektov špecifických pre zákazníka je možné stanoviť aj vtedy, keď ste so zákazníkmi dojednali rámcovú cenovú dohodu.

Ak chcete stanoviť cenník projektu špecifického pre zákazníka, postupujte nasledovne.

1. V oblasti **Predaj** vyberte možnosť **Zákazníci**.
2. V zozname svojich aktívnych obchodných vzťahov vyberte a otvorte záznam zákazníka, pre ktorý máte špeciálny cenník.
3. Na karte **Cenníky projektu** môžete vytvoriť nové priradenie cenníka a vytvoriť cenník projektu, ktorý je špecifický pre tohto zákazníka.

## <a name="create-custom-pricing-on-a-project-quote"></a>Vytvorenie vlastných cien na v cenovej ponuke projektu

Keď budete mať predvolené organizačné cenníky projektu a cenníky projektu špecifické pre zákazníka, vaše projektové cenové ponuky sa automaticky vytvoria s týmito priradeniami cenníka projektu. V určitých prípadoch však možno budete musieť vytvoriť vlastnú cenu pre konkrétnu cenovú ponuku projektu. 

1. V časti **Cenová ponuka projektu** na karte **Cenník projektu** vo vedľajšej mriežke overte, či nie je vybraný žiadny špecifický záznam cenníka.
2. Vyberte možnosť **Vytvorenie vlastných cien**. Takto sa vytvoria kópie všetkých štandardných cenníkov, ktoré sú v súčasnosti spojené s cenovou ponukou, a tieto kópie sa priradia k cenovej ponuke. Existujúce priradenia k štandardným cenníkom budú odstránené. Predajca potom môže začať s úpravami cien na týchto kópiách. Tieto zmenené ceny sa budú vzťahovať iba na túto cenovú ponuku projektu.
