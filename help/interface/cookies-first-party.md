---
description: Läs om hur Adobe Analytics använder cookies för att ge information om variabler och komponenter som inte finns kvar mellan bildbegäranden och webbläsarsessioner.
keywords: cookies;sekretess
solution: Experience Cloud,Analytics
title: '"cookies från första part"'
index: y
snippet: y
feature: Cookies
topic: Administrering
role: Administrator
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 11b999ef0c0d4f258e8665eb9c5bf427f5d618c4
workflow-type: tm+mt
source-wordcount: '1576'
ht-degree: 0%

---

# Om cookies från första part

Analytics använder cookies för att ge information om variabler och komponenter som inte finns kvar mellan bildbegäranden och webbläsarsessioner. Där det är möjligt använder Adobe cookies från första part för att registrera aktiviteter på din webbplats. För att spela in aktivitet på olika webbplatser, t.ex. andra domäner som du äger, krävs cookies från tredje part.

Många webbläsare och antispionprogram är utformade för att avvisa och ta bort cookies från tredje part, inklusive cookies som används i [!DNL Analytics]-datainsamling. För att underlätta spårningen av hur besökarna interagerar med webbplatsen bör du se till att du har konfigurerat din datainsamling så att den använder cookies från första part:

Det finns två alternativ för att implementera cookies från första part:

* Om du använder Experience Platform Identity Service (ECID Service) anges cookies automatiskt i förstahandskontexten med JavaScript.
* Om du använder [!DNL Analytics] äldre identifierare (kallas `s_vi`-cookie) beror det på hur du har konfigurerat din datainsamlingsserver. Om datainsamlingsservern matchar webbplatsens domän anges cookies som förstapartsserver. Om samlingsservern inte matchar din aktuella domän anges cookies som tredje part. Om cookies från tredje part blockeras ställer [!DNL Analytics] in ett [återgångs-ID (s_fid)](cookies-analytics.md) som förstahandsval i stället för standardcookien &quot;s_vi&quot;.

Om du vill vara säker på att din samlingsserver matchar webbplatsens domän kan du använda en CNAME-implementering som tillåter att cookies ställs in i en förstapartskontext. Detta innebär ändringar av företagets DNS-inställningar för att konfigurera ett CNAME-alias så att det pekar mot en värddomän som ligger Adobe. Observera att även om olika Adobe-produkter stöder användning av CNAME används CNAME i samtliga fall för att skapa en tillförlitlig förstapartsslutpunkt för en viss kund och ägs av den kunden. Om du kontrollerar flera domäner kan de använda en enda CNAME-slutpunkt för att spåra användare över sina domäner, men där platsdomänen inte matchar CNAME-domäncookies anges som tredje part.

>[!NOTE]
>
>För båda alternativen gör Apples ITP-program (Intelligent Tracking Prevention) att förstapartscookies är kortlivade i webbläsare som styrs av ITP, som inkluderar Safari i macOS och alla webbläsare i iOS och iPadOS. Från och med november 2020 har båda typerna av cookies sju dagar på sig. Reservation för ändringar.

För det andra alternativet med CNAME kan du, om webbplatsen har säkra sidor med HTTPS-protokollet, arbeta med Adobe för att erhålla ett SSL-certifikat för att implementera cookies från första part. Adobe rekommenderar starkt att du endast använder HTTPS för datainsamling eftersom Adobe släpper stöd för HTTP-samling under andra halvåret 2020.

SSL-certifikatutfärdandeprocessen kan ofta vara förvirrande och tidskrävande. Adobe har därför upprättat ett partnerskap med DigiCert, en branschledande certifikatutfärdare (CA), och utvecklat en integrerad process genom vilken inköp och hantering av dessa certifikat automatiseras.

Med ditt tillstånd arbetar vi med CA för att utfärda, distribuera och hantera ett nytt SHA-2 SSL-certifikat åt dig. Adobe fortsätter att hantera det här certifikatet och ser till att ett oväntat förfallodatum, återkallande eller säkerhetsproblem inte hotar tillgängligheten för din organisations säkra samling.

## Adobe-hanterat certifikatprogram

Adobe Managed Certificate Program rekommenderas för implementering av ett nytt SSL-certifikat för cookies från första part.

Med programmet Hanterat certifikat i Adobe kan du implementera ett nytt SSL-certifikat från första part för cookies från första part utan extra kostnad (för dina första 100 CNAME). Om du för närvarande har ett eget kundhanterat SSL-certifikat kan du tala med Adobe kundtjänst om hur du migrerar till det Adobe-hanterade certifikatprogrammet.

### Implementera

Så här implementerar du ett nytt SSL-certifikat från första part för cookies från första part:

1. Fyll i formuläret [Begär cookie från första part](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx) och öppna en biljett där kundtjänst begär att få konfigurera cookies från första part i programmet som hanteras av Adobe. Varje fält beskrivs i dokumentet med exempel.

2. Skapa CNAME-poster (se instruktionerna nedan).

   När du fått biljetten ska en kundtjänstrepresentant ge dig en CNAME-post. Dessa poster måste konfigureras på företagets DNS-server innan Adobe kan köpa certifikatet åt dig. CNAME liknar följande:

   **Säker**  - Värdnamnet  `smetrics.example.com` pekar till exempel på:  `example.com.adobedc.net`.

>[!NOTE]
> Tidigare har Adobe rekommenderat att kunderna ska konfigurera två CNAME en för HTTPS och en för HTTP. Eftersom det är en god praxis att kryptera trafik och de flesta webbläsare avråder från HTTP rekommenderar vi inte längre att du konfigurerar en CNAME för HTTP. Om du behöver det skulle det se ut så här:
>    **Osäker** — värdnamnet `metrics.example.com` pekar på: `example.com.adobedc.net`.

1. När CNAME finns på plats arbetar Adobe med DigiCert för att köpa och installera ett certifikat på Adobe produktionsservrar.

   Om du har en befintlig implementering bör du överväga att migrera besökare för att behålla befintliga besökare. När certifikatet har publicerats till Adobe produktionsmiljö kan du uppdatera dina spårningsservervariabler till de nya värdnamnen. Om platsen inte är säker (HTTP) uppdaterar du `s.trackingServer`. Om webbplatsen är säker (HTTPS) uppdaterar du både `s.trackingServer` och `s.trackingServerSecure` variabler.

2. [Validera vidarebefordran](#validate)  av värdnamn (se nedan).

3. [Uppdatera implementeringskod](#update)  (se nedan).

### Underhåll och förnyelser

SSL-certifikat upphör att gälla varje år, vilket innebär att Adobe måste köpa ett nytt certifikat för varje implementering på årsbasis. Alla användare i organisationen som stöds får ett e-postmeddelande varje gång en implementering håller på att upphöra. För att Adobe ska kunna förnya ditt värdnamn måste en användare som stöds svara på e-postmeddelandet från Adobe och ange att du tänker fortsätta använda det förfallande värdnamnet för datainsamling. Då köper och installerar Adobe automatiskt ett nytt certifikat.

### Vanliga frågor

| Fråga | Svar |
|---|---|
| **Är den här processen säker?** | Ja, det Adobe-hanterade programmet är säkrare än vår gamla metod eftersom inget certifikat eller någon privat nyckel ändrar händer utanför Adobe och certifikatutfärdaren. |
| **Hur kan Adobe köpa ett certifikat för vår domän?** | Certifikatet kan bara köpas om du har pekat på det angivna värdnamnet (till exempel `telemetry.example.com`) till ett värdnamn som ägs av Adobe. Detta innebär att värdnamnet delegeras till Adobe och att Adobe kan köpa certifikatet för din räkning. |
| **Kan jag begära att certifikatet återkallas?** | Ja, som ägare av domänen har du rätt att begära att certifikatet återkallas. Du behöver bara öppna en biljett hos Kundtjänst för att få detta färdigt. |
| **Använder det här certifikatet SHA-2-kryptering?** | Ja, Adobe kommer att arbeta med DigiCert för att utfärda ett SHA-2-certifikat. |
| **Kostar detta något?** | Nej, Adobe erbjuder den här tjänsten till alla nuvarande Adobe-kunder med digitala upplevelser utan extra kostnad. |

## Skapa CNAME-poster

Organisationens nätverksteam bör konfigurera dina DNS-servrar genom att skapa CNAME-poster. Varje värdnamn vidarebefordrar data till Adobe datainsamlingsservrar.

FPC-specialisten ger dig det konfigurerade värdnamnet och vilken CNAME de ska peka på. Exempel:

* **SSL-värdnamn**:`smetrics.mysite.com`
* **SSL CNAME**:`mysite.com.adobedc.net`

>[!NOTE]
> Om du fortfarande använder osäkert ser det ut så här:
> * **Värdnamn** som inte är SSL:`metrics.mysite.com`
> * **CNAME** som inte är SSL:`mysite.com.adobedc.net`


Så länge implementeringskoden inte ändras kommer det här steget inte att påverka datainsamlingen och kan utföras när som helst efter att implementeringskoden har uppdaterats.

>[!NOTE]
>
>Experience Cloud Visitor ID-tjänsten är ett alternativ till att konfigurera en CNAME så att cookies från första part aktiveras.

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

(Värdet `-k` inaktiverar säkerhetsvarningen.)

Om du har konfigurerat en CNAME och certifikatet är installerat kör du:
`curl https://smetrics.adobe.com/_check`
Svar: `SUCCESS`

### Validera med [!DNL nslookup]

Du kan använda `nslookup` för validering. Använd `smetrics.adobe.com`som exempel genom att öppna en kommandotolk och skriva `nslookup smetrics.adobe.com`

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

Innan du redigerar kod på din webbplats för att använda cookies från första part måste du uppfylla följande krav:

* Begär ett SSL-certifikat genom att följa stegen ovan i *Implementera*-avsnittet i [Adobe-hanterat certifikatprogram](#adobe-managed-certificate-program).
* Skapa CNAME-poster (se ovan).
* Validera värdnamnen (se ovan).

När du har verifierat att dina värdnamn svarar och vidarebefordrar till datainsamlingsservrar i Adobe kan du ändra implementeringen så att den pekar på dina egna värdnamn för datainsamling.

1. Öppna JavaScript-huvudfilen (`s_code.js/AppMeasurement.js`).
1. Om du vill uppdatera kodversionen ersätter du hela `s_code.js/AppMeasurement.js`-filen med den nyare versionen och ersätter eventuella plugin-program eller anpassningar. **Eller** om du vill uppdatera koden som bara är relevant för cookies från första part ska du leta reda på variablerna s.trackingServer och s.trackingServerSecure (om du använder SSL) och peka dem mot dina nya värdnamn för datainsamling. Använda mysite.com som exempel:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. Överför den uppdaterade JavaScript-huvudfilen till din webbplats.

1. Om du går över till cookies från en långvarig implementering, eller byter till ett annat värdnamn för en egen samling, rekommenderar Adobe att du migrerar besökare från den tidigare domänen till den nya domänen.

Se [Besökarmigrering](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/visitor-migration.html?lang=en) i Analytics Implementeringshandbok.

När du har överfört JavaScript-filen konfigureras allt för insamling av cookie-data från första part. Adobe rekommenderar att ni övervakar Analytics-rapporter under de kommande timmarna för att säkerställa att datainsamlingen fortsätter som vanligt. Om så inte är fallet kontrollerar du att alla ovanstående steg har slutförts och att någon av de användare i organisationen som stöds kontaktar kundtjänst.