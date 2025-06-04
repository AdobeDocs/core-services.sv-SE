---
title: Generativ AI i Experience Cloud-program
description: Läs mer om generativ AI (GenAI) och hur Experience Cloud-program använder GenAI och [!DNL AI Assistant].
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: c7cea04619bdf74c4037bef0de9a1c22596e41cb
workflow-type: tm+mt
source-wordcount: '1631'
ht-degree: 2%

---

# Generativ AI i Experience Cloud-produkter

Generativ AI (genAI) i Experience Cloud hjälper dig att automatisera kreativa och kognitiva uppgifter och öka produktiviteten. På den här sidan beskrivs var Experience Cloud-program har stöd för genAI och AI Assistant, och här finns länkar för mer information om dessa funktioner.

**Vad är genAI?**

Generativ AI är en typ av AI som kan skapa ursprungligt innehåll. Det kan till exempel skapa text, bilder, video, ljud eller programvarukod som svar på en användares uppmaning eller begäran.

* **Skapa:** Möjlighet att generera innehåll (text, bilder, musik eller videor) från grunden, baserat på utbildning och inmatningsanvisningar. Den här möjligheten är den _generativa_ aspekten av generativ AI.

* **Generera ett svar:** AI ger ett svar eller en reaktion på en fråga, som vanligtvis baseras på tillgängliga data- och kunskapsdatabaser.

**Vad är [!DNL AI Assistant]?**

[!DNL AI Assistant] är ett konversationsverktyg som stöds i Experience Platform och relaterade program. Använd den för att snabbt få _produktkunskaper_ och _driftsinsikter_ i produkter som stöds.

* **Produktkunskap:** Produktkunskap avser begrepp och ämnen som anges i Experience League-dokumentationen. Lär dig hur du skapar effektiva, [målbaserade uppmaningar](https://experienceleague.adobe.com/sv/docs/experience-platform/ai-assistant/home) för att få ut det mesta av [!DNL AI Assistant]. Alla svar från Experience League kan verifieras och anges med länkar.

* **Driftsinsikter:** [Driftsinsikter](https://experienceleague.adobe.com/sv/docs/experience-platform/ai-assistant/questions#objects-questions) refererar till genererade svar om dina metadataobjekt (attribut, målgrupper, dataflöden, datauppsättningar och så vidare). Med [!DNL AI Assistant] kan du uppnå på några sekunder vad som annars kan ta timmar eller dagar.

* **Kundsupport**: [Produktsupportagenten](https://experienceleague.adobe.com/sv/docs/experience-platform/ai-assistant/new-features/customer-support) är en självbetjäningsfelsöknings- och felsökningsfunktion hos [!DNL AI Assistant] som du kan använda för Experience Platform-funktioner och program. Felsök supportproblem utan att lämna arbetsflödena, skapa kundsupportärenden och följ upp ärendeutvecklingen med hjälp av AI Assistant.

  **Obs!** Den här funktionen finns i Alpha och är kanske inte tillgänglig för din organisation. Om du vill delta i Alpha och använda den här funktionen kontaktar du ditt kontoteam för Adobe.

[Läs mer om AI Assistant](https://experienceleague.adobe.com/sv/docs/experience-platform/ai-assistant/landing)

## GenAI-tillgänglighet i Experience Cloud-produkter {#products}

Följande Experience Cloud-program har stöd för generativ AI eller [!DNL AI Assistant]. Support för Adobe Firefly anges också per produkt.

Uppdaterat: **4 juni 2025**

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager]](#aem)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign] hanterade molntjänster](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## GenStudio för prestationsbaserad marknadsföring {#gspm}

[!DNL GenStudio for Performance Marketing] är en generativ AI-applikation som är utformad för att hjälpa marknadsföringsteam att skapa, aktivera och optimera kampanjinnehåll för företag över kanaler som betalda medier, e-post och displayannonser.

Marknadsförarna kan använda naturliga språk för att generera personaliserade, varumärkesanpassade resurser. GenStudio for Performance Marketing snabbar upp kampanjgenomförandet, anpassar innehållsproduktionen utan att varumärkesintegriteten äventyras och tillhandahåller prestandaanalyser för att förbättra den totala avkastningen.

[Läs mer](https://experienceleague.adobe.com/sv/docs/genstudio-for-performance-marketing/user-guide/home)

Kompatibilitet med Adobe Firefly: **Ja**

## [!DNL Experience Manager] {#aem}

I följande avsnitt beskrivs kortfattat generativ AI i AEM-program.

### Experience Manager Sites

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

Kompatibilitet med Adobe Firefly: **Ja**

[Läs mer](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

### Experience Manager Assets

I AEM Assets kan du använda generativ AI i **Content Hub** och **AI-genererade smarta taggar**.

Kompatibilitet med Adobe Firefly: **Ja**

**Content Hub**

[!UICONTROL Content Hub] är tillgänglig som en del av [!DNL Experience Manager Assets as a Cloud Service] för att demokratisera åtkomsten till varumärkesinnehåll för organisationer och deras affärspartners. Fokus ligger på att distribuera resurser för aktivering i stor skala och att skapa innehållsvarianter för varumärke, vilket ger förbättrad marknadsföringsflexibilitet.

I Content Hub kan du skapa innehåll med Adobe Express (om du har Adobe Express-rättigheter). Du kan redigera befintligt innehåll med enkla verktyg, producera varumärkesanpassade varianter med mallar och märkeselement och skapa innehåll med de senaste GenAI-funktionerna från [!DNL Adobe Firefly]. [Läs mer](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview)

**Smarta taggar**

I stället för att förlita sig på manuell inmatning kan AI automatiskt tilldela beskrivande taggar till digitala resurser. Dessa AI-genererade taggar förbättrar metadatakvaliteten och gör materialet enklare att söka, kategorisera och rekommendera.

Om resursen till exempel är en bild kan AI identifiera objekt, scener, känslor eller till och med varumärkeslogotyper. Det kan generera relevanta taggar som _solnedgång_, _strand_, _semester_ eller _leende_. [Läs mer](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/assets/manage/smart-tags#ai-smart-tags)

## Adobe [!DNL Journey Optimizer] {#journey-optimizer}

I [!DNL Journey Optimizer] (AJO) kan du använda [ AI Assistant](https://experienceleague.adobe.com/sv/docs/journey-optimizer/using/get-started/ai-assistant) för att få _produktkunskap_ och _driftsinsikter_ (beta).

### Exempel på hur du använder AI Assistant i AJO

Här är ett exempel på produktinformation:

* _Hur många aktiva aktiviteter kan jag ha i en Journey Optimizer-sandlåda?_

  Utdata genereras från Experience League och andra Adobe datalager.

Här är ett exempel på indata för driftsinsikter:

* _Hur många resor har skapats de senaste sju dagarna?_

  AI Assistant hämtar utdata från ett kundspecifikt datalager. Datalagret innehåller centraliserade, driftsdata om [!UICONTROL Journeys]. Den här funktionen är kundagnostiker och hämtar endast metadata från affärsobjekt. Den har inte åtkomst till data i din sandlåda.

[Läs mer](https://experienceleague.adobe.com/sv/docs/journey-optimizer/using/get-started/ai-assistant)

Adobe Firefly-kompatibilitet: **Nej**

### AI Assistant för innehållsgenerering (AJO Prime och Ultimate) {#ajo-prime}

I AJO _Prime_ och _Ultimate_ kan du använda [innehållsgenerering](https://experienceleague.adobe.com/sv/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) för innehållsgenerering för att ge proaktiva variantförslag för text och bilder.

Den här funktionen är tillgänglig för e-post, push-meddelanden, webbsidor, innehåll och SMS-kanaler. Den ger snabb generering av text och bilder. Utdata från innehållsgenerering i AJO Prime och Ultimate är ersättningsberättigande.

[Läs mer](https://experienceleague.adobe.com/sv/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Kompatibilitet med Adobe Firefly: **Ja**

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition använder [!DNL AI Assistant] för att hjälpa dig med produktkännedom.

Exempelindata:

* _Hur skickar jag ett e-postmeddelande i en kontoresa?_

  Produkternas kunskapsresultat hämtas från Experience League.

[Läs mer](https://experienceleague.adobe.com/sv/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Adobe Firefly-kompatibilitet: **Nej**

## [!DNL Campaign] hanterade molntjänster {#campaign-cs}

Kampanjhanterade molntjänster använder [!DNL AI Assistant] för innehållsgenerering. Med den här funktionen kan ni automatiskt generera personaliserat, engagerande och effektivt innehåll baserat på ert marknadsföringsmål, med innehåll som är optimerat för varumärkesanpassade format, layouter, färgtoner med mera. Ni kan använda det i alla kanaler, som e-post, SMS och push.

**Obs!** Utdata från innehållsgenerering i Campaign Managed Cloud Services har försäkringsskydd.

[Läs mer](https://experienceleague.adobe.com/sv/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Kompatibilitet med Adobe Firefly: **Ja**

## [!DNL Customer Journey Analytics] {#cja}

Med Customer Journey Analytics kan du använda generativ AI på följande sätt:

* [!DNL AI Assistant] för produktinformation
* [!DNL Product Support Agent] i AI Assistant (för närvarande i Alpha)
* [!UICONTROL Intelligent Captions] i Workspace-visualiseringar
* AI och GenAI om du vill tilldela alla metadata för resurser automatiskt i [!DNL Content Analytics]

Adobe Firefly-kompatibilitet: **Nej**

**AI-assistenten**

Upptäck produktkunskaper från Experience League. Om du är ny som användare kan du snabbt lära dig Customer Journey Analytics koncept och ta dig an produkter och funktioner. Exempel:

* _Hur skickar jag ett e-postmeddelande i en kontoresa?_

Erfarna användare får avancerade användningsexempel eller lär sig strategier för att utföra uppgifter i snabb takt. Du kan snabbt förstå koncept, felsöka problem eller söka efter information.

[Läs mer](https://experienceleague.adobe.com/sv/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

**Intelligenta bildtexter**

Du kan använda _Intelligenta bildtexter_ i [!DNL Customer Journey Analytics] för att få naturtrogna språkkunskaper för de vanligaste Workspace-visualiseringarna. Intelligenta bildtexter är idealiska för analytiker som behöver berättarröster och sammanhang för att dela med andra användare. Affärsanvändare kan använda den för att snabbt upptäcka högnivåaktiviteter.

Exempel:

* **Indata:** I CJA kör du en visualisering som stöds (inklusive Line, Area, Bar, Flow eller Fallout) och klickar sedan på **[!UICONTROL Intelligent captions]**.

* **Utdata:** Visa automatiskt genererade, naturliga språkbeskrivningar som visar sammanhang och viktiga uppgifter. Sedan kan du vidta åtgärder för genererade data, till exempel granska, kopiera och dela dem med din organisation. [Se hur](https://video.tv.adobe.com/v/3420131/?quality=12&learn=on#_blank)

[Läs mer](https://experienceleague.adobe.com/sv/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

**Content Analytics**

Content Analytics använder AI och GenAI för att tilldela alla metadata för resurser automatiskt, till exempel motiv, scener, förgrundsfärger och så vidare. Ett attribut är en AI-tilldelad metadatatagg som beskriver vad som finns i en resurs eller upplevelse.

Till exempel: förgrunden `color: red` är ett automatiskt tilldelat attribut. Med visualiseringarna kan du identifiera vilka attribut i dina resurser som bidrar mest till konverteringen. [Läs mer](https://experienceleague.adobe.com/sv/docs/analytics-platform/using/content-analytics/report/report#template)

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDP använder [!DNL AI Assistant] för att hjälpa dig med produktkunskaper från Experience League. Här finns även användbara insikter (i betaversion). [!DNL AI Assistant] frågar efter ett kundspecifikt datalager med verksamhetsinsikter som innehåller centraliserade driftdata, som är partitionerat i din AEP-sandlåda. Systemet hämtar endast metadata från attribut, målgrupper, dataflöden, datauppsättningar, destinationer, scheman och källor och har inte åtkomst till data i sandlådan.

Om du till exempel frågar efter en publik kan [!DNL AI Assistant] komma åt målgruppens namn och andra associerade metadata, men inte komma åt profilerna inom den målgruppen.

[Läs mer](https://experienceleague.adobe.com/sv/docs/experience-platform/ai-assistant/home)

Adobe Firefly-kompatibilitet: **Nej**

## [!DNL Marketo] {#marketo}

I Marketo finns generativ AI i interaktiva webbinarier och Dynamic Chat.

**Interaktiva webbinarier**

Generera kapitel och sammanfattningar automatiskt för dina inspelade webbinarier, så att de blir mer tillgängliga och lättare att navigera i. Funktioner:

* Skapa kapitel automatiskt
* AI-genererad textsammanfattning
* Redigerbart innehåll - Ändra genererade kapitel och sammanfattningar
* Enkel integrering - Lägg till kapitel och sammanfattningar på dina landningssidor genom att kopiera HTML-koden till den webbsidesredigerare du väljer

[Läs mer](https://experienceleague.adobe.com/sv/docs/marketo/using/product-docs/demand-generation/events/interactive-webinars/gen-ai)

**Dynamic Chat**

Med de generativa AI-baserade funktionerna i Adobe Dynamic Chat kan ni optimera produktiviteten för säljarna, få insikter i besökarnas avsikter och besvara besökarnas frågor på ett säkert sätt. Du kan förgodkänna frågorna, svaren och konversationssammanfattningen.

[Läs mer](https://experienceleague.adobe.com/sv/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Adobe Firefly-kompatibilitet: **Nej**

## [!DNL Workfront] {#workfront}

[!DNL AI Assistant] i [!DNL Workfront] hjälper dig att slutföra ditt arbete genom att erbjuda information och förslag i appen. Du kan:

* Få sammanfattningar av vissa objekt, vilket ger dig en högnivåvy över objektets avsikt eller detaljer.
* Ställ frågor och låt [!DNL AI Assistant] hitta svar på Experience League.
* Hämta genererade formler baserat på dina uppmaningar. Du kan också lösa fel i ogiltiga anpassade uttryck i beräkningsfält.
* Hitta projekt, uppgifter och problem.

[Läs mer](https://experienceleague.adobe.com/sv/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Adobe Firefly-kompatibilitet: **Nej**

## Ytterligare resurser

* [Ansvariga AI-resurser på Trust Center](https://www.adobe.com/trust/responsible-ai.html)<!-- * [Customer AI Propensity Scoring Model Card](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/model-cards/ai-model-cards/customer-ai) -->

**Ansvarsfriskrivning:** Informationen på den här sidan är endast avsedd som allmän information. Vi vill hålla det korrekt och uppdaterat, men program och AI-funktioner kan ändras ofta. Vi garanterar inte att informationen alltid är fullständig eller tillförlitlig. Kontrollera viktig information innan du fattar beslut baserat på innehållet.
