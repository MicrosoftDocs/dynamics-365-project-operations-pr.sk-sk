---
title: Správa viacerých zákazníkov v projektových zmluvách
description: Tento článok poskytuje informácie o tom, ako spravovať viacerých zákazníkov v rámci projektovej zmluvy.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 78ee117c1068e7af4674cc3b21e1055fd05bb43a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928359"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Správa viacerých zákazníkov v projektových zmluvách

Tento článok poskytuje informácie o tom, ako spravovať viacerých zákazníkov v rámci projektovej zmluvy. Projektovú zmluvu môžete použiť, keď je na financovanie obchodu potrebná zmluva pre viacerých zákazníkov. Na stránke **Projektová zmluva** obsahuje karte **Súhrn** informácie o primárnom zákazníkovi obchodu. Ďalší zákazníci, ktorí sa zúčastňujú na obchode, sa môžu pridať na karte **Zákazníci**.

Všetci zmluvní zákazníci na karte **Zákazníci** v projektovej zmluve predvolene vystupujú ako zákazníci riadku zmluvy v akýchkoľvek nových riadkoch zmlúv založených na projekte, ktoré sú vytvorené pre projektovú zmluvu. Akékoľvek existujúce riadky zmlúv založené na projekte nededia nových zmluvných zákazníkov, ktorí sa vytvárajú neskôr.

Pred získaním zmluvy môžete kedykoľvek pridávať, aktualizovať alebo odstraňovať zákazníkov zmluvy alebo riadka zmluvy. Zákazník v rámci projektovej zmluvy musí byť zriadený ako zákazník vo vlastniacej spoločnosti alebo právnickej osobe na stránke **Zákazníci**. Právnické osoby sú zriadené v module **Projektové riadenie a účtovníctvo** aplikácie Dynamics 365 Project Operations a sú dostupné ako spoločnosti v moduloch **Projektový predaj** a **Dodanie** aplikácie Project Operations.

## <a name="primary-customers"></a>Primárni zákazníci

Potenciálny zákazník uvedený na karte **Súhrn** projektovej zmluvy je primárnym zákazníkom zmluvy. Primárneho zákazníka nemožno aktualizovať zo zoznamu zmluvných zákazníkov. Pri pokuse o odstránenie primárneho zákazníka zo zoznamu zákazníkov v zmluve sa zobrazí chyba, že záznam primárneho zákazníka v zmluve nie je možné odstrániť. Namiesto toho zmeňte zákazníka v poli **Potenciálny zákazník** na karte **Súhrn** projektovej zmluvy. Keď aktualizujete toto pole, novo vybraný zákazník sa pridá ako nový zákazník zmluvy s príznakom **Primárny** nastaveným na **Áno**. Predchádzajúci primárny zákazník je stále zákazníkom na základe zmluvy, už však nie je primárnym zákazníkom.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Vytvorenie, aktualizácia alebo odstránenie záznamu zmluvného zákazníka

Zmluvného zákazníka môžete vytvoriť, aktualizovať alebo vymazať z karty **Zmluvní zákazníci** na stránke **Zmluva**. Nasledujúce polia sú obsiahnuté v zázname zmluvného zákazníka projektovej zmluvy.

| **Pole** | **Miesto** | **Opis** | 
| --- | --- | --- | 
| Konto | Editovateľná mriežka na karte **Zmluvní zákazníci** a hlavná stránka a stránka rýchleho vytvorenia pre zmluvného zákazníka. | Zobrazenie zoznamu všetkých aktívnych účtov. Po vytvorení záznamu je toto pole uzamknuté. Ak chcete aktualizovať záznam, mali by ste ho odstrániť a znova vytvoriť. Ak ste zaznamenali nejaké skutočné hodnoty alebo ak je záznam zmluvného zákazníka primárnym zákazníkom, nemôžete záznam odstrániť. Vy vytvorení riadka zmluvy sa zmluvní zákazníci prekopírujú ako zákazníci riadka zmluvy. |
| Percento rozdelenia fakturácie | Editovateľná mriežka na karte **Zmluvní zákazníci** a hlavná stránka a stránka rýchleho vytvorenia pre zmluvného zákazníka. | Predstavuje percento každej nevyfakturovanej predajnej transakcie, ktorá sa pripisuje zmluvnému zákazníkovi. Keď sa vytvoria nové riadky zmluvy, percentuálny podiel rozdelenia fakturácie sa skopíruje do nových vytvorených riadkov zmluvy a do zákazníkov v riadkoch zmluvy k projektu. |
| Meno kontaktu platiteľa | Editovateľná mriežka na karte **Zmluvní zákazníci** a hlavná stránka a stránka rýchleho vytvorenia pre zmluvného zákazníka. | Toto textové pole by sa malo použiť na identifikáciu kontaktnej osoby pre zákazníka. Hodnota sa predvolene získava zo záznamu súvisiaceho obchodného vzťahu. Názov kontaktu sa kopíruje do poľa **Fakturovať na názov zmluvy** na faktúre, ktorá sa generuje pre zákazníka. |
| Fakturačné meno | Editovateľná mriežka na karte **Zmluvní zákazníci** a hlavná stránka a stránka rýchleho vytvorenia pre zmluvného zákazníka. | Toto pole použite na identifikáciu kontaktnej osoby pre zákazníka. Hodnota sa predvolene získava zo záznamu súvisiaceho obchodného vzťahu. Názov sa kopíruje do poľa **Fakturovať na názov zmluvy** na faktúre, ktorá sa generuje pre zákazníka. |
| Platobné podmienky | Editovateľná mriežka na karte **Zmluvní zákazníci** a hlavná stránka a stránka rýchleho vytvorenia pre zmluvného zákazníka. | Hodnota sa predvolene získava zo záznamu súvisiaceho obchodného vzťahu. Termíny sa kopírujú do poľa **Fakturovať na názov zmluvy** na faktúre, ktorá sa generuje pre zákazníka. |
| Vlastniaca spoločnosť | Editovateľná mriežka na karte **Zmluvní zákazníci projektu** a hlavná stránka a stránka rýchleho vytvorenia pre zmluvného zákazníka projektu. | Právnická osoba, v ktorej je zákazník nastavený v module **Projektové riadenie a účtovníctvo**. Toto pole je iba na čítanie a je nastavené na spoločnosť, ktorá vlastní projektovú zmluvu.</br>Zoznam zákazníkov, ktorých je možné pridať do poľa **Obchodný vzťah** je už filtrované do zoznamu z vlastniacej spoločnosti v module **Projektové riadenie a účtovníctvo** v Project Operations. Vlastniaca spoločnosť sa rovná právnickej osobe v module **Projektové riadenie a účtovníctvo** aplikácie Project Operations. Všetky náklady a výnosy z projektu sa účtujú v hlavnej účtovnej knihe vlastniacej spoločnosti. |
| Zaokrúhľuje | Editovateľná mriežka na karte **Zmluvní zákazníci** a hlavná stránka a stránka rýchleho vytvorenia pre zmluvného zákazníka. | Označuje, či je zákazník predvoleným zákazníkom zaokrúhľovania pre dohodu. Na projektovej zmluve môže byť iba jeden zákazník zaokrúhľovania. Keď sa náklady a nefakturované predaje rozdelia podľa množstva dôjde k rozdielu v zaokrúhľovaní, použije sa tento rozdiel na skutočnú hodnotu, ktorá sa mapuje na zákazníka. |
| Limit, ktorý sa nesmie prekročiť | Editovateľná mriežka na karte **Zmluvní zákazníci** a hlavná stránka a stránka rýchleho vytvorenia pre zmluvného zákazníka. | Označuje, či existuje dohodnutý limit alebo strop celkovej sumy, ktorá bude zákazníkovi fakturovaná za zákazku. Limit, ktorý sa nesmie prekročiť, nastavený na úrovni zmluvného zákazníka sa bude vyhodnocovať na základe nefakturovaných skutočných predajov, ktoré odkazujú na tohto zmluvného zákazníka. |

## <a name="edit-billing-split-percentages"></a>Upraviť percentá rozdelenia fakturácie

Môžete upraviť percentá rozdelenia fakturácie úpravou mriežky. Ak percentá rozdelenia fakturácie nedosiahnu 100 percent, nastane chyba. Po úprave percenta rozdelenia fakturácie chybu odstránite obnovením stránky **Projektová zmluva**.

Môžete tiež vybrať **Rovnomerne distribuovať** na vedľajšej mriežke zákazníkov projektovej zmluvy. Rozdelenia fakturácie sú alokované rovnomerne medzi všetkých zákazníkov v riadku projektovej zmluvy. Ak existuje akýkoľvek faktor zaokrúhľovania, faktor pridá sa k zákazníkovi zaokrúhľovania. Jeden zo zmluvných zákazníkov má vždy príznak **Zaokrúhľovanie** nastavený na **Áno**. Tento zákazník je zákazníkom zaokrúhľovania. Zákazník zaokrúhľovania je zvyčajne tiež primárnym zákazníkom zmluvy, ale nie je to potrebné.


[!INCLUDE[footer-include](../includes/footer-banner.md)]