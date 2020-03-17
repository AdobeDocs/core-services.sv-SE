---
description: Lär dig mer om Experience Cloud Admin Tool, för att visa en sorterbar och filterbar lista över alla Experience Cloud-användare.
keywords: core services
seo-description: Lär dig mer om Experience Cloud Admin Tool, för att visa en sorterbar och filterbar lista över alla Experience Cloud-användare.
seo-title: Visa Experience Cloud-användare och användarinformation
solution: Experience Cloud
title: 'Visa Experience Cloud-användare och användarinformation '
index: true
translation-type: tm+mt
source-git-commit: 5e57aedb38e6914f7e99b1b26df9e4bb52b9e13d

---


# Visa Experience Cloud-användare i Admin Tool

Administratörer kan visa en sorterbar och filterbar lista över alla Experience Cloud-användare och deras information i Admin Tool. Användarinformationen innehåller information om en användares produktåtkomst, roller och den senast öppnade informationen. (**Obs!** Användar- och produkthantering är konfigurerad i [Admin Console](admin-getting-started.md).)

1. Logga in på `https://experience.adobe.com/.`

   ![](assets/admin-tool.png)

1. Klicka på Experience Cloud Home **[!UICONTROL Admin Tool.]**

   (I hemsidans URL kan du även ersätta _hemsidan_ med _admin._)

   Sidan visas [!UICONTROL Users] .

## Sidan Användare

På den här sidan visas en fullständig lista över användare som har tillgång till Experience Cloud i din organisation. Här finns information om lösningsberättigande och senaste inloggning. Du kan söka, sortera och filtrera efter anpassade vyer av användarlistan.

![](assets/admin-tool-users.png)

| Element | Beskrivning |
|---|---|
| [!UICONTROL Name] | Användarens för- och efternamn. Du kan sortera den här kolumnen från A till Z och Z till A.  Klicka på en användares namn för att se mer information om användaren. |
| [!UICONTROL Email] | E-postadressen som är associerad med användaren. Kolumnen kan sorteras A->Z, Z->A. |
| [!UICONTROL ID Type] | Identitetstypen för användarens konto. Du kan använda filter för att visa specifika ID-typer. Mer information finns i [Hantera identitetstyper](https://helpx.adobe.com/enterprise/using/identity.html) . |
| [!UICONTROL Solutions] | Sammanfattning av Experience Cloud-lösningar som användaren har tillgång till. Du kan använda filter för att begränsa listan över användare med specifik lösningsåtkomst. |
| [!UICONTROL Last Login] | Tid och datum för den senaste användarinloggningen till Experience Cloud. Den här kolumnen kan sorteras efter stigande eller fallande datum. <br> **Viktigt:** Från och med den 13 januari 2020 sparas användarens senaste inloggningsuppgifter i 365 dagar. Den här informationen är avsedd att visa den aktuella inloggningsaktiviteten i Experience Cloud och inte en rekommendation om att vidta åtgärder för inaktiva konton före den 13 januari 2020. |

## Anpassa användarlistvyn

Du kan söka efter, sortera eller filtrera kolumnerna för att anpassa användarlistan.

* Sök efter användare efter namn eller e-post. Sökningar matchar textsträngen som du skriver.
* Sortera kolumnen efter stigande eller fallande värden. Detta gäller för [!UICONTROL Name,] spalter [!UICONTROL Email,] och [!UICONTROL Last Login] spalter.
* Klicka på **[!UICONTROL Filter By]** ikonen om du vill använda flera filter för att lista användare med specifika villkor. När flera filterkategorier används innehåller sökningarna e-postdomän- `AND` ID- `AND` typslösning.

| Element | Beskrivning |
|---------|----------|
| [!UICONTROL Email Domain] filter | Sök efter teckensträngar i kolumnen E-post om du vill begränsa resultatet till en eller flera domäner. Lägg till flera filter genom att trycka på Retur efter varje sökord |
| [!UICONTROL ID Type] filter | Välj bland tillgängliga ID-typer. Flera ID-typer kan användas som filter. |
| [!UICONTROL Solution] filter | Välj bland tillgängliga lösningar. Flera lösningsfilter söker efter resultat som innehåller Lösning 1 `OR` Lösning 2. |

## Visa användarinformation

Klicka på användarens e-postadress om du vill visa information för en användare på [!UICONTROL Users] sidan.

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

I det här avsnittet visas en sammanfattning av Experience Cloud-lösningar som användaren har tillgång till. Inkluderar produktens administrativa roll när det är tillämpligt

## Detaljerad lista över produktåtkomst

I det här avsnittet visas en fullständig lista över alla produktprofilmedlemskap för användaren.

| Element | Beskrivning |
|---------|----------|
| [!UICONTROL Product] | Namn på den produkt som är associerad med produktprofilen. |
| [!UICONTROL Instance] | Namn på den instans (till exempel inloggningsföretag eller innehavare) som är associerad med produkt- och produktprofilen. |
| [!UICONTROL Product Profile] | Unikt namn på produktprofilen. |
| [!UICONTROL Assigned by Group] | Namnet på den användargrupp som associerar användaren med en produktprofil. Tomma resultat indikerar att användaren har tilldelats produktprofilen direkt, inte via en grupp. |
| [!UICONTROL Product Roles] | Rolltilldelning av användaren i produktprofilen. För närvarande gäller den här informationen endast för Target-produktprofiler. |
