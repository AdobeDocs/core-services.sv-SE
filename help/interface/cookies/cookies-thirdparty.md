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
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# Hur ändringar av stöd för cookies från tredje part påverkar kunder{#how-changes-to-third-party-cookie-support-impacts-customers}

Stödet för cookies från tredje part har blivit mer begränsat i olika webbläsare. Adobe har därför arbetat med nya lösningar som noggrant balanserar kundens krav med konsumentens rätt till integritet mellan olika Experience Cloud-tillämpningar.

Följande lista visar hur stöd för cookies från tredje part påverkar nuvarande implementeringar av Experience Cloud-program:

## Adobe Analytics och Adobe Target

* Analyserna och Target påverkas inte särskilt mycket eftersom samma webbplatsaktivitet endast bygger på cookies från första part. Det krävs cookies från tredje part för att förstå användaraktivitet i olika domäner. För webbläsare där cookies från tredje part blockeras går det inte att spåra domäner med hjälp av cookies.

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
   * Adobe arbetar internt och tillsammans med våra annonspartners för att utvärdera i vilken utsträckning annonserna påverkar resultatet.
