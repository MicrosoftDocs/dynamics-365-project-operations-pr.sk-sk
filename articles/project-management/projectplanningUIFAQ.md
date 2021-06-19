---
title: Riešenie problémov s prácou v mriežke úloh
description: Táto téma poskytuje informácie o riešení problémov potrebných pri práci v mriežke úloh.
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213419"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Riešenie problémov s prácou v mriežke úloh 

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma popisuje, ako opraviť problémy, s ktorými sa môžete stretnúť pri práci so správou nákladov.

## <a name="enable-cookies"></a>Povoliť súbory cookie

Project Operations vyžaduje, aby boli povolené súbory cookie tretích strán, aby sa zobrazila štruktúra rozdelenia práce. Ak súbory cookie tretích strán nie sú povolené, namiesto zobrazenia úloh sa po výbere karty **Úlohy** na stránke **Projekt** zobrazí prázdna stránka.

![Prázdna karta, keď nie sú povolené súbory cookie tretích strán](media/blankschedule.png)


### <a name="workaround"></a>Riešenie
V prípade prehliadačov Microsoft Edge alebo Google Chrome nasledujúce postupy naznačujú, ako aktualizovať nastavenie prehliadača tak, aby boli povolené súbory cookie tretích strán.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Otvorte prehľadávač Edge.
2. V pravom hornom rohu vyberte **tri bodky** (...) a následne vyberte položku **Nastavenia**.
3. V časti **Súbory cookie a povolenia lokality** vyberte **Súbory cookie a údaje o lokalite**.
4. Vypnite **Blokovať súbory cookie tretích strán**.

#### <a name="google-chrome"></a>Google Chrome

1. Otvorte prehľadávač Chrome.
2. V pravom hornom rohu vyberte tri zvislé bodky a potom vyberte položku **Nastavenia**.
3. V časti **Ochrana osobných údajov a zabezpečenie** vyberte **Súbory cookie a iné údaje o lokalite**.
4. Vyberte **Povoliť všetky súbory cookie**.

> [!IMPORTANT]
> Ak zablokujete súbory cookie tretích strán, zablokujú sa všetky súbory cookie a údaje lokalít z iných webov, aj keď je tento web povolený vo vašom zozname výnimiek.

## <a name="pex-endpoint"></a>Koncový bod PEX

Project Operations vyžaduje, aby parameter projektu odkazoval na koncový bod PEX. Tento koncový bod je potrebný na komunikáciu so službou použitou na vykreslenie štruktúry rozdelenia práce. Ak parameter nie je povolený, zobrazí sa chyba „Parameter projektu nie je platný“. 

### <a name="workaround"></a>Riešenie
 ![Pole Koncový bod PEX v parametri projektu](media/projectparameter.png)

1. Pridajte pole **Koncový bod PEX** na stránke **Parametre projektu**.
2. Aktualizujte pole o túto hodnotu: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`
3. Odstráňte pole zo stránky **Parametre projektu**.

## <a name="privileges-for-project-for-the-web"></a>Oprávnenia pre Project for Web

Project Operations sa spolieha na externú plánovaciu službu. Táto služba vyžaduje, aby mal používateľ priradených niekoľko rol na čítanie a zápis do entít týkajúcich sa štruktúry rozdelenia práce. Medzi tieto entity patria projektové úlohy, priradenia zdrojov a závislosti úloh. Ak používateľ nemôže pri prechode na kartu **Úlohy** vykresliť štruktúru rozdelenia práce, je to pravdepodobne preto, že nebol povolený projekt pre Project Operations. Používateľ môže dostať buď chybu roly zabezpečenia, alebo chybu súvisiacu s odmietnutím prístupu.


## <a name="workaround"></a>Riešenie

1. Prejdite na **Nastavenie > Zabezpečenie > Používatelia > Používatelia aplikácie**.  

   ![Čítačka aplikácie](media/applicationuser.jpg)
   
2. Dvakrát kliknite na záznam používateľa aplikácie a overte nasledovné:

 - Používateľ má prístup k projektu. Toto overenie sa zvyčajne vykonáva tak, že sa zabezpečí, že používateľ má rolu zabezpečenia **Projektový manažér**.
 - Používateľ aplikácie Microsoft Project existuje a je správne nakonfigurovaný.
 
3. Ak tento používateľ neexistuje, môžete vytvoriť nový záznam používateľa. Vyberte **Noví používatelia**. Zmeňte formulár na zadávanie v časti **Používateľ aplikácie** a potom pridajte **ID aplikácie**.

   ![Podrobnosti o používateľovi aplikácie](media/applicationuserdetails.jpg)

4. Skontrolujte, či používateľovi bola pridelená správna licencia a či je služba povolená v podrobnostiach plánu služieb licencie.
5. Overte, či môže používateľ otvoriť project.microsoft.com.
6. Prostredníctvom parametrov projektu overte, či systém ukazuje na správny koncový bod projektu.
7. Overte, či je vytvorený užívateľ projektovej aplikácie.
8. Aplikujte na používateľa nasledujúce roly zabezpečenia:

  - Používateľ služby Dataverse
  - Systém riešenia Project Operations
  - Systém projektu

## <a name="error-when-updating-the-work-breakdown-structure"></a>Chyba pri aktualizácii štruktúry rozdelenia práce

Keď sa vykoná jedna alebo viac aktualizácií štruktúry rozdelenia práce, zmeny nakoniec zlyhajú a neuložia sa. V mriežke rozvrhu sa vyskytla chyba a upozornila, že „Poslednú zmenu, ktorú ste vykonali, sa nepodarilo uložiť.“

### <a name="workaround"></a>Riešenie

1. Skontrolujte, či používateľovi bola pridelená správna licencia a či je služba povolená v podrobnostiach plánu služieb licencie.
2. Overte, či môže používateľ otvoriť project.microsoft.com.
3. Overte, či systém ukazuje na správny koncový bod projektu.
4. Overte, či bol vytvorený užívateľ projektovej aplikácie.
5. Aplikujte na používateľa nasledujúce roly zabezpečenia:
  
  - Používateľ Dataverse alebo základný používateľ
  - Systém riešenia Project Operations
  - Systém projektu
  - Systém dvojitého zápisu Project Operations (táto rola je vyžadovaná, ak v Project Operations nasadzujete scenár založený na zdrojoch/chýbajúcich zdrojoch.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
