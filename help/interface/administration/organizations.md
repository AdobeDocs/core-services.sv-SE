---
description: Lär dig mer om organisationer (organisations-ID för IMS) och hur du länkar lösningskonton till Experience Cloud.
solution: Experience Cloud
title: Organisationer och kontolänkning
uuid: ae47ad18-ac33-4efa-8b68-2bfaf77397aa
feature: Organizations
topic: Administration
role: Admin
level: Experienced
exl-id: 6eb58530-2a7a-48c7-9a5b-48a6e980a034
source-git-commit: 0724136e77d6fe1341a64aea75051127956df3b2
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 3%

---

# Organisationer i Experience Cloud

En *organisation* (Org ID) är den entitet som gör att en administratör kan konfigurera grupper och användare samt styra enkel inloggning i Experience Cloud.

Organisationen fungerar som ett inloggningsföretag som omfattar alla produkter och program från Experience Cloud. Oftast är en organisation ditt företagsnamn. Ett företag kan dock ha många organisationer.

![Experience Cloud-organisationer](../assets/organizations-menu.png)

Kontrollera att du har loggat in på rätt organisation genom att klicka på din profilavatar för att se organisationens namn. Om du har tillgång till mer än en organisation kan du även visa och växla till en annan organisation i sidhuvudsfältet.

## Federated ID

Om din organisation använder Federated ID:n kan du med Experience Cloud logga in med din organisations enkla inloggning utan att behöva ange din e-postadress och ditt lösenord. Lägg till `#/sso:@domain` i Experience Cloud-URL:en (`https://experience.adobe.com`) för att utföra den här åtgärden.

För en organisation med Federated ID och domänen `adobecustomer.com` anger du URL-länken till `https://experience.adobe.com/#/sso:@adobecustomer.com`. Du kan också gå direkt till ett specifikt program genom att skapa ett bokmärke för den här URL:en, som bifogas med programsökvägen. (För Adobe Analytics, till exempel, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.)

## Visa ditt organisations-ID {#concept_EA8AEE5B02CF46ACBDAD6A8508646255}

Du kan hitta ditt tilldelade organisations-ID i supportsyfte. Du kan verifiera att du är i rätt organisation eller växla mellan organisationer med hjälp av menyn **[!UICONTROL Organization]**.

Organisations-ID är det ID som är kopplat till ditt tilldelade Experience Cloud-företag. Detta ID är en alfanumerisk sträng med 24 tecken, följt av (och måste innehålla) `@AdobeOrg`.

Du kan visa ditt organisations-ID och annan kontoinformation med hjälp av kortkommandot **Ctrl+i** från valfri sida på `https://experience.adobe.com`.

**Om du vill visa ditt organisations-ID**

1. I [Experience Cloud](https://experience.adobe.com) trycker du på **Ctrl+i** på tangentbordet.

   ![Tilldelat organisations-ID](../assets/assigned-organization.png)

1. Under **[!UICONTROL User Information]** söker du efter **[!UICONTROL Current Org ID]** och hittar ditt organisations-ID.

   Administratörer kan också logga in på Admin Console (gå till [https://adminconsole.adobe.com](https://adminconsole.adobe.com)) och visa ditt organisations-ID i URL:en.

   I följande URL:

   `https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

   ID:

   `C538193582390300A495CC9@AdobeOrg`

## Länka ett programkonto till en Adobe ID {#task_FD389E78640848919E247AC5E95B8369}

Administratörer i Experience Cloud ger vanligtvis tillgång till program och tjänster. I sällsynta fall kan du länka programinloggningsuppgifter till en Adobe ID.

1. Följ stegen i din e-postinbjudan till Experience Cloud.

1. Logga in med ditt Adobe ID eller Enterprise ID.

1. Välj programväljaren. ( ![meny](../assets/menu-icon.png)).

   ![Länka ett programkonto till ett Adobe ID](../assets/solutions-active.png)

   De program som du har åtkomst till är färgade.

1. Välj önskat program.

   ![Välj önskat program](../assets/analytics-link-accounts.png)

   Den här typen av meddelande visas om du tillhör rätt grupp (och har behörighet till programmet) men ännu inte har länkat dina kontoinloggningsuppgifter till din Adobe ID.

1. Välj **[!UICONTROL Link Account]** och ange dina autentiseringsuppgifter.

## Ange en standardorganisation och landningssida {#concept_6A191B42A9874A9780882903BA18F071}

Du kan ange vilken standardorganisation och landningssida som ska användas när du loggar in.

Välj **[!UICONTROL Edit Profile]** i din profil.

![Redigera profil](../assets/edit-profile.png)

Under **[!UICONTROL Default Organization & Landing Page]** kan du anpassa din inloggningsupplevelse.

![Standardsida för organisation och landning](../assets/default-organization.png)

## Felsöka problem med kontolänkning {#concept_DFCB29A3B4834FC59AA29E0BBA301584}

Hjälp om problem som uppstår vid kontolänkning.

Kontolänkning misslyckas oftast eftersom Adobe ID är länkat till en tidigare användare. När kontolänkningen misslyckas kan du:

* [Kontakta Adobe support](https://experienceleague.adobe.com/?support-solution=General#support).
* Använd standardinloggningen när problemet är löst.
