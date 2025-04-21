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
source-git-commit: 4c0e9ef974ab31a7d82a61c3a69f7d76389774f9
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 2%

---

# AI i Experience Cloud-program

På den här sidan kan du förstå hur du genererar AI och hur du kan använda det i Experience Cloud-program. Ta reda på vilka produktfunktioner som använder generativ AI, AI Assistant och om Adobe Firefly stöds.

## Om generativ AI- och AI-assistent

Generativ AI är en typ av artificiell intelligens som gör mer än att bara svara på frågor. Det _skapar_-innehåll och _svarar_ på dina _uppmaningar_ (frågor och satser).

* **Skapa:** Avser AI:ns möjlighet att generera nytt innehåll (text, bilder, musik eller videor) från grunden, baserat på utbildning och inmatningsanvisningar. Den här möjligheten är den _generativa_ aspekten av generativ AI.

* **Svara:** Avser AI som ger ett svar eller en reaktion på en viss fråga, vanligtvis baserat på dess kunskaper eller resonansfunktioner.

Om du inte har använt Experience Cloud tidigare kan du använda generativ AI för att snabbt få produktkunskap. Som erfaren användare kan ni identifiera driftsinsikter på några sekunder snarare än timmar.

### AI-assistenten

[AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing) är ett konversationsverktyg som stöds i Experience Platform och relaterade program. Använd det för att snabba upp arbetsflödena, förbättra produktkunskapen, felsöka problem eller söka i informationen. I vissa program kan du med AI Assistant omedelbart upptäcka operativa insikter.

Produktkunskapssvaren från Experience League kan verifieras och citeras med länkar. Lär dig mer om de olika typerna av [målinriktade uppmaningar](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) för att få ut så mycket som möjligt av AI Assistant.

## Program med funktioner som stöder AI

* [GenStudio för prestationsbaserad marknadsföring](#gspm)
* [Generera variationer i AEM Sites (Cloud Service)](#aem-sites)
* [AI Assistant i Journey Optimizer](#journey-optimizer)
* [Adobe Journey Optimizer Prime och Ultimate](#ajo-prime-ultimate)
* [Journey Optimizer B2B-version](#ajo-b2b)
* [AI Assistant i Journey Optimizer Prime och Ultimate](#ajo-prime-ultimate)
* [AI Assistant i Journey Optimizer B2B edition](#ajo-b2b)
* [AI-assistenten i Campaign Managed Cloud Services](#campaign-cs)
* [AI Assistant i Customer Journey Analytics](#cja)
* [Intelligenta bildtexter i Customer Journey Analytics](#cja-captions)
* [AI Assistant i Real-Time CDP](#rtcdp)
* [DYNAMIC CHAT i MARKETO](#marketo)
* [AI Assistant i Workfront](#workfront)

### GenStudio för prestationsbaserad marknadsföring {#gspm}

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) är inte en funktion utan en generativ AI-driven plattform. Dess generativa AI-funktioner förändrar hur marknadsföringsmaterial skapas, granskas, delas och analyseras.

På hemsidan [Skapa](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview) kan du skapa högpresterande varumärkesupplevelser. Generera innehåll för:

* E-post
* Meta ads
* LinkedIn-annonser
* Visa annonser
* Banderoller

Ni kan också utbilda GenStudio for Performance Marketing om ert varumärke med hjälp av exempel, beskrivningar av kundprofiler och produkter samt varumärkesriktlinjer. [Läs mer...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)

**Kompatibel med Adobe Firefly:** Planerad

### Generera variationer i Experience Manager Sites {#aem-sites}

[Generera variationer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations) i AEM Sites använder generativ AI för att skapa innehållsvariationer baserat på uppmaningar. Dessa uppmaningar tillhandahålls antingen av [Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) eller skapas och hanteras av [användare](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt).

När du har skapat varianter kan du använda innehållet på webbplatsen och mäta hur det fungerar med hjälp av Experimentationsfunktionen i Edge Delivery Services.

### Indata- och utdatafält

Indatafält innehåller:

* Antal variationer att generera
* Audience Source
* Målgrupp
* Ytterligare sammanhang
* Kunddrivna uppmaningar

Resultatet genereras innehåll eller marknadskopia.

Du kan också generera bilder i Adobe Express med Firefly generativa AI-funktioner. [Läs mer...](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image)

**Kompatibel med Adobe Firefly:** Ja

## AI Assistant i Journey Optimizer {#journey-optimizer}

I Journey Optimizer kan AI Assistant hjälpa dig att få produktkunskaper och driftsinsikter.

**Produktkunskap:** AI Assistant frågar Adobe datalager (t.ex. Experience League produktdokumentation) efter produktinformation. Resultatet är kundagnostiker.

Exempel:

* _Hur många aktiva aktiviteter kan jag ha i en Adobe Journey Optimizer-sandlåda?_

**Operational Insights (Beta)** - AI Assistant frågar efter ett kundspecifikt datalager med driftsinsikter som innehåller centraliserade driftdata om resor, som partitioneras av kundens sandlåda. Den här funktionen hämtar endast metadata från affärsobjekt och får inte åtkomst till data i sandlådan.

Exempelfråga:

* _Hur många resor har skapats de senaste sju dagarna?_

Operativa insikter som skapas beror på metadata som hämtas från kundens affärsobjekt. Resultatet är kundagnostiker.

_Resor_ är det enda tillgängliga objektet för AI Assistant i Journey Optimizer, och metadata hämtas från den aktuella sandlådan. [Läs mer..](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant).

**Kompatibel med Adobe Firefly:** Nej

## AI Assistant i Journey Optimizer Prime och Ultimate {#ajo-prime-ultimate}

Journey Optimizer Prime och Ultimate använder [AI Assistant för Content Accelerator](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) för att ge proaktiva variantförslag för text och bilder.

Den här funktionen är tillgänglig för kanalerna [e-post](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email), [push-meddelanden](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push), [webbsida](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web), [innehåll](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation) och [SMS](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms). Den ger snabb generering av text och bilder.

**Obs!** Utdata från Content Accelerator i AJO Prime och Ultimate är ersättningsberättigande.

**Kompatibel med Adobe Firefly:** Ja

## AI Assistant i Journey Optimizer B2B edition {#ajo-b2b}

Journey Optimizer B2B edition använder [AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview) för att hjälpa dig med produktkunskap, baserat på dina produktkunskapsfrågor.

**Produktkunskap** - Frågar Adobe datalager (t.ex. Experience League produktdokumentation) efter produktinformation. Resultatet är kundagnostiker.

* **Indata:** Hur skickar jag ett e-postmeddelande under en kontoresa?

* **Utdata:** Produktinformation hämtas från Experience League (offentlig dokumentation). [Läs mer...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/question-guidance)

**Kompatibel med Adobe Firefly:** Nej

## AI-assistenten i Campaign Managed Cloud Services {#campaign-cs}

Kampanjhanterade molntjänster använder [AI-assistenten för Content Accelerator](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs). Med den här funktionen kan ni automatiskt generera personaliserat, engagerande och effektivt innehåll baserat på ert marknadsföringsmål, med innehåll som är optimerat för varumärkesanpassade format, layouter, färgtoner med mera. Du kan använda det i flera kanaler, som [email](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content), [SMS](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) och [push](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push).

**Obs!** Utdata från Content Accelerator i Campaign Managed Cloud Services har försäkringsskydd.

**Kompatibel med Adobe Firefly:** Ja

## AI Assistant i Customer Journey Analytics {#cja}

Customer Journey Analytics använder [AI Assistant](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant) för att hjälpa dig att identifiera produktkunskaper och insikter från Experience League.

**Exempelfråga:** Hur skapar jag ett beräknat mått?

Nya användare kan använda den för att lära sig Customer Journey Analytics koncept och ta till sig själv med produkter och funktioner som du inte är bekant med.

Erfarna användare kan använda AI Assistant för att visa upp mer avancerade användningsfall eller tips och tricks och utföra uppgifter i snabb takt. Förstå koncept, felsök problem eller sök efter information. [Läs mer...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge)

**Kompatibel med Adobe Firefly:** Nej

## Intelligenta bildtexter i Customer Journey Analytics {#cja-captions}

[Intelligenta bildtexter](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) i Customer Journey Analytics ger insikter i naturliga språk för de vanligaste Workspace-visualiseringarna.

**Kompatibel med Adobe Firefly:** Nej

## AI Assistant i Real-Time CDP {#rtcdp}

Real-Time CDP använder [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) för att hjälpa dig att identifiera produktkunskaper och insikter från Experience League. [Få tips](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/questions) om hur du ställer frågor.

Här finns även användbara insikter (i betaversion). AI Assistant skickar frågor till ett kundspecifikt datalager med verksamhetsinsikter som innehåller centraliserade driftdata, som partitioneras av kundens AEP-sandlåda. Metadata hämtas endast från Attribut, Publiker, Dataflöden, Datauppsättningar, Destinationer, Scheman och Källor, och de har inte åtkomst till data i sandlådan.

För en fråga om en målgrupp kan till exempel [!DNL AI Assistant] komma åt målgruppens namn och andra associerade metadata, men kan inte komma åt profilerna inom den målgruppen.

Exempel:

* Indata: _Hur många datauppsättningar har jag?_

* Svar: Operational Insights-utdata är beroende av metadata som hämtas från kundens affärsobjekt (attribut, målgrupper, dataflöden, datauppsättningar, destinationer, scheman och källor), och innehåller en länk till en specifik gränssnittssida med efterfrågade data.

Mer exempel finns i indatatabellerna _Produktkunskap_ och _Operational Insights_ i [AI Assistant i Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)

**Kompatibel med Firefly:** Nej

## DYNAMIC CHAT i MARKETO {#marketo}

Med de generativa AI-baserade funktionerna i Adobe Dynamic Chat kan ni optimera produktiviteten för säljarna, få insikter i besökarnas avsikter och besvara besökarnas frågor på ett säkert sätt. Du kan förgodkänna frågorna, svaren och konversationssammanfattningen. [Läs mer...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

**Kompatibel med Firefly:** Nej

## AI Assistant i Workfront {#workfront}

AI Assistant i Workfront hjälper dig att slutföra arbetet genom att erbjuda information och förslag i appen. Du kan:

* Få sammanfattningar av vissa objekt, vilket ger dig en högnivåvy över objektets avsikt eller detaljer.
* Ställ frågor och låt [!DNL AI Assistant] hitta svar på Experience League.
* Hämta genererade formler baserat på dina uppmaningar. Du kan också lösa fel i ogiltiga anpassade uttryck i beräkningsfält.
* Hitta projekt, uppgifter och problem.

[Läs mer...](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

**Kompatibel med Firefly:** Nej

<!-- ## Experience Cloud applications that use AI

Learn how Experience Cloud applications use generative AI or AI Assistant, and whether Adobe Firefly is supported. 

| Application | How Generative AI Is Used | Examples | Adobe Firefly? |
|----------|------------|-----------|----------------|
| GenStudio for Performance Marketing | [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) is a generative AI-driven platform. It infuses the content creation lifecycle with generative AI capabilities that transform how marketing content is created, reviewed, shared, and analyzed.<br>You can train GenStudio for Performance Marketing on your brand using examples, descriptions of customer personas and products, and brand guidelines. |_GenStudio for Performance Marketing Create_ lets you generate content for emails, Meta ads, LinkedIn ads, display ads, and banners. <br>**Inputs:** <ul><li>Use templates to start the content creation process. </li><li>Add parameters like Brands, Products, and Personas (guidelines) and Content (assets) to shape the generated experience. </li><li>Enter descriptive prompts that describe the context or experience you intend to generate. [Learn more...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)</li></ul> |Yes |
|Adobe Experience Manager Sites (Cloud Service)  | AEM Sites uses [Generate Variations](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). <br>Generate Variations uses generative AI to create content variations based on prompts. These prompts are either provided by Adobe or created and managed by users. |After creating variations, you can use the content on your website and measure its success using the Experimentation functionality of Edge Delivery Services. <br>**Input:** Input fields include Number of Variations to generate; Audience Source / Audience Target; Additional Context, and customer-driven prompts. <ul><li>[Adobe prompt template](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) </li><li>[User generated prompt](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)</li></ul> **Output:** Generated Content / Market Copy. You also have the option to generate images in Adobe Express using the generative AI capabilities of Firefly. See [Generate Image](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image). | Yes|
| Adobe Journey Optimizer |Journey Optimizer uses [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) with two classes of questions:<ul><li>**Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. </li><li>**Operational Insights (Beta)** - queries a customer-specific operational insights data store that contains centralized operational data about Journeys, partitioned by the customer's sandbox. Pulls metadata only from business objects and does not access data within the sandbox.</li></ul>|<ul><li>**Product Knowledge Input:** How many live activities can I have in one Adobe Journey Optimizer sandbox?</li><li>**Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li><li>**Operational Insights Input:** How many Journeys have been created in the last seven days? </li><li>**Operational Insights Output:** Operational Insights output depends on metadata pulled from customer's business objects. Journeys is the only object available in AJO, and metadata is pulled from the current sandbox. </li></ul> See [Work with the AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) and [Field Readiness](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) | No |
| Journey Optimizer: _Prime_ and _Ultimate_  | [AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) brings proactive content variation suggestions for text and images. It is available for email, push, web and SMS channels. This new capability provides prompt-based text and image generation. |<ul><li> **Email** - generate a full email, text only or image only. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email) </li><li> **Push Notification** - Generate a full push notification, text only or image only. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push) </li><li> **SMS** - Generate a full SMS, or text only. [Learn more](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) </li><li> **Webpage** - Generate web page images or web page text. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web) </li><li> **Content** - Generate content for various messaging campaigns. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)</li></ul> **Note:** Output from Content Accelerator in AJO Prime and Ultimate is indemnified. | Yes   |
| Journey Optimizer B2B Edition  | Uses [AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) with one class of questions: <br> **Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. | <ul><li>**Input:** How do I send an email in an account journey?</li><li>**Output:** Product Knowledge pulls from Experience League (public documentation). [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul>   | No   |
| Campaign Managed Cloud Services | [AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) auto-generates personalized, engaging, and effective content based on the marketing objective with content optimized for brand outlined styles, layouts, tone, and more across channels like Email, SMS, Push. |<ul><li> **Email** - Generate a full email, text only or image only. [Learn more](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content) </li><li> **SMS** - Generate full SMS or text only. [Learn more...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) </li><li> **Push** - Craft compelling messaging and generate content. [Learn more...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) </li></ul> **Note:** Output from Content Accelerator in Campaign Managed Cloud Services is indemnified. | Yes  |
| Customer Journey Analytics   | CJA uses [AI Assistant](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) to help you discover product knowledge and insights from Experience League. <br>For example, new users can use it to learn Customer Journey Analytics concepts and onboard yourself to products and features that you are unfamiliar with. <br>Experienced users can use AI Assistant to present more advanced use cases or tips and tricks and perform tasks at a fast pace. Understand concepts, troubleshoot problems, or search for information. [Learn more...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge) | <ul><li>**Product Knowledge Input:** How do I build a calculated metric? </li><li> **Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li></ul> | No |
| Customer Journey Analytics    | [Intelligent Captions](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) provides natural-language insights for line visualizations in Workspace visualizations.| <ul><li>**Input:** Line visualizations. Captions are auto-generated based on such line visualizations when you click **Intelligent captions**. </li><li> **Output:** Auto-generated natural-language captions.</li></ul>  | No             |
| Real-Time CDP |Uses [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) to help you discover product knowledge and insights from Experience League. It queries a database and translates data from the database into a human-readable answer. Two classes of questions: <br> **Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. <br> **Operational Insights (Beta)** - Queries a customer-specific operational insights data store that contains centralized operational data, partitioned by the customer's AEP sandbox. Pulls metadata only from Attributes, Audiences, Dataflows, Datasets, Destinations, Schemas, and Sources, and does not access data within the sandbox. <br>For example, for a query about an audience [!DNL AI Assistant] can access the name of the audience and other associated metadata but cannot access the profiles within that audience. | <ul><li>**Product Knowledge Input:** How is profile richness calculated? </li><li>**Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li><li> **Operational Insights Input:** How many datasets do I have? </li><li> **Operational Insights Output:** Operational Insights output depends on metadata pulled from Customer's business objects (Attributes, Audiences, Dataflows, Datasets, Destinations, Schemas, and Sources), and includes a link to specific UI page containing queried data. </li></ul>For examples, see the _Product Knowledge_ and _Operational Insights_ input tables in [AI Assistant in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)  | No |
| Marketo  | [Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) creates AI-assisted conversations with customized and pre-approved questions and answers, as well as conversation summary |<ul><li> **Generate Questions:** Provide URLs from which content is extracted and used to generate questions / responses. </li><li> **Conversation Summary:** Generates a summary of a chat conversation. </li></ul> [Learn more...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library)  | No |
| Workfront | [AI Assistant](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) in Workfront helps you accomplish your work by offering in-app information and suggestions in a natural-language conversation. AI Assistant offers the following functionality: Summarizes projects/tasks/issues/documents, provides instructions or reference information pulled from the Workfront documentation on Experience League, generates or refines formulas for calculated custom fields.  | <ul><li>**Summarize Project Input:** Summarize this project </li><li> **Summarize Project Output:** Returns brief descriptions of the project's purpose and status, gives examples of tasks that are completed and that are still pending, and provides some additional details and notes.</li><li> **Generate/Refine Formula Input:** "Rewrite this formula to remove the invalid expression error." </li><li> **Generate/Refine Formula Output:** Generated or refined formula. </li></ul>**Note:** AI Assistant may take a few moments to generate the revised formula, depending on the size and complexity of the formula. | No  | -->
