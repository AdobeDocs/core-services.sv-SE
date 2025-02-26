---
title: Hantering av användar- och produktlicenser
description: Hantera användare och produktlicenser i Admin Console for Experience Cloud-program.
application: Experience Cloud
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: c82821c4-aa5d-48ae-8bef-5937fede8db2
source-git-commit: 9932f21e4aa4d4a5bf08d7f1617b4c25d4fb14bb
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 2%

---

# Användarhantering och produktlicenser

Den här sidan innehåller information för Experience Cloud-administratörer, med länkar till vanliga användar- och produkthanteringsdokument.

Allmän hjälp om identitetshantering för alla Adobe-program finns i [Administratörshandboken för Enterprise och teams](https://helpx.adobe.com/se/enterprise/admin-guide.html).

I följande avsnitt finns länkar till resurser i hjälpen för Admin Console.

## Administrativa roller i Admin Console

Admin Console har tre primära administrativa roller med specifika nivåer av åtkomst och ansvar:

**Systemadministratör:** Fullständig åtkomst - Hanterar alla aspekter av konsolen.

Viktiga ansvarsområden:

* Lägg till, ta bort och hantera användare.
* Tilldela och återkalla produktlicenser.
* Konfigurera inställningar för identitet och autentisering.
* Visa och hantera faktureringsinformation.
* Ställ in ytterligare administratörer och delegatroller.

  **Passar bäst för:** IT-administratörer eller team som leder övervakningen av hela organisationens Adobe-miljö.

**Produktadministratör:** Produktspecifik hantering - Styr åtkomst och behörigheter för specifika Adobe-produkter.

Viktiga ansvarsområden:

* Tilldela och hantera licenser för en viss produkt.
* Skapa och hantera produktprofiler.
* Lägg till eller ta bort användare i tilldelade produkter.

  **Passar bäst för:** Team/användare som hanterar viss programvara som Marketo Engage eller Adobe Creative Cloud.

**Administratör för produktprofil:** Detaljerad rollhantering - Fokuserar på hantering av användargrupper och behörigheter i en produkt.

* Viktiga ansvarsområden:
* Skapa och hantera produktprofiler.
* Tilldela behörigheter och funktionsåtkomst i profiler.
* Lägg till eller ta bort användare i profiler.

  **Passar bäst för:** Avdelningsledare eller gruppchefer som övervakar mindre grupper med särskilda behov

  Administratörer kan kombinera roller för större flexibilitet beroende på organisationens krav.

## Admin Console

Om du vill hantera identitet och produktlicenser för Experience Cloud-program går du till [Admin Console](https://adminconsole.adobe.com/enterprise/).

* [Konfigurera identitet och enkel inloggning](https://helpx.adobe.com/enterprise/using/set-up-identity.html) - Lär dig hur du konfigurerar dina användarkonton med olika ID-typer med eller utan enkel inloggning (SSO). Konfigurera enkel inloggning för Adobe, konfigurera SAML-inställningar och gå igenom de vanligaste frågorna och felen.

* [Konfigurera organisation via katalogförtroende](https://helpx.adobe.com/enterprise/using/directory-trust.html) - Använd katalogförtroende för att autentisera dina användare mot en domän som redan tagits i anspråk av en annan organisation.

  Mer information om organisationer finns i [Organisationer i Experience Cloud](organizations.md).

* [Autentiseringsinställningar (enterprise)](https://helpx.adobe.com/enterprise/using/authentication-settings.html) - Admin Console stöder flera lösenordsskyddsnivåer och principer för att säkerställa säkerhet och säkerhet. Du kan ange att en lösenordsskyddsnivå ska användas för alla användare i organisationen. Adobe kundtjänst - tre säkerhetsnivåer.

* [Sekretess- och säkerhetskontakter](https://helpx.adobe.com/enterprise/using/security-contacts.html) - Adobe betonar att skydda din organisations och dina användares data. Vid säkerhetstillbud som inbegriper våra programvarulösningar skickas meddelanden till de ansvariga för regelefterlevnad.

  Företag har sin egen personal vars roll är specifik för dataskydd, integritet och andra regelefterlevnadsfrågor. Kontaktinformation för sådan personal är därför mycket viktig för att säkerställa snabb information i händelse av säkerhetstillbud.

## Användarhantering

* [Hantera flera användare](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) Massöverföring av CSV - Lär dig hur du hanterar flera användare via CSV-massöverföring på Adobe Admin Console.

* [Identitetstyper](https://helpx.adobe.com/enterprise/using/identity.html) - Identitetstyper tillåter organisationen olika nivåer av kontroll över användarnas konton och data. Ditt val av identitetsmodell påverkar hur organisationen lagrar och delar resurser. Federated ID- och Enterprise ID-modeller skapas och hanteras av organisationen, men Adobe ID:n skapas och hanteras av individen.

* [Användarsynkroniseringsverktyg](https://helpx.adobe.com/enterprise/using/user-sync.html) (UST) - Adobe användarsynkroniseringsverktyg är ett skrivbordsprogram som används för att automatisera synkroniseringen av användardata mellan en organisations identitetshanteringssystem (som Active Directory) och Adobe Adobe Admin Console. Med det här verktyget kan administratörer effektivisera användarnas etablering, uppdateringar och inaktivering av Adobe-produkter.

  Med verktyget för användarsynkronisering kan organisationer förenkla hanteringen av användarkonton och licenser genom att automatiskt synkronisera användardata (t.ex. roller, grupper och åtkomstbehörigheter) mellan katalogtjänsten och Adobe-systemen. Det här verktyget är särskilt användbart för företag med stora team. Det bidrar till att upprätthålla enhetlighet och säkerhet samtidigt som det säkerställs att användarna bara har tillgång till de produkter och tjänster som de har rätt till.

* [Visa användarinformation (Admin Tool)](admin-tool-experience-cloud.md) - Administratörer kan visa en sorterbar och filterbar lista över alla Experience Cloud-användare och -profiler med information i [!UICONTROL Admin Tool].

## Rapporter och loggar

* [Granskningslogg](https://helpx.adobe.com/enterprise/using/audit-logs.html) Om du vill spåra alla ändringar som gjorts i Admin Console.

Om du vill ha hjälp som inte beskrivs ovan kan du bläddra i [Administratörshandboken för Enterprise och teams](https://helpx.adobe.com/se/enterprise/admin-guide.html).

## Programspecifika resurser

Länkarna hjälper dig att hitta administrationsinformation för specifika Experience Cloud-program.

<!-- | Application | Link to resource|
| ------- | ------- |
|  [!DNL Analytics] <p>Customer Journey Analytics| [Analytics in the Adobe Admin Console overview](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home) <p>[Administration requirements](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace) |
| [!DNL Audience Manager] | [Audience Manager user migration to Admin Console](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/administration/admin-console-migration) |
| [!DNL Campaign] v8 |  [Get started with permissions](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/admin/permissions/gs-permissions) |
| [!DNL Campaign Standard] to [!DNL Campaign v8] | [User access management from Campaign Standard to Campaign V8](https://experienceleague.adobe.com/en/docs/campaign-web/acs-to-ac/user-management-acs) |
| [!DNL Commerce] | [Configure the Commerce Admin Integration with Adobe ID](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config) |
| [!DNL Dynamic Media Classic] | [Administration setup](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/setup/administration-setup#user_administration) |
| [!DNL Experience Manager as a Cloud Service] |  [Accessing the Admin Console](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console) |
| [!DNL Experience Platform] <p>[!DNL Data Collection] | [Access control UI overview](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/overview) <p>[Permission management for data collection in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/collection/permissions)|
| [!DNL GenStudio for Performance Marketing] | [Provision Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning) |
| [!DNL Journey Optimizer] | [Manage users and roles](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/permissions) |
| [!DNL Journey Optimizer B2B Edition] | [User management](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management) |
|[!DNL  Journey Orchestration] | [Access management](https://experienceleague.adobe.com/en/docs/journeys/using/starting-with-journeys/access-management) |
| [!DNL Marketo Engage] | [Understanding Marketo Subscription and User Migration to the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console) |
| [!DNL Marketo Measure] | [Adobe Admin Console Setup](https://experienceleague.adobe.com/en/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup) |
| [!DNL Mix Modeler] | [Access controls](https://experienceleague.adobe.com/en/docs/mix-modeler/using/data-governance/access-controls) |
| [!DNL Pass] | [Get started with Account IQ](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started) |
| [!DNL Target] | [Administrator first steps](https://experienceleague.adobe.com/en/docs/target/using/administer/start-target) <p> [User management](https://experienceleague.adobe.com/en/docs/target/using/administer/manage-users/user-management) |
| [!DNL Workfront] | [Manage users in the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console) |

 -->

* [Analytics](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home) 
* [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace)
* [Audience Manager](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/administration/admin-console-migration)
* [Campaign v8](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/admin/permissions/gs-permissions)
* [Campaign Standard](https://experienceleague.adobe.com/en/docs/campaign-web/acs-to-ac/user-management-acs)
* [Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config)
* [Dynamic Media Classic](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/setup/administration-setup#user_administration)
* [Experience Manager as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console)
* [Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/overview) och [Datainsamling](https://experienceleague.adobe.com/en/docs/experience-platform/collection/permissions)
* [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning)
* [Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/permissions)
* [Journey Optimizer B2B edition](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management)
* [Journey Orchestration](https://experienceleague.adobe.com/en/docs/journeys/using/starting-with-journeys/access-management)
* [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console)
* [Marketo Measure](https://experienceleague.adobe.com/en/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup)
* [Mix Modeler](https://experienceleague.adobe.com/en/docs/mix-modeler/using/data-governance/access-controls)
* [Adobe Pass](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started)
* [Mål](https://experienceleague.adobe.com/en/docs/target/using/administer/start-target)
* [Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console)