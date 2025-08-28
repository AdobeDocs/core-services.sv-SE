---
description: Lär dig hur du validerar  [!DNL Customer Attributes] schemat i Adobe Experience Cloud.
solution: Experience Cloud
title: Så här validerar du  [!DNL Customer Attributes] schemat
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
source-git-commit: 21120abb5ab0fcc8d556012851548f39f3875038
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Validera schemat

Med valideringsprocessen kan du mappa visningsnamn och beskrivningar till överförda attribut (strängar, heltal, tal och så vidare).

Ett schema skapas baserat på dessa inställningar. Schemat används för att validera alla framtida data som överförs till den här datakällan. Mappningsprocessen ändrar inte originaldata.

>[!NOTE]
>
>Om du uppdaterar schemat efter valideringen tas kundattributen bort. Se [Uppdatera schemat (tar även bort attribut)](t-crs-usecase.md).

**Verifiera schemat**

1. I [!DNL Customer Attributes] klickar du på attributkällan som du vill redigera.

1. Klicka på **[!UICONTROL Edit Customer Attribute Source]** på **[!UICONTROL File Upload]**.

1. På sidan [!UICONTROL File Upload and Schema Validation] klickar du på **[!UICONTROL Actions]** > **[!UICONTROL View/Edit Schema]**

   ![Redigera ett schema](assets/view_edit_schema.png)

   På sidan [!UICONTROL Edit Schema] representerar varje rad i schemat en kolumn i den överförda CSV-filen.

   ![Redigera schemasida i Experience Cloud](assets/edit-schema.png)

**Åtgärder**

* **[!UICONTROL Add Data:]** Överför nya attributdata till den här datakällan.

* **[!UICONTROL View/Edit Schema:]** Mappa visningsnamn till attributdata enligt beskrivningen i nästa steg.

* **[!UICONTROL FTP Setup:]** Skapa ditt FTP-konto för att [överföra dina data via FTP](t-upload-attributes-ftp.md) (valfritt).

* **[!UICONTROL ID Lookup:]** Ange ett kund-ID (CID) från din `.csv` för att söka efter Experience Cloud-information för ID:t. Den här funktionen är användbar för att felsöka varför attributdata inte visas för en besökare:

   * **[!UICONTROL ECID (Experience Cloud ID):]** Visar om du använder den senaste Experience Cloud ID-tjänsten. Om du är i MCID-tjänsten men det inte finns några ID:n i listan här, har Experience Cloud inte fått något alias för det CID:t. Det innebär att besökaren inte har loggat in eller att implementeringen inte skickar det ID:t till.

   * **[!UICONTROL CID (customer ID):]** De attribut som är associerade med detta CID. Om du använder en prop eller eVar för att överföra CID:n (AVID) och du ser attribut som visas, men inget AVID, indikerar detta att besökaren inte har loggat in på din webbplats.

   * **[!UICONTROL AVID (Analytics visitor ID):]** visas om du använder en säljare eller eVar för att överföra CID:n. Om dessa ID:n skickas till Experience Cloud visas alla besökar-ID:n som är kopplade till det angivna CID:t här.
