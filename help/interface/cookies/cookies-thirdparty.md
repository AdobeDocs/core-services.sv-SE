---
description: I takt med att stödet för cookies från tredje part har blivit allt mer begränsat i olika webbläsare har Adobe arbetat på nya lösningar som noggrant balanserar kundens krav med konsumentens rätt till integritet i alla Adobe Experience Cloud-lösningar.
keywords: cookies;privacy
seo-description: I takt med att stödet för cookies från tredje part har blivit allt mer begränsat i olika webbläsare har Adobe arbetat på nya lösningar som noggrant balanserar kundens krav med konsumentens rätt till integritet i alla Adobe Experience Cloud-lösningar.
seo-title: Hur ändringar i stödet för cookies från tredje part påverkar kunderna
solution: Marketing Cloud,Analytics,Target,Social
title: Hur ändringar i stödet för cookies från tredje part påverkar kunderna
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
translation-type: tm+mt
source-git-commit: 012283d79bda42f9dabb20b25903927b075f6d54

---


# Hur ändringar i stödet för cookies från tredje part påverkar kunderna{#how-changes-to-third-party-cookie-support-impacts-customers}

I takt med att stödet för cookies från tredje part har blivit allt mer begränsat i olika webbläsare har Adobe arbetat på nya lösningar som noggrant balanserar kundens krav med konsumentens rätt till integritet i alla Adobe Experience Cloud-lösningar.

Följande lista visar hur stöd för cookies från tredje part påverkar aktuella implementeringar av Adobe Experience Cloud-lösningar:

## Adobe Analytics och Adobe Target

* Kunder med en [förstahandsimplementering](/help/interface/cookies/cookies-first-party.md) påverkas inte alls.
* Kunder som inte använder förstahandsimplementering kan implementera [Experience Platform ID Service](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html) för att lagra ID-cookien som en cookie utan en förstahandsimplementering.

## Adobe Experience Manager

* Eftersom Adobe Experience Manager fungerar helt och hållet inom kundens domän finns det minimal interaktion med cookies från tredje part och är därmed minimal eller obefintlig.

## Adobe Social

* Sociala medier påverkas inte så länge kunden har den senaste versionen av koden.

## Adobe Advertising Cloud

* Sök:

   * Om sökningen optimeras baserat på Adobe Analytics-data påverkas sökningen på samma sätt som Adobe Analytics.
   * Samlingen av konverteringsdata bör inte påverkas.

* Visa:

   * Dagens återmarknadsföring av displayannonser är helt beroende av användningen av cookies från tredje part.
   * Visningen är också mycket beroende av tillgängligheten av olika annonsnätverks-cookies för synkronisering.
   * Den övergripande effekten är okänd. Men, per första punkt påverkas visningen mer än andra tjänster.
   * Vi arbetar internt och tillsammans med våra annonseringspartners för att utvärdera i vilken utsträckning annonserna påverkar resultatet.

* Socialt:

   * Marknadsföringsannonser på Facebook påverkas inte.
   * Facebook Exchange (FBX) påverkas på samma sätt som leverans av displayannonser.
