---
title: Procesy predaja
description: Táto téma poskytuje informácie o základných predajných procesoch.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: a169dee5-f4a7-42c8-9bf1-7f0018cc25cb
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: eaaa4b8fe6577ff572489ac0c6abac3c4e970c63
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755599"
---
# <a name="sales-processes"></a>Procesy predaja

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Predajné procesy, ktoré sa používajú v organizácii založenej na projekte, sa odlišujú od predajných procesov, ktoré sa používajú v organizácii založenej na produktoch. Tento rozdiel sa vyskytuje, pretože predajné cykly pre organizácie založené na projekte sú dlhšie a vyžadujú prispôsobené metódy odhadu na analýzu a vytváranie cenových ponúk pre každú dohodu. Dynamics 365 Project Service Automation používa niektoré rovnaké funkcie, ktoré sa používajú v procese predaja pre Dynamics 365 Sales. Tu sú niektoré príklady:

- Vedúca entita zákazníka sa používa na sledovanie procesu predaja.
- Kvalifikačný potenciálni zákazníci sa sledujú ako príležitosti. Proces predaja môže tiež začať s príležitosťou.
- Všetky súvisiace artefakty pre príležitosť sú prístupné. Medzi tieto artefakty patrí predajný tím, zúčastnené strany, pravdepodobnosť, hodnotenie, stupne predaja a obchodné procesy.
- Pre príležitosť sa vytvoria viaceré cenové ponuky.
- Cenová ponuka je označená **Zatvorená ako vyhraná** na vytvorenie predajnej objednávky. V PSA je predajná objednávka prispôsobená a nazýva sa projektová zmluva.

Nasledujúci obrázok znázorňuje typický proces predaja v organizácii založenej na projekte.

> ![Proces predaja v organizácii založenej na projekte](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Odhad predaja
Hodnota predaja sa môže odhadnúť na základe projektov, ktoré boli predtým dodané, a zložitosti projektov. V prípade projektov, ktoré zahŕňajú rozšírenia na predchádzajúce projekty alebo projekty, v ktorých sú odborné znalosti dodávateľa vysoké a dobre známe pracovné šablóny, môžete použiť jednoduchší proces odhadu. Zložitejšie projekty majú zvyčajne dlhší proces nákupu. Preto existuje viac etáp v procese odhadu predaja. Na začiatku procesu používa predajný tím vstup manažérov účtov a odborníkov na predmet (MSP), aby začali vytvárať odhad na vysokej úrovni pre každú odlišnú zložku práce, ktorá je ponúkaná. Tieto súčasti práce sú reprezentované riadkami cenových ponúk. 

Môžete vytvoriť odhad cenovej ponuky na vysokej úrovni. Nakoniec, tento odhad na vysokej úrovni bude nahradený podrobnejším odhadom, ktorý je založený na pláne projektu, ktorý vytvoríte pomocou štandardizovaných šablón projektu. Tieto šablóny vám pomôžu vytvoriť plán a určiť peňažné hodnoty v cenovej ponuke a jej súčasti (riadky cenovej ponuky). 

Môžete vytvoriť viacero cenových ponúk pre projekt a zoskupiť ich pod typom entity jednej príležitosti. Nakoniec, je jedna z týchto ponúk označená **uzavretá ako vyhraná**, a projekt zmluvy alebo vyhlásenie o dielo (SOW) je vytvorený. Projektová zmluva obsahuje zmluvnú hodnotu pre každú súčasť (riadok zmluvy), ktorú zákazník akceptuje na doručenie. SOW sa zvyčajne vytvára ako Microsoft Word dokument. Všetky faktúry, ktoré sú odoslané zákazníkovi v priebehu projektu dodania odkaz projektu zmluvy alebo SOW.

Môžete tiež vytvoriť alternatívne cenové ponuky v rámci jedného typu entity príležitosti alebo nastaviť systém tak, aby sa projektová zmluva vytvorila pri vyhranej cenovej ponuke. V takom prípade môžete priložiť dokument programu Word, ktorý predstavuje SOW do záznamu zmluvy o projekte.

![Uzavretie cenovej ponuky na vytvorenie zmluvy o projekte](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Konfigurácia procesu predaja
Môžete použiť Business Process toky (BPFs) v Microsoft Dynamics 365 a nakonfigurovať proces predaja. BPF dajú svojim predajným pracovníkom riadené vizuálne rozhranie, ktoré môžu použiť na presun ponuky vpred cez etapy, ktoré sú typické pre vašu firmu.

Napríklad vaša spoločnosť môže mať v procese predaja nasledujúcich šesť etáp:

1. Kvalifikovať
2. Odhadované
3. Interná kontrola
4. Zmluva
5. Doručiť
6. Zavrieť

Týchto šesť etáp je zastúpených šípkami (\>), ktoré vyberiete rozbalením v každej príležitosti typu entity, ktoré vytvoríte.

![Nastavenie obchodného procesu v Dynamics 365](media/basic-guide-3.png)
 
Vaša organizácia môže používať rôzne entity na to, aby zastupovala rovnaké riešenie, ako sa vyvíja. Na začiatku predajného procesu je dohoda zastúpená entitou príležitosť. Ako plynie čas a ďalšie podrobnosti sa objavia, môžete použiť odhady na vysokej úrovni na vytvorenie jednej alebo viacerých cenových ponúk. Ak jedna z týchto cenových ponúk je preskúmaná interne a zainteresovanými zákazníckymi stranami, cenová ponuka entity predstavuje riešenie. Po tom, ako zákazník akceptuje cenovú ponuku, zmluva alebo SOW predstavuje dohodu. Na podporu tohto správania, sú BPF štruktúrované tak, že každá fáza procesu je prepojená s inou databázovú tabuľkou.

**Kvalifikovaná** fáza v procese predaja môže byť podporovaná entitou príležitosti. **Odhad** a **interné revízie** etapy môžu byť podporené citovať entity. **Zmluvná**, **dodacia** a **zatváracia** fáza môže byť podporovaná entitou zmluvy o projekte.

Počas presúvania ponúk fázami sa zobrazí výzva na vytvorenie príslušného záznamu entity, ktorý vám pomôže a prevedie vás procesom. Etapy môžu byť podmienené. Ak napríklad požadujete interné preskúmanie cenovej ponuky iba v prípade, že cenová ponuka používa vlastný cenník, môžete túto podmienku nakonfigurovať v príslušnom štádiu obchodného procesu. Fáza **interného preskúmania** sa potom zobrazí len pre cenové ponuky, ktoré používajú vlastný cenník. Pre všetky ostatné dohody a cenové ponuky, fáza **odhadu** nasleduje fáza **zmluvy**.

> [!NOTE]
> PSA má špecifické stránky pre entity príležitosti, ponuky, objednávky a faktúry. Pomocou stránok s informáciami o projekte pre tieto entity musíte vytvoriť príležitosti, cenové ponuky, objednávky a faktúry služby Project Service. Ak na vytvorenie záznamu použijete inú stránku, záznam sa nebude môcť otvoriť na stránke s **informáciami o projekte**. Ak chcete otvoriť záznam na stránke **projektové informácie**, musíte odstrániť záznam a znova ho použiť na stránke s **informáciami** o projekte. Na stránke **Projektové informácie** obchodná logika pre každý z týchto typov entít zaručuje, že pole **typ** záznamu je správne nastavené a všetky povinné koncepty sú správne inicializované.

> ![Informácie o projekte pre novú objednávku](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Rozdiely medzi Project Service Automation a predajom
Hoci proces predaja v PSA používa základné možnosti predajného procesu v predaji, to robí niektoré kľúčové rozdiely, kvôli rozdielom v obchodných praktikách založené organizácií založených na projektoch. Tu sú niektoré príklady:

- **Projektové cenové ponuky** - v Project Service Automation, je cenová ponuka uzavretá po vytvorení projektovej zmluvy z cenovej ponuky. V predaji môžete ponechať cenovú ponuku otvorenú potom, ako ju vyhráte. Dôvodom tohto rozdielu je, že zhoda medzi cenovou ponukou a projektovou zmluvou je lepšia pre organizácie založené na projekte. 
- **Aktivácia a revízie** – v PSA, Aktivácia a revízie nie sú podporované pre projektové cenové ponuky. V predaji môže byť cenová ponuka zamknutá, aby sa predišlo ďalším úpravám.
- **Zatvorenie cenovej ponuky ako stratenej alebo vyhranej** – v PSA, keď je cenová ponuka zatvorená ako vyhraná alebo stratená, príležitosť zostane otvorená. Všetky ostatné cenové ponuky na príležitosti sú uzavreté ako stratené. Pri predaji, keď je cenová ponuka uzavretá ako vyhraná alebo stratená, sa používateľovi zobrazí výzva na akciu na príležitosti. V závislosti od vstupu používateľa môže byť základná príležitosť zatvorená alebo ponechaná otvorená.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Sledovanie revízií cenových ponúk a projektových plánov v predajnom cykle
V PSA nie je možné sledovať revízie vykonané v cenovej ponuke. Namiesto toho musíte označiť existujúcu cenovú ponuku **uzavretú ako stratenú** a potom vytvoriť novú cenovú ponuku. Môžete skopírovať cenovú ponuku alebo klonovať cenové ponuky založené na projekte pomocou PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Sledovanie komentárov a schválení cenových ponúk a projektových zmlúv
Môžete spravovať preskúmanie a schvaľovanie cenových ponúk a projektových zmlúv pomocou záznamu múru a príspevkov. Vaša organizácia môže vytvoriť vlastné pracovné postupy a doplnky na priraďovanie, presmerovanie, eskaláciu a spravovanie upozornení na položkách kontroly a schvaľovania.
