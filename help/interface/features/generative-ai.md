---
title: AI i Experience Cloud-program
description: Läs mer om generativ AI och hur Experience Cloud-program använder genAI och [!DNL AI Assistant].
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: cadc0d7eaaa9acb868f96561c2a562d9d29fc9ac
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 2%

---

# AI i Experience Cloud-produkter

På den här sidan kan du lära dig vilka produkter som stöder generativ AI, [!DNL AI Assistant] och om Adobe Firefly är kompatibelt. Du kan även hitta länkar till produktspecifika hjälpresurser om hur du använder AI i Experience Cloud.

**Om generativ AI**

Generativ AI är en typ av artificiell intelligens som gör mer än att bara svara på frågor. Den kan _skapa_ innehåll och _generera ett svar_ på dina frågor eller satser (kallas _uppmaningar_).

* **Skapa:** Möjlighet att generera innehåll (text, bilder, musik eller videor) från grunden, baserat på utbildning och inmatningsanvisningar. Den här möjligheten är den _generativa_ aspekten av generativ AI.

* **Generera ett svar:** AI ger ett svar eller en reaktion på en fråga, som vanligtvis baseras på tillgängliga data- och kunskapsdatabaser.

**Vad är [!DNL AI Assistant]?**

[!DNL AI Assistant] är ett konversationsverktyg som stöds i Experience Platform och relaterade program. Använd den för att snabbt få _produktkunskap_ och, i program som stöds, få _driftsinsikter_ nästan omedelbart.

* **Produktkunskap:** Produktkunskap syftar på begrepp och ämnen som beskrivs i Experience League-dokumentationen. Svar från Experience League kan verifieras och anges med länkar. Lär dig mer om de olika typerna av [målinriktade uppmaningar](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) för att få ut det mesta av [!DNL AI Assistant].

* **Driftsinsikter:** Driftsinsikter refererar till svar AI Assistant genererar om dina metadata-objekt (attribut, målgrupper, dataflöden, datauppsättningar, destinationer, resor, scheman och källor), inklusive antal, sökningar och linjepåverkan. Med hjälp av AI Assistant kan du identifiera driftsinsikter på några sekunder istället för timmar.

[Läs mer](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

**Dina data är fortfarande dina**

I AI Assistant är säkerhet högsta prioritet:

* Kunddata används inte för att utbilda språkmodeller.
* AI Assistant tittar bara på de dokument du skickar till den. Du har kontrollen.
* Dina medarbetare kan bara använda AI Assistant för dokument som de har tillgång till.
* Det är granskningsklart: Svaren kan tillskrivas källdokument.
* Enterprise-kontroller finns för att hantera vem som har AI-åtkomst i företaget.

## AI-tillgänglighet i Experience Cloud-produkter

Läs om stöd för generativ AI eller [!DNL AI Assistant] i Experience Cloud-produkter. Support för Adobe Firefly anges också.

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager Sites]](#aem-sites)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign] Managed Services (Campaign v8 Web)](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Customer Journey Analytics]](#cja-captions)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## Adobe GenStudio for Performance Marketing {#gspm}

[!DNL GenStudio for Performance Marketing] är en AI-driven plattform som ger dig möjlighet att generera och hantera marknadsföringsinnehåll som följer varumärkesstandarderna och följer företagets policyer. Generera material för e-post, Meta-annonser, LinkedIn-annonser, displayannonser och banners.

Ni kan också utbilda GenStudio for Performance Marketing om ert varumärke med hjälp av exempel, beskrivningar av kundprofiler och produkter samt varumärkesriktlinjer.

[Läs mer](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home)

Kompatibilitet med Adobe Firefly: **Ja**

## Adobe [!DNL Experience Manager Sites] {#aem-sites}

I AEM Sites kan du använda _[!UICONTROL Generate Variations]_. Den här funktionen använder generativ artificiell intelligens för att skapa innehållsvariationer baserat på dina inmatningsfrågor. Frågorna tillhandahålls antingen av Adobe eller skapas och hanteras av dig.

När du har skapat varianter kan du använda innehållet på webbplatsen och mäta resultatet med hjälp av funktionen [Experimentation](https://www.aem.live/docs/experimentation) i Edge Delivery Services. Du kan också generera bilder i Adobe Express med Firefly generativa AI-funktioner.

**Exempel på in- och utdata**

Indatafält innehåller:

* Antal variationer att generera
* Audience Source
* Målgrupp
* Ytterligare sammanhang
* Kunddrivna uppmaningar

Resultatet genereras innehåll eller marknadskopia.

[Läs mer om Generera variationer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

Kompatibilitet med Adobe Firefly: **Ja**

## Adobe [!DNL Journey Optimizer] {#journey-optimizer}

I [!DNL Journey Optimizer] (AJO) kan du använda [ AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) för att få _produktkunskap_ och _driftsinsikter_ (beta).

### Exempel på hur du använder AI Assistant i AJO

Här är ett exempel på produktinformation:

* _Hur många aktiva aktiviteter kan jag ha i en Journey Optimizer-sandlåda?_

  Utdata genereras från Experience League och andra Adobe datalager.

Här är ett exempel på indata för driftsinsikter:

* _Hur många resor har skapats de senaste sju dagarna?_

  AI Assistant hämtar utdata från ett kundspecifikt datalager. Datalagret innehåller centraliserade, driftsdata om [!UICONTROL Journeys]. Den här funktionen är kundagnostiker och hämtar endast metadata från affärsobjekt. Den har inte åtkomst till data i din sandlåda.

[Läs mer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant).

Kompatibilitet med Adobe Firefly: **Nej**

### AI Assistant för innehållsgenerering (AJO Prime och Ultimate) {#ajo-prime}

I AJO _Prime_ och _Ultimate_ kan du använda [innehållsgenerering](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) för innehållsgenerering för att ge proaktiva variantförslag för text och bilder.

Den här funktionen är tillgänglig för e-post, push-meddelanden, webbsidor, innehåll och SMS-kanaler. Den ger snabb generering av text och bilder. Utdata från innehållsgenerering i AJO Prime och Ultimate är ersättningsberättigande.

[Läs mer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Kompatibilitet med Adobe Firefly: **Ja**

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition använder [!DNL AI Assistant] för att hjälpa dig med produktkännedom.

Exempelindata:

* _Hur skickar jag ett e-postmeddelande i en kontoresa?_

  Produkternas kunskapsresultat hämtas från Experience League.

[Läs mer](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Kompatibilitet med Adobe Firefly: **Nej**

## [!DNL Campaign] Managed Services (Campaign v8 Web) {#campaign-cs}

Campaign v8 (Campaign Managed Cloud Services) använder [!DNL AI Assistant] för innehållsgenerering. Med den här funktionen kan ni automatiskt generera personaliserat, engagerande och effektivt innehåll baserat på ert marknadsföringsmål, med innehåll som är optimerat för varumärkesanpassade format, layouter, färgtoner med mera. Ni kan använda det i alla kanaler, som e-post, SMS och push.

**Obs!** Utdata från innehållsgenerering i Campaign Managed Cloud Services har försäkringsskydd.

[Läs mer](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Kompatibilitet med Adobe Firefly: **Ja**

## [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analytics använder [!DNL AI Assistant] för att hjälpa dig att identifiera produktkunskaper och insikter från Experience League.

Om du är ny som användare kan du snabbt lära dig Customer Journey Analytics koncept och ta dig an produkter och funktioner. Exempel:

* _Hur skickar jag ett e-postmeddelande i en kontoresa?_

Erfarna användare får avancerade användningsexempel eller lär sig strategier för att utföra uppgifter i snabb takt. Du kan snabbt förstå koncept, felsöka problem eller söka efter information.

[Läs mer](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

Kompatibilitet med Adobe Firefly: **Nej**

## [!DNL Customer Journey Analytics] {#cja-captions}

Du kan använda _Intelligenta bildtexter_ i [!DNL Customer Journey Analytics] för att få naturtrogna språkkunskaper för de vanligaste Workspace-visualiseringarna. Intelligenta bildtexter är idealiska för analytiker som behöver berättarröster och sammanhang för att dela med andra användare. Affärsanvändare kan använda den för att snabbt upptäcka högnivåaktiviteter.

Exempel:

* **Indata:** I CJA kör du en visualisering som stöds (inklusive Line, Area, Bar, Flow eller Fallout) och klickar sedan på **[!UICONTROL Intelligent captions]**.

* **Utdata:** Visa automatiskt genererade, naturliga språkbeskrivningar som visar sammanhang och viktiga uppgifter. Sedan kan du vidta åtgärder för genererade data, till exempel granska, kopiera och dela dem med din organisation. [Se hur](https://video.tv.adobe.com/v/3420131/?quality=12&learn=on#_blank)

[Läs mer](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

Kompatibilitet med Adobe Firefly: **Nej**

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDP använder [!DNL AI Assistant] för att hjälpa dig med produktkunskaper från Experience League. Här finns även användbara insikter (i betaversion). [!DNL AI Assistant] frågar efter ett kundspecifikt datalager med verksamhetsinsikter som innehåller centraliserade driftdata, som är partitionerat i din AEP-sandlåda. Systemet hämtar endast metadata från attribut, målgrupper, dataflöden, datauppsättningar, destinationer, scheman och källor och har inte åtkomst till data i sandlådan.

Om du till exempel frågar efter en publik kan [!DNL AI Assistant] komma åt målgruppens namn och andra associerade metadata, men inte komma åt profilerna inom den målgruppen.

[Läs mer](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)

Kompatibilitet med Adobe Firefly: **Nej**

## [!DNL Marketo] {#marketo}

Med de generativa AI-baserade funktionerna i Adobe Dynamic Chat kan ni optimera produktiviteten för säljarna, få insikter i besökarnas avsikter och besvara besökarnas frågor på ett säkert sätt. Du kan förgodkänna frågorna, svaren och konversationssammanfattningen.

[Läs mer](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Kompatibilitet med Adobe Firefly: **Nej**

## [!DNL Workfront] {#workfront}

[!DNL AI Assistant] i [!DNL Workfront] hjälper dig att slutföra ditt arbete genom att erbjuda information och förslag i appen. Du kan:

* Få sammanfattningar av vissa objekt, vilket ger dig en högnivåvy över objektets avsikt eller detaljer.
* Ställ frågor och låt [!DNL AI Assistant] hitta svar på Experience League.
* Hämta genererade formler baserat på dina uppmaningar. Du kan också lösa fel i ogiltiga anpassade uttryck i beräkningsfält.
* Hitta projekt, uppgifter och problem.

[Läs mer](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Kompatibilitet med Adobe Firefly: **Nej**
