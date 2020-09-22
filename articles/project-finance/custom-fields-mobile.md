---
title: Implementujte vlastné polia pre mobilnú aplikáciu Microsoft Dynamics 365 Project Timesheet pre iOS a Android
description: Táto téma poskytuje bežné vzory používania rozšírení na implementáciu vlastných polí.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: 4564bbda-34ea-4647-a9bc-f6ef17b1038b
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 16c3b79dcaaf8c5c491587618256694f82f44753
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755546"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementujte vlastné polia pre mobilnú aplikáciu Microsoft Dynamics 365 Project Timesheet pre iOS a Android

[!include [banner](../includes/banner.md)]

Táto téma poskytuje bežné vzory používania rozšírení na implementáciu vlastných polí. Pokrývajú sa tieto témy:

- Rôzne typy údajov, ktoré podporuje rámec vlastného poľa
- Ako zobraziť polia iba na čítanie alebo upraviteľné polia v záznamoch časových výkazov a ukladať hodnoty poskytnuté používateľom späť do databázy
- Ako zobraziť polia iba na čítanie v hlavičke časového rozvrhu
- Ako integrovať inú vlastnú obchodnú logiku, aby ste do polí zadali predvolené hodnoty a vykonali ďalšie overenie

## <a name="audience"></a>Publikum

Táto téma je určená pre vývojárov, ktorí integrujú svoje vlastné polia do mobilnej aplikácie Microsoft Dynamics 365 Project Timesheet, ktorá je k dispozícii pre Apple iOS a Google Android. Predpokladom je, že čitatelia sú oboznámení s vývojom X++ a funkciou časových výkazov projektu.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Zmluva o údajoch - trieda TSTimesheetCustomField X++

Trieda **TSTimesheetCustomField** je trieda kontraktu údajov X++, ktorá predstavuje informácie o vlastnom poli pre funkčnosť časového rozvrhu. Zoznamy objektov vlastných polí sa odovzdávajú v dátovej zmluve TSTimesheetDetails aj v dátovej zmluve TSTimesheetEntry, aby sa v mobilnej aplikácii zobrazili vlastné polia.

- **TSTimesheetDetails** - Zmluva o hlavičke časového rozvrhu.
- **TSTimesheetEntry** - Zmluva o transakcii s časovým rozvrhom. Skupiny týchto objektov, ktoré majú rovnaké informácie o projekte a **timesheetLineRecId** hodnota predstavuje riadok.

### <a name="fieldbasetype-types"></a>fieldBaseType (typy)

Vlastnosť **FieldBaseType** na objekt **TsTimesheetCustom** určuje typ poľa, ktoré sa zobrazí v aplikácii. Nasledujúce hodnoty **typov**, ktoré sú podporované.

| Typ hodnoty | Typ              | Poznámky |
|-------------|-------------------|-------|
| 0           | Reťazec (a Enum) | Pole sa zobrazuje ako textové pole. |
| 1           | Integer           | Hodnota sa zobrazuje ako číslo bez desatinných miest. |
| 2           | Reálne číslo              | Hodnota sa zobrazuje ako číslo s desatinnými miestami.<p>Skutočnú hodnotu meny v aplikácii zobrazíte pomocou vlastnosti **fieldExtenededType**. Môžete použiť vlastnosť **numberOfDecimals** a nastaviť počet desatinných miest, ktoré sa zobrazia.</p> |
| 3           | Dátum              | Formáty dátumu sú určené používateľom nastavením **Formát dátumu, času a čísla**, ktoré je uvedené v **Preferencie jazyka a krajiny/regiónu** v časti **Možnosti používateľa**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Ak vlastnosť **stringOptions** nie je poskytovaná v objekte **TSTimesheetCustomField** je používateľovi poskytnuté pole s voľným textom.

    Vlastnosť **stringLength** sa dá použiť na nastavenie maximálnej dĺžky reťazca, ktorú môžu používatelia zadať.

- Ak vlastnosť **stringOptions** sa poskytuje v objekte **TSTimesheetCustomField**, tieto prvky zoznamu sú jediné hodnoty, ktoré môžu používatelia vybrať pomocou prepínačov (prepínačov).

    V takom prípade môže pole reťazca slúžiť ako hodnota vymenovania na účely zadania používateľom. Ak chcete uložiť hodnotu do databázy ako vymenovanie, ručne namapujte hodnotu reťazca späť na hodnotu vymenovania pred uložením do databázy pomocou reťazca príkazov (pozrite si časť „Použiť reťazec príkazov v triede TSTimesheetEntryService na uloženie záznamu časového výkazu z aplikácie späť do databázy“ ďalej v tejto téme).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Túto vlastnosť môžete použiť na formátovanie skutočných hodnôt ako meny. Tento prístup je použiteľný, iba ak hodnota **fieldBaseType** je **Reálne**.

- **TSCustomFieldExtendedType:None** – Neaplikuje sa žiadne formátovanie.
- **TSCustomFieldExtendedType::Currency** – Formátovanie hodnoty ako meny.

    Keď je aktívne formátovanie meny, pole **stringValue** možno použiť na odovzdanie kódu meny, ktorý by sa mal zobraziť v aplikácii. Hodnota je hodnotou iba na čítanie.

    Pole **realValue** obsahuje čiastku peňazí, ktorá by sa mali uložiť do databázy.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Túto vlastnosť môžete použiť na určenie miesta, kde sa má vlastné pole v aplikácii zobraziť.

- **TSCustomFieldSection::Header** – Pole sa zobrazí v sekcii aplikácie **Zobraziť ďalšie podrobnosti**. Tieto polia sú vždy iba na čítanie.
- **TSCustomFieldSection::Line** – Toto pole sa zobrazí po všetkých predpripravených riadkových poliach v záznamoch časového rozvrhu. Tieto polia môžu byť upraviteľné alebo iba na čítanie.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Táto vlastnosť identifikuje pole, keď sa hodnoty, ktoré poskytuje aplikácia, uložia späť do databázy.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Táto vlastnosť identifikuje pole, keď sa hodnoty, ktoré poskytuje aplikácia, uložia späť do databázy.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Nastaviť túto vlastnosť na **Áno**, čím stanovíte, že pole v časti zadania časového rozvrhu by mali používatelia upravovať. Nastavte vlastnosť na **Nie**, aby bolo pole iba na čítanie.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Nastavte túto vlastnosť na **Áno**, čím stanovíte, že pole v časti zadania časového rozvrhu musí byť povinné.

### <a name="label-str"></a>označenie (str)

Táto vlastnosť určuje označenie, ktoré sa zobrazuje vedľa poľa v aplikácii.

### <a name="stringoptions-list-of-strings"></a>stringOptions (Zoznam reťazcov)

Táto vlastnosť je použiteľná iba ak je **fieldBaseType** nastavené na **Reťazec**. Ak je možnosť **stringOptions** nastavená, hodnoty reťazcov, ktoré sú k dispozícii na výber pomocou prepínačov, sú určené reťazcami v zozname. Ak nie sú zadané žiadne reťazce, je povolené zadávanie voľného textu do poľa reťazca (príklad nájdete ďalej v časti „Použite reťazec príkazov v triede TSTimesheetEntryService na uloženie záznamu časového výkazu z aplikácie späť do databázy“.)

### <a name="stringlength-int"></a>stringLength (int)

Táto vlastnosť určuje maximálnu dĺžku poľa reťazca. Je použiteľná iba ak je **fieldBaseType** nastavené na **Reťazec**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Táto vlastnosť určuje počet desatinných miest, ktoré sa zobrazujú pre skutočné pole. Je použiteľná iba ak je **fieldBaseType** nastavené na **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Táto vlastnosť riadi poradie, v ktorom sa vlastné polia zobrazia v aplikácii, keď je zadaných viac ako jedno vlastné pole. Najskôr sa zobrazia polia s nižšími číslami.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Pre polia typu **Booleovské**, táto vlastnosť odovzdá boolovskú hodnotu poľa medzi serverom a aplikáciou.

### <a name="guidvalue-guid"></a>guidValue (guid)

Pre polia typu **GUID**, táto vlastnosť odovzdá hodnotu GUID poľa medzi serverom a aplikáciou.

### <a name="int64value-int64"></a>int64Value (int64)

Pre polia typu **Int64**, táto vlastnosť odovzdá Int64 hodnotu poľa medzi serverom a aplikáciou.

### <a name="intvalue-int"></a>intValue (int)

Pre polia typu **Int**, táto vlastnosť odovzdá Int hodnotu poľa medzi serverom a aplikáciou.

### <a name="realvalue-real"></a>realValue (real)

Pre polia typu **Real**, táto vlastnosť odovzdá real hodnotu poľa medzi serverom a aplikáciou.

### <a name="stringvalue-str"></a>stringValue (str)

Pre polia typu **Reťazec**, táto vlastnosť odovzdá hodnotu reťazca poľa medzi serverom a aplikáciou. Používa sa tiež na polia typu **Real**, ktoré sú naformátované ako mena. V prípade týchto polí sa vlastnosť používa na odovzdanie kódu meny do aplikácie.

### <a name="datevalue-date"></a>dateValue (date)

Pre polia typu **Dátum**, táto vlastnosť odovzdá hodnotu dátumu poľa medzi serverom a aplikáciou.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Zobraziť a uložiť vlastné pole v časti zadania časového rozvrhu

Nižšie je snímka obrazovky z mobilnej aplikácie vytvorenia záznamu časového rozvrhu. Zobrazuje vopred pripravené polia a vlastné pole v sekcii „Zadávanie času“ s názvom „Testovací reťazec“ s hodnotou enum už nastavenej „Druhej možnosti”.

![Vyskúšajte vlastné pole reťazca v aplikácii](media/timesheet-entry.jpg)



Nižšie je uvedený obrázok obrazovky z mobilnej aplikácie používateľa, ktorý si vybral jednu z možností výčtu dostupných pre vlastné pole „Testovací reťazec“.  Dve možnosti sú „Prvá možnosť“ a „Druhá možnosť“ zobrazené ako prepínače. Druhá možnosť je momentálne vybraná.

![Prepínače pre vlastné pole Testovací reťazec](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Rozšírte tabuľku TSTimesheetLine tak, aby mala vlastné pole

V typických scenároch je pravdepodobné, že údaje pre vlastné pole v časti zadania časového rozvrhu sa uložia do tabuľky TSTimesheetLine. Iné tabuľky však možno použiť, ak je možné údaje načítať na základe poskytnutého záznamu TSTimesheetTrans alebo ak nemá konkrétny kontext záznamu (napríklad ak je pole v parametroch projektu nastavené ako iba na čítanie),

Upozorňujeme, že vlastné polia nemusia mať žiadne sprievodné záznamy databázy. Môžu byť dynamicky generované na základe logiky X++. Tento prístup môže byť užitočný v scenároch iba na čítanie (príklad dynamicky generovaných vlastných hodnôt polí nájdete v časti „Použiť reťazec príkazov na triede TSTimesheetDetails, metóda buildCustomFieldListForHeader na vyplnenie podrobností časového rozvrhu“.)

Nižšie je snímka obrazovky z Visual Studio stromu aplikačných objektov. Zobrazuje rozšírenie tabuľky TSTimesheetLine s poľom TestLineString pridaným ako vlastné pole.

![Riadkový reťazec](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Použite príkazový riadok v metóde buildCustomFieldList triedy TSTimesheetSettings na zobrazenie poľa v časti zadania časového rozvrhu

Tento kód riadi nastavenia zobrazenia poľa v aplikácii. Napríklad ovláda typ poľa, štítok, či je pole povinné a v ktorej časti sa pole zobrazuje.

Nasledujúci príklad ukazuje pole reťazca pre časové údaje. Toto pole má dve možnosti, **Prvá možnosť** a **Druhá možnosť**, ktoré sú k dispozícii prostredníctvom prepínačov. Pole v aplikácii je spojené s poľom **TestLineString**, ktoré sa pridá do tabuľky TSTimesheetLine.

Všimnite si použitie metódy **TSTimesheetCustomField::newFromMetatdata()** na zjednodušenie inicializácie vlastností vlastného poľa: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** a **numberOfDecimals**. Tieto parametre môžete podľa potreby nastaviť aj manuálne.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Použite príkazový riadok v metóde buildCustomFieldListForEntry triedy TSTimesheetEntry na zadanie hodnôt v časti zadania časového rozvrhu

Metóda **buildCustomFieldListForEntry** sa používa na zadávanie hodnôt do uložených riadkov časového rozvrhu v mobilnej aplikácii. Ako parameter trvá záznam TSTimesheetTrans. Polia z tohto záznamu možno použiť na vyplnenie hodnoty vlastného poľa v aplikácii.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Pomocou reťazca príkazov v triede TSTimesheetEntryService uložíte záznam časového rozvrhu z aplikácie späť do databázy

Ak chcete uložiť vlastné pole späť do databázy pri bežnom používaní, musíte rozšíriť viac metód:

- Metóda **timesheetLineNeedsUpdating** sa používa na zistenie, či bol záznam linky zmenený používateľom v aplikácii a musí byť uložený do databázy. Ak výkon nie je problémom, je možné túto metódu zjednodušiť, aby sa vždy vrátila hodnota **true**.
- Metódy **populateTimesheetLineFromEntryDuringCreate** a **populateTimesheetLineFromEntryDuringUpdate** je možné rozšíriť tak, aby zadávali hodnoty do záznamu databázy TSTimesheetLine z poskytnutého záznamu zmluvy údajov TSTimesheetEntry. V nasledujúcom príklade si všimnite, ako sa mapovanie medzi databázovým poľom a vstupným poľom vykonáva ručne pomocou kódu X++.
- Metóda **populateTimesheetWeekFromEntry** môže byť tiež rozšírená, ak vlastné pole, ktoré je namapované na objekt **TSTimesheetEntry** sa musí zapísať späť do databázovej tabuľky TSTimesheetLineweek.

> [!NOTE]
> Nasledujúci príklad uloží hodnotu **firstOption** alebo **secondOption**, ktorú si používateľ vyberie, do databázy ako nespracovanú hodnotu reťazca. Ak je databázové pole poľom typu **enum**, tieto hodnoty je možné manuálne namapovať na hodnotu enum a potom uložiť do poľa enum v databázovej tabuľke.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Zobraziť a uložiť vlastné pole v časti hlavičky časového rozvrhu

Nižšie je snímka obrazovky z mobilnej aplikácie používateľa prezerajúceho si časový rozvrh. V pravom hornom rohu bolo vybrané tlačidlo „Viac informácií“, aby sa zobrazila možnosť „Zobraziť ďalšie podrobnosti“.  

![Príkaz zobrazenia ďalších podrobností](media/show-more.png)

Nižšie je snímka obrazovky z mobilnej aplikácie zobrazujúca časť „Viac” časového rozvrhu. Do sekcie hlavičky časového výkazu bolo pridané vlastné pole s názvom „Miera využitia tohto časového rozvrhu (vypočítané vlastné pole)“. Vo vlastnom poli je nastavená hodnota iba na čítanie „0,667“.

![Časť Viac](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Rozšírte tabuľku TSTimesheetTable tak, aby mala vlastné pole

V typických scenároch je pravdepodobné, že údaje pre vlastné pole v časti hlavičky časového rozvrhu sa vytiahnu z tabuľky TSTimesheetHeader. Iné tabuľky však možno použiť, ak je možné údaje načítať na základe poskytnutého záznamu TSTimesheetTable alebo ak nemá konkrétny kontext záznamu (napríklad ak je pole v parametroch projektu nastavené ako iba na čítanie),

Upozorňujeme, že vlastné polia nemusia mať žiadne sprievodné záznamy databázy. Môžu byť dynamicky generované na základe logiky X++. Nasledujúci príklad ukazuje tento prístup.

Polia v sekcii hlavičky sú v aplikácii vždy iba na čítanie.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Použite príkazový riadok v metóde buildCustomFieldList triedy TSTimesheetSettings na zobrazenie poľa v časti hlavičky

Tento kód riadi nastavenia zobrazenia poľa v aplikácii. Napríklad ovláda typ poľa, štítok, či je pole povinné a v ktorej časti sa pole zobrazuje.

Nasledujúci príklad ukazuje vypočítanú hodnotu v časti hlavičky v aplikácii.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Použite príkazový riadok v metóde buildCustomFieldListForHeader triedy TSTimesheetDetails na vyplnenie podrobností v časovom rozvrhu

Metóda **buildCustomFieldListForHeader** sa používa na vyplnenie podrobností hlavičky časového rozvrhu v mobilnej aplikácii. Ako parameter vezme záznam TSTimesheetTable. Polia z tohto záznamu možno použiť na vyplnenie hodnoty vlastného poľa v aplikácii. Nasledujúci príklad nečíta z databázy žiadne hodnoty. Namiesto toho používa logiku X++ na vygenerovanie vypočítanej hodnoty, ktorá sa potom zobrazí v aplikácii.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Ďalšie možnosti konfigurovateľnosti/rozšíriteľnosti

### <a name="adding-additional-validation-for-the-app"></a>Pridáva sa ďalšie overenie aplikácie

Existujúca logika pre funkčnosť časového rozvrhu na úrovni databázy bude stále fungovať podľa očakávaní. Môžete prerušiť dokončenie operácií ukladania alebo odosielania a zobraziť konkrétnu chybovú správu **throw error("message to user")** do kódu prostredníctvom reťazca rozšírenia príkazov. Tu sú tri príklady užitočných rozšíriteľných metód:

- Ak **validateWrite** v tabuľke TSTimesheetLine vráti hodnotu **false** počas operácie uloženia riadku časového rozvrhu sa v mobilnej aplikácii zobrazí chybové hlásenie.
- Ak **validateSubmit** v tabuľke TSTimesheetTable vráti hodnotu **false** počas operácie odoslania časového rozvrhu sa v aplikácii používateľovi zobrazí chybové hlásenie.
- Logika, ktorá vypĺňa polia (napríklad **Vlastnosť riadku**) počas metódy **vložiť** v tabuľke TSTimesheetLine bude stále bežať.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Skrytie a označenie vopred pripravených polí ako konfigurácie iba na čítanie

Z parametrov projektu môžete v mobilnej aplikácii urobiť hotové polia iba na čítanie alebo skryté. Nastavte možnosti v časti **Mobilné časové rozvrhy** na karte **Časový rozvrh** stránky **Parametre projektového riadenia a účtovníctva**.

![Parametre projektu](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Zmena aktivít, ktoré sú k dispozícii na výber prostredníctvom rozšírení

Aktivity, ktoré sú k dispozícii na výber pre projekt, sa vypĺňajú cez metódy **getActivitiesForProject()** a **getActivityQuery()** v triede **TsTimesheetProjectService**. Na zmenu tohto správania môžete použiť reťazec príkazov tak, aby zodpovedal vášmu obchodnému scenáru pre aktivity, ktoré sú k dispozícii na výber pre konkrétny projekt.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Zadanie predvolenej kategórie projektu do záznamov časového rozvrhu

Zadanie predvolenej kategórie projektu do položiek časového rozvrhu sa vyskytuje na troch úrovniach. Pomocou reťazca príkazov môžete rozšíriť správanie na ktorejkoľvek alebo všetkých týchto úrovniach, aby ste dosiahli požadované správanie. Používa sa táto hierarchia:

1. Aplikácia sa pokúsi vložiť predvolenú kategóriu z prostriedku projektu. Táto predvolená kategória je nastavená v metóde **getCurrentUserResource** a **getDelegatedResourcesForCurrentUser** v triede **TSTimesheetSettingsService**.
2. Ak predvolená kategória nie je poskytnutá na úrovni prostriedkov projektu, aplikácia sa ju pokúsi stiahnuť z aktivity projektu. Táto predvolená kategória je nastavená v metóde **getActivitiesForProject** v triede **TSTimesheetProjectService**.
3. Ak predvolená kategória nie je poskytnutá na úrovni aktivity, predvolená kategória sa vezme z parametrov projektu. Táto predvolená kategória je nastavená v metóde **getProjectDetailsbyRule** v triede **TSTimesheetProjectService**.
