---
title: Vad är kundattribut och hur fungerar de?
description: Läs mer om tjänsten Customer Attributes i Adobe Experience Cloud. Upptäck hur du överför kundattributdata för användning i Adobe Analytics och Adobe Target.
solution: Experience Cloud
feature: Experience Cloud Customer Attributes
role: Administrator
translation-type: tm+mt
source-git-commit: 253ec3d13c66be792214e09616f83e8b24929c3c
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 1%

---


# Så här använder du kundattribut i Experience Cloud

Med kundattribut i Adobe Experience Cloud kan du överföra dina hämtade företagsdata från en CRM-databas (customer relationship management). Du kan överföra data till en datakälla för kundattribut i Experience Cloud och sedan använda data i Adobe Analytics och Adobe Target.

Navigera till **[!DNL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Customer Attributes]**

![](assets/custom_reports.png)

## Krav för att överföra kundattribut {#section_BD38693AFBF34926BA28E964963B4EA0}

* **Aktivera lösningar:** [Aktivera lösningar för Experience Platform-tjänster](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C).

* **Gruppmedlemskap:** För att kunna överföra kundattributdata måste användarna vara medlemmar i gruppen [ ](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)Kundattribut. Du måste också tillhöra en Adobe Analytics-grupp eller en Adobe Target-grupp.

   Om du vill veta om ditt företag har tillgång till kundattribut ska [!DNL Experience Cloud]-administratören logga in på [Experience Cloud](https://experience.adobe.com). Navigera till **[!UICONTROL Administration]** > **[!UICONTROL Admin Console]** > **[!UICONTROL Products]**. Om *kundattribut* visas som en av [!UICONTROL Product Profiles] är du redo att börja.

   Användare som läggs till i kundattributen kan se menyalternativet [!UICONTROL Customer Attributes] till vänster om Experience Cloud.

* **Adobe Target** `at.js`  (valfri version) eller  `mbox.js` version 58 eller senare krävs för kundattribut.

   Se [Så här distribuerar du at.js](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/deploy-at-js/how-to-deployatjs.html) eller [implementering av Mbox.js](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/mbox-download.html).

## Vad är företagsdata? {#section_6F34C29F11414842AA57D2B1248FA3C6}

Företagsdata finns i andra system. Det kan vara komplicerat och betyda olika saker för olika människor. Dessa data kan omfatta information som medlemskap, lojalitetsnivå, ålder, kön, ägda produkter, intressen och livstidsvärde.

Följande bild är ett exempel på en datafil som visar prenumerationsdata för produkter, inklusive medlems-ID, berättigade produkter, de mest lanserade produkterna osv.

![](assets/01_crs_usecase.png)

När du har skapat datafilen kan du överföra den till kundattributskällan som du skapar i **[!UICONTROL Experience Cloud]** > **[!UICONTROL Customer Attributes]**.

Mer information om det här arbetsflödet finns i [Överför kundattributdata](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

## Exempel på kundattribut i Analytics och Target {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

När data finns i Experience Cloud kan ni anpassa dem och dela dem till lösningar för rapportering, segmentering, aktiviteter och kampanjer.

Exempel:

| Lösning | Fördelar och användningsområden |
|--- |--- |
| Adobe Analytics | Marknadsförare och analytiker kan förstå:<ul><li>De onlinekampanjer som är mest effektiva för era kunder på guldnivå.</li><li>De produkter som kunder på guldnivå söker efter jämfört med produkter som kunder på platinanivå söker efter.</li><li>Om omdesignen av webbplatsen har en positiv inverkan på konverteringsgraden för äldre kunder.</li><li>Vilka produkter har kunder med lågt livstidsvärde en tendens att hitta på min webbplats.</li></ul> |
| Adobe Target | Med attributdata kan Adobe Target-användare:<ul><li>Visa specialrabatter och erbjudanden för medlemmar i lojalitetsklubben.</li><li>Rekommendera dyrare produkter till era lyxkunder.</li><li>För kunder som redan får e-postmeddelanden kan du visa ett merförsäljningserbjudande i det utrymme som normalt är reserverat för e-postregistreringar</li></ul> |
