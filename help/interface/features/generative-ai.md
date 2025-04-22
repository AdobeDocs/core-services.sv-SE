---
title: AI i Experience Cloud-program
description: Läs om hur Experience Cloud-program använder generativ AI- och AI-assistent.
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 7060cc75e06a00dd06475958f94b03ceaf39ae62
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
