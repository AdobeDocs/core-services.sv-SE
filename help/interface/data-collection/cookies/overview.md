---
description: Läs om hur lösningar och tjänster i Adobe Experience Cloud använder cookies.
title: Hur cookies används i Experience Cloud
uuid: 4255a13a-917b-4b5f-a7d4-4b2e7521d189
exl-id: 60f1a89e-d989-461b-a6a3-c1df022cd30b
source-git-commit: b4d7cc357393798f2265e09885dd4ea2f80ab31e
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 0%

---

# Cookies som används i Experience Cloud

Många av Adobe Experience Cloud-tjänsterna använder cookies. En cookie är en liten datadel som presenteras av en webbplats för en webbläsare. Webbläsaren lagrar data så att en webbplats kan referera till data vid behov. Den här åtgärden utförs för varje efterföljande begäran om sidor och bilder.

Cookies tillhandahålls för att upprätthålla information under och ibland mellan besök på en webbplats. Cookies gör att enheter kan skiljas från andra webbläsare som visar webbplatsen.

Lagar, bestämmelser och självreglerande principer kräver att du får besökarnas samtycke innan du kan lagra eller hämta information på en dator eller annan webbansluten enhet. Adobe föreslår att ni tillsammans med er juridiska rådgivare granskar vilka lagar, förordningar och principer som styr er användning av cookies.

## Om cookies från första part

Adobe Experience Cloud tjänster använder cookies för att tillhandahålla information om variabler och komponenter som inte finns kvar mellan bildbegäranden och webbläsarsessioner. Där det är möjligt använder Adobe cookies från första part för att registrera aktiviteter på din webbplats. För att spela in aktivitet på olika webbplatser, t.ex. andra domäner som du äger, krävs cookies från tredje part.

Många webbläsare och antispionprogram är utformade för att avvisa och ta bort cookies från tredje part. Adobe ser till att cookies alltid kan anges även om cookies från tredje part blockeras. Det specifika beteendet varierar beroende på om du använder Experience Platform Identity Service (ECID-tjänsten) eller Analytics äldre identifierare (till exempel cookie-filen `s_vi`):

* [Experience Platform Identity Service (ECID Service)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) anger automatiskt cookies från första part oavsett om din samlingsdomän matchar din webbplatsdomän eller inte. Om de inte matchar använder identitetstjänsten JavaScript för att ange cookies i webbplatsens domän.
* Om du använder [Äldre analysidentifierare](analytics.md) (till exempel `s_vi`-cookien) beror det på hur du har konfigurerat din datainsamlingsserver. Om datainsamlingsservern matchar webbplatsens domän anges cookies som förstapartsserver. Om samlingsservern inte matchar din aktuella domän anges cookies som tredjepartsservrar. I det här fallet, om cookies från tredje part blockeras, ställer Analytics in ett återgångs-ID (`s_fid`) från första part i stället för standardcookien för `s_vi`.

Om du vill vara säker på att din samlingsserver matchar webbplatsens domän kan du använda en CNAME-implementering som möjliggör vidarebefordran från en anpassad domän som anges i din CNAME-implementering till Adobe-samlingsservrar. Den här aktiviteten innebär ändringar av företagets DNS-inställningar för att konfigurera ett CNAME-alias så att det pekar mot en värddomän som ligger Adobe. Observera att även om olika Adobe-produkter stöder användning av CNAME används CNAME i samtliga fall för att skapa en tillförlitlig förstapartsslutpunkt för en viss kund och ägs av den kunden. Om du kontrollerar flera domäner kan de använda en enda CNAME-slutpunkt för att spåra användare över sina domäner, men där platsdomänen inte matchar CNAME-domäncookies anges som tredje part.

>[!NOTE]
>
>Oavsett om din samlingsdomän matchar din webbplatsdomän så gör Apple ITP-program (Intelligent Tracking Prevention) de cookies från första part som anges av Adobe kortlivade i webbläsare som styrs av ITP, som inkluderar Safari på macOS och alla webbläsare på iOS och iPadOS. Från november 2020 har cookies som anges via CNAME också samma förfallodatum som cookies som anges via JavaScript. Reservation för ändringar.

## Cookies och sekretess

Att upprätthålla kundens integritet och datasäkerhet är de viktigaste prioriteringarna på Adobe. Adobe deltar i flera integritetsorganisationer och samarbetar med integritetsreglerande organ och självreglerande principer. Samarbetet innefattar programmet Digital Advertising Alliance AdChoices för att ge kunderna information om hur deras information används och valmöjligheter vad gäller användningen.

De flesta cookies som anges av Experience Cloud-produkter innehåller ingen personligt identifierbar information. Dessa cookies och tillhörande data är säkra och används endast för företagets rapporter och för att tillhandahålla relevant innehåll och relevanta annonser. Uppgifterna är inte tillgängliga för tredje part eller andra Adobe-kunder, såvida de inte används i aggregerade branschrapporter. [!DNL Digital Marketing Insight Report] analyserar till exempel aggregerade och anonyma data mellan återförsäljare.

Adobe sammanfogar inte information på webbläsarnivå över olika företag. För att skydda kundens integritet och säkerhet erbjuder vissa av tjänsterna i Experience Cloud företag möjligheten att använda en separat uppsättning cookies för varje webbplats som spåras. Vissa erbjudanden ger även kunderna möjlighet att använda sitt eget domännamn som ägare av cookien. Med den här metoden skapas ett extra lager av sekretess och säkerhet, eftersom cookies från Experience Cloud blir *cookies från första part* som tillhör företagets webbplats permanent.

Cookies kan endast lagra och tillhandahålla den information som tidigare lagrats i dem. De kan inte köra kod eller komma åt annan information som lagras på datorn. Webbläsare begränsar även åtkomsten till cookie-data. Webbläsare tillämpar en skyddsprofil för cookies som gör alla cookie-data tillgängliga endast för den webbplats som ursprungligen angav informationen.

Data som finns i cookies-uppsättningar från Adobe.com webbplats kan till exempel inte visas av någon annan webbplats än Adobe.com.

I följande diagram visas användningen av cookies för en standardbildbegäran:

![Cookie-användning för en standardbildbegäran](assets/CookiesProcessGraphic-01.png)

I följande diagram visas cookie-användning för en rak bildbegäran (används i scenarier där en JS-fil inte har lästs in):

![Cookie-användning för en begäran om rak bild](assets/CookiesProcessGraphic2.png)
