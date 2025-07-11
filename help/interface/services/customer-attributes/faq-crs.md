---
description: Vanliga frågor om  [!DNL customer attributes] i Adobe Experience Cloud, för Adobe Analytics och Adobe Target.
solution: Experience Cloud
title: Vanliga frågor om  [!DNL customer attributes]
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 0%

---

# Vanliga frågor om [!DNL customer attributes]

Vanliga frågor och metodtips för [!DNL customer attributes] i Adobe Analytics och Adobe Target.

## God praxis och begränsningar {#best_practices}

Vägledning och begränsningar när [!DNL customer attributes] används.

| Problem | Beskrivning |
|--- |--- |
| [!UICONTROL customer attribute] prenumerationsbegränsningar | När du uppgraderar till Analytics Premium tar det 24 timmar innan fler attribut finns tillgängliga. Ett [!UICONTROL attribute Subscription Max]-fel kan ha uppstått under fördröjningen. |
| Flera inloggningar på samma enhet | När du använder [!DNL customer attributes] för att överföra kundprofiler till en datakälla, rekommenderar Adobe att användare delar enheter (det vill säga samma Experience Cloud-ID). Experience Cloud-id:t (ECID) finns kvar på enheten. Delningsenheter kan göra att ECID länkar flera användare till samma ECID, vilket kan ge oväntade resultat i [!DNL Target]. **Obs!** För mobilen är ECID permanent efter att mobilappen har installerats. Installera om programmet för att generera ett nytt ECID. För webben genereras ett nytt ECID när webbläsarens cookie har rensats. |
| Begränsning av överföring av frekvens per dag | Adobe rekommenderar att du bara uppdaterar [!DNL customer attributes] en gång om dagen. Du måste vänta minst 24 timmar för att överföra ytterligare en kundprofildatafil för samma uppsättning profiler. |
| ID för anpassad analys (`s.visitorID`) | Att ange ett kund-ID med `s.visitorID` är ett sätt att identifiera användare i Adobe Analytics. Integrationer där [!DNL Analytics]-data exporteras eller importeras med ID-tjänsten fungerar emellertid inte när en besökare identifieras med `s.visitorID.`<br>Detta inkluderar, men är inte begränsat till, delade målgrupper, [!DNL Analytics] för Adobe Target (A4T) och [!DNL customer attributes].<br>För dessa integreringar stöds inte inställning av ett anpassat analys-ID. |
| Begränsningar för teckenlängd i [!DNL Analytics] | När du skapar en [!DNL Analytics]-prenumeration trunkeras fältlängderna för de överförda filerna till 255. |

{style="table-layout:auto"}

## Vanliga frågor om [!DNL customer attributes] {#section_E47866EEA83348E09FE43CEC5E44C461}

| Fråga | Svar |
|--- |--- |
| Kan jag få meddelanden om överföringsstatus för [!DNL customer attributes]? | Ja. |
| Vad bör jag göra för att komma igång med [!DNL customer attributes]? | <ol><li>Få etablerat. Om du är Adobe Analytics-kund etablerar Adobe dig för [!DNL customer attributes]. Om du bara använder Adobe Target och inte har Analytics, begär du etablering för bastjänsterna genom att kontakta kundtjänst.</li> <li>Diskutera med CRM-teamet. Ta reda på vilken typ av kunddata som finns tillgängliga och som du vill använda i Analytics och i hela Experience Cloud.</li><li>Implementera bastjänster.</li></ol> |
| Hur många [!DNL customer attributes] får jag använda? | Du kan överföra hundratals `.csv`-kolumner till kundattributtjänsten. När du konfigurerar prenumerationer och väljer attribut gäller dock följande begränsningar (per rapportsvit), beroende på vilka program du äger:  <ul><li>Foundation: 0</li><li>Välj: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 totalt</li><li>Premium: 200</li><li>Adobe Target Standard: 5</li><li>Adobe Target Premium: 200</li></ul> |
| Krävs migrering till Experience Cloud ID-tjänsten? | Migreringen beror på vilka program du använder. <ul><li>Adobe Analytics: Vi rekommenderar </li><li>Adobe Target: Obligatoriskt. </li></ul><br>Med Experience Cloud ID-tjänsten får du tillgång till de senaste Experience Cloud-funktionerna, inklusive målgrupper i realtid, Adobe Target modernisering, Analytics-integrering och loggning av pulsslag. |
| Hur hör kundattributets funktionalitet ihop med Adobe Audience Manager? | Audience Manager kan ta emot data för att identifiera målgrupper, men kan inte utföra analysfunktioner som knyter attribut till historiska beteendedata. Den innehåller inte heller de funktioner för rapportering, analys och segmentering som finns i Adobe Analytics. Med [!UICONTROL Customer Attributes] kan omfattande data från olika program knytas ihop och kopplas till ett enda ID för användning i hela Experience Cloud. <br>I Adobe Target visas [!DNL customer attributes] som enskilda attribut som kan kombineras med andra regler för att skapa målgrupper. Publiker som delas med tjänsten [!UICONTROL People] är fullständiga målgrupper som inte kan ändras. |
| **(Endast Adobe Analytics)** Hur skiljer sig den här funktionen från vad som anges i Analytics Premium? | Tidigare har kunder som är intresserade av att kombinera kundattributsdata med analysdata varit starkt beroende av Data Workbench verktyg för den här funktionen. [!DNL customer attributes] visar den här funktionen för en större publik genom att tillhandahålla [!DNL customer attributes] som mått och mätvärden i Report Builder. Kunder med Analytics Standard har tillgång till [!DNL customer attributes], men med begränsade funktioner. Den fullständiga funktionaliteten är tillgänglig för kunder som har Analytics Premium. |
| **(Endast Adobe Target)** Kan jag ladda upp data i förväg för kunder som Adobe Target aldrig har sett? | Ja. När besökaren gör sin första begäran till Adobe Target hämtar systemet den befintliga informationen som Adobe har om dem från [!DNL customer attributes] och använder dessa data för målinriktning. **Obs!** Det kan ta upp till 20 minuter att hämta data från besökarens första interaktion med Adobe Target. |
| **(Endast Adobe Target)** Kan jag skapa en superpublik genom att kombinera kundattributsdata med delade målgruppsdata? | Nej. Delade målgruppsdata är en komplett målgrupp. |
| **(Endast Adobe Target)** Hur fungerar funktionen [!DNL customer attributes] jämfört med Adobe Target massprofil-API? | Massprofilens API gör att Adobe Target-profiler kan uppdateras direkt via API:t, antingen för en enskild profil eller gruppvis. Funktionen liknar [!DNL customer attributes], med följande viktiga skillnader:<ul><li>Profil-API:t är ett REST API-anrop och [!DNL customer attributes] använder FTP.</li><li>Adobe Target profil-API skickar bara data till Adobe Target i stället för till hela Experience Cloud.</li><li>[!DNL customer attributes] har ett enkelt gränssnitt för att skapa och hantera externa data.</li></ul> |
| **(Endast Adobe Target)** Utökar överföringen av data från [!DNL customer attributes] till Adobe Target Adobe Target-besökarens profillivstid? | Ja. Se [Livstid för besökarprofil](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=sv-SE) i hjälpen för Adobe Target. |
| **(Endast Adobe Target)** Kan jag rikta in mig på data som överförts i [!DNL customer attributes] omedelbart efter att besökaren har identifierats av kund-ID:t? | Ja. På serveranropet till Adobe Target, som innehåller mbox-ID:t, finns alla kundattributsdata tillgängliga. |
| **(Endast Adobe Target)** Vad representerar kolumnen **[!UICONTROL Sync Status]** för filer som överförts i kundattributskällan? | Du kan visa antalet poster som publicerats och synkroniserats av Adobe Target genom att välja ikonen Synkroniseringsstatus mot en viss attributfil. `Sync %` är ett realtidsmått som anger % av profilerna som har synkroniserats i Adobe Target.<br> **Obs!** Det kan ta upp till 24 timmar för attribut att synkronisera med Adobe Target. |
| Vad representerar mätvärdena för filöverföring i [!DNL customer attributes] Source? | Du kan kontrollera statusen för attribut som överförts till [!DNL customer attributes] med hjälp av följande mått: <ul><li>Poster: Antal poster i attributfilen.</li><li>**Nya poster:** Antal nya poster i attributfilen.</li> <li>**Uppdaterade poster:** Antal poster i [!DNL customer attributes] med uppdaterade värden i filen.</li><li>**Alla data (poster):** Totalt antal poster som har överförts till [!DNL customer attributes].</li></ul> |

{style="table-layout:auto"}
