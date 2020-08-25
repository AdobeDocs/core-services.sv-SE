---
description: Hantera översättning av besöksdata till målgruppssegmentering.
seo-description: Hantera översättning av besöksdata till målgruppssegmentering.
seo-title: Publiker
solution: Experience Cloud
title: Publiker
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
translation-type: tm+mt
source-git-commit: e969dd515dc89e0d96988466a90a740591f67e9f
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 4%

---


# Publiker {#topic_679810123CAA4E0CA4FA3417FB0100C7}

Målgrupper är samlingar med besökare (en lista med besökar-ID:n). Adobe hanterar översättningen av besöksdata till målgruppssegmentering. Att skapa och hantera målgrupper liknar alltså att skapa och använda segment, med möjlighet att dela målgruppssegmentet till [!DNL Experience Cloud]målgruppen.

![](assets/audiences.png)

Målgrupper kan skapas eller härledas från olika källor, till exempel:

* Nya som skapats i [!DNL Experience Cloud]
* Från [!DNL Analytics] segment som publiceras till [!DNL Experience Cloud]
* From [!DNL Audience Manager]

**Realtid kontra historiska målgrupper**

Alla målgrupper, oavsett var de finns, är tillgängliga för användning i realtid med målinriktning. Målgrupper som delas från Analytics till Audience Manager är dock inte tillgängliga för målgruppsanpassning i realtid. Systemet utvärderar målgrupper på två sätt:

* Historiska målgrupper från Analytics utvärderas var fjärde timme. Total tid att bearbeta och dela kan ta upp till 8 timmar.  Historiska målgrupper omfattar alltid återkommande besökare.
* Målgrupper i realtid hämtas från Experience Cloud och utvärderas i realtid.

## Hur lösningar använder målgrupper {#concept_01EB9345C5344597BC94A864EDD38EE1}

I följande tabell beskrivs hur målgrupper används i Experience Cloud-lösningar:

| Lösning | Beskrivning |
|--- |--- |
| Experience Cloud målgrupper | Skapa, hantera och dela målgrupper direkt med hjälp av [Audience Library](../audience-library/audience-library.md) . Ni kan:<ul><li>Använd målgrupper i realtid med råanalysattribut</li><li>Kombinera målgrupper för att skapa sammansatta, sammanfogade realtids- och historiska data</li><li>Se grafiska vyer av uppskattad målgruppsstorlek</li></ul><br>Information om vilken typ av målgrupp du vill skapa finns i: [Experience Cloud målgrupper](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html). |
| Analytics    | Vid segmentering kan du skapa ett segment, kombinera det med en rapportsvit och sedan publicera segmentet på Experience Cloud. När du publicerar segmentet visas det på [!UICONTROL Audience Library] sidan i Experience Cloud. (Mer information finns i [Publicera segment på Experience Cloud](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-publish.html) i Analytics-hjälpen.) Publiken finns också som målgrupp för en kampanjupplevelse som levereras av Adobe Target och i Audience Manager. När en målgrupp har delats från Adobe Analytics och valts ut för användning i en aktiv kampanj skickas alla besökarprofiler som uppfyllde villkoren för segmentdefinitionen för de senaste 90 dagarna till plattformen Experience Cloud [!UICONTROL Audience Services] . Gränsen för delade målgrupper har ökat till 75. Målgrupper som delas till Experience Cloud från Analytics får inte överstiga 20 miljoner unika medlemmar. På grund av cachelagring kräver borttagna rapportsviter i Analytics 12 timmar innan borttagningen visas i Experience Cloud. |
| Mobiltjänster | Analysera mobiltrafiken med solbränsvisualisering i [!UICONTROL Device Types] rapporten. |
| [!DNL Target] | Med [ID-tjänsten](https://docs.adobe.com/content/help/sv-SE/id-service/using/home.html) kombineras besökar-ID:n och data i en enda användbar profil för användning i olika lösningar. Med kryssrutan [Publicera på Experience Cloud](../audience-library/audience-library.md) när du skapar segment i Adobe Analytics kan segmentet vara tillgängligt i Adobe Target anpassade målgruppsbibliotek. Ett segment som skapats i Analytics eller Audience Manager kan användas för aktiviteter i [!DNL Target]. Ni kan till exempel skapa kampanjaktiviteter baserat på [!DNL Analytics] konverteringsstatistik och målgruppssegment som skapats i [!DNL Analytics]. |
| Audience Manager | Delade målgrupper finns i segmentering med Audience Manager. Alla Experience Cloud-målgrupper finns i Audience Manager, vilket innebär att<ul><li>Inbyggd automatisering av hur de delas och används i lösningsarbetsflöden</li><li>Destinationer utanför webbplatsen</li><li>Look-alike-modellering</li></ul> |
| Campaign | <ul><li>Importera delade målgrupper från olika Adobe Experience Cloud-lösningar till Adobe Campaign.</li><li>Exportera mottagarlistor i form av delade målgrupper. Dessa delade målgrupper kan användas i de olika Adobe Experience Cloud-lösningar ni använder.</li></ul> |
| Media Optimizer | Använd målgruppen som mål. |

>[!IMPORTANT]
>
>När en besökare har kvalificerat sig för den målgrupp som delas från Analytics uppstår en fördröjning på 4-8 timmar innan den informationen kan användas i [!DNL Target], Ad Cloud och Campaign Standard.

## Mer hjälp - frågor, vägledning och användningsfall {#section_C7F151644D8A45F7B6FC54F58845635D}

| Hjälp med | Resurs |
|--- |--- |
| Hittar du inte publiker? | Se till att du är etablerad. Se [Komma igång - aktivera lösningar för bastjänster](../core-services/core-services.md).<br>Klicka [här](https://www.adobe.com/go/audiences) för att begära åtkomst till profiler och målgrupper (provisioneringsformulär för integreringar). |
| Användningsfall | Mer information om vilken lösning du ska använda finns i [Alternativ](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html) för målgruppsskapande i kunskapsbasen. |
| Forum | Audiences- [forumet](https://forums.adobe.com/community/experience-cloud/platform/core-services/people-service/audiences) är ytterligare en resurs för att få hjälp med målgrupper. |

## Gränssnittselement i målgruppsbiblioteket {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

Det [!DNL Experience Cloud] innehåller ett bibliotek för att skapa och hantera målgrupper med inbyggd målgruppsidentifiering i realtid.

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Audience Library]**

![](assets/audience_library.png)

| Element | Beskrivning |
|--- |--- |
| Nytt | [Skapa en målgrupp](../audience-library/audience-library.md). |
| Titel och beskrivning | En kolumnrubrik som identifierar och beskriver målgruppen. |
| Författare | Personen som skapade målgruppssegmentet. |
| Källa | Identifierar var målgruppen skapades.<ul><li>**Analyser:** Ett segment som skapats i rapporter och analyser eller ad hoc-analyser och sedan [publicerats på Experience Cloud](../audience-library/audience-library.md).</li><li>**Experience Cloud:** En ny publik [som skapats i Experience Cloud Publiker](../audience-library/audience-library.md).</li><li>**Audience Manager:** Publiker som skapats Audience Manager visas automatiskt i Experience Cloud Publiker.</li></ul> |
| Aktuell storlek | Den aktuella målgruppsstorleken. |
| Aktiv | Segmentets aktiva status. |
