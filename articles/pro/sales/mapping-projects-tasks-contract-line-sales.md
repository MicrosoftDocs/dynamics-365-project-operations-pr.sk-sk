---
title: Mapovanie projektov a úloh na riadok zmluvy založenej na projekte – čiastočné
description: Táto téma poskytuje informácie o pridávaní a odstraňovaní projektov a úloh na riadok zmluvy.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b86e03192625b0dabb89080f2ade1ed9e3567cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994651"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Mapovanie projektov a úloh na riadok projektovej zmluvy 

_**Vzťahuje sa na:** Čiastočné nasadenie – dohoda o fakturácii pro forma, Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

V riadkoch zmlúv založených na projektoch môžete mapovať konkrétne úlohy v projekte na riadok zmluvy.

Keď mapujete konkrétne úlohy na riadok zmluvy, metóda fakturácie, možnosti účtovania, limity neprekročenia a zákazníci definovaní na riadku zmluvy sa budú vzťahovať iba na tieto konkrétne úlohy.

Ak máte scenár, v ktorom jedna fáza projektu, napríklad fáza prototypov, má pevnú cenu a všetky ostatné fázy sú závislé od času a materiálu, budete môcť fázu prototypu a všetky súvisiace podradené úlohy priradiť k riadku zmluvy pre túto fázu s metódou fakturácie za pevnú cenu.

Všetky ďalšie fázy vo vašej štruktúre rozdelenia práce na projekte (WBS) môžu byť spojené s riadkom zmluvy závislým od času a materiálu.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Priradenie úloh k riadkom zmluvy založeným na projekte

Úlohy môžu byť spojené s riadkami zmluvy z karty **Fakturovateľné úlohy** na stránke **Riadok zmluvy** alebo z karty **Fakturácia úloh** na stránke **Projekt**.

### <a name="from-the-contract-line-page"></a>Zo stránky Riadok zmluvy

Vykonajte nasledujúce kroky na priradenie projektových úloh k riadku zmluvy z karty **Fakturovateľné úlohy** stránky **Riadok zmluvy**.

1. Na karte **Všeobecné** na karte riadku zmluvy založenej na projekte overte, či je pole **Projekt** vyplnené.
2. V poli **Zahrnuté úlohy** vyberte pole **Iba vybrané úlohy**.
3. Uloží zmeny. Formulár sa obnoví a karta **Fakturovateľné úlohy** bude viditeľná.
4. Vyberte kartu **Fakturovateľné úlohy** a vo vedľajšej mriežke vyberte **Pridajte úlohu riadka zmluvy**.
5. Na stránke **Úlohy riadkov zmlúv** v rozbaľovacej ponuke **Úlohy** vyberte úlohu. 
6. Zadajte informácie do poľa **Typ fakturácie** a potom vyberte **Uložiť a zavrieť**. Vybraná úloha je priradená k riadku zmluvy.

> [!NOTE]
> Toto nie je optimálny postup na priradenie projektových úloh k riadkom zmluvy. Každý projekt bude musieť byť v rámci tohto postupu priradený ručne. Preferovaný spôsob je z karty **Fakturácia úloh** na stránke **Projekt**.

### <a name="from-the-project-page"></a>Zo stránky projektu

Toto je optimálna metóda na priradenie úloh k riadkom zmluvy. Môžete vybrať viac úloh a priradiť všetky z nich a ich podradené úlohy vybranému riadku zmluvy. Vykonajte nasledujúce kroky na priradenie úloh k riadku zmluvy zo stránky **Projekt**.

1. Na karte **Všeobecné** na karte riadku zmluvy založenej na projekte overte, či je pole **Projekt** vyplnené.
2. V poli **Zahrnuté úlohy** vyberte **Iba vybrané úlohy**.
3. Uložte riadok zmluvy založený na projekte. Formulár sa obnoví a karta **Fakturovateľné úlohy** bude viditeľná. Je to len na overovacie účely.
4. Na karte **Všeobecné** riadka zmluvy založenej na projekte, v poli **Projekt**, vyberte odkaz na projekt.
5. Na stránke **Projekt** vyberte kartu **Nastavenie fakturácie úloh**.
6. Nachádzajú sa tu dve mriežky. Jedna mriežka je pre riadky zmlúv, ktoré sa vzťahujú na celý projekt. Druhá mriežka sa vzťahuje na nastavenie fakturácie pre konkrétnu úlohu. V druhej mriežke vyberte jednu alebo viac úloh a potom vyberte **Priradiť riadky zmlúv**.
7. Na otvorenej dialógovej stránke vyberte z rozbaľovacej ponuky riadok zmluvy.
8. Použite rozbaľovacie pole **Typ fakturácie** a označte úlohy ako fakturovateľné alebo nefakturovateľné.
9. Začiarknutím políčka označte, či by priradenie malo obsahovať aj podradené úlohy vybratých úloh. Začiarknutím tohto políčka sa tiež podradené úlohy vybraných úloh priradia k riadku zmluvy.
10. Výberom možnosti **OK** zatvoríte dialógové okno.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Zrušenie priradenia úloh z riadkov zmlúv založených na projekte

### <a name="from-the-contract-line-page"></a>Zo stránky riadka zmluvy

Vykonajte nasledujúce kroky na zrušenie priradenia projektových úloh z riadka zmluvy na karte **Fakturovateľné úlohy** stránky **Riadok zmluvy**.

1. Na karte **Fakturovateľné úlohy** vyberte **Vymazať úlohu na riadku zmluvy**.
2. Varovná správa naznačuje, že odstránenie tohto priradenia by mohlo mať za následok vrátenie akýchkoľvek skutočných hodnôt, ktoré boli predtým zaznamenané v úlohe. Výberom **OK** v dialógovom okne odstránite asociácie medzi úlohou a riadkom zmluvy založenej na projekte. 

> [!NOTE]
> Týmto sa úloha z projektu neodstráni. Namiesto toho odstráni priradenie úlohy z riadku zmluvy založenej na projekte.

### <a name="from-the-project-page"></a>Zo stránky projektu

Toto je vhodnejší postup na zrušenie priradenia projektových úloh od riadkov zmluvy. Môžete vybrať viac úloh a zrušiť priradenie všetkých z nich a ich podradených úloh z vybraného riadka zmluvy. Vykonajte nasledujúce kroky na zrušenie priradenia úloh od riadka zmluvy.

1. Na karte **Všeobecné** riadka zmluvy založenej na projekte, v poli **Projekt**, kliknite na odkaz na projekt.
2. Na stránke **Projekt** vyberte kartu **Nastavenie fakturácie úloh**.
3. Na stránke sú dve mriežky. Jedna mriežka je pre riadky zmlúv, ktoré sa vzťahujú na celý projekt, a druhá pre nastavenie fakturácie pre konkrétnu úlohu. V druhej mriežke vyberte jednu alebo viac úloh a potom vyberte **Zrušiť priradenie riadkov zmlúv**.
4. Na otvorenej dialógovej stránke vyberte z rozbaľovacej ponuky riadok zmluvy.
5. Začiarknutím políčka označte, či by sa priradenie malo odstrániť aj od všetkých podradených úloh vybratých úloh. Začiarknutím tohto políčka dôjde k zrušeniu priradenia podradených úloh vybraných od riadka zmluvy.
6. Vyberte položku **OK**. Varovná správa naznačuje, že odstránenie tohto priradenia by mohlo mať za následok vrátenie akýchkoľvek skutočných hodnôt, ktoré boli zaznamenané v úlohe predtým. Výberom **OK** v dialógovom okne s varovaním odstránite asociácie medzi úlohou a riadkom zmluvy založenej na projekte.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
