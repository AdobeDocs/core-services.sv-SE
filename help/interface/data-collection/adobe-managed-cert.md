---
description: Lär dig hur du ställer in säkra certifikat för användning med Adobe Experience Cloud cookies från första part.
solution: Experience Cloud,Analytics
title: Certifikatprogram som hanteras av Adobe
index: y
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 028b11dfbcfc0c5c9f6fd1c69350574f81f2846b
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# Certifikatprogram som hanteras av Adobe

Det Adobe-hanterade certifikatprogrammet är den rekommenderade processen för att skapa förstapartscertifikat som behövs för en CNAME-implementering. Programmet är helt automatiserat när det har konfigurerats. Certifikaten förnyas i tid så att datainsamlingen inte påverkas på grund av utgångna certifikat. Programmet är kostnadsfritt för dina första 100 CNAME.

Om du för närvarande hanterar dina egna certifikat ansvarar du för att köpa, underhålla och tillhandahålla ett certifikat till Adobe för cookie-användning från första part. Du kan kontakta Adobe kundtjänst för att diskutera övergången till det Adobe-hanterade certifikatprogrammet.

## Implementering

Följ de här stegen för att implementera ett nytt certifikat för datainsamling från första part:

1. Hämta och fyll i formuläret [Förstpartsdomänbegäran](cookies/assets/First_Party_Domain_Request_Form.xlsx)

1. Öppna en biljett där Adobe kundtjänst ber om att få ställa in insamling av förstahandsdata för det Adobe-hanterade certifikatprogrammet.

1. När du fått biljetten får du en CNAME-post från Adobe:s representant. Dessa poster måste konfigureras på företagets DNS-server innan Adobe kan köpa certifikatet åt dig. Värdnamnet `data.example.com` pekar till exempel på `hiodsibxvip01.data.adobedc.net`.

1. När CNAME-posten finns på organisationens servrar arbetar Adobe med DigiCert för att köpa och installera ett certifikat på Adobe datainsamlingsservrar.

## Verifiera vidarebefordran av värdnamn {#validate}

När Adobe har installerat certifikatet kan du använda någon av följande metoder för att validera att det fungerar.

+++**Validering av webbläsare**

Du kan använda vilken webbläsare som helst för att validera att ett certifikat är korrekt installerat. Skriv CNAME med `_check` som sökväg i adressfältet. Exempel:

`data.example.com/_check`

Om allt fungerar visas `SUCCESS` i webbläsaren. Om certifikatet inte är korrekt installerat får du en säkerhetsvarning.

+++

+++**Kommandorad (`curl`)**

De flesta moderna operativsystem har redan [`curl`](https://curl.se) installerat.

Skriv följande på kommandoraden:

```sh
curl data.example.com/_check
```

Om allt fungerar korrekt returnerar konsolen `SUCCESS`.

>[!TIP]
>
>Du kan använda flaggan `-k` för att inaktivera säkerhetsvarningen för att hjälpa till med felsökningen.

+++

+++**Kommandorad (`nslookup`)**

Skriv följande på kommandoraden:

```sh
nslookup data.example.com
```

Om allt fungerar som det ska returneras Adobe datainsamlingsservrar:

```text
Server: hiodsibxvip01.corp.adobe.com
Address: 10.50.112.247

Name: example.com.ssl.d1.sc.omtrdc.net
Addresses: 63.140.37.126
    63.140.37.206
    63.140.36.51
    63.140.36.145
Aliases: smetrics.example.com
```

+++

## Uppdatera implementeringskod {#update}

När du har verifierat att ditt certifikat fungerar som det ska kan du uppdatera din Adobe-implementering så att dessa värden används.

* Uppdatera konfigurationsvariabeln [`trackingServer`](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/config-vars/trackingserver) för implementeringar av Adobe Analytics AppMeasurement. Om du har en befintlig implementering kan du läsa [Besöksmigrering](https://experienceleague.adobe.com/en/docs/analytics/technotes/visitor-migration) för ytterligare steg om hur du förhindrar att befintliga besökare räknas som nya besökare.
* Uppdatera egenskapen [`edgeDomain`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/edgedomain) i kommandot [`configure`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) för Web SDK-implementeringar.

## Underhåll och förnyelser

Trettio dagar innan ditt förstapartscertifikat upphör att gälla validerar Adobe om CNAME fortfarande är giltigt och används. I så fall antar Adobe att du vill fortsätta använda tjänsten och förnyar automatiskt certifikatet åt dig.

>[!IMPORTANT]
>
>Om din organisations CNAME-post tas bort eller inte längre mappas till det säkra värdnamnet för Adobe kan Adobe inte förnya certifikatet. Posten i Adobe är markerad för borttagning utan ytterligare kommunikation.

## Vanliga frågor och svar

+++Är den här processen säker?

Ja. Certifikatprogrammet som hanteras av Adobe är säkrare än den organisation som förser Adobe med ett certifikat. Inget certifikat eller någon privat nyckel ändrar händer utanför Adobe och certifikatutfärdaren.

+++

+++Hur kan Adobe köpa ett certifikat för vår domän?

Certifikatet kan bara köpas när du har angett ett värdnamn som tillhör Adobe. Du delegerar i princip det här värdnamnet till Adobe och tillåter Adobe att köpa certifikatet för din räkning.

+++

+++Kan jag begära att certifikatet återkallas?

Ja. Som ägare av domänen har du rätt att begära att certifikatet återkallas. Kontakta Adobe kundtjänst för att starta processen.

+++

+++Vilken krypteringstyp används?

Adobe samarbetar med DigiCert för att utfärda ett SHA-2-certifikat.

+++

+++Kostar det här programmet ytterligare?

Nej. Adobe erbjuder denna tjänst till alla Adobe Experience Cloud-kunder utan extra kostnad.

+++

+++Vilka chiffreringssäkerhetsnivåer erbjuder Adobe?

Adobe erbjuder två krypteringsnivåer för att uppfylla olika kundbehov när det gäller säkerhet vid datainsamling från första part. Dessa nivåer avgör vilka krypteringsalgoritmer som stöds för HTTPS-anslutningar med Adobe-servrar. Adobe granskar och uppdaterar regelbundet de algoritmer som stöds baserat på nuvarande säkerhetspraxis. Kontakta kundtjänst om du vill ändra säkerhetsinställningarna för chiffrering.

* **Standard** kräver TLS 1.2 eller senare och minst 128-bitars kryptering. Den är utformad för att ge största möjliga enhetskompatibilitet samtidigt som den bevarar säker kryptering.
* **Hög** krypteringssäkerhet kräver TLS 1.2 eller senare och tar bort stöd för svagare chiffer. Den är utformad för kunder som vill ha den starkaste krypteringen och inte bryr sig om stöd för äldre enheter.

Följande klienter är kända för att inte kunna ansluta med krypteringssäkerhet inställd på **Hög**:

* Windows 8.1 och tidigare (senast uppdaterat 2018)
* Windows Phone 8.1 och tidigare (senast uppdaterad 2016)
* OS X 10.10 och tidigare (senast uppdaterat 2017)
* iOS 8.4 och tidigare (senast uppdaterad 2015)

+++

+++Vilka HTTPS-certifikattyper stöds?

Adobe stöder både RSA- och ECC-certifikattyper för att uppfylla olika kundbehov. RSA-certifikat stöds i större utsträckning för klienter, men ECC-certifikat använder mindre bearbetning både på server- och klientsidan. För certifikat som hanteras av Adobe tillhandahålls både RSA och ECC. För kundhanterade certifikat krävs RSA och ECC rekommenderas. Moderna klienter har stöd för både RSA och ECC. Följande klienter har vanligtvis bara stöd för RSA-certifikat:

* Windows Vista och tidigare (senast uppdaterat 2012)
* Windows Phone 8.0 och tidigare (senast uppdaterad 2014)
* OS X 10.8 och tidigare (senast uppdaterat 2013)
* iOS 5.1 och tidigare (senast uppdaterad 2012)
* Android 4.3 och tidigare (senast uppdaterad 2013)

+++
