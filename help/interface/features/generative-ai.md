---
title: AI i Experience Cloud-program
description: Läs om hur Experience Cloud-program använder generativ AI- och AI-assistent.
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
hide: false
hidefromtoc: true
index: n
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 4d784762d7d533b672e0cfa6944a3f26ebca0eaa
workflow-type: tm+mt
source-wordcount: '1994'
ht-degree: 3%

---

# AI i Experience Cloud-program

På den här sidan får du hjälp att förstå hur Experience Cloud-program använder generativ AI och var du kan hitta programspecifik information. Lär dig mer om klasser med frågor, frågor, indata- och utdatamodeller.

## Om generativ AI- och AI-assistent

Generativ AI är en typ av artificiell intelligens som kan _skapa_ nytt innehåll och _svara_ på dina satser och frågor (uppmaningar):

* **Skapa:** Avser AI:ns möjlighet att generera nytt innehåll (text, bilder, musik eller videor) från grunden, baserat på utbildning och inmatningsanvisningar. Den här möjligheten är den _generativa_ aspekten av generativ AI.

* **Svara:** Avser AI som ger ett svar eller en reaktion på en viss fråga, ett visst uttryck eller en viss fråga, eller en viss fråga, som vanligtvis bygger på dess kunskaper eller resonansfunktioner.

Vissa Experience Cloud-program utnyttjar generativ AI, vilket hjälper nya användare att snabbt få produktkunskaper och erfarna användare upptäcker driftsinsikter på några sekunder istället för timmar.

### AI-assistenten

[AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing) är ett konversationsverktyg som stöds i Experience Platform och relaterade program. Använd det för att snabba upp arbetsflödena, förbättra produktkunskapen, felsöka problem eller söka i informationen. Med AI Assistant kan du identifiera driftsinsikter på några sekunder, i stället för timmar.

Alla svar på produktkännedom kan verifieras och citeras med länkar till produktdokumentation i Experience League. [Lär dig mer om AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) och de olika typerna av målinriktade tips som hjälper dig att få ut så mycket som möjligt av AI Assistant.

## Experience Cloud-program som använder AI

>[!TIP]
>
>Subhead-version (endast en start)..


* [Adobe GenStudio for Performance Marketing](#gspm)
* [Adobe Experience Manager Sites (Cloud Service)](#aem-sites)
* [Adobe Journey Optimizer](#journey-optimizer)
* [Adobe Journey Optimizer Prime och Ultimate](#ajo-prime-ultimate)

### GenStudio för prestationsbaserad marknadsföring {#gspm}

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) är en generativ AI-driven plattform. Den ger innehållsframtagningen en livscykel med generativa AI-funktioner som förändrar hur marknadsföringsmaterial skapas, granskas, delas och analyseras.

_GenStudio for Performance Marketing Create_ utnyttjar kraften i Adobe GenAI för att göra det möjligt för marknadsförare och utspridda team att skapa högpresterande varumärkesanpassade upplevelser. Generera innehåll för:

* E-post
* Meta ads
* LinkedIn-annonser
* Visa annonser
* Banderoller

Ni kan utbilda GenStudio for Performance Marketing om ert varumärke med hjälp av exempel, beskrivningar av kundprofiler och produkter samt varumärkesriktlinjer. [Läs mer.](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)

**Kompatibilitet med Adobe Firefly:** planerad

### Experience Manager Sites {#aem-sites}

AEM Sites använder [Generera variationer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). Generate Variations använder generativ AI för att skapa innehållsvariationer baserat på uppmaningar. Dessa uppmaningar tillhandahålls antingen av [Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) eller skapas och hanteras av [användare](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt).

När du har skapat varianter kan du använda innehållet på webbplatsen och mäta hur det fungerar med Experimentationsfunktionen i Edge Delivery Services.

**Indata:** Indatafält innehåller:

* Antal variationer att generera
* Audience Source
* Målgrupp
* Ytterligare sammanhang
* Kunddrivna uppmaningar

**Utdata:** Genererat innehåll/marknadskopia. Du kan också generera bilder i Adobe Express med Firefly generativa AI-funktioner.

Se [Generera bild](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image).

**Kompatibilitet med Adobe Firefly:** Ja

## Journey Optimizer {#journey-optimizer}

Journey Optimizer använder [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) med två frågeklasser:

**Produktkunskap** - Frågar Adobe datalager (t.ex. Experience League produktdokumentation) efter produktinformation. Resultatet är kundagnostiker. Exempel:

* Hur många aktiva aktiviteter kan jag ha i en Adobe Journey Optimizer-sandlåda?

**Operational Insights (Beta)** - Frågar ett kundspecifikt datalager för operativa insikter som innehåller centraliserade driftdata om resor, som partitioneras av kundens sandlåda. Hämtar endast metadata från affärsobjekt och får inte åtkomst till data i sandlådan.

* Hur många resor har skapats de senaste sju dagarna?

Operativa insikter som skapas beror på metadata som hämtas från kundens affärsobjekt.

Resor är det enda tillgängliga objektet för AI Assistant i Journey Optimizer, och metadata hämtas från den aktuella sandlådan.

Mer information finns i [Arbeta med AI-assistenten](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) och [Fältberedskap](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11).

**Kompatibilitet med Adobe Firefly:** Nej

## Journey Optimizer Prime och Ultimate {#ajo-prime-ultimate}

Journey Optimizer Prime och Ultimate använder [AI Assistant för Content Accelerator](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) för att ge proaktiva variantförslag för text och bilder.

Den här funktionen är tillgänglig för e-post-, push-, webb- och SMS-kanaler. Den ger snabb generering av text och bilder.

**E-post** - generera ett fullständigt e-postmeddelande, endast text eller endast bild. [Läs mer...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email)

**Push-meddelande** - Generera ett fullständigt push-meddelande, endast text eller endast bild. [Läs mer...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push)

**SMS** - Generera ett fullständigt SMS eller endast text. [Läs mer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms)

**Webbsida** - Generera webbsidesbilder eller webbsidestext. [Läs mer...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web)

**Innehåll** - Generera innehåll för olika meddelandekampanjer. [Läs mer...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)

**Obs!** Utdata från Content Accelerator i AJO Prime och Ultimate är ersättningsberättigande.

**Kompatibilitet med Adobe Firefly:** Ja

## Journey Optimizer B2B-version {#ajo-b2b}

[AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) används för frågor om produktkunskap.

**Produktkunskap** - Frågar Adobe datalager (t.ex. Experience League produktdokumentation) efter produktinformation. Resultatet är kundagnostiker. | <ul><li>**Indata:** Hur skickar jag ett e-postmeddelande under en kontoresa?</li><li>**Utdata:** Produktinformation hämtas från Experience League (offentlig dokumentation). [Läs mer...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul>   | Nej   |

## Experience Cloud-program som använder AI

>[!TIP]
>
>Tabellversion...


Läs om hur Experience Cloud-program använder generativ AI- eller AI-assistent och om Adobe Firefly stöds.

| Program | Hur generativ AI används | Exempel | Adobe Firefly? |
|----------|------------|-----------|----------------|
| GenStudio för prestationsbaserad marknadsföring | [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) är en generativ AI-driven plattform. Den ger innehållsframtagningen en livscykel med generativa AI-funktioner som förändrar hur marknadsföringsmaterial skapas, granskas, delas och analyseras.<br>Du kan utbilda GenStudio for Performance Marketing om ditt varumärke med hjälp av exempel, beskrivningar av kundprofiler och produkter samt varumärkesriktlinjer. | Med _GenStudio for Performance Marketing Create_ kan du generera innehåll för e-post, Meta-annonser, LinkedIn-annonser, visningsannonser och banners. <br>**Indata:** <ul><li>Använd mallar för att börja skapa innehåll. </li><li>Lägg till parametrar som Varumärke, Produkter och Personas (riktlinjer) och Innehåll (resurser) för att utforma den genererade upplevelsen. </li><li>Ange beskrivande uppmaningar som beskriver sammanhanget eller upplevelsen som du tänker generera. [Läs mer...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)</li></ul> | Ja |
| Adobe Experience Manager Sites (Cloud Service) | AEM Sites använder [Generera variationer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). <br>Generera variationer använder generativ AI för att skapa innehållsvariationer baserat på uppmaningar. Dessa uppmaningar tillhandahålls antingen av Adobe eller skapas och hanteras av användare. | När du har skapat varianter kan du använda innehållet på webbplatsen och mäta hur det fungerar med Experimentationsfunktionen i Edge Delivery Services. <br>**Indata:** Indatafälten innehåller antal variationer som ska genereras, målgrupps-Source/målgruppsmål, ytterligare kontext och kunddrivna uppmaningar. <ul><li>[Adobe-promptmall](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) </li><li>[Användargenererad fråga](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)</li></ul> **Utdata:** Genererat innehåll/marknadskopia. Du kan också generera bilder i Adobe Express med Firefly generativa AI-funktioner. Se [Generera bild](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image). | Ja |
| Adobe Journey Optimizer | Journey Optimizer använder [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) med två frågeklasser:<ul><li>**Produktkunskap** - Frågar Adobe datalager (t.ex. Experience League produktdokumentation) efter produktinformation. Resultatet är kundagnostiker. </li><li>**Operational Insights (Beta)** - Frågar ett kundspecifikt datalager för operativa insikter som innehåller centraliserade driftdata om resor, som partitioneras av kundens sandlåda. Hämtar endast metadata från affärsobjekt och får inte åtkomst till data i sandlådan.</li></ul> | <ul><li>**Produktkunskapsdata:** Hur många aktiva aktiviteter kan jag ha i en Adobe Journey Optimizer-sandlåda?</li><li>**Produkt- och kunskapsutdata:** Produktkunskaper hämtas från Experience League (offentlig dokumentation). </li><li>**Operational Insights-indata:** Hur många resor har skapats de senaste sju dagarna? </li><li>**Operational Insights-utdata:** Operational Insights-utdata är beroende av metadata som hämtas från kundens affärsobjekt. Resor är det enda tillgängliga objektet i AJO, och metadata hämtas från den aktuella sandlådan. </li></ul> Se [Arbeta med AI-assistenten](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) och [Fältberedskap](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) | Nej |
| Journey Optimizer: _Prime_ och _Ultimate_ | [AI Assistant för Content Accelerator](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) ger proaktiva variantförslag för text och bilder. Det är tillgängligt för e-post-, push-, webb- och SMS-kanaler. Den nya funktionen ger snabb generering av text och bilder. | <ul><li> **E-post** - generera ett fullständigt e-postmeddelande, endast text eller endast bild. [Läs mer...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email) </li><li> **Push-meddelande** - Generera ett fullständigt push-meddelande, endast text eller endast bild. [Läs mer...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push) </li><li> **SMS** - Generera ett fullständigt SMS eller endast text. [Läs mer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) </li><li> **Webbsida** - Generera webbsidesbilder eller webbsidestext. [Läs mer...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web) </li><li> **Innehåll** - Generera innehåll för olika meddelandekampanjer. [Läs mer...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)</li></ul> **Obs!** Utdata från Content Accelerator i AJO Prime och Ultimate är ersättningsberättigande. | Ja |
| Journey Optimizer B2B-version | Använder [AI-assistenten](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) med en frågeklass: <br> **Produktkunskap** - Frågar Adobe datalager (t.ex. Experience League produktdokumentation) efter produktinformation. Resultatet är kundagnostiker. | <ul><li>**Indata:** Hur skickar jag ett e-postmeddelande under en kontoresa?</li><li>**Utdata:** Produktinformation hämtas från Experience League (offentlig dokumentation). [Läs mer...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul> | Nej |
| Kampanjhanterade molntjänster | [AI Assistant för Content Accelerator](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) genererar automatiskt personaliserat, engagerande och effektivt innehåll baserat på marknadsföringsmålet med innehåll som är optimerat för varumärkesprofilerade format, layouter, färgtoner och mycket annat över kanaler som e-post, SMS, push. | <ul><li> **E-post** - Generera ett fullständigt e-postmeddelande, endast text eller endast bild. [Läs mer](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content) </li><li> **SMS** - Generera endast fullständigt SMS eller text. [Läs mer...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) </li><li> **Tryck** - Skapa övertygande meddelanden och generera innehåll. [Läs mer...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) </li></ul> **Obs!** Utdata från Content Accelerator i Campaign Managed Cloud Services har försäkringsskydd. | Ja |
| Customer Journey Analytics | CJA använder [AI Assistant](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) för att hjälpa dig att identifiera produktkunskaper och insikter från Experience League. <br>Nya användare kan till exempel använda den för att lära sig Customer Journey Analytics koncept och ta in sig själv i produkter och funktioner som du inte är bekant med. <br>Erfarna användare kan använda AI Assistant för att visa mer avancerade användningsfall eller tips och tricks och utföra uppgifter i snabb takt. Förstå koncept, felsök problem eller sök efter information. [Läs mer...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge) | <ul><li>**Produktkunskapsdata:** Hur skapar jag ett beräknat mätvärde? </li><li> **Produkt- och kunskapsutdata:** Produktkunskaper hämtas från Experience League (offentlig dokumentation). </li></ul> | Nej |
| Customer Journey Analytics | [Intelligenta bildtexter](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) ger naturliga språkkunskaper för linjevisualiseringar i Workspace-visualiseringar. | <ul><li>**Indata:** Radvisualiseringar. Bildtexter genereras automatiskt baserat på sådana radvisualiseringar när du klickar på **Intelligenta bildtexter**. </li><li> **Utdata:** Automatiskt genererade naturliga språkbeskrivningar.</li></ul> | Nej |
| Real-Time CDP | [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) används för att hjälpa dig att identifiera produktkunskaper och insikter från Experience League. Den frågar en databas och översätter data från databasen till ett läsbart svar. Två frågeklasser: <br> **Produktkunskap** - Frågar Adobe datalager (t.ex. Experience League produktdokumentation) efter produktinformation. Resultatet är kundagnostiker. <br> **Operational Insights (Beta)** - Frågar ett kundspecifikt datalager för operativa insikter som innehåller centraliserade driftdata, som partitioneras av kundens AEP-sandlåda. Hämtar endast metadata från attribut, målgrupper, dataflöden, datauppsättningar, destinationer, scheman och källor och har inte åtkomst till data i sandlådan. <br>För en fråga om en publik kan [!DNL AI Assistant] till exempel komma åt målgruppens namn och andra associerade metadata, men kan inte komma åt profilerna inom den målgruppen. | <ul><li>**Produktkunskapsdata:** Hur beräknas profilrikedomen? </li><li>**Produkt- och kunskapsutdata:** Produktkunskaper hämtas från Experience League (offentlig dokumentation). </li><li> **Operational Insights-indata:** Hur många datauppsättningar har jag? </li><li> **Operational Insights-utdata:** Operational Insights-utdata är beroende av metadata som hämtas från kundens affärsobjekt (attribut, målgrupper, dataflöden, datauppsättningar, destinationer, scheman och källor), och innehåller en länk till en specifik gränssnittssida som innehåller efterfrågade data. </li></ul>Se till exempel indatatabellerna _Produktkunskap_ och _Operational Insights_ i [AI Assistant i Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) | Nej |
| Marketo | [Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) skapar AI-stödda konversationer med anpassade och förgodkända frågor och svar, samt en sammanfattning av konversationer | <ul><li> **Generera frågor:** Ange URL:er som innehållet extraheras från och används för att generera frågor/svar. </li><li> **Konversationssammanfattning:** Skapar en sammanfattning av en chattkonversation. </li></ul> [Läs mer...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library) | Nej |
| Workfront | [AI-assistenten](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) i Workfront hjälper dig att slutföra ditt arbete genom att erbjuda information och förslag i appen i en konversation på ett naturligt språk. AI Assistant har följande funktioner: Sammanfattar projekt/uppgifter/ärenden/dokument, ger instruktioner eller referensinformation som hämtas från Workfront-dokumentationen för Experience League, genererar eller förfinar formler för beräknade anpassade fält. | <ul><li>**Sammanfatta projektindata:** Sammanfatta det här projektet </li><li> **Sammanfatta projektutdata:** Returnerar korta beskrivningar av projektets syfte och status, ger exempel på aktiviteter som är slutförda och som fortfarande väntar samt ger ytterligare information och anteckningar.</li><li> **Generera/förfina formelindata:** &quot;Skriv om formeln för att ta bort det ogiltiga uttrycksfelet.&quot; </li><li> **Generera/förfina formelutdata:** Genererad eller förfinad formel. </li></ul>**Obs!** Det kan ta en stund att generera den reviderade formeln, beroende på formelns storlek och komplexitet. | Nej |
