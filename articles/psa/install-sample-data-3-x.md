---
title: Inštalácia vzorových údajov
description: Táto téma poskytuje informácie o inštalácii vzorových údajov v Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: aaeb4163c7ace1c3bf4db61f1a10a13cfbdc4fc2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144522"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Inštalácia vzorových údajov pre aplikáciu Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

Aby vám spoločnosť Microsoft pomohla vybudovať vlastné vzorové prostredia, poskytuje na stiahnutie vzorky údajových balíkov, ktoré prezentujú možnosti vašich aplikácií. Existujú dva typy balíkov vzorových údajov:
- referenčné/konfiguračné údaje
- ukážkové údaje (referenčné/konfiguračné a transakčné údaje, ako napríklad objednávky prác a projekty)

Vzorové balíky s **referenčnými** údajmi sa dajú prevziať v troch odlišných balíkoch, takže môžete inštalovať údaje len pre Project Service, alebo len pre Field Service, alebo môžete nainštalovať vzorové údaje pre obe aplikácie naraz.

Vzorové balíky konfiguračných/referenčných údajov sú:

- [**V902PSMasterData** – Len Project Service ver. 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** – Len Field Service ver. 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** – Field Service 8.x a Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Najnovší balík **ukážkových** údajov je:

 - [**FPSDemoData** – Field Service 8.x a Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Pokyny na inštaláciu sa mierne líšia v časti vytvorenia a konfigurácie, ale zvyšok je rovnaký ako predchádzajúci [**blogový príspevok**](https://aka.ms/fpsdemodatablog). Tento balík obsahuje redukovanú množinu ukážkových údajov a jeho inštalácia zaberie približne 3 hodiny.

Tieto balíky vzorových údajov sú dostupné len v angličtine.

> [!IMPORTANT]
> **Neexistuje spôsob, ako odinštalovať vzorové údaje.** Tieto balíky by ste preto mali inštalovať len na demonštráciu, hodnotenie, školenie alebo testovanie systémov. Tiež nezabudnite, že inštalácia individuálneho balíka a následná inštalácia iného individuálneho balíka nie je podporovaná. (Inými slovami, nemôžete nainštalovať **FSMasterData** a následne **PSMasterData** alebo naopak.) Ak si myslíte, že v budúcnosti budete potrebovať vzorové údaje pre obe aplikácie, mali by ste nainštalovať balík **v902FPSMasterData**.

Pri inštalácii ktoréhokoľvek z balíkov vzorových údajov inštalačný proces vykoná nasledujúce akcie:

- Vytvorí alebo nastaví predvolené parametre pre používanie Project Service, Field Service alebo oboch aplikácií (v prípade potreby).

- Importuje vzorové údaje pre aplikácie, ako sú rezervovateľné zdroje, špecifické úlohy pre aplikácie, zoznamy predaja a obstarávacích cien, organizačné jednotky, záznamy spracovania predaja a iné entity na predvedenie rozhodujúcich schopností.  

S balíkom **ukážkových údajov** dostanete vyššie uvedené a dodatočné transakčné údaje, ako sú napríklad objednávky prác a projekty.

Zaujíma vás, aké schopnosti môžete predstaviť so vzorovými údajmi? Pozrite fiktívny scenár Fabrikam Robotics v [technických poznámkach](#technical-notes).

Ak máte otázky týkajúce sa inštalácie týchto balíkov so vzorovými údajmi, [pošlite nám e-mail na fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Požiadavky

Inštalačný protokol predpokladá nasledujúce o cieľovej inštancii (organizácii):

- Základný jazyk je angličtina a základnou menou je americký dolár (USD, $).

- Organizácia ešte nemá žiadne údaje Project Service alebo Field Service, alebo má len holé predvolené údaje, ktoré sa dodávajú k akejkoľvek novej organizácii.

- Je už nainštalovaná správna verzia obchodnej aplikácie:
       
    - **Pre FPSDemoData alebo v902FPSMasterData:** Organizácia má nainštalované Field Service verzia 8.x a Project Service verzia 3.x.

    - **Pre v902PSMasterData:** Organizácia má nainštalovanú Project Service verzia 3.x.

    - **Pre v902FSMasterData:** Organizácia má nainštalovanú Field Service verzia 8.x.

> [!NOTE]
> Ak potrebujete inštalovať vzorové údaje do existujúcej skúšobnej alebo demo verzie prostredia Project Service a Field Service, ktoré už obsahuje údaje (neodporúča sa), budete musieť pozastaviť bezpečnostné predbežné kontroly, ktoré vykonáva inštalátor. Ďalšie informácie nájdete v technických poznámkach nižšie.

## <a name="prepare-for-installation"></a>Príprava na inštaláciu

Musíte spustiť inštalátor na počítači s najnovšiu verziou systému Windows (preferovaný Windows 10).

Mali by ste počítať s tým, že počítač musí zostať pripojený k sieti a že inštalácia zaberie až **1 hodinu** pre **konfiguračné/referenčné údaje**. (Zvyčajne inštalácia trvá približne 30 minút pre **FPSMasterData**, ktoré obsahujú vzorové údaje pre obe aplikácie.) Pre **FPSDemoData** bude inštalácia trvať asi **3 hodiny**.

Počítač by mal mať vypnutú funkciu šetriča obrazovky. Inak by sa poverenia relácie pre inštaláciu mohli stratiť, keď sa aktivuje šetrič obrazovky (pokiaľ nebudete udržovať počas tej doby reláciu v aktívnom stave).

> [!div class="mx-imgBorder"]
> ![Snímka obrazovky nastavenia šetriča obrazovky, s vypnutým šetričom obrazovky](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Stiahnuť a rozbaliť

Inštalátor vzorových údajov Project Service a Field Service sa distribuuje ako samorozbaľovací spustiteľný súbor. Názvy súborov sa môžu líšiť v závislosti od balíka vzorových údajov, ale inak postup je rovnaký bez ohľadu na to, ktorý balík nainštalujete.

Po stiahnutí balíka spustite súbor .exe, prijmite podmienky a nechajte rozbaliť komprimovaný zip súbor. Obsah tohto súboru potrebujete rozbaliť do priečinka v počítači.

V závislosti od operačného systému a nastavenia zabezpečenia budete možno musieť vykonať nasledujúce kroky po rozbalení súboru zip:

1. Vyhľadajte súbor **FPSDemoData.dll** v priečinku **v902FPSMasterData** / **PackageDeployer_FPSDemoData** a kliknite naň pravým tlačidlom.

2. Vyberte **Odblokovať**.

3. Vyberte **Použiť**.

4. Vyberte položku **OK**.


## <a name="create-or-configure-users"></a>Vytvorenie alebo konfigurovanie používateľov

Balík **FPSDemoData** vyžaduje šesť používateľov, zatiaľ čo balíky **FPSMasterData** vyžadujú jedného používateľa. Vyberte si správny balík vzorových údajov.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Vytvorenie alebo konfigurácia používateľov – konfiguračné/referenčné údajové balíky

Balík **FPSMasterData** je určený na inštaláciu jedného používateľa s názvom Spencer Low s nastaveniami popísanými tu. Ak chcete balík nainštalovať správne, musíte vytvoriť (alebo dočasne premenovať) používateľov vo vašom prostredí, aby zodpovedali prichádzajúcej konfigurácii vzorových údajov.

Ak chcete vytvoriť alebo konfigurovať používateľov, prejdite na **Nastavenia** > **Zabezpečenie** > **Používatelia** a vykonajte nasledujúce:

1. Nastavte UserFullname = „Spencer Low“ s používateľským menom „spencerl“ (**malé**) na roly Projektový správca a Správca postupov.

2. Vyberte používateľa **Spencer Low** a potom **Spravovať roly**. Vyhľadajte a vyberte rolu **Správcu systému** a potom vyberte **OK** a udeľte úplné práva správcu používateľovi Spencer Low. Tento krok je potrebné zabezpečiť, aby vzorové záznamy boli vytvorené so správnym používateľským vlastníctvom a správne vypĺňali zobrazenia.

3. Zo stiahnutého balíka musíte aktualizovať súbor mapovanie údajov o e-mailové adresy kontextu predvoleného používateľa. Urobíte tak otvorením **PkgFolder** a následným vyhľadaním a otvorením súboru **ImportUserMapFile.xml** v Poznámkovom bloku (alebo Visual Studio alebo v inom editore XML). Nastavte pole **DefaultUserToMapTo=** na e-mailovú adresu používateľa Spencer Low.

4. Ak nepoužívate Spencer Low s používateľským menom **spencerl**, budete musieť aktualizovať ďalší súbor. Otvorte súbor **DemoDataPreImportConfig.xml** a nájdite značku **userstocreateandconfigure**. Aktualizujte značku **\<login\>** používateľským menom používateľa Jakub Mihálik. Ďalšie podrobnosti nájdete v časti [Technické poznámky](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Vytvorenie alebo konfigurovanie používateľov – balík ukážkových údajov

Balík ukážkových údajov vyžaduje šiestich používateľov. Aby sa balík nainštaloval správne, postupujte nasledovne:

 1. Vytvorte alebo dočasne premenujte existujúcich používateľov, aby zodpovedali konfigurácii ukážkových údajov – v ponuke **Nastavenia** > **Zabezpečenie** > **Používatelia**.
 
    Tieto roly sú potrebné len pre ukážky založené na osobách.  
    - Úplné meno používateľa = „David So“ ako technik služieb u zákazníka   
    - Úplné meno používateľa = „Jamie Reding“ ako dispečer služieb pre zákazníkov a služieb u zákazníka   
    - Úplné meno používateľa = „Molly Clark“ ako manažér obchodného vzťahu   
    - Úplné meno používateľa = „Spencer Low“ ako manažér praxe a projektov  
    - Úplné meno používateľa = „Veronica Quek“ ako člen tímu   
    - Úplné meno používateľa = „William Contoso“
  
2. Na účely importu ukážkových údajov priraďte šiestim používateľom vyššie rolu správcu, aby import ukážkových záznamov prebehol správne. 

3. Otvorte **PkgFolder** a potom vyhľadajte a otvorte **ImportUserMapFile.xml**. Aktualizujte polia **Nové=** na e-mailové adresy zodpovedajúcich používateľov vo vašom systéme.

   > [!div class="mx-imgBorder"]
   > ![Snímka obrazovky UserMapFile](media/sample-data-7.png)

4. Ak vaše úplné meno používateľa „Spencer Low“ má iné ID používateľa než **„spencerl“**, potom budete musieť aktualizovať ďalší súbor. Otvorte **DemoDataPreImportConfig.xml** a nájdite značku **userstocreateandconfigure**. Aktualizujte značku **\<login\>** s loginId (rozlišuje veľké a malé písmená). 

5. Kalendár prvého používateľa (v značke **userstocreateandconfigure**) sa používa na vyplnenie pracovnej doby pre všetky rezervovateľné zdroje pri importe ukážkových údajov. Prejdite na **Nastavenia** > **Zabezpečenie** > **Používatelia**, nájdite svojho používateľa „Spencer Low“ a otvorte možnosť „Pracovná doba“. Upravte existujúcu pracovnú dobu výberom možnosti **Celý opakujúci sa týždenný plán od začiatku do konca**. Zabezpečte **nastavenie pracovnej doby od 8.00 do 17.00 (9 hodín), pondelok až piatok, a časové pásmo nastavené na tichomorský čas (USA & Kanada)**. Je to potrebné na zabezpečenie toho, aby sa tabuľa projektu a plánovania zobrazila podľa očakávania.

**Odporúčanie:** Zvážte teraz vytvorenie zálohy vašej organizácie pre prípad, že by ste sa potrebovali vrátiť na začiatok, ak sa niečo pokazí počas inštalácie vzorových údajov. Ďalšie informácie nájdete v téme [Zálohovanie a obnovenie inštancií](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Spusťte Package Deployer

1. Nájdite a spustite **PackageDeployer.exe** v priečinku **v902FPSMasterData** ALEBO **PackageDeployer_FPSDemoData**.

2. Prijmite podmienky a požiadavky.

3. V ďalšom okne:

   a. Vyberte typ nasadenia **Office 365**.

   b. Použite používateľa a heslo používateľa v úlohe správcu systému nakonfigurovaného v časti „Vytvorenie alebo konfigurácia používateľov“ („Spencer Low“ s používateľským menom „spencerl“).

   c. Uistite sa, že je vybrané pole **Zobraziť zoznam dostupných organizácií**.

      > [!div class="mx-imgBorder"]
      > ![Snímka obrazovky okna nástroja Package Deployer s vybranou možnosťou „Zobrazenie zoznamu dostupných organizácií“](media/sample-data-2.png)

4. Vyberte organizáciu kam chcete inštalovať vzorové údaje.

5. Vyberajte **Ďalej** dovtedy, pokiaľ sa nezobrazí dialógové okno **Nastavenie demo údajov** .

   > [!div class="mx-imgBorder"]
   > ![Sníma obrazovky stavového okna inštalátora demo údajov](media/sample-data-3.png)

6. Pred pokračovaním pripomíname, že inštalácia vzorových údajov môže trvať až jednu hodinu (zvyčajne cca 10 minút). Budete musieť zabezpečiť, aby počas inštalácie zostal počítač pripojený do siete, a aby relácia zostala aktívna.   

7. Keď budete pripravení, kliknite na tlačidlo **Ďalej**, čím sa spustí proces inštalácie vzorových údajov. Po načítaní vzorových údajov kliknite na tlačidlo **Dokončiť**.

## <a name="verify-the-sample-data-installation"></a>Overenie inštalácie vzorových údajov

Pre kontrolu overte, či sa počet záznamov a typy entít uvedené vo fiktívnom scenári Fabrikam Robotics zobrazujú podľa očakávania.

Po úplnom načítaní vzorových údajov sa prihláste ako používateľ Spencer Low a potvrďte toto:

- Ak je nainštalovaná aplikácia Project Service, prejdite na **Project Service** > **Nastavenia** > **Cenníky**. Potvrdiť, že sadzby fakturácie a sadzby nákladov existujú s primeranou menou pre každú krajinu alebo región v množine údajov.

- Ak je nainštalovaná aplikácia Project Service, prejdite na **Universal Resource Scheduling** > **Nastavenia** > **Organizačné jednotky**. Potvrďte, že zoznam obstarávacích cien s primeranou menou bol spojený s každou jednotkou organizácie (okrem mestských položiek). Ak čokoľvek chýba, vyhľadajte a priraďte správny zoznam obstarávacích cien.

- Ak je nainštalovaná aplikácia Field Service, prejdite na **Project Service** > **Nastavenia** > **Cenníky**. Skontrolujte, či existujú sadzby fakturácie a sadzby nákladov. Prejdite do **Field Service** > **Nastavenia** > **Cenníky** a skontrolujte, či existujú sadzby fakturácie a sadzby nákladov s primeranou menou pre každú krajinu alebo región v množine údajov.

  > [!div class="mx-imgBorder"]
  > ![Snímka obrazovky aktívnych cenníkov](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Snímka obrazovky aktívnych organizačných jednotiek](media/sample-data-5.png)

## <a name="technical-notes"></a>Technické poznámky

Nižšie sú uvedené ďalšie technické podrobnosti o inštalácii týchto údajov.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Inštalácia vzorových údajov nad existujúce údaje (neodporúča sa)

Ak potrebujete inštalovať vzorové údaje do existujúcej skúšobnej alebo demo verzie prostredia Project Service alebo Field Service, ktoré už obsahuje údaje, budete musieť pozastaviť bezpečnostné predbežné kontroly, ktoré vykonáva inštalátor.

Ak to chcete urobiť, prejdite do priečinka **PkgFolder**, vyhľadajte a otvorte súbor **DemoDataPreImportConfig.xml** v Poznámkovom bloku (alebo inom editore XML).

Nájdite nasledujúcu hodnotu, a potom zmeňte nastavenie z pravdivého na nepravdivé:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Táto zmena spôsobí, že inštalátor obíde niektoré dôležité bezpečnostné kontroly, vrátane:

- Potvrdenie, že neexistuje viac ako jeden aktívny záznam **Organizačná jednotka** a následné premenovanie na **Fabrikam US**.

- Potvrdenie, že neexistuje viac ako jeden aktívny záznam **Šablóna práce**.

- Potvrdenie, že neexistuje viac ako jeden aktívny záznam **Parameter projektu** a následné premenovanie tejto položky na **Parametre**.

### <a name="configuration-components"></a>Konfigurácia súčastí

Existuje množstvo ďalších konfigurácií súčastí v tomto konfiguračnom súbore predbežného importu. Pre technicky zdatných používateľov sem patria:

- **\<RequiredSolutions\>** určuje nevyhnutné inštalácie riešenia a ich čísla verzií.

- **\<InstallSampleData\>** ovláda, či sa nainštalujú pripravené vzorové údaje pre a aplikácie.

    - nepravda – vynechá sa inštalácia týchto vstavaných dát (ktoré sa dajú odstrániť)

    - pravda – nainštalujú sa vstavené údaje súčasne s inštaláciou vzorových údajov FS a PSA

- **\<PreImportDataCollection\>** určuje textové súbory mám údajov a pridružené záznamy na import pred inštaláciou hlavných vzorových údajov.

- **\<EntitiesToEnableScheduling\>** určuje, ktoré entity by mali byť povolené pre rezerváciu v Microsoft Dynamics Scheduling (alias Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** určuje rezervovateľné zdroje, ktoré sa vytvoria (ak ešte neexistujú) predtým, než sa spustí import vzorových údajov. Upozorňujeme, že vzorové údaje zdrojového systému rezervovateľného zdroja zodpovedajú záznamov rezervovateľného zdroja cieľového systému z hľadiska úplného mena a prihlasovacieho mena každého zdroja. Preto NIE JE možné zmeniť názvy v tomto predkonfiguračnom súbore, pokiaľ najprv nenaimportujete vzorové údaje do cieľového systému pomocou týchto názvov a potom nepremenujte rezervovateľné zdroje na vami zvolené meno set spolu so záznamami povoleného používateľa, a potom neexportujete údaje znovu pre import do vášho finálneho cieľového systému (aktualizácia starých a nových položiek **ImportUserMapFile.xml** zodpovedajúcim spôsobom).

- **\<PluginsToDisable\>** určuje veľmi diskrétne riadkové položky doplnkov, ktoré musia byť zakázané počas importu vzorových údajov a potom opätovne povolené.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fiktívny scenár Fabrikam Robotics

Balíky ukážkových referenčných údajov Field Service a Project Service nainštalujú **riešenie Fabrikam Manufacturing Master Data (ver. 3.0.0.0)** spolu s približne 4000 záznamami a približne 40 rôznymi entitami. Samostatné balíky vzorových údajov pre Field Service alebo Project Service obsahujú podmnožinu vzorových údajov **v902FPSMasterData** pre danú aplikáciu. Balík **ukážkových údajov** nainštaluje **riešenie Fabrikam Manufacturing Demo Data (v3.0.0.7)** s približne 22 000 záznamami a 148 entitami.

Fiktívna spoločnosť Fabrikam Robotics je výrobca robotických liniek na montáž elektronických zariadení a je známa svojou kvalitou výrobkov, inováciami a solídnym zákazníckym servisom, vrátane plánovania inštalácie, implementácie a službám priebežnej údržby. Fabrikam sídli v Spojených štátoch (Fabrikam US) a má projektové servisné operácie vo Francúzsku, Indii, Veľkej Británii a Švajčiarsku.

Operácie služieb u zákazníka sú sústredené v USA, predovšetkým v aglomerácii Seattle. Spoločnosť je zameraná na využitie pripojenia internetu vecí (IoT) na sledovanie výkonu majetku zákazníka a poskytovanie proaktívnych služieb na mieste.

Podrobný prehľad vzorových údajov:

- Spoločné prvky vzorových údajov (súčasťou pre obe aplikácie)

    - 1 používateľ

    - 71 účtov

    - 137 kontaktov

    - Rôzne typy transakcií a kategórie

    - 50 produktov v 1 cenníku produktov

    - 14 fakturačných/obstarávacích cien

    - 31 charakteristík (odbornosti zdroja) v 2 modeloch hodnotenia s 3 úrovňami (hodnoty hodnotenia)

- Project Service

    - 8 organizačných jednotiek

    - 6 úrovní využitia špecifických pre roly

    - Viac než 2,8 tisíca špecifikácií rol cien

- Field Service

    - 4 územia

    - 5 typov objednávok prác

    - 22 aktív zákazníka

    - 9 typov incidentov s radom priradených charakteristík zdrojov (9), služieb (13) a servisných úloh (13)
   
Balík **ukážkových údajov** nainštaluje približne 179 objednávok prác, 12 projektov a súvisiace transakčné údaje. 

### <a name="change-the-work-hours-for-sample-resources"></a>Zmena pracovnej doby pre ukážkové zdroje

V predvolenom nastavení majú všetky rezervovateľné zdroje kalendár 24 pracovných hodín.

Ak potrebujete zmeniť pracovné hodiny pre vzorové rezervovateľné zdroje, prejdite na **Universal Resource Scheduling** > **Plánovanie** > **Zdroje**.

Vyberte používateľa (napríklad Spencer Low) a zmeňte pracovné hodiny Spencera na hodiny, ktoré chcete použiť pre viacerých používateľov. Prejdite na **Universal Resource Scheduling** > **Nastavenie** > **Šablóny pracovných hodín** a upravte záznam **Predvolená šablóna**. V poli **Šablóna zdrojov** vyberte používateľa s pracovnými hodinami, ktoré chcete použiť na iné zdroje. Prejdite na **Universal Resource Scheduling** > **Plánovanie** > **Zdroje** > **Aktívne rezervovateľné zdroje**. Vyberte zdroje, ktoré chcete zmeniť, a potom vyberte **Nastaviť kalendár**. V rozbaľovacom zozname **Šablóna práce** vyberte šablónu **Predvolená pracovná doba** alebo inú šablónu so správnym správne zdrojom na tvorbu šablón. Keď prejdete na tabuľu plánovania, mali by ste vidieť, že zdroje majú teraz aktualizované pracovné hodiny.

> [!div class="mx-imgBorder"]
> ![Snímka obrazovky aktívnych rezervovateľných zdrojov](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]