---
description: Frågor och svar om [!DNL Customer Attributes] i Adobe Experience Cloud, för Adobe Analytics och Adobe Target.
solution: Experience Cloud
title: Vanliga frågor om [!DNL Customer Attributes]
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 1%

---

# Frågor och svar om [!DNL Customer Attributes]

Vanliga frågor och bästa praxis för [!DNL Customer Attributes] i Adobe Analytics och Adobe Target.

## God praxis och begränsningar {#section_7F5189B3DAA84EE6865B91D2026EE05A}

Vägledning och begränsningar vid användning [!DNL Customer Attributes].

| Problem | Beskrivning |
|--- |--- |
| [!UICONTROL Customer attribute] prenumerationsbegränsningar | När du uppgraderar till Analytics Premium tar det 24 timmar innan fler attribut finns tillgängliga. Du kanske ser en [!UICONTROL Attribute Subscription Max] fel uppstod under denna fördröjning. |
| Flera inloggningar på samma enhet | När du använder [!DNL Customer Attributes] om du vill överföra kundprofiler till en datakälla rekommenderar Adobe mot användare som delar enheter (dvs. samma Experience Cloud-ID). Experience Cloud ID (ECID) finns kvar på enheten. Delningsenheter kan göra att ECID länkar flera användare till samma ECID, vilket kan ge oväntade resultat [!DNL Target]. **Obs!** För mobiler är ECID permanent efter att mobilappen har installerats. Installera om programmet för att generera ett nytt ECID. För webben genereras ett nytt ECID när webbläsarens cookie har rensats. |
| Begränsning av överföring av frekvens per dag | Adobe rekommenderar att du uppdaterar [!DNL Customer Attributes] endast en gång om dagen. Du måste vänta minst 24 timmar för att överföra ytterligare en kundprofildatafil för samma uppsättning profiler. |
| ID för anpassad analys (`s.visitorID`) | Ange ett kund-ID med `s.visitorID` är ett sätt att identifiera användare i Analytics. integreringar i vilka [!DNL Analytics] data exporteras eller importeras med ID-tjänsten fungerar inte när en besökare identifieras med `s.visitorID.`<br>Detta omfattar, men är inte begränsat till, delade målgrupper, [!DNL Analytics] för Adobe Target (A4T), och [!DNL Customer Attributes].<br>För dessa integreringar stöds inte inställning av ett anpassat analys-ID. |
| Begränsningar i teckenlängd i [!DNL Analytics] | När en [!DNL Analytics] prenumerationer, förkortas fältlängden för de överförda filerna till 255. |

{style="table-layout:auto"}

## Frågor och svar om [!DNL Customer Attributes] {#section_E47866EEA83348E09FE43CEC5E44C461}

| Fråga | Svar |
|--- |--- |
| Kan jag få meddelanden om överföringsstatus för [!DNL Customer Attributes]? | Ja. |
| Vad bör jag göra för att komma igång med [!DNL Customer Attributes]? | <ol><li>Få etablerat. Om du är Analytics-kund etablerar Adobe dig för [!DNL Customer Attributes]. Om du bara använder Adobe Target och inte har Analytics, begär du etablering för bastjänsterna genom att kontakta Kundtjänst.</li> <li>Diskutera med CRM-teamet. Ta reda på vilken typ av kunddata som finns tillgängliga och som du vill använda i Analytics och i hela Experience Cloud.</li><li>Implementera bastjänster.</li></ol> |
| Hur många [!DNL Customer Attributes] Får jag använda? | Du kan överföra hundratals `.csv` kolumner till tjänsten Customer Attribute. När du konfigurerar prenumerationer och väljer attribut gäller dock följande begränsningar (per rapportsvit), beroende på vilka program du äger:  <ul><li>Foundation: 0</li><li>Välj: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 totalt</li><li>Premium: 200</li><li>Adobe Target Standard: 5</li><li>Adobe Target Premium: 200</li></ul> |
| Krävs migrering till Experience Cloud ID-tjänsten? | Migreringen beror på vilka program du använder. <ul><li>Adobe Analytics: Vi rekommenderar </li><li>Adobe Target: Obligatoriskt. </li></ul><br>Med tjänsten Experience Cloud ID får du tillgång till de senaste Experience Cloud-funktionerna, inklusive målgrupper i realtid, Adobe Target modernisering, Analytics-integrering och loggning av pulsslag. |
| Hur hör kundattributsfunktionen ihop med Adobe Audience Manager? | Även om Audience Manager kan ta emot data för att utföra målgruppsidentifiering kan det inte utföra analysfunktioner som kopplar attribut till historiska beteendedata. Den innehåller inte heller de funktioner för rapportering, analys och segmentering som finns i Adobe Analytics. [!UICONTROL People] gör att omfattande data från olika program kan knytas ihop och kopplas till ett enda ID för användning i hela Experience Cloud. <br>I ADOBE TARGET [!DNL Customer Attributes] visas som enskilda attribut som kan kombineras med andra regler för att skapa målgrupper. Målgrupper som delas med [!UICONTROL People] är fullmålgrupper som inte kan ändras. |
| **(Endast analys)** På vilket sätt skiljer sig den här funktionaliteten från vad som ingår i Analytics Premium? | Tidigare har kunder som är intresserade av att kombinera kundattributsdata med analysdata varit starkt beroende av Datan Workbench för den här funktionen. [!DNL Customer Attributes] ger en större publik tillgång till denna funktionalitet genom att erbjuda [!DNL Customer Attributes] som mått och mätvärden i rapporter och analyser, Ad Hoc Analysis och Report builder. Analytics Standard-kunder har tillgång till [!DNL Customer Attributes], men med begränsade funktioner. Den fullständiga funktionaliteten är tillgänglig för kunder som har Analytics Premium. |
| **(Endast Adobe Target)** Kan jag ladda upp data i förväg till kunder som Adobe Target aldrig har sett? | Ja. När besökaren gör sin första förfrågan till Adobe Target hämtar systemet den befintliga information som Adobe har om dem från [!DNL Customer Attributes] och använda dessa data för målinriktning. **Obs!**  Det kan ta upp till 20 minuter att hämta data från besökarens första interaktion med Adobe Target. |
| **(Endast Adobe Target)** Kan jag skapa en supermålgrupp genom att kombinera kundattributsdata med delade målgruppsdata? | Nej. Delade målgruppsdata är en komplett målgrupp. |
| **(endast Adobe Target)** Hur fungerar [!DNL Customer Attributes] jämfört med Adobe Target massprofil-API? | Massprofilens API gör att Adobe Target-profiler kan uppdateras direkt via API:t, antingen för en enskild profil eller gruppvis. Funktionen liknar [!DNL Customer Attributes], med följande viktiga skillnader:<ul><li>Profil-API:t är ett REST API-anrop och [!DNL Customer Attributes] använder FTP.</li><li>Adobe Target profil-API skickar bara data till Adobe Target i stället för till hela Experience Cloud.</li><li>[!DNL Customer Attributes] har ett enkelt gränssnitt för att skapa och hantera externa data.</li></ul> |
| **(endast Adobe Target)** Överför data från [!DNL Customer Attributes] till Adobe Target förlänga Adobe Target besökares livslängd? | Ja. Se [Livstid för besökarprofil](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html) i Adobe Target Help. |
| **(endast Adobe Target)** Kan jag rikta in mig på data som överförs i [!DNL Customer Attributes] omedelbart efter det att besökaren har identifierats av kund-ID:t? | Ja. På serveranropet till Adobe Target, som innehåller mbox-ID:t, finns alla kundattributsdata tillgängliga. |
| **(endast Adobe Target)** Vad gör **[!UICONTROL Sync Status]** representerar kolumnen filer som överförts i kundattributskällan? | Du kan visa antalet poster som publicerats och synkroniserats av Adobe Target genom att välja ikonen Synkroniseringsstatus mot en viss attributfil. `Sync %` är ett realtidsmått som anger procentandelen profiler som har synkroniserats i Adobe Target.<br> **Obs!** Det kan ta upp till 24 timmar för attribut att synkronisera med Adobe Target. |
| Vad representerar mätvärdena för filöverföring i [!DNL Customer Attributes] Källa? | Du kan kontrollera statusen för attribut som överförts till [!DNL Customer Attributes] med hjälp av följande mätvärden: <ul><li>Poster: Antal poster i attributfilen.</li><li>**Nya poster:** Antal nya poster i attributfilen.</li> <li>**Uppdaterade poster:** Antal poster i som finns i [!DNL Customer Attributes] med uppdaterade värden i filen.</li><li>**Alla data (poster):** Totalt antal poster som har överförts till [!DNL Customer Attributes].</li></ul> |

{style="table-layout:auto"}