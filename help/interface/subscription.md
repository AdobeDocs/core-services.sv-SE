---
description: Lär dig mer om lösningsdatakällor och hur du konfigurerar prenumerationer. Prenumerationer möjliggör dataflöde mellan Experience Cloud och lösningar för kundattribut (Analytics och Target).
keywords: Kundattribut;bastjänster
solution: Experience Cloud
title: 'Konfigurera prenumerationer '
uuid: f74a8155-0a21-46b3-9b1e-4c838f72f24f
feature: Kundattribut
topic: Administrering
role: Administrator
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
source-git-commit: ebefd433e96da422674e7ee71c8988d4011fed11
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---

# Konfigurera prenumerationer i Experience Cloud

Lär dig mer om lösningsdatakällor och hur du konfigurerar prenumerationer. Prenumerationer möjliggör dataflöde för kundattribut mellan Experience Cloud och lösningar ([!DNL Analytics] och [!DNL Target]).

En Adobe Analytics-prenumeration kan t.ex. aktivera attributdata i rapporter. Om du använder Adobe Target kan du överföra kundattribut för målgruppsanpassning och segmentering.

**[!UICONTROL Customer Attribute Source]** > **[!UICONTROL Create New Customer Attribute Source]** > **[!UICONTROL New]**

![](assets/configure_subscription_page.png)

| Element | Beskrivning |
|--- |--- |
| Lösning | **Adobe**<br> AnalyticsVälj Analytics, ange de rapportsviter som du vill ta emot attributdata till och de attribut som ska inkluderas.<br>**Adobe**<br> TargetDu kan överföra kundattribut för målinriktning och segmentering. Den här funktionen är användbar om du vill ha ett test baserat på attributdata eller göra data tillgängliga för segmentering i Analytics.<br>Överförda kundattributdata för en besökare finns tillgängliga vid inloggning, i  **[!DNL Target]** >  **Publiker**.<br>Flera datakällor stöds. När du [anger kund-ID](core-services.md) på webbplatsen kontrollerar du att minst ett av aliaserna prenumererar på [!DNL Target]. |
| Report Suite (Analytics) | Rapporteringssviterna från Analytics.<br>Du kan inte lägga till mer än totalt 10 rapportsviter i Analytics-prenumerationer i en enda attributkälla. När du väljer vilka rapportsviter som ska inkluderas bör du tänka på följande:<ul><li>Välj rapportsviter som har en gemensam uppsättning autentiserade kunder. Om de autentiserade kunderna i en rapportserie inte överlappar de autentiserade kunderna i en annan rapportserie, skiljer du dessa rapportsviter åt i olika attributkällor.</li><li>Om det är möjligt bör rapportsviterna som ingår i en attributkälla ha liknande trafikvolym.</li></ul><br>Om ni har fler än 10 rapportsviter med en gemensam uppsättning autentiserade kunder kan ni konfigurera ytterligare källor för kundattribut, var och en med upp till 10 rapportsviter. |
| Attribut som ska inkluderas (Analytics och [!DNL Target]) | De attribut som du vill skicka till lösningen. <br>När du konfigurerar prenumerationer och väljer attribut gäller följande begränsningar  _per rapportsvit,_ beroende på vilka lösningar du har:<ul><li>Foundation: 0</li><li>Välj: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 totalt</li><li>Premium: 200 per rapportserie</li><li>[!DNL Target] Standard: 5</li><li>[!DNL Target] Premium: 200</li></ul><br>**Obs!** När du uppgraderar till Analytics Premium uppstår en 24-timmars fördröjning innan ytterligare attribut är tillgängliga. Ett Max-fel för attributprenumeration kan visas under den här fördröjningen. |
