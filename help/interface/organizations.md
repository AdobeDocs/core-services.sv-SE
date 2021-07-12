---
description: Läs mer om organisationer och länkning av lösningskonton till Experience Cloud.
keywords: Adobe Experience Cloud-tjänster
solution: Experience Cloud
title: 'Organisationer och kontolänkning '
uuid: ae47ad18-ac33-4efa-8b68-2bfaf77397aa
feature: Admin Console
topic: Administrering
role: Admin
level: Experienced
exl-id: 6eb58530-2a7a-48c7-9a5b-48a6e980a034
source-git-commit: 1fb1abc7311573f976f7e6b6ae67f60ada10a3e7
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 8%

---

# Organisationer och kontolänkning

Lär dig hur du hanterar organisationer och länkar lösningskonton till Experience Cloud.

## Identifiera er organisation {#concept_384D169B0B724B799D573B8ECB5C39BF}

En *organisation* är den enhet som gör det möjligt för en administratör att konfigurera grupper och användare samt att styra enkel inloggning i Experience Cloud. Organisationen fungerar som ett inloggningsföretag som omfattar alla produkter och lösningar i Experience Cloud. Oftast är en organisation ditt företagsnamn. Ett företag kan dock ha många organisationer.

Du kan också behöva hitta ditt organisations-ID för support. Du kan verifiera att du är i rätt organisation, eller växla mellan organisationer, via menyn **[!UICONTROL Organization]**.

![Stegresultat](assets/organization-switch.png)

## Hitta ditt företags-ID {#concept_EA8AEE5B02CF46ACBDAD6A8508646255}

**Organisations-ID** är det ID som är associerat med ditt tilldelade Experience Cloud-företag. Detta ID är en alfanumerisk sträng med 24 tecken, följt av (och måste innehålla) @AdobeOrg.

Om du vill visa ditt organisations-ID går du till startsidan för Experience Cloud eller väljer ( ![](assets/menu-icon.png)) och sedan **[!UICONTROL Administration]**. Du kan hitta organisations-ID:t längst ned på sidan [!UICONTROL Getting Started with the Experience Cloud] eller på sidan [!UICONTROL Administration].

![](assets/administration-page.png)

## Länka ett lösningskonto till en Adobe ID {#task_FD389E78640848919E247AC5E95B8369}

Administratörer i Experience Cloud ger oftast tillgång till lösningar och tjänster. I sällsynta fall kan du behöva länka autentiseringsuppgifterna för lösningen till en Adobe ID.

1. Följ stegen i din e-postinbjudan till Experience Cloud.
1. Logga in med ditt Adobe ID eller Enterprise ID.
1. Välj lösningsväljaren. ( ![](assets/menu-icon.png)).

   ![](assets/solutions-active.png)

   De lösningar du har tillgång till är färglagda.
1. Välj önskad lösning.

   ![](assets/analytics-link-accounts.png)

   Den här typen av meddelande visas om du tillhör rätt grupp (och har behörighet till lösningen) men ännu inte har länkat dina kontoinloggningsuppgifter till din Adobe ID.
1. Välj **[!UICONTROL Link Account]** och ange dina autentiseringsuppgifter.

## Ange en standardorganisation och landningssida {#concept_6A191B42A9874A9780882903BA18F071}

Du kan ange vilken standardorganisation och landningssida som ska användas när du loggar in.

Välj **[!UICONTROL Edit Profile]** i din profil.

![](assets/edit-profile.png)

Under Standardsida för organisation och landning kan du anpassa din inloggningsupplevelse.

![](assets/default-organization.png)

## Felsöka problem med kontolänkning {#concept_DFCB29A3B4834FC59AA29E0BBA301584}

Hjälp om problem som uppstår vid kontolänkning.

Kontolänkning misslyckas oftast eftersom Adobe ID är länkat till en tidigare användare. När kontolänkningen misslyckas kan du:

* [Kontakta supporten för](https://experienceleague.adobe.com/?support-solution=General#support) Adobe.
* Använd standardinloggningen när problemet är löst.
