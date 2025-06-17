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
source-git-commit: 0a60e253d84fd45cd929ce70406af354df927f7f
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# Adobe Target cookies

Adobe Target använder cookies för att ge webbplatsoperatörerna möjlighet att testa vilket onlineinnehåll och vilka erbjudanden som är mer relevanta för besökarna.

>[!NOTE]
>
>Informationen i den här artikeln gäller endast för [Adobe Target JavaScript-biblioteket](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} (`at.js`). Mer information om målimplementeringar med hjälp av Web SDK finns i [Adobe Experience Platform Web SDK-cookies](web-sdk.md).
>
>Du kan ändra inställningarna som beskrivs i den här artikeln om det behövs, förutom cookie-varaktighet. [Kontakta din kontorepresentant](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank} när du ändrar cookie-inställningar.

## cookies från första part

Följande cookies från första part lagras på kundens domän:

| Cookie | Information |
| --- | --- |
| `mbox` | Lagrar anonyma identifierare om besökaren.<P>**Cookie-domän**: Domänen som du betjänar mbox från. Eftersom den här cookien betjänas från ditt företags domän är cookien en cookie från första part. Om något av dina domännamn innehåller en landskod, t.ex. `example.co.uk`, kan du tillsammans med klienttjänster konfigurera `at.js` så att koden stöds. Mer information om hur du anpassar cookie-domänen finns i `cookieDomain` under [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} i utvecklarhandboken för Adobe Target.<P>**Serverdomän**: `clientcode.tt.omtrdc.net`, använder klientkoden för ditt Adobe Target-konto.<P>**Cookie-varaktighet**: Cookien finns kvar i besökarens webbläsare två år efter den senaste inloggningen. Du kan inte ändra varaktighet för cookie-filen.<P>Cookien innehåller vissa värden för att hantera hur besökarna upplever [!DNL Target]-aktiviteter:<P>**sessions-ID**: En unik identifierare för en given användarsession. Som standard går sessionen ut efter 30 minuters inaktivitet. Om du genererar `sessionId` själv (till exempel för [implementeringar på serversidan](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}) måste du se till följande:<ul><li>Sessions-ID kan vara vilken utskrivbar sträng som helst, förutom blanksteg, frågetecken ( ? ), klammerparenteser ( { } ) eller ett snedstreck ( / ). Det ska vara mellan 1 och 128 tecken långt.</li><li>Sessions-ID:t ska vara mellan 1 och 128 tecken långt.</li><li>För en viss session måste cookie-filens värde vara detsamma för flera begäranden.</li><li>Du bör aldrig ha parallella sessioner (distinkta `sessionIds`) för en viss besökare vid något tillfälle.</li></ul>Routning till en viss nod i edge-klustret görs med sessions-ID.<ul><li>Sessionen är aktiv i 30 minuter på serversidan. Du bör därför inte använda ett annat sessions-ID för en viss `tntId/thirdPartyId` inom 30 minuter från den senaste begäran som gjordes med `tntId/thirdPartyId`. Annars kan ändringar i profilen vara inkonsekventa och oförutsägbara.</li><li>Ett nytt sessions-ID måste användas efter trettio minuters inaktivitet från en besökare.</li><li>Om du använder samma sessions-ID med flera `tntIds/thirdPartyIds` kan det medföra oförutsägbara ändringar i profilerna som identifieras av `tntId/thirdPartyIDs`.</li></ul>OBS! Se [gräns för antal samtidiga begäranden](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html#content-delivery){target=_blank} för ett givet sessions-ID.<P>**pc-ID**: Ett halvpermanent ID för en besökares webbläsare. Varar tills cookies tas bort manuellt.<P>**check**: Ett enkelt testvärde används för att avgöra om en besökare stöder cookies. Ange varje gång en besökare begär en sida.<P>**disable**: Ange om inläsningstiden för en besökare överskrider den timeout som har konfigurerats i filen at.js. Som standard varar den här tidsgränsen en timme. |
| `at_check` | Tillfällig cookie för att kontrollera om läs-/skrivfunktionen för cookies är aktiverad i webbläsaren. |
| `mboxEdgeCluster` | Den här cookies finns bara när/om [overrideMboxEdgeServer-inställningen](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} är inställd på `true`. |

Det går inte att använda `HTTPOnly` på dessa cookies från första part. JavaScript-biblioteket `at.js` måste läsa/skriva till dessa cookies. Dessa cookies har skapats av `at.js` och har inte angetts från servern.

Inställningen `secure` kan aktiveras för alla dessa cookies med hjälp av konfigurationen `secureOnly: true` i `at.js`.

## cookies från tredje part

Adobe Target-användare kan skapa anpassade cookies från tredje part. Följande cookies från tredje part lagras på `tt.omtrdc.net`:

| Cookie | Information |
| --- | --- |
| `customerclientcode!mboxPC` | Finns om korsdomän är aktiverad. |
| `customerclientcode!mboxSession` | Finns om korsdomän är aktiverad. |

Dessa cookies från tredje part är endast tillgängliga för HTTPO och anges av Adobe Target datainsamlingsservrar.

Inställningen `secure` kan aktiveras för alla cookies med konfigurationen `secureOnly: true` i `at.js`.
