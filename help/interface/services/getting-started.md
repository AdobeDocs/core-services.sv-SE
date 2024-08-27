---
description: Modernisera era era Adobe Analytics- och Adobe Target-program för olika programtjänster. Lär dig hur du börjar använda Experience Cloud-tjänster.
solution: Experience Cloud
title: Kom igång med Experience Cloud Services
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: 48e79e23-b339-4143-b3b1-969c370efeff
source-git-commit: 2a80851c0a7d4ef7dbcc2565177b239f3e063164
workflow-type: tm+mt
source-wordcount: '1919'
ht-degree: 0%

---

# Kom igång med Experience Cloud-tjänster

Om du nyligen har implementerat Experience Cloud med Experience Platform-taggar är du redan inställd på Kundattribut och Experience Cloud-målgrupper. Du kan också hantera användare och produkter i Admin Console.

Befintliga kunder kan modernisera sina applikationsimplementationer och implementera Experience Cloud. På så sätt kan ni använda kundattribut och målgruppsfunktioner i Adobe Analytics, Audience Manager och Adobe Target.

## Gå med i Experience Cloud och bli administratör {#section_2423F0BD3DF642658103310EE5EA6154}

Vad du måste göra för att gå med i Experience Cloud:

1. Kontrollera att du har rätt SKU för Adobe Analytics eller Adobe Target.

   * **Adobe Analytics:** Standard eller Premium (inte den äldre [!DNL SiteCatalyst] SKU:n).
   * **Adobe Target:** Standard eller Premium.

   >[!NOTE]
   >
   >Migrera till at.js från `mbox.js` för [!DNL Target]. Se [Uppgradera från at.js 1. x till at.js 2. x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/upgrading-from-atjs-1x-to-atjs-20.html).

1. Hantera användare och produkter i [!UICONTROL Admin Console].

### Administratörsinloggning

När du är administratör kan du logga in på [experience.adobe.com](https://experience.adobe.com).

Länken **[!UICONTROL Admin Console]** är tillgänglig i navigeringen på Experience Cloud-menyn.

### Användarinloggning

Om du vill logga in på Experience Cloud måste du:

* Ha en Adobe ID (eller ett Enterprise ID för ditt företag).
* Logga in på [experience.adobe.com](https://experience.adobe.com).
* Tillhör en programgrupp som är mappad till en företagsgrupp.
* Länka vid behov deras programkonton till deras Adobe ID (beskrivs nedan).

### Valfritt: Länka befintliga användarkonton.

Det är sannolikt att du har användare som redan är medlemmar i programgrupper, till exempel en Analytics-grupp som du tidigare har hanterat i [!UICONTROL Analytics] > [!UICONTROL Admin Tools].

När du mappar de här grupperna till Experience Cloud Enterprise-grupper måste de användarna manuellt länka sina inloggningsuppgifter för programkonton till sina Adobe ID.

Se [Länka konton i Experience Cloud](../administration/organizations.md)

>[!NOTE]
>
>När enterprise- och programgrupper har mappats länkas nya användare automatiskt. (Autentiseringsuppgifter för lösningen skapas automatiskt och länkas till deras Adobe ID.)

I följande avsnitt beskrivs hur du moderniserar implementeringen. Genom att modernisera implementeringen kan du få bastjänster i Experience Cloud.

## Implementera [!UICONTROL Experience Cloud ID Service] {#section_3C9F6DF37C654D939625BB4D485E4354}

[!UICONTROL Experience Cloud ID Service] innehåller ett gemensamt ID för integrering mellan program. Det ger identifiering av besökare över domäner och en sökväg för målinriktning och personalisering mellan olika enheter/webbläsare baserat på CRM-data som överförts via [!UICONTROL Customer Attributes].

Det enklaste sättet att aktivera Experience Cloud bastjänster är att aktivera det automatiskt för Analytics och Adobe Target via [Experience Cloud ID-tjänsttillägget](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html) i [!UICONTROL Experience Platform Launch].

Fullständig hjälp om Experience Cloud ID-tjänsten (tidigare besökar-ID) finns [här](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html#intro).

**Använder inte [!UICONTROL Experience Platform tags]?**

Om du inte använder [!UICONTROL Experience Platform tags] implementerar du ID-tjänsten manuellt via JavaScript-distributionen (`VisitorAPI.js`) enligt följande:

| Uppgift | Beskrivning |
| -----------| ---------- |  
| [Implementera Experience Cloud ID-tjänsten för analyser](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html) | Adobe rekommenderar även att du anger ytterligare [kund-ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html). Dessa ID:n är kopplade till varje besökare och aktiverar nuvarande och framtida funktioner i Experience Cloud. |
| Uppdatera din befintliga `s_code` till version H.27.3 eller senare, eller din befintliga `AppMeasurement.js` till version 1.4 eller senare. | De här filerna är tillgängliga för hämtning i [Code Manager](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html) i Analytics Admin Tools. (Guiden [JavaScript-implementering](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html#js) är tillgänglig om du behöver mer information om `AppMeasurement.js`.) |

{style="table-layout:auto"}

### Analytics &amp; Adobe Target - synkronisera kund-ID {#section_AD473A6A21C1446498E700363F9A8437}

Som en del av konfigurationen av tjänsten Experience Cloud ID rekommenderar Adobe att du synkroniserar dina [kund-ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) med Experience Cloud för Analytics och [!DNL Target].

I Adobe Target måste `mbox3rdpartyid` hämta kundens ID och skicka det till [!DNL Target]. (Se [Arbeta med kundattribut](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) i [!DNL Target].)

När en besökare autentiserar sig på din webbplats, eller på annat sätt identifierar sig själv, måste din implementering visa den personens CRM-kund-ID för sidan eller appen. Sedan kan du använda rätt funktionsanrop för att synkronisera ditt kund-ID med Experience Cloud. Den här synkroniseringen lagrar besökarens CRM-kund-ID i Experience Cloud och aktiverar kundens attribut för användning i Experience Cloud.

Anta till exempel att Bob har kund-ID `52mc210tr42` i ditt CRM-system. När Bob autentiserar på din webbplats måste du visa detta ID på sidan och använda ID:t för att synkronisera det på något av två sätt:

* Anropa `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` med tjänsten för besökar-ID. Eller
* Fyll i *`Customer ID (52mc210tr42)`* i ett utkast eller en eVar.

Kund-ID måste anges för varje [!DNL Analytics]-serveranrop där Kund-ID är känt.

#### Analys: synkronisera kund-ID:t med bakåtfyllningsmetoden för Data Warehouse

När kundattribut blev tillgängliga hade vissa kunder ännu inte implementerat tjänsten Experience Cloud ID och kunde inte använda kundattribut på ett enkelt sätt. För att lösa detta problem har Adobe skapat ett sätt att göra en bakåtfyllning av ID-synk med Adobe Analytics-Datan Warehouse. Den här funktionen kallas för bakfyllning av Data Warehouse. Bakåtfyllning av Data Warehouse är nu i allmänhet inte nödvändig och därför kommer den inte längre att vara tillgänglig från och med oktober 2022.


### SDK för mobiler

I avsnittet *Experience Cloud ID-tjänst* finns syntaxexempel på hur du anger ytterligare kund-ID i [Android™](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html)- och [iOS](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html)-mobilprogram.

### Aktivera attribut för historiska data

Kundattributdata blir tillgängliga när besökarna loggar in. Om du ännu inte har implementerat ID-tjänsten, och om du historiskt har spårat kund-ID:n i en säljare eller eVar, kan du begära en process som skickar historiska inloggningar till Experience Cloud. Med den här processen kan du börja använda kundattribut direkt.

Kontakta kundtjänst om du vill aktivera historikdata.

## Mappa rapportsviter till en Experience Cloud-organisation {#section_7B08516B01BA421681DF03D0E86CE3BA}

>[!NOTE]
>
>Rapportsvitens mappningsfunktion togs bort i november 2020. Kontakta kundsupporten om du har frågor.

Experience Cloud-tjänster (som Experience Cloud ID-tjänsten och [!UICONTROL People service]) är kopplade till en Experience Cloud-organisation i stället för till en enskild Analytics-rapportserie. För att dessa tjänster ska fungera på rätt sätt måste varje analysrapport mappas till en Experience Cloud-organisation.

## Uppdatera Analytics-AppMeasurementen {#section_1798D9D0F05C47E29816AC4EEB9A0913}

Om du använder cookies från första part läser du [CNAME och Experience Cloud ID-tjänsten](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/cname.html) för information om datainsamling-CNAME och spårning mellan domäner.

Vi rekommenderar att du moderniserar implementeringen av Analytics genom att uppdatera dina JavaScript-bibliotek, inklusive Visitor API. Det enkla sättet att uppnå detta är att lägga till ett [Adobe Analytics-tillägg](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html) i datainsamlingen i Experience Platform.

## Uppdatera implementeringen av Adobe Target {#section_C2F4493C7A36406DAE2266B429A4BD24}

* Vi rekommenderar att du lägger till ett [Adobe Target-tillägg](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target-v2/overview.html) i [!UICONTROL Experience Platform] -taggar så att bibliotekshämtningen sker automatiskt. Du kan också konfigurera [Experience Cloud ID-tjänsttillägget](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html) för Adobe Target (och andra program) med [!UICONTROL Experience Platform] -taggar. [!UICONTROL Experience Cloud ID Service]-uppdateringen **krävs** för att Adobe Target ska kunna använda persontjänsterna.
* Om du inte använder [!UICONTROL Experience Platform]-taggar [uppdaterar du mbox-biblioteket](https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/implement-target-for-client-side-web.html) manuellt.
* Begär åtkomst att använda Adobe Analytics som rapportkälla för [!DNL Adobe Target]. [!DNL Target]- och [!DNL Analytics]-data kombineras på samma serveranrop under bearbetningen så att besökarna är anslutna mellan de två programmen. Se [Analyser för målinriktad implementering](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html).

  >[!IMPORTANT]
  >
  >Alla Analytics-kunder har redan etablerats för bastjänster som kundattribut. Om du inte är Analytics-kund kontaktar du kundtjänst för att begära att få etableras.

## Verifiera implementeringen {#section_E641782A0F4F44AF8C9C91216BE330D5}

Använd följande process för att se till att Experience Cloud ID-tjänsten implementeras korrekt på din webbplats.

1. Rensa cookies för din webbplats så att du kan se begäran till Experience Cloud ID-tjänsten (begäran görs vid första besöket och sedan en gång per besökare per vecka).
1. Använd en paketanalyserare eller nätverkspanelen i en webbläsarfelsökare för att leta efter en begäran som går till [!DNL dpm.demdex.net].
1. Kontrollera att svaret innehåller `d_mid` och ett värde, till exempel: `_setMarketingCloudFields({"d_mid":"4235...`
1. Kontrollera att Analytics-begäran innehåller parametern `mid` (Experience Cloud-ID). Under respitperioden (om den är aktiverad) ska du även se en `aid`-parameter (Analytics-besökar-ID).

Förväntat svar som innehåller Experience Cloud-ID:

![Förväntat svar som innehåller Experience Cloud-ID](../assets/mac_id_response.png)

Analysbildbegäran som innehåller Experience Cloud-ID (kallas även `mid` eller _besökar-ID_):

![Analysbildbegäran som innehåller Experience Cloud-ID:t](../assets/mid.png)

Experience Cloud ID i mbox-begäran:

![Experience Cloud-ID i mbox-begäran](../assets/mbox_request.png)

### Hur lång är fristen?

När du har distribuerat Experience Cloud ID-tjänsten får nya besökare inte längre något Experience Cloud-ID för Analytics från din datainsamlingsserver. Om delar av din webbplats ännu inte har implementerat ID-tjänsten identifieras inte Experience Cloud-ID:t när besökare bläddrar till de här avsnitten och besökarna tilldelas ett äldre besökar-ID för Analytics. Detta kan orsaka potentiella problem, inklusive dubblettbesök och felaktig attribuering.

Om supportavsnittet på din webbplats till exempel hanteras i en separat CMS kan du ha en annan Analytics JavaScript-fil för det här avsnittet. Om du distribuerar Experience Cloud ID på huvudwebbplatsen innan du distribuerar ID-tjänsten till supportwebbplatsen får nya besökare ett äldre Analytics ID när de besöker supportavsnittet. Besök som spänner över båda webbplatsavsnitten rapporteras som olika besök.

Distribuering av Experience Cloud ID-tjänsten på webbplatser som använder flera JavaScript-filer eller andra tekniker (till exempel Flash) kan orsaka problem med samordningen. Dessa problem uppstår eftersom du måste aktivera Experience Cloud ID-tjänsten på alla delar av platsen samtidigt. Genom att konfigurera en respitperiod kan nya besökare fortsätta att ta emot ett besökar-ID för Analytics från ID-tjänsten. Besökare kan identifieras på ett konsekvent sätt i avsnitt på platsen som inte har uppgraderats för att använda besökar-ID-tjänsten.

## Hantera användare och produkter {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

När du är igång går du till [Admin Console](https://adminconsole.adobe.com/) där du kan hantera användare och produktprofiler.

![Åtkomst till Admin Console](../assets/menu-administration-shell.png)

### Kundattribut

Användare som läggs till i gruppen [!UICONTROL Customer Attributes] kan se menyalternativet [!UICONTROL Customer Attributes] till vänster om Experience Cloud.

## Börja dela attribut och målgruppsdata {#section_960C06093623462E8EA247B3E97274A1}

Utnyttja följande funktioner.

### [!UICONTROL People] > [!UICONTROL Customer Attributes]

Om du samlar in data om företagskunder i en CRM-databas (customer relationship management) kan du överföra dessa data till en datakälla för kundattribut i Experience Cloud. Använd data i [!DNL Adobe Analytics] och [!DNL Adobe Target] när de har överförts.

Mer information finns i [Kundattribut](customer-attributes/attributes.md).

### [!UICONTROL People] > [!UICONTROL Audience Library]

Experience Cloud [!UICONTROL Audiences] är det gränssnitt som gör att du kan skapa målgrupper, kombinera befintliga målgrupper för att skapa sammansatta målgrupper och visa alla delade målgrupper.

Mer information finns i [Publiker](audiences/overview.md).

## Datalagring och sekretess

Om du använder målgruppsprofilering i realtid och andra bastjänster i Adobe [!DNL Experience Cloud], kan användningen av dessa tjänster påverka vilket datacenter (och vilket land) dina data finns i. Eftersom [!DNL Experience Cloud] använder Audience Manager måste data som används i tjänsten [!UICONTROL People] finnas i Audience Manager-servrar i USA.

När du använder tjänster som är tillgängliga via tjänsten [!UICONTROL People] är de typer av data som skickas från andra Adobe-produkter till målgruppshantering:

* [!DNL Analytics] nyckel-/värdepar (props, eVars, list var o.s.v.). Som standard innehåller loggraderna IP-adress, inklusive IP-adressens sista oktett (förutsatt att IP-adressen inte ändrades av inställningarna för IP-förfalskning i Adobe [!DNL Analytics]).
* Fackar och segment som besökare är kvalificerade för baserat på regler som har upprättats i Audience Manager.
* (Valfritt) Ett eller flera ID:n. Beroende på din implementering av ID-tjänsten kan du även skicka in ett eller flera av dina ID:n, till exempel CRM-ID:n eller hash-kodade e-postadresser. Om dessa data skickas till Adobe [!DNL Analytics] överförs de till Adobe målgruppshantering. Adobe rekommenderar att du inte skickar personuppgifter till Adobe [!DNL Analytics]. Använd i stället en envägshash för att maskera data innan de skickas till Adobe.
* Segment med ursprung i [!DNL Analytics] via segmentdelningskapaciteten i bakände
* demdex.net cookie anges om cookies från tredje part inte blockeras. Den `AMCV_###@AdobeOrg` första part-cookien har alltid angetts med Experience Cloud ID-tjänsten.

Alla dessa dataelement levereras till Adobe Audience Manager som loggfiler. Audience Manager bearbetar och lagrar dessa data i USA. Audience Manager har inget alternativ för att lagra eller bearbeta dessa data utanför USA.
