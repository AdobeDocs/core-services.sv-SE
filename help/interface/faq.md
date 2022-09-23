---
description: Läs mer om webbläsarstöd och få svar på vanliga frågor för administratörer i Adobe Experience Cloud.
solution: Experience Cloud
title: Frågor och svar om Experience Cloud
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 062576da-328e-4b46-9e71-5a25733d607a
source-git-commit: eb2ad8a8255915be47b6002a78cc810b522170d2
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 2%

---

# Frågor och svar om Experience Cloud

Läs mer om webbläsarstöd och vanliga frågor och svar för administratörer i Experience Cloud.

## Vilka webbläsare stöds i Experience Cloud?

* Microsoft® Edge (nuvarande och två bakomliggande versioner)
* Google Chrome (aktuell och två bakåtkompatibla versioner)
* Mozilla Firefox (aktuell och två bakåtkompatibla versioner)
* Safari (nuvarande och två bakomliggande versioner)
* Opera (aktuell och två bakåtkompatibla versioner)

## Hur vet jag om mina program är aktiverade för bastjänster?

Om implementeringen inte har etablerats för bastjänsterna finns mer information i [Aktivera era program för bastjänster](core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)som beskriver hur du:

1. [Gå med i Experience Cloud och bli administratör](core-services.md#section_2423F0BD3DF642658103310EE5EA6154)
1. [Implementera Experience Cloud ID-tjänsten med Experience Platform Launch](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html?lang=en).
1. [Mappa rapportsviter till en Experience Cloud-organisation](core-services.md#concept_apg_zq2_rw)
1. [(Endast analys) Modernisera AppMeasurement Code för analyser](core-services.md#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [(Endast Adobe Target) Modernisera implementeringen av Adobe Target](core-services.md#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [Verifiera implementeringen](core-services.md#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [Hantera användare och produkter](core-services.md#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [Börja använda bastjänsterna](core-services.md#section_960C06093623462E8EA247B3E97274A1)

Mer hjälp får du om du [Kontakta Adobe support](https://experienceleague.adobe.com/?support-solution=General#support).

## Tar Adobe mitt företag betalt för Experience Cloud?

Nej. Experience Cloud ingår utan extra kostnad. Vissa bastjänster kan dock medföra extrakostnader.

## Varför måste mitt företag logga in via Experience Cloud-gränssnittet?

De funktioner som finns i gränssnittet Experience Cloud ger ditt företag ett mervärde. Det är också standardsökvägen för att komma åt program som går framåt och som till slut ersätter andra inloggningsflöden för enskilda program. Inloggning via Experience Cloud underlättar en smidigare övergång senare.

## Hur löser jag problemen med att migrera mitt företag?

[Kontakta Adobe support](https://experienceleague.adobe.com/?support-solution=General#support).

## Hur kan [!DNL Adobe Support] i molnmiljön i Adobe kan du felsöka ett problem -

[!DNL Adobe Support] kan skicka in en personifieringsbegäran som du får ett Adobe-märkt e-postmeddelande för (exempel nedan) som efterfrågar din uttryckliga behörighet. Åtkomsten beviljas för en begränsad tid. När åtkomsten har beviljats kan du återkalla den när som helst. Adobe loggar alla åtgärder som vidtas av företrädare för Adobe.

![Adobe supportärende](assets/support-email.png)

## Vad är _etablering?_

Med tillhandahållande i Experience Cloud avses

* Dina användare kan börja logga in på [!DNL Experience Cloud] och länka program.
* De kan börja använda de funktioner som är tillgängliga via Experience Cloud, till exempel Personer.
* Du kan bli redo att avsluta din programspecifika inloggningsprocess.
* Du kan behålla åtkomstkontroll för program.

## Hur hanterar jag användare och produktprofiler?

* Se [Användarhandbok för Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html) om du behöver hjälp.

* Användarrättigheter och produkthantering utförs i [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) (produktlänk).

* **Viktigt:** Analysadministratörer, se [Hantera analysanvändare i Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/migrate-users/c-migration-tool.html?lang=en) om hur du migrerar användar-ID:n från administrationsverktygen för Analytics till Admin Console.

## Vad gör jag om någon inte kan logga in på Experience Cloud?

Admin Console-administratörer kan ge användare åtkomst. Användarna får e-post med inloggningsinstruktioner.

Du kanske måste [Kontakta Adobe support](https://experienceleague.adobe.com/?support-solution=General#support) för att verifiera att ditt företag har etablerats fullständigt.

## Var kan en användare gå för att hantera kontolänkning?

Vissa användare kan behöva länka sitt programkonto (Analytics) till Adobe ID eller Enterprise ID.

Se [Länka ett programkonto till en Adobe ID](organizations.md#task_FD389E78640848919E247AC5E95B8369).

## Hur hanterar jag profiler och organisationer för användarkonton?

Se [Hantera användarkonton](organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1).

## Vad är en organisation?

An [organisation](organizations.md) är den enhet som gör det möjligt för en administratör att konfigurera grupper och användare samt att styra enkel inloggning i Experience Cloud. Organisationen fungerar som ett inloggningsföretag som omfattar alla produkter och program i Experience Cloud. Oftast är en organisation ditt företagsnamn. Ett företag kan dock ha många organisationer.

## Var hittar jag mitt IMS-organisations-ID?

Se [Visa ditt organisations-ID](organizations.md) för mer information.

## Vad ska jag göra när någon av mina användare lämnar mitt företag?

Deras åtkomst bör tas bort från själva programmet. De kommer inte att kunna komma åt produkten från Experience Cloud eller via inloggningen direkt. Du bör även ta bort dem på Experience Cloud-nivå.

## Vad är en Adobe ID?

Se [Identitetstyper](https://helpx.adobe.com/enterprise/using/identity.html).

## Kan jag länka programkonton till mina användare?

Nej. Användarna måste länka sina egna program med sina användarnamn och lösenord.

## Varför ser jag Social när mitt företag inte har det?

Adobe Social är en produkt som kan säljas med Analytics. Om du har Analytics kommer du att se det här programmet, men du kommer inte att ha tillgång till det om du inte har köpt det.
