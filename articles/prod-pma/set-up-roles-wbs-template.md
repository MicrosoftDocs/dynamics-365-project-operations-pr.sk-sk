---
title: Nastavenie rol v šablónach štruktúry rozdelenia práce
description: Tento článok poskytuje informácie o nastavení informácií o rolách v šablónach štruktúry rozdelenia práce.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8721c5e5798c2b80c6f3eb65cef118d1ade5e680
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920815"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Nastavenie rol v šablónach štruktúry rozdelenia práce

[!include [banner](../includes/banner.md)]

Projektoví manažéri môžu nastaviť šablóny štruktúry rozdelenia práce (WBS), ktoré môžu použiť pri vytváraní štruktúry WBS pre nové projekty. Projektoví manažéri môžu pridávať roly pri vytváraní šablón. Pomocou nasledujúceho postupu môžete priradiť rolu šablóne štruktúry WBS.

1. Vyberte **Projektové riadenie a účtovníctvo** > **Nastaviť** > **Projekty** > **Šablóny štruktúry rozdelenia práce**.
2. Vyberte **Podrobnosti** pre vybranú šablónu štruktúry WBS.
3. Vyberte úlohu v zozname a potom v poli **Rola** vyberte rolu, ktorú chcete priradiť k úlohe.

## <a name="work-with-a-wbs"></a>Práca so štruktúrami WBS

Môžete vytvoriť novú štruktúru WBS alebo skopírovať štruktúru WBS z existujúcej šablóny štruktúry WBS. Projektový manažér môže ľahko spravovať zdroje prideľovaním rolí novým úlohám v štruktúre WBS. Roly je možné vymeniť buď po získaní zdroja, alebo po identifikácii potvrdeného zdroja na prácu na úlohe. Táto flexibilita umožňuje projektovým manažérom vykonávať tieto úlohy:

- Určiť počet zdrojov, ktoré sú potrebné pre pracovné balíčky štruktúry WBS.
- Odhadnúť náklady na projekt.
- Stanoviť predbežný rozpočet.
- Odhadnúť trvanie aktivity na základe rolí a zdrojov.
- Vypracovať niektoré plány riadenia projektu na základe dostupných informácií o projekte.

Do štruktúry WBS boli pridané ďalšie možnosti, aby sa lepšie využila funkčnosť zdrojov.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Možnosť</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Priradenia zdrojov</td>
<td>Zobrazovanie pridelených zdrojov, dátumov, počtu hodín a typu rezervácie pre úlohy v štruktúre WBS.</td>
</tr>
<tr class="even">
<td>Automaticky generovať tím</td>
<td>Automatické pridávanie plánovaných zdrojov pomocou rolí, ktoré sú spojené s úlohou. Služba Finance automaticky navrhuje plánované zdroje pomocou multikriteriálnej rozhodovacej analýzy založenej na rolách. Po nastavení rol a úsilia (hodín) pre úlohy v štruktúre WBS a po uvoľnení štruktúry vyberte <strong>Automaticky generovať tím</strong>. Požadovaný počet plánovaných zdrojov sa pridá do štruktúry WBS a na kartu <strong>Plánovanie projektu a tímu</strong>.</td>
</tr>
<tr class="odd">
<td>Zdroj (rozbaľovací zoznam)</td>
<td>Na stránke <strong>Spustiť priradenie zdrojov</strong> môžete vybrať zdroje pre pevnú alebo predbežnú rezerváciu, na základe zadaného trvania. Môžete upraviť nastavenie zobrazenia, aby ste videli a nastavili trvanie aktivít zdrojov. Zdroje na úrovni pracovného balíka môžete vybrať a priradiť pomocou nasledujúcich možností:
<ul>
<li><strong>Prijať</strong> – Potvrdenie zmien zdroja, ktorý je priradený k úlohe.</li>
<li><strong>Zrušiť</strong> – Zrušenie zmien zdroja, ktorý je priradený k úlohe.</li>
<li><strong>Priradiť automaticky</strong> – Dostupný personálny zdroj, ktorý má zodpovedajúcu rolu, sa automaticky vyberie a priradí k vybranej úlohe.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na stránke **Všetky projekty** vyberte projekt **Fáza 2 inovácie na XYZ**.
2. Vyberte **Plán** > **Aktivity** > **Štruktúra rozdelenia práce**.
3. Vyberte **Nový** a pridajte do štruktúry WBS tieto aktivity prvej úrovne:

    - Inicializácia
    - Plánovanie
    - Vykonáva sa
    - Monitorovanie a riadenie
    - Zatvoriť

4. Nastavenie dátumov a úsilia (hodiny), ako je znázornené na nasledujúcom obrázku.

    [![Nastavenie dátumov a úsilia.](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Vyberte riadok úloh **Inicializácia** a potom v poli **Rola** vyberte **Senior projektový manažér**.
6. Stlačte možnosť **Publikovať**.
7. Na rovnakom riadku v poli **Zdroje** vyberte **Daniel Goldschmidt** a potom vyberte **Prijať**.
8. Vyberte riadok úloh **Plánovanie** a potom v priečinku **Rola** vyberte **Obchodný analytik**.
9. Vyberte **Publikovať** a potom vyberte **Automaticky generovať tím**.
10. V dialógovom okne vyberte **Áno**.
11. V poli **Zdroj** overte, či obsahuje hodnotu **Obchodný analytik 1**.
12. Pre zdroj **Obchodný analytik 1** otvorte vyhľadávanie a vyberte **Spustiť priradenie zdrojov**. Potom vyberte pracovníka pre danú úlohu.
13. Vyberte **Predbežné priradenie** &gt; **Plná kapacita**.

    > [!NOTE] 
    > Nedostanete varovanie, že zadaný zdroj je teraz 2, pretože počet zdrojov zostáva 1.

14. Na stránke **Štruktúra rozdelenia práce** overte priradenie zdrojov v štruktúre WBS a potom vyberte **Uložiť**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]