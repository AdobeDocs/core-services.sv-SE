---
description: Läs om hur lösningar och tjänster i Adobe Experience Cloud använder cookies.
title: Hur cookies används i Experience Cloud
uuid: 4255a13a-917b-4b5f-a7d4-4b2e7521d189
exl-id: 60f1a89e-d989-461b-a6a3-c1df022cd30b
source-git-commit: d6dc659104b3b24b60495cd97adb21ebb3962fc7
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---

# Cookies som används i Experience Cloud

Adobe Experience Cloud använder cookies. En cookie är en liten datadel som en webbplats skickar till webbläsaren, som lagrar den för senare bruk. Cookies hjälper webbplatsen att komma ihåg saker när du besöker igen eller förflyttar dig mellan sidor. Cookies hjälper dig att spåra besök och skilja en enhet från en annan.

Lagar kräver ofta att du får tillstånd innan du lagrar eller använder cookies på någons enhet. Adobe rekommenderar att du kontaktar din juridiska avdelning för att få en förståelse för gällande regler.

## Om cookies från första part

Adobe Experience Cloud använder cookies för att spåra information som inte varar mellan sidvisningar eller webbläsarsessioner. När det är möjligt använder Adobe cookies från första part (som är knutna till din egen webbplats). För att spåra aktivitet över flera webbplatser eller domäner som du äger behövs cookies från tredje part.

Vissa webbläsare och antispionprogram blockerar cookies från tredje part. Adobe kan se till att cookies fortfarande fungerar även om cookies blockeras. Hur detta fungerar beror på om du använder Experience Platform Identity Service (ECID) eller äldre Analytics-cookies (som `s_vi`-cookies):

* [Experience Cloud Identity Service](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview): ECID-tjänsten anger alltid cookies från första part, oavsett om din samlingsdomän matchar din webbplatsdomän. Den använder JavaScript för att placera cookien på din webbplats domän.

* [Analyserar äldre identifierare](analytics.md) (till exempel cookie-filen `s_vi`): Om cookies är första eller tredje part beror på din konfiguration:

   * Om din datainsamlingsserver matchar webbplatsens domän är cookies förstapartsservrar.
   * Om det inte matchar är cookies tredje part. Om cookies från tredje part blockeras, ställer Adobe in en reservcookie (`s_fid`) i stället för den vanliga.

Du kan använda en **CNAME-konfiguration** om du vill vara säker på att din samlingsserver matchar webbplatsens domän. Detta innebär att uppdatera dina DNS-inställningar så att de pekar på en anpassad domän (du äger) till Adobe servrar. Detta gör att spårningskakan visas som förstahandsval. En CNAME kan fungera i flera domäner, men alla domäner som inte matchar CNAME kommer ändå att ange cookies från tredje part.

>[!NOTE]
>
>Apple ITP (Intelligent Tracking Prevention) begränsar hur länge Adobe cookies från första part varar, även om din samlingsdomän matchar din webbplatsdomän. ITP påverkar Safari på macOS och alla webbläsare på iOS och iPadOS. Sedan november 2020 upphör cookies som angetts med CNAME att gälla lika snabbt som cookies som angetts med JavaScript. Denna tidsfrist kan komma att ändras i framtiden.

Här är en förenklad version av texten:

## Cookies och sekretess

Adobe tar integritet och datasäkerhet på allvar. Det fungerar med integritetsorganisationer, tillsynsmyndigheter och program som AdChoices för att ge människor kontroll över hur deras data används.

De flesta cookies från Adobe Experience Cloud lagrar inte personuppgifter. De är säkra och används endast av ert företag - för rapportering, innehåll och annonsering. Adobe delar inte dessa data med andra kunder eller tredje part, utom i anonyma branschomfattande rapporter (som Digital Marketing Insight Reports).

Adobe kombinerar inte webbläsardata mellan olika företag. För att skydda integriteten kan vissa Adobe-verktyg låta varje webbplats använda sina egna cookies. Vissa tillåter också att du använder din egen domän för cookies, vilket gör dem säkrare och mer personliga.

Cookies kan bara lagra information som sparats i dem tidigare. De kan inte köra kod eller läsa andra data på din enhet. Webbläsare tillåter bara att cookies läses av den webbplats som ställer in dem. Till exempel kan bara Adobe.com läsa cookies som anges i den.

I följande diagram visas användningen av cookies för en standardbildbegäran:

![Cookie-användning för en standardbildbegäran](assets/CookiesProcessGraphic-01.png)

I följande diagram visas cookie-användning för en rak bildbegäran (används i scenarier där en JS-fil inte har lästs in):

![Cookie-användning för en begäran om rak bild](assets/CookiesProcessGraphic2.png)
