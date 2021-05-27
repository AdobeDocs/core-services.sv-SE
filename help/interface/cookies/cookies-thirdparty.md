---
description: Läs om hur stödet för cookies från tredje part har blivit allt mer begränsat i olika webbläsare.
keywords: cookies;sekretess
solution: Experience Cloud,Analytics,Target
title: 'Hur ändringar av cookie-support från tredje part påverkar kunderna '
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
feature: Cookies
topic: Administrering
role: Administrator
level: Experienced
exl-id: 3d12a1b1-c952-4b42-815d-f64b31429cec
source-git-commit: ef6196c3096ac7b26633eb4b1b9b2db26237732a
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---

# Hur ändringar av stöd för cookies från tredje part påverkar kunder{#how-changes-to-third-party-cookie-support-impacts-customers}

I takt med att stödet för cookies från tredje part har blivit allt mer begränsat i olika webbläsare har Adobe arbetat med nya lösningar som noggrant balanserar kundens krav med konsumentens rätt till integritet i alla Adobe Experience Cloud-lösningar.

Följande lista visar hur stöd för cookies från tredje part påverkar aktuella implementeringar av Adobe Experience Cloud-lösningar:

## Adobe Analytics och Adobe Target

* Analyserna och Target påverkas inte i någon större utsträckning eftersom samma webbplatsaktivitet endast bygger på cookies från första part. Det krävs cookies från tredje part för att förstå användaraktivitet i olika domäner. För webbläsare där cookies från tredje part är blockerade går det inte att spåra domäner med hjälp av cookies.

## Adobe Experience Manager

* Eftersom Adobe Experience Manager arbetar helt och hållet inom kundens område finns det minimal interaktion med cookies från tredje part och därför minimalt eller oslagbart.

## Adobe Social

* Sociala medier påverkas inte så länge kunden har den senaste versionen av koden.

## Adobe Advertising Cloud

* Sökning:

   * Om sökningen optimeras baserat på Adobe Analytics data påverkas sökningen på samma sätt som Adobe Analytics.
   * Samlingen av konverteringsdata bör inte påverkas.

* Visa:

   * Dagens återmarknadsföring av displayannonser är helt beroende av användningen av cookies från tredje part.
   * Visningen är också mycket beroende av tillgängligheten av olika annonsnätverks-cookies för synkronisering.
   * Den övergripande effekten är okänd. Men, per första punkt påverkas visningen mer än andra tjänster.
   * Vi arbetar internt och tillsammans med våra annonseringspartners för att utvärdera i vilken utsträckning annonserna påverkar resultatet.
