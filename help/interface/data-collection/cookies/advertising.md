---
description: Läs mer om Adobe Advertising cookies för att mappa annonsevenemang till konverteringshändelser och, eventuellt, använda den informationen för att optimera annonsanbud.
title: Adobe Advertising cookies
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 1%

---

# Adobe Advertising cookies

Adobe Advertising (tidigare Adobe Advertising Cloud) använder cookies för att mappa annonsengagemangshändelser till konverteringshändelser och, eventuellt, för att använda informationen för att optimera annonserbjudanden.

>[!NOTE]
>
>Taggen Adobe Advertising Javascript som använder [Tjänsten Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) skapar första part [Experience Cloud](experience-cloud.md) `s_ecid` cookies, inte Adobe Advertising cookies.

| Kaknamn | Förfallotid | Storlek | Plats | Beskrivning |
| --- | --- | --- | --- | --- |
| **`_lcc`** | 15 minuter | 52 byte | `everesttech.net` | Lagrar ID:n och tidsstämplar för visningsklickningar. Avgör om en klickningshändelse på en visningsannons gäller för en Adobe Analytics-träff. |
| **`_tmae`** | 1 år | 1 kB | `everesttech.net` | Lagrar kodade ID:n och tidsstämplar för annonsinsatser med hjälp av DSP. Inkluderar användarinteraktion med annonser, till exempel annonser som visades senast |
| **`adcloud`** | 1 år | 50-150 byte | Förste part | Tidsstämplar för besökarens senaste besök på webbplatsen och besökarens senaste sökklick. Lagrar även `ef_id` som skapades när besökaren klickade på en annons. Kopplar besökar-ID:t till relevanta målgruppssegment och konverteringar. Hjälper till att optimera sidinläsningstiden genom att undvika onödiga förfrågningar till Adobe. |
| **`ev_sync_*`** |  | 8 byte | `everesttech.net` | Det datum då synkronisering utförs i `yyymmdd` format. Synkroniserar besökar-ID:t för Adobe Advertising med partnerannonsutbytet. Den skapas för nya besökare och skickar en synkroniseringsbegäran när den har gått ut. Inkluderar cookies `ev_sync_ax`, `ev_sync_bk`, `ev_sync_dd`, `ev_sync_fs`, `ev_sync_ix`, `ev_sync_nx`, `ev_sync_ox`, `ev_sync_pm`, `ev_sync_rc`, `ev_sync_tm`och `ev_sync_yh`. |
| **`everest_g_v2`** | 1 år | ~27 byte | `everesttech.net` | Lagrar webbläsarens och besökarens ID. Skapas efter att en användare först klickat på en annons. Används för att mappa den aktuella och efterföljande klickningen till andra händelser på webbplatsen. |
| **`everest_session_v2`** | Session | ~16 byte | `everesttech.net` | Lagrar aktuellt sessions-ID. |
| **`ev_tm`** | 2 år | ~20 byte | `everesttech.net` | Lagrar Adobe Advertising Demand Side Platform (DSP)-ID:t. Motsvarar besökar-ID:t i `everest_g_v2` cookie. |
| **`id_adcloud`** | 91 dagar | 16 byte | Förste part | Lagrar besökar-ID:t. |

{style="table-layout:auto"}
