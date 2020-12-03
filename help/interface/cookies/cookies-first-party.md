---
description: Analytics använder cookies för att ge information om variabler och komponenter som inte finns kvar mellan bildbegäranden och webbläsarsessioner.
keywords: cookies;privacy
seo-description: Analytics använder cookies för att ge information om variabler och komponenter som inte finns kvar mellan bildbegäranden och webbläsarsessioner.
seo-title: Cookies från första part
solution: Experience Cloud,Analytics
title: Cookies från första part
index: y
snippet: y
translation-type: tm+mt
source-git-commit: b34cec87be58b9a4df3e9b061010689e5db4adb6
workflow-type: tm+mt
source-wordcount: '1460'
ht-degree: 0%

---


# Om cookies från första part

Analytics använder cookies för att ge information om variabler och komponenter som inte finns kvar mellan bildbegäranden och webbläsarsessioner. Dessa ofarliga cookies, som härstammar från en domän som är värd för Adobe, kallas cookies från tredje part.

Många webbläsare och antispionprogram är utformade för att avvisa och ta bort cookies från tredje part, bland annat de som används vid datainsamling i Analytics. För att hjälpa er att spåra hur besökarna interagerar med er webbplats kan ni implementera cookies från första part.

Det finns två alternativ för att implementera cookies från första part:

* Experience Platform ID-tjänsten. ID-tjänsten kan ställa in cookien i förstahandskontexten med JavaScript.
* DNS-poster på ditt företags DNS-server för att konfigurera ett CNAME-alias för en värddomän i Adobe. Observera att även om olika Adobe-produkter stöder användning av CNAME används CNAME i samtliga fall för att skapa en tillförlitlig förstapartsslutpunkt för en viss kund och ägs av den kunden. Om den kunden kontrollerar flera domäner kan de använda en enda CNAME-slutpunkt för att spåra användare över sina domäner, men eftersom detta kräver cookies från tredje part för alla domäner utanför CNAME:s domän fungerar det inte när cookies från tredje part blockeras och rekommenderas därför inte. Adobe CNAME används aldrig för att spåra en individ eller enhet över domäner som ägs av olika kunder.

Även om du använder det första alternativet med Experience Cloud ID-tjänsten kommer Apples ITP att göra cookies från första part kortlivade, så det är bäst att använda tillsammans med det andra alternativet.

För det andra alternativet med CNAME kan du, om webbplatsen har säkra sidor med HTTPS-protokollet, arbeta med Adobe för att erhålla ett SSL-certifikat för att implementera cookies från första part. Adobe rekommenderar starkt att du endast använder HTTPS för datainsamling eftersom vi kommer att släppa stödet för HTTP-samling under andra halvåret 2020.

SSL-certifikatutfärdandeprocessen kan ofta vara förvirrande och tidskrävande. Adobe har därför upprättat ett partnerskap med DigiCert, en branschledande certifikatutfärdare (CA), och utvecklat en integrerad process genom vilken inköp och hantering av dessa certifikat automatiseras.

Med ditt tillstånd arbetar vi tillsammans med vår certifikatutfärdare för att utfärda, distribuera och hantera ett nytt SHA-2 SSL-certifikat åt dig. Adobe kommer att fortsätta att hantera det här certifikatet och se till att ett oväntat förfallodatum, återkallande eller säkerhetsproblem inte hotar tillgängligheten för din organisations säkra samling.

## Adobe Managed Certificate Program

Adobe Managed Certificate Program rekommenderas för implementering av ett nytt SSL-certifikat för cookies från första part.

Med programmet Hanterat certifikat i Adobe kan du implementera ett nytt SSL-certifikat från första part för cookies från första part utan extra kostnad (för dina första 100 CNAME). Om du för närvarande har ett eget kundhanterat SSL-certifikat kan du tala med Adobe kundtjänst om hur du migrerar till Adobe Managed Certificate Program.

### Implementera

Så här implementerar du ett nytt SSL-certifikat från första part för cookies från första part:

1. Fyll i formuläret [för begäran om cookie från](/help/interface/cookies/assets/FPC_Request_Form.xlsx) första part och öppna en biljett där kundtjänst begär att få konfigurera cookies från första part för programmet som hanteras i Adobe. Varje fält beskrivs i dokumentet med exempel.

1. Skapa CNAME-poster (se instruktionerna nedan).

   När du får biljetten ska du få ett par CNAME-poster från kundtjänst. Dessa poster måste konfigureras på företagets DNS-server innan Adobe kan köpa certifikatet åt dig. CNAMES kommer att se ut ungefär så här:

   **Säker** - värdnamnet `smetrics.example.com` pekar till exempel på: `example.com.ssl.d1.omtrdc.net`.

   **Osäker** - värdnamnet `metrics.example.com` pekar till exempel på: `example.com.d1.omtrdc.net`.

1. När dessa CNAMES finns på plats kommer Adobe att arbeta med DigiCert för att köpa och installera ett certifikat på Adobe produktionsservrar.

   Om du har en befintlig implementering bör du överväga att migrera besökare för att behålla befintliga besökare. När certifikatet har publicerats till Adobe produktionsmiljö kan du uppdatera dina spårningsservervariabler till de nya värdnamnen. Om platsen inte är säker (HTTP) uppdaterar du `s.trackingServer`. Om webbplatsen är säker (HTTPS) uppdaterar du både `s.trackingServer` - och `s.trackingServerSecure` -variabler.

1. [Validera vidarebefordran](#validate) av värdnamn (se nedan).

1. [Uppdatera implementeringskod](#update) (se nedan).

### Underhåll och förnyelser

SSL-certifikat upphör att gälla varje år, vilket innebär att Adobe måste köpa ett nytt certifikat för varje implementering på årsbasis. Alla användare i organisationen som stöds får ett e-postmeddelande varje gång en implementering närmar sig förfallodatumet. För att Adobe ska kunna förnya ditt värdnamn måste en användare som stöds svara på e-postmeddelandet från Adobe och ange att du tänker fortsätta använda det förfallande värdnamnet för datainsamling. Då köper och installerar Adobe automatiskt ett nytt certifikat.

### Vanliga frågor

| Fråga | Svar |
|---|---|
| **Är den här processen säker?** | Ja, Adobe Managed är säkrare än vår gamla metod eftersom inget certifikat eller någon privat nyckel ändrar händer utanför Adobe och certifikatutfärdaren. |
| **Hur kan Adobe köpa ett certifikat för vår domän?** | Certifikatet kan bara köpas om du har pekat det angivna värdnamnet (till exempel `smetrics.example.com`) mot ett värdnamn som ägs av Adobe. Detta innebär att värdnamnet delegeras till Adobe och att Adobe kan köpa certifikatet för din räkning. |
| **Kan jag begära att certifikatet återkallas?** | Ja, som ägare av domänen har du rätt att begära att certifikatet återkallas. Du behöver bara öppna en biljett hos Kundtjänst för att få detta färdigt. |
| **Använder det här certifikatet SHA-2-kryptering?** | Ja, Adobe kommer att arbeta med DigiCert för att utfärda ett SHA-2-certifikat. |
| **Kostar detta något?** | Nej, Adobe erbjuder den här tjänsten till alla nuvarande Adobe-kunder med digitala upplevelser utan extra kostnad. |

## Skapa CNAME-poster

Organisationens nätverksteam bör konfigurera dina DNS-servrar genom att skapa nya CNAME-poster. Varje värdnamn vidarebefordrar data till Adobe datainsamlingsservrar.

FPC-specialisten ger dig konfigurerade värdnamn och vilka CNAME som de ska peka på. Exempel:

* **SSL-värdnamn**:`smetrics.mysite.com`
* **SSL CNAME**:`mysite.com.ssl.sc.omtrdc.net`
* **Värdnamn** som inte är SSL:`metrics.mysite.com`
* **CNAME** som inte är SSL:`mysite.com.sc.omtrdc.net`

Så länge implementeringskoden inte ändras kommer det här steget inte att påverka datainsamlingen och kan utföras när som helst efter att implementeringskoden har uppdaterats.

>[!NOTE]
>
>Experience Cloud Visitor ID-tjänsten är ett alternativ till att konfigurera en CNAME för att aktivera cookies från första part, men på grund av de senaste ändringarna i Apple ITP rekommenderar vi fortfarande att du allokerar en CNAME även när du använder tjänsten Experience Cloud ID.

## Verifiera vidarebefordran av värdnamn {#validate}

Följande metoder är tillgängliga för validering:

### Validera med en webbläsare

Om du har konfigurerat en CNAME och har installerat certifikatet kan du använda webbläsaren för validering:

`https://sstats.adobe.com/_check`

>[!NOTE]
>
>En säkerhetsvarning visas om inget certifikat är installerat.

### Validera med [!DNL curl]

Adobe rekommenderar att du använder [[!DNL curl]](https://curl.haxx.se/) från kommandoraden. ([!DNL Windows] användare kan installera [!DNL curl] från: <https://curl.haxx.se/windows/>)

Om du har en CNAME men inget certifikat är installerat kör du:
`curl -k https://sstats.adobe.com/_check`
Svar: `SUCCESS`

(Värdet `-k` inaktiverar säkerhetsvarningen.)

Om du har konfigurerat en CNAME och certifikatet är installerat kör du:
`curl https://sstats.adobe.com/_check`
Svar: `SUCCESS`

### Validera med [!DNL nslookup]

Du kan använda `nslookup` för validering. Öppna en kommandotolk `sstats.adobe.com`och skriv in `nslookup sstats.adobe.com`

Om allt är klart att konfigureras visas en retur som liknar:

```
nslookup sstats.adobe.com
Server:             10.30.7.247
Address:     10.30.7.247#53

sstats.adobe.com    canonical name = adobe.com.ssl.d1.sc.omtrdc.net.
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.218.180.161
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 52.39.8.230
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.187.216.46
```

## Uppdatera implementeringskod {#update}

Innan du redigerar kod på webbplatsen för att använda cookies från första part måste du uppfylla följande krav:

* Begär ett SSL-certifikat genom att följa stegen som beskrivs ovan i avsnittet *Implementera* i [Adobe Managed Certificate Program](#adobe-managed-certificate-program).
* Skapa CNAME-poster (se ovan).
* Validera värdnamnet (se ovan).

När du har verifierat att dina värdnamn svarar och vidarebefordrar till datainsamlingsservrar i Adobe kan du ändra implementeringen så att den pekar på dina egna värdnamn för datainsamling.

1. Öppna JavaScript-huvudfilen (`s_code.js/AppMeasurement.js`).
1. Om du vill uppdatera kodversionen ersätter du hela `s_code.js/AppMeasurement.js` filen med den nyare versionen och ersätter eventuella plugin-program eller anpassningar. **Eller** om du vill uppdatera koden som bara är relevant för cookies från första part ska du leta reda på variablerna s.trackingServer och s.trackingServerSecure (om du använder SSL) och peka dem mot dina nya värdnamn för datainsamling. Använda mysite.com som exempel:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. Överför den uppdaterade JavaScript-huvudfilen till din webbplats.

1. Om du går över till cookies från en långvarig implementering, eller byter till ett annat värdnamn för en egen samling, rekommenderar vi att du migrerar besökare från den tidigare domänen till den nya domänen.

Se [Besöksmigrering](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html) i Analytics-implementeringshandboken.

När du har överfört JavaScript-filen konfigureras allt för insamling av cookie-data från första part. Vi rekommenderar att ni övervakar Analytics-rapporter under de kommande timmarna för att säkerställa att datainsamlingen fortsätter som vanligt. Om så inte är fallet kontrollerar du att alla ovanstående steg har slutförts och att någon av de användare i organisationen som stöds kontaktar Kundtjänst.
