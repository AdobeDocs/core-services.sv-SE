---
title: Adobe Experience Platform Web SDK-cookies
description: Lär dig hur Web SDK använder cookies som kan användas i din implementering.
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
source-git-commit: 66f78a04674a82335f5df20c4c15d983b6ebdc66
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# Adobe Experience Platform Web SDK-cookies

Adobe Experience Platform Web SDK använder cookies för att lagra värden som är specifika för din implementering.

| Namn | Maximal ålder | Beskrivning |
|---|---|---|
| **kndct_orgid_identity** | 34128000 (395 dagar) | Lagrar ECID samt annan information som rör ECID. |
| **kndctr_original_medgivande_check** | 7 200 (2 timmar) | Signalerar servern att söka efter serversidan för medgivandeinställningar. |
| **kndctr_orgid_medgivande** | 15552000 (180 dagar) | Lagrar användarens medgivandeinställning för webbplatsen. |
| **kndctr_orgid_Cluster** | 1 800 (30 minuter) | Lagrar det Edge Network-område som betjänar den aktuella användarens begäran. Regionen används i URL-sökvägen så att Edge Network kan dirigera begäran till rätt region. Om en användare ansluter till en annan IP-adress eller i en annan session dirigeras begäran igen till närmaste region. |
| **mbox** | 63072000 (två år) | Visas när inställningen för målmigrering är true. Det tillåter att Target [mbox cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) anges av Web SDK. |
| **mboxEdgeCluster** | 1 800 (30 minuter) | Visas när inställningen för målmigrering är true. Med den kan Web SDK kommunicera rätt edge-kluster till `at.js` så att målprofilerna kan vara synkroniserade när användare navigerar på en plats. |
| **AMCV_###@AdobeOrg** | 34128000 (395 dagar) | Visas när [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/idmigrationenabled) är aktiverat. Det hjälper när du går över till Web SDK medan vissa delar av webbplatsen fortfarande använder `visitor.js`. |

Edge Network ställer in alla cookies med `secure` och `sameSite="none"` attribut. Om du för närvarande har både säkra och osäkra avsnitt på webbplatsen kan användaridentifieringen vara felaktig. När en användare navigerar från ett säkert avsnitt på webbplatsen till ett osäkert avsnitt, genererar Edge Network ett nytt `ECID` med begäran.
