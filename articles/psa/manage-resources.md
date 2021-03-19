---
title: Spravujte zdroje
description: Táto téma poskytuje informácie o tom, ako spravovať zdroje.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d47be6c11ced70b94b7497dfbc0c67d1a3f631b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275017"
---
# <a name="manage-resources"></a>Spravujte zdroje

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation obsahuje tabuľu správcu zdrojov, ktorá poskytuje vizuálny prehľad dopytu a využitia zdrojov v celej organizácii. Grafy na tejto tabuli môžete použiť na vizualizáciu nasledujúcich informácií:

- **Dopyt po zdrojoch** – graf **požiadavky na aktívny zdroj** zobrazuje zdroje, ktoré boli odoslané. Zdroje sú agregované buď rolou alebo projektom.
- **Dopyt na nepredložený zdroj** – graf **dopytu na nepriradené zdroje** zobrazuje všetky požiadavky na zdroje, ktoré neboli predložené. Pomáha správcom zdrojov zobraziť dopyt, ktorý nie je pevný a môže byť predložený prostredníctvom žiadosti o prostriedky.
- **Fakturovateľné využitie za uplynulý týždeň** – graf **využitia rolí** zobrazuje percento skutočného fakturovateľného využitia organizácie podľa roly proti jeho cieľovému fakturovateľnému využitiu podľa roly.

    > [!NOTE]
    > Aby bol graf **využitia rolí** k dispozícii, vytvorte prácu, ktorá spúšťa pracovný postup UpdateRoleUtilization. Táto opakovaná úloha sa spúšťa každých sedem dní na výpočet fakturovateľného využitia za predchádzajúcich sedem dní. Výsledky sú agregované podľa role.

## <a name="manage-project-team-members"></a>Spravujte členov projektového tímu

Projektoví manažéri môžu na spravovanie zdrojov na projektoch použiť tabuľu správca prostriedkov. Napríklad môžu pridať člena tímu priamo do projektu a rezervovať člena tímu, aby splnil požiadavky na zdroje, ktoré boli zachytené všeobecným prostriedkom.

### <a name="add-a-team-member-directly-to-a-project"></a>Pridajte člena tímu priamo do projektu

Ak chcete pridať člena tímu priamo do projektu, na stránke **projekty** na karte **tím** vyberte položku **nové**. Zobrazí sa dialógové okno **rýchle vytvorenie člena projektového tímu**. V tomto dialógovom okne môžete vykonávať tieto úlohy:

- **Rezervujte si pomenovaný zdroj** – v poli **rezervovateľné zdroje** vyberte názov zdroja. Potom vyberte rolu, nastavte obdobie a vyberte spôsob pridelenia. Pomenovaný zdroj, ktorý ste vybrali, sa pridá do projektu pomocou vybratej metódy prideľovania a zdrojového kalendára.
- **Pridať všeobecný zdroj** – ponechajte prázdne pole **rezervovateľného zdroja** a potom vyberte rolu, nastavte obdobie a vyberte preferovaný spôsob pridelenia. Všeobecný zdroj sa pridá do tímu ako zástupný symbol, aby držal vzor dopytu, ktorý sa používa na rezerváciu pomenovaných zdrojov v tíme. Požiadavka sa vykonáva v súlade s kalendárom projektu.
- **Pridanie pomenovaného zdroja do tímu bez spotreby kapacity zdrojov** – v poli **rezervovateľné zdroje** vyberte zdroj. Potom vyberte obdobie a vyberte **Nič** ako spôsob pridelenia. Zdroj sa pridá do tímu, ale kapacita zdroja nie je spotrebovaná prostredníctvom rezervácie.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezervujte si člena tímu, tak aby splnil požiadavky na zdroje pre všeobecný zdroj

V PSA si môžete rezervovať všeobecný zdroj v projektovom tíme a môžete špecifikovať úlohu, požadovanú kapacitu a spôsob rozdelenia tejto kapacity. V požiadavke na zdroj môžete zadať atribúty, ktoré súvisia so všeobecným zdrojom. Tieto atribúty zahŕňajú požadované zručnosti, preferovanú organizačnú jednotku a preferované zdroje.

Ak chcete určiť požadované zručnosti na všeobecný zdroj pre vývojára, postupujte podľa týchto krokov.

1. Na stránke **projekty** na karte **tím** vyberte položku **nové**, ak chcete rezervovať všeobecný zdroj.

    ![Všeobecný zdroj rezervovaný pre tím](media/Resource-Management-image9.png)

2. V zobrazení **všetci členovia tímu** v stĺpci **požiadavka zdroja** vyberte prepojenie na pridanie požadovaných zručností pre všeobecný zdroj.

    ![Odkaz na požiadavku](media/Resource-Management-image10.png)

3. Na stránke **požiadavky na zdroje**, ktorá sa zobrazí v mriežke **zručnosti** , vyberte elipsu (**...**) a potom vyberte **pridať novú charakteristiku požiadavky** pre pridanie požadovaných zručnosti pre vývojárov.

    ![Pridajte príkaz nová charakteristika požiadavky](media/Resource-Management-image11.png)

4. V dialógovom okne **rýchle vytvorenie: charakteristika požiadavky**, ktoré sa zobrazí v poli **charakteristika**, vyberte požadované zručnosti. Potom v poli **hodnota hodnotenia** vyberte úroveň odbornosti pre danú zručnosť. Nakoniec v poli **požiadavka na zdroj** nastavte požiadavku na zdrojové prostriedky z organizačných jednotiek alebo dokonca pomenovaných zdrojov. Po dokončení vyberte **Uložiť**.

    ![Rýchle vytvorenie: dialógové okno vlastnosti požiadavky](media/Resource-Management-image12.png)

5. Na stránke **požiadavky na zdroje** vyberte položku **rezervovať**, čím sa splní požiadavka na zdroje.

    ![Tlačidlo rezervovať na stránke požiadavky na zdroje](media/Resource-Management-image13.png)

    Môžete tiež vybrať všeobecný prostriedok v mriežke **všetci členovia tímu** a potom vyberte položku **rezervovať.**

    ![Tlačidlo rezervovať nad mriežkou Všetci členovia tímu](media/Resource-Management-image14.png)

    > [!NOTE]
    > V tomto príklade je 40 požadovaných hodín, ale žiadne aktuálne rezervované hodiny, pretože všeobecné zdroje nemajú rezervácie. Okrem toho nie sú priradené žiadne hodiny, pretože všeobecný zdroj bol pridaný priamo do tímu. Nebolo pridané pomocou priradenia úlohy.

    Na stránke **asistent plánovania** môžete filtrovať dostupné zdroje podľa požiadaviek, ktoré sú zadané v požiadavke na zdroj. Zdroje sú zoradené podľa parametrov zoradenia, ktoré sú špecifikované na tabuli plánovania.

    ![Stránka Asistent plánovania](media/Resource-Management-image15.png)

    Tu sú niektoré filtre, ktoré sa často používajú:

    - **Charakteristika spolu s hodnotením** - Filter podľa zručností, certifikácií a ďalších zdrojov kvality, okrem hodnotenia odbornosti.
    - **Roly** – Filter podľa predvolených rolí priradených k rezervovateľným zdrojom.
    - **Organizačné jednotky** – Filter rezervovateľné zdroje organizačnými jednotkami, ku ktorým sú priradené.

6. Ak nie ste spokojní s výsledkami úvodného vyhľadávania požiadaviek, môžete zmeniť kritériá filtra. Rozbaľte panel **zobrazenie filtra** na ľavej strane a potom vyberte položku **Hľadať** a vyhľadajte ďalšie zdroje.

    ![Panel filtrovať zobrazenie](media/Resource-Management-image16.png)

7. Ak chcete zmeniť spôsob zoradenia výsledkov, vyberte **zoradiť**.

    ![Príkaz Zoradiť](media/Resource-Management-image17.png)

8. Vyberte zdroje podľa dopytu, ktorý je špecifikovaný v požiadavke, ako je uvedené v hornej časti mriežky. Môžete vymazať výber buniek v mriežke a ponechať kapacitu zdroja otvorenú. Ako rezervované je možné vybrať len jeden zdroj naraz.

9. Vyberte **rezervovať**, ak chcete rezervovať vybratý zdroj a nechať otvorenú panel plánovania, aby ste mohli vybrať ďalšie zdroje. Prípadne vyberte položku **rezervovať & východ**, ak chcete rezervovať vybratý zdroj a zatvoriť panel plánovania.

    ![Zdroj, ktorý sa má rezervovať](media/Resource-Management-image19.png)

    Zobrazí sa upozornenie o rezervovaní hodín. Indikátory dopytu ukazujú, nakoľko je požiadavka na rezerváciu splnená a koľko zostáva. Môžete tiež zistiť, koľko kapacity vybratého prostriedku sa spotrebuje. Výberom **rozbaliť** zobrazíte ďalšie podrobnosti o rezerváciách zdrojov.

9. Vráťte sa do zobrazenia **všetci členovia tímu** . V mriežke si všimnite, že všeobecný prostriedok bol nahradený názvom prostriedku a 40 hodín je uvedených ako rezervované pre daný zdroj.

    ![Aktualizovaná mriežka všetkých členov tímu](media/Resource-Management-image20.png)

    > [!NOTE]
    > Nie sú zobrazené žiadne priradené hodiny, pretože boli rezervované priamo v tíme. Neboli rezervované pomocou priradenia úloh.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Priradenie všeobecných zdrojov k úlohe a generovanie zdrojových požiadaviek

V PSA môžete vytvárať úlohy a potom im priradiť všeobecné zdroje. Týmto spôsobom môže byť dopyt po zdroji zastupovaný zástupnými symbolmi, zatiaľ čo vy odhadnete svoj rozvrh a finančné čísla. Potom môžete generovať požiadavky na zdroje pre všeobecné zdroje a naplniť ich.

1. Na stránke **projekty**, na karte **plán** vyberte položku **pridať** a vytvorte úlohu.

    ![Nová úloha vytvorená](media/Resource-Management-image21.png)

2. V poli **zdroje** vyberte symbol **výberu zdroja**. Zobrazí sa výber zdrojov a zobrazí existujúcich členov tímu projektu.

    ![Výber zdroja](media/Resource-Management-image22.png)

3. Zadajte názov nového všeobecného prostriedku a potom vyberte položku **vytvoriť.**

    ![Názov nového všeobecného zdroja zadaný](media/Resource-Management-image23.png)

4. V dialógovom okne **rýchle vytvorenie: člena projektového tímu**, ktoré sa zobrazí v poli **rola**, vyberte rolu pre všeobecné zdroje. V poli **zdrojová jednotka** vyberte organizačnú jednotku pre všeobecný zdroj. Potom vyberte **Uložiť**.

    ![Zobrazí sa dialógové okno rýchle vytvorenie: člena projektového tímu.](media/Resource-Management-image24.png)

    Člen všeobecného tímu je teraz priradený k úlohe.

    ![Člen všeobecného tímu je priradený k úlohe.](media/Resource-Management-image25.png)

    Na karte **tím** sa zobrazí nový všeobecný člen tímu. Všimnite si, že má len pridelené hodiny. Tieto hodiny sú súčtom všetkých úloh, ktoré sú priradené všeobecnému členovi tímu. Všeobecný člen tímu ešte nemá požadované hodiny alebo požiadavku na zdroje.

    ![Všeobecný člen tímu na karte tím](media/Resource-Management-image26.png)

5. Teraz môžete priradiť všeobecného člena tímu k iným úlohám pomocou výberu zdrojov.

    ![Všeobecný člen tímu vo výbere zdrojov](media/Resource-Management-image27.png)

    Po dokončení priraďovania všeobecného zdroja k úlohám môžete vygenerovať požiadavku zdroja pre všeobecný zdroj.

5. Na karte **tím** vyberte všeobecný zdroj a potom vyberte **generovať požiadavku.**

    ![Príkaz generovať požiadavku](media/Resource-Management-image28.png)

    Po vygenerovaní požiadavky, všeobecný člen tímu bude mať požadované hodiny a odkaz na zdroj požiadavky.

    ![Odkaz na požiadavku na zdroj](media/Resource-Management-image29.png)

    Po dokončení rezervácie pomenovaného zdroja sa všeobecný zdroj odstráni z tímu a je nahradený pomenovaným zdrojom.

    ![Všeobecný prostriedok nahradený pomenovným zdrojom](media/Resource-Management-image30.png)

    Na karte **plán** sa všeobecné priradenia zdrojov odstránia a nahradia názvom zdroja.

    ![Na karte plán sa priradenia všeobecných zdrojov odstránia a nahradia sa názvom zdroja.](media/Resource-Management-image31.png)

    > [!NOTE]
    > Toto správanie sa vyskytuje len v prípade, že pomenovaný zdroj je plne rezervovaný pre všeobecné zdroje požiadavky. Keď buď pomenovaný zdroj čiastočne nahradí požiadavku na generické zdroje alebo viaceré pomenované prostriedky nahradia požiadavku na generické zdroje, všeobecný zdroj zostáva priradený k úlohe.

    Na nasledujúcom obrázku, bola 80-hodinová úloha naplánovaná na päťdňové trvanie (16 hodín denne počas piatich dní) a priradený všeobecný zdroj, ktorý je pomenovaný **funkčný**.

    ![80-hodinová, päťdňová úloha priradená k funkčnému všeobecnému zdroju](media/Resource-Management-image32.png)

    Keď vygenerujete požiadavku, je to pre 80 hodín v priebehu piatich dní.

    ![Požiadavka vytvorená pre 80 hodín počas piatich dní](media/Resource-Management-image33.png)

    Keďže dostupné zdroje fungujú len osem hodín denne, na splnenie požiadavky sú potrebné dva zdroje.

    ![Druhý zdroj](media/Resource-Management-image35.png)

    Na karte **tím** teraz môžete vidieť, že všeobecný zdroj nemá požadované hodiny, ale priradené hodiny sa stále zobrazujú spolu s dvomi pomenovanými zdrojmi, ktoré tvoria naplnenie.

    ![Dve pomenované zdroje na karte tím](media/Resource-Management-image36.png)

    Na karte **plán** zostáva všeobecný zdroj priradený k úlohe.

    ![Všeobecné zdroje na karte Plánovanie](media/Resource-Management-image37.png)

PSA nepriraďuje oba zdroje k úlohe, pretože toto správanie by produkovalo menej predvídateľný harmonogram. V tomto jednoduchom príklade je jednoduché rozdeliť hodiny rovnomerne medzi dva zdroje. Avšak, v zložitejších scenároch, ktoré zahŕňajú viac úloh a viac zdrojov, PSA bude musieť urobiť predpoklady o tom, ako by mal prideliť rezervácie, ktoré sú prijaté pre viac zdrojov naprieč viacerými úlohami.

Preto v týchto scenároch, projektový manažér je zodpovedný za analyzovanieí viacerých rezervácií a ich priraďovanie podľa potreby. Na pridelenie rezervácie, projektový manažér priradí úlohy zo všeobecných zdrojov na pomenované zdroje a potom používa zobrazenie **odsúhlasenie** na uistenie sa, že pridelenie funguje s rezervami.

### <a name="edit-a-resource-requirement"></a>Upravte požiadavku na zdroj

Po vytvorení požiadavky zdroja môže manažér projektu alebo Správca zdrojov upraviť podrobnosti, aby sa pri použití tabule plánovania spresnili kritériá vyhľadávania. Ak chcete upraviť požiadavku zdroja, postupujte nasledovne.

1. Na stránke **projekty**, na karte **tím** vyberte odkaz na akúkoľvek požiadavku na všeobecný zdroj.
2. Na stránke **požiadavky na zdroj**, ktorá sa zobrazí, môžete aktualizovať niekoľko atribútov. Tu sú niektoré príklady:

    - Názov
    - Dátum Od
    - Dátum Do
    - Trvanie
    - Typ zdroja

Na stránke **požiadavka na zdroj** môže manažér projektu alebo Správca prostriedkov definovať aj nasledujúce informácie:

- Odbornosti
- Roly
- Predvoľby zdrojov
- Preferovaná organizačná jednotka

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Aktualizujte rezervácie zdrojov po ich rezervovaní na projekte

Po pridaní všeobecného alebo pomenovaného zdroja do projektového tímu môžete zmeniť rezervácie prostriedku.

1. Ak chcete pridať člena tímu priamo do projektu, na stránke **projekty** na karte **tím** vyberte položku člen tímu a potm vyberte **nový**.

    ![Tabuľa plánovania otvorená pre vybraný člen tímu](media/Resource-Management-image40.png)

    Zobrazí sa tabuľa plánovania a zobrazí sa rezervácia člena projektového tímu. Rozbaľte záznam člena tímu a zobrazte hodiny, ktoré boli rezervované proti tomuto projektu, a ďalšie projekty, ktoré spotrebúvajú kapacitu člena tímu.

2. Výberom a presunutím rezervácie ju rozšírte alebo skráťte. Zobrazí sa dialógové okno **vytvorenie rezervačného prostriedku**, ktoré umožňuje upraviť rezerváciu.

    ![Dialógové okno vytvorenie rezervácie zdroja](media/Resource-Management-image41.png)

3. Kliknite pravým tlačidlom myši na rezerváciu. Potom môžete použiť kontextovú ponuku na dokončenie nasledujúcich akcií:

    - Zmeňte stav rezervácie
    - Upravte rezerváciu
    - Nahraďte zdroj v projektovom tíme.

### <a name="change-the-booking-status"></a>Zmeňte stav rezervácie

Môžete zmeniť ľubovoľný predvolený alebo vlastný stav rezervácie.

![Príkaz zmena stavu](media/Resource-Management-image42.png)

V PSA sú obsiahnuté nasledujúce stavy:

- **Zrušené** – tento stav zruší rezerváciu zdroja a uvoľní kapacitu zdroja.
- **Tvrdá rezervácia** – tento stav spotrebuje kapacitu zdroja. Rezervácia má zvyčajne tento stav pri otvorení **udržiavať rezervácie** od mriežky **všetkých členov tímu** na stránke **projekty**.
- **Jemná rezervácia** – tento stav pridá zdroj do tímu, ale nespotrebuje kapacitu zdroja. To naznačuje, že zdroj bol vyhradený pre potenciálnu prácu, ale stále má kapacitu, ak je to potrebné na iné pracovné miesta. Vzhľadom na celkovú dostupnosť zdrojov majú mäkké rezervácie iný status ako tvrdé rezervácie.
- **Navrhovaný** – tento stav predstavuje návrh manažéra zdroja alebo projektového manažéra. Návrhy nespotrebúvajú kapacitu zdroja a zdroj nie je pridaný do projektového tímu. Ak chcete tvrdú rezerváciu zdroja v tíme, projektový manažér musí prijať návrh.

### <a name="submit-resource-requests"></a>Odošle žiadosti o zdroj

Požiadavky na zdroje sa používajú na vykonanie dopytu (požiadavka na zdroje), ktorú musí správca zdrojov splniť. Pre všeobecný zdroj, ktorý je už v tíme, môžete priamo odoslať požiadavku zdroja. Žiadosť o zdroj možno splniť dvomi spôsobmi:

- Správca zdroja priamo splní požiadavku. V tomto prípade sa všeobecný zdroj nahradí tvrdou rezerváciou s pomenovaným zdrojom.
- Správca zdrojov navrhne zdroj projektovému manažérovi a projektový manažér schváli alebo odmieta navrhovaný zdroj.

#### <a name="direct-fulfillment-of-resource-requests"></a>Priame naplnenie požiadaviek na zdroje

Keď vzniká požiadavka na zdroj, projektový manažér môže odoslať požiadavku zdroja pre všeobecný zdroj výberom zdroja a následným výberom položky **Odoslať žiadosť.**

![Tlačidlo odoslať žiadosť](media/Resource-Management-image45.png)

Komentáre k zdroju možno poskytnúť správcovi zdrojov, ktorý spĺňa požiadavku. Po odoslaní žiadosti, sa pole **stav** pre člena tímu zmení na **odoslané**.

![Zadávanie voliteľných komentárov](media/Resource-Management-image46.png)

Keď správca zdrojov splní požiadavku, všeobecný člen tímu sa nahradí názvom zdroja v mriežke **všetkých členov** tímu.

![Všeobecný člen tímu nahradený názvom zdroja v mriežke všetkých členov tímu](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Použitie návrhu zdroja pre žiadosti o zdroje

Namiesto priamej rezervácie zdroja na žiadosť o zdroje môže správca zdrojov navrhnúť zdroj pre projektového manažéra. Správca zdrojov môže túto možnosť použiť, ak nie je k dispozícii presná zhoda požiadaviek. Keď správca zdrojov navrhne zdroj, projektový manažér vidí, že pole **stav** pre všeobecného člena tímu sa zmení na **prieskum potrieb**.

![Stav všeobecného člena tímu sa zmenil na potreba preskúmať](media/Resource-Management-image48.png)

Ak chcete zobraziť navrhovaný zdroj spolu s vizualizáciou vplyvu rezervácie návrhu, dvakrát kliknite na člena tímu, ktorý má stav **potreba preskúmať**. Potom vyberte kartu **navrhované zdroje**.

![Karta navrhované zdroje](media/Resource-Management-image49.png)

Vyberte možnosť **prijať všetky návrhy**, aby ste prijali všetky navrhované zdroje alebo **odmietnuť všetky návrhy** na ich odmietnutie. Ak akceptujete navrhované zdroje, sú na projekte natvrdo rezervované ako členovia tímu a nahradia všeobecné zdroje.

> [!NOTE]
> Musíte buď prijať alebo odmietnuť všetky navrhované prostriedky. Nemôžete ich čiastočne akceptovať ani odmietnuť.

### <a name="substitute-a-resource-on-the-project-team"></a>Nahraďte zdroj v projektovom tíme.

Projektový manažér niekedy musí nahradiť rezervovaného člena tímu na projekte.

1. Ak chcete pridať člena tímu priamo do projektu, na stránke **projekty** na karte **tím** vyberte položku zdroj ktorý potrebuje výmenu a potom vyberte **udržiavať rezervácie**.
2. Rozbaľte zdroj na zobrazenie projektov, ku ktorým je priradený.

    ![Rozšírený zdroj na zobrazenie priradených projektov](media/Resource-Management-image50.png)

3. Kliknite na projektr pravým tlačidlom myši, a potom vyberte **nahradiť zdroj**.
4. Ak poznáte zdroj, ktorým chcete nahradiť aktuálny zdroj, vyberte alebo zadajte názov a potom vyberte položku **znova priradiť.**

    ![Určenie náhradného zdroja](media/Resource-Management-image51.png)

    Prípadne, ak chcete vyhľadať zdroj, postupujte podľa týchto krokov:

    1. Vyberte **Hľadať náhradu**.

        ![Hľadanie náhradného zdroja](media/Resource-Management-image52.png)

        Asistent plánovania vráti zoznam dostupných náhradníkov. V Asistentovi plánovania môžete ďalej filtrovať dostupné zdroje a nájsť vhodnú náhradu.

        ![Zoznam dostupných náhrad.](media/Resource-Management-image53.png)

    2. K nahradeniu zdroja vyberte zdroj, ktorý chcete a potom vyberte **nahradiť**.

        ![Náhradný zdroj je vybraný](media/Resource-Management-image54.png)

    Rezervácie a priradenia sú nahradené novým zdrojom.

    ![Rezervácie a priradenia nahradené novým zdrojom.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Zmierenie rezervácií a priradení člena tímu

Pre členov tímu sú rezervácie a priradenia voľne spojené. Inými slovami, zdroje môžu mať úlohy, ale žiadne rezervácie, alebo môžu mať rezerváciu, ale žiadne úlohy. V ideálnom prípade by mali byť rezervácie a úlohy zarovnané tak, aby zdroje zaplnili kapacity na plnenie úloh. Rezervácie však môžu byť založené na dostupnosti a časovanie úloh sa môže zmeniť, keď projekt pokračuje. Preto voľné spojenie rezervácií a úloh poskytuje flexibilitu.

PSA má kartu **odsúhlasenie**, ktorá umožňuje projektovým manažérom zosúladiť rezervácie členov tímu a ich úlohy pre projektové tímy.

![Karta zmierenia](media/Resource-Management-image56.png)

Na karte **odsúhlasenie** sa zobrazujú rezervácie a priradenia na úrovni jednotlivých priradení úloh pre každého člena tímu. To zobrazuje hodiny v bunkách, ktoré môžu reprezentovať časové periódy od mesiacov ku dňom.

Na karte sa tiež zobrazuje celková čistá suma projektu spolu s celkovým stĺpcom.

Pre každý zdroj karta vypočíta rozdiel medzi rezerváciami člena tímu a súhrnom priradení úloh člena tímu. V ideálnom prípade by tento rozdiel mal byť 0 (nula). Inými slovami, nemal by existovať žiadny rozdiel medzi rezerváciou a úlohami. Rozdiely sú farebné a zatienené aby upozornili na dve podmienky:

- **Nedostatok rezervácií** – Nedostatky rezervácií sa objavia, keď má zdroj viac priradení než rezervácie. Keďže táto kapacita nebola vyhradená, projektový manažér by túto podmienku mal chcieť napraviť rozšírením rezervácií prostriedkov na krytie deficitu.
- **Rozšírené rezervácie** – Nadmerná rezervácia nastane, keď sa zdroj zarezervuje do projektu, no nebude priradený k úlohám. Táto podmienka môže byť prijateľná v prípadoch, keď bol zdroj rezervovaný do projektu pred priradením úlohy. V ostatných prípadoch však zdroj nie je naplánovaný na priraďenie k úlohe. V takýchto prípadoch by mal projektový manažér zvážiť zrušenie rezervácií prostriedku tak, aby sa kapacita mohla použiť pre iný projekt.

V niektorých prípadoch, keď zobrazíte čas na vyššej úrovni ako na úrovni dňa (napríklad na úrovni mesiaca), môže sa zobraziť čistý rozdiel nula pre zdroj (inými slovami, rezervácie = úlohy). Avšak, ak si prezriete čas na úrovni týždňa, môžete vidieť, že existujú úlohy nula hodín a rezervácie 40 hodín v prvom týždni, ale úlohy 40 hodín a rezervácie nula hodín v druhom týždni. Celkovo sú rezervácie a úlohy zmierené, ale líšia sa od jedného týždňa do nasledujúceho.

Keď zobrazíte čas na vyšších úrovniach, bunky na karte **odsúhlasenie** majú indikátor, ktorý vám oznámi, že existujú rozdiely na nižších úrovniach. Dvojitým kliknutím na bunku môžete zväčšiť zobrazenie rozdielu. Potom môžete kliknutím pravým tlačidlom myši na vzdialiť. Výberom prostriedku a následným použitím ovládacieho prvku **ďalší rozdiel** na paneli s nástrojmi mriežky môžete prejsť na ďalší rozdiel medzi rezerváciami a priradeniami pre daný zdroj. Potom môžete použiť na vrátenie kontrolu **predchádzajúci rozdiel**. V časti **nastavenia** môžete tiež vypnúť ukazovateľ rozdielu a správanie navigácie.

![Ukazovateľ rozdielu](media/Resource-Management-image57.png)

Ak máte priradenia úloh pre zdroj, ale žiadne rezervácie, na stránke **projekty** na karte **odsúhlasenie** vyberte nedostatok rezervácie a potom vyberte položku **rozšíriť rezerváciu.** Zobrazí sa dialógové okno **rozšíriť rezerváciu** a zobrazí sa rezervácia, ktorá je potrebná na vyriešenie nedostatku zdroja. Zobrazuje aj existujúce rezervácie zdrojov vo všetkých projektoch alebo iných plánovateľných entitách. Ak vyberiete **OK**, ak chcete vytvoriť rezerváciu zdroja bez ohľadu na dostupnosť tohto prostriedku, môžete spôsobiť prekročenie rezervácie.

![Dialógové okno rozšírenie rezervácie](media/Resource-Management-image58.png)

Projektový manažér alebo správca zdrojov potom môže pomocou tabule plánovania spravovať všetky situácie, v ktorých je zdroj prerezervovaný nad rámec jeho kapacity.


[!INCLUDE[footer-include](../includes/footer-banner.md)]