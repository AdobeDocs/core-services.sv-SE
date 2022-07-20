---
title: Hantera användare och produkter
description: Läs om hur du loggar in på Admin Console och hanterar användarbehörigheter och produktprofiler för Experience Cloud. Läs om hur du delegerar administratörsrättigheter till Experience Cloud och om webbläsarstöd för Experience Cloud.
solution: Admin
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: af9eda5b-d984-44b7-a7b3-52dfc4e03d8f
source-git-commit: 271d8496ee617f55741cb2e636eecc869e1ec284
workflow-type: tm+mt
source-wordcount: '1846'
ht-degree: 3%

---

# Hantera Experience Cloud-användare och -produkter

Lär dig hur du loggar in på Admin Console, hanterar användarbehörigheter för Experience Cloud och produktprofiler samt webbläsarstöd.

>[!IMPORTANT]
>
>Följande information gäller särskilt för Experience Cloud. Denna information kompletterar den vidare administrativa informationen i [Användarhandbok för företagsadministration](https://helpx.adobe.com/enterprise/admin-guide.html) för alla Adobe molnprodukter.

Du kan visa en sorterbar och filterbar lista över alla Experience Cloud-användare och deras information i Admin Tool. Se [Visa Experience Cloud-användare i administrationsverktyget](admin-tool-experience-cloud.md).

## Etablerar uppdateringsmeddelande{#provisioning}

Uppdaterat: **20 juli 2022**

>[!IMPORTANT]
>
>Läs följande meddelande om etablering av Experience Cloud.

Adobe uppdaterar sin etablering för att ge alla Experience Cloud-kunder tillgång till grundläggande funktioner som underlättar samverkan mellan vissa Experience Cloud-produkter. Adobe Experience Platform läggs till i Experience Cloud-organisationer med [!UICONTROL Data Collection] som en inkluderad tjänst.

Adobe Experience Platform [!UICONTROL Data Collection] inkluderar [taggar](https://experienceleague.adobe.com/docs/tags.html?lang=en) för förenklad universell tagghantering och erbjuder en tillförlitlig, robust och komplett infrastruktur för strömmande data. Taggar förenklar datainsamlingen för kundupplevelsen och effektiviserar leveransen av upplevelser.

**Förändringar i Admin Console**

Administratörer kan se ändringar eller tillägg i Admin Console enligt följande:

* Adobe Experience Platform produktkort i Admin Console kommer att innehålla:

   * Platser
   * Säkerhet
   * Identitetsnamnutrymme
   * Sandlådor
   * Experience Data Model
   * Scheman
   * Datastreams
   * Besökar-ID

   För organisationer som inte använder Experience Platform ser du nu _Adobe Experience Platform_ i Admin Console, inklusive de funktioner som anges ovan.

   För organisationer som för närvarande använder Experience Platform _Platser_ kommer nu att konsolideras i Experience Platform-kortet.

* Adobe Experience Platform Data Collection (tidigare Launch) och Privacy (Privacy) kommer att visas som separata produktkort jämfört med andra Experience Platform-funktioner.

Mer information om de nya funktionerna finns på Experience League:

* [Datainsamling](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/reporting-interface/overview-data-collection.html)
* [Platser](https://experienceleague.adobe.com/docs/places/using/home.html?lang=sv)
* [Säkerhet](https://experienceleague.adobe.com/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance.html%3Flang%3Dde)
* [Identitetsnamnutrymme](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=en)
* [Sandlådor](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=en)
* [Experience Data Model](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=sv)
* [Scheman](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html)
* [Datastreams](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=en)
* [Besökar-ID](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html?lang=en#section_3C9F6DF37C654D939625BB4D485E4354)
* [Integritet](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=en)

## Autentisering av Experience Cloud-användare (planerad migrering){#migration}

Från och med februari 2022 uppdaterar Adobe sitt profilhanteringssystem så att organisationer bättre kan hantera sina rättigheter till enskilda profiler. Alla användare med en personlig profil, som motsvarar en enskild Adobe ID (Type1), kommer därför att migreras till en ny affärsprofil. Den här profilen motsvarar en _Företags-ID_ (Type2e).

Se [Identitetstyper på Adobe Admin Console](https://helpx.adobe.com/enterprise/using/identity.html) för information om identitetstyper.

### Migreringsprocess

När det är dags för din migrering får organisationens administratörer ett e-postmeddelande 30 dagar före migreringen.

* Migreringen planeras till kl. 10.00. - 6.00, baserat på organisationens primära tidszon eller på helgen.
* Under migreringen kan programmet Experience Cloud vara otillgängligt i ungefär 15 minuter och Admin Console kan vara otillgängligt i upp till 30 minuter. Annars kommer migreringen att vara sömlös.

### Ändringar efter migreringen

Admin Console

* Administratörer med flera konton kan se en profilväljare när de loggar in [!UICONTROL Admin Console].
* Enskilda Adobe ID-användare uppdateras till Business ID.
* Arbets-ID-katalogen läggs till i **[!UICONTROL Settings]** > **[!UICONTROL Identity]** > **[!UICONTROL Directories]**.

   ![Admin Console-identitet - företags-ID](assets/identity-home.png)

### Logga in efter migreringen

Inloggningsupplevelsen ändras inte med den här uppdateringen:

1. Logga in på `experience.adobe.com` med samma inloggningsuppgifter.

1. En ny profil som är associerad med ditt företags-ID skapas. Du uppmanas att **[!UICONTROL Join now]** eller **[!UICONTROL Skip]**.

1. Om något av alternativen används blir landningssidan en befintlig upplevelse.

1. En Adobe-profil är associerad med varje affärsplan och ger möjlighet att ordna resurser som skapats från ytterligare Adobe Cloud-erbjudanden (Creative Cloud och Document Cloud).

Mer information finns i [Nu kommer Adobe-profiler](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html).

## Vad är en produktprofil? {#section_AB50558124D541CF80A0D3D76D35A4BF}

_[!UICONTROL Product Profiles]_är grupper av produkter och tjänster som du kan tilldela användare. I Experience Cloud baseras behörigheter på en produkts profil, inte på användaren. (Du kan dock delegera administratörsbehörighet till vissa användare.)

I Analytics kan du till exempel konfigurera en samling rapporteringsverktyg, som Analysis Workspace och Report Builder, tillsammans med rapportsviter, mätvärden och dimensioner. Du kan ge behörighet till en produktprofil genom att lägga till användare i profilen.

* Se [Tilldela behörigheter för Analytics-åtkomst till en produktprofil](admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) på den här sidan.
* Se [Delegera administrativa roller till användare](#delegate-rights) på den här sidan

## Hantera produktprofiler för Experience Cloud {#task_16335111C52D40E9BAC73D0699584DBF}

Du kan skapa en produktprofil och tilldela den till en behörighetsgrupp.

När du bjuder in en användare till en organisation kan du ge användaren tillgång till produkter och produktprofiler. Du kan även delegera begränsade administrativa behörigheter till en användare. På samma sätt kan du skapa användargrupper och sedan lägga till gruppen i en produktprofil för att aktivera åtkomst.

1. I [Admin Console](https://adminconsole.adobe.com/enterprise/), markera **[!UICONTROL Products]**.
1. Välj organisationsnamn.
1. Välj **[!UICONTROL New Profile]**.
1. Konfigurera profilinformationen och välj sedan **[!UICONTROL Save]**.

Mer information (och om du vill ha hjälp om produkthantering för Creative Cloud och Document Cloud) finns i [Identitet](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/identity.ug.html) i [Användarhandbok för administration](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/users.ug.html).

**Relaterad hjälp**

* [Hantera produkter och profiler](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html) i administrationshandboken.
* [Enterprise-användarbehörigheter](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=en) i Adobe Target om du vill ha mer information.
* Video: [Konfigurera Adobe Target Workspaces i Adobe Admin Console](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-17521.html?lang=en)

## Delegera administrativa roller till användare {#delegate-rights}

I Admin Console kan du delegera begränsade administrativa rättigheter till andra i organisationen. Delegerade roller gör det möjligt för användare att administrera programåtkomst till slutanvändare, ge åtkomst till distributionsfunktioner och fungera som supportrepresentanter.

Du kan till exempel:

* Ge din creative director åtkomst till Creative Cloud.
* Tillåt marknadsföringschefen att ge åtkomst till Experience Cloud.
* Håll de här två rollerna åtskilda så att de inte kan överlappa varandras roller.

Genom att använda de här rollerna kan du delegera hantering till andra utan att ge dem mer kapacitet än de behöver.

1. I Admin Console väljer du **[!UICONTROL Users]** väljer du sedan användarens namn.

   ![Administrativa rättigheter i Admin Console](assets/edit-admin-rights.png)

1. Välj **[!UICONTROL Edit admin rights]**.

   ![Redigera administrativa rättigheter i Admin Console](assets/edit-admin-rights-page.png)

1. Ange användarens administratörsbehörighet.
1. Välj **[!UICONTROL Save]**.

## Hantera Analytics-användare och -produkter {#section_97DE101F92CD494AB073893680992F1A}

Du kan tilldela åtkomstbehörigheter för analysrapporter (rapportsviter, mätvärden, dimensioner och så vidare) till en produktprofil.

Du kan till exempel skapa en produktprofil som innehåller flera analysverktyg ([!UICONTROL Analysis Workspace], [!UICONTROL Reports & Analytics]och [!UICONTROL Report Builder]). Dessa profiler innehåller behörigheter till specifika mått och mått (inklusive eVars) och funktioner som att skapa segment eller beräknade mätvärden.

1. Logga in på [Admin Console](https://adminconsole.adobe.com/enterprise)väljer **[!UICONTROL Products]**.
1. På [!UICONTROL Products] väljer du produkt och sedan **[!UICONTROL Permissions]** (endast tillgängligt för administratörer).
1. Konfigurera profilens behörigheter:

| Element | Beskrivning |
|--- |--- |
| Rapportsviter | Aktivera behörigheter för specifika rapportsviter. |
| Mätvärden | Aktivera behörigheter för trafik, konvertering, anpassade händelser, programhändelser, innehållsmedveten osv. |
| Mått | Anpassa användaråtkomsten på detaljnivå, inklusive eVars, trafikrapporter, programrapporter och sökvägsrapporter. |
| Report Suite-verktyg | Aktivera användarbehörigheter för Web Services, Report Suite Management, Tools and Reports och Dashboard Items. |
| Analysverktyg | Aktivera användarbehörigheter för allmänna objekt (fakturering, loggar o.s.v.), företagshantering, verktyg, webbtjänståtkomst, Report Builder och Data Connectors-integrering. Företagsinställningar från kategorin Anpassa Admin Console har flyttats till Analytics-verktyg. |

**Migrering av användarkonto**

Det finns ett verktyg för migrering av användar-ID:n i Analytics som hjälper Analytics-administratörer att migrera användarkonton från Analytics-användarhantering till [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/).

Kontomigreringen introduceras till kunder i faser. Adobe meddelar och hjälper dig när det är dags att migrera befintliga användarkonton från **[!UICONTROL Admin Tools]** > **[!UICONTROL User Management]** till Admin Console.

Efter migreringen loggar användare in med sin Adobe ID (eller Enterprise ID) och autentiserar till Experience Cloud-program och -tjänster på [experience.adobe.com](https://experience.adobe.com). Om användare försöker logga in via äldre inloggningar ([!DNL my.omniture.com], [!DNL sc.omniture.com] och [!DNL experiencecloud.adobe.com]) omdirigeras de till [!DNL experience.adobe.com].

**Relaterad hjälp**

* [Analyser i Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=en)
* [Migrering av användar-ID för analyser](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/migrate-users/c-migration-tool.html?lang=en)

## Hantera Adobe Target - produktprofiler jämfört med arbetsytor {#section_3860AF177C9E4C7E9C390D36A414F353}

I Adobe Target är en arbetsyta en produktprofil. Det gör att en organisation kan tilldela en viss uppsättning användare till en viss uppsättning egenskaper. På många sätt liknar en arbetsyta en rapportserie i Adobe Analytics.

Se:

* [Enterprise-användarbehörigheter](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=en)
* [Hantera produkter och profiler](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html)
* Video: [Konfigurera Adobe Target Workspaces i Adobe Admin Console](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-17521.html?lang=en)

## Hantera kampanjproduktprofiler, klientorganisationer och säkerhetsgrupper {#section_09CDF75366444CF5810CF321B7C712F3}

A *tenant* i Campaign visas som *produkt* på Admin Console Products-sidan.

*Säkerhetsgrupp* visas som en produktprofil.

Se [Hantera grupper och användare](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html?lang=en) för information om säkerhetsgrupper och hur du tilldelar användare till säkerhetsgrupper.

## Hantera Experience Platform-datainsamling (Launch) {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform [!UICONTROL Data Collection] ([!UICONTROL Launch]) visas på [!UICONTROL Products] sidan i [!UICONTROL Admin Console]. Du kan inkludera andra program och tjänster i en Launch-produktprofil.

Bjud in användare till [!UICONTROL Platform Launch] och tilldela användarroller och -rättigheter.

Se [Användarbehörigheter](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html?lang=en) om du vill ha information om användarbehörigheter i Admin Console och om hur du ställer in startspecifika alternativ, inklusive tilldelning av behörigheter till profiler.

## Experience Manager as a Cloud Service

Adobe Enterprise-kunder representeras av organisationer i Adobe [!UICONTROL Admin Console]. Experience Manager-kunder kan använda Adobe [!UICONTROL Admin Console] hantera produktberättiganden och IMS-autentisering till Experience Manager som [!UICONTROL Cloud Service].

Se [IMS-stöd för Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=en).

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Skapa Audience Manager-användare och tilldela dem till grupper. Du kan även visa gränser (egenskaper, segment, mål och [!DNL AlgoModel]).

Se [Administration](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/administration/administration-overview.html?lang=en) i Audience Manager hjälp.

## Webbläsare i Experience Cloud som stöds

* [!DNL Microsoft® Edge] (Microsoft® har [avslutad support](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) för Internet Explorer 8, 9 och 10. Därför åtgärdar inte Adobe problem som rapporteras mot dessa specifika versioner av Internet Explorer.)
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**Obs!** Även om Experience Cloud-gränssnittet har stöd för dessa webbläsare, stöder inte enskilda program alla webbläsare. (Exempel: [Analyser](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=en) stöder inte [!DNL Opera]och [Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=en) stöder inte [!DNL Safari].)

### Lösningar och produktkrav

* [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=en) 
* [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/report-builder-setup/system-requirements.html?lang=en)
* [Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=en)
