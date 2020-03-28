---
description: Lär dig mer om Experience Cloud Admin Tool, för att visa en sorterbar och filterbar lista över alla Experience Cloud-användare.
keywords: core services
seo-description: Lär dig mer om Experience Cloud Admin Tool, för att visa en sorterbar och filterbar lista över alla Experience Cloud-användare.
seo-title: Visa Experience Cloud-användare och användarinformation
solution: Experience Cloud
title: 'Visa Experience Cloud-användare och användarinformation '
index: true
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Visa Experience Cloud-användare i Admin Tool

Administratörer kan visa en sorterbar och filterbar lista över alla Experience Cloud-användare och deras information i Admin Tool. Användarinformationen innehåller information om en användares produktåtkomst, roller och den senast öppnade informationen. (**Obs!** Användar- och produkthantering är konfigurerad i [Admin Console](admin-getting-started.md).)

1. Logga in på `https://experience.adobe.com/.`

   ![](assets/admin-tool.png)

1. Klicka på **[!UICONTROL Administratörsverktyg på startsidan för Experience Cloud.]**

   (I hemsidans URL kan du även ersätta _hemsidan_ med _admin._)

   Sidan [!UICONTROL Användare] visas.

## Sidan Användare

På den här sidan visas en fullständig lista över användare som har tillgång till Experience Cloud i din organisation. Här finns information om lösningsberättigande och senaste inloggning. Du kan söka, sortera och filtrera efter anpassade vyer av användarlistan.

![](assets/admin-tool-users.png)

| Element | Beskrivning |
|---|---|
| [!UICONTROL Namn] | Användarens för- och efternamn. Du kan sortera den här kolumnen från A till Z och Z till A.  Klicka på en användares namn för att se mer information om användaren. |
| [!UICONTROL E-post] | E-postadressen som är associerad med användaren. Kolumnen kan sorteras A->Z, Z->A. |
| [!UICONTROL ID-typ] | Identitetstypen för användarens konto. Du kan använda filter för att visa specifika ID-typer. Mer information finns i [Hantera identitetstyper](https://helpx.adobe.com/enterprise/using/identity.html) . |
| [!UICONTROL Lösningar] | Sammanfattning av Experience Cloud-lösningar som användaren har tillgång till. Du kan använda filter för att begränsa listan över användare med specifik lösningsåtkomst. |
| [!UICONTROL Senaste inloggning] | Tid och datum för den senaste användarinloggningen till Experience Cloud. Den här kolumnen kan sorteras efter stigande eller fallande datum. <br> **Viktigt:** Från och med den 13 januari 2020 sparas användarens senaste inloggningsuppgifter i 365 dagar. Den här informationen är avsedd att visa den aktuella inloggningsaktiviteten i Experience Cloud och inte en rekommendation om att vidta åtgärder för inaktiva konton före den 13 januari 2020. |

## Anpassa användarlistvyn

Du kan söka efter, sortera eller filtrera kolumnerna för att anpassa användarlistan.

* Sök efter användare efter namn eller e-post. Sökningar matchar textsträngen som du skriver.
* Sortera kolumnen efter stigande eller fallande värden. Detta gäller kolumnerna [!UICONTROL Namn,] [!UICONTROL E-post och] Senaste inloggning  .
* Klicka på ikonen **[!UICONTROL Filtrera efter]** om du vill använda flera filter på en lista med användare med specifika villkor. När flera filterkategorier används innehåller sökningarna e-postdomän- `AND` ID- `AND` typslösning.

| Element | Beskrivning |
|---------|----------|
| [!UICONTROL E-postdomänfilter] | Sök efter teckensträngar i kolumnen E-post om du vill begränsa resultatet till en eller flera domäner. Lägg till flera filter genom att trycka på Retur efter varje sökord |
| [!UICONTROL ID-typsfilter] | Välj bland tillgängliga ID-typer. Flera ID-typer kan användas som filter. |
| [!UICONTROL Lösning] , filter | Välj bland tillgängliga lösningar. Flera lösningsfilter söker efter resultat som innehåller Lösning 1 `OR` Lösning 2. |

## Visa användarinformation

Klicka på användarens e-postadress på sidan [!UICONTROL Användare] om du vill visa information om en användare.

![](assets/admin-tool-user-details.png)

En detaljerad vy över varje användare visar viktig information om användarens lösningsåtkomst, admin- och produktroller samt information om den senaste åtkomsten.

## Om avsnitt

I det här avsnittet visas en sammanfattning av användarkontot, inklusive:

* User Avatar and System Admin Badge (om tillämpligt)
* Namn
* E-post
* Användarnamn (Federated ID-konton kan ha andra användarnamn än e-postadresser)
* [ID-typ](https://helpx.adobe.com/enterprise/using/identity.html)
* Land
* Senaste inloggning

## Sammanfattning av lösningar

I det här avsnittet visas en sammanfattning av Experience Cloud-lösningar som användaren har tillgång till. Inkluderar den administrativa rollen för produkten när det är tillämpligt.

## Detaljerad lista över produktåtkomst

I det här avsnittet visas en fullständig lista över alla produktprofilmedlemskap för användaren.

| Element | Beskrivning |
|---------|----------|
| [!UICONTROL Produkt] | Namn på den produkt som är associerad med produktprofilen. |
| [!UICONTROL Instans] | Namn på den instans (till exempel inloggningsföretag eller innehavare) som är associerad med produkt- och produktprofilen. |
| [!UICONTROL Produktprofil] | Unikt namn på produktprofilen. |
| [!UICONTROL Tilldelad av grupp] | Namnet på den användargrupp som associerar användaren med en produktprofil. Tomma resultat indikerar att användaren har tilldelats produktprofilen direkt, inte via en grupp. |
| [!UICONTROL Produktroller] | Rolltilldelning av användaren i produktprofilen. För närvarande gäller dessa uppgifter endast produktprofiler för Adobe Target. |
