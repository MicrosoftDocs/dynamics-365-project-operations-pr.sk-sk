---
title: Práca s dátovým modelom Project Service Automation
description: Táto téma poskytuje informácie o tom, ako pracovať s dátovým modelom.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 375850b893b7afead8371824606b422d3f36c36de4da908fdf76666bd1b415ee
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002440"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Práca s dátovým modelom Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation rozširuje ostatné entity aplikácií a zavádza svoje vlastné entity v Common Data Service dátovom modeli. Táto téma opisuje niektoré entity, s ktorými sa stretnete v typických scenároch hlásenia PSA.

## <a name="reporting-on-opportunities"></a>Vytváranie zostáv o príležitostiach

Project Service Automation rozširuje entitu **Príležitosti** Dynamics 365 Sales pridaním polí, ktoré umožňujú scenáre založené na projekte. Tieto polia sú identifikované názvom schémy, ktorá je predurčená s **msdyn\_**. Jedno nové pole, ktoré je dôležité pre podávanie správ o možnostiach PSA je **Typ objednávky**. Hodnota **Založené na práci** tohto poľa naznačuje, že príležitosť je príležitosťou PSA. Medzi ďalšie polia, ktoré boli pridané do entity, patria **Zmluvná organizácia**, ktorá zachytáva organizáciu, ktorá drží príležitosť, a **Manažér obchodného vzťahu**, ktorý zachytáva názov správcu účtu, ktorý je zodpovedný za túto príležitosť.

Entita **Riadok príležitosti** obsahuje aj polia, ktoré súvisia s Project Service. **Spôsob fakturácie** udáva, či sa má riadok príležitosti účtovať na základe času a materiálov alebo na základe pevnej ceny, pričom **Projekt** zachytáva názov projektu, ktorý túto príležitosť podporuje. Ostatné polia, ktoré môžete využívať na vykazovanie zachytávajú sumy nákladov a rozpočtov zákazníkov pre položku riadka.

## <a name="reporting-on-quotes"></a>Vykazovanie o cenových ponukách

PSA rozširuje entitu **Cenová ponuka** Sales pridaním polí súvisiacich s projektom. **Typ objednávky** rozlišuje cenové ponuky PSA od cenových ponúk mimo PSA. Hodnota **Založené na práci** tohto poľa naznačuje, že cenová ponuka je cenovou ponukou PSA. Ďalšie polia, ktoré môžu byť relevantné pre vykazovanie cenových ponúk PSA, zahŕňajú polia čiastky, akú sú **Fakturovateľné náklady**, **Nefakturovateľné náklady**, **Hrubá marža**, **Odhady** a **Rozpočet**. Ďalšie užitočné polia označujú, či je cenová ponuka zisková, či už bude dokončená podľa plánu, a či spĺňa očakávania rozpočtu zákazníka.

PSA tiež rozširuje entitu **Riadka cenovej ponuky** Sales. Jedno pole, ktoré PSA pridáva, je **Spôsob fakturácie**, ktoré udáva, ako sa bude účtovať riadok cenovej ponuky (čas a materiály alebo pevná cena). Ostatné polia, ktoré boli pridané do entity zachytávajúcej súvisiaci projekt, ktorý je podporený riadkom cenovej ponuky, fakturácia, náklady a rozpočet.

PSA tiež pridáva nové entity súvisiace s cenovou ponukou k dátovému modelu Dynamics 365. Tu sú niektoré príklady:

- **Podrobnosti o riadku cenovej ponuky** – Táto entita obsahuje podrobnosti odhadu projektu na riadku cenovej skupiny. Má dva záznamy pre každý riadok cenovej ponuky. Jeden záznam uchováva informácie o nákladoch a nákladoch riadka cenovej ponuky a druhý záznam uchováva čiastku predaja a podrobnosti predaja riadka cenovej ponuky.
- **Plán faktúry v riadku cenovej ponuky** – Táto entita obsahuje plán fakturácie pre riadok cenovej ponuky. Tento plán je generovaný na základe fakturačnej frekvencie, ktorá je priradená k riadku cenovej ponuky.
- **Medzník v riadku cenovej ponuky** – Táto entita obsahuje fakturačné míľniky pre riadky cenovej ponuky s pevnou cenou.
- **Rozdelenie analytických údajov riadka cenovej ponuky** – Táto entita obsahuje finančné podrobnosti riadka cenovej ponuky. Tieto podrobnosti môžu byť užitočné pre vykazovanie predajnej sumy s cenovou ponuku a sumy odhadovaných nákladov podľa rôznych dimenzií.

Ostatné entity, ktoré PSA pridáva k cenovým ponukám, sú **Projektový cenník riadka cenovej ponuky**, **Kategória zdroja v riadku cenovej ponuky** a **Kategória transakcie v riadku cenovej ponuky**.

![Schéma znázorňujúca cenovú ponuku, riadok cenovej ponuky a vzťahy projektu.](media/PS-Reporting-image2.png "Schéma znázorňujúca cenovú ponuku, riadok cenovej ponuky a vzťahy projektu")

## <a name="reporting-on-project-contracts"></a>Podávanie správ o projektových zmluvách

PSA rozširuje entitu predajnej **objednávky**, ktorá sa používa na zaznamenávané zmluvy projektu. Pridá dôležité nové pole **Typ objednávky**, ktoré identifikuje zmluvu ako projektovú zmluvu PSA namiesto predajnej objednávky. Hodnota **Založené na práci** tohto poľa naznačuje, že objednávka je zmluvou projektu PSA. Ďalšie nové polia, ktoré sa pridajú do entity **Objednávka**, zachytávajú podrobnosti o nákladoch, stave zmluvy PSA a organizácii, ktorá vlastní zmluvu.

PSA tiež rozširuje entitu **Riadky predajných objednávok**. Medzi polia, ktoré pridáva, patria polia, ktoré zachytávajú metódu fakturácie (čas a materiály alebo pevnú cenu), čiastky rozpočtu zákazníka a základný projekt.

PSA tiež pridáva nové entity, ktoré sú určené pre projektové zmluvy. Tu sú niektoré príklady:

- **Podrobnosti o riadku projektovej zmluvy** – Táto entita obsahuje podrobnosti o úrovni riadka, ktoré sú zrolované do čiastky riadka zmluvy. Tieto môžu byť tak podrobné ako riadkové položky, ktoré sú generované z plánu projektu na úrovni úlohy.
- **Plán faktúr v riadkoch zmluvy** – Táto entita obsahuje plán fakturácie, ktorý vzniká na základe frekvencie faktúry priradenej k riadku zmluvy.
- **Medzník zmluvy** – Táto entita obsahuje fakturačné míľniky pre riadky zmluvy, ktoré majú fakturačný výraz s pevnou cenou.

Ostatné entity, ktoré PSA pridáva k zmluvám, sú **Projektový cenník riadka zmluvy**, **Kategória zdroja v riadku projektovej zmluvy** a **Kategória transakcie v riadku projektovej zmluvy**.

![Schéma znázorňujúca objednávku, riadok objednávky a vzťahy projektu.](media/PS-Reporting-image3.png "Schéma znázorňujúca objednávku, riadok objednávky a vzťahy projektu")

## <a name="reporting-on-projects"></a>Podávanie správ o projektoch

Entita **Projekty** a súvisiace entity sú exkluzívne pre PSA. **Projekt** je entita najvyššej úrovne, ktorá sa používa na zachytenie práce a nákladov na strane operácií. Tu je zoznam súvisiacich entít:

- **Člen projektového tímu** – Táto entita obsahuje podrobnosti o rezervovateľných zdrojoch, ktoré sú priradené k projektu. Tieto zdroje môžu byť generické rezervovateľné zdroje, alebo môžu byť pomenované rezervovateľné zdroje, ktoré sú buď zadané zo strany projektového manažéra, alebo generované z plánu projektu.
- **Projektová úloha** – Táto entita obsahuje úlohy, ktoré tvoria plán projektu alebo plán.
- **Priradenie zdroja** – Táto entita obsahuje priradenie úlohy pre rezervovateľný prostriedok.
- **Požiadavka na zdroj** – Táto entita obsahuje požiadavky pre všetkých členov tímu všeobecných zdrojov.
- **Odhad** a **Riadok odhadu** – Tieto entity majú vzťah hlavičky a čiary a obsahujú odhady výdavkov pre projekt. Odhady úloh sú uložené v entite **Odhad zdroja**.

![Schéma znázorňujúca požiadavku zdroja a vzťahy projektu.](media/PS-Reporting-image4.png "Schéma znázorňujúca požiadavku zdroja a vzťahy projektu")

## <a name="reporting-on-resources"></a>Podávanie správ o zdrojoch

Projektové prostriedky používajú entity **rezervovateľných zdrojov** od Universal Resource Scheduling (URS), ktoré sú zdieľané s inými aplikáciami, ako je napríklad Microsoft Dynamics 365 Field Service. Tu je zoznam entít, ktoré možno budete musieť použiť pri správe o zdrojoch projektu:

- **Rezervovateľný zdroj** – Táto entita predstavuje používateľa, kontakt, všeobecný prostriedok, konto, skupinu alebo zariadenie, ktoré sa používa v projektovom tíme.
- **Charakteristiky rezervovateľných zdrojov** – Táto entita zahŕňa zručnosti, certifikácie alebo vzdelávanie zdroja. Vlastnosti môžu mať hodnoty hodnotenia, ktoré sú definované modelom hodnotenia.
- **Kategória rezervovateľného zdroja** – táto entita predstavuje úlohu rezervovateľného prostriedku.
- **Rezervácie rezervovateľných zdrojov** – táto entita predstavuje čas, ktorý je rezervovaný na projektoch pre zdroj. Každá rezervácia má hlavičku entity a riadok entity a každý riadok má stav, ktorý predstavuje stav rezervácie.

![Schéma znázorňujúca vlastnosti vzťahov rezervovateľných zdrojov.](media/PS-Reporting-image5.png "Schéma znázorňujúca vlastnosti vzťahov rezervovateľných zdrojov")

## <a name="reporting-on-actual-transactions"></a>Podávanie správ o skutočných transakciách

Keď schválime výkaz alebo náklad, alebo faktúru zmluvu v PSA, obchodná transakcia je zachytená v entite **Skutočné hodnoty**. Táto entita môže slúžiť ako základ pre takmer všetky správy týkajúce sa financií v PSA. Entita **Skutočná hodnota** zachytáva náklady a predajné transakcie pre obchodnú udalosť. Zachytáva tiež mnoho relevantných atribútov.

Keď pracujete s entitou **Skutočná hodnota**, je dôležité, aby ste pochopili, aké transakcie alebo transakcie sa zaznamenávajú v entite, a kedy sa transakcie zaznamenávajú. Tu je typický postup pri práci s časmi (tok pre položky výdavkov je podobný):

1. Keď je položka času uložená, v entite **Skutočná hodnota** sa nevytvoria žiadne záznamy.
2. Keď je položka času odoslaná, v entite **Skutočná hodnota** sa nevytvoria žiadne záznamy.
3. Po schválení časovej položky sa vytvorí jeden záznam v entite **Skutočná hodnota** a môže sa vytvoriť aj druhý záznam. Prvý záznam ukladá náklady na zadanie času. Druhý záznam ukladá nefakturovanú čiastku predaja zadania času. Druhý záznam závisí od projektu, ktorý má zákazníka, cenovú ponuku alebo riadok zmluvy, ktorý mu bol priradený.

    | Dátum dokumentu | Typ transakcie | Trieda transakcie | Zákazník         | Zmluva   | Zdroj     | Rola zdroja | Typ fakturácie | Množstvo | Jednotková cena | Čiastka |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Náklady             | Time              | Alpine Ski House | Alpine CRM | Jarmila Gajdošová | Project Mgr   | Účtovateľné   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Nefakturovaný predaj   | Time              | Alpine Ski House | Alpine CRM | Jarmila Gajdošová | Project Mgr   | Účtovateľné   | 8.0      | 100.00     | 800.00 |

    Tieto dva záznamy sú samostatné, ale súvisiace záznamy. Nie sú ani inkasá ani kredity.

4. Ak je zmluva priradená k projektu, keď je položka času fakturovaná, v entite **Skutočná hodnota** sa vytvoria ďalšie dva záznamy. Najprv sa vytvorí záporná čiastka pre nefakturovaný predajný záznam. Tento záznam v podstate vracia nefakturovaný predaj. Po druhé, vytvorí sa transakcia pre fakturovaný predaj. Tieto záznamy sú znova samostatné, ale súvisiace záznamy, nie inkasá ani kredity.

    | Dátum dokumentu | Typ transakcie | Trieda transakcie | Zákazník         | Zmluva   | Zdroj     | Rola zdroja | Typ fakturácie | Množstvo | Jednotková cena | Čiastka   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Nefakturovaný predaj   | Time              | Alpine Ski House | Alpine CRM | Jarmila Gajdošová | Project Mgr   | Účtovateľné   | - 8.0    | 100.00     | - 800.00 |
    | 2/4/18        | Fakturovaný predaj     | Time              | Alpine Ski House | Alpine CRM | Jarmila Gajdošová | Project Mgr   | Účtovateľné   | 8.0      | 100.00     | 800.00   |

Entita **Pôvod transakcie** zaznamenáva pôvod záznamu **Skutočná hodnota** a entita **Kontaktná osoba pre transakciu** zaznamenáva súvisiace záznamy pre záznam **Skutočná hodnota**. Okrem toho záznam **Skutočná hodnota** obsahuje odkazy projektu, projektovú zmluvy (objednávka), rezervovateľný zdroj a zákazníka.

![Schéma znázorňujúca transakčné spojenie, pôvod a skutočné vzťahy.](media/PS-Reporting-image6.png "Schéma znázorňujúca transakčné spojenie, pôvod a skutočné vzťahy")


[!INCLUDE[footer-include](../includes/footer-banner.md)]