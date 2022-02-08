---
description: Lär dig mer om centrala gränssnittskomponenter för Experience Cloud. I den här hjälpen ingår användar- och produktadministration i Admin Console, aktivering av program för Experience Cloud-tjänster samt hjälp om Audience Library, Customer Attributes, Experience Cloud Assets med flera.
solution: Experience Cloud
title: Hjälp och dokumentation för Experience Cloud-gränssnittet
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: 540896e1127c4d2abea2bf4ca63ac85315dda8c2
workflow-type: tm+mt
source-wordcount: '1326'
ht-degree: 2%

---

# Handbok för gränssnittskomponenter i Experience Cloud Central

[Experience Cloud](https://experience.adobe.com) är en integrerad familj av program, produkter och tjänster för digital marknadsföring. Från det intuitiva gränssnittet får du snabbt tillgång till dina molnprogram, produktfunktioner och tjänster.

![Experience Cloud](assets/landing.png)

Från Experience Cloud kan du:

* Få tillgång till dina program och tjänster
* Sök efter produktdokumentation, självstudiekurser och communityinlägg
* Sök efter affärsobjekt globalt med hjälp av en global sökning (endast Experience Platform)
* Hantera dina kontoinställningar (aviseringar, aviseringar och prenumerationer)

## Logga in på Experience Cloud {#signin}

Logga in och verifiera att du är rätt [organisation](organizations.md).

1. Navigera till [Adobe Experience Cloud](https://experience.adobe.com).
1. Skriv din e-postadress för Adobe och välj **[!UICONTROL Continue]**.

   Administratörer, se [Experience Cloud användarautentisering](admin-getting-started.md#migration) för viktiga uppdateringar av identitetstyper (företags-ID).

1. Välj ett konto.
1. Skriv ditt lösenord.
1. Kontrollera att du är i rätt organisation.

   ![Verifiera att du är i rätt organisation](assets/organizations-menu.png)

   **Verifiera din organisation**

   Så här verifierar du att du har loggat in på rätt [organisation](organizations.md)klickar du på din profilavatar för att se organisationens namn. Om du har tillgång till mer än en organisation kan du även visa och växla till en annan organisation direkt i sidhuvudsfältet.

   Om din organisation använder Federated ID:n kan du med Experience Cloud logga in med din organisations inloggning utan att behöva ange din e-postadress och ditt lösenord. Lägg till `#/sso:@domain` till Experience Cloud URL (`https://experience.adobe.com`).

   För en organisation med Federated ID och domänen `adobecustomer.com`, ange URL-länken till `https://experience.adobe.com/#/sso:@adobecustomer.com`. Du kan också gå direkt till ett specifikt program genom att skapa ett bokmärke för den här URL:en, som bifogas med programsökvägen. (Exempel: för Adobe Analytics `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.)

## Använd Experience Cloud {#navigation}

När du har loggat in på Experience Cloud kan du snabbt komma åt alla program, tjänster och organisationer från det enhetliga huvudet.

Gå till programväljaren för att få åtkomst till Experience Cloud-program och -tjänster som du har fått i din organisation ![](assets/menu-icon.png).

![Använd Experience Cloud](assets/platform-core-services.png)

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

Alla programteam arbetar för globalt språkstöd, men alla program finns inte på alla språk som anges ovan. Om ditt primära språk inte stöds i ett Experience Cloud-program kan du även ange ett sekundärt språk som standard till när det är tillämpligt. Detta kan göras i [Användarinställningar för Experience Cloud](https://experience.adobe.com/preferences).

## Få hjälp och support {#support}

Lär dig mer och få hjälp med hjälpikonen (![resurs](assets/help-icon.png)) i sidhuvudet, inklusive hjälpinnehåll (dokumentation, självstudiekurser och kurser) på [Experience League](https://experienceleague.adobe.com/#home), samt ytterligare resurser för enskilda program. Du kan även skicka in öppen feedback och skapa prioriterade supportärenden.

![Få hjälp och support](assets/search-menu.png)

The [!UICONTROL Help] -menyn ger dig även tillgång till

* **[!UICONTROL Support]:** Skapa en supportanmälan eller kontakt [!UICONTROL Support] med Twitter.
* **[!UICONTROL Feedback]:** Dela feedback om Experience Cloud. Dina synpunkter används för att förbättra Adobe produkter och tjänster.
* **[!UICONTROL Status]:** Navigera till `https://status.adobe.com/experience_cloud` och kontrollera produktens driftstatus och [!UICONTROL Manage Subscriptions].
* **[!UICONTROL Developer Connection]:** Navigera till `adobe.io` och hitta dokumentation för utvecklare.

## Sök globalt efter objekt och enheter {#search}

Med den globala sökningen kan du söka efter sökbara affärsobjekt eller entiteter på ett smidigt och enhetligt sätt med ett enda klick. Den här sökningen visar de objekt du nyligen har använt.

![Sök globalt efter objekt och enheter](assets/platform-search.png)

>[!NOTE]
>
>Den globala sökningen är inte tillgänglig i alla Experience Cloud-program, men allt eftersom mer innehåll indexeras läggs det till i relevanta program. Tillgänglighet från och med juli 2021:

* Experience Platform
* Journey Optimizer

## Användarprofil och kontoinställningar {#preferences}

Inställningarna för Experience Cloud omfattar meddelanden, prenumerationer och varningar. På kontoinställningsmenyn kan du:

* Ange ett mörkt tema (alla program stöder inte det här temat)
* Sök efter [Organisationer](organizations.md)
* Logga ut
* Konfigurera kontoinställningar, meddelanden och prenumerationer

Om du vill hantera inställningar väljer du **[!UICONTROL Preferences]** från din kontomeny ![](assets/preferences-icon-sm.png).

![Användarprofil och kontoinställningar](assets/preferences-page.png)

På [!UICONTROL Experience Cloud preferences]kan du konfigurera följande funktioner:

| Funktion | Beskrivning |
|--- |--- |
| Standard [organisation](organizations.md) | Välj den organisation som du vill se när du startar Experience Cloud. |
| [!UICONTROL Subscriptions] | Välj de produkter och kategorier som du vill prenumerera på. Meddelanden i [!UICONTROL Notifications] popup-fönster och i mejl. |
| [!UICONTROL Priority] | Välj de kategorier som du vill ska ha hög prioritet. Dessa kategorier är markerade med en hög tagg och kan konfigureras för leverans som varningar. |
| [!UICONTROL Alerts] | Välj de meddelanden som du vill visa aviseringar för i webbläsaren. Varningar visas i fönstrets övre högra hörn under några sekunder. |
| E-post | Ange hur ofta du vill få e-postmeddelanden. (Inte skickat, direkt, dagligen eller varje vecka.) |

{style=&quot;table-layout:auto&quot;}

## Meddelanden {#notifications}

Välj **[!UICONTROL Notifications]** att få varningar om relevanta och användbara uppdateringar, inklusive produktreleaser, underhållsmeddelanden, delade artiklar och godkännandeförfrågningar.

![Meddelanden](assets/notifications-menu-small.png)

## Experience Cloud domäner {#domains}

Experience Cloud använder följande värdar för att leverera programmet, förbättra prestanda och produktupplevelse. Adobe rekommenderar att du lägger till dessa domäner i tillåtelselista i din brandvägg för att få en optimal upplevelse. Ytterligare domäner kan också användas för särskilda Experience Cloud-program, som Adobe Analytics. Mer information finns i dokumentationen för dessa program.

| Teknik | Domäner |
|--- |--- |
| Adobe Experience Cloud domäner | `adobe.com`, `adobe.net`, `adobe.io` |
| Adobe Identity Management Service (IMS) | `adobelogin.com` |
| Experience Cloud-teckensnitt | `typekit.net` |
| Gainsight (för produktvägledning och hjälp) | `esp.aptrinsic.com` |

## Få hjälp med administration och programövergripande tjänster

I den här guiden får du hjälp om Experience Cloud och produktadministration i Admin Console, vilket möjliggör användning av plattformstjänster. Du kan även få hjälp via Audience Library, Customer Attributes, Experience Cloud Assets med flera:

* [[!UICONTROL Audience Library]](audience-library.md)
* [[!UICONTROL Customer Attributes]](attributes.md)
* [[!UICONTROL Triggers]](triggers.md)
* [Experience Cloud [!UICONTROL Assets]](experience-cloud-assets.md)
* [Experience Cloud cookies](cookies-privacy.md)
* [Hantering av användare och produkter](admin-getting-started.md) (Admin Console)
* [Aktivera era program för bastjänster](core-services.md)
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
* [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/application-services/rtcdp/understanding-the-real-time-customer-data-platform.html?lang=en)

## Versionsinformation och tillhörande Experience Cloud-hjälp

* [Produktdokumentation för alla Experience Cloud-program](https://experienceleague.adobe.com/docs/home.html?lang=en) - Bläddra efter hjälp på Experience Cloud studiematerial och support
* [Versionsinformation och produktuppdateringar](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=en) - Nyheter i Experience Cloud och prenumerera för att få uppdateringar
* [Tutorials för att införa bastjänster](https://experienceleague.adobe.com/docs/launch-learn/tutorials/overview.html?lang=en) - Utforska videor och självstudiekurser om bastjänster
* [Experthjälp på Experience League](https://experienceleague.adobe.com/) - Få guidad inlärning från experter och communityn
* [Utbildning](https://helpx.adobe.com/se/learning.html?promoid=KAUDK) - Ta kontakt med Adobe för att få ut så mycket som möjligt av Adobe
* [Customer Experience Blog](https://blog.adobe.com/en/topics/digital-transformation.html) - Läs Experience Cloud bloggen
* [Kundtjänst](https://experienceleague.adobe.com/?support-solution=General#support) - Kontakta Adobe kundtjänst
