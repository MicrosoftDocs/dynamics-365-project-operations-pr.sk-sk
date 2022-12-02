---
title: Zdroje v riadku subdodávateľskej zmluvy
description: Tento článok vysvetľuje, ako špecifikovať vyhradené zdroje, ktoré poskytuje dodávateľ pre konkrétny riadok subdodávateľskej zmluvy pre určitý čas.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 04e3e5ee70c50068304a8a6c8f7e93df48ed7e85
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522392"
---
# <a name="subcontract-line-resources"></a>Zdroje v riadku subdodávateľskej zmluvy

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

V Dynamics 365 Project Operations dodávateľ môže špecifikovať zdroje, ktoré sa použijú na dodanie kapacity zdrojov, ktoré sa nakupujú na riadku subdodávateľskej zmluvy pre čas.

## <a name="create-subcontract-line-resources"></a>Vytvorenie zdrojov v riadku subdodávateľskej zmluvy

Ak chcete vytvoriť zdroje v riadku subdodávateľskej zmluvy, postupujte podľa nasledujúcich krokov.

1. Na navigačnej table vyberte položku **Subdodávateľské zmluvy** a otvorte subdodávateľskú zmluvu, s ktorou chcete pracovať.
2. Otvorte riadok subdodávateľskej zmluvy pre čas, v ktorom chcete zadať zdroje dodávateľa.
3. Na karte **Zdroje v riadku subdodávateľskej zmluvy** vyberte na vedľajšej mriežke **+ Nový zdroj v riadku subdodávateľskej zmluvy**.
4. Na stránke **Nový zdroj riadka subdodávateľskej zmluvy** zadajte požadované informácie a potom stlačte **Uložiť a zavrieť**.

Nasledujúca tabuľka vysvetľuje polia na zdroji v riadku subdodávateľskej zmluvy.

| Pole | Popis | Funkčný vplyv |
| ----- | ----------- | ----------------- |
| Rezervovateľný zdroj | Vyberte rezervovateľný zdroj typu **Zmluvný pracovník**, ktorý chcete použiť ako zdroj v riadku subdodávateľskej zmluvy.| Ak ste pre zmluvného pracovníka nevytvorili rezervovateľný zdroj, nechajte toto pole prázdne. Po uložení záznamu sa vytvorí rezervovateľný zdroj.  |
| Kontakt | Zdroj riadka subdodávateľa môžete vytvoriť z existujúceho kontaktu. Pomocou vyhľadávania zobrazte zoznam aktívnych kontaktov v systéme. Vyberte kontakt na dodávateľa tejto subdodávateľskej zmluvy. Ak kontakt, ktorý ste vybrali, nie je platným kontaktom dodávateľa v rámci subdodávky, záznam zdroja riadku subdodávateľskej zmluvy sa neuloží.| Ak pre zvolený kontakt neexistuje žiadny rezervovateľný zdroj, systém vytvorí rezervovaný zdroj pre vybratý kontakt pred vytvorením zdroja v riadku subdodávateľskej zmluvy. |
| Používateľ | Zdroj riadka subdodávateľskej zmluvy môžete vytvoriť výberom aktívneho používateľa. Pomocou vyhľadávania zobrazte zoznam aktívnych používateľov v systéme.| Ak pre zvoleného používateľa neexistuje žiadny rezervovateľný zdroj, systém vytvorí rezervovaný zdroj pre vybraného používateľa pred vytvorením zdroja v riadku subdodávateľskej zmluvy. |
| Počiatočný dátum | Dátum, kedy sa začne plnenie zo strany pracovníka subdodávateľskej zmluvy.| Ak je tento zdroj rezervovaný na obdobie, ktoré spadá pred tento rozsah dátumov, zobrazí sa upozornenie. |
| Konečný dátum | Dátum, kedy sa skončí plnenie zo strany pracovníka subdodávateľskej zmluvy.| Ak je tento zdroj rezervovaný na obdobie, ktoré spadá za tento rozsah dátumov, zobrazí sa upozornenie. |
| Úsilie | Celkový počet hodín úsilia, ktoré zmluvný pracovník strávi na tomto riadku subdodávateľskej zmluvy.| Ak je tento zdroj rezervovaný nad rámec úsilia, ktoré je alokované v rámci tejto subdodávky, zobrazí sa varovanie. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
