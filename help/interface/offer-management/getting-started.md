---
description: En översikt över Erbjudandehantering, hur du får tillgång till den och hur du beviljar användarbehörigheter.
seo-description: En översikt över Erbjudandehantering, hur du får tillgång till den och hur du beviljar användarbehörigheter.
seo-title: Komma igång
title: Komma igång
uuid: 28d83606-ee36-4bbf-b52d-bbe8b097f6d5
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 2f0c2eb70313c42da9e7ac1d75429ec768dea10d

---


# Adobes erbjudandehantering {#section_07CBD4C01F4049A5A19781737D2DCD35}

[!UICONTROL Offer Management] ger möjlighet att skapa, hantera och fatta beslut i alla kanaler i Experience Cloud. Det fungerar som en central katalog för erbjudanden där du kan koppla berättiganderegler och flera innehållsdelar till varje _erbjudandeobjekt._ Ni kan publicera dessa erbjudanden över olika kanaler och platser och leverera det bästa erbjudandet för varje kund vid varje interaktion. Dessa funktioner gör att ni kontinuerligt kan leverera det bästa erbjudandet till era kunder på ett sätt som är enhetligt och samordnat för upplevelsen.

Några fördelar:

* Förbättrade prestanda för e-postkampanjer genom att leverera mer personaliserade erbjudanden i era e-postmeddelanden.
* Förbättrat arbetsflöde: I stället för att skapa flera leveranser eller kampanjer kan marknadsföringsteamen förbättra arbetsflödet genom att skapa en enda leverans och variera erbjudandena i olika delar av mallen.
* Gör att ni kan skapa, hantera och godkänna erbjudanden utanför Adobe Campaign Standard-arbetsflödet för e-postkampanjer.
* Styr hur många gånger ett erbjudande visas för e-postkampanjer och kunder.

## Åtkomst till erbjudanden {#task_DEB6F6A4B6E04E15AD3E1817D700688E}

Lär dig hur du får tillgång till Erbjudandehantering.

1. Kontakta Adobe för etablering.

   En Experience Cloud-organisation måste ha en instans av Campaign Standard. Adobe kan också aktivera en funktion i Campaign som gör att ni kan skapa erbjudandeaktiviteter i e-postmeddelanden.

1. Klicka på lösningsväljaren på Experience Clouds navigeringsmeny och klicka sedan på **[!UICONTROL Offers]**.

   ![](assets/access-offers.png)

   Om du vill få tillgång till erbjudanden i Campaign Standard klickar du på **[!UICONTROL Offers]** ikonen i en e-postmall.

   ![](assets/campaign-add-offer.png)

   När du ser båda dessa objekt i Marketing Cloud och i ditt Adobe Campaign-konto har du fått de funktioner som krävs för att komma igång.

## Användare och behörigheter {#concept_81F0ABB07ACC49E099EDCD87AA0436E1}

Administratörer kan lägga till användare [!UICONTROL Offer Management] i Admin Console. En e-postinbjudan skickas till den nya användaren med instruktioner om hur man kommer åt produkten. När en användare har lagts till kan du justera deras behörigheter och ge dem åtkomst till olika funktioner i hela [!UICONTROL Offer Management]processen.

Mer information om hur du använder Admin Console finns i dokumentationen [till Admin Console i](https://helpx.adobe.com/enterprise/help/aedash.html)HelpX.

I Campaign har standardanvändare automatiskt rätt att bädda in erbjudandeaktiviteter i en e-postmall.

>[!NOTE]
>
>Det finns inga behörigheter för betaversion. Alla användare som har lagts till i erbjudanden har full tillgång till alla funktioner i [!UICONTROL Offer Management].

## Skapa en produktprofil för Erbjudandehantering

En produktprofil är en uppsättning behörigheter som kan kombineras för att skapa en användarroll i en produkt. Produktprofiler måste skapas och sedan tilldelas användare eller grupper.

1. Gå till Adobe [Admin Console](https://adminconsole.adobe.com/).

1. Klicka på proceduren (till **[!UICONTROL Offers]** exempel).

1. På [!UICONTROL Product Pofiles] sidan klickar du på **[!UICONTROL New Profile]**.

1. Ange ett namn och en beskrivning för produktprofilen och klicka sedan på **[!UICONTROL Done]**.

1. Klicka på **[!UICONTROL Save]**.

### Behörigheter - definitioner

En beskrivning av [!UICONTROL Offer Management] behörigheter som är tillgängliga för produktprofiler i [!UICONTROL Admin Console].

| Element | Beskrivning |
|--- |--- |
| Skapa och redigera erbjudanden | Ger användarna möjlighet att skapa och redigera erbjudanden i [!UICONTROL Offer Management]. Om en användare har den här behörigheten men inte _behörigheten Godkänn erbjuder_ , kan användaren bara skapa ett erbjudande och skicka det för godkännande. Den kan inte användas i en erbjudandeaktivitet förrän den har godkänts. |
| Ta bort erbjudanden | Ger användarna åtkomst till raderade erbjudanden. |
| Godkänn erbjudanden | Ger användarna möjlighet att godkänna ett erbjudande. Användare med den här behörigheten får ett meddelande när de loggar in på Offer Management om erbjudanden behöver godkännas. Om en användare har både den här behörigheten och _skaps- och redigeringsbehörigheten_ kan han/hon skapa och godkänna erbjudanden i ett enda arbetsflöde. |
| Arkivera erbjudanden | Ger användarna möjlighet att arkivera ett erbjudande. |
| Skapa etiketter | Ger användarna möjlighet att skapa etiketter, både på fliken Etikett och i presentationsfönstret. Utan den här behörigheten kan en användare bara välja redan skapade erbjudanden när han eller hon skapar ett erbjudande. |
| Redigera etiketter | Ger användaren möjlighet att redigera etiketter på fliken Etiketter. |
| Ta bort etiketter | Ger användaren möjlighet att ta bort etiketter på fliken Etiketter. |
| Skapa placeringar | Ger användaren möjlighet att skapa placeringar på fliken Placeringar. |
| Redigera placeringar | Ger användaren möjlighet att redigera placeringar på fliken Placeringar. |
| Ta bort placeringar | Ger användaren möjlighet att ta bort placeringar på fliken Placeringar. **Obs!** Det går endast att ta bort placeringar som inte används i en erbjudandeaktivitet. |