---
description: Lär dig hur du loggar in och om de centrala gränssnittskomponenterna i Experience Cloud. Lär dig mer om global sökning, dina kontoinställningar och hur du navigerar i gränssnittet och får hjälp.
solution: Experience Cloud
title: Viktiga användargränssnittkomponenter i Experience Cloud
feature: Central Interface Components
topic: Administration
role: Admin, User
level: Beginner, Intermediate, Experienced
source-git-commit: 1ca98d86c3559bf82c33c4fa3c7ec04bde26f1d8
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 1%

---

# Experience Cloud-gränssnittshjälp

Experience Cloud centrala gränssnittskomponenter innehåller funktioner som gör att du kan:

* Logga in och få tillgång till dina program och tjänster
* Söka efter produkthjälp och affärsobjekt med en global sökning
* Hantera dina kontoinställningar (aviseringar, aviseringar och prenumerationer)

## Stöd för webbläsare i Experience Cloud {#browser}

För bästa prestanda är Experience Cloud optimerat för de vanligaste webbläsarna, inklusive den senaste versionen, plus de två tidigare.

* Chrome
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

Alla programteam arbetar för globalt språkstöd, men alla program finns inte på alla språk som anges ovan. Om ditt primära språk inte stöds i ett Experience Cloud-program kan du även ange ett sekundärt språk som standard till när det är tillämpligt. Detta kan du göra i [Experience Cloud-användarinställningarna](https://experience.adobe.com/preferences).

## Logga in på Experience Cloud {#signin}

Logga in och verifiera att du är i rätt [organisation](organizations.md).

1. Navigera till [Adobe Experience Cloud](https://experience.adobe.com).
1. Välj **[!UICONTROL Sign in with an Adobe ID]**.
1. Kontrollera att du är i rätt organisation.

   ![Verifiera din organisation](assets/organizations-menu.png)

   Kontrollera att du har loggat in på rätt [organisation](organizations.md) genom att klicka på din profilavatar för att visa organisationsnamnet. Om du har tillgång till mer än en organisation kan du även visa och växla till en annan organisation direkt i sidhuvudsfältet.

   Om din organisation använder Federated ID:n kan du med Experience Cloud logga in med din organisations enkla inloggning utan att behöva ange din e-postadress och ditt lösenord. Lägg till `#/sso:@domain` i Experience Cloud-URL:en (`https://experience.adobe.com`) för att utföra den här åtgärden.

   För en organisation med Federated ID och domänen `adobecustomer.com` anger du URL-länken till `https://experience.adobe.com/#/sso:@adobecustomer.com`. Du kan också gå direkt till ett specifikt program genom att skapa ett bokmärke för den här URL:en, som bifogas med programsökvägen. (För Adobe Analytics, till exempel, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.)

## Access Experience Cloud-program {#navigation}

När du har loggat in på Experience Cloud kan du snabbt komma åt alla program, tjänster och organisationer från det enhetliga huvudet.

Markera programväljaren ![menyn](assets/menu-icon.png) för att komma åt de Experience Cloud-tjänster som du äger.

![Öppna Experience Cloud-program](assets/platform-core-services.png)

## Söka och få support i Experience Cloud {#search-support}

Med Experience Cloud-sökning kan du söka efter hjälp (dokumentation, självstudiekurser och kurser) på [Experience League](https://experienceleague.adobe.com/#home).

![Söka och support i Experience Cloud](assets/search-menu.png)

Menyn [!UICONTROL Help] ger dig även åtkomst till:

* **[!UICONTROL Support]:** Skapa en supportanmälan eller kontakta [!UICONTROL Support] med hjälp av Twitter.
* **[!UICONTROL Feedback]:** Kontakta Adobe med hjälp av feedback och berätta vad du tycker.
* **[!UICONTROL Status]:** Navigera till `https://status.adobe.com/experience_cloud` och kontrollera produktdriftsstatus och [!UICONTROL Manage Subscriptions].
* **[!UICONTROL Developer Connection]:** Navigering till `adobe.io` och hitta dokumentation för utvecklare.

## Kontoinställningar {#account-menu}

På kontoinställningsmenyn kan du:

* Ange ett mörkt tema (alla program stöder inte det här temat)
* Sök efter [organisationer](organizations.md)
* Logga ut
* Konfigurera inställningar, meddelanden och prenumerationer för kontot [](#preferences)

### Hantera Experience Cloud [!UICONTROL Preferences] {#preferences}

Inställningarna för Experience Cloud omfattar meddelanden, prenumerationer och varningar.

Välj **[!UICONTROL Preferences]** på din kontomeny ![inställningar](assets/preferences-icon-sm.png) för att hantera inställningar.

![Hantera Experience Cloud](assets/preferences-page.png)

På [!UICONTROL Experience Cloud preferences] kan du konfigurera följande funktioner:

| Funktion | Beskrivning |
|--- |--- |
| [Standardorganisation](organizations.md) | Välj den organisation som du vill se när du startar Experience Cloud. |
| [!UICONTROL Subscriptions] | Välj de produkter och kategorier som du vill prenumerera på. Meddelanden i popup-fönstret [!UICONTROL Notifications] och i ditt e-postmeddelande. |
| [!UICONTROL Priority] | Välj de kategorier som du vill ska ha hög prioritet. Dessa kategorier är markerade med en hög tagg och kan konfigureras för leverans som varningar. |
| [!UICONTROL Alerts] | Välj de meddelanden som du vill visa aviseringar för i webbläsaren. Varningar visas i fönstrets övre högra hörn under några sekunder. |
| E-post | Ange hur ofta du vill få e-postmeddelanden. (Inte skickat, direkt, dagligen eller veckovis.) |

{style="table-layout:auto"}

## Meddelanden {#notifications}

Välj **[!UICONTROL Notifications]** om du vill visa meddelanden som är viktiga för dig och meddelanden från Adobe.

![Meddelanden och meddelanden](assets/notifications-menu-small.png)

Du kan konfigurera meddelanden i inställningarna för [Experience Cloud](#preferences).
