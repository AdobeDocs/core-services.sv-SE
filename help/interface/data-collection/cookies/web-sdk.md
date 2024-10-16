---
title: Adobe Experience Platform Web SDK Cookies
description: Lär dig hur Web SDK använder cookies som kan användas i din implementering.
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
source-git-commit: d69af76f6deff4f2b73e67ee7b69b9fee1ee3a2e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Adobe Experience Platform Web SDK-cookies

Adobe Experience Platform Web SDK använder cookies för att lagra värden som är specifika för din implementering.

| Namn | Maximal ålder | Storlek | Beskrivning |
|---|---|---|---|
| **kndctr_&lt;ORG_ID>_identity** | 34128000 (395 dagar) | 100-120 byte (variabel) | Lagrar ECID samt annan information som rör ECID. |
| **kndctr_&lt;ORG_ID>_medgivande** | 15552000 (180 dagar) | 10-11 byte | Lagrar användarens medgivandeinställning för webbplatsen. |
| **kndctr_&lt;ORG_ID>_Cluster** | 1 800 (30 minuter) | 3-5 byte | Lagrar det Edge Network-område som betjänar den aktuella användarens begäran. Regionen används i URL-sökvägen så att Edge Network kan dirigera begäran till rätt region. Om en användare ansluter till en annan IP-adress eller i en annan session dirigeras begäran igen till närmaste region. |
| **mbox** | 63072000 (två år) | | Visas när inställningen för målmigrering är true. Den tillåter att målcookien [mbox](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) anges av Web SDK. |
| **mboxEdgeCluster** | 1 800 (30 minuter) | | Visas när inställningen för målmigrering är true. Det gör att Web SDK kan kommunicera rätt edge-kluster till `at.js` så att målprofiler kan vara synkroniserade när användare navigerar på en webbplats. |
| **AMCV_###@AdobeOrg** | 34128000 (395 dagar) | | Visas när [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/idmigrationenabled) är aktiverad. Det är till hjälp vid övergång till Web SDK medan vissa delar av webbplatsen fortfarande använder `visitor.js`. |

Edge Network ställer in alla cookies med attributen `secure` och `sameSite="none"`. Om du för närvarande har både säkra och osäkra avsnitt på webbplatsen kan användaridentifieringen vara felaktig. När en användare navigerar från ett säkert avsnitt på webbplatsen till ett osäkert avsnitt, genererar Edge Network en ny `ECID` med begäran.
