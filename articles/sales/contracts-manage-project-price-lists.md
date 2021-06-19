---
title: Správa projektových cenníkov v projektových zmluvách
description: Táto téma poskytuje informácie o správe projektových cenníkov v projektových zmluvách.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3313eef74b5e7a0624b32d2a336cd986dfdda839
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010400"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Správa projektových cenníkov v projektových zmluvách

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Projektové zmluvy v rámci Dynamics 365 Project Operations sú navrhnuté tak, aby podporovali viacdenné efektívne predajné cenníky v rámci zmluvy. V aplikácii Project Operations existuje nová pridružená entita s názvom **Projektové cenníky**. Táto entita má vzťah typu jeden k mnohým k projektovej zmluve.

Cenníky projektu sa používajú na ocenenie časových, materiálových a výdavkových transakcií projektu. Ak má zmluva jeden alebo viac projektových cenníkov, tieto cenníky sa používajú na stanovenie ceny za čas, materiál, odhady výdavkov a skutočné hodnoty v projektoch, ktoré sú spojené so zmluvou prostredníctvom riadku zmluvy.

Ak na projektovej zmluve nie sú uvedené žiadne projektové cenníky, zobrazí sa varovná správa, že neexistujú žiadne projektové cenníky a vaše odhady, skutočná práca na projekte, materiál a zaznamenané náklady nebudú ocenené. Za predajné hodnoty sa nebude platiť žiadna cena.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Priradenie alebo zrušenie priradenia projektového cenníka k projektovej zmluve

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Vytvorenie alebo priradenie konkrétneho cenníka pre odhad projektovej práce, materiálu a výdavkov

1. Na projektovej zmluve vyberte kartu **Projektové cenníky**.
2. Vo vedľajšej mriežke vyberte **+ Pridať nový projektový cenník**.
3. Na jazdci **Rýchle vytvorenie** vyberte cenník. 

  Rozbaľovací zoznam zobrazuje všetky cenníky, pre ktoré je nastavený kontext **Predaj**, kde sa mena v cenníku zhoduje s menou na zmluve.
  
4. Zadajte popis priradenia projektového cenníka, zvoľte **Uložiť** a potom zatvorte jazdec **Rýchle vytvorenie**.

   Vytvorí sa priradenie cenníka projektu.
   
5. Opakovaním krokov 1 – 4 priraďte k projektovej zmluve viac ako jeden projektový cenník. Viac projektových cenníkov vytvorte iba vtedy, ak máte rozdielny dátum účinnosti pre každý z pridružených projektových cenníkov.

> [!NOTE]
> Aplikácia Project Operations nepodporuje prekrývanie dátumovej účinnosti projektových cenníkov. Ak existuje viac projektových cenníkov pre transakciu s daným dátumom, cena tejto transakcie bude predvolene nastavená na nulu.

### <a name="remove-a-project-price-list-association"></a>Odstránenie priradenie projektového cenníka

- Vyberte projektový cenník a potom zvoľte na vedľajšej mriežke možnosť **Odstrániť projektový cenník zmluvy**. 

  Cenník sa odstráni z projektových cenníkov v zmluve. Samotný cenník sa neodstráni. Odstráni sa iba priradenie k zmluve.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Nastavenie automatického predvolenia projektových cenníkov v zmluve

Projektový cenník je možné nastaviť ako predvolený projektový cenník. Toto nastavenie zaisťuje, že všetky zmluvy vo vašej organizácii vždy začínajú štandardným projektovým cenníkom pre dané cenové obdobie.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Nastavenie predvolenej hodnoty organizácie pre projektové cenníky

1. Prejdite do ponuky **Nastavenie** > **Všeobecné** a potom vyberte **Parametre**.
2. Na stránke so zoznamom **Aktívne parametre** vyberte záznam a dvojitým kliknutím ho otvorte. Pri dvojitom kliknutí sa uistite, že neklikáte na hodnotu poľa, ktorá je hypertextovým odkazom. 
3. Na stránke **Aktívne parametre** vyberte kartu **Cenník**. Vedľajšia mriežka zobrazuje zoznam predvolených cenníkov. Toto je zoznam štandardných nákladových a predajných cenníkov. Ak budete mať na tomto mieste priradený cenník **Predaj** pre každú menu, v ktorej predávate, budete mať istotu, že cenník pre predaj je predvolený pre všetky zmluvy, ktoré vytvoríte pre zákazníkov, ktorí obchodujú v tejto mene.

### <a name="set-up-a-customer-specific-project-price-list"></a>Vytvorenie projektového cenníka pre konkrétneho zákazníka

Ak ste so zákazníkmi dohodli rámcovú cenovú dohodu, môžete vytvoriť aj projektové cenníky špecifické pre zákazníka.

1. Prejdite do časti **Predaj** > **Zákazníci**.
2. Zo zoznamu aktívnych obchodných vzťahov vyberte zákazníka, pre ktorého má špeciálny cenník.
3. Vyberte záznam zákazníka, aby ste ho otvorili, a potom vyberte kartu **Projektové cenníky**. Na vedľajšej mriežke sa zobrazí zoznam projektových cenníkov špecifických pre tohto zákazníka. 
4. Vytvorte tu nové priradenie cenníkov, aby bol projektový cenník špecifický pre tohto zákazníka.

## <a name="custom-pricing-on-a-project-contract"></a>Vlastné ceny v projektovej zmluve

Keď budete mať predvolené projektové cenníky pre organizácie a zákazníkov, vaše projektové zmluvy sa automaticky vytvoria s týmito asociáciami projektových cenníkov. Projektové cenníky v projektovej zmluve sa však vždy kopírujú s dátumom a názvom zmluvy, ktorý je k nim pripojený. Manažéri obchodných vzťahov a projektoví manažéri potom môžu upravovať ceny v týchto kópiách. Tieto zmenené ceny sa budú vzťahovať iba na túto projektovú zmluvu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
