---
title: Spravovanie viacerých zákazníkov v projektových cenových ponukách – čiastočné
description: Táto téma poskytuje informácie o práci na cenových ponukách s viacerými zákazníkmi, ktorí budú financovať projekt. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c9b3c1a1b958de0fc5d58199b8229ea5b3b221d01efe6602eecffdd100f13cae
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001675"
---
# <a name="manage-multiple-customers-on-project-quotes---lite"></a>Spravovanie viacerých zákazníkov v projektových cenových ponukách – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Cenové ponuky projektu podporujú scenár, keď návrh zahŕňa viacerých zákazníkov, ktorí budú financovať obchod. Karta **Súhrn** cenovej ponuky obsahuje pole **Potenciálny zákazník**, ktoré identifikuje primárneho zákazníka obchodu. Ďalší zákazníci pre obchod môžu byť nastavení na karte **Zákazníci** cenovej ponuky projektu.

Všetky cenové ponuky zákazníkov na karte **Zákazníci** cenovej ponuky projektu budú predvolené ako riadok cenovej ponuky zákazníkov na všetkých **nových** riadkoch cenovej ponuky založenej na projekte vytvorených pre cenovú ponuku. Žiadne existujúce riadky cenových ponúk založené na projekte nebudú dediť nové zákaznícke záznamy cenových ponúk vytvorené po nich.

Riadky cenových ponúk založených na produkte sú automaticky spojené s primárnym zákazníkom, ktorý je zároveň zákazníkom v poli **Potenciálny zákazník** na karte **Súhrn** cenovej ponuky.

Zákazníci cenových ponúk a zákazníci riadkov cenových ponúk môžu byť pridaní, aktualizovaní alebo vymazaní kedykoľvek pred získaním cenovej ponuky.

## <a name="concept-of-a-primary-customer"></a>Koncept primárneho zákazníka

Zákazník, ktorý je na karte Súhrn cenovej ponuky projektu ako potenciálny zákazník je primárnym zákazníkom cenovej ponuky. Ak sa pokúsite odstrániť primárneho zákazníka zo zoznamu zákazníkov v cenovej ponuke, uvidíte chybu, že záznam primárneho zákazníka z cenovej ponuky nemožno vymazať.

Primárny zákazník by nemal byť aktualizovaný zo zoznamu zákazníkov v cenovej ponuke. Primárneho zákazníka však môžete ovplyvniť zmenou potenciálneho zákazníka na karte **Zhrnutie** cenovej ponuky. Keď sa toto pole aktualizuje na **Súhrn cenovej ponuky**, novo vybraný potenciálny zákazník je pridaný ako nový zákazník cenovej ponuky s nastaveným príznakom **Primárny**. Starý potenciálny zákazník bude naďalej zákazníkom uvedeným v cenovej ponuke.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Vytvorenie, aktualizovanie alebo odstránenie záznamu zákazníka cenovej ponuky

Zákazník cenovej ponuky môže byť vytvorený, aktualizovaný alebo vymazaný na karte **Zákazníci cenovej ponuky** na stránke **Cenová ponuka**. Polia uvedené v nasledujúcej tabuľke sa nachádzajú v zázname zákazníka cenovej ponuky v cenovej ponuke projektu.

| **Pole** | **Miesto** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- | --- |
| Konto | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Zobrazenie zoznamu všetkých aktívnych účtov. Po vytvorení záznamu je toto pole uzamknuté. Ak ho chcete aktualizovať, odstráňte záznam a znova ho vytvorte. Ak ste zaznamenali akékoľvek skutočné hodnoty alebo ak je záznam cenovej ponuky zákazníka primárnym zákazníkom, budete môcť záznam odstrániť. | Zákazníci cenových ponúk sa pri vytváraní riadkov cenových ponúk kopírujú ako zákazníci cenových ponúk. Po získaní cenovej ponuky sa zákazníci cenovej ponuky prekopírujú aj k zákazníkom so zmluvou o projekte. |
| Percento rozdelenia fakturácie | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Predstavuje percento každej nevyfakturovanej predajnej transakcie, ktorá sa pripíše tomuto zákazníkovi cenovej ponuky. | Skopírované do nových riadkov cenových ponúk a zmluvných zákazníkov projektu. |
| Meno kontaktu platiteľa | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Toto je textové pole a malo by sa použiť na identifikáciu kontaktnej osoby pre zákazníka. Sú predvolené zo záznamu súvisiaceho obchodného vzťahu | Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky a následne do poľa Meno kontaktu platiteľa na faktúre, ktorá je generovaná pre tohto zákazníka. |
| Fakturačné meno | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Toto textové pole by sa malo použiť na identifikáciu kontaktnej osoby faktúry pre zákazníka. | Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky a následne do poľa **Meno kontaktu platiteľa** na faktúre, ktorá je generovaná pre tohto zákazníka. |
| Platobné podmienky | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Toto je množina možností s hodnotami, ktoré sú predvolené zo záznamu súvisiaceho obchodného vzťahu. | Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky a následne do poľa **Meno kontaktu platiteľa** na faktúre, ktorá je generovaná pre tohto zákazníka, |
| Zaokrúhľuje | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Označuje, či je tento zákazník predvoleným zákazníkom zaokrúhľovania pre túto dohodu. | Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky. |
| Limit, ktorý sa nesmie prekročiť | Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky. | Označuje, či existuje dohodnutý limit alebo strop celkovej sumy, ktorá bude fakturovaná tomuto zákazníkovi za túto zákazku | Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky. |

## <a name="editing-billing-split-percentages"></a>Úprava percenta rozdelenia fakturácie

Percentuálne podiely rozdelenia fakturácie môžete upraviť pomocou prostredia na úpravy v mriežke. Ak percentá rozdelenia fakturácie nedosiahnu 100 %, dôjde k chybe. Po aktualizácii percentuálnych podielov rozdelenia fakturácie chybu obnovte obnovením stránky.

Môžete tiež skúsiť vybrať **Rovnomerne distribuovať** na vedľajšej mriežke zákazníkov cenovej ponuky. Táto akcia prideľuje rozdelenie fakturácie všetkým zákazníkom cenových ponúk. Ak existuje nejaký faktor zaokrúhľovania, pridá sa k zákazníkovi zaokrúhľovania. Jeden zo zákazníkov cenovej ponuky je vždy označený ako zákazník zaokrúhľovania. to znamená, že záznam zákazníka cenovej ponuky má nastavený príznak **Zaokrúhľovanie** na **Áno**. Spravidla ide o primárneho zákazníka cenovej ponuky, ale túto voľbu je možné zmeniť.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]