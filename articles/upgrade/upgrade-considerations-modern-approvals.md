---
title: Dôležité informácie týkajúce sa inovácie pre moderné schválenia
description: Tento článok obsahuje body, ktoré by správcovia mali zvážiť pri aktivácii funkcie Moderné schválenia.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931763"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Dôležité informácie týkajúce sa inovácie pre moderné schválenia 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

V rámci vydania 1. vlny z apríla 2022 bude funkcia Moderné schválenia predvolene povolená. Táto funkcia zlepšuje spoľahlivosť logiky schvaľovania a zabezpečuje, že môžete určiť príčinu zlyhania logiky schvaľovania.

V rámci tejto zmeny sa aktualizujú zmeny stavu schvaľovania projektov. Stav teraz prechádza priamo z **Odoslané** ma **Schválené**. **Nevybavené** už nie je stavom schválenia. Ak chcete zistiť, či sa čaká na schválenie, overte, že schválenie je súčasťou množiny schválení, a skontrolujte stav pripojenej množiny schválení.

## <a name="before-you-upgrade"></a>Pred inováciou

Pred inováciou na Moderné schválenia sa uistite, že nemáte žiadne čakajúce schválenia. Funkcia Moderné schválenia nepoužíva stav **Nevybavené**. Preto akékoľvek schválenia, ktoré sú ešte označené ako **Nevybavené**, sa po inovácii nespracujú.

## <a name="after-you-upgrade"></a>Po inovácii

Po inovácii na Moderné schválenia musí správca overiť, či bol povolený postup v cloude, ktorý spracúva schválenia.

1. Prihláste sa do [flow.microsoft.com](https://flow.microsoft.com)
2. V pravom hornom rohu stránky prepnite svoje prostredie na prostredie, ktoré ste inovovali.
3. Vyberte **Riešenia** na zobrazenie riešení, ktoré sú nainštalované v prostredí.
4. V zozname riešení vyberte **Project Operations** alebo **Project Service**.
5. Vymeňte filter zo **Všetky** na **Postupy v cloude**.
6. Overte si, že možnosť **Project Service – Opakovane naplánovať množiny schválení projekt** je nastavená na **Zapnuté**. Ak nie je, vyberte postup a potom vyberte položku **Zapnúť**.
7. Overte si, že spracovanie prebieha každých päť minút kontrolou zoznamu **Systémové úlohy** v oblasti **Nastavenia**.

## <a name="short-term-rollback"></a>Krátkodobé vrátenie zmien

Ak nemôžete prijať zmeny alebo ak narazíte na vážny problém s touto funkciou, môžete sa dočasne vrátiť k pôvodnému postupu schvaľovania vykonaním nasledujúcich krokov:
1. Prihláste sa do svojho prostredia a overte, že neexistujú žiadne nevybavené schválenia.
2. Prejdite do **Nastavenia** > **Parametre projektu**.
3. Vyberte **Ovládanie funkcií** a potom vyberte **Moderné schválenia** na vypnutie funkcie.

## <a name="removing-the-feature-flag"></a>Odstránenie príznaku funkcie

V aktualizácii 2. vlny z októbra 2022 bude možnosť vypnúť túto funkciu odstránená.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
