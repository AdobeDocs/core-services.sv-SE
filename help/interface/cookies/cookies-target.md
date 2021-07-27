---
description: Läs om hur Adobe Target använder cookies för att ge webbplatsoperatörer möjlighet att testa vilket onlineinnehåll och vilka erbjudanden som är mer relevanta för besökarna.
keywords: cookies;sekretess
solution: Experience Cloud,Analytics,Target,Social
title: 'Adobe Target Cookies '
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administrering
role: Administrator
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: a244ee8927e0417fbb502e8eaa3c371151ec3044
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 1%

---

# Adobe Target Cookies{#target-cookies}

Adobe Target använder cookies för att ge webbplatsoperatörerna möjlighet att testa vilket onlineinnehåll och vilka erbjudanden som är mer relevanta för besökarna.

Du kan ändra de här inställningarna om det behövs, förutom för cookie-varaktighet. Kontakta din kontorepresentant när du ändrar cookie-inställningarna.

>[!NOTE]
>
>Adobe Target-användare kan också skapa anpassade cookies från tredje part.

| Inställning | Information |
| --- | --- |
| Cookie-namn | mbox. |
| Cookie-domän | Den andra och övre nivån i de domäner som du använder mbox från. Eftersom cookie används av ditt företags domän är den en cookie från första part. Exempel: `mycompany.com`. |
| Serverdomän | `clientcode.tt.omtrdc.net`, med hjälp av klientkoden för ditt  [!DNL Adobe Target] konto. |
| Cookie-varaktighet | Cookien finns kvar i besökarens webbläsare två år efter hans eller hennes senaste inloggning. Du kan inte ändra varaktighet för cookie-filen. |



>[!NOTE]
>
>Om något av dina domännamn innehåller en landskod, t.ex. `mycompany.co.uk`, kan du tillsammans med dina klienttjänster konfigurera [!DNL at.js] så att de stöder detta.

Denna cookie har ett antal värden för att hantera hur besökarna upplever Adobe Target kampanjer:

| Värde | Definition |
| --- | --- |
| sessions-ID | En unik identifierare för en given användarsession. Som standard går sessionen ut efter 30 minuters inaktivitet. Om du genererar sessionId själv (till exempel för implementeringar på serversidan) ska du kontrollera följande:<ul><li>Sessions-ID kan vara vilken utskrivbar sträng som helst förutom blanksteg, frågetecken ( ? ) eller ett snedstreck ( / ).</li><li>* Sessions-ID:t måste vara mellan 1 och 128 tecken långt.</li><li>För en viss session måste dess värde vara detsamma för flera begäranden</li><li>Du bör aldrig ha parallella sessioner (distinkta sessions-ID) för en viss besökare vid något tillfälle.</li></ul>Routning till en viss nod i edge-klustret görs med sessions-ID.<ul><li>Sessionen är aktiv i 30 minuter på serversidan. Du bör därför inte använda ett annat sessions-ID för en viss `tntId/thirdPartyId` inom 30 minuter från den senaste begäran som gjordes med `tntId/thirdPartyId`. Annars kan ändringar i profilen vara inkonsekventa och oförutsägbara.</li><li>Om du använder samma sessions-ID med flera `tntIds/thirdPartyIds` kan det medföra oförutsägbara ändringar i profilerna som identifieras av `tntId/thirdPartyIDs`.</li></ul>**Obs**: Se  [begränsning av antalet samtidiga ](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=en#content-delivery) begäranden för ett givet sessions-ID. |
| pc-ID | Ett halvpermanent ID för en besökares webbläsare. Varar tills cookies tas bort manuellt. |
| check | Ett enkelt testvärde som används för att avgöra om en besökare stöder cookies. Ange varje gång en besökare begär en sida. |
| disable | Ange om besökarens inläsningstid överskrider den timeout som har konfigurerats i filen at.js. Som standard varar detta 1 timme. |

