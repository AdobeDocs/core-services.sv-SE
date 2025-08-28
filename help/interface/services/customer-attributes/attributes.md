---
title: Om [!DNL Customer Attributes]
description: Läs mer om  [!DNL Customer Attributes] i Experience Cloud. Upptäck hur du överför data från kundattribut för användning i Adobe Analytics och Adobe Target.
solution: Experience Cloud,Target,Analytics
feature: Customer Attributes
role: Admin
topic: Administration
level: Experienced
exl-id: fe8ad013-76da-49f8-aa51-dc5f6c1b1d79
source-git-commit: 21120abb5ab0fcc8d556012851548f39f3875038
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 5%

---

# [!DNL Customer Attributes] i Experience Cloud

Med [!DNL Customer Attributes] i Experience Cloud kan du överföra dina hämtade företagsdata från en CRM-databas (customer relationship management). Du kan överföra data till en datakälla för kundattribut i Experience Cloud och sedan använda data i [!DNL Adobe Analytics] och [!DNL Adobe Target].

## Hitta funktionen [!DNL Customer Attributes]

1. Logga in på [!DNL Experience Cloud] och välj menyikonen ![menu](assets/menu-icon.png) .

1. Välj **[!DNL Customer Attributes]**.

![Översikt över kundattribut](assets/custom_reports.png)

## Krav för överföring av kundattributdata {#prerequisites}

* **Gruppmedlemskap:** Om du vill överföra kundattributdata måste användarna vara medlemmar i gruppen Kundattribut. Du måste också tillhöra en Adobe Analytics-grupp eller en Adobe Target-grupp.

  Om du vill veta om ditt företag har åtkomst till kundattribut bör [!DNL Experience Cloud]-administratören logga in på [Experience Cloud](https://experience.adobe.com). Navigera till **[!UICONTROL Admin Console]** > **[!UICONTROL Products]**. Om *[!DNL Customer Attributes]* visas som en av [!UICONTROL product profiles] är du redo att börja.

  Användare som läggs till i [!DNL Customer Attributes] ser menyalternativet [!DNL Customer Attributes] till vänster i Experience Cloud-gränssnittet.

* **Adobe Target** `at.js` (valfri version) eller `mbox.js` version 58 eller senare krävs för kundattribut.

  Se [Distribuera på.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html?lang=sv-SE).

## Vad är företagsdata? {#enterprise_data}

Företagsdata finns i andra system. Det kan vara komplicerat och betyda olika saker för olika människor. Dessa data kan omfatta information som medlemskap, lojalitetsnivå, ålder, kön, ägda produkter, intressen och livstidsvärde.

Följande bild är ett exempel på en datafil som visar prenumerationsdata för produkter, inklusive medlems-ID, berättigade produkter, de mest lanserade produkterna osv.

![Vad är företagskunddata?](assets/01_crs_usecase.png)

När du har skapat datafilen kan du överföra den till kundattributskällan som du skapar i **[!UICONTROL Experience Cloud]** > **[!UICONTROL Customer attributes]**.

Mer information om det här arbetsflödet finns i [Överför kundattributdata](t-crs-usecase.md).

## Exempel på kundattribut i Analytics och Target {#examples}

När data finns i Experience Cloud kan ni anpassa dem och dela dem med lösningar för rapportering, segmentering, aktiviteter och kampanjer.

Exempel:

| Lösning | Fördelar och användningsområden |
|--- |--- |
| Adobe Analytics | Marknadsförare och analytiker kan förstå:<ul><li>De onlinekampanjer som är mest effektiva för era kunder på guldnivå.</li><li>De produkter som kunder på guldnivå söker efter jämfört med produkter som kunder på platinanivå söker efter.</li><li>Huruvida omdesignen av webbplatsen har en positiv inverkan på konverteringsgraden för äldre kunder.</li><li>De produkter som kunder med en låg livstid har tenderar att undersöka på min webbplats.</li></ul> |
| Adobe Target | Med attributdata kan Adobe Target-användare:<ul><li>Visa specialrabatter och erbjudanden för medlemmar i lojalitetsklubben.</li><li>Rekommendera dyrare produkter till era lyxkunder.</li><li>För kunder som redan får e-postmeddelanden kan du visa ett merförsäljningserbjudande i det utrymme som normalt är reserverat för e-postregistreringar</li></ul> |

{style="table-layout:auto"}
