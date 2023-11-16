---
description: Läs om hur Adobe Analytics använder cookies för att ge information om variabler och komponenter som inte finns kvar mellan bildbegäranden och webbläsarsessioner.
solution: Experience Cloud,Analytics
title: "cookies från första part"
index: y
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 92d03444472fc7dddbe955d386452291ed1ca2d8
workflow-type: tm+mt
source-wordcount: '1616'
ht-degree: 0%

---

# Om cookies från första part

Analytics använder cookies för att ge information om variabler och komponenter som inte finns kvar mellan bildbegäranden och webbläsarsessioner. Där det är möjligt använder Adobe cookies från första part för att registrera aktiviteter på din webbplats. För att spela in aktivitet på olika webbplatser, t.ex. andra domäner som du äger, krävs cookies från tredje part.

Många webbläsare och antispionprogram är utformade för att avvisa och ta bort cookies från tredje part. Adobe ser till att cookies alltid kan anges även om cookies från tredje part blockeras. Det specifika beteendet varierar beroende på om du använder Experience Platform Identity Service (ECID Service) eller Analytics äldre identifierare (s_vi cookie):

* The [Experience Platform identitetstjänst (ECID-tjänst)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en) konfigurerar automatiskt cookies från första part oavsett om din samlingsdomän matchar din webbplatsdomän. Om de inte matchar använder identitetstjänsten JavaScript för att ange cookies i webbplatsens domän.
* Om du använder [Analysera äldre identifierare](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=en) (även `s_vi` cookie) beror på hur du har konfigurerat din datainsamlingsserver. Om datainsamlingsservern matchar webbplatsens domän anges cookies som förstapartsserver. Om samlingsservern inte matchar din aktuella domän anges cookies som tredje part. I det här fallet, om cookies från tredje part blockeras, ställer Analytics in en första part [fallback-id (s_fid)](cookies-analytics.md) i stället för standardcookien&quot;s_vi&quot;.

Om du vill vara säker på att din samlingsserver matchar webbplatsens domän kan du använda en CNAME-implementering som möjliggör vidarebefordran från en anpassad domän som anges i din CNAME-implementering till Adobe-samlingsservrar. Detta innebär ändringar av företagets DNS-inställningar för att konfigurera ett CNAME-alias så att det pekar mot en värddomän som ligger Adobe. Observera att även om olika Adobe-produkter stöder användning av CNAME används CNAME i samtliga fall för att skapa en tillförlitlig förstapartsslutpunkt för en viss kund och ägs av den kunden. Om du kontrollerar flera domäner kan de använda en enda CNAME-slutpunkt för att spåra användare över sina domäner, men där platsdomänen inte matchar CNAME-domäncookies anges som tredje part.

>[!NOTE]
>
>Oavsett om din samlingsdomän matchar din webbplatsdomän så gör Apple ITP-program (Intelligent Tracking Prevention) de cookies från första part som anges av Adobe kortlivade i webbläsare som styrs av ITP, som inkluderar Safari på macOS och alla webbläsare på iOS och iPadOS. Från november 2020 har cookies som anges via CNAME också samma förfallodatum som cookies som anges via JavaScript. Reservation för ändringar.

Om du vill upprätta en CNAME för datainsamling och om webbplatsen har säkra sidor med HTTPS-protokollet, kan du arbeta med Adobe för att få ett SSL-certifikat.

SSL-certifikatutfärdandeprocessen kan ofta vara förvirrande och tidskrävande. Adobe har därför upprättat ett partnerskap med DigiCert, en branschledande certifikatutfärdare (CA), och utvecklat en integrerad process genom vilken inköp och hantering av dessa certifikat automatiseras.

Med ditt tillstånd arbetar vi med CA för att utfärda, distribuera och hantera ett nytt SHA-2 SSL-certifikat åt dig. Adobe fortsätter att hantera det här certifikatet och ser till att ett oväntat förfallodatum, återkallande eller säkerhetsproblem inte hotar tillgängligheten för din organisations säkra samling.

## Adobe-hanterat certifikatprogram

Adobe Managed Certificate Program är den rekommenderade processen för att konfigurera SSL-certifikat från första part som krävs för en CNAME-implementering som ser till att Adobe-samlingsservern matchar din webbplatsdomän.

Med programmet Hanterat certifikat i Adobe kan du implementera ett nytt SSL-certifikat från första part utan extra kostnad (för dina första 100 CNAME). Om du för närvarande har ett eget kundhanterat SSL-certifikat kan du tala med Adobe kundtjänst om hur du migrerar till det Adobe-hanterade certifikatprogrammet.

### Implementering

Så här implementerar du ett nytt SSL-certifikat från första part för datainsamling:

1. Fyll i [Formulär för begäran om domäner från första part](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx) och öppna en biljett där kundtjänst ber att få ställa in insamling av data från första part i programmet som hanteras av Adobe.

   Varje fält beskrivs i dokumentet med exempel.

1. Skapa CNAME-poster (se instruktionerna nedan).

   När du fått biljetten ska en kundtjänstrepresentant ge dig en CNAME-post. Dessa poster måste konfigureras på företagets DNS-server innan Adobe kan köpa certifikatet åt dig. CNAME liknar följande:

   **Säker** - till exempel värdnamnet `smetrics.example.com` pekar på: `[random-10-character-string].data.adobedc.net`.

   >[!NOTE]
   > Tidigare har Adobe rekommenderat att kunderna ska konfigurera två CNAME, en för HTTPS och en för HTTP. Eftersom det är en bra metod att kryptera trafik, och de flesta webbläsare avråder från HTTP, rekommenderar vi inte längre att du konfigurerar en CNAME för HTTP. Det anses nu som bästa praxis att ange båda `trackingServer` och `trackingServerSecure` med samma CNAME. Till exempel båda `trackingServer` och `trackingServerSecure` ställs in på `smetrics.example.com`. HTTP tillåts bara för värdnamn från tredje part.

1. När CNAME finns på plats arbetar Adobe med DigiCert för att köpa och installera ett certifikat på Adobe produktionsservrar.

   Om ni har en befintlig implementering bör ni överväga att migrera besökarna för att behålla era befintliga besökare. När certifikatet har publicerats till Adobe produktionsmiljö kan du uppdatera dina spårningsservervariabler till de nya värdnamnen. Om platsen inte är säker (HTTP) uppdaterar du `s.trackingServer`. Om webbplatsen är säker (HTTPS) uppdaterar du båda `s.trackingServer` och `s.trackingServerSecure` variabler.

1. [Verifiera vidarebefordran av värdnamn](#validate) (se nedan).

1. [Uppdatera implementeringskod](#update) (se nedan).

### Underhåll och förnyelser

Trettio dagar innan ditt förstapartscertifikat upphör att gälla validerar Adobe om CNAME fortfarande är giltigt och används. I så fall antar Adobe att du vill fortsätta använda tjänsten och automatiskt förnya certifikatet för din räkning.

>[!NOTE]
> Om CNAME har tagits bort och/eller inte längre är giltig (mappas inte till det angivna Adobe SSL-värdnamnet) kan Adobe inte förnya certifikatet och posten i vårt system markeras för borttagning utan ytterligare kommunikation.

### Frågor och svar

| Fråga | Svar |
|---|---|
| **Är den här processen säker?** | Ja, det Adobe-hanterade programmet är säkrare än vår gamla metod eftersom inget certifikat eller någon privat nyckel ändrar händer utanför Adobe och certifikatutfärdaren. |
| **Hur kan Adobe köpa ett certifikat för vår domän?** | Certifikatet kan bara köpas när du har pekat på det angivna värdnamnet (till exempel `telemetry.example.com`) till ett värdnamn som ägs av Adobe. Detta innebär att värdnamnet delegeras till Adobe och att Adobe kan köpa certifikatet för din räkning. |
| **Kan jag begära att certifikatet återkallas?** | Ja, som ägare av domänen har du rätt att begära att certifikatet återkallas. Öppna en biljett hos Kundtjänst om du vill att det här ska bli färdigt. |
| **Använder det här certifikatet SHA-2-kryptering?** | Ja, Adobe arbetar med DigiCert för att utfärda ett SHA-2-certifikat. |
| **Kostar detta något?** | Nej, Adobe erbjuder den här tjänsten till alla nuvarande Adobe-kunder med digitala upplevelser utan extra kostnad. |

{style="table-layout:auto"}

## Skapa CNAME-poster

Organisationens nätverksteam bör konfigurera dina DNS-servrar genom att skapa CNAME-poster. Varje värdnamn vidarebefordrar data till Adobe datainsamlingsservrar.

FPC-specialisten ger dig det konfigurerade värdnamnet och vilken CNAME de ska peka på. Exempel:

* **SSL-värdnamn**:`smetrics.example.com`
* **SSL CNAME**:`[random-10-character-string].data.adobedc.net`

>[!NOTE]
> Om du fortfarande använder osäkert ser det ut så här:
>
> * **Värdnamn som inte är SSL**:`metrics.example.com`
> * **ICKE-SSL CNAME**:`[random-10-character-string].data.adobedc.net`

Så länge implementeringskoden inte ändras kommer det här steget inte att påverka datainsamlingen och kan utföras när som helst efter att implementeringskoden har uppdaterats.

## Verifiera vidarebefordran av värdnamn {#validate}

Följande metoder är tillgängliga för validering:

### Validera med en webbläsare

Om du har konfigurerat en CNAME och har installerat certifikatet kan du använda webbläsaren för validering:

`https://smetrics.adobe.com/_check`

>[!NOTE]
>
>Du får en säkerhetsvarning om inget certifikat är installerat.

### Validera med [!DNL curl]

Adobe rekommenderar att du använder [[!DNL curl]](https://curl.se/) från kommandoraden. ([!DNL Windows] användare kan installera [!DNL curl] från: <https://curl.se/windows/>)

Om du har en CNAME men inget certifikat är installerat kör du:
`curl -k https://smetrics.adobe.com/_check`
Svar: `SUCCESS`

(Med `-k` värdet inaktiverar säkerhetsvarningen.)

Om du har konfigurerat en CNAME och certifikatet är installerat kör du:
`curl https://smetrics.adobe.com/_check`
Svar: `SUCCESS`

### Validera med [!DNL nslookup]

Du kan använda `nslookup` för validering. Använda `smetrics.adobe.com`som ett exempel: öppna en kommandotolk och skriv `nslookup smetrics.adobe.com`

Om allt är korrekt inställt visas en retur som liknar:

```
nslookup smetrics.adobe.com
Server:             10.30.7.247
Address:     10.30.7.247#53

smetrics.adobe.com    canonical name = adobe.com.ssl.d1.sc.omtrdc.net.
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.218.180.161
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 52.39.8.230
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.187.216.46
```

## Uppdatera implementeringskod {#update}

Innan du redigerar kod på din webbplats för att använda datainsamling från första part måste du uppfylla följande krav:

* Begär ett SSL-certifikat genom att följa stegen som beskrivs ovan i *Implementera* i [Adobe-hanterat certifikatprogram](#adobe-managed-certificate-program).
* Skapa CNAME-poster (se ovan).
* Validera värdnamnen (se ovan).

När du har verifierat att dina värdnamn svarar och vidarebefordrar till datainsamlingsservrar i Adobe kan du ändra implementeringen så att den pekar på dina egna värdnamn för datainsamling.

1. Öppna JavaScript-huvudfilen (`s_code.js/AppMeasurement.js`).
1. Om du vill uppdatera kodversionen ersätter du hela `s_code.js/AppMeasurement.js` med den nyare versionen och ersätt eventuella plugin-program eller anpassningar. **eller** Om du bara vill uppdatera koden som är relevant för datainsamling från första part letar du reda på variablerna s.trackingServer och s.trackingServerSecure (om du använder SSL) och pekar dem mot dina nya värdnamn för datainsamling. Exempel:

   ```js
   s.trackingServer = "metrics.example.com";
   s.trackingServerSecure = "smetrics.example.com";
   ```

1. Överför den uppdaterade JavaScript-huvudfilen till din webbplats.

1. Om du övergår till en datainsamling från en långvarig implementering, eller byter till ett annat värdnamn för en egen samling, rekommenderar Adobe att du migrerar besökare från den tidigare domänen till den nya domänen.

Se [Migrering av besökare](https://experienceleague.adobe.com/docs/analytics/technotes/visitor-migration.html?lang=en) i Analytics Implementation Guide.

När du har överfört JavaScript-filen konfigureras allt för insamling av förstahandsdata. Adobe rekommenderar att ni övervakar Analytics-rapporter under de kommande timmarna för att säkerställa att datainsamlingen fortsätter som vanligt. Om så inte är fallet kontrollerar du att alla ovanstående steg har slutförts och att någon av de användare i organisationen som stöds kontaktar Kundtjänst.
