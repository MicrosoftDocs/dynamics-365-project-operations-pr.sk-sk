---
title: Správa návrhov projektových faktúr
description: Táto téma poskytuje podrobnosti o spracovaní faktúr orientovaných na zákazníka v Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 61b43e05eb179e2b00189076290433dd72f89a6bc7ef72140fc1efd752149d43
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989930"
---
# <a name="manage-project-invoice-proposals"></a>Správa návrhov projektových faktúr

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Vaše fakturačné oddelenie môže spracovať návrhy projektových faktúr, ak sú splnené tieto dve podmienky:

  - Projektový manažér potvrdí pro forma faktúru v Microsoft Dataverse.
  - Všetky časovo a vecne nevyfakturované predajné transakcie, ktoré sú zahrnuté v pro forma faktúre, sa účtujú pomocou účtovného denníka **integrácie Project Operations** Dynamics 365.

Podľa týchto pokynov môžete dokončiť návrh faktúry projektu v Dynamics 365 Finance.

1. Skontrolujte fakturačné údaje týkajúce sa časových a vecných transakcií a zaúčtujte účtovný denník **Integrácia Project Operations**.
2. Skontrolujte fakturačné informácie a nájdite medzníky fakturácie s pevnou cenou.
3. Skontrolujte a naformátujte návrhy projektových faktúr.
4. Zaúčtujte a vytlačte projektové faktúry.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Spravujte fakturačné informácie v účtovnom denníku integrácie Project Operations

Skutočné hodnoty projektu vytvorené v Dataverse sú skontrolované a zaúčtované v aplikácii Finance účtovníkom projektu. Ďalšie informácie o práci s denníkom integrácie nájdete v časti [Denník integrácie v aplikácii Project Operations](../project-accounting/project-operations-integration-journal.md).

Skutočné náklady a nefakturované skutočné predaje sa do denníka integrácie pridávajú ako samostatné riadky:

  - Obstarávacia cena jednotky a suma nákladov pri predvolenom nastavení skutočných nákladov z transakcie skutočných nákladov projektu v Dataverse.
  - Jednotková predajná cena a suma predaja v nevyplatenej predajnej transakcii sú predvolené od skutočnej nevyfakturovanej predajnej transakcie v Dataverse.

### <a name="billing-sales-tax"></a>Fakturačná daň z predaja

Výpočet dane z predaja pre fakturáciu je určený prostredníctvom kombinácie polí **Skupina fakturovanej dane z predaja** a **Skupina dane z predaja fakturovanej položky** na nevyfakturovanom zázname o predaji v zázname **Integrácia Project Operations** v účtovnom denníku. Systém predvolene nastavuje tieto hodnoty poľa na základe nastavení na karte **Financie** na stránke **Parametre projektového riadenia a účtovníctva**.

- **Metóda skupiny dane z predaja** určuje predvolenú logiku skupiny dane z predaja:
  
  - **Projekt**: Vždy nastaví predvolenú skupinu fakturácie dane z predaja z projektu. Výberom možnosti **Zobraziť predvolené účtovníctvo** na stránke **Všetky projekty** môžete skontrolovať alebo zmeniť predvolenú skupinu fakturácie dane z predaja v projekte.
  - **Projektová zmluva**: Vždy nastaví predvolenú skupinu fakturácie dane z predaja z projektovej zmluvy. Výberom možnosti **Zobraziť predvolené účtovníctvo** na stránke **Projektové zmluvy** môžete skontrolovať alebo zmeniť predvolenú skupinu dane z predaja v projektovej zmluve.
  - **Zákazník**: Vždy nastaví predvolenú skupinu fakturácie dane z predaja zo zákazníka.
  - **Vyhľadávanie**: Bude prehľadávať všetky vyššie uvedené entity a vyberie prvú dostupnú hodnotu. Hľadanie sa začína entitou **Projekt**, potom entitou **Projektová zmluva** a nakoniec entitou **Zákazník**.

- **Metóda skupiny dane z predaja položky** určuje predvolenú logiku skupiny dane z predaja položky:
  
  - Pre typy časových, nákladových a poplatkových transakcií bude skupina dane z predaja fakturovanej položky vždy predvolená podľa entity **Kategória projektu**.
  - Pre materiálové typy transakcií je predvolená skupina dane z obratu fakturovanej položky na základe nastavenia **Metóda skupiny dane z predaja položky** v časti **Parametre projektového riadenia a účtovníctva**. Predvolené číslo položky je skupina DPH z položky z entity **Vydaný produkt**. Predvolená kategória je skupina DPH z položky z entity **Kategória projektu**.

### <a name="financial-dimensions"></a>Finančné dimenzie

Finančné dimenzie pre nevyfakturované záznamy o predaji v denníku **Integrácia Project Operations** sú predvolene z entity **Projekt**. Finančné dimenzie možno skontrolovať a upraviť výberom možnosti **Rozdeliť sumy**. Ak potrebujete zmeniť finančné dimenzie nevyfakturovaného záznamu o predaji po zaúčtovaní denníka integrácie, ale skôr ako sa potvrdí pro forma faktúra, prejdite na **Všetky projekty** > **Spravovať** > **Zaúčtované transakcie**, vyberte transakciu a potom vyberte **Proces** > **Upraviť účtovníctvo**.

### <a name="exchange-rates"></a>Výmenné kurzy

Nevyfakturovaná mena transakcie v Dataverse sa používa ako mena transakcie v aplikácii Finance a prevádza sa na účtovnú menu spoločnosti pomocou výmenných kurzov definovaných v aplikácii Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Spravujte finančné atribúty medzníkov fakturácie 

Riadky projektových zmlúv využívajúce fakturačný postup s pevnou cenou sa fakturujú prostredníctvom možnosti [Medzníky pevnej ceny](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Účtovník projektu môže skontrolovať medzníky fakturácie v aplikácii Finance, v časti **Projektové riadenie a účtovníctvo** > **Všetky projekty** > **Spravovať** > **Transakcie na účet**.

### <a name="billing-sales-tax"></a>Fakturačná daň z predaja

Hodnoty **Skupina dane z predaja** a **Skupina dane z predaja položky** sú predvolene z nastavení, keď sa v Dataverse vytvorí nový medzník fakturácie. Systém predvolene nastavuje hodnoty na tieto polia na základe nastavení na karte **Financie** na stránke **Parametre projektového riadenia a účtovníctva**.

- **Metóda skupiny dane z predaja** určuje predvolenú logiku položky **Skupina dane z fakturovaného predaja**:

    - **Projekt** vždy nastaví predvolenú skupinu fakturácie dane z predaja z projektu. Výberom možnosti **Zobraziť predvolené účtovníctvo** na stránke **Všetky projekty** môžete skontrolovať alebo zmeniť predvolenú skupinu dane z predaja v projekte.
    - **Projektová zmluva** vždy nastaví predvolenú skupinu fakturácie dane z predaja z projektovej zmluvy. Výberom možnosti **Zobraziť predvolené účtovníctvo** na stránke **Projektové zmluvy** môžete skontrolovať alebo zmeniť predvolenú skupinu dane z predaja v projektovej zmluve.
    - **Zákazník** vždy nastaví predvolenú skupinu fakturácie dane z predaja zo zákazníka.
    - **Vyhľadávanie** bude prehľadávať všetky entity z tohto zoznamu a vyberie prvú dostupnú hodnotu. Hľadanie sa začína entitou **Projekt**, potom entitou **Projektová zmluva** a potom entitou **Zákazník**.

- **Skupina s daňou z obratu položky s pevnou cenou** sa používa ako predvolená hodnota v poli **Skupina dane z obratu tovaru** pre míľnik fakturácie. Účtovník môže túto hodnotu skontrolovať a upraviť na stránke **Transakcie na účte**. Systém používa hodnotu z transakcie na účte pri vytváraní riadku návrhu faktúry projektu.
 

### <a name="financial-dimensions"></a>Finančné dimenzie

Predvolené finančné dimenzie pre medzník fakturácie s pevnou cenou sú stanovené v riadkoch zmlúv projektu. Prejdite na **Zmluvy o projekte** > **Zobraziť predvolené účtovníctvo** a na karte **Riadky zmluvy** vyberte **cenu riadku zmluvy**, potom nastavte hodnoty finančnej dimenzie, ktoré chcete použiť ako predvolené.

Účtovník projektu môže upravovať informácie o dani z predaja a finančných dimenziách na medzníkoch faktúr, kým sa nevytvorí návrh faktúry projektu.


## <a name="create-project-invoice-proposals"></a>Vytvorenie návrhov projektových faktúr

Návrhy projektových faktúr je možné skontrolovať v module **Projektové riadenie a účtovníctvo** v časti **Faktúry projektu** > **Návrhy faktúr projektu**.

Hlavička návrhu faktúry projektu sa vytvorí v aplikácii Finance, keď sa potvrdí pro forma faktúra v Dataverse. Pre jednoduchšie zosúladenie systém nastaví číslo návrhu faktúry projektu v aplikácii Finance na rovnaké číslo ako ID pro forma faktúry v Dataverse. Pretože pro forma faktúry nie sú nevyhnutne potvrdené v rovnakom poradí, v akom sú vytvorené, postupnosť čísiel návrhov faktúr projektu v službe Finance musí umožňovať zmeny na nižšie a vyššie čísla. Nakonfigurujte postupnosť čísel podľa nasledujúcich krokov:

1. V aplikácii Finance prejdite na **Správa organizácie** > **Číselné sekvencie** > **Číselné sekvencie**.
2. Vo filtri **Oblasť** vyberte **Projekty**.
3. Vo filtri **Odkaz** vyberte **Návrh faktúry**.
4. Pole **Spoločnosť** použite na filtrovanie každej právnickej entity s povolenou integráciou Project Operations Dataverse.
5. Otvorte **Podrobnosti o postupnosti čísel** a na karte **Všeobecné** nastavte:

    - **Povoliť zmeny používateľa: na nižší počet** = **Áno**
    - **Povoliť zmeny používateľa: na vyšší počet** = **Áno**

Riadky s návrhmi faktúr pre projekt pridáva systém pomocou pravidelného procesu **Import z pracovnej tabuľky** (**Projektový manažment a účtovníctvo** > **Pravidelné** > **Integrácia Project Operations** > **Import z pracovnej tabuľky**). Tento proces je možné spustiť manuálne alebo pomocou pravidelného plánu. Systém nepridá riadky do dokumentu návrhu faktúry, kým nebudú všetky riadky pripravené na fakturáciu. Časové a materiálové transakcie sú pripravené na fakturáciu, až keď sa zaúčtujú pomocou denníka **Integrácia Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Formátovanie a tlač návrhov faktúr

Účtovník projektu môže prispôsobiť výtlačok projektovej faktúry pomocou stránky **Naformátovať návrh faktúry** možností správy tlače.

### <a name="format-invoice-proposals"></a>Formátovanie návrhov faktúr

Stránka **Naformátovať návrhy faktúr** umožňuje zobrazenie vlastných zoskupovacích transakcií vo faktúre projektu zákazníka.

1. Na stránke **Návrh projektovej faktúry** vyberte **Tlač** > **Naformátovať návrh faktúry**.
2. Výberom možnosti **Nové** vytvoríte nové zoskupenie pre výtlačok faktúry projektu.
3. V poli **Podrobnosti/zhrnutie** vyberte možnosti pre toto zoskupenie:

    - Vyberte **Podrobnosti** na vytlačenie podrobností transakcie zákazníckej faktúry.
    - Vyberte **Súhrn** na vytlačenie súhrnu transakcie zákazníckej faktúry.

> [!NOTE]
> Výber v poli **Podrobnosti/zhrnutie** na stránke **Naformátovať návrh faktúry** prepíše možnosť vybranú v poli **Formát faktúry** na stránke **Návrhy faktúr** na vytlačenie podrobnej faktúry alebo súhrnnej faktúry.

- Vyberte riadky transakcií, ktoré chcete zahrnúť do tejto časti na karte **Dostupné transakcie** a vyberte **Zahrnúť transakcie** na ich presun na kartu **Vybrané transakcie**.
- Vyberte **Posunúť nahor** a **Posunúť nadol** na zmenu poradia sekcií.
- Vyberte **Ukážka pred tlačou** na náhľad naformátovanej faktúry.

### <a name="print-management"></a>Správa tlače

Správa tlače používa na tlač rôzne súbory správ, špecifikáciu cieľov a prispôsobenie textu päty pre faktúru. Správu tlače je možné nastaviť na úrovni modulu, tieto nastavenia však možno prepísať pre konkrétneho zákazníka, zmluvu alebo návrh faktúry. Pre prístup k tejto funkcii na stránke **Návrh projektovej faktúry** vyberte možnosť **Tlačiť** > **Správa tlače**.

Nastavenie správy tlače sa zobrazuje ako stromové zobrazenie, kde každá úroveň uzla zobrazuje dostupné dokumenty, ktoré je potrebné upraviť. Môžete priradiť vlastné výtlačky na úrovni modulu, zákazníka, zmluvy alebo návrhu faktúry. Ak chcete upraviť výtlačok pôvodného dokumentu, rozbaľte požadovaný uzol a vyberte **Pôvodná položka**. V poli **Formát zostavy** vyberte formát zostavy, ktorý sa má použiť na tlač. Môžete použiť vlastné formáty zostáv pomocou možnosti [Rámec riadenia obchodných dokumentov](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Zaúčtovanie návrhov faktúr

Po skontrolovaní a úprave faktúry a uspokojivom riadku návrhu faktúry skontrolujte súčty faktúry a daň z predaja. V skupine **Podrobnosti** vyberte **Súčty** a potom vyberte **Zaúčtovať** na zaúčtovanie faktúry.

Ak chcete zobraziť faktúru pred zaúčtovaním, zrušte začiarknutie políčka **Zaúčtovanie**. **Pro forma** sa vytlačí na faktúre na znak toho, že ide o vzor faktúry. Ak chcete vytlačiť faktúru, začiarknite políčko **Vytlačiť faktúru**.

Okrem stránky **Návrh faktúry** je možné zaslať návrhy faktúr spustením pravidelnej úlohy **Zaúčtovať návrhy faktúr**. Ak chcete nájsť túto úlohu, prejdite na **Projektové riadenie a účtovníctvo** > **Pravidelné** > **Faktúry projektu** > **Zaúčtovať návrhy faktúr**.

Táto stránka zobrazuje všetky návrhy faktúr, ktoré sú pripravené na zaúčtovanie. Výberom možnosti **Dávka** môžete naplánovať účtovanie návrhov faktúr. Nastavte **Parameter dávkového spracovania** na **Áno** a nastavte opakovanie dávkového spracovania výberom **Opakovanie**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
