---
title: Pridávanie členov tímu z mriežky Člen tímu
description: Táto téma poskytuje informácie o tom, ako spravovať zdroje členov tímu.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 0f975d295b4c0ccef9827767beabd32ffd761faa
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897740"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Pridávanie členov tímu z mriežky Člen tímu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations obsahuje tabuľu správcu zdrojov, ktorá poskytuje vizuálny prehľad dopytu a využitia zdrojov v celej organizácii. Grafy na tejto tabuli môžete použiť na vizualizáciu nasledujúcich informácií:

- **Dopyt po zdrojoch**: graf **požiadavky na aktívny zdroj** zobrazuje zdroje, ktoré boli odoslané. Zdroje sú agregované buď rolou alebo projektom.
- **Dopyt na nepredložený zdroj**: graf **dopytu na nepriradené zdroje** zobrazuje všetky požiadavky na zdroje, ktoré neboli predložené. Tento graf pomáha správcom zdrojov zobraziť dopyt, ktorý nie je pevný a môže byť predložený prostredníctvom žiadosti o prostriedky.
- **Fakturovateľné využitie za uplynulý týždeň**: graf **Využitie podľa roly** zobrazuje percento skutočného fakturovateľného využitia organizácie podľa roly proti jeho cieľovému fakturovateľnému využitiu podľa roly.

    > [!NOTE]
    > Aby bol graf **využitia rolí** k dispozícii, vytvorte úlohu, ktorá spúšťa pracovný postup **UpdateRoleUtilization**. Táto opakovaná úloha sa spúšťa každých sedem dní na výpočet fakturovateľného využitia za predchádzajúcich sedem dní. Výsledky sú agregované podľa role.

## <a name="manage-project-team-members"></a>Spravujte členov projektového tímu

Projektoví manažéri môžu na spravovanie zdrojov na projektoch použiť tabuľu správca prostriedkov. Napríklad môžu pridať člena tímu priamo do projektu a rezervovať člena tímu, aby splnil požiadavky na zdroje, ktoré boli zachytené všeobecným prostriedkom.

### <a name="add-a-team-member-directly-to-a-project"></a>Pridajte člena tímu priamo do projektu

Ak chcete pridať člena tímu priamo do projektu, vo formulári **Projekty** na karte **Tím** vyberte položku **Nové**. Zobrazí sa dialógové okno **rýchle vytvorenie člena projektového tímu**. V tomto dialógovom okne môžete vykonávať tieto úlohy:

- **Rezervujte si pomenovaný zdroj**: v poli **rezervovateľné zdroje** vyberte názov zdroja. Potom vyberte rolu, nastavte obdobie a vyberte spôsob pridelenia. Pomenovaný zdroj, ktorý ste vybrali, sa pridá do projektu pomocou vybratej metódy prideľovania a zdrojového kalendára.
- **Pridať všeobecný zdroj**: ponechajte prázdne pole **Rezervovateľný zdroj** a potom vyberte rolu, nastavte obdobie a vyberte preferovaný spôsob pridelenia. Ako zástupný symbol sa do tímu pridá všeobecný zdroj. Zástupný symbol udržiava vzor dopytu, ktorý sa používa na rezerváciu pomenovaných zdrojov v tíme. Požiadavka sa vykonáva v súlade s kalendárom projektu.
- **Pridanie pomenovaného zdroja do tímu bez spotreby kapacity zdrojov**: v poli **Rezervovateľné zdroje** vyberte zdroj. Vyberte obdobie a potom vyberte **Nič** ako spôsob pridelenia. Zdroj sa pridá do tímu, ale kapacita zdroja nie je spotrebovaná prostredníctvom rezervácie.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezervujte si člena tímu, tak aby splnil požiadavky na zdroje pre všeobecný zdroj

V Project Operations si môžete rezervovať všeobecný zdroj v projektovom tíme. Môžete tiež určiť rolu, požadovanú kapacitu a spôsob distribúcie tejto kapacity. Pre požiadavku na zdroj môžete zadať atribúty, ktoré súvisia so všeobecným zdrojom. Tieto atribúty zahŕňajú požadované zručnosti, preferovanú organizačnú jednotku a preferované zdroje.

Ak chcete určiť požadované zručnosti na všeobecný zdroj pre vývojára, postupujte podľa nasledujúcich krokov.

1. Vo formulári **Projekty** na karte **Tím** vyberte položku **Nové**, ak chcete rezervovať všeobecný zdroj.
2. V zobrazení **všetci členovia tímu** v stĺpci **požiadavka zdroja** vyberte prepojenie na pridanie požadovaných zručností pre všeobecný zdroj.
3. Vo formulári **Požiadavky na zdroje** v mriežke **Zručnosti** vyberte elipsu (**...**) a potom vyberte **Pridať novú charakteristiku požiadavky** pre pridanie požadovaných zručnosti pre vývojárov.
4. Vo formulári **Rýchle vytvorenie: charakteristika požiadavky** v poli **Charakteristika**, vyberte požadované zručnosti.
5. V poli **Hodnota hodnotenia** vyberte úroveň odbornosti pre danú zručnosť. 
6. V poli **Požiadavka na zdroj** nastavte požiadavku na zdrojové prostriedky z organizačných jednotiek alebo dokonca pomenovaných zdrojov. Po dokončení vyberte **Uložiť**.
7. Vo formulári **Požiadavky na zdroje** vyberte položku **rezervovať**, čím sa splní požiadavka na zdroje. Môžete tiež vybrať všeobecný prostriedok v mriežke **všetci členovia tímu** a potom vyberte položku **rezervovať.**

    > [!NOTE]
    > V tomto príklade je 40 požadovaných hodín, ale žiadne aktuálne rezervované hodiny, pretože všeobecné zdroje nemajú rezervácie. Okrem toho nie sú priradené žiadne hodiny, pretože všeobecný zdroj bol pridaný priamo do tímu namiesto pridania pomocou priradenia úlohy.

    Vo formulári **asistent plánovania** môžete filtrovať dostupné zdroje podľa požiadaviek, ktoré sú zadané v požiadavke na zdroj. Zdroje sú zoradené podľa parametrov zoradenia, ktoré sú špecifikované na tabuli plánovania.

   Medzi najčastejšie používané filtre patria:

    - **Charakteristika spolu s hodnotením**: Filter podľa zručností, certifikácií a ďalších zdrojov kvality, okrem hodnotenia odbornosti.
    - **Roly**: Filter podľa predvolených rolí priradených k rezervovateľným zdrojom.
    - **Organizačné jednotky**: Filter rezervovateľné zdroje organizačnými jednotkami, ku ktorým sú priradené.

8. Ak nie ste spokojní s výsledkami úvodného vyhľadávania požiadaviek, môžete zmeniť kritériá filtra. Rozbaľte panel **zobrazenie filtra** na ľavej strane a potom vyberte položku **Hľadať** a vyhľadajte ďalšie zdroje. Ak chcete zmeniť spôsob zoradenia výsledkov, vyberte **zoradiť**.
9. Vyberte zdroje podľa dopytu, ktorý je špecifikovaný v požiadavke, ako je uvedené v hornej časti mriežky. Môžete vymazať výber buniek v mriežke a ponechať kapacitu zdroja otvorenú. Ako rezervované je možné vybrať len jeden zdroj naraz.
10. Vyberte **rezervovať**, ak chcete rezervovať vybratý zdroj a nechať otvorenú panel plánovania, aby ste mohli vybrať ďalšie zdroje. Prípadne vyberte položku **rezervovať & východ**, ak chcete rezervovať vybratý zdroj a zatvoriť panel plánovania.
11. Vráťte sa do zobrazenia **všetci členovia tímu** . V mriežke si všimnite, že všeobecný prostriedok bol nahradený názvom prostriedku a 40 hodín je uvedených ako rezervované pre daný zdroj.

    > [!NOTE]
    > Nie sú zobrazené žiadne priradené hodiny, pretože boli rezervované priamo v tíme. Neboli rezervované pomocou priradenia úloh.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Priradenie všeobecných zdrojov k úlohe a generovanie zdrojových požiadaviek

V Project Operations môžete vytvárať úlohy a potom im priradiť všeobecné zdroje. Dopyt po zdroji potom môže byť zastupovaný zástupnými symbolmi, zatiaľ čo vy odhadnete svoj rozvrh a finančné čísla. Potom môžete generovať požiadavky na zdroje pre všeobecné zdroje a naplniť ich.

1. Vo formulári **Projekty**, na karte **Plán** vyberte položku **Pridať** a vytvorte úlohu.
2. V poli **zdroje** vyberte symbol **výberu zdroja**. Zobrazí sa výber zdrojov a zobrazí existujúcich členov tímu projektu.
3. Zadajte názov nového všeobecného prostriedku a potom vyberte položku **vytvoriť.**
4. V dialógovom okne **rýchle vytvorenie: člena projektového tímu**, ktoré sa zobrazí v poli **rola**, vyberte rolu pre všeobecné zdroje. 
5. V poli **zdrojová jednotka** vyberte organizačnú jednotku pre všeobecný zdroj. Potom vyberte **Uložiť**. Člen všeobecného tímu je teraz priradený k úlohe.

   Na karte **tím** sa zobrazí nový všeobecný člen tímu. Všimnite si, že má len pridelené hodiny. Tieto hodiny sú súčtom všetkých úloh, ktoré sú priradené všeobecnému členovi tímu. Všeobecný člen tímu nemá požadované hodiny alebo požiadavku na zdroje.

6. Teraz môžete priradiť všeobecného člena tímu k iným úlohám pomocou výberu zdrojov.

   Po dokončení priraďovania všeobecného zdroja k úlohám môžete vygenerovať požiadavku zdroja pre všeobecný zdroj.

7. Na karte **tím** vyberte všeobecný zdroj a potom vyberte **generovať požiadavku.** Po vygenerovaní požiadavky, všeobecný člen tímu bude mať požadované hodiny a odkaz na zdroj požiadavky.

  Po dokončení rezervácie pomenovaného zdroja sa všeobecný zdroj odstráni z tímu a je nahradený pomenovaným zdrojom. Na karte **plán** sa všeobecné priradenia zdrojov odstránia a nahradia názvom zdroja.

  > [!NOTE]
  > Toto správanie sa vyskytuje len v prípade, že pomenovaný zdroj je plne rezervovaný pre všeobecné zdroje požiadavky. Keď buď pomenovaný zdroj čiastočne nahradí požiadavku na generické zdroje alebo viaceré pomenované prostriedky nahradia požiadavku na generické zdroje, všeobecný zdroj zostáva priradený k úlohe.

Project Operations nepriraďuje oba zdroje k úlohe, pretože toto správanie by produkovalo menej predvídateľný harmonogram. V tomto jednoduchom príklade je jednoduché rozdeliť hodiny rovnomerne medzi dva zdroje. Avšak, v zložitejších scenároch, ktoré zahŕňajú viac úloh a viac zdrojov, PSA bude musieť urobiť predpoklady o tom, ako by mal prideliť rezervácie, ktoré sú prijaté pre viac zdrojov naprieč viacerými úlohami.

Preto v týchto scenároch, projektový manažér je zodpovedný za analyzovanie viacerých rezervácií a ich priraďovanie podľa potreby. Na pridelenie rezervácie, projektový manažér priradí úlohy zo všeobecných zdrojov na pomenované zdroje a potom používa zobrazenie **Odsúhlasenie** na uistenie sa, že pridelenie funguje s rezervami.

### <a name="edit-a-resource-requirement"></a>Upravte požiadavku na zdroj

Po vytvorení požiadavky zdroja môže Manažér projektu alebo Správca zdrojov upraviť podrobnosti, aby sa pri použití tabule plánovania spresnili kritériá vyhľadávania. Ak chcete upraviť požiadavku zdroja, postupujte nasledovne.

1. Vo formulári **Projekty**, na karte **Tím** vyberte odkaz na akúkoľvek požiadavku na všeobecný zdroj.
2. Vo formulári **Požiadavka na zdroj** ktorý sa zobrazí, zadajte potrebné informácie o poli

   Vo formulári **Požiadavka na zdroj** môže projektový manažér alebo manažér zdrojov definovať aj zručnosti, roly, preferencie zdrojov a preferovanú organizačnú jednotku.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Aktualizujte rezervácie zdrojov po ich rezervovaní na projekte

Po pridaní všeobecného alebo pomenovaného zdroja do projektového tímu môžete zmeniť rezervácie prostriedku.

1. Ak chcete pridať člena tímu priamo do projektu, vo formulári **Projekty** na karte **Tím** vyberte člena tímu a potom vyberte **Spravovať rezervácie**.
 
   Zobrazí sa tabuľa plánovania a zobrazí sa rezervácia člena projektového tímu. Rozbaľte záznam člena tímu a zobrazte hodiny, ktoré boli rezervované proti tomuto projektu, a ďalšie projekty, ktoré spotrebúvajú kapacitu člena tímu.

2. Výberom a presunutím rezervácie ju rozšírte alebo skráťte. Zobrazí sa dialógové okno **vytvorenie rezervačného prostriedku**, ktoré umožňuje upraviť rezerváciu.
3. Kliknite pravým tlačidlom myši na rezerváciu. Potom môžete použiť kontextovú ponuku na dokončenie nasledujúcich akcií:

    - Zmeňte stav rezervácie
    - Úprava rezervácie
    - Nahraďte zdroj v projektovom tíme.

### <a name="change-the-booking-status"></a>Zmeňte stav rezervácie

Môžete zmeniť ľubovoľný predvolený alebo vlastný stav rezervácie.

V Project Operations sú obsiahnuté nasledujúce stavy:

- **Zrušené**: zruší rezerváciu zdroja a uvoľní kapacitu zdroja.
- **Tvrdá rezervácia**: spotrebúva kapacitu zdroja. Rezervácia má zvyčajne tento stav pri otvorení **Udržiavať rezervácie** z mriežky **Všetci členovia tímu** vo formulári **Projekty**.
- **Jemná rezervácia**: pridá zdroj do tímu, ale nespotrebuje kapacitu zdroja. Tento stav naznačuje, že zdroj bol vyhradený pre potenciálnu prácu, ale stále má kapacitu, ak je to potrebné na iné pracovné miesta. Vzhľadom na celkovú dostupnosť zdrojov majú mäkké rezervácie iný status ako tvrdé rezervácie.
- **Navrhovaný**: tento stav predstavuje návrh manažéra zdroja alebo projektového manažéra. Návrhy nespotrebúvajú kapacitu zdroja a zdroj nie je pridaný do projektového tímu. Ak chcete tvrdú rezerváciu zdroja v tíme, projektový manažér musí prijať návrh.

### <a name="submit-resource-requests"></a>Odoslanie žiadostí o zdroje

Požiadavky na zdroje sa používajú na vykonanie dopytu alebo požiadavky na zdroje, ktorú musí správca zdrojov splniť. Pre všeobecný zdroj, ktorý je už v tíme, môžete priamo odoslať požiadavku zdroja. Žiadosť o zdroj možno splniť dvomi spôsobmi:

- Správca zdrojov priamo splní požiadavku. V tomto prípade sa všeobecný zdroj nahradí tvrdou rezerváciou s pomenovaným zdrojom.
- Správca zdrojov navrhne zdroj projektovému manažérovi a projektový manažér schváli alebo odmieta navrhovaný zdroj.

#### <a name="direct-fulfillment-of-resource-requests"></a>Priame naplnenie požiadaviek na zdroje

Keď vzniká požiadavka na zdroj, projektový manažér môže odoslať požiadavku zdroja pre všeobecný zdroj výberom zdroja a následným výberom položky **Odoslať žiadosť**. Komentáre k zdroju možno poskytnúť správcovi zdrojov, ktorý spĺňa požiadavku. Po odoslaní žiadosti, sa pole **stav** pre člena tímu zmení na **odoslané**. Keď správca zdrojov splní požiadavku, všeobecný člen tímu sa nahradí názvom zdroja v mriežke **všetkých členov** tímu.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Použitie návrhu zdroja pre žiadosti o zdroje

Namiesto priamej rezervácie zdroja na žiadosť o zdroje môže správca zdrojov navrhnúť zdroj pre projektového manažéra. Správca zdrojov môže túto možnosť použiť, ak nie je k dispozícii presná zhoda požiadaviek. Keď správca zdrojov navrhne zdroj, projektový manažér vidí, že pole **stav** pre všeobecného člena tímu sa zmení na **prieskum potrieb**.

Môžete si pozrieť navrhovaný zdroj spolu s vizualizáciou účinku rezervácie návrhu. 

1. Dvakrát kliknite na člena tímu, ktorý má stav **Potrebná kontrola**. 
2. Vyberte kartu **Navrhované zdroje**.
3. Vyberte možnosť **prijať všetky návrhy**, aby ste prijali všetky navrhované zdroje alebo **odmietnuť všetky návrhy** na ich odmietnutie. Ak akceptujete navrhované zdroje, sú na projekte natvrdo rezervované ako členovia tímu a nahradia všeobecné zdroje.

> [!NOTE]
> Musíte buď prijať alebo odmietnuť všetky navrhované prostriedky. Nemôžete ich čiastočne akceptovať ani odmietnuť.

### <a name="substitute-a-resource-on-the-project-team"></a>Nahraďte zdroj v projektovom tíme.

Projektový manažér niekedy musí nahradiť rezervovaného člena tímu na projekte.

1. Ak chcete pridať člena tímu priamo do projektu, vo formulári **Projekty** na karte **Tím** vyberte položku zdroj ktorý potrebuje výmenu a potom vyberte **Udržiavať rezervácie**.
2. Rozbaľte zdroj na zobrazenie projektov, ku ktorým je priradený.
3. Kliknite na projektr pravým tlačidlom myši, a potom vyberte **nahradiť zdroj**.
4. Ak poznáte zdroj, ktorým chcete nahradiť aktuálny zdroj, vyberte alebo zadajte názov a potom vyberte položku **Znova priradiť**.

Alebo. Ak potrebujete vyhľadať zdroj, vykonajte nasledujúce kroky.

1. Vyberte **Hľadať náhradu**.

   Asistent plánovania vráti zoznam dostupných náhradníkov. V Asistentovi plánovania môžete ďalej filtrovať dostupné zdroje a nájsť vhodnú náhradu.

2. K nahradeniu zdroja vyberte zdroj, ktorý chcete a potom vyberte **nahradiť**.   

   Rezervácie a priradenia sú nahradené novým zdrojom.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Zmierenie rezervácií a priradení člena tímu

Pre členov tímu sú rezervácie a priradenia voľne spojené. Inými slovami, zdroje môžu mať úlohy, ale žiadne rezervácie, alebo môžu mať rezerváciu, ale žiadne úlohy. V ideálnom prípade by mali byť rezervácie a úlohy zarovnané tak, aby zdroje zaplnili kapacity na plnenie úloh. Rezervácie však môžu byť založené na dostupnosti a časovanie úloh sa môže zmeniť, keď projekt pokračuje. Preto voľné spojenie rezervácií a úloh poskytuje flexibilitu.

Project Operations obsahuje kartu **Zosúladenie**, ktorá umožňuje projektovým manažérom zosúladiť rezervácie členov tímu a ich úlohy pre projektové tímy.

Na karte **odsúhlasenie** sa zobrazujú rezervácie a priradenia na úrovni jednotlivých priradení úloh pre každého člena tímu. To zobrazuje hodiny v bunkách, ktoré môžu reprezentovať časové periódy od mesiacov ku dňom.

Na karte sa tiež zobrazuje celková čistá suma projektu spolu s celkovým stĺpcom.

Pre každý zdroj karta vypočíta rozdiel medzi rezerváciami člena tímu a súhrnom priradení úloh člena tímu. V ideálnom prípade by tento rozdiel mal byť 0 (nula). Inými slovami, nemal by existovať žiadny rozdiel medzi rezerváciou a úlohami. Rozdiely sú farebné a zatienené aby upozornili na dve podmienky:

- **Nedostatok rezervácií**: nastane, keď má zdroj viac priradení než rezervácie. Keďže táto kapacita nebola vyhradená, projektový manažér by túto podmienku mal chcieť napraviť rozšírením rezervácií prostriedkov na krytie deficitu.
- **Rozšírené rezervácie**: nastane, keď sa zdroj zarezervuje do projektu, no nebude priradený k úlohám. Táto podmienka môže byť prijateľná v prípadoch, keď bol zdroj rezervovaný do projektu pred priradením úlohy. V ostatných prípadoch však zdroj nie je naplánovaný na priraďenie k úlohe. V takýchto prípadoch by mal projektový manažér zvážiť zrušenie rezervácií prostriedku tak, aby sa kapacita mohla použiť pre iný projekt.

V niektorých prípadoch, keď zobrazíte čas na vyššej úrovni ako na úrovni dňa (napríklad na úrovni mesiaca), môže sa zobraziť čistý rozdiel nula pre zdroj. Inými slovami, rezervácie = priradenia. Avšak, ak si prezriete čas na úrovni týždňa, môžete vidieť, že existujú úlohy nula hodín a rezervácie 40 hodín v prvom týždni, ale úlohy 40 hodín a rezervácie nula hodín v druhom týždni. Celkovo sú rezervácie a úlohy zmierené, ale líšia sa od jedného týždňa do nasledujúceho.

Keď zobrazíte čas na vyšších úrovniach, bunky na karte **odsúhlasenie** majú indikátor, ktorý vám oznámi, že existujú rozdiely na nižších úrovniach. Dvojitým kliknutím na bunku zväčšíte zobrazenie rozdielu. Potom môžete kliknutím pravým tlačidlom myši na vzdialiť. Výberom prostriedku a následným výberom možnosti **Ďalší rozdiel** na paneli mriežky môžete prejsť na ďalší rozdiel medzi rezerváciami a priradeniami pre daný zdroj. Na návrat späť vyberte **Predchádzajúci rozdiel**. V časti **nastavenia**môžete tiež vypnúť ukazovateľ rozdielu a správanie navigácie.

Ak máte priradenia úloh pre zdroj, ale žiadne rezervácie, vo formulári **projekty** na karte **odsúhlasenie** vyberte nedostatok rezervácie a potom vyberte položku **rozšíriť rezerváciu**. Zobrazí sa dialógové okno **rozšíriť rezerváciu** a zobrazí sa rezervácia, ktorá je potrebná na vyriešenie nedostatku zdroja. Dialógové okno zobrazuje aj existujúce rezervácie zdrojov vo všetkých projektoch alebo iných plánovateľných entitách. Ak vyberiete **OK**, ak chcete vytvoriť rezerváciu zdroja bez ohľadu na dostupnosť tohto prostriedku, môžete spôsobiť prekročenie rezervácie.

Projektový manažér alebo správca zdrojov potom môže pomocou tabule plánovania spravovať všetky situácie, v ktorých je zdroj prerezervovaný nad rámec jeho kapacity.
