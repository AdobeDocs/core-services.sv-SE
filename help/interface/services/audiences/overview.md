---
title: "[!DNL Audience Library]"
description: Lär dig hur du översätter besöksdata till målgruppssegmentering i Experience Cloud [!DNL Audience Library].
solution: Experience Cloud
type: Documentation
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 2%

---

# Experience Cloud målgrupper {#topic_679810123CAA4E0CA4FA3417FB0100C7}

The [!DNL Audience Library] visar målgrupper i Experience Cloud. Målgrupper är samlingar med besökare (en lista med [!DNL Experience Cloud] ID). Ni kan hantera översättningen av besöksdata till målgruppssegmentering. Att skapa och hantera målgrupper liknar alltså att skapa och använda segment. Du kan också dela målgruppssegmentet med produkter och tjänster i [!DNL Experience Cloud].

![Experience Cloud målgrupper](assets/audiences.png)

Målgrupper kan skapas eller härledas från olika källor, till exempel:

* Nya som skapats i [!DNL Experience Cloud]
* [!DNL Analytics] segment som publicerats i [!DNL Experience Cloud]
* [!DNL Audience Manager]

**Realtidsanvändare kontra historiska målgrupper**

Alla målgrupper, oavsett var de finns, är tillgängliga för användning i realtid med målinriktning. Målgrupper som delas från Analytics till Audience Manager är dock inte tillgängliga för målgruppsanpassning i realtid. Systemet utvärderar målgrupper på två sätt:

* Historiska målgrupper från Analytics utvärderas var fjärde timme. Total tid att bearbeta och dela tar upp till åtta timmar. Historiska målgrupper omfattar alltid återkommande besökare.
* Målgrupper i realtid hämtas från Experience Cloud och utvärderas i realtid.

## Hur applikationer använder målgrupper {#concept_01EB9345C5344597BC94A864EDD38EE1}

I följande tabell beskrivs hur målgrupper används i Experience Cloud-program:

| Lösning | Beskrivning |
|--- |--- |
| Experience Cloud-målgrupper | Skapa, hantera och dela målgrupper direkt med hjälp av målgruppsbiblioteket. Du kan:<ul><li>Använd målgrupper i realtid med råanalysattribut</li><li>Kombinera målgrupper för att skapa sammansatta, sammanfogade realtids- och historiska data</li><li>Se grafiska vyer av uppskattad målgruppsstorlek</li></ul><br>Information om vilken typ av målgrupp du vill skapa finns i [Alternativ för att skapa målgrupper](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html). |
| Analytics  | Vid segmentering kan du skapa ett segment, kombinera det med en rapportsvit och sedan publicera segmentet på Experience Cloud. När du publicerar segmentet visas det på [!DNL Audience Library] sida i Experience Cloud. (Se [Publicera segment i Experience Cloud](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html) in [!DNL Analytics] hjälp för mer information.) Publiken finns också som målgrupp för en kampanjupplevelse som levereras av [!DNL Adobe Target]och in [!DNL Audience Manager]. När du har delat en målgrupp från [!DNL Adobe Analytics]och väljer att använda den i en aktiv kampanj skickas de besökarprofiler som uppfyller villkoren för segmentdefinition för de senaste 90 dagarna till [!UICONTROL Audience Services]. Gränsen för delade målgrupper har ökat till 75. Målgrupper som delas med Experience Cloud från [!DNL Analytics] får inte överskrida 20 miljoner unika medlemmar. På grund av cachelagring kräver borttagna rapportsviter i Analytics 12 timmar innan borttagningen visas i Experience Cloud. |
| Mobile-tjänster | Analysera mobiltrafik med solbränsvisualisering i [!UICONTROL Device Types] rapport. |
| [!DNL Target] | The [ID-tjänst](https://experienceleague.adobe.com/docs/id-service/using/home.html) kombinerar besökar-ID:n och data i en enda, användbar profil som kan användas i olika program. The [!UICONTROL Publish to Experience Cloud] när du skapar segment i Adobe Analytics kan segmentet vara tillgängligt i Adobe Target anpassade målgruppsbibliotek. Ett segment som skapats i [!DNL Analytics] eller [!DNL Audience Manager] kan användas för aktiviteter i [!DNL Target]. Du kan till exempel skapa kampanjaktiviteter baserat på [!DNL Analytics] konverteringsstatistik och målgruppssegment skapade i [!DNL Analytics]. |
| [!DNL Audience Manager] | Delade målgrupper finns i [!DNL Audience Manager] segmentering. Alla Experience Cloud-målgrupper är tillgängliga direkt i [!DNL Audience Manager], som innehåller:<ul><li>Inbyggd automatisering av hur de delas och används i arbetsflöden</li><li>Destinationer utanför webbplatsen</li><li>Look-alike-modellering</li></ul> |
| Campaign | <ul><li>Importera delade målgrupper från olika Adobe Experience Cloud-program till Adobe Campaign.</li><li>Exportera mottagarlistor i form av delade målgrupper. Dessa delade målgrupper kan användas i de olika Adobe Experience Cloud-program som du använder.</li></ul> |
| Advertising Cloud | Använd målgruppen som mål. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>När en besökare kvalificerar sig för den målgrupp som delas från Analytics, sker en 4-8 timmars fördröjning innan informationen kan användas i [!DNL Target], Ad Cloud och Campaign Standard.

## Gränssnittselement i målgruppsbiblioteket {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

The [!DNL Experience Cloud] innehåller ett bibliotek för att skapa och hantera målgrupper med inbyggd målgruppsidentifiering i realtid.

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Audience Library]**

![Lägga till målgrupper i målgruppsbiblioteket](assets/audience_library.png)

| Element | Beskrivning |
|--- |--- |
| Nytt | [Skapa en målgrupp](create.md). |
| Titel och beskrivning | En kolumnrubrik som identifierar och beskriver målgruppen. |
| Författare | Personen som skapade målgruppssegmentet. |
| Källa | Identifierar var målgruppen skapades.<ul><li>**Analyser:** Ett segment som skapats i Adobe Analytics och sedan publicerats i Experience Cloud.</li><li>**Experience Cloud:** En ny publik [som skapats i Experience Cloud-målgrupper](create.md).</li><li>**Audience Manager:** Publiker som skapats Audience Manager visas automatiskt i Experience Cloud Publiker.</li></ul> |
| Aktuell storlek | Den aktuella målgruppsstorleken. |
| Aktiv | Segmentets aktiva status. |

{style="table-layout:auto"}

## Publicera målgrupper från Adobe Analytics

Se [Publicera segment i Experience Cloud](https://experienceleague.adobe.com/en/docs/analytics/components/segmentation/segmentation-workflow/seg-publish) i Adobe Analytics-dokumentationen.
