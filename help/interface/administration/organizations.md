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
source-git-commit: f83ddfe82a55c6b88cf35a14b030d9b82c17f16d
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 3%

---

# Organisationer i Experience Cloud

En *organisation* (Org ID) är den entitet som gör det möjligt för en administratör att konfigurera grupper och användare samt att styra enkel inloggning i Experience Cloud.

Organisationen fungerar som ett inloggningsföretag som omfattar alla Experience Cloud-produkter och program. Oftast är en organisation ditt företagsnamn. Ett företag kan dock ha många organisationer.

![Experience Cloud-organisationer](../assets/organizations-menu.png)

Om du vill verifiera att du har loggat in i rätt organisation klickar du på **[!UICONTROL Profile]** för att visa standardorganisationsnamnet. Om du har tillgång till mer än en organisation kan du även visa och växla till en annan organisation i sidhuvudsfältet.

>[!NOTE]
>
>Genom att växla mellan olika organisationer får du tillgång till Admin Console för just den organisationen. Om du inte ser önskad organisation kan du behöva begära åtkomst från en administratör i den organisationen. (Om du behöver sammanfoga flera Admin Consoles kontaktar du Adobe kundsupport för hjälp.)

## Federated ID

Om din organisation använder Federated ID:n kan du med Experience Cloud logga in med din organisations enkla inloggning utan att behöva ange din e-postadress och ditt lösenord. Lägg till `#/sso:@domain` i Experience Cloud-URL:en (`https://experience.adobe.com`) för att utföra den här åtgärden.

För en organisation med Federated ID och domänen `adobecustomer.com` anger du URL-länken till `https://experience.adobe.com/#/sso:@adobecustomer.com`. Du kan också gå direkt till ett specifikt program genom att skapa ett bokmärke för den här URL:en, som bifogas med programsökvägen. (För Adobe Analytics, till exempel, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.)

## Visa ditt organisations-ID {#concept_EA8AEE5B02CF46ACBDAD6A8508646255}

Du kan hitta ditt tilldelade organisations-ID i supportsyfte. Du kan verifiera att du är i rätt organisation, eller växla mellan organisationer, med väljaren **[!UICONTROL Organization]** i sidhuvudet.

Organisations-ID är det ID som är kopplat till ditt tilldelade Experience Cloud-företag. Detta ID är en alfanumerisk sträng med 24 tecken, följt av (och måste innehålla) `@AdobeOrg`.

Du kan visa ditt organisations-ID och annan kontoinformation med hjälp av kortkommandot **Ctrl+i** från valfri sida på `https://experience.adobe.com`.

**Om du vill visa ditt organisations-ID**

1. I [Experience Cloud](https://experience.adobe.com) trycker du på **Ctrl+i** på tangentbordet.

   ![Tilldelat organisations-ID](../assets/assigned-organization.png)

1. Under **[!UICONTROL User Information]** söker du efter **[!UICONTROL Current Org ID]** och hittar ditt organisations-ID.

   Administratörer kan också logga in på Admin Console (gå till [https://adminconsole.adobe.com](https://adminconsole.adobe.com)) och visa ditt företags-ID i URL:en.

   I följande URL:

   `https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

   ID:

   `C538193582390300A495CC9@AdobeOrg`

## Länka ett programkonto till en Adobe ID {#task_FD389E78640848919E247AC5E95B8369}

Vanligtvis ger Experience Cloud-administratörer tillgång till program och tjänster. I sällsynta fall kan du länka programinloggningsuppgifter till en Adobe ID.

1. Följ stegen i din e-postinbjudan till Experience Cloud.

1. Logga in med din Adobe ID eller Enterprise ID.

1. Klicka på **[!UICONTROL Application selector]**. ( ![meny](../assets/apps-icon.png)).

   ![Länka ett programkonto till ett Adobe ID](../assets/solutions-active.png)

   De program som du har åtkomst till är färgade.

1. Klicka på önskat program.

   ![Klicka på programmet](../assets/analytics-link-accounts.png)

   Den här typen av meddelande visas om du tillhör rätt grupp (och har behörighet till programmet) men ännu inte har länkat dina kontoinloggningsuppgifter till din Adobe ID.

1. Klicka på **[!UICONTROL Link Account]** och ange dina autentiseringsuppgifter.

## Ange en standardorganisation {#concept_6A191B42A9874A9780882903BA18F071}

Du kan ange en standardorganisation som ska användas när du loggar in.

1. Klicka på **[!UICONTROL Profile]** i sidhuvudet och sedan på Inställningar.

1. Välj en standardorganisation under [!UICONTROL General].


![Redigera profil](../assets/edit-profile.png)

## Felsöka problem med kontolänkning {#concept_DFCB29A3B4834FC59AA29E0BBA301584}

Hjälp om problem som uppstår vid kontolänkning.

Kontolänkning misslyckas oftast eftersom Adobe ID är länkat till en tidigare användare. När kontolänkningen misslyckas kan du:

* [Kontakta Adobe support](https://experienceleague.adobe.com/sv?support-solution=General#support).
* Använd standardinloggningen när problemet är löst.
