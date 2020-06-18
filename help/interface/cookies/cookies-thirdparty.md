---
description: I takt med att stödet för cookies från tredje part har blivit allt mer begränsat i olika webbläsare har Adobe arbetat på nya lösningar som noggrant balanserar kundens krav med konsumentens rätt till integritet i alla Adobe Experience Cloud-lösningar.
keywords: cookies;privacy
seo-description: I takt med att stödet för cookies från tredje part har blivit allt mer begränsat i olika webbläsare har Adobe arbetat på nya lösningar som noggrant balanserar kundens krav med konsumentens rätt till integritet i alla Adobe Experience Cloud-lösningar.
seo-title: Hur ändringar i stödet för cookies från tredje part påverkar kunderna
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: Hur ändringar i stödet för cookies från tredje part påverkar kunderna
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
translation-type: tm+mt
source-git-commit: f65132e291ba925ded39d75e92b24cf707d520b5
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---


# Hur ändringar i stödet för cookies från tredje part påverkar kunderna{#how-changes-to-third-party-cookie-support-impacts-customers}

I takt med att stödet för cookies från tredje part har blivit allt mer begränsat i olika webbläsare har Adobe arbetat på nya lösningar som noggrant balanserar kundens krav med konsumentens rätt till integritet i alla Adobe Experience Cloud-lösningar.

Följande lista visar hur stöd för cookies från tredje part påverkar aktuella implementeringar av Adobe Experience Cloud-lösningar:

## Adobe Analytics och Adobe Target

* Kunder med en [förstahandsimplementering](/help/interface/cookies/cookies-first-party.md) påverkas inte alls.
* Kunder som inte använder förstahandsimplementering kan implementera [Experience Platform ID-tjänsten](https://docs.adobe.com/content/help/en/id-service/using/implementation/implementation-guides.html) för att lagra ID-cookien som en cookie utan förstahandsimplementering.

## Adobe Experience Manager

* Eftersom Adobe Experience Manager är helt och hållet verksamt inom kundens område finns det minimal interaktion med cookies från tredje part och därför minimal eller ingen påverkan.

## Adobe Social

* Sociala medier påverkas inte så länge kunden har den senaste versionen av koden.

## Adobe Advertising Cloud

* Sökning:

   * Om sökningen optimeras baserat på Adobe Analytics-data påverkas sökningen på samma sätt som i Adobe Analytics.
   * Samlingen av konverteringsdata bör inte påverkas.

* Visa:

   * Dagens återmarknadsföring av displayannonser är helt beroende av användningen av cookies från tredje part.
   * Visningen är också mycket beroende av tillgängligheten av olika annonsnätverks-cookies för synkronisering.
   * Den övergripande effekten är okänd. Men, per första punkt påverkas visningen mer än andra tjänster.
   * Vi arbetar internt och tillsammans med våra annonseringspartners för att utvärdera i vilken utsträckning annonserna påverkar resultatet.

* Socialt:

   * Marknadsföringsannonser på Facebook påverkas inte.
   * Facebook Exchange (FBX) påverkas på samma sätt som leverans av displayannonser.
