---
title: Zdroje v riadku subdodávateľskej zmluvy
description: Táto téma vysvetľuje, ako špecifikovať vyhradené zdroje, ktoré poskytuje dodávateľ pre konkrétny riadok subdodávateľskej zmluvy pre určitý čas.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323390"
---
# <a name="subcontract-line-resources"></a>Zdroje v riadku subdodávateľskej zmluvy

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

V Dynamics 365 Project Operations dodávateľ môže špecifikovať zdroje, ktoré sa použijú na dodanie kapacity zdrojov, ktoré sa nakupujú na riadku subdodávateľskej zmluvy pre čas.

## <a name="create-subcontract-line-resources"></a>Vytvorenie zdrojov v riadku subdodávateľskej zmluvy

Ak chcete vytvoriť zdroje v riadku subdodávateľskej zmluvy, postupujte podľa nasledujúcich krokov.

1. Na navigačnej table vyberte položku **Subdodávateľské zmluvy** a otvorte subdodávateľskú zmluvu, s ktorou chcete pracovať.
2. Otvorte riadok subdodávateľskej zmluvy pre čas, v ktorom chcete zadať zdroje dodávateľa.
3. Na karte **Zdroje v riadku subdodávateľskej zmluvy** vyberte na vedľajšej mriežke **+ Nový zdroj v riadku subdodávateľskej zmluvy**.
4. Na stránke **Nový medzník v riadku subdodávateľskej zmluvy** zadajte požadované informácie a potom vyberte **Uložiť a zavrieť**.

Nasledujúca tabuľka vysvetľuje polia na zdroji v riadku subdodávateľskej zmluvy.

| Pole |  Popis |
| ----- | ------------ |
| Rezervovateľný zdroj | Vyberte rezervovateľný zdroj typu „zmluvný pracovník“, ktorý chcete použiť ako zdroj v riadku subdodávateľskej zmluvy. Ak ste pre zmluvného pracovníka ešte nevytvorili rezervovateľný zdroj, nechajte toto pole prázdne. Pri uložení záznamu sa vytvorí rezervovateľný zdroj.  |
| Kontakt | Ak je pole **Rezervovateľný zdroj** prázdne, môžete vytvoriť zdroj v riadku subdodávateľskej zmluvy z existujúceho kontaktu. Pomocou vyhľadávania zobrazte zoznam aktívnych kontaktov v systéme. Vyberte kontakt na dodávateľa tejto subdodávateľskej zmluvy. Kontakt, ktorý vyberiete, sa overí pri uložení záznamu. Ak vybraný kontakt nie je platným kontaktom, váš záznam sa neuloží. Ak pre zvolený kontakt neexistuje žiadny rezervovateľný zdroj, systém vytvorí rezervovaný zdroj pre vybratý kontakt pred vytvorením zdroja v riadku subdodávateľskej zmluvy. |
| Používateľ | Ak je pole **Rezervovateľný zdroj** prázdne, môžete vytvoriť zdroj v riadku subdodávateľskej zmluvy výberom aktívneho používateľa. Pomocou vyhľadávania zobrazte zoznam aktívnych používateľov v systéme. Ak pre zvoleného používateľa neexistuje žiadny rezervovateľný zdroj, systém vytvorí rezervovaný zdroj pre vybraného používateľa pred vytvorením zdroja v riadku subdodávateľskej zmluvy. |
| Počiatočný dátum | Dátum, kedy sa začne plnenie zo strany pracovníka subdodávateľskej zmluvy. Ak je tento zdroj rezervovaný na obdobie, ktoré spadá pred tento rozsah dátumov, zobrazí sa upozornenie. |
| Konečný dátum | Dátum, kedy sa skončí plnenie zo strany pracovníka subdodávateľskej zmluvy. Ak je tento zdroj rezervovaný na obdobie, ktoré spadá za tento rozsah dátumov, zobrazí sa upozornenie. |
| Úsilie | Celkový počet hodín úsilia, ktoré pracovník subdodávateľskej zmluvy strávi na tomto riadku subdodávateľskej zmluvy. Ak je tento zdroj rezervovaný nad rámec úsilia, ktorému sú alokované v rámci tejto subdodávateľskej zmluvy, zobrazí sa varovanie. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
