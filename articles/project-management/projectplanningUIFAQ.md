---
title: Riešenie problémov s prácou v mriežke úloh
description: Tento článok poskytuje informácie o riešení problémov potrebné pri práci v mriežke úloh.
author: ruhercul
ms.date: 07/22/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 208ed55abf4cdf0ad2b035bd923e183ff3cae660
ms.sourcegitcommit: e91136d3335ee03db660529eccacd48907774453
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/22/2022
ms.locfileid: "9188251"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Riešenie problémov s prácou v mriežke úloh 


_**Vzťahuje sa na:** Project Operations pre scenáre založené na zdrojoch/nenaskladnené, nasadenie Lite – dohoda o proforma fakturácii, Project for the Web_

Mriežka úloh, ktorú používa Dynamics 365 Project Operations je hostený prvok iframe v rámci Microsoft Dataverse. V dôsledku tohto použitia musia byť splnené špecifické požiadavky na zabezpečenie správneho fungovania autentifikácie a autorizácie. Tento článok popisuje bežné problémy, ktoré môžu ovplyvniť schopnosť vykresľovať mriežku alebo spravovať úlohy v štruktúre rozpisu práce (WBS).

Bežné problémy zahŕňajú:

- Karta **Úloha** na mriežke úloh je prázdna.
- Pri otváraní projektu sa projekt nenačíta a používateľské rozhranie (UI) sa zasekne na číselníku.
- Správa oprávnení pre **Project for the Web**.
- Pri vytváraní, aktualizácii alebo odstraňovaní úlohy sa zmeny neuložia.

## <a name="issue-the-task-tab-is-empty"></a>Problém: Karta Úloha je prázdna

### <a name="mitigation-1-enable-cookies"></a>Zmiernenie 1: Povoliť súbory cookie

Project Operations vyžadujú, aby boli súbory cookie tretích strán povolené na vykreslenie štruktúry rozdelenia práce. Ak nie sú povolené súbory cookie tretích strán, namiesto zobrazenia úloh sa po výbere možnosti zobrazí prázdna stránka **Úlohy** kartu na **Projekt** stránku.

V prípade prehliadačov Microsoft Edge alebo Google Chrome nasledujúce postupy naznačujú, ako aktualizovať nastavenie prehliadača tak, aby boli povolené súbory cookie tretích strán.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Otvorte prehľadávač Edge.
2. V pravom hornom rohu vyberte **tri bodky** (...) a následne vyberte položku **Nastavenia**.
3. V časti **Súbory cookie a povolenia lokality** vyberte **Súbory cookie a údaje o lokalite**.
4. Vypnite **Blokovať súbory cookie tretích strán**.
5. Obnovte prehliadač. 

#### <a name="google-chrome"></a>Google Chrome

1. Otvorte prehľadávač Chrome.
2. V pravom hornom rohu vyberte tri zvislé bodky a potom vyberte položku **Nastavenia**.
3. V časti **Ochrana osobných údajov a zabezpečenie** vyberte **Súbory cookie a iné údaje o lokalite**.
4. Vyberte **Povoliť všetky súbory cookie**.
5. Obnovte prehliadač. 

> [!NOTE]
> Ak zablokujete súbory cookie tretích strán, zablokujú sa všetky súbory cookie a údaje lokalít z iných webov, aj keď je tento web povolený vo vašom zozname výnimiek.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Zmiernenie 2: Overenie, či bol koncový bod PEX správne nakonfigurovaný

Project Operations vyžaduje, aby parameter projektu odkazoval na koncový bod PEX. Tento koncový bod je potrebný na komunikáciu so službou, ktorá sa používa na vykreslenie štruktúry rozdelenia práce. Ak parameter nie je povolený, zobrazí sa chyba „Parameter projektu nie je platný“. Ak chcete aktualizovať koncový bod PEX, vykonajte nasledujúce kroky.

1. Pridajte pole **Koncový bod PEX** na stránke **Parametre projektu**.
2. Identifikujte typ produktu, ktorý používate. Táto hodnota sa používa, keď je nastavený koncový bod PEX. Po načítaní je typ produktu už definovaný v koncovom bode PEX. Ponechajte si túto hodnotu.
3. Aktualizujte pole o túto hodnotu: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Nasledujúca tabuľka uvádza parameter typu, ktorý by sa mal použiť na základe typu výrobku.

      | **Typ produktu**                     | **Parameter typu** |
      |--------------------------------------|--------------------|
      | Project for the Web v predvolenej organizácii   | type=0             |
      | Project for the Web v organizácii s názvom CDS | type=1             |
      | Project Operations                   | type=2             |

4. Odstráňte pole zo stránky **Parametre projektu**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Zmiernenie 3: prihláste sa do project.microsoft.com

V prehliadači otvorte novú kartu, prejdite na project.microsoft.com a prihláste sa s rolou používateľa, ktorú používate na prístup k prevádzke projektu. Je dôležité, aby bol do produktu spoločnosti Microsoft v prehliadači prihlásený iba jeden používateľ. Chybové hlásenie „login.microsoftonline.com sa odmietol pripojiť“ sa najčastejšie vyskytuje, keď je prihlásených viac používateľov, ako je znázornené na nasledujúcom obrázku.

![Vyberte prihlasovaciu stránku účtu, na ktorej sú prihlásení dvaja používatelia.](media/MULTIPLE_USERS_LOGGED_IN.png)

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problém: Projekt sa nenačíta a používateľské rozhranie je prilepené na číselníku

Na účely autentifikácie musia byť pre načítanie mriežky úloh povolené kontextové okná. Ak vyskakovacie okná nie sú povolené, obrazovka sa prilepí na číselník načítania. Nasledujúci obrázok zobrazuje adresu URL so zablokovaným kontextovým štítkom v paneli s adresou, čo vedie k zaseknutiu rotujúceho pri pokuse o načítanie stránky. 

   ![Zaseknutý číselník a vyskakovací blok.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Zmiernenie 1: Povoliť vyskakovacie okná

Keď sa váš projekt zasekne na číselníku, je možné, že nie sú povolené kontextové okná.

#### <a name="microsoft-edge"></a>Microsoft Edge

Vo vašom prehliadači Edge existujú dva spôsoby, ako povoliť vyskakovacie okná.

1. V prehliadači Edge vyberte upozornenie v pravom hornom rohu prehliadača.
2. Vyberte **Vždy povoliť kontextové okná a presmerovania z** konkrétneho prostredia Dataverse.
 
     ![Vyskakovacie okná zablokovali okno.](media/enablepopups.png)

Prípadne môžete tiež urobiť jeden z týchto úkonov.

1. Otvorte prehľadávač Edge.
2. V pravom hornom rohu vyberte ikonu **elipsy** (...), a potom vyberte **Nastavenia** > **Povolenia stránok** > **Vyskakovacie okná a presmerovania**.
3. Prepnite **Vyskakovacie okná a presmerovania** na blokovanie kontextových okien alebo ich zapnutím povoľte na svojom zariadení kontextové okná.
4. Po povolení vyskakovacích okien obnovte prehliadač. 

#### <a name="google-chrome"></a>Google Chrome
1. Otvorte prehľadávač Chrome.
2. Prejdite na stránku, kde sú blokované kontextové okná.
3. V paneli s adresou zvoľte **Vyskakovacie okno je zablokované**.
4. Vyberte odkaz na vyskakovacie okno, ktoré chcete vidieť.
5. Po povolení vyskakovacích okien obnovte prehliadač. 

> [!NOTE]
> Ak chcete, aby sa na stránke vždy zobrazovali kontextové okná, vyberte položku **Vždy povoliť kontextové okná a presmerovania z [web]** a potom vyberte **Hotovo**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problém 3: Správa oprávnení pre Project for the Web.

Project Operations sa spolieha na externú plánovaciu službu. Služba vyžaduje, aby mal používateľ priradených niekoľko rolí, ktoré mu umožňujú čítať a zapisovať do entít súvisiacich s WBS. Medzi tieto entity patria projektové úlohy, priradenia zdrojov a závislosti úloh. Ak používateľ nemôže vykresliť WBS, keď prejde na **Úlohy** kartu, je to pravdepodobne preto **Projekt** pre **Projektové operácie** nebolo povolené. Používateľ môže dostať buď chybu roly zabezpečenia, alebo chybu súvisiacu s odmietnutím prístupu.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Zmiernenie 1: Overte roly zabezpečenia používateľa aplikácie a koncového používateľa

1. Prejdite na **Nastavenie** > **Zabezpečenie** > **Používatelia** > **Používatelia aplikácie**.  

   ![Čítačka aplikácie.](media/applicationuser.jpg)
   
2. Dvojitým kliknutím na záznam používateľa aplikácie overíte:

     - Používateľ má prístup k projektu. Môžete to urobiť tak, že overíte, že používateľ má rolu zabezpečenia **Projektový manažér**.
     - Používateľ aplikácie Microsoft Project existuje a je správne nakonfigurovaný.
 
3. Ak tento používateľ neexistuje, vytvorte nový záznam používateľa. 
4. Vyberte **Noví používatelia**, zmeňte vstupný formulár na **Používateľ aplikácie**, a potom pridajte **ID aplikácie**.

   ![Podrobnosti o používateľovi aplikácie.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problém 4: Pri vytváraní, aktualizácii alebo odstraňovaní úlohy sa zmeny neuložia

Keď vykonáte jednu alebo viac aktualizácií WBS, zmeny sa nepodaria a neuložia sa. V mriežke plánu sa zobrazí chyba so správou, že „Nedávne zmeny, ktoré ste vykonali, sa nepodarilo uložiť“.

### <a name="mitigation-1-validate-the-license-assignment"></a>Zmiernenie 1: Overte priradenie licencie

1. Skontrolujte, či používateľovi bola pridelená správna licencia a či je služba povolená v podrobnostiach plánu služieb licencie.  
2. Overte, či môže používateľ otvoriť **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Zmiernenie 2: Konfigurácia overenia používateľa aplikácie Project
1. Overte, či bol vytvorený užívateľ aplikácie Project.
2. Aplikujte na používateľa nasledujúce roly zabezpečenia:
  
  - Používateľ Dataverse alebo základný používateľ
  - Systém riešenia Project Operations
  - Systém projektu
  - Systém duálneho zápisu Project Operations Táto rola je potrebné pre scenáre nasadenia na základe zdroja/nenaskladnenia v rámci Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
