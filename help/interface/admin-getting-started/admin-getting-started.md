---
description: Ta reda på hur du hanterar användarbehörigheter och produktprofiler för Adobe Experience Cloud. Läs om hur du loggar in på Adobe Admin Console och webbläsarstöd för Experience Cloud.
solution: Admin
title: 'Hantering av användare och produkter '
index: true
feature: Admin Console
topic: Administration
role: Administrator
level: Experienced
translation-type: tm+mt
source-git-commit: 61d60273e933c637dfe4400da78257e1c80015b3
workflow-type: tm+mt
source-wordcount: '1395'
ht-degree: 5%

---


# Hantera Experience Cloud-användare och -produkter {#topic_3FCB4099640647E3B2411ADBFCE81909}

Lär dig mer om att logga in på Admin Console, hantera användarbehörigheter och produktprofiler för Experience Cloud samt webbläsarstöd.

>[!IMPORTANT]
>
>När du hanterar användare i Admin Console introduceras nya termer, gränssnitt och navigering. Följande information beskriver dessa ändringar och innehåller länkar till ytterligare hjälpresurser. Den här hjälpen kompletterar informationen i [användarhandboken för företagsadministration](https://helpx.adobe.com/enterprise/managing/user-guide.html) för alla molnprodukter från Adobe.

## Nyheter i användarhantering för Experience Cloud {#concept_06A0A13362F644FB90F947238407637A}

Läs om de senaste funktionerna för användare och produkthantering i Experience Cloud.

<!-- ### Business ID type

Adobe is introducing an identity type called Business ID. This identity type improves the control of user and product management. Adobe is migrating all Adobe IDs (owned by individuals) that are used for business to the new enterprise Business IDs owned by your organization.

If you are an existing Experience Cloud customer, Adobe will migrate all your users with Adobe IDs in the Admin Console to Business IDs. If you are a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID.

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a user was a member of multiple organizations before the migration.)

Beginning May 2020, enterprise administrators cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM-->

### Administratörsverktyg

Administratörer kan visa en sorterbar och filterbar lista över alla Experience Cloud-användare och deras information i Admin Tool. Se [Visa Experience Cloud-användare i Admin Tool](admin-tool-experience-cloud.md).

## Logga in på Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

Administratörer hanterar inte längre användare i specifika produktlösningar. Användar- och produkthantering för Experience Cloud finns nu i Admin Console.

Så här loggar du in på Admin Console:

1. Navigera till [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. Skriv ditt [Adobe ID eller Enterprise ID](https://helpx.adobe.com/enterprise/help/identity.html) och lösenord.

Du kan också gå till Experience Cloud-menyn ( ![](assets/menu-icon.png)) och klicka på **[!UICONTROL Administration]** > **[!UICONTROL Launch Admin Console]**.

**Relaterad hjälp**

[Administrationsanvändarhandbok ](https://helpx.adobe.com/se/enterprise/using/users.html) för Creative Cloud och Document Cloud. Viss information är relevant för användarhantering i Experience Cloud, till exempel [hantering av identitetstyper](https://helpx.adobe.com/enterprise/help/identity.html).

[Logga in och hantera dina profilinställningar](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0).

## Produktprofiler och grupper {#section_AB50558124D541CF80A0D3D76D35A4BF}

Tillägget av produktprofiler innebär en förändring från hur produkter och tjänster tidigare hanterades (med grupper). I Admin Console baseras behörigheter på produktprofiler, som är grupper av produkter och tjänster som du kan tilldela användare.

I Analytics kan du till exempel konfigurera en samling rapporteringsverktyg, som Analysis Workspace och Report Builder, tillsammans med rapportsviter, mätvärden, dimensioner och så vidare. Du kan ge användare behörighet till en produktprofil genom att lägga till dem i profilen. Se [Tilldela behörigheter för analysåtkomst till en produktprofil](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) på den här sidan.

**Delegera administrativa rättigheter**

Se [Delegera begränsad administrationsbehörighet](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E) på den här sidan.

## Analytics{#section_97DE101F92CD494AB073893680992F1A} 

Hantera användar- och produktbehörigheter för Analytics i Admin Console.

[Tilldela behörigheter för Analytics-åtkomst till en produktprofil](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) (på den här sidan).

**Migrering av användarkonto**

Det finns ett verktyg för migrering av användar-ID:n i Analytics som kan hjälpa Analytics-administratörer att migrera användarkonton från Analytics-användarhantering till [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/).

Kontomigreringen introduceras till kunder i faser. Adobe meddelar och hjälper dig när det är dags att migrera befintliga användarkonton från **[!UICONTROL Admin Tools]** > **[!UICONTROL User Management]** till Admin Console.

Efter migreringen loggar användare in med sin Adobe ID (eller Enterprise ID) och autentiserar till sina Experience Cloud-lösningar och -tjänster på [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com). Om användare försöker logga in via äldre inloggningar ([!DNL my.omniture.com] och [!DNL sc.omniture.com]) dirigeras de om till [!DNL experiencecloud.adobe.com].

**Relaterad hjälp**

[Migrering av användar-ID för analyser](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Adobe Target - produktprofiler jämfört med arbetsytor {#section_3860AF177C9E4C7E9C390D36A414F353}

I Adobe Target är en arbetsyta en produktprofil. Det gör att en organisation kan tilldela en viss uppsättning användare till en viss uppsättning egenskaper. På många sätt liknar en arbetsyta en rapportserie i Adobe Analytics.

Se:

* [Enterprise-användarbehörigheter](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html)
* [Hantera produkter och profiler](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* Video: [Konfigurera Adobe Target Workspaces i Adobe Admin Console](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Kampanj - produktprofiler, innehavare och säkerhetsgrupper {#section_09CDF75366444CF5810CF321B7C712F3}

En *klientorganisation* i Campaign visas som en *produkt* på Admin Console-produktsidan.

*Säkerhetsgrupper* visas som en produktprofil.

Se [Hantera grupper och användare](https://helpx.adobe.com/campaign/standard/administration/using/managing-groups-and-users.html) för information om säkerhetsgrupper och hur du tilldelar användare till säkerhetsgrupper.

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Launch visas på sidan Produkter i Admin Console. Du kan inkludera andra lösningar och tjänster i en Launch-produktprofil.

Se [Användarhantering](https://docs.adobelaunch.com/launch-reference/administration/user-permissions) om du vill ha information om användarbehörigheter i Admin Console och ange startspecifika alternativ, inklusive tilldelning av behörigheter till profiler.

## Experience Manager as a Cloud Service

Adobe Enterprise-kunder representeras som IMS-organisationer i Adobe Admin Console. Det här är den portal som Adobe-kunder använder för att hantera sina produkträttigheter för användare och grupper. AEM kan använda Adobe Admin Console för att hantera sina produkträttigheter och IMS-autentisering AEM som en Cloud Service.

Se [IMS-stöd för AEM som en Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/security/ims-support.html#managing-products-and-user-access-in-admin-console).

## Experience Platform Launch {#section_3A41CF2BD5994B9891537D063571D4ED}

Bjud in användare till [!UICONTROL Platform Launch] och tilldela användarroller och rättigheter.

Se [Användarbehörigheter](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html?lang=en#admin).

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Skapa Audience Manager-användare och tilldela dem till grupper. Du kan också visa gränser (egenskaper, segment, mål och [!DNL AlgoModel]).

Se [Administration](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) i hjälpen för Audience Manager.

## Hantera Experience Cloud-produkter {#task_16335111C52D40E9BAC73D0699584DBF}

Skapa en produktprofil och tilldela den till en behörighetsgrupp.

När du bjuder in en användare till en organisation kan du ge användaren tillgång till produkter och produktprofiler. Du kan även delegera begränsade administrativa behörigheter till en användare. På samma sätt kan du skapa användargrupper och sedan lägga till gruppen i en produktprofil för att aktivera åtkomst.

1. Klicka på **[!UICONTROL Products]** i [Admin Console](https://adminconsole.adobe.com/enterprise/).
1. Klicka på **[!UICONTROL New Profile]**.
1. Konfigurera profilinformationen och klicka sedan på **[!UICONTROL Next]**.
1. Klicka på **[!UICONTROL Done]**.

Mer hjälp finns här:

* [Hantera produkter och profiler](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* [Enterprise User ](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html) Permission i Adobe Target - hjälp för mer information.
* Video: [Konfigurera Adobe Target Workspaces i Adobe Admin Console](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Tilldela behörigheter för Analytics-åtkomst till en produktprofil {#task_040673FE3E3E429B9531FBCB8B6A4391}

Tilldela åtkomstbehörigheter för analysrapporter (rapportsviter, mätvärden, dimensioner och så vidare) till en produktprofil.

Du kan till exempel skapa en produktprofil som innehåller flera analysverktyg ( [!UICONTROL Analysis Workspace], [!UICONTROL Reports & Analytics] och [!UICONTROL Report Builder]), med behörighet till specifika mått och mått (inklusive eVars) och funktioner som att skapa segment eller beräknade värden.

1. Logga in på [Admin Console](https://adminconsole.adobe.com/enterprise) och klicka sedan på **[!UICONTROL Products]** (eller klicka på ditt produktnamn).
1. Klicka på **[!UICONTROL Permissions]** (endast tillgängligt för administratörer) i produktprofilen.
1. Konfigurera profilens behörigheter:

| Element | Beskrivning |
|--- |--- |
| Rapportsviter | Aktivera behörigheter för specifika rapportsviter. |
| Mätvärden | Aktivera behörigheter för trafik, konvertering, anpassade händelser, lösningshändelser, innehållsmedveten osv. |
| Mått | Anpassa användaråtkomsten på detaljnivå, inklusive eVars, trafikrapporter, lösningsrapporter och sökvägsrapporter. |
| Report Suite-verktyg | Aktivera användarbehörigheter för Web Services, Report Suite Management, Tools and Reports och Dashboard Items. |
| Analysverktyg | Aktivera användarbehörigheter för allmänna objekt (fakturering, loggar osv.), företagshantering, verktyg, webbtjänståtkomst, Report Builder och integrering med Data Connectors. Företagsinställningar från kategorin Anpassa Admin Console har flyttats till Analytics-verktyg. |

## Delegera administrativa roller till användare {#task_3A072C4AA9734BC59FFA7E015271BC7E}

I Admin Console kan du delegera begränsade administrativa rättigheter till andra i organisationen. Delegerade roller gör det möjligt för användare att administrera programåtkomst till slutanvändare, ge åtkomst till distributionsfunktioner och fungera som supportrepresentanter.

Du kan till exempel:

* Ge din creative director åtkomst till Creative Cloud.
* Tillåt marknadsföringschefen att ge åtkomst till Experience Cloud.
* Håll de här två rollerna åtskilda så att de inte kan överlappa varandras roller.

Genom att använda de här rollerna kan du delegera hantering till andra utan att ge dem mer kapacitet än de behöver.

1. Klicka på **[!UICONTROL Users]** i Admin Console och sedan på användarens namn.
1. Klicka på **[!UICONTROL Edit admin rights]**.
1. Konfigurera användarens administratörsrättigheter.
1. Klicka på **[!UICONTROL Next]** för att granska inställningarna och klicka sedan på **[!UICONTROL Save]**.

## Webbläsare som stöds och systemkrav {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Webbläsare som stöds i Experience Cloud.

* [!DNL Microsoft Edge] (Microsoft har  [avslutat ](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) stödet för Internet Explorer 8, 9 och 10. Adobe kommer därför inte att åtgärda problem som rapporterats mot dessa specifika versioner av Internet Explorer.)
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**Obs!** Även om Experience Cloud-gränssnittet har stöd för dessa webbläsare kanske inte enskilda lösningar har stöd för alla webbläsare. (Till exempel stöder [Analytics](https://docs.adobe.com/content/help/sv-SE/analytics/admin/sys-reqs.html) inte [!DNL Opera] och [Adobe Target](https://docs.adobe.com/help/sv-SE/target/using/implement-target/before-implement/supported-browsers.html) inte [!DNL Safari].)

### Lösningar och produktkrav

* [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html) 
* [Report Builder](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html)
