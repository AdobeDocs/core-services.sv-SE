---
description: Lär dig hur du använder attributregler för att skapa en målgrupp och definiera en sammansatt målgrupp i Experience Cloud.
keywords: core services
seo-description: Lär dig hur du använder attributregler för att skapa en målgrupp och definiera en sammansatt målgrupp i Experience Cloud.
seo-title: Skapa en målgrupp
solution: Experience Cloud
title: Skapa en målgrupp
uuid: 7e622539-296e-4ff3-93b0-ec1c08b35429
translation-type: tm+mt
source-git-commit: cc523480327172c89d590065e4321cf1d5f9ab6e
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 3%

---


# Skapa en målgrupp

Lär dig hur du använder attributregler för att skapa en målgrupp och definiera en sammansatt målgrupp i Experience Cloud.

Den här artikeln hjälper dig att förstå hur du gör:

* Skapa en målgrupp
* Skapa en regel
* Använd regler för att definiera en sammansatt målgrupp

Följande bild representerar två regler i en sammansatt målgrupp.

![](assets/audience_sharing.png)

Varje cirkel representerar en regel som definierar målgruppsmedlemskap. Besökare som kvalificerar sig som medlemmar i båda målgruppsreglerna överlappar varandra och blir den sammansatta, definierade målgruppen.

>[!NOTE]
>
>Publiken definieras helt efter att datainsamlingen för den angivna perioden har slutförts.

I följande exempel visas hur du skapar regler för en sammansatt målgrupp. Denna målgrupp består av:

* Avsnittet Hem och Garden är härlett från siddata eller råanalysdata.
* Chrome- och Safari-användare härleds från ett [!DNL Adobe Analytics] segment som [publicerats](../audience-library/audience-library.md#task_32FEEFE0B32E4E388CD4D892D727282A) i [!DNL Experience Cloud].

   ![](assets/audience_create.png)

1. Klicka på [!DNL Experience Cloud]> i [!DNL Experience Platform]under **[!UICONTROL People]** **[!UICONTROL Audience Library].**
1. På sidan [!UICONTROL Audiences] klickar du på **[!UICONTROL New]**.![](assets/add_icon_small.png)

   ![Stegresultat](assets/audience_create_new.png)

1. Ange en rubrik och beskrivning på [!UICONTROL Create New Audience] sidan.
1. Under [!UICONTROL Rules]väljer du en attributkälla:

   * **[!UICONTROL Real-Time Analytics Data:]** (eller Raw-data) Detta är attributdata som härletts från bildbegäranden i realtid med Analytics, och innehåller data som eVars och events. Du måste välja en rapportserie när du använder den här attributkällan och definiera dimensionen eller händelsen som ska inkluderas. Rapportsvitens urval innehåller den variabelstruktur som används av rapportsviten.
   >[!NOTE]
   >
   >På grund av cachelagring kräver borttagna rapportsviter i Analytics 12 timmar innan borttagningen visas i Experience Cloud.

   * **[!UICONTROL Experience Cloud:]** Attributdata härledda från [!DNL Experience Cloud] källorna. Detta kan till exempel vara data från målgruppssegment som du skapar i [!DNL Analytics]eller data från [!DNL Audience Manager].

1. Definiera målgruppsregler och klicka sedan **[!UICONTROL Save].**

>[!NOTE]
>
>Ni bör förstå era implementeringsvariabler när ni definierar målgruppsregler.

Under [!UICONTROL Rules]definierar du *`Home & Garden`* attributval:

* **[!UICONTROL Attribute Source:]** Råanalysdata
* **[!UICONTROL Report Suite:]** Report Suite 31
* Dimension = **[!UICONTROL Store (Merch) (v6)]** > **[!UICONTROL Equals]** > **[!UICONTROL Home & Garden]**

![](assets/home_garden.png)

Besökarna *i* Chrome och Safari är ett målgruppssegment som delas av Analytics:

* **[!UICONTROL Attribute Source:]** Experience Cloud
* **[!UICONTROL Dimension:]** Besökare i Chrome och Safari

![](assets/chrome_safari.png)

Som en jämförelse kan du lägga till en *OR* -regel för att se alla besökare i en webbplatssektion, till exempel Patio &amp; Furniture.

![](assets/audiences_rule_patio.png)

Den resulterande regeln är en definierad målgrupp som omfattar Chrome- och Safari-användare som besökte Home &amp; Garden. Segmentet Patio &amp; Furniture ger ytterligare insikter om alla besökare som besöker den webbplatssektionen.

![](assets/defined_audience.png)

* **Historisk uppskattning:** (Prickad cirkel) Representerar regler som skapats utifrån [!DNL Analytics] data.
* **Faktisk publik:** (Helfylld cirkel) En regel som har skapats med 30 dagars data från Audience Manager. När data från Audience Manager når 30 dagar blir raden heldragen och representerar faktiska tal.

När datainsamlingen har slutförts för den angivna perioden visas en definierad målgrupp i cirklarna.

När målgruppen har sparats är den tillgänglig för andra lösningar. Du kan till exempel inkludera en delad målgrupp i en Adobe Target-aktivitet.
