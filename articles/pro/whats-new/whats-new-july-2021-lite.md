---
title: Čo je nové júli 2021 – nasadenie Project Operations Lite
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní nasadenia Project Operations Lite z júla 2021.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7964f38c1bc7a8e0440e2e922ff153fd9bede131
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914007"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Čo je nové júli 2021 – nasadenie Project Operations Lite

_Platí pre: Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

  - Project Operations v prostredí Dataverse verzie 4.12.0.148 alebo 4.12.0.152.

## <a name="quality-updates"></a>Aktualizácie kvality
| **Oblasť funkcií**              | **Číslo odkazu** | **Aktualizácia kvality**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fakturácia a tvorba cien           | 2224046              | Pole **Trieda transakcie** je editovateľné na karte **Detaily riadka cenovej ponuky**, ale je uzamknutá, ak pracujete z ponuky **Detaily riadku cenovej ponuky** na stránke.                                                                     |
| Fakturácia a tvorba cien           | 2224400              | Akcia **Uzavrieť cenovú ponuku ako využitú** nemá úspech, ak cenová ponuka nemá medzníky dátumu.                                                                                                                                    |
| Fakturácia a tvorba cien           | 2234089              | Keď manuálne zadáte popis produktu, vymaže sa po zadaní množstva pre odhad materiálu.                                                                                                                         |
| Fakturácia a tvorba cien           | 2234100              | Mriežka **Nastavenie fakturácie úloh** nezahŕňa stĺpec **Materiál** a jeho hodnota je na karte **Účtovanie úloh** projektu.                                                                                                       |
| Fakturácia a tvorba cien           | 2277409              | ID produktu nie je k dispozícii v podrobnostiach riadku zmluvy pre riadok typu materiálu.                                                                                                                                        |
| Fakturácia a tvorba cien           | 2281728              | Vytvorenie riadku zmluvy zbytočne prehodnocuje skutočnosti, čo spôsobuje výrazné zvýšenie objemu údajov, čo ovplyvňuje výkon.                                                                                |
| Fakturácia a tvorba cien           | 2298668              | Riadky denníka spojené s odvolaným a odstráneným výdavkom sa neodstránia.                                                                                                                                     |
| Fakturácia a tvorba cien           | 2300192              | Keď upravuje faktúru viac používateľov, je možné, aby sa na potvrdenej faktúre vytvoril nový detail riadku faktúry.                                                                                   |
| Fakturácia a tvorba cien           | 2301569              | Faktúry nemožno opraviť, ak bola použitá zadržiavacia čiastka \$0.                                                                                                                                        |
| Fakturácia a tvorba cien           | 2307965              | Ak sa vytvorí cena kategórie s chýbajúcimi hodnotami, zobrazí sa chyba.                                                                                                                           |
| Fakturácia a tvorba cien           | 2326870              | V aplikácii sa vyskytla chyba **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** ak je **producttypecode** null.                                                                            |
| Fakturácia a tvorba cien           | 2332732              | Chyba sa objaví, ak sa míľnik riadka zmluvy vytvorí bez riadku objednávky.                                                                                                                |
| Plánovanie a sledovanie projektu | 2181094              | Rozhranie API pre plánovanie projektu teraz podporuje protokoly PSS a protokoly operačných množín, ktoré sú uložené 90 dní.                                                                                                                  |
| Plánovanie a sledovanie projektu | 2254201              | Štítok **Režim plánovania** je aktualizovaný podrobnosťami, ktoré popisujú predvolenú logiku.                                                                                                                                      |
| Plánovanie a sledovanie projektu | 2300252              | Vyrovnávacia pamäť **openProject** je aktualizovaná a obsahuje majiteľa tokenu v kľúči vyrovnávacej pamäte, **základná adresa URL** a **Adresa URL segmentu** takže prvok **Adresa URL žiadosti** je možné vždy znovu vytvoriť, ak dôjde k zmene **základnej adresy URL**. |
| Plánovanie a sledovanie projektu | 2301312              | **msdyn_membershipstatus** bol odstránený zo zobrazenia **člena projektového tímu**.                                                                                                                                        |
| Plánovanie a sledovanie projektu | 2302759              | Výrobky sú zbytočne načítané v kartách **Priradenia zdrojov**, **Odhady** a **Odhady výdavkov**.                                                                                                        |
| Plánovanie a sledovanie projektu | 2308050              | **CopyProject** zlyhá s chybou „Nepodarilo sa získať token na komunikáciu so vzdialenou službou“.                                                                                                                           |
| Plánovanie a sledovanie projektu | 2322650              | Zobrazenie **Zoznam projektových úloh** bolo aktualizované, aby sa predvolene zobrazoval dátum úlohy.                                                                                                            |
| Plánovanie a sledovanie projektu | 2327266              | **CopyProject** pri kopírovaní odhadov generuje chybu „Kľúč sa nenašiel v slovníku“.                                                                                                      |
| Plánovanie a sledovanie projektu | 2328123              | **CopyProject** vygeneruje chybu „Nepodarilo sa získať token na komunikáciu so vzdialenou službou“.                                                                                                                          |
| Plánovanie a sledovanie projektu | 2336258              | **CopyProject** nesprávne kopíruje názvy pozícií zdrojov.                                                                                                                                                 |
| Fakturácia a tvorba cien           | 2224476              | Pole **Rezervovateľný zdroj** nie je správne predvolené pre prihláseného používateľa na stránke **Využitie materiálu**.                                                                                                            |
| Správa zdrojov           | 2277249              | Pri aktualizácii požiadavky na neprojektové zdroje sa vyskytne chyba.                                                                                                            |
| Správa zdrojov           | 2323869              | Využitie zdrojov správne nerozpozná filtrované zdroje.                                                                                                                                             |
| Čas a výdavky              | 2176538              | Sú aplikované nesprávne operátory filtra na ovládací prvok **Zadanie času**.                                                                                                                                                   |
| Čas a výdavky              | 2177462              | Vymazaním záznamu času v mriežke sa neaktualizuje stav tlačidla **Odoslať**, **Pripomenúť**, **Odstrániť** a **Upraviť záznam** podľa očakávania.                                                                                        |
| Čas a výdavky              | 2299985              | **TimeEntriesImportFromResourceAssignment** nezachováva čas začatia/ukončenia z obrysov priradenia.                                                                                                  |
| Čas a výdavky              | 2318426              | Po zadaní času je možné uzamknuté polia stále upravovať.                                                                                                                                   |
| Čas a výdavky              | 2323749              | Chyba sa vyskytne, keď sa výdavok vytvorí z karty **Súvisiace** rezervovateľného zdroja.                                                                                                      |
| Čas a výdavky              | 2327678              | Keď vytvoríte časový záznam z karty **Súvisiace** rezervovateľného prostriedku, nadradený prostriedok nie je odovzdaný do ovládacieho prvku zadávania času.                                                                            |
| Všeobecné                       | 2296857              | Sledovanie pokroku pri dlhodobých úlohách.                                                                                                                                                                        |
| Všeobecné                       | 2253682              | Riešenie duálneho zápisu Project Operations by sa nemalo inštalovať, keď je základ duálneho zápisu nainštalovaný v prostredí bez riešenia orchestrácie s duálnym zápisom.                                                |
| Všeobecné                       | 2316420              | Poskytovanie Project Service Core zlyhá, ak sa zmení obchodná jednotka používateľa aplikácie.                                                                                                                     |
| Všeobecné                       | 2376405              | Opravený problém s aktualizáciou riadenou vydavateľom (Aktualizácia kvality je k dispozícii vo verzii 4.12.0.152)                                                                                                                     |
