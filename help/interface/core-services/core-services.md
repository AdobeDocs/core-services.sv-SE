---
description: Implementera Experience Cloud och bli administratör. Den här processen moderniserar era lösningar för funktioner som kundattribut och målgrupper.
keywords: core services;Customer Attributes
seo-description: Implementera Experience Cloud och bli administratör. Den här processen moderniserar era lösningar för funktioner som kundattribut och målgrupper.
seo-title: Möjliggör era Experience Cloud-lösningar för kundattribut och målgrupper
solution: Experience Cloud
title: Möjliggör era lösningar för bastjänsterna
index: true
translation-type: tm+mt
source-git-commit: 570cf3bd7cb86a701006e64d14ddf45c4cd24426
workflow-type: tm+mt
source-wordcount: '2313'
ht-degree: 2%

---


# Aktivera implementeringen av Experience Cloud-tjänster

Om du nyligen har implementerat Experience Cloud med Experience Platform Launch har du redan ställt in kundattribut och Experience Cloud målgrupper. Du kan också hantera användare och produkter i Admin Console.

För befintliga kunder kan ni behöva modernisera era lösningar och implementera Experience Cloud. På så sätt kan ni utnyttja kundattribut och målgruppsfunktioner i Adobe Analytics, Audience Manager och Adobe Target. För att uppnå detta ska du:

1. [Gå med i Experience Cloud och bli administratör](#section_2423F0BD3DF642658103310EE5EA6154)
1. [Implementera tjänsten Experience Cloud ID](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [Mappa rapportsviter till en Experience Cloud-organisation](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [Uppdatera din Analytics AppMeasurement-kod](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [Uppdatera implementeringen av Adobe Target](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [Verifiera implementeringen](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [Hantera användare och produkter](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [Börja dela attribut och målgruppsdata](#section_960C06093623462E8EA247B3E97274A1)

## Steg 1. Gå med i Experience Cloud och bli administratör {#section_2423F0BD3DF642658103310EE5EA6154}

Vad du behöver göra för att gå med i Experience Cloud:

![](assets/step1_icon.png) Kontrollera att du har rätt SKU för Adobe Analytics eller Adobe Target.

* **Adobe Analytics:** Standard eller Premium (inte den äldre [!DNL SiteCatalyst] SKU:n).
* **Adobe Target:** Standard eller Premium.

>[!NOTE]
>
>Du [!DNL Target]kan till exempel migrera till at.js från [!DNL mbox.js]. Se [Uppgradera från at.js 1. x till at.js 2. x](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/upgrading-from-atjs-1x-to-atjs-20.html).

![](assets/step2_icon.png) Modernisera implementeringen och få status som administratör.

1. Följ stegen nedan i [Distribuera [!UICONTROL Experience Cloud ID Service]](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354).
1. Kontakta din kontohanterare och starta provisioneringsprocessen för Experience Cloud.

![](assets/step3_icon.png) Hantera användare och produkter i [!UICONTROL Admin Console].

### Administratörsinloggning

När du är administratör kan du logga in på [experienceCloud.adobe.com](https://experiencecloud.adobe.com).

Länken visas i navigeringen på Experience Cloud-menyn. **[!UICONTROL Administration]**

Mer information finns i [Experience Cloud och produktadministration](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909) .

### Användarinloggning

För att kunna logga in på Experience Cloud måste dina användare:

1. Ha en Adobe ID (eller ett Enterprise ID för ditt företag).
1. Logga in på [experienceCloud.adobe.com](https://experiencecloud.adobe.com).
1. Tillhör en lösningsgrupp som är mappad till en företagsgrupp.
1. Länka vid behov deras lösningskonton till deras Adobe ID (beskrivs nedan).

![](assets/step4_icon.png) Valfritt: Länka befintliga användarkonton.

Troligen har du användare som redan är medlemmar i lösningsgrupper, till exempel en Analytics-grupp som du tidigare har hanterat i [!UICONTROL Analytics] > [!UICONTROL Admin Tools].

När du mappar de här grupperna till företagsgrupper i Experience Cloud måste dessa användare manuellt länka sina autentiseringsuppgifter för lösningskonton till sina Adobe ID.

Se [Länka konton i Experience Cloud](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

>[!NOTE]
>
>När enterprise- och lösningsgrupper har mappats länkas nya användare automatiskt. (Autentiseringsuppgifter för lösningen skapas automatiskt och länkas till deras Adobe ID.)

I följande avsnitt beskrivs hur du moderniserar implementeringen. Genom att modernisera implementeringen kan du få tillgång till bastjänster i Experience Cloud.

## Steg 2. implementera [!UICONTROL Experience Cloud ID Service] med [!UICONTROL Experience Platform Launch], eller [!UICONTROL Dynamic Tag Management] {#section_3C9F6DF37C654D939625BB4D485E4354}

Det [!UICONTROL Experience Cloud ID Service] ger ett gemensamt ID för integrering mellan olika lösningar. Det ger identifiering av besökare över domäner och en sökväg för målinriktning och personalisering mellan olika enheter/webbläsare baserat på CRM-data som överförs via [!UICONTROL Customer Attributes].

Det enklaste sättet att aktivera Experience Cloud bastjänster är att aktivera det automatiskt för Analytics och Adobe Target via [Experience Cloud ID-tjänsttillägget](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html) i [!UICONTROL Experience Platform Launch]eller via ECID-verktyget i [!UICONTROL Dynamic Tag Management]. (Experience Platform Launch rekommenderas starkt.)

Fullständig hjälp om Experience Cloud ID-tjänsten (tidigare besökar-ID) finns [här](https://docs.adobe.com/content/help/sv-SE/id-service/using/home.html).

**Använder du inte [!UICONTROL Experience Platform Launch] eller [!UICONTROL Dynamic Tag Management]?**

Om du inte använder [!UICONTROL Experience Platform Launch] eller [!UICONTROL Dynamic Tag Management]implementerar du ID-tjänsten manuellt via JavaScript Deployment ([!DNL VisitorAPI.js]) enligt följande:

| Uppgift | Beskrivning |
| -----------| ---------- |  
| [Implementera Experience Cloud ID-tjänsten för analys](https://docs.adobe.com/content/help/en/id-service/using/implementation/setup-analytics.html) | Adobe rekommenderar även att du anger ytterligare [kund-ID](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html). Dessa ID:n är kopplade till varje besökare och aktiverar nuvarande och framtida funktioner i Experience Cloud. |
| Uppdatera din befintliga version [!DNL s_code] till version H.27.3 eller senare, eller din befintliga [!DNL AppMeasurement.js] till version 1.4 eller senare. | De här filerna är tillgängliga för hämtning i [kodhanteraren](https://docs.adobe.com/content/help/sv-SE/analytics/admin/admin-tools/code-manager-admin.html) i administrationsverktygen för analyser.  (Handboken för [JavaScript-implementering](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) finns tillgänglig om du behöver mer information om [!DNL AppMeasurement.js].) |
| Synkronisera kund-ID för Analytics | Se [Analytics - synching the customer ID](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437) (below). |

## Analytics &amp; Adobe Target - synkronisera kund-ID {#section_AD473A6A21C1446498E700363F9A8437}

Som en del av konfigurationen av Experience Cloud ID-tjänsten rekommenderar Adobe för Analytics och [!DNL Target] att du synkroniserar dina [kund-ID](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) med Experience Cloud.

I Adobe Target `mbox3rdpartyid` måste kunden hämta sitt ID och skicka det till [!DNL Target]. (Se [Arbeta med kundattribut](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) i [!DNL Target].)

När en besökare autentiserar sig på din webbplats, eller på annat sätt identifierar sig själv, måste din implementering visa den personens CRM-kund-ID för sidan eller appen. Sedan kan du använda rätt funktionsanrop för att synkronisera ditt kund-ID med Experience Cloud. Den här synkroniseringen lagrar besökarens CRM-kund-ID i Experience Cloud och aktiverar kundens attribut för användning i Experience Cloud.

Anta till exempel att Bob har ett kund-ID `52mc210tr42` i ditt CRM-system. När Bob autentiserar på din webbplats måste du visa detta ID på sidan och använda ID:t för att synkronisera det på något av två sätt:

* Ring `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` med tjänsten för besökar-ID. Eller
* Fyll *`Customer ID (52mc210tr42)`* i ett utkast eller en eVar.

Kund-ID måste anges för varje [!DNL Analytics] serversamtal där Kund-ID:t är känt.

### SDK för mobiler

I avsnittet *Experience Cloud ID-tjänst* finns syntaxexempel på hur du ställer in ytterligare kund-ID:n i [Android](https://docs.adobe.com/content/help/sv-SE/mobile-services/android/overview.html) - och [iOS](https://docs.adobe.com/content/help/sv-SE/mobile-services/ios/overview.html) -mobilprogram.

### Aktivera attribut för historiska data

Kundattributdata blir tillgängliga när besökarna loggar in. Om du ännu inte har implementerat den senaste Experience Cloud ID-tjänsten, och om du historiskt har spårat kundens ID i en prop eller eVar, kan du begära en process som skickar historiska inloggningar till Experience Cloud. Med den här processen kan du börja använda kundattribut direkt.

Kontakta kundtjänst om du vill aktivera historikdata.

## Steg 3. Mappa rapportsviter till en Experience Cloud-organisation {#section_7B08516B01BA421681DF03D0E86CE3BA}

Experience Cloud-tjänster (som Experience Cloud ID-tjänsten och [!UICONTROL People service]) är kopplade till en Experience Cloud-organisation i stället för till en enskild Analytics-rapportsvit. För att dessa tjänster ska fungera på rätt sätt måste varje analysrapport mappas till en Experience Cloud-organisation.

See [Map report suites to an organization](report-suite-mapping.md).

## Steg 4. (Adobe Analytics) Uppdatera din Analytics AppMeasurement-kod {#section_1798D9D0F05C47E29816AC4EEB9A0913}

Kontrollera att du använder regional datainsamling. Om din datainsamlingsdomän är [!DNL omtrdc.net]eller om CNAME är mappad till [!DNL omtrdc.net]är du på RDC. Mer information finns i [Övergång till RDC](https://docs.adobe.com/content/help/en/analytics/technotes/rdc/regional-data-collection.html) . Om du använder cookies från första part läser du i [CNAME och Experience Cloud ID-tjänsten](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html) för information om datainsamling-CNAME och spårning mellan domäner.

Vi rekommenderar att du moderniserar din Analytics-implementering genom att uppdatera dina JavaScript-bibliotek, inklusive Visitor API. Det enkla sättet att uppnå detta är att lägga till ett [!DNL Adobe Analytics] verktyg i Dynamic Tag Management, som anger *`Automatic`* som konfigurationsmetod.

I [!UICONTROL Dynamic Tag Management]klickar du på **`<Web Property Name>`** > **[!UICONTROL Overview]** > **[!UICONTROL Add a Tool]** > **[!UICONTROL Adobe Analytics]**. Mer distributionsinformation finns i [Adobe Analytics-inställningar](https://docs.adobe.com/content/help/en/dtm/using/tools/analytics-dtm.html) i Dynamic Tag Management.

## Steg 5. (Adobe Target) Uppdatera er Adobe Target-implementering {#section_C2F4493C7A36406DAE2266B429A4BD24}

* Vi rekommenderar att du lägger till ett [Adobe Target-tillägg](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/targetv2-extension/adobe-target-extension-v2.html) i [!UICONTROL Experience Platform Launch]så att bibliotekshämtningen sker automatiskt. Du kan också konfigurera [Experience Cloud ID-tjänsttillägget](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html) för Adobe Target (och andra lösningar) med [!UICONTROL Experience Platform Launch]. Uppdateringen [!UICONTROL Experience Cloud ID Service] krävs **** för att Adobe Target ska kunna använda bastjänsterna. (Om du använder [!UICONTROL Dynamic Tag Management]kan du lägga till ett [Adobe Target-verktyg](https://docs.adobe.com/content/help/en/dtm/using/tools/target.html). Du kan också använda [!UICONTROL Dynamic Tag Management] för att distribuera Experience Cloud ID-tjänsten för Adobe Target.)
* Om du inte använder [!UICONTROL Experience Platform Launch] eller [!UICONTROL Dynamic Tag Management]ska du [uppdatera mbox-biblioteket](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html) manuellt.
* Begär åtkomst att använda Adobe Analytics som rapportkälla för [!DNL Adobe Target]. [!DNL Target] och [!DNL Analytics] data kombineras på samma serveranrop under bearbetningen så att besökarna är sammankopplade mellan de två lösningarna. Se [Analytics for Target Implementation](https://docs.adobe.com/content/help/sv-SE/target/using/integrate/a4t/a4t.html).

   >[!IMPORTANT]
   >
   >Alla Analytics-kunder har redan etablerats för bastjänster som kundattribut. Om du inte är Analytics-kund kontaktar du kundtjänst för att begära att få etableras.

## Steg 6. Verifiera implementeringen {#section_E641782A0F4F44AF8C9C91216BE330D5}

Använd följande process för att säkerställa att Experience Cloud ID-tjänsten implementeras korrekt på din webbplats.

1. Rensa cookies för din webbplats så att du kan se begäran till Experience Cloud ID-tjänsten (begäran görs vid det första besöket och sedan ungefär en gång per besökare per vecka).
1. Använd en paketanalyserare eller nätverkspanelen i en webbläsarfelsökare för att leta efter en begäran som ska skickas [!DNL dpm.demdex.net].
1. Kontrollera att svaret innehåller `d_mid` och ett värde, till exempel: `_setMarketingCloudFields({"d_mid":"4235...`
1. Kontrollera att Analytics-begäran innehåller `mid` parametern (Experience Cloud-ID). Under respitperioden (om den är aktiverad) bör du även se en `aid` parameter (besökar-ID:t för Analytics).

Förväntat svar som innehåller Experience Cloud-ID:

![](assets/mac_id_response.png)

Analysbildbegäran som innehåller Experience Cloud-ID (kallas även `mid` eller _besökar-ID_):

![](assets/mid.png)

Experience Cloud ID i mbox-begäran:

![](assets/mbox_request.png)

### Hur lång är fristen?

När du har distribuerat Experience Cloud ID-tjänsten får nya besökare inte längre något Experience Cloud-ID för Analytics från din datainsamlingsserver. Om delar av din webbplats ännu inte har implementerat Experience Cloud ID-tjänsten identifieras inte Experience Cloud ID:t när besökare bläddrar till de här avsnitten och besökarna tilldelas ett äldre besökar-ID för Analytics. Detta kan orsaka potentiella problem, inklusive dubblettbesök och felaktig attribuering.

Om supportavsnittet på webbplatsen till exempel hanteras i ett separat CMS-system kan du ha en annan Analytics JavaScript-fil för det här avsnittet. Om du distribuerar Experience Cloud ID på huvudwebbplatsen innan du distribuerar ID-tjänsten till supportwebbplatsen får nya besökare ett äldre Analytics ID när de besöker supportavsnittet, och besök som sträcker sig över båda webbplatsavsnitten rapporteras som olika besök.

Om du distribuerar Experience Cloud ID-tjänsten på webbplatser som använder flera JavaScript-filer eller andra tekniker (till exempel Flash) kan det orsaka problem med samordningen eftersom du måste aktivera Experience Cloud ID-tjänsten på alla delar av platsen samtidigt. Genom att konfigurera en respitperiod kan nya besökare fortsätta att ta emot ett besökar-ID för Analytics från ID-tjänsten, så att besökare kan identifieras på ett konsekvent sätt på delar av webbplatsen som inte har uppgraderats för att använda besökar-ID-tjänsten.

## Steg 7. Hantera användare och produkter {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

När du är igång går du till [Admin Console](https://adminconsole.adobe.com/)där du kan hantera användare och produktprofiler.

![](assets/menu-administration-shell.png)

Se [Experience Cloud och produkthantering](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909).

### Kundattribut

Användare som läggs till i [!UICONTROL Customer Attributes] gruppen kan se [!UICONTROL Customer Attributes] menyalternativet till vänster i Experience Cloud.

## Steg 8. Börja dela attribut och målgruppsdata {#section_960C06093623462E8EA247B3E97274A1}

Utnyttja följande funktioner.

### [!UICONTROL People] > [!UICONTROL Customer Attributes]

Om du samlar in data om företagskunder i en CRM-databas (customer relationship management) kan du överföra dessa data till en datakälla för kundattribut i Experience Cloud. När data har överförts kan du utnyttja dem i [!DNL Adobe Analytics] och [!DNL Adobe Target].

Se [Kundattribut](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

### [!UICONTROL People] > [!UICONTROL Audience Library]

Experience Cloud [!UICONTROL Audiences] är gränssnittet där du kan skapa målgrupper, kombinera befintliga målgrupper för att skapa sammansatta målgrupper och visa alla delade målgrupper.

Se [målgrupper](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

## Datalagring och sekretess

Om ni utnyttjar målgruppsprofilering i realtid och andra bastjänster inom Adobe [!DNL Experience Cloud]kan användningen av dessa tjänster påverka vilket datacenter (och vilket land) era data finns i. Eftersom Adobe bastjänster [!DNL Experience Cloud] utnyttjar Adobe Audience Manager måste data som används inom [!UICONTROL People] tjänsten finnas på Audience Manager-servrar i USA.

När man utnyttjar bastjänsterna som tillhandahålls via [!UICONTROL People] tjänsten är de typer av data som skickas från andra Adobe-produkter till målgruppshantering följande:

* [!DNL Analytics] nyckel-/värdepar (props, eVars, list-var o.s.v.). Som standard innehåller loggraderna IP-adress, inklusive IP-adressens sista oktett (förutsatt att IP-adressen inte har ändrats av inställningarna för IP-förfalskning i Adobe [!DNL Analytics]).
* Fackar och segment som besökare är kvalificerade för baserat på regler som har upprättats i Audience Manager.
* (Valfritt) Ett eller flera av dina ID:n. Beroende på din implementering av ID-tjänsten kan du även skicka in ett eller flera av dina ID:n, till exempel CRM-ID:n eller hash-kodade e-postadresser. Om dessa data skickas till Adobe [!DNL Analytics]överförs de till Adobe målgruppshantering. Adobe rekommenderar att man inte lämnar personuppgifter till Adobe [!DNL Analytics]. Använd i stället en envägshash för att maskera data innan de skickas till Adobe.
* Segment som härrör från [!DNL Analytics] segmentdelning via bakomliggande segment.
* Cookien demdex.net anges om cookies från tredje part inte blockeras. Den första `AMCV_###@AdobeOrg` -parts-cookien ställs alltid in med Experience Cloud ID-tjänsten.

Alla dessa dataelement levereras till Adobe Audience Manager i form av loggfiler. Audience Manager bearbetar och lagrar dessa data i USA. Audience Manager har inget alternativ för att lagra eller bearbeta dessa data utanför USA.

### Cookies och Opt-Outs

Användning av målgruppsprofiler i realtid utnyttjar Audience Manager cookie, utöver de cookies som används för [!DNL Analytics] och [!DNL Target].

Om du vill ha rätt avanmälningsmöjlighet måste besökare på din webbplats lägga till avanmälan från Audience Manager i din befintliga avanmälningsprocess.

Mer information finns i [Adobe Experience Cloud - Implementera Adobe Opt-Outs](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/data-collection/opt-out.html) .

Se [Datainsamling-CNAME och Spårning](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html) mellan domäner för att aktivera spårning mellan domäner.
