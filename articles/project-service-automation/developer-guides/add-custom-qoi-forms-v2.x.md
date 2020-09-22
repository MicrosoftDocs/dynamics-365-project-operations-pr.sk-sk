---
title: Pridanie nových vlastných formulárov entít (Project Service Automation 2.x)
description: Táto téma poskytuje informácie o pridávaní vlastných formulárov entít pre príležitosti, cenové ponuky, objednávky alebo faktúry v Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9eb9fc5e-4c7d-466c-9362-fdb0faa30506
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 2bd955ad3eb26d31676ac4ad387baccaee913cd2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755497"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Pridanie nových vlastných formulárov entít (Project Service Automation 2.x)

## <a name="type-field"></a>Typ poľa 

Dynamics 365 Project Service Automation spolieha na pole **Typ** (**msdyn\_ordertype**) príležitosti, ponuky, objednávky a faktúry entity na rozlišovanie **založené na práci** verzie týchto entít z **založené na položke** a **založené na službách** verzie. Verzie založené na práci týchto entít spracúva PSA. Veľa obchodnej logiky na strane klienta a na strane servera riešenia závisí od **Typ** poľa. Preto je dôležité, aby sa pole inicializoval správnou hodnotou pri vytvorení entít. Nesprávna hodnota môže spôsobiť nesprávne správanie a určitá obchodná logika nemusí fungovať správne.

## <a name="automatic-form-switching"></a>Automatické prepínanie formulárov

Aby sa predišlo možnému poškodeniu údajov a neočakávanému správaniu, ktoré sú spôsobené nesprávnou inicializáciou a úpravou záznamov entity predaja, PSA teraz obsahuje logiku automatického prepínania formulárov v out-of-box formulárov. Táto logika posúva používateľov na správny formulár pre prácu s verziou na práci založená alebo akýkoľvek iný typ Príležitosti, Ponuky, Objednávky alebo Faktúry entity. Keď používateľ otvorí verziu založenú na práci pre Príležitosti, Ponuky, Objednávky alebo Faktúry entity, formulár sa prepne na **Projektové Informácie**.

Logika automatického prepínania formulára spolieha na mapovanie medzi **formId** hodnotou a **msdyn\_OrderType** poľom. Všetky out-of-box formuláre boli pridané do tohto mapovania. Vlastné formuláre však musia byť manuálne pridané, aby uviedli, ktorá verzia entity je určená na spracovanie. Toto je založené na **msdyn\_OrderType** poli. Ak prepínaniu formulára chýba mapovanie, logika sa prepne na out-of-box formulár, na základe hodnoty, ktorá je uložená v **msdyn\_OrderType** poli entity.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Pridanie vlastných formulárov a zapnutie logiky prepínania formulárov

Nasledujúci príklad ukazuje, ako pridať vlastný formulár, **Moje projektové informácie**, takže pracuje s príležitosťami založenými na práci. Rovnaký proces sa používa na pridávanie vlastných formulárov tak, aby pracovali s ponukami, objednávkami a faktúrami.

Ak chcete vytvoriť vlastnú verziu informačného formulára **Projektové Informácie**, postupujte podľa týchto krokov.

1. V entite príležitosť otvorte formulár **Projektové informácie** a uložte kópiu pod názvom **Moje projektové informácie**.
2. Otvorte nový formulár a potom vo vlastnostiach, sa uistite, že formulár inicializačné skripty z formulára **Projektové Informácie** sú prítomné. 

    > [!IMPORTANT]
    > Neodstraňujte skripty. V opačnom prípade niektoré údaje môžu byť inicializované nesprávne.

3. Skontrolujte, či pole **Typ** (**msdyn\_OrderType**) je prítomný vo formulári. 

    > [!IMPORTANT]
    > Neodstraňujte toto pole. V opačnom prípade inicializácia skriptov zlyhá.

4. Vyhľadajte hodnotu **formId** nového formulára. Tento krok môžete urobiť dvoma rôznymi spôsobmi:

    - Exportujte formulár **Moje informácie o projekte** ako súčasť nespravovaného riešenia a potom vyhľadajte hodnotu **formId** v súbore customization.XML exportovaného riešenia.
    - Otvorte formulár **Moje informácie o projekte** v editore formulárov, a potom vyhľadajte globálne jednoznačný identifikátor (GUID) vedľa parametra **fromId** v URL, ako je znázornené na nasledujúcom obrázku.

    ![Hodnota formId nového formulára v URL](media/how-to-add-custom-forms-in-v2.0.png)

5. Vytvorenie mapovania **msdyn\_ordertype** pre hodnotu **formId** úpravou msdyn\_/salesdocument/PSSalesdocumentcustomFormIds.js webový zdroj. Odstráňte kód zo zdroja a nahraďte ho nasledujúcim kódom.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Uložte a potom zverejnite prispôsobenia.
