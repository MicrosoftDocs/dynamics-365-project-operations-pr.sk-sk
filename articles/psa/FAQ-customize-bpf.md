---
title: Ako prispôsobiť projektové fázy toku obchodného procesu?
description: Prehľad ako môžte prispôsobiť tok obchodného procesu v rámci etáp projektu?
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2dccc33088cd9e49e7ffe609f9d9754ef33a5dba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084550"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Ako prispôsobiť projektové fázy toku obchodného procesu?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Je známe obmedzenia v starších verziách aplikácie Project Service že mená etapy projektu fázach pracovného procesu sa musia presne s očakávanými anglickými názvami ( **Quote** , **Plan** , **Close** ). V opačnom prípade nebude obchodná logika, ktorá sa spolieha na názvy fáz v angličtine, pracovať podľa očakávaní. To je dôvod, prečo nevidíte známe akcie, akými sú **Prepnúť proces** alebo **Upraviť proces** na formulári projektu a nie je podporovaná ani možnosť prispôsobenia toku obchodného procesu. 

Toto obmedzenie bolo vyriešené vo verzii 2.4.5.48 a novšej. Tento článok poskytuje navrhované riešenia pre staršie verzie, ak potrebujete prispôsobenie predvoleného toku obchodného procesu pre staršie verzie.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Obchodná logika si vyžaduje presnú zhodu s anglickými názvami fáz

Projektové fázy toku obchodných procesov zahŕňajú obchodnú logiku, ktorá poháňa nasledujúce správania v aplikácii:
- Keď sa projekt priradí k cenovej ponuke, kód nastaví tok obchodného procesu na fázu **Quote**.
- Keď sa projekt priradí ku zmluve, kód nastaví tok obchodného procesu na fázu **Plan**.
- Keď tok obchodného procesu prejde do fázy **Close** , záznam projektu sa deaktivuje. Ak je deaktivovaný projektu, projektový formulár a prácu štruktúru činností (WBS) sú nastavené iba na čítanie, pomenovaných zdrojov rezervácie sú uvoľnené a akékoľvek priradené Cenníky sú deaktivované.

Tento biznis logika sa opiera o anglické názvy pre fázy projektu. Táto závislosti na anglických názvoch fáz predstavuje hlavný dôvod, prečo sa neodporúča upravovať fázy projektu toku obchodného procesu. Rovnako pre to tiež nevidíte spoločné akcie toku obchodných procesov, akými je **Prepnúť proces** alebo **Upraviť proces** v entite projektu.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Čo sa stane, ak sa názov fázy nebude hodovať s anglickými názvami?

V aplikácii Project Service verzie 1.x na platforme 8.2, keď sa názov etapy v toku obchodných procesov presne nezhodujú s anglickými názvami etapy, obchodná logika, ktorá nastavuje správnu etapu cenových ponúk alebo zmlúv, alebo tá, ktorá projektu uzatvára, bude preskočená. Nezobrazia sa žiadne chybové hlásenia. Z toho dôvodu sa zdá, že nemôžete upravovať tok obchodného procesu fáz projektu. Nezobrazia sa vám však ani žiadne automatické procesy pracujúce na cenových ponukách, zmluvách a uzatváraní projektu.

V aplikácii Project Service verzie 2.4.4.30 alebo novšej na platforme 9.0 došlo k výraznej architektonickej zmene toku obchodných procesov, ktorá si vyžadovala prepísanie obchodnej logiky toku obchodného procesu. Výsledkom je, že v prípade, ak sa názvy etapy procesu nezhodujú s očakávanými anglickými názvami, zobrazí sa vám chybové hlásenie. 

Preto ak chcete prispôsobiť projektové fázy pracovného procesu pre projekt entitu, môžete len pridať zbrusu novej etapy do predvoleného pracovného procesu pre projekt subjektu, pričom ponecháte etapy **Cenová ponuka** , **Plán** a **Zavrieť** tak, ako sú. Toto obmedzenie zaisťuje, že sa vám nebudú zobrazovať chyby z obchodnej logiky, ktorá očakáva v toku obchodných procesov anglické názvy etáp.

Vo verzii 2.4.5.48 alebo novšej bola obchodná logika popísaná v tomto článku odstránená z predvoleného toku obchodného procesu pre entitu projektu. Inováciou na danú alebo novšiu verziu budete môcť upravovať alebo nahrádzať predvolený tok obchodného procesu tým vlastným. 

## <a name="workarounds-for-earlier-versions"></a>Riešenia pre staršie verzie

Ak inovácia nie je možnosť, môžete prispôsobiť projektové fázy toku obchodného procesu pre projektovú entitu jedným z týchto dvoch spôsobov:

1. Pridať ďalšie etapy s predvolenou konfiguráciou, pri zachovaní anglicky fáze mená pre **Cenová ponuka** , **Plán** , a **Zavrieť**.


![Snímka obrazovky pridávania etáp k predvolenej konfigurácii](media/FAQ-Customize-BPF-1.png)
 
2. Vytvorte si vlastný tok obchodných procesov a nastavte ho ako hlavný tok obchodných procesov pre entitu projektu, čo vám umožní mať ľubovoľné názvy etáp. Ak však chcete používať rovnaké štandardné projektové etapy **Cenová ponuka** , **Plán** a **Zatvoriť** , budete musieť vykonať niekoľko prispôsobení, ktoré sú odvodené od vlastných názvov etáp. Komplexnejšia logika sa využíva pri zatváraní projektu, čo možno aj naďalej spustiť obyčajnou deaktiváciou záznamu projektu.

![Prispôsobenie BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Ďalšie pokyny pre aplikáciu Project Service verzie 2.4.4.30 alebo staršej na platforme 9.0

V Project Service 2.4.4.30 alebo staršej na platforme 9.0 sa s vlastným tokom obchodného procesu pole **Názov etapy** v projektovej entite použitej v grafe **Projekt podľa etapy** v zobrazení zoznamov projektov neaktualizuje, pretože je spojené s predvoleným tokom obchodných procesov projektových etáp. Tento problém možno riešiť nasledovným postupom:

- Pridajte vlastné pole, ktoré zachytí aktuálnu etapu toku obchodného procesu, ktorá sa aktualizuje vtedy, keď používateľ pokračuje vo vlastnom toku obchodného procesu.

- Upravte graf **Projekt podľa etapy** tak, aby vyhovoval vlastnému poľu a nie predvolenej konfigurácii.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Kroky na vytvorenie vlastného toku obchodného procesu pre entitu projektu

Na vytvorenie vlastného toku obchodného procesu pre entitu projektu postupujte nasledovne:

1. Prejdite do časti **Nastavenia** > **Centrum spracovania**. Nekopírujte projektové fázy toku obchodného procesu, pretože sa tým skopíruje aj obchodná logika Project Service.

  ![Vytvoriť proces](media/FAQ-Customize-BPF-3.png)

2. Návrhár procesov použite na vytvorenie požadovaných názvov etapy. Ak chcete rovnaké funkcie ako predvolené etapy pre **Cenová ponuka** , **Plán** a **Zavrieť** , budete to musieť vytvoriť na základe vlastných názvov fáz toku obchodného procesu.

   ![Snímka obrazovky návrhára procesov použitého pri prispôsobovaní BPF](media/FAQ-Customize-BPF-4.png) 

3. V návrhárovi procesu kliknite na možnosť **Tok procesu objednávky** a nastavte vlastný tok obchodných procesov ako hlavný tok obchodných procesov pre entitu projektu jeho presunutím nad etapy projektu toku obchodného procesu do hornej časti zoznamu.


   [Snímka obrazovky používania Toku procesu objednávky](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Nasledujúce kroky platia pre aplikáciu Project Service 2.4.4.30 alebo staršiu na platforme 9.0

4. Pridajte nové vlastné pole k entite projektu tak, aby zachytilo vlastné etapy vo vlastnom toku obchodných procesov. Budete musieť pridať obchodnú logiku (plugin/workflow) na aktualizáciu tohto poľa po aktualizácii etapy vo vlastnom toku obchodných procesov.

   ![Snímka obrazovky prispôsobenia projektovej entity](media/FAQ-Customize-BPF-6-720.png)

5. Upravte graf **Projekt podľa etapy** a použite nové vlastné pole pre etapy.

   ![Snímka obrazovky použitia grafu Projekt podľa etapy](media/FAQ-Customize-BPF-7-720.png)

6. Upravte akékoľvek zobrazenia pre entity projektu ,ktoré budú zahŕňať vaše nové vlastné pole pre etapy.

   ![Snímka obrazovky úpravy zobrazení projektovej entity](media/FAQ-Customize-BPF-8-720.png)

