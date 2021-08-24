---
description: 'Lär dig hur du loggar in och om de centrala gränssnittskomponenterna i Experience Cloud. Lär dig mer om global sökning, dina kontoinställningar och hur du navigerar i gränssnittet och får hjälp. '
solution: Experience Cloud
title: 'Experience Cloud centrala gränssnittskomponenter '
feature: '"Komponenter i det centrala gränssnittet"'
topic: Administrering
role: Admin, User
level: Beginner, Intermediate, Experienced
source-git-commit: c9a6059b0af9c6229fd72580f997c1c6f2dfbbe4
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 1%

---

# Experience Cloud-gränssnittshjälp

Experience Cloud centrala gränssnittskomponenter innehåller funktioner som gör att du kan:

* Logga in och få tillgång till dina program och tjänster
* Söka efter produkthjälp och affärsobjekt med en global sökning
* Hantera dina kontoinställningar (aviseringar, aviseringar och prenumerationer)

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

## Logga in på Experience Cloud {#signin}

Logga in och verifiera att du är i rätt [organisation](organizations.md).

1. Navigera till [Adobe Experience Cloud](https://experience.adobe.com).
1. Välj **[!UICONTROL Sign in with an Adobe ID]**.
1. Kontrollera att du är i rätt organisation.

   ![](assets/organizations-menu.png)

   Verifiera att du har loggat in på rätt [organisation](organizations.md) genom att klicka på din profilavatar för att visa organisationsnamnet. Om du har tillgång till mer än en organisation kan du även visa och växla till en annan organisation direkt i sidhuvudsfältet.

   Om din organisation använder Federated ID:n kan du med Experience Cloud logga in med din organisations inloggning utan att behöva ange din e-postadress och ditt lösenord. Om du vill göra det lägger du till `#/sso:@domain` i Experience Cloud-URL:en (`https://experience.adobe.com`).

   För en organisation med Federated ID och domänen `adobecustomer.com` anger du URL-länken till `https://experience.adobe.com/#/sso:@adobecustomer.com`. Du kan också gå direkt till ett specifikt program genom att skapa ett bokmärke för den här URL:en, som bifogas med programsökvägen. (För Adobe Analytics t.ex. `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.)

## Använd Experience Cloud {#navigation}

När du har loggat in på Experience Cloud kan du snabbt komma åt alla program, tjänster och organisationer från det enhetliga huvudet.

Markera programväljaren ![](assets/menu-icon.png) för att komma åt de Experience Cloud-tjänster som du äger.

![](assets/platform-core-services.png)

## Söka och få support i Experience Cloud {#search}

Med Experience Cloud-sökning kan du söka efter hjälp (dokumentation, självstudiekurser och kurser) på [Experience League](https://experienceleague.adobe.com/#home).

![](assets/search-menu.png)

Menyn [!UICONTROL Help] ger dig även åtkomst till:

* **[!UICONTROL Support]:** Skapa en supportanmälan eller kontakta  [!UICONTROL Support] Twitter.
* **[!UICONTROL Feedback]:** Kontakta Adobe med feedback och berätta vad du tycker.
* **[!UICONTROL Status]:** Navigera till  `https://status.adobe.com/experience_cloud` och kontrollera produktdriftsstatus och  [!UICONTROL Manage Subscriptions].
* **[!UICONTROL Developer Connection]:** Navigera till  `adobe.io` och hitta dokumentation för utvecklare.

## Kontoinställningar {#account-menu}

På kontoinställningsmenyn kan du:

* Ange ett mörkt tema (alla program stöder inte det här temat)
* Sök efter [organisationer](organizations.md)
* Logga ut
* Konfigurera konto [inställningar, meddelanden och prenumerationer](#preferences)

### Hantera Experience Cloud [!UICONTROL Preferences] {#preferences}

Inställningarna för Experience Cloud omfattar meddelanden, prenumerationer och varningar.

Välj **[!UICONTROL Preferences]** på din kontomeny ![](assets/preferences-icon-sm.png) om du vill hantera inställningarna.

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

Välj **[!UICONTROL Notifications]** om du vill visa meddelanden som är viktiga för dig och meddelanden från Adobe.

![](assets/notifications-menu-small.png)

Du kan konfigurera meddelanden i [Experience Cloud-inställningarna](#preferences).
