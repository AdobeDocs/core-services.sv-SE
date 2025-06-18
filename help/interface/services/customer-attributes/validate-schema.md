---
description: Lär dig validera kundattributschemat i Adobe Experience Cloud.
solution: Experience Cloud
title: Så här validerar du kundattributschemat
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Validera schemat

Med valideringsprocessen kan du mappa visningsnamn och beskrivningar till överförda attribut (strängar, heltal, tal och så vidare). Ett schema skapas baserat på dessa inställningar. Schemat används för att validera alla framtida data som överförs till den här datakällan. Mappningsprocessen ändrar inte originaldata.

>[!NOTE]
>
>Om du uppdaterar schemat efter valideringen tas kundattributen bort. Se [Uppdatera schemat (tar även bort attribut)](t-crs-usecase.md).

**[!UICONTROL customer attribute Source]** > **[!UICONTROL Create New customer attribute Source]** > **[!UICONTROL View/Edit Schema]**

![Redigera ett schema](assets/view_edit_schema.png)

På sidan [!UICONTROL Validate Schema] representerar varje rad i schemat en kolumn i den överförda CSV-filen.

![Verifiera schemasida i Experience Cloud](assets/06_crs_usecase.png)

* **[!UICONTROL Add Data:]** Överför nya attributdata till den här datakällan.

* **[!UICONTROL View/Edit Schema:]** Mappa visningsnamn till attributdata enligt beskrivningen i nästa steg.

* **[!UICONTROL FTP Setup:]** [Överför data via FTP](t-upload-attributes-ftp.md).

* **[!UICONTROL ID Lookup:]** Ange ett kund-ID (CID) från din `.csv` för att söka efter Experience Cloud-information för ID:t. Den här funktionen är användbar för att felsöka varför attributdata inte visas för en besökare:

   * **[!UICONTROL ECID (Experience Cloud ID):]** Visar om du använder den senaste Experience Cloud ID-tjänsten. Om du är i MCID-tjänsten men det inte finns några ID:n i listan här, har Experience Cloud inte fått något alias för det CID:t. Det innebär att besökaren inte har loggat in eller att implementeringen inte skickar det ID:t till.

   * **[!UICONTROL CID (customer ID):]** De attribut som är associerade med detta CID. Om du använder en prop eller eVar för att överföra CID:n (AVID) och du ser attribut som visas, men inget AVID, indikerar detta att besökaren inte har loggat in på din webbplats.

   * **[!UICONTROL AVID (Analytics visitor ID):]** visas om du använder en säljare eller eVar för att överföra CID:n. Om dessa ID:n skickas till Experience Cloud visas alla besökar-ID:n som är kopplade till det angivna CID:t här.

Du kan också överföra data via FTP när du har skapat en kundattributkälla och ett FTP-konto i Experience Cloud. Du skapar ett FTP-konto per attributkälla. De överförda filerna lagras i kontots rotmapp. Data måste vara i formatet `.csv`, med en andra `.fin`-fil för att indikera att överföringen är slutförd.

De namn du anger för strängar, heltal och tal används för att skapa [!DNL Analytics]-mått.

* **[!UICONTROL attribute:]** attributdata lästes från den överförda `.csv`-filen.

* **[!UICONTROL Type:]** Datatypen, till exempel:

   * **Sträng:** En teckensekvens.

   * **Heltal:** Hela tal.

   * **Nummer:** Kan innehålla upp till två decimaler.

* **[!UICONTROL Display Name:]** Ett eget namn för attributet. Du kan till exempel ändra attributet *kundens ålder* till *kund sedan*.

* **[!UICONTROL Description:]** En användarvänlig beskrivning av attributet.
