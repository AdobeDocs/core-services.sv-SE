---
description: Lär dig mer om centrala gränssnittskomponenter för Experience Cloud. I den här hjälpen ingår användar- och produktadministration i Admin Console, aktivering av program för Experience Cloud-tjänster samt hjälp om Audience Library, Customer Attributes, Experience Cloud Assets med flera.
solution: Experience Cloud
title: Hjälp och dokumentation för Experience Cloud-gränssnittet
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: '"Kundattribut"'
topic: Administrering
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: 4534f764ea821576c3ac5cd1959d387a3689e837
workflow-type: tm+mt
source-wordcount: '1273'
ht-degree: 2%

---

# Handbok för gränssnittskomponenter i Experience Cloud Central

[Experience ](https://experience.adobe.com) Cloudis Adobe integrerade en serie program, produkter och tjänster för digital marknadsföring. Från det intuitiva gränssnittet får du snabbt tillgång till dina molnprogram, produktfunktioner och tjänster.

![Experience Cloud](assets/landing.png)

Från Experience Cloud kan du:

* Få tillgång till dina program och tjänster
* Sök efter produktdokumentation, självstudiekurser och communityinlägg
* Sök efter affärsobjekt globalt med hjälp av en global sökning (endast Experience Platform)
* Hantera dina kontoinställningar (aviseringar, aviseringar och prenumerationer)

## Logga in på Experience Cloud {#signin}

Logga in och verifiera att du är i rätt [organisation](organizations.md).

1. Navigera till [Adobe Experience Cloud](https://experience.adobe.com).
1. Välj **[!UICONTROL Sign in with an Adobe ID]**.
1. Kontrollera att du är i rätt organisation.

   ![](assets/organizations-menu.png)

   **Verifiera din organisation**

   Verifiera att du har loggat in på rätt [organisation](organizations.md) genom att klicka på din profilavatar för att visa organisationsnamnet. Om du har tillgång till mer än en organisation kan du även visa och växla till en annan organisation direkt i sidhuvudsfältet.

   Om din organisation använder Federated ID:n kan du med Experience Cloud logga in med din organisations inloggning utan att behöva ange din e-postadress och ditt lösenord. Om du vill göra det lägger du till `#/sso:@domain` i Experience Cloud-URL:en (`https://experience.adobe.com`).

   För en organisation med Federated ID och domänen `adobecustomer.com` anger du URL-länken till `https://experience.adobe.com/#/sso:@adobecustomer.com`. Du kan också gå direkt till ett specifikt program genom att skapa ett bokmärke för den här URL:en, som bifogas med programsökvägen. (För Adobe Analytics t.ex. `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.)

## Använd Experience Cloud {#navigation}

När du har loggat in på Experience Cloud kan du snabbt komma åt alla program, tjänster och organisationer från det enhetliga huvudet.

Gå till programväljaren ![](assets/menu-icon.png) för att få åtkomst till Experience Cloud-program och -tjänster som har etablerats för dig inom din organisation.

![](assets/platform-core-services.png)

## Stöd för webbläsare i Experience Cloud {#browser}

För bästa prestanda är Experience Cloud optimerat för de vanligaste webbläsarna, inklusive den senaste versionen, plus de två tidigare.

* Krom
* Edge
* Firefox
* Opera
* Safari

Om webbläsaren inte finns med i listan kanske den fortfarande stöds, men du bör använda en av webbläsarna i listan.

>[!NOTE]
>
>Alla program som körs på Experience Cloud har inte stöd för alla webbläsare. Om du är osäker läser du dokumentationen för ett specifikt program.

## Språkstöd i Experience Cloud {#languages}

Experience Cloud har stöd för de språk som varje användare föredrar, enligt inställningarna för ditt Adobe-användarkonto. Språk som stöds är:

* Kinesiska
* Engelska
* Franska
* Tyska
* Italienska
* Japanska
* Koreanska
* Portugisiska
* Spanska
* Taiwanesiska

Alla programteam arbetar för globalt språkstöd, men alla program finns inte på alla språk som anges ovan. Om ditt primära språk inte stöds i ett Experience Cloud-program kan du även ange ett sekundärt språk som standard till när det är tillämpligt. Detta kan du göra i [användarinställningarna för Experience Cloud](https://experience.adobe.com/preferences).

## Få hjälp och support {#support}

Lär dig mer och hjälp med hjälpikonen (![resurs](assets/help-icon.png)) i sidhuvudet, inklusive hjälpinnehåll (dokumentation, självstudiekurser och kurser) på [Experience League](https://experienceleague.adobe.com/#home), samt ytterligare resurser för enskilda program. Du kan även skicka in öppen feedback och skapa prioriterade supportärenden.

![](assets/search-menu.png)

Menyn [!UICONTROL Help] ger dig även åtkomst till:

* **[!UICONTROL Support]:** Skapa en supportanmälan eller kontakta  [!UICONTROL Support] Twitter.
* **[!UICONTROL Feedback]:** Dela feedback om Experience Cloud. Dina synpunkter används för att förbättra Adobe produkter och tjänster.
* **[!UICONTROL Status]:** Navigera till  `https://status.adobe.com/experience_cloud` och kontrollera produktdriftsstatus och  [!UICONTROL Manage Subscriptions].
* **[!UICONTROL Developer Connection]:** Navigera till  `adobe.io` och hitta dokumentation för utvecklare.

## Sök globalt efter objekt och enheter {#search}

Med den globala sökningen kan du söka efter sökbara affärsobjekt eller entiteter på ett smidigt och enhetligt sätt med ett enda klick. Den här sökningen visar de objekt du nyligen har använt.

![](assets/platform-search.png)

>[!NOTE]
>
>Den globala sökningen är inte tillgänglig i alla Experience Cloud-program, men allt eftersom mer innehåll indexeras läggs det till i relevanta program. Tillgänglighet från och med juli 2021:

* Experience Platform
* Journey Optimizer

## Användarprofil och kontoinställningar {#preferences}

Inställningarna för Experience Cloud omfattar meddelanden, prenumerationer och varningar. På kontoinställningsmenyn kan du:

* Ange ett mörkt tema (alla program stöder inte det här temat)
* Sök efter [organisationer](organizations.md)
* Logga ut
* Konfigurera kontoinställningar, meddelanden och prenumerationer

Om du vill hantera inställningar väljer du **[!UICONTROL Preferences]** på din kontomeny ![](assets/preferences-icon-sm.png).

![](assets/preferences-page.png)

På [!UICONTROL Experience Cloud preferences] kan du konfigurera följande funktioner:

| Funktion | Beskrivning |
|--- |--- |
| Standardorganisation[organisation](organizations.md) | Välj den organisation som du vill se när du startar Experience Cloud. |
| [!UICONTROL Subscriptions] | Välj de produkter och kategorier som du vill prenumerera på. Meddelanden i popup-fönstret [!UICONTROL Notifications] och i ditt e-postmeddelande. |
| [!UICONTROL Priority] | Välj de kategorier som du vill ska ha hög prioritet. Dessa kategorier är markerade med en hög tagg och kan konfigureras för leverans som varningar. |
| [!UICONTROL Alerts] | Välj de meddelanden som du vill visa aviseringar för i webbläsaren. Varningar visas i fönstrets övre högra hörn under några sekunder. |
| E-post | Ange hur ofta du vill få e-postmeddelanden. (Inte skickat, direkt, dagligen eller varje vecka.) |

{style=&quot;table-layout:auto&quot;}

## Meddelanden {#notifications}

Välj **[!UICONTROL Notifications]** om du vill få meddelanden om relevanta och åtgärdbara uppdateringar, inklusive produktreleaser, underhållsmeddelanden, delade objekt och godkännandebegäranden.

![](assets/notifications-menu-small.png)

## Experience Cloud domäner {#domains}

Experience Cloud använder följande värdar för att leverera programmet, förbättra prestanda och produktupplevelse. Adobe rekommenderar att du lägger till dessa domäner i tillåtelselista i din brandvägg för att få en optimal upplevelse. Ytterligare domäner kan också användas för särskilda Experience Cloud-program, som Adobe Analytics. Mer information finns i dokumentationen för dessa program.

| Teknik | Domäner |
|--- |--- |
| Adobe Experience Cloud domäner | `adobe.com`, `adobe.net`, `adobe.io` |
| Adobe Identity Management Service (IMS) | `adobelogin.com` |
| Experience Cloud-teckensnitt | `typekit.net` |
| Gainsight (för produktvägledning och hjälp) | `esp.aptrinsic.com` |

## Få hjälp med administration och programövergripande tjänster

Den här guiden ger hjälp om Experience Cloud och produktadministration i Admin Console, vilket möjliggör lösningar för plattformstjänster. Du kan även få hjälp via Audience Library, Customer Attributes, Experience Cloud Assets med flera:

* [[!UICONTROL Audience Library]](audience-library.md)
* [[!UICONTROL Customer Attributes]](attributes.md)
* [[!UICONTROL Triggers]](triggers.md)
* [Experience Cloud [!UICONTROL Assets]](experience-cloud-assets.md)
* [Experience Cloud cookies](cookies-privacy.md)
* [Hantering](admin-getting-started.md)  av användare och produkter (Admin Console)
* [Möjliggör era lösningar för bastjänsterna](core-services.md)
* [Frågor och svar](admin-getting-started.md)
* [Organisationer och kontolänkning](organizations.md)
* [Integreringar](marketing-cloud-integrations.md)
* [Integrera Adobe Target med Experience Cloud](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=en)
* [Experience Cloud sekretess- och säkerhetsöversikt](assets/Adobe-Marketing-Cloud-Privacy-and-Security-Overview.pdf)
* [DNS-förhämtning](admin-getting-started.md#concept_6BC8C6856E3644F8956D7AD0A96383B7)

## Stödlinjer

Stödlinjer för Experience Cloud:

* [Adobe Mobile](https://experienceleague.adobe.com/docs/mobile-services/using/home.html?lang=en)
* [Experience Platform Co-op Graph](https://experienceleague.adobe.com/docs/device-co-op/using/home.html?lang=en)
* [Exchange](https://exchange.adobe.com/experiencecloud)
* [Experience Cloud ID-tjänst](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en)
* [Experience Platform datainsamling/start](https://experienceleague.adobe.com/docs/launch.html?lang=en)
* [Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=en)
* [Allmänt API för dataskyddsförordningen (GDPR)](https://www.adobe.io/apis/experiencecloud/gdpr.html)
* [[!UICONTROL Dynamic Tag Management]](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=en)

## Självstudiekurser

Självstudiekurser och snabba guider i Experience League:

* [Alla självstudiekurser i Experience League](https://experienceleague.adobe.com/?lang=en#quick-how-tos)
* [Självstudiekurser för Experience Platform](https://experienceleague.adobe.com/docs/launch-learn/tutorials/overview.html?lang=en)
* [Kunddataplattform i realtid](https://experienceleague.adobe.com/docs/platform-learn/tutorials/application-services/rtcdp/understanding-the-real-time-customer-data-platform.html?lang=en)

## Versionsinformation och tillhörande Experience Cloud-hjälp

* [Produktdokumentation för alla Experience Cloud-lösningar](https://experienceleague.adobe.com/docs/home.html?lang=en)  - Bläddra efter hjälp på Experience Cloud studiematerial och support
* [Versionsinformation och produktuppdateringar](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=en)  - Nyheter i Experience Cloud och prenumerationer för att få uppdateringar
* [Tutorials för implementering av bastjänster](https://experienceleague.adobe.com/docs/launch-learn/tutorials/overview.html?lang=en)  - Utforska videor och självstudiekurser om bastjänster
* [Experthjälp på Experience League](https://experienceleague.adobe.com/)  - Få hjälp av experter och communityn
* [Utbildning](https://helpx.adobe.com/se/learning.html?promoid=KAUDK)  - Ta kontakt med Adobe för att få ut det mesta av Adobe produkter
* [Kundupplevelsebloggen](https://blog.adobe.com/en/topics/digital-transformation.html)  - Läs Experience Cloud-bloggen
* [Kundtjänst](https://experienceleague.adobe.com/?support-solution=General#support)  - kontakta Adobe kundtjänst
