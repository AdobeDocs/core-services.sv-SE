---
description: Lär dig hur du skapar kundattributkällan och överför den till Adobe Experience Cloud.
keywords: Kundattribut;bastjänster
solution: Experience Cloud
title: 'Skapa en kundattributskälla och överför datafilen '
uuid: 53dca789-9a91-4385-839d-c9d1aa36b9be
feature: Kundattribut
topic: Administrering
role: Administrator
level: Experienced
exl-id: 21ed7c35-aac9-46f1-a50c-84e7c075209c
source-git-commit: 93f5eda7229990e3645b54efa2a172d7b57dcb9b
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 1%

---

# Skapa en kundattributskälla och överför datafilen

Skapa kundattributskällan (CSV- och FIN-filer) och överför data. Du kan aktivera datakällan när du är klar. När datakällan är aktiv delar du attributdata till Analytics och Target.

## Arbetsflöde för kundattribut {#concept_BF0AF88E9EF841219ED4D10754CD7154}

![](assets/crs.png)

1. [Skapa en datafil](t-crs-usecase.md#task_B5FB8C0649374C7A94C45DCF2878EA1A)
1. [Skapa attributkällan och överför datafilen](t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [Validera schemat](t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [Konfigurera prenumerationer och aktivera attributkällan](t-crs-usecase.md#task_1ACA21198F0E46A897A320C244DFF6EA)

När datakällan är aktiv kan du:

* [Använd kundattribut i Adobe Analytics](t-crs-usecase.md#task_7EB0680540CE4B65911B2C779210915D)
* [Använd kundattribut i Adobe Target](t-crs-usecase.md#task_FC5F9D9059114027B62DB9B1C7D9E257)

>[!IMPORTANT]
>
>För att få tillgång till den här funktionen måste användarna tilldelas till produktprofilen för kundattribut (kundattribut - standardåtkomst). Navigera till **[!UICONTROL Administration]** > **[!UICONTROL Admin Console]** > **[!UICONTROL Products]**. Om *kundattribut* visas som en av [!UICONTROL Product Profiles] är du redo att börja. Användare som läggs till i gruppen Kundattribut ser menyn [!UICONTROL Customer Attributes] till vänster om Experience Cloud.
>
>Om du vill använda funktionen Kundattribut måste användarna även tillhöra lösningsnivågrupper (Analytics eller [!DNL Target]).

Se [Hantera användare och produkter i Experience Cloud](admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9).

## Skapa en datafil {#task_B5FB8C0649374C7A94C45DCF2878EA1A}

Dessa data är företagskunddata från din CRM. Informationen kan omfatta prenumerationsdata för produkter, inklusive medlems-ID, berättigade produkter, mest lanserade produkter osv.

1. Skapa en `.csv`.

   >[!NOTE]
   >
   >Senare i den här processen drar och släpper du `.csv` för att överföra filen. Om du [överför via FTP](t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B) behöver du också en `.fin`-fil med samma namn som `.csv`.

   Exempel på kunddatafil för företag:

   ![](assets/01_crs_usecase.png)

1. Granska viktig information i [Datafilskrav](crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) innan du överför filen innan du fortsätter.
1. [Skapa en Customer Attribute-källa och överför data](t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78) enligt beskrivningen nedan.

## Skapa attributkällan och överför datafilen {#task_09DAC0F2B76141E491721C1E679AABC8}

Utför dessa steg på sidan Skapa ny källa för kundattribut i Experience Cloud.

>[!IMPORTANT]
>
>När du skapar, ändrar eller tar bort kundattributskällor är det en fördröjning på upp till en timme innan ID:n börjar synkronisera med den nya datakällan. Du måste ha administratörsbehörighet i Audience Manager för att kunna skapa eller ändra källor för kundattribut. Kontakta Audience Manager kundtjänst eller konsult för att få administrationsrättigheter.

1. I [!DNL Experience Cloud] väljer du menyikonen ![](assets/menu-icon.png).
1. Under **[!DNL Experience Platform]** väljer du **[!UICONTROL People]** > **[!UICONTROL Customer Attributes]**.

   På sidan [!UICONTROL Customer Attributes] kan du hantera och redigera befintliga attributdatakällor.

   ![Stegresultat](assets/03_crs_usecase.png)
1. Välj **[!UICONTROL New]**.

   ![Stegresultat](assets/04_crs_usecase.png)
1. Konfigurera följande fält på [!UICONTROL Edit Customer Attribute Source]-sidan:

   * **[!UICONTROL Name:]** Ett eget namn för datakällan för dataattribut. Attributnamn får inte innehålla blanksteg för [!DNL Adobe Target]. Om ett attribut med ett blanksteg skickas ignoreras det av [!DNL Target]. Andra tecken som inte stöds är: `< , >, ', "`.

   * **[!UICONTROL Description:]** (Valfritt) En beskrivning av datakällan för dataattribut.

   * **[!UICONTROL Alias ID:]** Representerar en källa för kundattributdata, t.ex. ett specifikt CRM-system. [!UICONTROL Alias ID] är ett unikt ID som används i din källkod för kundattribut. ID:t ska vara unikt, med gemener, utan blanksteg. Värdet som anges i fältet [!UICONTROL Alias ID] för en kundattributkälla i Experience Cloud ska matcha värdena som skickas från implementeringen (oavsett om det är via Datainsamling (Launch), Dynamic Tag Management eller JavaScript för Mobile SDK.)

      Alias-ID motsvarar vissa områden där du anger ytterligare värden för Kund-ID. Exempel:

      * **Dynamisk tagghantering:** Alias-ID motsvarar  *Integration* Codevalue under  [!UICONTROL Customer Settings], i  [Experience Cloud ID ](https://experienceleague.adobe.com/docs/dtm/using/tools/macid.html?lang=en) Service Tool.

      * **Besökar-API:t:** Alias-ID:t motsvarar de ytterligare  [kund-ID:n ](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=en) som du kan associera med varje besökare.

         Till exempel *&quot;crm_id&quot;* i:

         ```
         "crm_id":"67312378756723456"
         ```

      * **iOS:** Alias-ID motsvarar  *&quot;idType&quot;* i  [visitorSyncIdentifiers:Identifiers](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=en).

         Exempel:

         `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`

      * **Android™:** Alias-ID motsvarar  *&quot;idType&quot;* i  [syncIdentifiers](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=en).

         Exempel:

         `identifiers.put(`**`"idType"`**`, "idValue");`

         Se [Utnyttja flera datakällor](crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB) om du vill ha mer information om databearbetning för Alias ID-fältet och Kund-ID:n.
   * **[!UICONTROL File Upload:]** Du kan dra och släppa  `.csv` datafilen eller överföra data via FTP. (FTP kräver också en `.fin`-fil.) Se [Överför data via FTP](t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B).

      >[!IMPORTANT]
      >
      >Det finns särskilda krav på datafiler. Mer information finns i [Datafilskrav](crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19).


      När du har överfört filen visas tabelldata under rubriken [!UICONTROL File Upload] på den här sidan. Du kan validera schemat, konfigurera prenumerationer eller konfigurera FTP.

      **Filöverföring - grafik**

      ![](assets/file_upload_attributes.png)

   * **[!UICONTROL Unique Customer ID:]** Visar hur många unika ID:n du har överfört till den här attributkällan.

   * **[!UICONTROL Customer-Provided IDs Aliased to Experience Cloud Visitor IDs:]** Visar hur många ID:n som har alias för Experience Cloud Visitor ID:n.

   * **[!UICONTROL Customer-Provided IDs with High Alias Counts:]** Visar antalet kundtillhandahållna ID:n med 500 eller fler Experience Cloud-besökar-ID:n med alias. Dessa kundtillhandahållna ID:n representerar förmodligen inte individer utan snarare någon typ av delad inloggning. Attributen som är kopplade till dessa ID:n distribueras till de 500 senaste aliaserade Experience Cloud-besökar-ID:n, tills aliasantalet är 10 000. Systemet gör sedan kundens ID ogiltigt och distribuerar inte längre tillhörande attribut.



## Validera schemat {#task_404AAC411B0D4E129AB3AC8B7BE85859}

Med valideringsprocessen kan du mappa visningsnamn och beskrivningar till överförda attribut (strängar, heltal, tal och så vidare). Du kan även ta bort attribut genom att uppdatera schemat.

Se [Verifiera schemat](validate-schema.md#concept_B3A01A15D04E4F998118E09B3A9B5043).

Mer information om hur du tar bort attribut finns i [(Valfritt) Uppdatera schemat (tar bort attribut)](t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C).

## (Valfritt) Uppdatera schemat (ta bort attribut) {#task_6568898BB7C44A42ABFB86532B89063C}

Så här tar du bort attribut och ersätter attribut i schemat.

1. På sidan [!UICONTROL Edit Customer Attribute Source] tar du bort prenumerationen **[!UICONTROL Target]** eller **[!UICONTROL Analytics]** (under [!UICONTROL Configure Subscriptions]).
1. [Överför en ny datafil med uppdaterade fält](t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8).

## Konfigurera prenumerationer och aktivera attributkällan {#task_1ACA21198F0E46A897A320C244DFF6EA}

När du konfigurerar en prenumeration skapas dataflödet mellan Experience Cloud och lösningar. Genom att aktivera attributkällan kan data flöda till prenumererade lösningar. De kundposter som du har överfört matchas med inkommande ID-signaler från din webbplats eller ditt program.

Se [Konfigurera prenumerationer](subscription.md#concept_ECA3C44FA6D540C89CC04BA3C49E63BF).

**Så här aktiverar du en attributkälla**

På sidan [!UICONTROL Create New [or Edit] Customer Attribute Source] letar du reda på rubriken [!UICONTROL Activate] och väljer sedan **[!UICONTROL Active]**.

![Stegresultat](assets/activate_attribute_source.png)

## Använd kundattribut i Adobe Analytics {#task_7EB0680540CE4B65911B2C779210915D}

Med de data som nu finns i lösningar som Adobe Analytics kan ni rapportera data, analysera dem och vidta lämpliga åtgärder i era marknadsföringskampanjer.

I följande exempel visas ett [!DNL Analytics]-segment baserat på de överförda attributen. I det här segmentet visas [!DNL Photoshop Lightroom] prenumeranter vars mest lanserade produkt är Photoshop.

![](assets/08_crs_usecase.png)

När du publicerar ett segment på Experience Cloud blir det tillgängligt i Experience Cloud Publiker och Audience Manager.

## Använd kundattribut i Adobe Target {#task_FC5F9D9059114027B62DB9B1C7D9E257}

I [!DNL Target] kan du välja ett kundattribut i [!UICONTROL Visitor Profile]-avsnittet när du skapar en målgrupp. Alla kundattribut har prefixet `crs.` i listan. Kombinera dessa attribut efter behov med andra dataattribut för att skapa målgrupper.

![](assets/crs-add-attribute-target.png)

Se [Skapa en ny publik](https://experienceleague.adobe.com/docs/target/using/audiences/create-audiences/audiences.html?lang=en) i [!DNL Target]-hjälpen.
