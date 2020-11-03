---
title: Prehľad schválení
description: Táto téma poskytuje informácie o práci so schválením v Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084224"
---
# <a name="approvals-overview"></a>Prehľad schválení

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Predloženia času a výdavkov prechádzajú pracovným postupom schvaľovania. Po schválení záznamov sa transakcie zaznamenajú do skutočných hodnôt alebo sa čas zarezervuje do harmonogramu.

## <a name="approvals-workflow"></a>Pracovný postup schválenia
Keď vytvoríte a odošlete záznam o čase alebo výdavkoch, vytvorí sa záznam schválenia. Schvaľovateľ projektov alebo váš manažér záznam skontroluje a schváli. Ak sa záznam týka projektu, po jeho schválení sa vytvoria skutočné hodnoty. Vďaka tomu je možné sledovať náklady a fakturácie. 

## <a name="approve-an-entry"></a>Schválenie záznamu
Formulár **Schválenia** umožňuje prepínať medzi rôznymi zobrazeniami, aby ste si mohli pozrieť rôzne typy schválení.
  
1. Prejdite na formulár **Schválenia** a vyberte **Výdavky** , **Čas** alebo **Odvolania**.
2. Skontrolujte každé schválenie a vyberte tie, ktoré chcete schváliť.
3. Vyberte **Schváliť** na schválenie vybraných záznamov.
Systém tieto záznamy spracuje a vytvorí skutočné hodnoty alebo rezerváciu.

## <a name="reject-an-entry"></a>Odmietnutie záznamu
Ako schvaľovateľ projektu možno budete musieť poslať záznam späť používateľovi, ktorý ho opraví.
  
1. Prejdite do formulára **Schválenia** a vyberte záznam, ktorý chcete odmietnuť. 
2. Vyberte **Odmietnuť**.
3. Voliteľné – pridajte komentár do dialógového okna **Komentáre k odmietnutiu** na informovanie používateľa, prečo je záznam odmietnutý.
4. Vyberte položku **OK**. Položka sa vráti používateľovi.
  
## <a name="recall-entries"></a>Odvolanie záznamov
V určitom okamihu bude pravdepodobne potrebné odvolať podaný záznam. Ak záznam nebol schválený, bude okamžite vrátený. Schválený záznam však môže mať podstatný vplyv. Schvaľovateľ projektu je povinný schváliť odvolanie, aby sa transakcia stornovala v skutočných hodnotách.

## <a name="specify-project-approvers"></a>Špecifikovanie schvaľovateľov projektov
Každý projekt má niekoľko členov projektového tímu. Môžete určiť, ktorí členovia tímu sú tiež schvaľovateľmi projektu.

1. Prejdite do formulára **Projekty** a otvorte projekt zo zoznamu.
2. Na karte **Tím** vyberte člena tímu, ktorý bude schvaľovateľom projektu, a potom vyberte **Upraviť**.
3. Nastavte pole **Schvaľovateľ projektu** na **Áno**.
4. Vyberte položku **Uložiť**.
5. Ak chcete pridať ďalších schvaľovateľov projektu, zopakujte kroky 2 až 4.

## <a name="configure-the-users-manager"></a>Konfigurácia manažéra používateľa

1. Prejdite do položky **Nastavenie** > **Zabezpečenie** > **Používatelia**.
2. V zozname vyberte používateľa, ktorému priraďujete manažéra a v oblasti **Informácie o organizácii** vyberte manažéra zo zoznamu. 
3. Vyberte položku **Uložiť**.


