---
description: Läs om hur Adobe Target använder cookies för att ge webbplatsoperatörer möjlighet att testa vilket onlineinnehåll och vilka erbjudanden som är mer relevanta för besökarna.
solution: Target
title: Adobe Target Cookies
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: 9ee4d9b0e670dec35cda530892c49e36bf7cc107
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Adobe Target cookies

Adobe Target använder cookies för att ge webbplatsoperatörerna möjlighet att testa vilket onlineinnehåll och vilka erbjudanden som är mer relevanta för besökarna.

>[!NOTE]
>
>Informationen i den här artikeln gäller endast för [Adobe Target JavaScript-bibliotek](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} (`at.js`). Se [Adobe Experience Platform Web SDK-cookies](web-sdk.md) om du vill ha information om Target-implementeringar med Web SDK.
>
>Du kan ändra inställningarna som beskrivs i den här artikeln om det behövs, förutom cookie-varaktighet. [Kontakta din kontorepresentant](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank} när du ändrar cookie-inställningar.

## cookies från första part

Följande cookies från första part lagras på kundens domän:

| Cookie | Information |
| --- | --- |
| `mbox` | Lagrar anonyma identifierare om besökaren.<P>**Cookie-domän**: Domänen som du använder mbox från. Eftersom den här cookien betjänas från ditt företags domän är cookien en cookie från första part. Om något av dina domännamn innehåller en landskod, till exempel `example.co.uk`, arbeta med klienttjänster för att konfigurera `at.js` för att stödja den här koden. Mer information om hur du anpassar cookie-domänen finns i `cookieDomain` under [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} i Adobe Target utvecklarguide.<P>**Serverdomän**: `clientcode.tt.omtrdc.net`, med klientkoden för ditt Adobe Target-konto.<P>**Cookie-varaktighet**: Cookien finns kvar i besökarens webbläsare två år efter den senaste inloggningen. Du kan inte ändra varaktighet för cookie-filen.<P>Cookien har vissa värden för att hantera besökarnas upplevelse [!DNL Target] verksamhet:<P>**sessions-ID**: En unik identifierare för en given användarsession. Som standard går sessionen ut efter 30 minuters inaktivitet. Om du genererar `sessionId` själv (till exempel [implementeringar på serversidan](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}), se till att<ul><li>Sessions-ID kan vara vilken utskrivbar sträng som helst, förutom blanksteg, frågetecken ( ? ) eller ett snedstreck ( / ).</li><li>Sessions-ID:t ska vara mellan 1 och 128 tecken långt.</li><li>För en viss session måste cookie-filens värde vara detsamma för flera begäranden.</li><li>Du bör aldrig ha parallella sessioner (distinkta `sessionIds`) för en viss besökare när som helst.</li></ul>Routning till en viss nod i edge-klustret görs med sessions-ID.<ul><li>Sessionen är aktiv i 30 minuter på serversidan. Därför bör du inte använda ett annat sessions-ID för ett visst `tntId/thirdPartyId` inom 30 minuter från den senaste begäran som gjorts med `tntId/thirdPartyId`. Annars kan ändringar i profilen vara inkonsekventa och oförutsägbara.</li><li>Ett nytt sessions-ID måste användas efter trettio minuters inaktivitet från en besökare.</li><li>Använda samma sessions-ID med flera `tntIds/thirdPartyIds` kan orsaka oförutsägbara ändringar i de profiler som identifieras av `tntId/thirdPartyIDs`.</li></ul>Obs! Se [gräns för antal samtidiga begäranden](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html#content-delivery){target=_blank} för ett visst sessions-ID.<P>**pc-ID**: Ett halvpermanent ID för en besökares webbläsare. Varar tills cookies tas bort manuellt.<P>**check**: Ett enkelt testvärde som används för att avgöra om en besökare stöder cookies. Ange varje gång en besökare begär en sida.<P>**disable**: Ange om inläsningstiden för en besökare överskrider den timeout som har konfigurerats i filen at.js. Som standard varar den här tidsgränsen en timme. |
| `at_check` | Tillfällig cookie för att kontrollera om läs-/skrivfunktionen för cookies är aktiverad i webbläsaren. |
| `mboxEdgeCluster` | Den här cookies finns bara när/om [overrideMboxEdgeServer-inställning](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} är inställd på `true`. |

Det går inte att använda `HTTPOnly` på dessa cookies från första part. The `at.js` JavaScript-biblioteket måste läsa/skriva till dessa cookies. Dessa cookies skapas av `at.js` och anges inte från servern.

The `secure` kan aktiveras för alla dessa cookies med `secureOnly: true` konfiguration i `at.js`.

## cookies från tredje part

Adobe Target-användare kan skapa anpassade cookies från tredje part. Följande cookies från tredje part lagras på `tt.omtrdc.net`:

| Cookie | Information |
| --- | --- |
| `customerclientcode!mboxPC` | Finns om korsdomän är aktiverad. |
| `customerclientcode!mboxSession` | Finns om korsdomän är aktiverad. |

Dessa cookies från tredje part är endast tillgängliga för HTTPO och anges av Adobe Target datainsamlingsservrar.

The `secure` inställningen kan aktiveras för alla cookies med `secureOnly: true` konfiguration i `at.js`.
