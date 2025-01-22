---
description: Lär dig mer om centrala gränssnittskomponenter för Experience Cloud. Få hjälp med användar- och produktadministration i Admin Console, aktivera program för Experience Cloud-tjänster. Få hjälp med Audience Library, Customer Attributes, Experience Cloud Assets med flera.
title: Gränssnittsdokumentation för Experience Cloud
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: b122f71a8bffeaaeb20c974c618bacc5a40c2cd9
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Översikt över det centrala gränssnittet i Experience Cloud

[Experience Cloud](https://experience.adobe.com) är en integrerad familj av program, produkter och tjänster för digital marknadsföring i Adobe. Från det intuitiva gränssnittet får du snabbt tillgång till dina molnprogram, produktfunktioner och tjänster.

![Experience Cloud](assets/landing.png)

Från Experience Cloud kan du:

* Få tillgång till alla Experience Cloud-program och -tjänster
* På Hjälp-menyn söker du efter produktdokumentation, självstudiekurser och communityinlägg. Visa resultat i Experience League.
* Sök efter affärsobjekt globalt med hjälp av en global sökning (endast Experience Platform) i sökfältet.
* Hantera ditt konto [inställningar](features/account-preferences.md) (aviseringar, aviseringar och prenumerationer)

## Logga in på Experience Cloud {#signin}

Logga in och verifiera att du är i rätt [organisation](administration/organizations.md).

1. Navigera till [Adobe Experience Cloud](https://experience.adobe.com).
1. Skriv din e-postadress för Adobe och välj sedan **[!UICONTROL Continue]**.
1. Välj ett konto.
1. Skriv ditt lösenord.
1. Kontrollera att du är i rätt organisation.

   ![Verifiera att du är i rätt organisation](assets/organizations-menu.png)

   **Verifiera din organisation**

   [organisationen](administration/organizations.md) visas i gränssnittshuvudet.

   Om din organisation använder Federated ID:n kan du med Experience Cloud logga in med din organisations enkla inloggning utan att behöva ange din e-postadress och ditt lösenord. Lägg till `#/sso:@domain` i Experience Cloud-URL:en (`https://experience.adobe.com`) för att utföra den här åtgärden.

   För en organisation med Federated ID och domänen `adobecustomer.com` anger du URL-länken till `https://experience.adobe.com/#/sso:@adobecustomer.com`. Du kan också gå direkt till ett specifikt program genom att skapa ett bokmärke för den här URL:en, som bifogas med programsökvägen. (För Adobe Analytics, till exempel, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.)

## Access Experience Cloud-program {#navigation}

När du har loggat in på Experience Cloud kan du snabbt komma åt alla program, tjänster och organisationer från det enhetliga huvudet.

Gå till programväljaren ![menu](assets/apps-icon.png) om du vill komma åt Experience Cloud-program och -tjänster som har etablerats för dig i din organisation.

![Öppna Experience Cloud-program](assets/platform-core-services.png)

## Få hjälp och support {#support}

Få tillgång till inlärning och hjälp med **[!UICONTROL Help center]** (![asset](assets/help-icon.png)) i sidhuvudet, inklusive hjälpinnehåll (dokumentation, självstudiekurser och kurser) på [Experience League](https://experienceleague.adobe.com/#home), samt ytterligare resurser för enskilda program. Du kan även skicka in öppen feedback och skapa prioriterade supportärenden.

![Få hjälp och support](assets/search-menu.png)

Menyn [!UICONTROL Help] ger dig även åtkomst till:

* **[!UICONTROL Support]:** Skapa en supportanmälan eller kontakta [!UICONTROL Support] med hjälp av Twitter.
* **[!UICONTROL Feedback]:** Dela feedback om din Experience Cloud-upplevelse. Dina synpunkter används för att förbättra Adobe produkter och tjänster.
* **[!UICONTROL Status]:** Navigera till `https://status.adobe.com/experience_cloud` och kontrollera produktdriftsstatus och [!UICONTROL Manage Subscriptions].
* **[!UICONTROL Developer Connection]:** Navigering till `adobe.io` och hitta dokumentation för utvecklare.

## Hantera din användarprofil

På menyn [!UICONTROL Profile] kan du:

* Ange ett mörkt tema (alla program stöder inte det här temat)
* Hantera [inställningar för Experience Cloud](features/account-preferences.md)
* Välj eller sök efter en [organisation](administration/organizations.md)
* Visa [!UICONTROL Legal Notices]
* Logga ut
* Konfigurera kontoinställningar, meddelanden och prenumerationer

## Visa meddelanden och meddelanden i produkten {#notifications}

Klicka på klockikonen för att visa meddelanden och meddelanden. Meddelanden kan vara relevanta och användbara uppdateringar, inklusive produktreleaser, underhållsmeddelanden, delade artiklar och godkännandeförfrågningar.

![Meddelanden och meddelanden](assets/notifications-menu-small.png)

Mer information om hur du hanterar meddelanden och aviseringar finns i [Kontoinställningar och meddelanden](features/account-preferences.md)
