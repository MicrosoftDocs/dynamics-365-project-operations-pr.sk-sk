---
title: Ako môžem predbežne zarezervovať zdroje vo verzii aplikácie 2.x?
description: Tento článok popisuje ako predbežne zarezervovať členov tímu projektu pomocou Project Service.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Applies to Project Service version 2.x
ms.technology: ''
ms.assetid: 27063de4-cb0c-436f-970e-c87ebcab92db
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: aad119c0907cdd31220a0d73e6e7d99ee63e2e13
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755596"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Ako môžem predbežne zarezervovať zdroje vo webovej aplikácii (aplikácia Project Service v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Predbežne môžete naplánovať alebo predbežne zarezervovať zdroj do tímu projektu, aby sa zobrazil váš plán priradenia zdroju k projektu. Predbežné rezervácie nespotrebúvajú dostupnú kapacitu zdroja. Členovia tímu, ktorí sú predbežne rezervovaní, nemôžu byť priradení k úlohám projektu. K úlohám možno priradiť iba zdroje so stavom Pevne rezervované a typom potvrdenia Potvrdené (za predpokladu, že majú dostatok hodín pevnej rezervácie, ktoré pokryjú snahu priradenia).

Členovia tímu projektu s predbežnou rezerváciou sa zobrazia v mriežke člena tímu s predbežne zarezervovanými hodinami zobrazenými v stĺpci Predbežne rezervovať Zobrazia sa tiež na tabuli plánu. Znova nesignalizujú žiadnu spotrebu kapacity, pretože predbežná rezervácia nespotrebúva kapacitu zdroja.

Existujú tri spôsoby predbežnej rezervácie člena tímu k projektu pomocou Project Service verzie 2.x. Môžete vykonať predbežnú rezerváciu s tabuľou plánu, použiť funkciu správy rezervácií alebo vytvoriť všeobecnú rezerváciu. Tieto metódy sú popísané nižšie.

## <a name="soft-book-with-the-schedule-board"></a>Predbežná rezervácia použitím tabule plánovania

Na predbežnú rezerváciu pomocou tabule plánovania postupujte nasledovne: 
1. Otvorte tabuľu plánovania.
2. Zvoľte si kartu Projekt v spodnej časti panela Požiadavky na rezervácie tabule plánovania.
3. Vyhľadajte si projekt, ku ktorému chcete predbežne zarezervovať zdroj. Ak máte veľa projektov, kliknite na hlavičku stĺpca projekt a potom použite filter na vyhľadanie projektu.
4. Kliknite na projekt a potom potiahnite a pustite ho na časovú os zdroja.
5. Tým sa vpravo otvorí panel vytvorenia zdroja rezervácie. Upravte dátum začiatku a ukončenia, zvoľte si stav rezervácie ako predbežná a nastavte hodiny. 
6. Kliknite na rezervovať.
7. Späť v projekte sa zdroj začne zobrazovať ako člen tímu s predbežne zarezervovanými hodinami v stĺpci Predbežná rezervácia.

Upozorňujeme, že ich nemožno priraďovať k úlohám v štruktúre rozdelenia práce (WBS), pretože zdroje sa musia na priradenie k tímu zarezervovať pevne.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Predbežná rezervácia použitím funkcie Spravovať rezervácie

Na predbežnú rezerváciu pomocou funkcie Spravovať rezervácie postupujte nasledovne:
1. Na mriežke člena tímu kliknite na tlačidlo Nové.
2. Zvoľte si rezervovateľný zdroj, rolu, od/do.
3. Vyberte metódu prideľovania inú než Žiadne:
- Plná kapacita
- Kapacita v percentách
- Podľa rovnomerne rozmiestnených hodín
- Podľa hodín počiatočného vyťaženia
4. Kliknite na tlačidlo Uložiť. Na mriežke tímu uvidíte zdroj a ich spolu s hodinami, ktorý bude mať označenie Pevný.
5. Spravujte rezerváciu zdrojov kliknutím na možnosť Spravovať rezervácie.
6. Po otvorení tabule plánovania si rozbaľte zdroj, čím si zobrazíte jeho rezervácie. Stav rezervácie bude Pevná.
7. Kliknite pravým tlačidlom myši na rezerváciu. V časti Zmena stavu si zvoľte možnosť Predbežná rezervácia a potom Predbežne. Stav rezervácie bude Predbežne.
8. Po zatvorení tabule plánu uvidíte, že hodiny zdroja sa zmenili z Pevné na Predbežne na mriežke člena tímu.
Upozorňujeme, že ak pevne zarezervujete zdroj do tímu a následne im priradíte úlohy vo WBS, potom použijete správu rezervácií na zmenu stavu z Pevné na Predbežné. Odstráni sa priradenie z úloh daného zdroja, pretože iba pevne rezervované zdroje možno priradiť k úlohám.

## <a name="soft-book-by-creating-a-generic-resource"></a>Predbežná rezervácia všeobecného zdroja

Predbežnú rezerváciu možno vytvoriť vytvorením všeobecného zdroja člena tímu, vyplnením pomocou tabule plánovania alebo požiadavky na zdroj a zmenou typu počas rezervácie.
Urobte tak nasledovným postupom:

1. Na projekte WBS priraďte roly k úlohám, pre ktoré chcete vygenerovať všeobecných členov tímu.
2. Kliknite na možnosť Generovať projektový tím.
3. Na mriežke členov projektového tímu si vyberte všeobecný zdroj a kliknite na možnosť Rezervovať.
4. Na tabuli plánovania si zvoľte zdroj, ktorý si chcete zarezervovať.
5. Na paneli tabule plánovania Vytvoriť rezerváciu zdroja zmeňte stav rezervácie na Predbežná.
6. Kliknite na možnosť Rezervovať alebo Rezervovať a ukončiť.

Po zatvorení panelu plánovania sa vám zobrazí vybratý zdroj pridaný k tímu s predbežne zarezervovanými hodinami spolu s priradenými hodinami. Uvidíte tiež, že všeobecný prostriedok zostáva v tíme ako indikátor priradené úlohy jednotlivým predbežne zarezervovaným členom tímu.

Keď budete pripravený na zmenu predbežne rezervovaného zdroja člena tímu na pevne rezervovaného člena tímu, aby ste ich mohli priradiť k úlohám, postupujte nasledovne:

1. Označte zdroj a kliknite na možnosť Spravovať rezervácie.
2. Po otvorení tabule plánovania si rozbaľte zdroj, čím si zobrazíte jeho rezervácie. Zobrazí sa vám rezervácia označená ako Predbežná.
3. Kliknite pravým tlačidlom myši na rezerváciu. V časti Zmena stavu si zvoľte možnosť Pevná rezervácia a potom Pevná. Stav rezervácie bude Pevná.
4. Po zatvorení tabule plánu uvidíte, že hodiny zdroja sa zmenili z Predbežné na Pevné na mriežke člena tímu. Odteraz možno priraďovať zdroj k úlohám (za predpokladu, že je rovnováha medzi pevne zarezervovanými hodinami a hodinami úsilia pre priradenie). Upozorňujeme, že v prípade dodržania krokov vypĺňania všeobecného zdroja v položke 3, pri zmene stavu predbežne rezervovaného rezervovateľného zdroja na pevný, sa z tímu odstráni všeobecný člen tímu.
