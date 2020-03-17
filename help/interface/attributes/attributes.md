---
description: Översikt och förutsättningar för att överföra kundattribut till Experience Cloud.
keywords: core services;customer attributes
seo-description: Översikt och förutsättningar för att överföra kundattribut till Experience Cloud.
seo-title: Kundattribut
solution: Experience Cloud
title: Kundattribut
uuid: 1621402d-990f-46f9-981a-473280559069
translation-type: tm+mt
source-git-commit: 12c3ac8bfa64b7c8708312576ac6dc4036c1b7d8

---


# Kundattribut

## Översikt

Navigera [!UICONTROL customer attributes] till **[!DNL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Customer Attributes]**

Om du samlar in företagsdata i en CRM-databas (customer relationship management) kan du överföra data till en datakälla för kundattribut i Experience Cloud. När data har överförts kan du utnyttja dem i [!DNL Adobe Analytics] och [!DNL Adobe Target].

![](assets/custom_reports.png)

## Krav för överföring av kundattribut {#section_BD38693AFBF34926BA28E964963B4EA0}


* **Aktivera lösning:** [Möjliggör lösningar för bastjänster](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C).

* **Gruppmedlemskap:** För att kunna överföra kundattributdata måste användarna vara medlemmar i gruppen [](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)Kundattribut. Du måste också tillhöra antingen en Adobe Analytics-grupp eller en Adobe Target-grupp.

   Om du vill veta om ditt företag har tillgång till kundattribut bör din [!DNL Experience Cloud] administratör logga in på [!DNL Experience Cloud]. Navigera till **[!UICONTROL Administration]** > **[!UICONTROL Launch Admin Console]** > **[!UICONTROL Groups]**. Om *kundattribut* visas som en av grupperna är du redo att börja.

   Användare som läggs till i gruppen Kundattribut ser menyalternativet till vänster [!UICONTROL Customer Attributes] i Experience Cloud-gränssnittet.

* **Målruta:** mbox.js version 58 eller senare krävs för kundattribut.


   Se Implementering av [Mbox.js](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/mbox-download.html).

* **at.js:** Alla versioner.

## Vad är företagsdata? {#section_6F34C29F11414842AA57D2B1248FA3C6}

Företagsdata finns i andra system. Det kan vara komplicerat och betyda olika saker för olika människor. Dessa data kan omfatta information som medlemskap, lojalitetsnivå, ålder, kön, ägda produkter, intressen och livstidsvärde.

Följande bild är ett exempel på en datafil som visar prenumerationsdata för produkter, inklusive medlems-ID, berättigade produkter, de mest lanserade produkterna osv.

![](assets/01_crs_usecase.png)

När du har skapat datafilen kan du överföra den till kundattributkällan som du skapar i **[!UICONTROL Experience Cloud]** > **[!UICONTROL Customer Attributes]**.

Mer information om det här arbetsflödet finns i [Överför kundattributdata](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78) .

## Användningsexempel för lösning {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

När data finns i Experience Cloud kan ni anpassa dem och dela dem med lösningar för rapportering, segmentering, aktiviteter och kampanjer.

Exempel:

| Lösning | Fördelar och användningsområden |
|--- |--- |
| Adobe Analytics | Marknadsförare och analytiker kan förstå:<ul><li>De onlinekampanjer som är mest effektiva för era kunder på guldnivå.</li><li>De produkter som kunder på guldnivå söker efter jämfört med produkter som kunder på platinanivå söker efter.</li><li>Huruvida omdesignen av webbplatsen har en positiv inverkan på konverteringsgraden för äldre kunder.</li><li>Vilka produkter har kunder med lågt livstidsvärde en tendens att hitta på min webbplats.</li></ul> |
| Adobe Target | Med attributdata kan målanvändare:<ul><li>Visa specialrabatter och erbjudanden för medlemmar i lojalitetsklubben.</li><li>Rekommendera dyrare produkter till era lyxkunder.</li><li>För kunder som redan får e-post, visa ett merförsäljningserbjudande i det utrymme som normalt är reserverat för e-postregistreringar</li></ul> |