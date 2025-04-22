---
title: AI i Experience Cloud-program
description: Läs mer om generativ AI och hur Experience Cloud-program använder genAI och [!DNL AI Assistant].
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 4676c606f132ab835e0d1f8cdbc81d932e358028
workflow-type: tm+mt
source-wordcount: '1038'
ht-degree: 2%

---

# AI i Experience Cloud-produkter

På den här sidan kan du lära dig vilka produkter som stöder generativ AI, [!DNL AI Assistant] och om Adobe Firefly är kompatibelt. Du kan även hitta länkar till produktspecifika hjälpresurser om hur du använder AI i Experience Cloud.

**Om generativ AI**

Generativ AI är en typ av artificiell intelligens som gör mer än att bara svara på frågor. Den kan _skapa_ innehåll och _svara_ på dina frågor eller satser (kallas _uppmaningar_).

* **Skapa:** AI kan generera nytt innehåll (text, bilder, musik eller videor) från grunden, baserat på utbildning och inmatningsanvisningar. Den här möjligheten är den _generativa_ aspekten av generativ AI.

* **Svara:** AI ger ett svar eller en reaktion på en fråga, vanligen med hjälp av sina kunskaper eller resonemang.

Med generativ AI får du snabbt produktkännedom om du inte har använt Experience Cloud tidigare. Kända användare kan upptäcka driftsinsikter på några sekunder istället för timmar.

**Vad är [!DNL AI Assistant]?**

[!DNL AI Assistant] är ett konversationsverktyg som stöds i Experience Platform och relaterade program. De här programmen använder det på samma sätt men med produktspecifika fördelar. Använd det för att snabba upp arbetsflödena, förbättra produktkunskapen, felsöka problem eller söka i informationen. I vissa program kan du med [!DNL AI Assistant] omedelbart upptäcka användbara insikter.

Produktkunskapssvaren från Experience League kan verifieras och citeras med länkar. Lär dig mer om de olika typerna av [målinriktade uppmaningar](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) för att få ut det mesta av [!DNL AI Assistant].

[Läs mer](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

<!-- **Your data remains yours**

In AI Assistant, security is the priority:

* Customer data is not used to train language models.
* AI Assistant looks at only the documents that you tell it to. You are in control.
* Your people can use AI Assistant only on documents they can access.
* It's audit-ready: Responses are attributable to source documents.
* Enterprise controls are in place to manage who has AI access in the company. -->

## AI-tillgänglighet i Experience Cloud-produkter

Lär dig mer om stöd för generativ AI eller [!DNL AI Assistant] i Experience Cloud-produkter och om Adobe Firefly stöds.

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [Generera variationer i  [!DNL Experience Manager Sites]](#aem-sites)
* [[!DNL AI Assistant] i [!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL AI Assistant] i [!DNL Journey Optimizer] Prime och Ultimate](#ajo-prime-ultimate)
* [[!DNL AI Assistant] i [!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL AI Assistant] i  [!DNL Campaign] v8-webbanvändargränssnittet](#campaign-cs)
* [[!DNL AI Assistant] i [!DNL Customer Journey Analytics]](#cja)
* [Intelligenta bildtexter i  [!DNL Customer Journey Analytics]](#cja-captions)
* [[!DNL AI Assistant] i [!DNL Real-Time CDP]](#rtcdp)
* [Dynamic Chat in [!DNL Marketo]](#marketo)
* [[!DNL AI Assistant] i [!DNL Workfront]](#workfront)

## GenStudio för prestationsbaserad marknadsföring {#gspm}

[!DNL GenStudio for Performance Marketing] är en AI-driven plattform som ger dig möjlighet att generera och hantera marknadsföringsinnehåll som följer varumärkesstandarderna och följer företagets policyer. Generera material för e-post, Meta-annonser, LinkedIn-annonser, displayannonser och banners.

Ni kan också utbilda GenStudio for Performance Marketing om ert varumärke med hjälp av exempel, beskrivningar av kundprofiler och produkter samt varumärkesriktlinjer.

[Läs mer](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home)

Kompatibilitet med Adobe Firefly: **Planerad**

## Generera variationer i [!DNL Experience Manager Sites] {#aem-sites}

[!UICONTROL Generate Variations] i AEM Sites använder generativ AI för att skapa innehållsvariationer baserat på uppmaningar. Dessa uppmaningar tillhandahålls antingen av Adobe eller skapas och hanteras av dig.

När du har skapat varianter kan du använda innehållet på webbplatsen och mäta hur det fungerar med hjälp av Experimentationsfunktionen i Edge Delivery Services. Du kan också generera bilder i Adobe Express med Firefly generativa AI-funktioner.

[Läs mer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations)

Kompatibilitet med Adobe Firefly: **Ja**

## AI-assistenten i [!DNL Journey Optimizer] {#journey-optimizer}

I [!DNL Journey Optimizer] kan du använda [!DNL AI Assistant] för att få produktkunskap och driftsinsikter. Fråga till exempel _Hur många aktiva aktiviteter kan jag ha i en Journey Optimizer-sandlåda?_ Du får omedelbart svar från Experience League och andra Adobe datalager.

[!DNL AI Assistant] kan också hjälpa till med driftsinsikter (beta). Du kan till exempel snabbt lära dig hur många resor som har skapats de senaste sju dagarna.

[!DNL AI Assistant] frågar ett kundspecifikt datalager om det finns operativa insikter. Datalagret innehåller centraliserade, driftsdata om [!UICONTROL Journeys]. Den här funktionen är kundagnostiker och hämtar endast metadata från affärsobjekt. Den har inte åtkomst till data i din sandlåda.

[Läs mer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant).

Kompatibilitet med Adobe Firefly: **Nej**

## AI-assistenten i [!DNL Journey Optimizer] Prime och Ultimate {#ajo-prime-ultimate}

[!DNL Journey Optimizer] Prime och Ultimate använder [!DNL AI Assistant] för Content Accelerator för att ge förslag på proaktiva innehållsvarianter för text och bilder.

Den här funktionen är tillgänglig för e-post, push-meddelanden, webbsidor, innehåll och SMS-kanaler. Den ger snabb generering av text och bilder. Utdata från Content Accelerator i AJO Prime och Ultimate är ersättningsberättigande.

[Läs mer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Kompatibilitet med Adobe Firefly: **Ja**

## AI-assistenten i [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition använder [!DNL AI Assistant] för att hjälpa dig med produktkännedom.

[Läs mer](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Kompatibilitet med Adobe Firefly: **Nej**

## AI-assistenten i [!DNL Campaign] v8-webbgränssnittet {#campaign-cs}

Kampanjhanterade molntjänster använder [!DNL AI Assistant] för Content Accelerator. Med den här funktionen kan ni automatiskt generera personaliserat, engagerande och effektivt innehåll baserat på ert marknadsföringsmål, med innehåll som är optimerat för varumärkesanpassade format, layouter, färgtoner med mera. Ni kan använda det i alla kanaler, som e-post, SMS och push.

**Obs!** Utdata från Content Accelerator i Campaign Managed Cloud Services har försäkringsskydd.

[Läs mer](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Kompatibilitet med Adobe Firefly: **Ja**

## AI-assistenten i [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analytics använder [!DNL AI Assistant] för att hjälpa dig att identifiera produktkunskaper och insikter från Experience League. Om du är ny som användare kan du snabbt lära dig Customer Journey Analytics koncept och ta dig an produkter och funktioner.

Erfarna användare får avancerade användningsexempel eller lär sig strategier för att utföra uppgifter i snabb takt. Förstå koncept, felsök problem eller sök efter information.

[Läs mer](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

Kompatibilitet med Adobe Firefly: **Nej**

## Intelligenta bildtexter i [!DNL Customer Journey Analytics] {#cja-captions}

Intelligenta bildtexter i [!DNL Customer Journey Analytics] ger naturliga språkinsikter för de vanligaste Workspace-visualiseringarna. Intelligenta bildtexter är idealiska för analytiker som behöver berättarröster och sammanhang för att dela med andra användare. Affärsanvändare kan använda den för att snabbt upptäcka högnivåaktiviteter.

[Läs mer](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

Kompatibilitet med Adobe Firefly: **Nej**

## AI-assistenten i [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDP använder [!DNL AI Assistant] för att hjälpa dig med produktkunskaper från Experience League. Här finns även användbara insikter (i betaversion). [!DNL AI Assistant] frågar efter ett kundspecifikt datalager med verksamhetsinsikter som innehåller centraliserade driftdata, som är partitionerat i din AEP-sandlåda. Systemet hämtar endast metadata från attribut, målgrupper, dataflöden, datauppsättningar, destinationer, scheman och källor och har inte åtkomst till data i sandlådan.

Om du till exempel frågar efter en publik kan [!DNL AI Assistant] komma åt målgruppens namn och andra associerade metadata, men inte komma åt profilerna inom den målgruppen.

[Läs mer](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)

Kompatibilitet med Adobe Firefly: **Nej**

## Dynamic Chat i [!DNL Marketo] {#marketo}

Med de generativa AI-baserade funktionerna i Adobe Dynamic Chat kan ni optimera produktiviteten för säljarna, få insikter i besökarnas avsikter och besvara besökarnas frågor på ett säkert sätt. Du kan förgodkänna frågorna, svaren och konversationssammanfattningen.

[Läs mer](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Kompatibilitet med Adobe Firefly: **Nej**

## [!DNL AI Assistant] i [!DNL Workfront] {#workfront}

[!DNL AI Assistant] i [!DNL Workfront] hjälper dig att slutföra ditt arbete genom att erbjuda information och förslag i appen. Du kan:

* Få sammanfattningar av vissa objekt, vilket ger dig en högnivåvy över objektets avsikt eller detaljer.
* Ställ frågor och låt [!DNL AI Assistant] hitta svar på Experience League.
* Hämta genererade formler baserat på dina uppmaningar. Du kan också lösa fel i ogiltiga anpassade uttryck i beräkningsfält.
* Hitta projekt, uppgifter och problem.

[Läs mer](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Kompatibilitet med Adobe Firefly: **Nej**
