---
description: Skapa kundattributskällan och överför data.
keywords: customer attributes;core services
seo-description: Skapa kundattributskällan och överför data.
seo-title: Skapa en kundattributkälla och överför datafilen
solution: Experience Cloud
title: Skapa en kundattributkälla och överför datafilen
uuid: 53dca789-9a91-4385-839d-c9d1aa36b9be
translation-type: tm+mt
source-git-commit: d304e625bd2125854d9ed932674522284995e030

---


# Skapa en kundattributkälla och överför datafilen

Skapa kundattributskällan (CSV- och FIN-filer) och överför data. Du kan aktivera datakällan när du är klar. När datakällan är aktiv delar du attributdata till Analytics och Target.

## Arbetsflöde för kundattribut {#concept_BF0AF88E9EF841219ED4D10754CD7154}

![](assets/crs.png)

1. [Skapa en datafil](../attributes/t-crs-usecase.md#task_B5FB8C0649374C7A94C45DCF2878EA1A)
1. [Skapa attributkällan och överför datafilen](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [Validera schemat](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [Konfigurera prenumerationer och aktivera attributkällan](../attributes/t-crs-usecase.md#task_1ACA21198F0E46A897A320C244DFF6EA)


När datakällan är aktiv kan du:

* [Använd kundattribut i Adobe Analytics](../attributes/t-crs-usecase.md#task_7EB0680540CE4B65911B2C779210915D)
* [Använd kundattribut i Adobe Target](../attributes/t-crs-usecase.md#task_FC5F9D9059114027B62DB9B1C7D9E257)



>[!IMPORTANT]
>
>För att få tillgång till den här funktionen måste användarna tilldelas till produktprofilen för kundattribut (kundattribut - standardåtkomst). ( **[!UICONTROL Administration]** > **[!UICONTROL Admin Console]** > **[!UICONTROL Users]** > ). Användare som läggs till i gruppen Kundattribut ser menyalternativet i [!UICONTROL Customer Attributes] [!UICONTROL Audiences]till vänster om Experience Cloud-gränssnittet.
>
>Medlemskap i lösningsgruppen krävs också.

För att kunna använda funktionen Kundattribut måste användarna tillhöra gruppen Adobe Customer Attributes i användarhantering och i grupper på lösningsnivå (Analytics eller Target).

Se [Användare och grupper](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9).

## Skapa en datafil {#task_B5FB8C0649374C7A94C45DCF2878EA1A}

Dessa data är företagskunddata från din CRM. Informationen kan omfatta prenumerationsdata för produkter, inklusive medlems-ID, berättigade produkter, mest lanserade produkter osv.


1. Skapa en `.csv`.


   >[!NOTE]
   >
   >Senare i den här processen drar och släpper du filen `.csv` för att överföra den. Om du däremot [överför via FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)behöver du också en `.fin` fil med samma namn som `.csv`.



   Exempel på kunddatafil för företag:

   ![](assets/01_crs_usecase.png)

1. Innan du fortsätter bör du granska den viktiga informationen i [Datafilskraven](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)innan du överför filen.
1. [Skapa en källa för kundattribut och överför data](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)enligt beskrivningen nedan.

## Skapa attributkällan och överför datafilen {#task_09DAC0F2B76141E491721C1E679AABC8}

Utför dessa steg på sidan Skapa ny källa för kundattribut i Experience Cloud.


>[!IMPORTANT]
>
>När du skapar, ändrar eller tar bort kundattributskällor är det en fördröjning på upp till en timme innan ID:n börjar synkronisera med den nya datakällan. Du måste ha administratörsbehörighet i Audience Manager för att skapa eller ändra källor för kundattribut. Kontakta Audience Manager Customer Care eller konsult för att få administratörsrättigheter.


1. Klicka på [!DNL Experience Cloud]ikonen Meny i ![](assets/menu-icon.png) .
1. Klicka **[!DNL Experience Platform]** under **[!UICONTROL People]** > **[!UICONTROL Customer Attributes]**.

   På [!UICONTROL Customer Attributes] sidan kan du hantera och redigera befintliga attributdatakällor.

   ![Stegresultat](assets/03_crs_usecase.png)
1. Klicka på **[!UICONTROL New]**.

   ![Stegresultat](assets/04_crs_usecase.png)
1. Konfigurera följande fält på [!UICONTROL Edit Customer Attribute Source] sidan:


   * **[!UICONTROL Name:]** Ett eget namn för datakällan för dataattribut. Attributnamn [!DNL Adobe Target]får inte innehålla blanksteg. Om ett attribut med ett blanksteg skickas, [!DNL Target] ignoreras det. Andra tecken som inte stöds är: `< , >, ', "`.

   * **[!UICONTROL Description:]** (Valfritt) En beskrivning av datakällan för dataattribut.

   * **[!UICONTROL Alias ID:]** Representerar en källa för kundattributdata, t.ex. ett specifikt CRM-system. Ett unikt ID som används i källkoden för kundattributet. ID:t ska vara unikt, med gemener, utan blanksteg. Det värde som anges i fältet Alias ID för en kundattributkälla i Experience Cloud-gränssnittet bör matcha de värden som skickas från implementeringen (oavsett om det är via dynamisk tagghantering eller JavaScript för Mobile SDK.)

      Alias-ID motsvarar vissa områden där du anger ytterligare värden för Kund-ID. Exempel:

      * **Dynamisk tagghantering:** Alias-ID motsvarar *integreringskodvärdet* under [!UICONTROL Customer Settings]i [Experience Cloud ID-tjänstverktyget](https://docs.adobe.com/content/help/en/dtm/using/tools/macid.html) .

      * **Besökar-API:** Alias-ID motsvarar de ytterligare [kund-ID](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) som du kan koppla till varje besökare.

         Till exempel *&quot;crm_id&quot;* i:


         ```
         "crm_id":"67312378756723456"
         ```


      * **iOS:** Alias-ID motsvarar *&quot;idType&quot;* i [visitorSyncIdentifiers:identifiers](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html).

         Exempel:

         `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`


      * **Android:** Alias-ID motsvarar *&quot;idType&quot;* i [syncIdentifiers](https://docs.adobe.com/content/help/en/mobile-services/android/overview.html).

         Exempel:

         `identifiers.put(`**`"idType"`**`, "idValue");`

         Se [Använda flera datakällor](../attributes/crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB) för mer information om databearbetning för Alias ID-fältet och Kund-ID:n.
   * **[!UICONTROL File Upload:]** Du kan dra och släppa datafilen eller överföra data via FTP. `.csv` (FTP kräver också en `.fin` fil.) Se [Överföra data via FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B).


      >[!IMPORTANT]
      >
      >Det finns särskilda krav på datafiler. Mer information finns i [Datafilskrav](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) .


      När du har överfört filen visas tabelldata under rubriken på den här sidan [!UICONTROL File Upload] . Du kan validera schemat, konfigurera prenumerationer eller konfigurera FTP.



      **Filöverföring - grafik**

      ![](assets/file_upload_attributes.png)

   * **[!UICONTROL Unique Customer ID:]** Visar hur många unika ID:n du har överfört till den här attributkällan.

   * **[!UICONTROL Customer-Provided IDs Aliased to Experience Cloud Visitor IDs:]** Visar hur många ID:n som har alias för Experience Cloud Visitor ID:n.

   * **[!UICONTROL Customer-Provided IDs with High Alias Counts:]** Visar antalet kundtillhandahållna ID:n med 500 eller fler aliaserade Experience Cloud-besökar-ID:n. Dessa kundtillhandahållna ID:n representerar förmodligen inte individer utan snarare någon typ av delad inloggning. Systemet distribuerar de attribut som är kopplade till dessa ID:n till de 500 senast aliaserade Experience Cloud Visitor ID:n, tills aliasantalet når 10 000. Då blir det kundens ID ogiltigt och distribuerar inte längre tillhörande attribut.










## Validera schemat {#task_404AAC411B0D4E129AB3AC8B7BE85859}

Med valideringsprocessen kan du mappa visningsnamn och beskrivningar till överförda attribut (strängar, heltal, tal och så vidare). Du kan även ta bort attribut genom att uppdatera schemat.

Se [Validera schemat](../attributes/validate-schema.md#concept_B3A01A15D04E4F998118E09B3A9B5043).

Information om hur du tar bort attribut finns i [(Valfritt) Uppdatera schemat (tar bort attribut)](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C).

## (Valfritt) Uppdatera schemat (ta bort attribut) {#task_6568898BB7C44A42ABFB86532B89063C}

Så här tar du bort attribut och ersätter attribut i schemat.


1. På [!UICONTROL Edit Customer Attribute Source] sidan tar du bort **[!UICONTROL Target]** eller **[!UICONTROL Analytics]** prenumerationen (under [!UICONTROL Configure Subscriptions]).
1. [Överför en ny datafil med uppdaterade fält](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8).

## Konfigurera prenumerationer och aktivera attributkällan {#task_1ACA21198F0E46A897A320C244DFF6EA}

När du konfigurerar en prenumeration skapas dataflödet mellan Experience Cloud och lösningar. Genom att aktivera attributkällan kan data flöda till prenumererade lösningar. De kundposter som du har överfört matchas med inkommande ID-signaler från din webbplats eller ditt program.

Se [Konfigurera prenumerationer](../attributes/subscription.md#concept_ECA3C44FA6D540C89CC04BA3C49E63BF).

**Så här aktiverar du en attributkälla**

På sidan [!UICONTROL Create New [or Edit] Customer Attribute Source] letar du reda på [!UICONTROL Activate] rubriken och klickar sedan på **[!UICONTROL Active]**.

![Stegresultat](assets/activate_attribute_source.png)

## Använd kundattribut i Adobe Analytics {#task_7EB0680540CE4B65911B2C779210915D}

Med data som nu finns i lösningar som
<keyword>
Adobe Analytics
</keyword>kan ni rapportera om data, analysera dem och vidta lämpliga åtgärder i era marknadsföringskampanjer.

I följande exempel visas ett [!DNL Analytics] segment baserat på de överförda attributen. I det här segmentet visas Photoshop Lightroom-prenumeranter vars mest lanserade produkt är Photoshop.

![](assets/08_crs_usecase.png)

När du publicerar ett segment till Experience Cloud blir det tillgängligt i Experience Cloud-målgrupper och Audience Manager.

Mer information finns i [Kundattributrapport](https://docs.adobe.com/help/en/analytics/components/variables/dimensions-reports/reports-customer-attributes.html) i Analytics-hjälpen.

## Använd kundattribut i Adobe Target {#task_FC5F9D9059114027B62DB9B1C7D9E257}

I Target kan du välja ett kundattribut i avsnittet Besökarprofil när du skapar en målgrupp. Alla kundattribut har prefixet [!DNL crs.] i listan. Kombinera dessa attribut efter behov med andra dataattribut för att skapa målgrupper.

![](assets/crs-add-attribute-target.png)

Se [Skapa en ny publik](https://docs.adobe.com/content/help/en/target/using/audiences/create-audiences/audiences.html) i hjälpen för Target.