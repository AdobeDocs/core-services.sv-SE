---
description: Lär dig hur  [!DNL Adobe Target] använder cookies för att ge webbplatsoperatörer möjlighet att testa vilket onlineinnehåll och vilka erbjudanden som är mer relevanta för besökarna.
solution: Experience Cloud,Analytics,Target
title: Adobe Target cookies
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: 3ca021a0a2e6b0b6e265d35084d89d7720c28908
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# Adobe Target cookies

[!DNL Adobe Target] använder cookies för att ge webbplatsoperatörer möjlighet att testa vilket onlineinnehåll och vilka erbjudanden som är mer relevanta för besökarna.

>[!NOTE]
>
>Informationen i den här artikeln gäller endast för JavaScript-biblioteket [[!DNL Target] at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}.
>
>Mer information om cookies som används i en [!DNL Target]-implementering med [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target=_blank} finns i&quot;Använder [!DNL Adobe Experience Platform Web SDK] cookies? Om så är fallet, vilka cookies använder den?&quot; i [[!DNL Vanliga frågor och svar i översiktsguiden för Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html){target=_blank}.
>
>Du kan ändra inställningarna som beskrivs i den här artikeln om det behövs, förutom cookie-varaktighet. [Kontakta din kontorepresentant](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank} när du ändrar cookie-inställningar.
>
>[!DNL Target] användare kan också skapa anpassade cookies från tredje part.

## cookies från första part

Följande cookies från första part lagras på kundens domän:

| Cookie | Information |
| --- | --- |
| mbox | Lagrar anonyma identifierare om besökaren.<P>**Cookie-domän**: Domänen som du betjänar mbox från. Eftersom den här cookien betjänas från ditt företags domän är cookien en cookie från första part. Exempel: `mycompany.com`. Om något av dina domännamn innehåller en landskod, t.ex. `mycompany.co.uk`, bör du tillsammans med klienttjänsterna konfigurera at.js så att koden stöds. Om du vill ha mer information om hur du anpassar cookie-domänen kan du läsa `cookieDomain` under [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} i *[!DNL Adobe Target]Utvecklarhandbok*.<P>**Serverdomän**: `clientcode.tt.omtrdc.net`, använder klientkoden för ditt [!DNL Target]-konto.<P>**Cookie-varaktighet**: Cookien finns kvar i besökarens webbläsare två år efter den senaste inloggningen. Du kan inte ändra varaktighet för cookie-filen.<P>Cookien innehåller vissa värden för att hantera hur besökarna upplever [!DNL Target]-aktiviteter:<P>**sessions-ID**: En unik identifierare för en given användarsession. Som standard går sessionen ut efter 30 minuters inaktivitet. Om du genererar `sessionId` själv (till exempel för [implementeringar på serversidan](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}) måste du se till följande:<ul><li>Sessions-ID kan vara vilken utskrivbar sträng som helst, förutom blanksteg, frågetecken ( ? ), klammerparenteser ( { } ) eller ett snedstreck ( / ).</li><li>Sessions-ID:t ska vara mellan 1 och 128 tecken långt.</li><li>För en viss session måste cookie-filens värde vara detsamma för flera begäranden.</li><li>Du bör aldrig ha parallella sessioner (distinkta `sessionIds`) för en viss besökare vid något tillfälle.</li></ul>Routning till en viss nod i edge-klustret görs med sessions-ID.<ul><li>Sessionen är aktiv i 30 minuter på serversidan. Du bör därför inte använda ett annat sessions-ID för en viss `tntId/thirdPartyId` inom 30 minuter från den senaste begäran som gjordes med `tntId/thirdPartyId`. Annars kan ändringar i profilen vara inkonsekventa och oförutsägbara.</li><li>Ett nytt sessions-ID måste användas efter trettio minuters inaktivitet från en besökare.</li><li>Om du använder samma sessions-ID med flera `tntIds/thirdPartyIds` kan det medföra oförutsägbara ändringar i profilerna som identifieras av `tntId/thirdPartyIDs`.</li></ul>OBS! Se [gräns för antal samtidiga begäranden](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=en#content-delivery){target=_blank} för ett givet sessions-ID.<P>**pc-ID**: Ett halvpermanent ID för en besökares webbläsare. Varar tills cookies tas bort manuellt.<P>**check**: Ett enkelt testvärde används för att avgöra om en besökare stöder cookies. Ange varje gång en besökare begär en sida.<P>**disable**: Ange om inläsningstiden för en besökare överskrider den timeout som har konfigurerats i filen at.js. Som standard varar den här tidsgränsen en timme. |
| at_check | Tillfällig cookie för att kontrollera om läs-/skrivfunktionen för cookies är aktiverad i webbläsaren. |
| mboxEdgeCluster | Den här cookies finns bara när/om [overrideMboxEdgeServer-inställningen](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} är inställd på `true`. |

Det går inte att använda enbart HTTPO på dessa cookies från första part. JavaScript-biblioteket at.js behöver läsa/skriva till dessa cookies. Dessa cookies skapas av at.js och ställs inte in från servern.

Inställningen `secure` kan aktiveras för alla dessa cookies med konfigurationen `secureOnly: true` i implementeringen av at.js.

## cookies från tredje part

Följande cookies från tredje part lagras på `tt.omtrdc.net`:

| Cookie | Information |
| --- | --- |
| customerclientcode!mboxPC | Denna cookie finns om korsdomän är aktiverad. |
| customerclientcode!mboxSession | Denna cookie finns om korsdomän är aktiverad. |

Dessa cookies från tredje part är endast HTTPO från lådan och anges av edge-servrarna [!DNL Target].

Inställningen `secure` kan aktiveras för alla cookies med konfigurationen `secureOnly: true` i implementeringen av at.js.