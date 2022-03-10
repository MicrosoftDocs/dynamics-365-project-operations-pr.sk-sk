---
title: Záznam o výdavku (čiastočný)
description: Táto téma poskytuje informácie o tom, ako pracovať so záznamom o výdavku pri čiastočnom nasadení.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 48bf86a5cee475708f93462dc154e21b36240023f0a94cf31c49e9a096951736
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007840"
---
# <a name="expense-entry-lite"></a>Záznam o výdavku (čiastočný)

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Základné alebo čiastočné riadenie výdavkov je schopnosť zaznamenávať jednoduché výdavky. Môžete zaúčtovať výdavky oproti projektu a potom ich schvaľovateľ projektu skontroluje a schváli.

Ďalšie informácie o možnostiach výdavkov v systéme Dynamics 365 Project Operations nájdete v časti [Prehľad výdavkov](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Zachytenie základných výdavkov

Môžete zachytiť svoje výdavky, aby ste ich mohli predložiť schvaľovateľovi.

1. Prejdite do **Výdavky** a vyberte **Nový**.
2. Na stránke **Nové výdavky** zadajte požadované informácie o výdavkoch a potom vyberte **Uložiť**.

## <a name="submit-a-basic-expense"></a>Predloženie základných výdavkov

Keď skončíte so zachytávaním všetkých svojich výdavkov a budete pripravení na ich schválenie, musíte ich predložiť.

1. Prejdite do **Výdavky** a vyberte výdavok. Alebo vyberte všetky výdavky pomocou začiarkavacieho políčka v hlavičke.
2. Stlačte možnosť **Odoslať**. Systém spracuje vybrané položky a potom vytvorí žiadosti o schválenie výdavkov.

## <a name="add-an-attachment"></a>Pridať prílohu

Možno budete musieť poskytnúť schvaľovateľovi ďalšiu dokumentáciu o svojich výdavkovch. Na časovú os záznamu výdavkov môžete pripojiť potvrdenie. Vyberte **Upraviť** a v sekcii **Časová os** potom ťuknutím na ikonu kancelárskej sponky priložte potvrdenie.

## <a name="recall-a-basic-expense"></a>Odvolanie základných výdavkov

Ak omylom predložíte výdavok, môžete ho odvolať. Čas, ktorý je potrebný na odvolanie záznamu o výdavkoch, závisí od fázy jeho schválenia.  Ak schvaľovateľ ešte neschválil záznam, k odvolaniu môže dôjsť okamžite. Ak však už bol záznam schválený, požaduje sa od schvaľovateľa, aby schválil odvolanie a zrušil transakcie.

1. Prejdite do **Výdavky** a potom v zozname výdavkov vyberte výdavok na odvolanie.
2. Vyberte položku **Odvolať**. Ak záznam o výdavkoch ešte nebol schválený, systém ho okamžite odvolá. Ak bol záznam o výdavkoch už schválený, vytvorí sa požiadavka na odvolanie, aby sa schvaľovateľ informoval, že chcete výdavok zrušiť. Schvaľovateľ potom potvrdí, že je možné vykonať zrušenie a záznam sa vráti.

## <a name="delete-a-basic-expense"></a>Odstránenie základných výdavkov

Výdavky, ktoré ešte neboli odoslané, je možné odstrániť. Ak chcete odstrániť výdavok, ktorý už bol predložený, musíte ho najskôr odvolať.

## <a name="see-also"></a>Pozrite si tiež:

- [Prehľad schválení](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]