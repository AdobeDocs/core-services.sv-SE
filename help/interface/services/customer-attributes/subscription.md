---
description: Lär dig mer om lösningsdatakällor och hur du konfigurerar prenumerationer. Prenumerationer möjliggör dataflöde för kundattribut mellan Experience Cloud och program (Analytics och Target).
solution: Experience Cloud
title: Konfigurera prenumerationer
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Konfigurera prenumerationer i Experience Cloud

Lär dig mer om programdatakällor och hur du konfigurerar prenumerationer. Prenumerationer aktiverar dataflödet [!DNL customer attribute] mellan Experience Cloud och program ([!DNL Analytics] och [!DNL Target]).

En Adobe Analytics-prenumeration kan t.ex. aktivera attributdata i rapporter. Om du använder Adobe Target kan du överföra kundattribut för målgruppsanpassning och segmentering.

**[!UICONTROL customer attribute Source]** > **[!UICONTROL Create New customer attribute Source]** > **[!UICONTROL New]**

![Konfigurera prenumerationer i Experience Cloud](assets/configure_subscription_page.png)

| Element | Beskrivning |
|--- |--- |
| Lösning | **Adobe Analytics**<br> Välj [!DNL Analytics], ange de rapportsviter som du vill ta emot attributdata till och de attribut som ska inkluderas.<br>**Adobe Target**<br> Du kan överföra kundattribut för målinriktning och segmentering. Den här funktionen är användbar om du vill ha ett test som bygger på attributdata eller göra data tillgängliga för segmentering i Analytics.<br>Överförda kundattributdata för en besökare är tillgängliga vid inloggning, i **[!DNL Target]** > **Publiker**.<br>Flera datakällor stöds. När du anger kund-ID:n på webbplatsen kontrollerar du att minst ett av aliasen prenumererar på [!DNL Target]. |
| Report Suite (Adobe Analytics) | Rapporteringssviterna från Analytics.<br>Du kan inte lägga till mer än totalt 10 rapportsviter i Analytics-prenumerationer i en enda attributkälla. När du väljer vilka rapportsviter som ska inkluderas bör du tänka på följande:<ul><li>Välj rapportsviter som har en gemensam uppsättning autentiserade kunder. Om de autentiserade kunderna i en rapportserie inte överlappar de autentiserade kunderna i en annan rapportserie, skiljer du dessa rapportsviter åt i olika attributkällor.</li><li>Om det är möjligt bör rapportsviterna som ingår i en attributkälla ha liknande trafikvolym.</li></ul><br>Om du har fler än 10 rapportsviter med en gemensam uppsättning autentiserade kunder kan du konfigurera ytterligare källor för kundattribut, var och en med upp till 10 rapportsviter. |
| attribut att inkludera (Analytics och [!DNL Target]) | De attribut som du vill skicka till programmet. <br>När du konfigurerar prenumerationer och väljer attribut gäller följande begränsningar _per rapportserie,_ beroende på vilka program du äger:<ul><li>Foundation: 0</li><li>Välj: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 totalt</li><li>Premium: 200 per rapportserie</li><li>[!DNL Target] Standard: 5</li><li>[!DNL Target] Premium: 200</li></ul><br>**Obs!** När du uppgraderar till Analytics Premium uppstår en 24-timmars fördröjning innan ytterligare attribut är tillgängliga. Det kan hända att ett maximalt fel för attributprenumeration utfärdas under fördröjningen. |

{style="table-layout:auto"}
