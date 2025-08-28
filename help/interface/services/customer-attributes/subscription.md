---
description: Lär dig hur du konfigurerar prenumerationer på kundattribut för Analytics och Target samt hur du aktiverar en datakälla.
solution: Experience Cloud
title: Konfigurera prenumerationer
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
source-git-commit: fc60b49af0839769fdd8d18fd61863c8b28bbd57
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 1%

---

# Konfigurera prenumerationer och aktivera datakällan

Prenumerationer möjliggör dataflöde för kundattribut mellan Experience Cloud och program ([!DNL Analytics] och [!DNL Target]).

En Adobe Analytics-prenumeration kan t.ex. aktivera attributdata i rapporter. Om du använder Adobe Target kan du överföra kundattribut för målgruppsanpassning och segmentering.

**Konfigurera prenumerationer och aktivera datakällan**

1. Leta reda på kundens attributkälla för redigering:

   I [!DNL Experience Cloud] klickar du på **[!UICONTROL Apps]** ![menu](assets/menu-icon.png) > **[!DNL Customer Attributes]**.

1. På [!UICONTROL Edit Customer Attribute Source] klickar du på **[!UICONTROL File Upload]**.

1. Klicka på **[!UICONTROL Configure Subscriptions]**.

   ![Konfigurera prenumerationer i Experience Cloud](assets/configure-subscriptions.png)

1. Om du vill aktivera kundattributkällan klickar du på **[!UICONTROL Active]** och sedan på **[!UICONTROL Save]**.

1. Om du vill konfigurera en prenumeration på [!DNL Analytics] eller [!DNL Target] klickar du på **[!UICONTROL Configure]**.

   I följande exempel visas en [!DNL Target]-prenumeration:

   ![Stegresultat](assets/subscription-target.png)

   | Element | Beskrivning |
   |--- |--- |
   | Lösning | **Adobe Analytics**<br> Välj [!DNL Analytics], ange de rapportsviter som du vill ta emot attributdata till och de attribut som ska inkluderas.<br>**Adobe Target**<br> Du kan överföra kundattribut för målinriktning och segmentering. Den här funktionen är användbar om du vill ha ett test som bygger på attributdata eller göra data tillgängliga för segmentering i Analytics.<br>Överförda kundattributdata för en besökare är tillgängliga vid inloggning, i **[!DNL Target]** > **Publiker**.<br>Flera datakällor stöds. När du anger kund-ID:n på webbplatsen kontrollerar du att minst ett av aliasen prenumererar på [!DNL Target]. |
   | Report Suite (Adobe Analytics) | Rapporteringssviterna från Analytics.<br>Du kan inte lägga till mer än totalt 10 rapportsviter i Analytics-prenumerationer i en enda attributkälla. När du väljer vilka rapportsviter som ska inkluderas bör du tänka på följande:<ul><li>Välj rapportsviter som har en gemensam uppsättning autentiserade kunder. Om de autentiserade kunderna i en rapportserie inte överlappar de autentiserade kunderna i en annan rapportserie, skiljer du dessa rapportsviter åt i olika attributkällor.</li><li>Om det är möjligt bör rapportsviterna som ingår i en attributkälla ha liknande trafikvolym.</li></ul><br>Om du har fler än 10 rapportsviter med en gemensam uppsättning autentiserade kunder kan du konfigurera ytterligare källor för kundattribut, var och en med upp till 10 rapportsviter. |
   | Attribut som ska inkluderas (Analytics och [!DNL Target]) | De attribut som du vill skicka till programmet. <br>När du konfigurerar prenumerationer och väljer attribut gäller följande begränsningar _per rapportserie,_ beroende på vilka program du äger:<ul><li>Foundation: 0</li><li>Välj: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 totalt</li><li>Premium: 200 per rapportserie</li><li>[!DNL Target] Standard: 5</li><li>[!DNL Target] Premium: 200</li></ul><br>**Obs!** När du uppgraderar till Analytics Premium uppstår en 24-timmars fördröjning innan ytterligare attribut är tillgängliga. Det kan hända att ett maximalt fel för attributprenumeration utfärdas under fördröjningen. |

1. Klicka på **[!UICONTROL Save]**.
