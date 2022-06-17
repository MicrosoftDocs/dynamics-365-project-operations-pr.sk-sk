---
title: Manuálne nasadenie aplikácie Project Operations Dataverse s podporou duálneho zápisu
description: Tento článok vysvetľuje, ako manuálne nasadiť operácie projektu Dataverse tak, aby podporovala duálny zápis.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: be80ea3956fbf0264c2eeb7a5e30dd50b77e3c78
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912029"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Manuálne nasadenie aplikácie Project Operations Dataverse s podporou duálneho zápisu

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok vysvetľuje, ako manuálne nasadiť Microsoft Dynamics 365 Project Operations v Microsoft Dataverse takže podporuje duálny zápis. Project Operations zistí konfiguráciu prostredia a pridá ďalšiu podporu pre duálny zápis, ak sú splnené predpoklady.

Počas nasadenia cez Microsoft Dynamics Služby životného cyklu (LCS), ak ste postupovali podľa pokynov v tomto článku, môžete preskočiť nasadenie Microsoft Power Platform integrácia (predtým známa ako Common Data Service prostredie).

Proces nasadenia Project Operations v Dataverse, aby podporoval duálny zápis, má štyri hlavné kroky:

1. [Vytvorte nové prostredie v Dataverse, ktoré podporuje duálny zápis](#create).
2. [Pridajte do prostredia predpoklady pre duálny zápis](#prerequisites).
3. [Pridajte aplikáciu Project Operations Dataverse](#dataverse).
4. [Prepojte svoje prostredia](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Vytvorte nové prostredie v Dataverse, ktoré podporuje duálny zápis.

Na dokončenie tohto postupu sa musíte prihlásiť ako správca.

1. Otvorte [centrum správy Power Platform](https://admin.powerplatform.com) a prihláste sa ako správca.
2. Vytvorte nové prostredie a pomenujte ho.
3. Vyberte typ prostredia. Ak ste sa zaregistrovali na odber skúšobnej ponuky, stlačte možnosť **Skúšobná verzia (na základe predplatného)**.
4. Potvrďte oblasť nasadenia.
5. Aktivujte možnosť **Vytvoriť databázu pre toto prostredie**. 
6. Potvrďte jazyk a potom potvrďte, že sa mena zhoduje s menou pre vaše aplikácie Finance and Operations.
7. Aktivujte možnosť **Aplikácie Dynamics 365** a potvrďte, že je pole **Automaticky nasadiť tieto aplikácie** nastavené na **Žiadne**.
8. Ak je skupina zabezpečenia požadovaná, pridajte ju.
9. Výberom položky **Uložiť** vytvoríte prostredie.
10. Počkajte, kým sa nasadenie nedokončí a prostredie nedosiahne stav **Pripravené**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Pridajte do prostredia predpoklady pre duálny zápis.

Podpora duálneho zápisu obsahuje ďalšie polia, ktoré sa pridávajú ku kľúčovým entitám, ako je napríklad entita **Spoločnosť**. Ak pridávate podporu duálneho zápisu do existujúceho prostredia, bude pravdepodobne potrebné aktualizovať údaje, aby ste podporu povolili. Informácie o tom, ako načítať údaje, nájdete v časti [Bootstrap údajov spoločnosti](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Ďalšie informácie o duálnom zápise nájdete v časti [Systémové požiadavky pre duálny zápis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Dokončením tohto postupu pridáte do svojho prostredia predpoklady pre duálny zápis.

1. Otvorte prostredie, ktoré ste práve vytvorili, a potom prejdite do ponuky **Zdroj** \> **Aplikácie Dynamics 365**.
2. V zozname aplikácii stlačte možnosť **Základné riešenie duálneho zápisu** a nainštalujte ho.
3. Počkajte, kým sa inštalácia nedokončí. Potom stlačte v zozname aplikácii možnosť **Riešenie orchestrácie aplikácie duálneho zápisu** a nainštalujte ju.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Pridanie aplikácie Project Operations Dataverse

Tento postup môžete dokončiť, iba ak ste pred inštaláciou Project Operations dokončili predchádzajúce postupy. Počas inštalácie systém analyzuje konfiguráciu prostredia a v prípade potreby pridáva podporu pre duálny zápis.

1. Otvorte prostredie, ktoré ste vytvorili predtým, a potom prejdite do ponuky **Zdroj** \> **Aplikácie Dynamics 365**.
2. V zozname aplikácií stlačte možnosť **Microsoft Dynamics 365 Project Operations** a nainštalujte ju.

## <a name="link-your-environments"></a><a name="link"></a>Prepojte svoje prostredia

Po Dataverse prostredie, môžete nastaviť prepojenie vo svojich aplikáciách Finance and Operations. Postupujte podľa pokynov v časti [Na prepojenie prostredí použite sprievodcu dvojitým zápisom](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
