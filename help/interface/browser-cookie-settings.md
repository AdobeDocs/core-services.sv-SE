---
description: Lär dig hur du aktiverar sekretessinställningar för webbläsarcookies. Du kan ta bort användare som har blockerat alla cookies i webbläsare för datorer och mobila enheter.
solution: Experience Cloud, Analytics, Target
title: Sekretessinställningar för webbläsarcookies
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 5d852e0e-4004-4f94-a6f7-3a14a96cd42f
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Aktivera sekretessinställningar för webbläsarcookies{#enable-privacy-settings-for-browser-cookies}

Du kan ta bort användare som har blockerat alla cookies i webbläsare för datorer och mobila enheter. Den här funktionen är en sekretessinställning som utesluter användare som avanmäler sig från datainsamlingen, vilket gör att du kan respektera en användares avsikt att stoppa Analytics-bearbetningen.

**Aktivera sekretessinställningar för webbläsarcookies**

1. Navigera till **[!UICONTROL Admin Tools]** > **[!UICONTROL Report Suites]**.
1. Gå till **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Privacy Settings]**.
1. Aktivera **[!UICONTROL Privacy Settings]** (för dator eller mobil).

>[!IMPORTANT]
>
>Många mobilappar (till exempel webbläsaren i appen för Facebook eller Twitter) kan visas som en standardwebbläsare, men tillåter inte alla cookies. Om du aktiverar den här funktionen kan en stor andel mobiltrafik uteslutas från analysrapporter.

**Om Sekretessinställningar för webbläsare**

Lagar och riktlinjer har visat att en användares åtgärd för att blockera cookies är detsamma som en användares åtgärd för att välja bort profilering. Genom att aktivera den här funktionen undantas data som samlats in från webbläsare på stationära datorer, där användaren har angett att webbläsaren ska blockera alla cookies, från analysrapporter. Om Adobe inte känner igen webbläsaren inkluderas data i [!DNL Analytics] rapporter.

Jurister runt om i världen har angett (både i vägledning och i kvittningar) att webbläsar-inställningar för cookies är en indikation på att användaren väljer bort profilering. Dessa lagstiftare har särskilt angett att webbläsarinställningen för att blockera cookies från tredje part är en avanmälningsbegäran från spårning från tredje part (på flera webbplatser). Blockering av alla cookies är en avanmälningsbegäran för all spårning. Även om identifierare på serversidan (som IP-adress eller användaragent) kan vara ett önskvärt alternativ som åsidosätter webbläsar-inställningar för cookies, ser en del lagstiftare dem som ett kringgående av användarens val.
