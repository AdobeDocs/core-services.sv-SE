---
description: Lär dig hur du använder attributregler för att skapa en målgrupp och definiera en sammansatt målgrupp i Adobe Experience Cloud.
solution: Experience Cloud
title: Skapa en publik
uuid: 7e622539-296e-4ff3-93b0-ec1c08b35429
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: b65a12f5-fa89-400a-b279-13c381cd6c22
source-git-commit: 361175f290d73f1637673420700874a2415e3fca
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Skapa en målgrupp

Lär dig hur du använder attributregler för att skapa en målgrupp och definiera en sammansatt målgrupp i Experience Cloud.

Den här artikeln hjälper dig att förstå hur du gör:

* Skapa en målgrupp
* Skapa en regel
* Använd regler för att definiera en sammansatt målgrupp

Följande bild representerar två regler i en sammansatt målgrupp.

![Två regler i en sammansatt målgrupp](assets/audience_sharing.png)

Varje cirkel representerar en regel som definierar målgruppsmedlemskap. Besökare som kvalificerar sig som medlemmar i båda målgruppsreglerna överlappar varandra och blir den sammansatta, definierade målgruppen.

>[!NOTE]
>
>Publiken definieras helt efter att datainsamlingen för den angivna perioden har slutförts.

I följande exempel visas hur du skapar regler för en sammansatt målgrupp. Denna målgrupp består av:

* Avsnittet Hem och Garden är härlett från siddata eller råanalysdata.
* Chrome- och Safari-användare härledda från ett [!DNL Adobe Analytics]-segment [publicerat](overview.md) till [!DNL Experience Cloud].

  ![Skapa regler för en sammansatt målgrupp](assets/audience_create.png)

**Så här skapar du en publik**

1. I [!DNL Experience Cloud], under [!DNL Experience Platform], klickar du på **[!UICONTROL People]** > **[!UICONTROL Audience Library].**
1. Klicka på **[!UICONTROL New]** på sidan [!UICONTROL Audiences]. ![lägg till](assets/add_icon_small.png)

   ![Stegresultat](assets/audience_create_new.png)

1. Ange en rubrik och beskrivning på sidan [!UICONTROL Create New Audience].
1. Välj en attributkälla under [!UICONTROL Rules]:

   * **[!UICONTROL Real-Time Analytics Data:]** (eller Raw-data) Detta är attributdata som härleds från Real-Time Analytics-bildbegäranden och innehåller data som eVars och events. Du måste välja en rapportserie när du använder den här attributkällan och definiera dimensionen eller händelsen som ska inkluderas. Rapportsvitens urval innehåller den variabelstruktur som används av rapportsviten.

   >[!NOTE]
   >
   >På grund av cachelagring kräver borttagna rapportsviter i Analytics 12 timmar innan borttagningen visas i Experience Cloud.

   * **[!UICONTROL Experience Cloud:]** attributdata härledda från [!DNL Experience Cloud]-källor. Detta kan till exempel vara data från målgruppssegment som du skapar i [!DNL Analytics] eller data från [!DNL Audience Manager].

1. Definiera målgruppsregler och klicka sedan på **[!UICONTROL Save].**

>[!NOTE]
>
>Ni bör förstå era implementeringsvariabler när ni definierar målgruppsregler.

Definiera attributvalen *`Home & Garden`* under [!UICONTROL Rules]:

* **[!UICONTROL Attribute Source:]** råanalysdata
* **[!UICONTROL Report Suite:]** Report Suite 31
* Dimension = **[!UICONTROL Store (Merch) (v6)]** > **[!UICONTROL Equals]** > **[!UICONTROL Home & Garden]**

![Attributmarkeringar i målgruppsbiblioteket](assets/home_garden.png)

*Chrome- och Safari-besökarna* är ett målgruppssegment som delas av Analytics:

* **[!UICONTROL Attribute Source:]** Experience Cloud
* **[!UICONTROL Dimension:]** Chrome- och Safari-besökare

![Chrome- och Safari-besökare](assets/chrome_safari.png)

Som en jämförelse kan du lägga till en *OR*-regel för att se alla besökare i ett webbplatsavsnitt, till exempel Patio &amp; Furniture.

![OR-regel för en målgrupp](assets/audiences_rule_patio.png)

Den resulterande regeln är en definierad målgrupp som omfattar användare av Chrome &amp; Safari som besökte Home &amp; Garden. Segmentet Patio &amp; Furniture ger ytterligare insikter om alla besökare som besöker den webbplatssektionen.

![Definierad målgrupp i Experience Cloud](assets/defined_audience.png)

* **Historisk uppskattning:** (prickad cirkel) Representerar regler som skapats baserat på [!DNL Analytics]-data.
* **Faktisk publik:** (heldragen cirkel) En regel som har skapats med 30 dagars data från Audience Manager. När Audience Manager-data når 30 dagar blir raden heldragen och representerar faktiska tal.

När datainsamlingen har slutförts för den angivna perioden kombineras cirklarna för att visa en definierad målgrupp.

När målgruppen har sparats är den tillgänglig för andra program. Du kan till exempel inkludera en delad målgrupp i en Adobe Target-aktivitet.
