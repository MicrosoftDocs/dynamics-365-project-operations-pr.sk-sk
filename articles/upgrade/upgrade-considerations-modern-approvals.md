---
title: Úvahy o inovácii pre moderné schválenia
description: Táto téma sa zaoberá bodmi, ktoré by správcovia mali zvážiť, keď povolia funkciu Modern Approvals.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578405"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Úvahy o inovácii pre moderné schválenia 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

V rámci prvého vydania z apríla 2022 bude funkcia Modern Approvals predvolene povolená. Táto funkcia zlepšuje spoľahlivosť logiky schvaľovania a zabezpečuje, že môžete určiť príčinu zlyhania logiky schvaľovania.

V rámci tejto zmeny sa aktualizujú zmeny stavu schvaľovania projektov. Stav teraz prechádza priamo z **Predložené** do **Schválené**. **Čaká na spracovanie** už nie je stavom schválenia. Ak chcete zistiť, či sa čaká na schválenie, overte, že schválenie je súčasťou sady schválení, a skontrolujte stav pripojenej sady schválení.

## <a name="before-you-upgrade"></a>Pred inováciou

Pred inováciou na moderné schválenia sa uistite, že nemáte žiadne čakajúce schválenia. Modern Approvals nepoužíva **Čaká na spracovanie** postavenie. Preto akékoľvek schválenia, ktoré sú ešte označené ako **Čaká na spracovanie** po inovácii sa nespracuje.

## <a name="after-you-upgrade"></a>Po inovácii

Po inovácii na moderné schvaľovania musí správca overiť, či bol povolený cloudový tok, ktorý spracúva schvaľovanie.

1. Prihlásiť sa [flow.microsoft.com](https://flow.microsoft.com)
2. V pravom hornom rohu stránky prepnite svoje prostredie na prostredie, ktoré ste inovovali.
3. Vyberte **Riešenia** na zoznam riešení, ktoré sú nainštalované v prostredí.
4. V zozname riešení vyberte **Projektové operácie** alebo **Projektová služba**.
5. Vymeňte filter z **Všetky** do **Cloud Flows**.
6. Overte si, že **Projektová služba – Opakovane plánujte sady schvaľovania projektov** možnosť je nastavená na **zapnuté**. Ak nie je, vyberte tok a potom vyberte **Zapnúť**.
7. Overte, že spracovanie prebieha každých päť minút kontrolou **Systémové úlohy** zoznam v **nastavenie** oblasť.

## <a name="short-term-rollback"></a>Krátkodobý návrat

Ak nemôžete prijať zmeny alebo ak narazíte na vážny problém s touto funkciou, môžete sa dočasne vrátiť k pôvodnému postupu schvaľovania vykonaním nasledujúcich krokov:
1. Prihláste sa do svojho prostredia a overte, že neexistujú žiadne čakajúce schválenia.
2. Ísť do **nastavenie** > **Parametre projektu**.
3. Vyberte **Ovládanie funkcií** a potom vyberte **Moderné schválenia** na vypnutie funkcie.

## <a name="removing-the-feature-flag"></a>Odstránenie príznaku funkcie

V aktualizácii Wave 2 z októbra 2022 bude možnosť vypnúť túto funkciu odstránená.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
