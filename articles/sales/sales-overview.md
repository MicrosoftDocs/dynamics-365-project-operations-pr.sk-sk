---
title: Prehľad procesu predaja
description: Táto téma poskytuje informácie o základných predajných procesoch.
author: rumant
manager: Annbe
ms.date: 10/29/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8300887e7c5fbd78343d16d191775a67e43138e2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277402"
---
# <a name="sales-process-overview"></a>Prehľad procesu predaja

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Predajné procesy, ktoré sa používajú v organizácii založenej na projekte, sa odlišujú od predajných procesov, ktoré sa používajú v organizácii založenej na produktoch. Tento sa vyskytuje, pretože predajné cykly pre organizácie založené na projekte sú dlhšie a vyžadujú prispôsobené metódy odhadu na analýzu a vytváranie cenových ponúk pre každú dohodu. Dynamics 365 Project Operations využíva niektoré z nasledujúcich funkcií, ktoré sa používajú pri predajnom procese:

- Záznam potenciálneho zákazníka sa používa na sledovanie procesu predaja.
- Kvalifikačný potenciálni zákazníci sa sledujú ako príležitosti.
- Všetky súvisiace artefakty pre príležitosť sú prístupné. Medzi tieto artefakty patrí predajný tím, zúčastnené strany, pravdepodobnosť, hodnotenie, stupne predaja a obchodné procesy.
- Pre príležitosť sa vytvoria viaceré cenové ponuky.
- Cenová ponuka nadobudne stav **Zatvorená ako vyhraná** na vytvorenie predajnej objednávky. V Project Operations je predajná objednávka prispôsobená a nazýva sa projektová zmluva.

## <a name="estimate-a-sale"></a>Odhad predaja
Hodnota predaja sa môže odhadnúť na základe projektov, ktoré boli predtým dodané, a zložitosti projektov. V prípade projektov, ktoré zahŕňajú rozšírenia na predchádzajúce projekty alebo projekty, v ktorých sú odborné znalosti dodávateľa vysoké a dobre známe pracovné šablóny, môžete použiť jednoduchší proces odhadu. Zložitejšie projekty majú zvyčajne dlhší proces nákupu. Preto existuje viac etáp v procese odhadu predaja. Na začiatku procesu používa predajný tím informácie o manažérov obchodných vzťahov a odborníkov na danú oblasť (SME), aby vytvorili odhad na vysokej úrovni pre každú odlišnú zložku práce, ktorá bude súčasťou cenovej ponuky. Tieto súčasti práce sú reprezentované riadkami cenových ponúk. 

Môžete vytvoriť odhad cenovej ponuky na vysokej úrovni. Nakoniec, tento odhad na vysokej úrovni bude nahradený podrobnejším odhadom, ktorý je založený na pláne projektu, ktorý vytvoríte pomocou štandardizovaných šablón projektu. Tieto šablóny vám pomôžu vytvoriť plán a určiť peňažné hodnoty v cenovej ponuke a jej súčasti (riadky cenovej ponuky). 

Môžete vytvoriť viacero cenových ponúk pre projekt a zoskupiť ich pod jedným záznamom príležitosti. Prípadne je jedna z týchto ponúk označená ako **Uzavretá ako vyhraná**, a vytvorí sa projektová zmluva alebo výkaz prác(SOW). Projektová zmluva obsahuje zmluvnú hodnotu pre každú súčasť (riadok zmluvy), ktorú zákazník akceptuje na doručenie. SOW sa zvyčajne vytvára ako Microsoft Word dokument. Všetky faktúry, ktoré sú odoslané zákazníkovi v priebehu projektu dodania odkaz projektu zmluvy alebo SOW.

Môžete tiež vytvoriť alternatívne cenové ponuky v rámci jedného záznamu príležitosti alebo nastaviť systém tak, aby sa projektová zmluva vytvorila pri vyhranej cenovej ponuke. V takom prípade môžete priložiť dokument programu Word, ktorý predstavuje SOW do záznamu zmluvy o projekte.

## <a name="configure-the-sales-process"></a>Konfigurácia procesu predaja
Môžete použiť postupy podnikového procesu a nakonfigurovať proces predaja. Tieto postupy poskytujú vizuálne rozhranie so sprievodcom, ktoré posúva ponuky vpred cez fázy procesu predaja.

Napríklad vaša spoločnosť môže mať v procese predaja nasledujúcich šesť etáp:

1. Schváliť
2. Odhadované
3. Interná kontrola
4. Zmluva
5. Doručiť
6. Zatvoriť
 
Vaša organizácia môže používať rôzne entity na to, aby zastupovala rovnaké riešenie, ako sa vyvíja. Na začiatku predajného procesu je dohoda zastúpená entitou príležitosť. Ako plynie čas a ďalšie podrobnosti sa objavia, môžete použiť odhady na vysokej úrovni na vytvorenie jednej alebo viacerých cenových ponúk. Ak jedna z týchto cenových ponúk je preskúmaná interne a zainteresovanými zákazníckymi stranami, cenová ponuka entity predstavuje riešenie. Po tom, ako zákazník akceptuje cenovú ponuku, zmluva alebo SOW predstavuje dohodu. Na podporu tohto správania, sú BPF štruktúrované tak, že každá fáza procesu je prepojená s inou databázovú tabuľkou.

**Kvalifikovaná** fáza v procese predaja môže byť podporovaná entitou príležitosti. **Odhad** a **interné revízie** etapy môžu byť podporené citovať entity. **Zmluvná**, **dodacia** a **zatváracia** fáza môže byť podporovaná entitou zmluvy o projekte.

Počas presúvania ponúk fázami sa zobrazí výzva na vytvorenie príslušného záznamu entity, ktorý vám pomôže a prevedie vás procesom. Etapy môžu byť podmienené. Ak napríklad požadujete interné preskúmanie cenovej ponuky iba v prípade, že cenová ponuka používa vlastný cenník, môžete túto podmienku nakonfigurovať v príslušnom štádiu obchodného procesu. Fáza **interného preskúmania** sa potom zobrazí len pre cenové ponuky, ktoré používajú vlastný cenník. Pre všetky ostatné dohody a cenové ponuky, fáza **odhadu** nasleduje fáza **zmluvy**.

> [!NOTE]
> Project Operations má konkrétne stránky pre záznamy entít Príležitosť, Cenová ponuka, Objednávka alebo Faktúra. Tieto záznamy musíte vytvoriť pomocou informačných stránok projektu pre tieto entity. V opačnom prípade nebudete môcť otvoriť záznamy zo stránky **Informácie o projekte**. Ak chcete otvoriť záznam zo stránky **Informácie o projekte**, musíte záznam vymazať a znova vytvoriť pomocou stránky **Informácie o projekte**, kde obchodná logika pre každý z týchto typov entít zaisťuje, že pole **Typ** záznamu je správne nastavené a všetky povinné koncepty sú správne inicializované.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Sledovanie revízií cenových ponúk a projektových plánov v predajnom cykle
V Project Operations nie je možné sledovať revízie vykonané v cenovej ponuke. Namiesto toho musíte označiť existujúcu cenovú ponuku **uzavretú ako stratenú** a potom vytvoriť novú cenovú ponuku. Môžete skopírovať cenovú ponuku alebo klonovať cenové ponuky založené na projekte.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Sledovanie komentárov a schválení cenových ponúk a projektových zmlúv
Môžete spravovať preskúmanie a schvaľovanie cenových ponúk a projektových zmlúv pomocou záznamu múru a príspevkov. Vaša organizácia môže vytvoriť vlastné pracovné postupy a doplnky na priraďovanie, presmerovanie, eskaláciu a spravovanie upozornení o kontrole a schvaľovaní pracovných položiek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]