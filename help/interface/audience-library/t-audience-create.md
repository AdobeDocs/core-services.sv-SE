---
description: Lär dig hur du använder attributregler för att skapa en målgrupp och definiera en sammansatt målgrupp i Experience Cloud.
keywords: core services
seo-description: Lär dig hur du använder attributregler för att skapa en målgrupp och definiera en sammansatt målgrupp i Experience Cloud.
seo-title: Skapa en målgrupp
solution: Experience Cloud
title: Skapa en målgrupp
uuid: 7e622539-296e-4ff3-93b0-ec1c08b35429
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

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
I följande exempel visas hur du skapar regler för en sammansatt målgrupp. Målgruppen är:

* Avsnittet Hem och Garden är härlett från siddata eller råanalysdata.
* Chrome- och Safari-användare härleds från ett [!DNL Adobe Analytics] segment som [publicerats](../audience-library/audience-library.md#task_32FEEFE0B32E4E388CD4D892D727282A) i [!DNL Experience Cloud].

   ![](assets/audience_create.png)

1. I [!DNL Experience Cloud], under [!DNL Experience Platform], klickar du på **[!UICONTROL Personer]** > **[!UICONTROL Audience Library].**
1. På sidan [!UICONTROL Publiker] klickar du på **[!UICONTROL Nytt]**. ![](assets/add_icon_small.png)

   ![Stegresultat](assets/audience_create_new.png)

1. Ange en rubrik och beskrivning på sidan [!UICONTROL Skapa ny publik] .
1. Välj en attributkälla under [!UICONTROL Regler]:

   * **[!UICONTROL Realtidsanalysdata:]** (eller Raw-data) Detta är attributdata som härletts från bildbegäranden i realtid med Analytics, och innehåller data som eVars och events. Du måste välja en rapportserie när du använder den här attributkällan och definiera dimensionen eller händelsen som ska inkluderas. Rapportsvitens urval innehåller den variabelstruktur som används av rapportsviten.
   >[!NOTE]
   >
   >På grund av cachelagring kräver borttagna rapportsviter i Analytics 12 timmar innan borttagningen visas i Experience Cloud.

   * **[!UICONTROL Experience Cloud:]** Attributdata härledda från [!DNL Experience Cloud] källorna. Detta kan till exempel vara data från målgruppssegment som du skapar i [!DNL Analytics]eller data från [!DNL Audience Manager].

1. Definiera målgruppsregler och klicka sedan på **[!UICONTROL Spara].**

>[!NOTE]
>
>Ni bör förstå era implementeringsvariabler när ni definierar målgruppsregler.

Definiera [!UICONTROL attributval under]Regler *`Home & Garden`* :

* **[!UICONTROL Attributkälla:]** Råanalysdata
* **[!UICONTROL Report Suite:]** Report Suite 31
* Dimension = **[!UICONTROL Store (Merch) (v6)]** > **[!UICONTROL Lika med]** > **[!UICONTROL Hem &amp; Garden]**

![](assets/home_garden.png)

Besökarna *i* Chrome och Safari är ett målgruppssegment som delas av Analytics:

* **[!UICONTROL Attributkälla:]** Experience Cloud
* **[!UICONTROL Dimension:]** Besökare i Chrome och Safari

![](assets/chrome_safari.png)

Som en jämförelse kan du lägga till en *OR* -regel för att se alla besökare i en webbplatssektion, till exempel Patio &amp; Furniture.

![](assets/audiences_rule_patio.png)

Den resulterande regeln är en definierad målgrupp som omfattar Chrome- och Safari-användare som besökte Home &amp; Garden. Segmentet Patio &amp; Furniture ger ytterligare insikter om alla besökare som besöker den webbplatssektionen.

![](assets/defined_audience.png)

* **Historisk uppskattning:** (Prickad cirkel) Representerar regler som skapats utifrån [!DNL Analytics] data.
* **Faktisk publik:** (Helfylld cirkel) En regel som har skapats med 30 dagars data från Audience Manager. När data för Audience Manager når 30 dagar blir raden heldragen och representerar faktiska tal.

När datainsamlingen har slutförts för den angivna perioden kombineras cirklarna för att visa en definierad målgrupp.

När målgruppen har sparats är den tillgänglig för andra lösningar. Du kan till exempel inkludera en delad publik i en Adobe Target-aktivitet.
