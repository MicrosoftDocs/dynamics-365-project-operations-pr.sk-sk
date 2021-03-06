---
title: Spravovanie viacerých zákazníkov v projektových cenových ponukách
description: Táto téma poskytuje informácie o práci na cenových ponukách, ktoré sa týkajú viacerých zákazníkov, ktorí budú financovať projekt.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908588"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>Spravovanie viacerých zákazníkov v projektových cenových ponukách

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Cenové ponuky projektu podporujú scenár, keď návrh zahŕňa viacerých zákazníkov, ktorí budú financovať obchod. Karta **Súhrn** cenovej ponuky obsahuje pole **Potenciálny zákazník**, ktoré identifikuje primárneho zákazníka obchodu. Ďalší zákazníci pre obchod môžu byť nastavení na karte **Zákazníci** cenovej ponuky projektu.

Všetky cenové ponuky zákazníkov na karte **Zákazníci** cenovej ponuky projektu budú predvolené ako riadok cenovej ponuky zákazníkov na všetkých **nových** riadkoch cenovej ponuky založenej na projekte vytvorených pre cenovú ponuku. Žiadne existujúce riadky cenových ponúk založené na projekte nebudú dediť nové zákaznícke záznamy cenových ponúk vytvorené po nich.

Zákazníci cenových ponúk a zákazníci riadkov cenových ponúk môžu byť pridaní, aktualizovaní alebo vymazaní kedykoľvek pred získaním cenovej ponuky. Platný zákazník v cenovej ponuke musí byť nastavený ako zákazník vo vlastniacej spoločnosti alebo právnickej entite na stránke **Zákazníci**. Právnické entity sú zriadené v module **Projektové riadenie a účtovníctvo** v Dynamics 365 Project Operations a sú sprístupnené ako spoločnosti v moduloch **Predaj a dodanie projektu** v Project Operations.

## <a name="concept-of-a-primary-customer"></a>Koncept primárneho zákazníka

Zákazník uvedený na karte **Súhrn** cenovej ponuky projektu ako potenciálny zákazník je primárnym zákazníkom ponuky. Ak sa pokúsite odstrániť primárneho zákazníka zo zoznamu zákazníkov v cenovej ponuke, zobrazí sa chyba, že záznam primárneho zákazníka z cenovej ponuky nemožno vymazať.

Primárny zákazník by nemal byť aktualizovaný zo zoznamu zákazníkov v cenovej ponuke. Primárneho zákazníka však môžete ovplyvniť zmenou potenciálneho zákazníka na karte **Zhrnutie** cenovej ponuky. Keď sa toto pole aktualizuje na **Súhrn cenovej ponuky**, novo vybraný potenciálny zákazník je pridaný ako nový zákazník cenovej ponuky s nastaveným príznakom **Primárny**. Starý potenciálny zákazník bude naďalej zákazníkom uvedeným v cenovej ponuke.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Vytvorenie, aktualizovanie alebo odstránenie záznamu zákazníka cenovej ponuky

Zákazník cenovej ponuky môže byť vytvorený, aktualizovaný alebo vymazaný na karte **Zákazníci cenovej ponuky** na stránke **Cenová ponuka**. Polia uvedené v nasledujúcej tabuľke sa nachádzajú v zázname zákazníka cenovej ponuky v cenovej ponuke projektu.

| **Pole** | **Miesto** | **Relevantnosť, účel a pokyny** | **Nadväzujúci vplyv** |
| --- | --- | --- | --- |
| Konto | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Zobrazenie zoznamu všetkých aktívnych účtov. Po vytvorení záznamu je toto pole uzamknuté. Ak ho chcete aktualizovať, odstráňte záznam a znova ho vytvorte. Ak ste zaznamenali akékoľvek skutočné hodnoty alebo ak je záznam cenovej ponuky zákazníka primárnym zákazníkom, budete môcť záznam odstrániť. | Zákazníci cenových ponúk sa pri vytváraní riadkov cenových ponúk kopírujú ako zákazníci cenových ponúk. Po získaní cenovej ponuky sa zákazníci cenovej ponuky prekopírujú aj k zákazníkom so zmluvou o projekte. |
| Percento rozdelenia fakturácie | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Predstavuje percento každej nevyfakturovanej predajnej transakcie, ktorá sa pripíše tomuto zákazníkovi cenovej ponuky. | Skopírované do nových vytvorených riadkov cenových ponúk a zmluvných zákazníkov projektu. |
| Meno kontaktu platiteľa | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Toto je textové pole a malo by sa použiť na identifikáciu kontaktnej osoby pre zákazníka. Sú predvolené zo záznamu súvisiaceho obchodného vzťahu | Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky a následne do poľa Meno kontaktu platiteľa na faktúre, ktorá je generovaná pre tohto zákazníka. |
| Fakturačné meno | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Toto textové pole by sa malo použiť na identifikáciu kontaktnej osoby faktúry pre zákazníka. | Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky a následne do poľa **Meno kontaktu platiteľa** na faktúre, ktorá je generovaná pre tohto zákazníka. |
| Platobné podmienky | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Toto je množina možností s hodnotami, ktoré sú predvolené zo záznamu súvisiaceho obchodného vzťahu. | Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky a následne do poľa **Meno kontaktu platiteľa** na faktúre, ktorá je generovaná pre tohto zákazníka. |
| Zaokrúhľuje | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Označuje, či je tento zákazník predvoleným zákazníkom zaokrúhľovania pre túto dohodu. | Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky. |
| Vlastniaca spoločnosť | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Právnická entita, ktorú má tento zákazník zriadenú v module **Projektové riadenie a účtovníctvo**. Toto pole je iba na čítanie a je nastavené na spoločnosť, ktorá vlastní samotnú cenovú ponuku. Zoznam zákazníkov, ktorých je možné pridať do poľa **Obchodný vzťah** je už filtrované do zoznamu z tejto vlastniacej spoločnosti v module **Projektové riadenie a účtovníctvo** v Project Operations. | Vlastnená spoločnosť je rovnaká ako pojem právna entita v module **Projektové riadenie a účtovníctvo** v Project Operations. Všetky náklady a výnosy z tohto projektu sa účtujú v hlavnej účtovnej knihe vlastniacej spoločnosti, |
| Limit, ktorý sa nesmie prekročiť | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Označuje, či existuje dohodnutý limit alebo strop celkovej sumy, ktorá bude fakturovaná tomuto zákazníkovi za túto zákazku. | Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky. |

## <a name="editing-billing-split-percentages"></a>Úprava percenta rozdelenia fakturácie

Percentuálne podiely rozdelenia fakturácie môžete upraviť pomocou prostredia na úpravy v mriežke. Ak percentá rozdelenia fakturácie nedosiahnu 100 %, dôjde k chybe. Po aktualizácii percentuálnych podielov rozdelenia fakturácie chybu obnovte obnovením stránky.

Môžete tiež skúsiť vybrať **Rovnomerne rozdeliť** na vedľajšej mriežke zákazníka cenovej ponuky. Táto akcia prideľuje rozdelenie fakturácie všetkým zákazníkom cenových ponúk. Ak existuje nejaký faktor zaokrúhľovania, pridá sa k zákazníkovi zaokrúhľovania. Jeden zo zákazníkov cenovej ponuky je vždy označený ako zákazník zaokrúhľovania. to znamená, že záznam zákazníka cenovej ponuky má nastavený príznak **Zaokrúhľovanie** na **Áno**. Spravidla ide o primárneho zákazníka cenovej ponuky, ale túto voľbu je možné zmeniť.