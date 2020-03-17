---
description: Hantera översättning av besöksdata till målgruppssegmentering.
seo-description: Hantera översättning av besöksdata till målgruppssegmentering.
seo-title: Målgrupper
solution: Experience Cloud
title: Målgrupper
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
translation-type: tm+mt
source-git-commit: d304e625bd2125854d9ed932674522284995e030

---


# Audiences {#topic_679810123CAA4E0CA4FA3417FB0100C7}

Målgrupper är samlingar med besökare (en lista med besökar-ID:n). Adobes målgruppstjänster hanterar översättningen av besöksdata till målgruppssegmentering. Att skapa och hantera målgrupper liknar alltså att skapa och använda segment, med möjlighet att dela målgruppssegmentet till [!DNL Experience Cloud]målgruppen.

![](assets/audiences.png)

Målgrupper kan skapas eller härledas från olika källor, till exempel:

* Nya som skapats i [!DNL Experience Cloud]
* Från [!DNL Analytics] segment som publicerats till [!DNL Experience Cloud]
* Från [!DNL Audience Manager]

**Realtid kontra historiska målgrupper**

Alla målgrupper, oavsett var de finns, är tillgängliga för användning i realtid med målinriktning. Målgrupper som delas från Analytics till Audience Manager är dock inte tillgängliga för målgruppsanpassning i realtid. Systemet utvärderar målgrupper på två sätt:

* Historiska målgrupper hämtas från analyser och utvärderas var tolfte timme. Historiska målgrupper omfattar alltid återkommande besökare.
* Målgrupper i realtid hämtas från Experience Cloud-målgrupper och utvärderas i realtid.

## Hur lösningar använder målgrupper {#concept_01EB9345C5344597BC94A864EDD38EE1}

I följande tabell beskrivs hur målgrupper används i Experience Cloud-lösningar:

| Lösning | Beskrivning |
|--- |--- |
| Experience Cloud-målgrupper | Skapa, hantera och dela målgrupper direkt med hjälp av [Audience Library](../audience-library/audience-library.md) . Du kan:<ul><li>Använd målgrupper i realtid med råanalysattribut</li><li>Kombinera målgrupper för att skapa sammansatta, sammanfogade realtids- och historiska data</li><li>Se grafiska vyer av uppskattad målgruppsstorlek</li></ul><br>Information om vilken typ av målgrupp du vill skapa finns i: [Experience Cloud-målgrupper](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html). |
| Analyser | Vid segmentering kan ni skapa ett segment, kombinera det med en rapportsvit och sedan [publicera segmentet i Experience Cloud](../audience-library/audience-library.md). När du publicerar segmentet visas det på sidan [Publiker](../audience-library/audience-library.md) . Publiken finns också som målgrupp för en kampanjupplevelse som levereras av Adobe Target och i Audience Manager.   När en målgrupp har delats från Analytics och valts ut för användning i en aktiv kampanj skickas alla besökarprofiler som uppfyller villkoren för segmentdefinition för de senaste 90 dagarna till Experience Cloud Audience Services-plattformen.   Viktigt:  Ni måste begränsa antalet målgrupper som delas från Analytics till 20 för att undvika ytterligare förseningar. Målgrupper som delas med Experience Cloud från Analytics får inte överstiga 20 miljoner unika medlemmar. På grund av cachelagring kräver borttagna rapportsviter i Analytics 12 timmar innan borttagningen visas i Experience Cloud. |
| Mobiltjänster | Analysera mobiltrafiken med solbränsvisualisering i [!UICONTROL Device Types] rapporten. |
| Mål | Med [ID-tjänsten](https://docs.adobe.com/content/help/en/id-service/using/home.html) kombineras besökar-ID:n och data i en enda användbar profil för användning i olika lösningar. Kryssrutan [Publicera i Experience Cloud](../audience-library/audience-library.md) när du skapar segment i Adobe Analytics gör att segmentet kan vara tillgängligt i Adobe Target-målets anpassade målgruppsbibliotek. Ett segment som skapats i Analytics eller Audience Manager kan användas för aktiviteter i Target.  Ni kan till exempel skapa kampanjaktiviteter baserat på analysstatistik och målgruppssegment som skapats i Analytics. |
| Audience Manager | Delade målgrupper finns i Audience Manager-segmentering. Alla Experience Cloud-målgrupper är tillgängliga direkt i Audience Manager, som tillhandahåller:<ul><li>Inbyggd automatisering av hur de delas och används i lösningsarbetsflöden</li><li>Destinationer utanför webbplatsen</li><li>Look-alike-modellering</li></ul> |
| Campaign | <ul><li>Importera delade målgrupper från olika Adobe Experience Cloud-lösningar till Adobe Campaign.</li><li>Exportera mottagarlistor i form av delade målgrupper. Dessa delade målgrupper kan användas i de olika Adobe Experience Cloud-lösningar ni använder.</li></ul> |
| Media Optimizer | Använd målgruppen som mål. |

>[!IMPORTANT]
>
>När en besökare har kvalificerat sig för den målgrupp som delas från Analytics uppstår en 24-48 timmars fördröjning innan informationen kan användas i Target, Media Optimizer och Campaign.

## Mer hjälp - frågor, vägledning och användningsfall {#section_C7F151644D8A45F7B6FC54F58845635D}

| Hjälp med | Resurs |
|--- |--- |
| Hittar du inte publiker? | Se till att du är etablerad. Se [Komma igång - aktivera lösningar för bastjänster](../core-services/core-services.md).<br>Klicka [här](https://www.adobe.com/go/audiences) för att begära åtkomst till profiler och målgrupper (provisioneringsformulär för integreringar). |
| Användningsexempel | Mer information om vilken lösning du ska använda finns i [Alternativ](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html) för målgruppsskapande i kunskapsbasen. |
| Forum | Audiences- [forumet](https://forums.adobe.com/community/experience-cloud/platform/core-services/people-service/audiences) är ytterligare en resurs för att få hjälp med målgrupper. |

## Gränssnittselement i målgruppsbiblioteket {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

Det [!DNL Experience Cloud] innehåller ett bibliotek för att skapa och hantera målgrupper med inbyggd målgruppsidentifiering i realtid.

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Audience Library]**

![](assets/audience_library.png)

| Element | Beskrivning |
|--- |--- |
| Nytt | [Skapa en målgrupp](../audience-library/audience-library.md). |
| Titel och beskrivning | En kolumnrubrik som identifierar och beskriver målgruppen. |
| Upphovsman | Personen som skapade målgruppssegmentet. |
| Källa | Identifierar var målgruppen skapades.<ul><li>**Analyser:** Ett segment som skapats i rapporter och analyser eller ad hoc-analyser och sedan [publicerats i Experience Cloud](../audience-library/audience-library.md).</li><li>**Experience Cloud:** En ny publik [som skapats i Experience Cloud Audiences](../audience-library/audience-library.md).</li><li>**Audience Manager:** Publiker som skapats med Audience Manager visas automatiskt i Experience Cloud-målgrupperna.</li></ul> |
| Aktuell storlek | Den aktuella målgruppsstorleken. |
| Aktiv | Segmentets aktiva status. |
