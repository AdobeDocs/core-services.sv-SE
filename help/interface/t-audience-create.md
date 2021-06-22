---
description: Lär dig hur du använder attributregler för att skapa en målgrupp och definiera en sammansatt målgrupp i Adobe Experience Cloud.
keywords: bastjänster
solution: Experience Cloud
title: 'Skapa en målgrupp '
uuid: 7e622539-296e-4ff3-93b0-ec1c08b35429
feature: Målgruppsbibliotek
topic: Administrering
role: Administrator
level: Experienced
exl-id: b65a12f5-fa89-400a-b279-13c381cd6c22
source-git-commit: d2ff52ce1a591c7c607598b5f2892dbcca74594b
workflow-type: tm+mt
source-wordcount: '451'
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
* Chrome- och Safari-användare härledda från ett [!DNL Adobe Analytics]-segment [publicerat](audience-library.md#task_32FEEFE0B32E4E388CD4D892D727282A) till [!DNL Experience Cloud].

   ![](assets/audience_create.png)

**Skapa en publik**

1. I [!DNL Experience Cloud], under [!DNL Experience Platform], klickar du på **[!UICONTROL People]** > **[!UICONTROL Audience Library].**
1. På sidan [!UICONTROL Audiences] klickar du på **[!UICONTROL New]**.![](assets/add_icon_small.png)

   ![Stegresultat](assets/audience_create_new.png)

1. På sidan [!UICONTROL Create New Audience] anger du en titel och beskrivning.
1. Välj en attributkälla under [!UICONTROL Rules]:

   * **[!UICONTROL Real-Time Analytics Data:]** (eller Raw-data) Detta är attributdata som härleds från Real-Time Analytics bildbegäranden och innehåller data som eVars och events. Du måste välja en rapportserie när du använder den här attributkällan och definiera dimensionen eller händelsen som ska inkluderas. Rapportsvitens urval innehåller den variabelstruktur som används av rapportsviten.
   >[!NOTE]
   >
   >På grund av cachelagring kräver borttagna rapportsviter i Analytics 12 timmar innan borttagningen visas i Experience Cloud.

   * **[!UICONTROL Experience Cloud:]** Attributdata härledda från  [!DNL Experience Cloud] källorna. Detta kan till exempel vara data från målgruppssegment som du skapar i [!DNL Analytics] eller data från [!DNL Audience Manager].

1. Definiera målgruppsregler och klicka sedan på **[!UICONTROL Save].**

>[!NOTE]
>
>Ni bör förstå era implementeringsvariabler när ni definierar målgruppsregler.

Under [!UICONTROL Rules] definierar du attributvalen *`Home & Garden`*:

* **[!UICONTROL Attribute Source:]** Råanalysdata
* **[!UICONTROL Report Suite:]** Report Suite 31
* Dimension = **[!UICONTROL Store (Merch) (v6)]** > **[!UICONTROL Equals]** > **[!UICONTROL Home & Garden]**

![](assets/home_garden.png)

*Besökarna Chrome och Safari* är ett målgruppssegment som delas av Analytics:

* **[!UICONTROL Attribute Source:]** Experience Cloud
* **[!UICONTROL Dimension:]** Besökare i Chrome och Safari

![](assets/chrome_safari.png)

Som en jämförelse kan du lägga till en *OR*-regel för att se alla besökare i en webbplatssektion, till exempel Patio &amp; Furniture.

![](assets/audiences_rule_patio.png)

Den resulterande regeln är en definierad målgrupp som omfattar Chrome- och Safari-användare som besökte Home &amp; Garden. Segmentet Patio &amp; Furniture ger ytterligare insikter om alla besökare som besöker den webbplatssektionen.

![](assets/defined_audience.png)

* **Historisk uppskattning:** (prickcirkel) Representerar regler som skapats utifrån  [!DNL Analytics] data.
* **Faktisk målgrupp:** (heldragen cirkel) En regel som har skapats med 30 dagars data från Audience Manager. När data från Audience Manager når 30 dagar blir raden heldragen och representerar faktiska tal.

När datainsamlingen har slutförts för den angivna perioden visas en definierad målgrupp i cirklarna.

När målgruppen har sparats är den tillgänglig för andra lösningar. Du kan till exempel inkludera en delad målgrupp i en Adobe Target-aktivitet.
