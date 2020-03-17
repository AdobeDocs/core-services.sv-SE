---
description: Ta bort användare som har blockerat alla cookies i webbläsare på datorer och mobila enheter. Den här sekretessinställningen exkluderar användare som avanmäler sig från datainsamlingen i Analytics.
keywords: cookies;privacy
seo-description: Ta bort användare som har blockerat alla cookies i webbläsare på datorer och mobila enheter. Den här sekretessinställningen exkluderar användare som avanmäler sig från datainsamlingen i Analytics.
seo-title: Aktivera sekretessinställningar för webbläsarcookies
solution: Marketing Cloud,Analytics,Target,Social
title: Aktivera sekretessinställningar för webbläsarcookies
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
translation-type: tm+mt
source-git-commit: 688272e19e9d1828d070889bf8689cab7ed2c9c1

---


# Aktivera sekretessinställningar för webbläsarcookies{#enable-privacy-settings-for-browser-cookies}

Du kan ta bort användare som har blockerat alla cookies i webbläsare för datorer och mobila enheter. Den här funktionen är en sekretessinställning som utesluter användare som avanmäler sig från datainsamling, vilket gör att du kan respektera en användares avsikt att stoppa bearbetningen av analtyk.

**Aktivera sekretessinställningar för webbläsarcookies**

1. Navigera till **[!UICONTROL Admin Tools]** > **[!UICONTROL Report Suites]**.
1. Klicka på **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Privacy Settings]**.
1. Aktivera **[!UICONTROL Privacy Settings]** (för dator eller mobil).

>[!IMPORTANT]
>
>Observera att många mobilappar (till exempel appwebbläsaren för Facebook och Twitter) kan visas som en standardwebbläsare för mobila enheter, men inte alla cookies. Om du aktiverar den här funktionen kan en stor andel mobiltrafik uteslutas från analysrapporter.

**Om Sekretessinställningar för webbläsare**

Lagar och riktlinjer har visat att en användares åtgärd för att blockera cookies är detsamma som en användares åtgärd för att välja bort profilering. Genom att aktivera den här funktionen kommer data som samlats in från datorwebbläsare, där användaren har angett att webbläsaren ska blockera alla cookies, att exkluderas från analysrapporter. Om Adobe inte känner igen webbläsaren inkluderas data i Analytics-rapporter.

Jurister runt om i världen har angett (både i vägledning och i kvittningar) att webbläsar-inställningar för cookies är en indikation på att användaren väljer bort profilering. Dessa lagstiftare har särskilt angett att webbläsarinställningen för att blockera cookies från tredje part är en avanmälningsbegäran från spårning från tredje part (på flera webbplatser). Blockering av alla cookies är en avanmälningsbegäran för all spårning. Även om identifierare på serversidan (som IP-adress eller användaragent) kan vara ett önskvärt alternativ som åsidosätter webbläsar-inställningar för cookies, ser en del lagstiftare dem som ett kringgående av användarens val.