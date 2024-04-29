---
description: Lär dig mer om centrala gränssnittskomponenter för Experience Cloud. I den här hjälpen ingår användar- och produktadministration i Admin Console, aktivering av program för Experience Cloud-tjänster samt hjälp om Audience Library, Customer Attributes, Experience Cloud Assets med flera.
title: Hjälp och dokumentation för Experience Cloud-gränssnittet
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: a4e0461791cd676365857c2dd4ef28c0e40c3430
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Översikt över det centrala gränssnittet i Experience Cloud

[Experience Cloud](https://experience.adobe.com) är en integrerad familj av program, produkter och tjänster för digital marknadsföring i Adobe. Från det intuitiva gränssnittet får du snabbt tillgång till dina molnprogram, produktfunktioner och tjänster.

![Experience Cloud](assets/landing.png)

Från Experience Cloud kan du:

* Få tillgång till dina program och tjänster
* På Hjälp-menyn söker du efter produktdokumentation, självstudiekurser och communityinlägg. Visa resultat i Experience League.
* Sök efter affärsobjekt globalt med hjälp av en global sökning (endast Experience Platform) i sökfältet.
* Hantera dina kontoinställningar (aviseringar, aviseringar och prenumerationer)

## Logga in på Experience Cloud {#signin}

Logga in och verifiera att du är rätt [organisation](administration/organizations.md).

1. Navigera till [Adobe Experience Cloud](https://experience.adobe.com).
1. Skriv din e-postadress för Adobe och välj **[!UICONTROL Continue]**.
1. Välj ett konto.
1. Skriv ditt lösenord.
1. Kontrollera att du är i rätt organisation.

   ![Verifiera att du är i rätt organisation](assets/organizations-menu.png)

   **Verifiera din organisation**

   Så här verifierar du att du har loggat in på rätt [organisation](administration/organizations.md)klickar du på din profilavatar för att se organisationens namn. Om du har tillgång till mer än en organisation kan du även visa och växla till en annan organisation direkt i sidhuvudsfältet.

   Om din organisation använder Federated ID:n kan du med Experience Cloud logga in med din organisations enkla inloggning utan att behöva ange din e-postadress och ditt lösenord. Lägg till `#/sso:@domain` till Experience Cloud URL (`https://experience.adobe.com`) för att utföra den här uppgiften.

   För en organisation med Federated ID och domänen `adobecustomer.com`, ange URL-länken till `https://experience.adobe.com/#/sso:@adobecustomer.com`. Du kan också gå direkt till ett specifikt program genom att skapa ett bokmärke för den här URL:en, som bifogas med programsökvägen. (För Adobe Analytics, till exempel `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.)

## Access Experience Cloud-program {#navigation}

När du har loggat in på Experience Cloud kan du snabbt komma åt alla program, tjänster och organisationer från det enhetliga huvudet.

Gå till programväljaren för att få åtkomst till Experience Cloud-program och -tjänster som du har fått i din organisation ![meny](assets/menu-icon.png).

![Access Experience Cloud-program](assets/platform-core-services.png)

## Få hjälp och support {#support}

Lär dig mer och få hjälp med hjälpikonen (![resurs](assets/help-icon.png)) i sidhuvudet, inklusive hjälpinnehåll (dokumentation, självstudiekurser och kurser) på [Experience League](https://experienceleague.adobe.com/#home), samt ytterligare resurser för enskilda program. Du kan även skicka in öppen feedback och skapa prioriterade supportärenden.

![Få hjälp och support](assets/search-menu.png)

The [!UICONTROL Help] -menyn ger dig även tillgång till

* **[!UICONTROL Support]:** Skapa en supportanmälan eller kontakt [!UICONTROL Support] med Twitter.
* **[!UICONTROL Feedback]:** Dela feedback om Experience Cloud. Dina synpunkter används för att förbättra Adobe produkter och tjänster.
* **[!UICONTROL Status]:** Navigera till `https://status.adobe.com/experience_cloud` och kontrollera produktens driftstatus och [!UICONTROL Manage Subscriptions].
* **[!UICONTROL Developer Connection]:** Navigera till `adobe.io` och hitta dokumentation för utvecklare.

## Användarprofil och kontoinställningar {#preferences}

Inställningarna för Experience Cloud omfattar meddelanden, prenumerationer och varningar. På kontoinställningsmenyn kan du:

* Ange ett mörkt tema (alla program stöder inte det här temat)
* Sök efter [Organisationer](administration/organizations.md)
* Logga ut
* Konfigurera kontoinställningar, meddelanden och prenumerationer

Om du vill hantera inställningar väljer du **[!UICONTROL Preferences]** från din kontomeny ![inställningar](assets/preferences-icon-sm.png).

![Användarprofil och kontoinställningar](assets/preferences-page.png)

På [!UICONTROL Experience Cloud preferences]kan du konfigurera följande funktioner:

| Funktion | Beskrivning |
|--- |--- |
| Standard [organisation](administration/organizations.md) | Välj den organisation som du vill se när du startar Experience Cloud. |
| [!UICONTROL Product data collection] | Välj vilka tekniker Adobe kan använda för att samla in data om hur du använder dina Adobe-produkter. |
| [!UICONTROL Personalized learning recommendations and promotions] | Välj var du vill få personlig hjälp för dina Adobe-produkter. Den här hjälpen finns tillgänglig via e-post, i programmet och i Experience League Communities. [Läs mer.](features/personalized-learning.md) |
| [!UICONTROL Subscriptions] | Välj de produkter och kategorier som du vill prenumerera på. Meddelanden i [!UICONTROL Notifications] popup-fönster och i e-postmeddelandet. |
| [!UICONTROL Priority] | Välj de kategorier som du vill ska ha hög prioritet. Dessa kategorier är markerade med en hög tagg och kan konfigureras för leverans som varningar. |
| [!UICONTROL Alerts] | Välj de meddelanden som du vill visa aviseringar för i webbläsaren. Varningar visas i fönstrets övre högra hörn under några sekunder. |
| E-post | Ange hur ofta du vill få e-postmeddelanden. (Inte skickat, direkt, dagligen eller veckovis.) |

{style="table-layout:auto"}

## Meddelanden {#notifications}

Välj **[!UICONTROL Notifications]** att få varningar om relevanta och användbara uppdateringar, inklusive produktreleaser, underhållsmeddelanden, delade artiklar och godkännandeförfrågningar.

![Meddelanden](assets/notifications-menu-small.png)
