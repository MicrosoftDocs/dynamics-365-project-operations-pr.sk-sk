---
title: Mapovanie projektov a úloh na riadok cenovej ponuky založenej na projekte
description: Táto téma poskytuje informácie o tom, ako mapovať projekty a úlohy na riadok úlohy založenej na projekte.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272767"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Mapovanie projektov a úloh na riadok cenovej ponuky založenej na projekte

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Na riadkoch cenových ponúk založených na projektoch môžete mapovať konkrétne úlohy projektu, ktorý je už priradený k riadku cenovej ponuky.

Keď mapujete úlohy na riadok cenovej ponuky, nasledujúce položky definované v riadku cenovej ponuky sa budú vzťahovať iba na tieto úlohy:

- Spôsob fakturácie
- Možností účtovateľnosti
- Limity, ktoré sa nesmú prekročiť
- Zákazníci

Napríklad, môžete mať projekt, kde jedna fáza bude mať pevnú cenu a všetky ostatné fázy budú založené na čase a materiáli. V takom prípade môžete prvú fázu a všetky jej podradené úlohy priradiť k riadku cenovej ponuky pre túto fázu s metódou fakturácie za pevnú cenu. Potom môžete všetky ostatné fázy priradiť k cenovej ponuke založenej na čase a materiáli.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Priradenie úloh k riadkom cenových ponúk na základe projektu

Úlohy môžete priradiť k riadkom cenovej ponuky z nasledujúcich umiestnení:

- Stránka **Projekt** > karta **Fakturácia úloh** (optimálna)
- Stránka **Riadok cenovej ponuky** > karta **Fakturovateľné úlohy** 

### <a name="from-the-project-page"></a>Zo stránky projektu

Stránka **Projekt** poskytuje optimálne prostredie na priraďovanie úloh k riadkom cenových ponúk. Túto stránku môžete použiť na výber viacerých úloh a na priradenie všetkých úloh, plus ich podradených úloh, k vybranému riadku cenovej ponuky.

1. Na karte **Všeobecné** riadku ponuky založenej na projekte skontrolujte, či je vyplnené pole **Projekt**.
2. V poli **Zahrnuté úlohy** vyberte **Iba vybrané úlohy**.
3. Uloženie riadka cenovej ponuky založenej na projekte. Keď sa obnoví formulár, zobrazí sa karta **Fakturovateľné úlohy**.
4. Na karte **Všeobecné** vyberte odkaz na projekt z poľa **Projekt**.
5. Na stránke **Projekt** vyberte kartu **Fakturácia úloh**.
6. V druhej mriežke, ktorá sa vzťahuje na nastavenie fakturácie špecifickej pre úlohu, vyberte jednu alebo viac úloh a potom vyberte **Priradiť riadky cenovej ponuky**.
7. Na dialógovej stránke, ktorá sa zobrazí, vyberte riadok cenovej ponuky, ktorý v ponuke zobrazí riadky cenovej ponuky založené na projekte.
8. V poli **Typ fakturácie** označte, či sú tieto úlohy účtovateľné alebo neúčtovateľné.
9. Začiarknutím políčka označte, či by priradenie malo obsahovať podradené úlohy vybratých úloh. Začiarknutím tohto políčka sa podriadené úlohy vybraných úloh priradia k riadku cenovej ponuky.
10. Výberom možnosti **OK** zatvoríte dialógové okno.

### <a name="from-the-quote-line-page"></a>Na stránke riadka cenovej ponuky

Projektové úlohy môžete priradiť k riadkom cenovej ponuky na karte **Fakturovateľné úlohy** na stránke **Riadok cenovej ponuky**.

>[!NOTE]
>Optimálne miesto na priradenie projektových úloh k riadkom cenových ponúk na karte **Fakturácia úloh** na stránke **Projekt**. Ak priraďujete úlohy na karte **Fakturovateľné úlohy** na stránke **Riadok cenovej ponuky**, musíte každý projekt priradiť manuálne.

1. Na karte **Všeobecné** riadku ponuky založenej na projekte skontrolujte, či je v poli **Projekt** vybraný projekt.
2. V poli **Zahrnuté úlohy** vyberte **Iba vybrané úlohy**.
3. Uloženie riadka cenovej ponuky založenej na projekte. Keď sa obnoví formulár, zobrazí sa karta **Fakturovateľné úlohy**.
4. Na karte **Fakturovateľné úlohy** vyberte **Pridať úlohu riadka cenovej ponuky**.
5. Na stránke **Úloha riadka cenovej ponuky** v poli **Úlohy** vyberte úlohu a v poli **Typ fakturácie** vyberte **Uložiť**. 
6. Zatvorí stránku. Vybraná úloha je teraz priradená k riadku cenovej ponuky.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Zrušenie priradenia úloh v riadkoch cenových ponúk na základe projektu

### <a name="from-the-project-page"></a>Zo stránky projektu

Táto metóda poskytuje najoptimálnejšie prostredie na zrušenie priradenia úloh z riadkov cenových ponúk. Z vybratého riadku cenovej ponuky môžete vybrať viacero úloh a zrušiť priradenie všetkých z nich plus ich podradených úloh.

1. Na karte **Všeobecné** riadku ponuky založenej na projekte v poli **Projekt** vyberte prepojenie projektu.
2. Na stránke **Projekt** vyberte kartu **Fakturácia úloh**.
3. V druhej mriežke, ktorá sa vzťahuje na nastavenie fakturácie špecifickej pre úlohu, vyberte jednu alebo viac úloh a potom vyberte **Zrušiť priradenie riadkov cenovej ponuky**.
4. Na zobrazenej dialógovej stránke vyberte riadok cenovej ponuky.
5. Začiarknutím políčka označte, či sa má priradenie odstrániť aj z podradených úloh vybratých úloh. Začiarknutím tohto políčka sa zruší aj priradenie podriadených úloh z riadku cenovej ponuky.
6. Vyberte položku **OK**. Výstražné hlásenie správa informuje, že ak odstránite toto priradenie, všetky skutočné hodnoty predtým zaznamenané v úlohe môžu byť obrátené. 
7. Vyberte **OK**, ak chcete pokračovať a odstrániť priradenie medzi úlohou a riadkom cenovej ponuky založenej na projekte.

### <a name="from-the-quote-line-page"></a>Na stránke riadka cenovej ponuky

Priradenie projektových úloh môžete zrušiť v riadkoch cenovej ponuky na karte **Fakturovateľné úlohy** na stránke **Riadok cenovej ponuky**.

1. Na karte **Fakturovateľné úlohy** vyberte **Odstrániť úlohu riadka cenovej ponuky**.
2. Vyberte položku **OK**. Výstražné hlásenie správa informuje, že ak odstránite toto priradenie, všetky skutočné hodnoty predtým zaznamenané v úlohe môžu byť obrátené. 
3. Vyberte **OK**, ak chcete pokračovať a odstrániť priradenie medzi úlohou a riadkom cenovej ponuky založenej na projekte.

>[!NOTE]
> Tento postup neodstráni úlohu z projektu. Odstráni iba priradenie úlohy z riadku cenovej ponuky založenej na projekte.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]