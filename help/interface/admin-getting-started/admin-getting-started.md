---
description: Lär dig hur du loggar in på Admin Console, hanterar användarbehörigheter och produktprofiler för Experience Cloud samt webbläsarstöd.
keywords: core services
seo-description: Lär dig hur du loggar in på Admin Console, hanterar användarbehörigheter och produktprofiler för Experience Cloud samt webbläsarstöd.
seo-title: Hantera Experience Cloud-användare och -produkter
solution: Experience Cloud
title: Hantera Experience Cloud-användare och -produkter
uuid: aea4e4c3-f543-4e8d-b553-d838418477d6
translation-type: tm+mt
source-git-commit: 5e57aedb38e6914f7e99b1b26df9e4bb52b9e13d

---


# Hantera Experience Cloud-användare och -produkter {#topic_3FCB4099640647E3B2411ADBFCE81909}

Lär dig hur du loggar in på Admin Console, hanterar användarbehörigheter och produktprofiler för Experience Cloud samt webbläsarstöd.

>[!IMPORTANT]
>
>När du hanterar användare på Admin Console introduceras nya termer, gränssnitt och navigering. Följande information beskriver dessa ändringar och innehåller länkar till ytterligare hjälpresurser. Den här hjälpen kompletterar informationen i [Enterprise Administration User Guide](https://helpx.adobe.com/enterprise/managing/user-guide.html) för alla Adobe-molnprodukter.

## Nyheter i Experience Cloud-användarhantering {#concept_06A0A13362F644FB90F947238407637A}

Läs om de senaste funktionerna i Experience Cloud-användarhantering.

## Logga in på Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

Administratörer hanterar inte längre användare i lösningar. Användar- och produkthantering för Experience Cloud finns nu i Admin Console.

**Logga in på Admin Console**

1. Gå till [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. Skriv ditt [Adobe-ID eller Enterprise-ID](https://helpx.adobe.com/enterprise/help/identity.html) och lösenord.

Du kan också gå till Experience Cloud-menyn ( ![](assets/menu-icon.png)) och klicka på **[!UICONTROL Administration]** > **[!UICONTROL Launch Admin Console]**.

**Relaterad hjälp**

[Användarhandbok](https://helpx.adobe.com/enterprise/using/users.html) för administration av Creative Cloud och Document Cloud. Viss information är relevant för Experience Cloud-användarhantering, till exempel [hantering av identitetstyper](https://helpx.adobe.com/enterprise/help/identity.html).

[Logga in och hantera dina profilinställningar](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0) för att hantera lösenord, organisationer och meddelanden.

## Produktprofiler och produktgrupper {#section_AB50558124D541CF80A0D3D76D35A4BF}

Tillägget av produktprofiler innebär en förändring från hur produkter och tjänster tidigare hanterades (med grupper). I Admin Console baseras behörigheter på produktprofiler, som är grupper av produkter och tjänster som du kan tilldela användare.

I Analytics kan du till exempel konfigurera en samling rapporteringsverktyg, som Analysis Workspace och Report Builder, tillsammans med rapportsviter, mått och så vidare. Du kan ge användare behörighet till en produktprofil genom att lägga till dem i profilen. Se [Tilldela behörigheter för Analytics-åtkomst till en produktprofil](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391).

**Relaterad hjälp**

[Delegera begränsade administrationsbehörigheter](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analyser {#section_97DE101F92CD494AB073893680992F1A}

Hantera användar- och produktbehörigheter för Analytics i Admin Console.

[Tilldela behörigheter för Analytics-åtkomst till en produktprofil](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)(på den här sidan).

**Migrering av användarkonto**

Det finns ett verktyg för migrering av användar-ID:n i Analytics som kan hjälpa Analytics-administratörer att migrera användarkonton från Analytics-användarhantering till [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/).

Kontomigreringen introduceras till kunder i faser. Adobe meddelar och hjälper dig när det är dags att migrera befintliga användarkonton från **[!UICONTROL Admin Tools]** > **[!UICONTROL User Management]** till Admin Console.

Efter migreringen loggar användare in med sitt Adobe ID (eller Enterprise ID) och autentiserar sig med sina Experience Cloud-lösningar och -tjänster på [experienceCloud.adobe.com](https://experiencecloud.adobe.com). Om användare försöker logga in via äldre inloggningar ([!DNL my.omniture.com] och [!DNL sc.omniture.com]) dirigeras de om till [!DNL experiencecloud.adobe.com].

**Relaterad hjälp**

[Migrering av användar-ID för analyser](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Mål - produktprofiler jämfört med arbetsytor {#section_3860AF177C9E4C7E9C390D36A414F353}

I Target är en arbetsyta en produktprofil. Det gör att en organisation kan tilldela en viss uppsättning användare till en viss uppsättning egenskaper. På många sätt liknar en arbetsyta en rapportserie i Adobe Analytics.

Se:
* [Enterprise-användarbehörigheter](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html)
* [Hantera produkter och profiler](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* Video: Konfigurera [målarbetsytor i Adobe Admin Console](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Campaign - produktprofiler, hyresgäster och säkerhetsgrupper {#section_09CDF75366444CF5810CF321B7C712F3}

En *klientorganisation* i Campaign visas som en *produkt* på sidan Produkter i Admin Console.

*Säkerhetsgruppen* visas som en produktprofil.

Mer information om säkerhetsgrupper och hur du tilldelar användare till säkerhetsgrupper finns i [Hantera grupper och användare](https://helpx.adobe.com/campaign/standard/administration/using/managing-groups-and-users.html) .

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Launch visas på sidan Produkter i Admin Console. Du kan inkludera andra lösningar och tjänster i en Launch-produktprofil.

Se [Användarhantering](https://docs.adobelaunch.com/launch-reference/administration/user-permissions) för information om användarbehörigheter i Admin Console och ange startspecifika alternativ, inklusive tilldelning av behörigheter till profiler.

## Dynamisk tagghanterare {#section_3A41CF2BD5994B9891537D063571D4ED}

Bjud in användare till dynamisk tagghantering och tilldela användarroller och lägg till användare i grupper.

Mer information om hur du bjuder in användare till dynamisk tagghantering och tilldelar användarroller och lägger till användare i grupper finns i [Användare och behörigheter](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) .

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Skapa Audience Manager-användare och tilldela dem till grupper. Du kan också visa begränsningar (egenskaper, segment, mål och AlgoModel).

Se [Administration](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) i hjälpen för Audience Manager.

## Hantera Experience Cloud-produkter {#task_16335111C52D40E9BAC73D0699584DBF}

Skapa en produktprofil och tilldela den till en behörighetsgrupp.

När du bjuder in en användare till en organisation kan du ge användaren tillgång till produkter och produktprofiler. Du kan även delegera begränsade administrativa behörigheter till en användare. På samma sätt kan du skapa användargrupper och sedan lägga till gruppen i en produktprofil för att aktivera åtkomst.

1. Klicka på [Admin Console](https://adminconsole.adobe.com/enterprise/)**[!UICONTROL Products]**.
1. Klicka på **[!UICONTROL New Profile]**.
1. Konfigurera profilinformationen och klicka sedan på **[!UICONTROL Next]**.
1. Klicka på **[!UICONTROL Done]**.

Mer hjälp finns här:

* [Hantera produkter och profiler](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* [Enterprise User Permissions](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html) in Target help for more information.
* Video: Konfigurera [målarbetsytor i Adobe Admin Console](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Tilldela behörigheter för Analytics-åtkomst till en produktprofil {#task_040673FE3E3E429B9531FBCB8B6A4391}

Tilldela åtkomstbehörigheter för analysrapporter (rapportsviter, mätvärden, dimensioner och så vidare) till en produktprofil.

Du kan till exempel skapa en produktprofil som innehåller flera analysverktyg (, [!UICONTROL Analysis Workspace]och [!UICONTROL Reports & Analytics][!UICONTROL Report Builder]), med behörighet till specifika mått och dimensioner (inklusive eVars) och funktioner som att skapa segment eller beräknade mätvärden.

1. Logga in på [Admin Console](https://adminconsole.adobe.com/enterprise)och klicka sedan på **[!UICONTROL Products]** (eller klicka på ditt produktnamn).
1. Klicka på **[!UICONTROL Permissions]** (endast tillgängligt för administratörer) i produktprofilen.
1. Konfigurera profilens behörigheter:

| Element | Beskrivning |
|--- |--- |
| Rapportsviter | Aktivera behörigheter för specifika rapportsviter. |
| Mått | Aktivera behörigheter för trafik, konvertering, anpassade händelser, lösningshändelser, innehållsmedveten osv. |
| Dimensioner | Anpassa användaråtkomsten på detaljnivå: eVars, trafikrapporter, lösningsrapporter och kundvägsrapporter. |
| Report Suite-verktyg | Aktivera användarbehörigheter för Web Services, Report Suite Management, Tools and Reports och Dashboard Items. |
| Analysverktyg | Aktivera användarbehörigheter för allmänna objekt (fakturering, loggar osv.), företagshantering, verktyg, Web Service Access, Report Builder och integrering med Data Connectors. Företagsinställningar från kategorin Anpassa Admin Console har flyttats till Analytics-verktyg. |

## Delegera administrativa roller till användare {#task_3A072C4AA9734BC59FFA7E015271BC7E}

På Admin Console kan du delegera begränsade administrativa rättigheter till andra i organisationen. Delegerade roller gör det möjligt för användare att administrera programåtkomst till slutanvändare, ge åtkomst till distributionsfunktioner och fungera som supportrepresentanter.

Du kan till exempel:

* Ge din creative director tillgång till Creative Cloud.
* Tillåt marknadsföringschefen att ge åtkomst till Experience Cloud.
* Håll de här två rollerna åtskilda så att de inte kan överlappa varandras roller.

Genom att använda de här rollerna kan du delegera hantering till andra utan att ge dem mer kapacitet än de behöver.

1. I Admin Console klickar du på **[!UICONTROL Users]** och sedan på användarens namn.
1. Klicka på **[!UICONTROL Edit admin rights]**.
1. Konfigurera användarens administratörsrättigheter.
1. Klicka **[!UICONTROL Next]** för att granska inställningarna och klicka sedan på **[!UICONTROL Save]**.

## Webbläsare och systemkrav som stöds {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Webbläsare som stöds i Experience Cloud.

Följande webbläsare stöds i Experience Cloud:

* [!DNL Microsoft Edge] (Microsoft har [upphört med stödet](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) för Internet Explorer 8, 9 och 10. Därför kommer Adobe inte att åtgärda problem som rapporteras mot dessa specifika versioner av Internet Explorer.)
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**Obs!** Trots att Experience Cloud-gränssnittet har stöd för dessa webbläsare kanske inte enskilda lösningar har stöd för alla webbläsare. ( [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html) stöder till exempel inte [!DNL Opera]och [Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html) stöder inte [!DNL Safari].)

**Lösningar och produktkrav**

* [Analyser](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html)
* [Report Builder](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html)