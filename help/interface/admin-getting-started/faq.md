---
description: Vanliga frågor och svar för administratörer i Experience Cloud.
keywords: core services
seo-description: Vanliga frågor och svar för administratörer i Experience Cloud.
seo-title: Frågor och svar
solution: Experience Cloud
title: Frågor och svar
uuid: 3ed0b4eb-690f-4c14-a31c-0cc1118fb3b4
translation-type: tm+mt
source-git-commit: d225ef8800228d35c1920904f6fe7590bd751de3

---


# Frågor och svar

Vanliga frågor och svar för administratörer i Experience Cloud.

**Hur vet jag om mina lösningar är aktiverade för bastjänster?**

Om implementeringen inte har etablerats för bastjänster, se [Aktivera lösningar för bastjänster](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C), som beskriver hur du:

1. [Gå med i Experience Cloud och bli administratör](../core-services/core-services.md#section_2423F0BD3DF642658103310EE5EA6154)
1. [Implementera Experience Cloud ID-tjänsten med Dynamic Tag Manager](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354) (eller den nya [Experience Platform Launch](https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html))
1. [Mappa rapportsviter till en Experience Cloud-organisation](../core-services/core-services.md#concept_apg_zq2_rw)
1. [(Endast analys) Modernisera AppMeasurement Code för analyser](../core-services/core-services.md#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [(Endast Target) Modernisera implementeringen av Adobe Target](../core-services/core-services.md#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [Verifiera implementeringen av bastjänsterna](../core-services/core-services.md#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [Hantera användare och produkter](../core-services/core-services.md#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [Börja använda bastjänsterna](../core-services/core-services.md#section_960C06093623462E8EA247B3E97274A1)

Om du behöver mer hjälp [kontaktar du Adobes support](https://helpx.adobe.com/marketing-cloud/contact-support.html).

**Tar Adobe betalt av mitt företag för Experience Cloud-åtkomst?**

Nej. Experience Cloud ingår utan extra kostnad. Vissa bastjänster kan dock medföra extrakostnader.

**Varför måste mitt företag logga in via Experience Cloud-gränssnittet?**

De funktioner som finns i Experience Cloud-gränssnittet ger ert företag ett mervärde. Det kommer också att vara standardvägen för att komma åt lösningar som går framåt och som så småningom ersätter andra inloggningsflöden för enskilda lösningar. Logga in via Experience Cloud för att underlätta en smidigare övergång senare.

**Hur löser jag problemen med att migrera mitt företag?**

[Kontakta Adobes support](https://helpx.adobe.com/marketing-cloud/contact-support.html).

**Vad är _etablering?_**

Med provisionering i Experience Cloud avses följande:

* Dina användare kan börja logga in på [!DNL Experience Cloud] och länka lösningar.
* De kan börja använda de funktioner som är tillgängliga via Experience Cloud, till exempel Personer.
* Du kan bli redo att dra tillbaka den lösningsspecifika inloggningsprocessen.
* Ni kan behålla kontrollen över lösningarna.

**Hur hanterar jag användare och produktprofiler?**

* Mer information finns i användarhandboken [för](https://helpx.adobe.com/enterprise/administering/user-guide.html) Admin Console.

* Användarrättigheter och produkthantering utförs i [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) (produktlänk).

* **Viktigt:** Analysadministratörer kan läsa [Hantera Analytics-användare på Admin Console](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html) om hur du migrerar användar-ID:n från Analytics Admin Tools till Admin Console.

**Vad gör jag om någon inte kan logga in på Experience Cloud?**

Administratörer för Admin Console kan ge användare åtkomst. Användarna får e-post med inloggningsinstruktioner.

Du kan behöva [kontakta Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) för att kontrollera att ditt företag har etablerats helt.

**Var kan en användare gå för att hantera kontolänkning?**

Vissa användare kan behöva länka sitt lösningskonto (Analytics) till Adobe ID:t eller Enterprise ID:t.

Se [Länka ett lösningskonto till ett Adobe ID](../admin-getting-started/organizations.md#task_FD389E78640848919E247AC5E95B8369).

**Hur hanterar jag profiler och organisationer för användarkonton?**

Se [Hantera användarkonton](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1).

**Vad är en organisation?**

En *organisation* är den enhet som gör det möjligt för en administratör att konfigurera grupper och användare samt att styra enkel inloggning i Experience Cloud. Organisationen fungerar som ett inloggningsföretag som omfattar alla Experience Cloud-produkter och -lösningar. Oftast är en organisation ditt företagsnamn. Ett företag kan dock ha många organisationer.

**Var hittar jag mitt IMS-organisations-ID?**

Se [Hitta ditt företags-ID](organizations.md).

Organisations-ID:t visas på landningssidan för Experience Cloud och på landningssidan [för](https://adminconsole.adobe.com)Admin Console.

Administratörer kan också logga in på Admin Console (gå till [https://adminconsole.adobe.com](https://adminconsole.adobe.com#)) för en viss organisation, och du kan se ditt IMS-organisations-ID i URL:en.

I följande URL:

`https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

ID:t är:

`C538193582390300A495CC9@AdobeOrg`

**Vad ska jag göra när någon av mina användare lämnar mitt företag?**

Deras åtkomst bör tas bort från själva lösningen. De kommer inte att kunna komma åt produkten från Experience Cloud eller via den direkta inloggningen. Du bör också ta bort dem på Experience Cloud-nivå.

**Vad är ett Adobe-ID?**

Se [Identitetstyper](https://helpx.adobe.com/enterprise/help/identity.html).

**Kan jag länka lösningskonton för mina användare?**

Nej. Användarna måste länka sina egna lösningar till sina användarnamn och lösenord.

**Varför ser jag Social när mitt företag inte har det?**

Adobe Social är en produkt som kan säljas med Analytics. Om ni har Analytics kommer ni därför att se den här lösningen, men ni kommer inte att ha tillgång till den om ni inte har köpt den.