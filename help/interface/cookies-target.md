---
description: Läs om hur Adobe Target använder cookies för att ge webbplatsoperatörer möjlighet att testa vilket onlineinnehåll och vilka erbjudanden som är mer relevanta för besökarna.
solution: Experience Cloud,Analytics,Target
title: Adobe Target cookies
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: a1d24f95b1ac567686d58af8adf0132e5beb8f2a
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Adobe Target cookies

[!DNL Adobe Target] använder cookies för att ge webbplatsoperatörer möjlighet att testa vilket onlineinnehåll och vilka erbjudanden som är mer relevanta för besökarna.

>[!NOTE]
>
>Informationen i den här artikeln gäller för [[!DNL Target] at.js JavaScript-bibliotek](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} endast.
>
>Mer information om cookies som används i en [!DNL Target] implementering med [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target=_blank}, see "Does the [!DNL Adobe Experience Platform Web SDK] use cookies? If so, what cookies does it use?" in [Frequently Asked questions in the DNL Platform Web SDK overview guide](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html){target=_blank}.
>
>Du kan ändra inställningarna som beskrivs i den här artikeln om det behövs, förutom cookie-varaktighet. [Kontakta din kontorepresentant](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank} när du ändrar cookie-inställningar.
>
>[!DNL Target] -användare kan också skapa anpassade cookies från tredje part.

## cookies från första part

Följande cookies från första part lagras på kundens domän:

| Cookie | Information |
| --- | --- |
| mbox | Lagrar anonyma identifierare om besökaren.<P>**Cookie-domän**: Domänen som du använder mbox från. Eftersom den här cookien betjänas från ditt företags domän är cookien en cookie från första part. Exempel: `mycompany.com`. Om något av dina domännamn innehåller en landskod, till exempel `mycompany.co.uk`arbetar du med klienttjänsterna för att konfigurera at.js så att koden kan hanteras. Mer information om hur du anpassar cookie-domänen finns i &quot;`cookieDomain`&quot; under [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} i *[!DNL Adobe Target]Utvecklarhandbok*.<P>**Serverdomän**: `clientcode.tt.omtrdc.net`, med hjälp av klientkoden för [!DNL Target] konto.<P>**Cookie-varaktighet**: Cookien finns kvar i besökarens webbläsare två år efter den senaste inloggningen. Du kan inte ändra varaktighet för cookie-filen.<P>Cookien har vissa värden för att hantera besökarnas upplevelse [!DNL Target] verksamhet:<P>**sessions-ID**: En unik identifierare för en given användarsession. Som standard går sessionen ut efter 30 minuters inaktivitet. Om du genererar `sessionId` själv (till exempel [implementeringar på serversidan](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}), se till att<ul><li>Sessions-ID kan vara vilken utskrivbar sträng som helst förutom blanksteg, frågetecken ( ? ) eller ett snedstreck ( / ).</li><li>Sessions-ID:t ska vara mellan 1 och 128 tecken långt.</li><li>För en viss session måste cookie-filens värde vara detsamma för flera begäranden.</li><li>Du bör aldrig ha parallella sessioner (distinkta `sessionIds`) för en viss besökare när som helst.</li></ul>Routning till en viss nod i edge-klustret görs med sessions-ID.<ul><li>Sessionen är aktiv i 30 minuter på serversidan. Därför bör du inte använda ett annat sessions-ID för ett visst `tntId/thirdPartyId` inom 30 minuter från den senaste begäran som gjorts med `tntId/thirdPartyId`. Annars kan ändringar i profilen vara inkonsekventa och oförutsägbara.</li><li>Ett nytt sessions-ID måste användas efter trettio minuters inaktivitet från en besökare.</li><li>Använda samma sessions-ID med flera `tntIds/thirdPartyIds` kan orsaka oförutsägbara ändringar i de profiler som identifieras av `tntId/thirdPartyIDs`.</li></ul>OBS! Se [gräns för antal samtidiga begäranden](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=en#content-delivery){target=_blank} för ett visst sessions-ID.<P>**pc-ID**: Ett halvpermanent ID för en besökares webbläsare. Varar tills cookies tas bort manuellt.<P>**check**: Ett enkelt testvärde som används för att avgöra om en besökare stöder cookies. Ange varje gång en besökare begär en sida.<P>**disable**: Ange om inläsningstiden för en besökare överskrider den timeout som har konfigurerats i filen at.js. Som standard varar den här tidsgränsen en timme. |
| at_check | Tillfällig cookie för att kontrollera om läs-/skrivfunktionen för cookies är aktiverad i webbläsaren. |
| mboxEdgeCluster | Den här cookies finns bara när/om [overrideMboxEdgeServer-inställning](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} är inställd på `true`. |

Det går inte att använda enbart HTTPO på dessa cookies från första part. JavaScript-biblioteket at.js måste läsa/skriva till dessa cookies. Dessa cookies skapas av at.js och ställs inte in från servern.

The `secure` kan aktiveras för alla dessa cookies med `secureOnly: true` konfiguration i implementeringen av at.js.

## cookies från tredje part

Följande cookies från tredje part lagras på `tt.omtrdc.net`:

| Cookie | Information |
| --- | --- |
| customerclientcode!mboxPC | Denna cookie finns om korsdomän är aktiverad. |
| customerclientcode!mboxSession | Denna cookie finns om korsdomän är aktiverad. |

Dessa cookies från tredje part är endast HTTPO-utdata och anges av [!DNL Target] edge-servrar.

The `secure` inställningen kan aktiveras för alla cookies med `secureOnly: true` konfiguration i implementeringen av at.js.