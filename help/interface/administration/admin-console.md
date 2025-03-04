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
source-git-commit: 77841faeb5b005e4913408edb3e9cfbbdfc8961d
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 2%

---

# Användarhantering och produktlicenser

Den här sidan innehåller information för Experience Cloud-administratörer, med länkar till vanliga användar- och produkthanteringsdokument.

Allmän hjälp om identitetshantering för alla Adobe-program finns i [Administratörshandboken för Enterprise och teams](https://helpx.adobe.com/se/enterprise/admin-guide.html).

## Administrativa roller i Admin Console

Admin Console har tre primära administrativa roller med specifika nivåer av åtkomst och ansvar:

| Roll | Beskrivning |
| ------- | ------- |
| Systemadministratör | Fullständig åtkomst - Hanterar alla delar av konsolen. <br>Viktiga ansvarsområden: <br><ul><li>Lägg till, ta bort och hantera användare.</li><li>Tilldela och återkalla produktlicenser.</li><li>Konfigurera inställningar för identitet och autentisering</li><li>Visa och hantera faktureringsinformation.</li><li>Ställ in ytterligare administratörer och delegatroller.</li></ul> **Passar bäst för:** IT-administratörer eller team som leder övervakningen av hela organisationens Adobe-miljö. |
| Produktadministratör | Produktspecifik hantering - Styr åtkomst och behörigheter för specifika Adobe-produkter.<br>Viktiga ansvarsområden:<ul><li>Tilldela och hantera licenser för en viss produkt.</li><li>Skapa och hantera produktprofiler.</li><li>Lägg till eller ta bort användare i tilldelade produkter.</li></ul>   **Passar bäst för:** Team/användare som hanterar viss programvara som Marketo Engage eller Adobe Creative Cloud. |
| Produktprofiladministratör | Detaljerad rollhantering - Fokuserar på hantering av användargrupper och behörigheter i en produkt.<br>Viktiga ansvarsområden:<ul><li>Skapa och hantera produktprofiler.</li><li>Tilldela behörigheter och funktionsåtkomst i profiler.</li><li>Lägg till eller ta bort användare i profiler.</li></ul> **Passar bäst för:** Avdelningsledare eller gruppchefer som övervakar mindre grupper med specialiserade behov. <br> Administratörer kan kombinera roller för större flexibilitet, beroende på organisatoriska krav. |

## Admin Console för Experience Cloud

Om du vill hantera identitet och produktlicenser för Experience Cloud-program går du till [Admin Console](https://adminconsole.adobe.com/enterprise/).

Här är resurser som du kan behöva för att komma igång som administratör i Admin Console:

### Konfigurera resurser

| Hjälplänk | Beskrivning |
| ------- | ------ |
| [Konfigurera identitet och enkel inloggning](https://helpx.adobe.com/enterprise/using/set-up-identity.html) | **[!UICONTROL  Admin Console]** > **[!UICONTROL Settings]** <br> Lär dig hur du konfigurerar dina användarkonton med olika ID-typer med eller utan enkel inloggning (SSO). Konfigurera enkel inloggning för Adobe, konfigurera SAML-inställningar och gå igenom de vanligaste frågorna och felen. |
| [Konfigurera organisation via katalogförtroende](https://helpx.adobe.com/enterprise/using/directory-trust.html) | Autentisera dina användare mot en domän som redan tagits i anspråk av en annan organisation. Mer information om hur du söker efter och byter organisation finns i [Organisationer i Experience Cloud](organizations.md). |
| [Autentiseringsinställningar (Enterprise)](https://helpx.adobe.com/enterprise/using/authentication-settings.html) | Admin Console stöder flera skyddsnivåer och principer för lösenord för att säkerställa säkerheten. Du kan ange att en lösenordsskyddsnivå ska användas för alla användare i organisationen. |
| [Kontakter för sekretess och säkerhet](https://helpx.adobe.com/enterprise/using/security-contacts.html) | Skydda organisationens och användarnas data. Om en säkerhetsincident inträffar med våra programvarulösningar, skickas meddelanden till lämplig personal. Företag har personal vars roll är specifik för dataskydd, integritet och andra regelefterlevnadsfrågor. Kontaktinformation för sådan personal är därför mycket viktig för att säkerställa snabb information i händelse av säkerhetstillbud. |

### Användarhantering

| Hjälplänk | Beskrivning |
| ------- | ------- |
| [Hantera flera användare](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) | **[!UICONTROL Admin Console]** > **[!UICONTROL Users]** <br>Lär dig hantera flera användare via CSV-massöverföring till Admin Console. |
| [Identitetstyper](https://helpx.adobe.com/enterprise/using/identity.html) | Med identitetstyper kan organisationen ha olika nivåer av kontroll över användarnas konton och data. Ditt val av identitetsmodell påverkar hur organisationen lagrar och delar resurser. Federated ID- och Enterprise ID-modeller skapas och hanteras av organisationen, men Adobe ID:n skapas och hanteras av individen. |
| [Verktyget för användarsynkronisering](https://helpx.adobe.com/enterprise/using/user-sync.html) (UST) | Adobe användarsynkroniseringsverktyg är ett datorprogram som används för att automatisera synkroniseringen av användardata mellan en organisations identitetshanteringssystem (som Active Directory) och Adobe Admin Console. Med det här verktyget kan administratörer effektivisera användarnas etablering, uppdateringar och inaktivering av Adobe-produkter. |
| [Visa användarinformation (Admin Tool)](admin-tool-experience-cloud.md) | Visa en sorterbar och filtrerbar lista över alla Experience Cloud-användare och principer med information i [!UICONTROL Admin Tool]. |

### Rapporter och loggar

| Hjälplänk | Beskrivning |
| ------- |------- |
| [Granskningslogg](https://helpx.adobe.com/enterprise/using/audit-logs.html) | **[!UICONTROL Insights]** > **[!UICONTROL Logs]** > **[!UICONTROL Audit Log]** <br> Spåra alla ändringar som gjorts i Admin Console. |


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

Huvuddelen av Admin Console-hjälpen för alla Adobe-program beskrivs i [Administratörshandboken för Enterprise och team](https://helpx.adobe.com/se/enterprise/admin-guide.html).
