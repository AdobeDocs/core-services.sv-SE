---
description: Lär dig hur du implementerar DNS-förhämtning för att minska sidinläsningstiden med olika program och tjänster i Experience Cloud.
solution: Experience Cloud
title: Använd DNS-förhämtning
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
topic: Administration
role: Admin
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
source-git-commit: 9ee4d9b0e670dec35cda530892c49e36bf7cc107
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# Använd DNS-förhämtning

Implementera DNS-förhämtning för att minska sidinläsningstiden med olika program och tjänster.

## Om DNS-förhämtning

Webbläsare använder DNS-förhämtning för att automatiskt matcha domännamn som är länkade på en webbsida med deras motsvarande IP-adresser. Förhämtningsprocessen startar när webbläsaren läser in en webbsida. Anta att sidan innehåller en markeringsbar länk till `www.adobe.com`. När en webbläsare läser in den här sidan används [DNS-system](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/) om du vill söka efter det länkade domännamnet och matcha det med en motsvarande numerisk IP-adress. DNS-förhämtning hjälper till att förbättra sidans prestanda eftersom domännamnet redan har matchats med en IP-adress innan en besökare klickar på länken eller knappen. DNS-förhämtningsprocessen är genomskinlig för användarna.

## DNS-förhämtning och Adobe Experience Cloud-program

DNS-förhämtning fungerar automatiskt med statiska, inbäddade länkar på en sida. Detta innebär också att automatisk DNS-förhämtning inte fungerar med olika [!UICONTROL Experience Cloud] program och tjänster eftersom:

* Varje program eller tjänst i Experience Cloud genererar DNS-anrop dynamiskt när sidan läses in.
* Webbläsaren kan inte matcha domännamn med IP-adress innan dessa anrop görs.

Du kan emellertid implementera DNS-förhämtning manuellt med dina Experience Cloud-program. Det gör du genom att lägga till HTML `<dns-prefetch>` -taggen till `<head>` av sidkoden enligt nedan. DNS-förhämtning kan spara några millisekunder av sidinläsningstiden när den implementeras på rätt sätt.

## Exempel på DNS-förhämtningskod

I följande exempel visas hur du gör DNS-förhämtningsanrop till olika [!DNL Experience Cloud] program och tjänster. Vissa förhämtningssamtal kräver [!DNL Adobe] Organisations-ID eller spårningsserverinformation. I de här exemplen finns koden i *kursiv* representerar en variabelplatshållare. Du skulle ersätta koden med din egen [!DNL Adobe] partner-ID, kundkod eller spårningsserverinformation osv.

* **Analyser:** `<link rel="dns-prefetch" href="//data.example.com">`.

  Lägg till en separat tagg för varje DNS-namn om du använder icke-säkra och säkra spårningsservrar.

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Experience Cloud ID-tjänst:** `<link rel="dns-prefetch" href="//fast.examplepartnerid.demdex.net">`

* **Advertising Cloud:**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttech.net">`

* **[!DNL Target]:** `<link rel="dns-prefetch" href="//example.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* [DNS-förhämtning](https://www.chromium.org/developers/design-documents/dns-prefetching) på kromium
