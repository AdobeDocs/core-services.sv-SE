---
description: Frågor och svar om kundattribut i Adobe Experience Cloud, Adobe Analytics och Adobe Target.
keywords: Kundattribut
solution: Experience Cloud
title: 'Få svar på vanliga frågor om kundattribut '
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: Kundattribut
topic: Administrering
role: Administrator
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: eef7326f9f04f68eefb60b5d9fd4cc91cbe52119
workflow-type: tm+mt
source-wordcount: '1152'
ht-degree: 1%

---

# Vanliga frågor och svar om [!UICONTROL Customer Attributes]

Vanliga frågor och metodtips för [!UICONTROL Customer Attributes] i Adobe Analytics och Adobe Target.

## Bästa praxis och begränsningar {#section_7F5189B3DAA84EE6865B91D2026EE05A}

Vägledning och begränsningar när du använder [!UICONTROL Customer Attributes].

| Problem | Beskrivning |
|--- |--- |
| [!UICONTROL Customer attribute] prenumerationsbegränsningar | När du uppgraderar till Analytics Premium tar det 24 timmar innan fler attribut finns tillgängliga. Ett [!UICONTROL Attribute Subscription Max]-fel kan ha uppstått under fördröjningen. |
| Flera inloggningar på samma enhet | När du använder [!UICONTROL Customer Attributes] för att överföra kundprofiler till en datakälla rekommenderar Adobe mot användare som delar enheter (vilket innebär samma Experience Cloud-ID). Experience Cloud ID (ECID) finns kvar på enheten. Delningsenheter kan göra att ECID länkar flera användare till samma ECID, vilket kan ge oväntade resultat i [!DNL Target]. **Obs!** För mobiler är ECID permanent efter att mobilappen har installerats. Installera om programmet för att generera ett nytt ECID. För webben genereras ett nytt ECID när webbläsarens cookie har rensats. |
| Begränsning av överföring av frekvens per dag | Adobe rekommenderar att du bara uppdaterar kundattribut en gång om dagen. Du måste vänta minst 24 timmar för att överföra ytterligare en kundprofildatafil för samma uppsättning profiler. |
| ID för anpassad analys (`s.visitorID`) | Att ange ett kund-ID med `s.visitorID` är ett sätt att identifiera användare i Analytics. Integrationer där [!DNL Analytics]-data exporteras eller importeras med ID-tjänsten fungerar emellertid inte när en besökare identifieras med `s.visitorID.`<br>Detta inkluderar, men är inte begränsat till, delade målgrupper, [!DNL Analytics] för Adobe Target (A4T) och [!UICONTROL Customer Attributes].<br>För dessa integreringar stöds inte inställning av ett anpassat analys-ID. |
| Begränsningar av teckenlängd i [!DNL Analytics] | När du skapar en [!DNL Analytics]-prenumeration trunkeras fältlängderna för de överförda filerna till 255. |

## Frågor och svar om kundattribut {#section_E47866EEA83348E09FE43CEC5E44C461}

| Fråga | Svar |
|--- |--- |
| Kan jag få meddelanden om överföringsstatus för kundattribut? | Ja. |
| Vad ska jag göra för att komma igång med kundattribut? | <ol><li>Få etablerat. Om du är Analytics-kund tilldelar Adobe dig kundattribut. Om du bara använder Adobe Target och inte har Analytics, begär du etablering för bastjänsterna genom att kontakta Kundtjänst.</li> <li>Diskutera med CRM-teamet. Ta reda på vilken typ av kunddata som finns tillgängliga och som du vill använda i Analytics och i hela Experience Cloud.</li><li>Implementera bastjänster. Se [Aktivera lösningar för bastjänster](core-services.md) för steg om hur du moderniserar implementeringen. (Se avsnittet om synkronisering av kund-ID:n för viktig information.)</li></ol> **Obs!** Administratörens Frågor och svar för implementering av bastjänster finns  [här](faq.md). |
| Hur många kundattribut får jag använda? | Du kan överföra hundratals `.csv`-kolumner till tjänsten Kundattribut. När du konfigurerar prenumerationer och väljer attribut gäller dock följande begränsningar (per rapportsvit), beroende på vilka lösningar du äger:  <ul><li>Foundation: 0</li><li>Välj: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 totalt</li><li>Premium: 200</li><li>Adobe Target Standard: 5</li><li>Adobe Target Premium: 200</li></ul> |
| Krävs migrering till Experience Cloud ID-tjänsten? | Migreringen beror på vilka lösningar du använder. <ul><li>Adobe Analytics: Rekommenderas starkt </li><li>Adobe Target: Obligatoriskt. </li></ul><br>Med tjänsten Experience Cloud ID får du tillgång till de senaste Experience Cloud-funktionerna, inklusive målgrupper i realtid, Adobe Target modernisering, Analytics-integrering och loggning av pulsslag. <br> Mer information finns i  [Aktivera lösningar för bastjänster](core-services.md). <br>**Obs!** Tjänsten  [Experience Cloud ID ](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en) är en moderniserad implementering av det som tidigare kallades  _besökar-ID för Analytics._ |
| Hur hör kundattributsfunktionen ihop med Adobe Audience Manager? | Även om Audience Manager kan ta emot data för att utföra målgruppsidentifiering kan det inte utföra analysfunktioner som kopplar attribut till historiska beteendedata. Den innehåller inte heller de funktioner för rapportering, analys och segmentering som finns i Adobe Analytics. [!UICONTROL People] gör att omfattande data från olika lösningar kan knytas ihop och kopplas till ett enda ID för användning i hela Experience Cloud. <br>I Adobe Target visas kundattribut som enskilda attribut som kan kombineras med andra regler för att skapa målgrupper. Målgrupper som delas med [!UICONTROL People]-tjänsten är fullständiga målgrupper som inte kan ändras. |
| **(Endast Analytics)** Hur skiljer sig den här funktionen från vad som ingår i Analytics Premium? | Tidigare har kunder som är intresserade av att kombinera kundattributsdata med analysdata varit starkt beroende av Datan Workbench för den här funktionen. [!UICONTROL Customer Attributes] ger en större publik tillgång till denna funktionalitet genom att tillhandahålla kundattribut som mått och mätvärden i rapporter och analyser, Ad Hoc Analysis och rapportverktyg. Kunder med Analytics Standard har tillgång till kundattribut, men med begränsade funktioner. Den fullständiga funktionaliteten är tillgänglig för kunder som har Analytics Premium. |
| **(Endast Adobe Target)** Kan jag förladda eller ladda upp data till kunder som Adobe Target aldrig har sett? | Ja. När besökaren gör sin första förfrågan till Adobe Target hämtar systemet den befintliga informationen som Adobe har om dem från kundattribut och använder dessa data för målinriktning. **Obs!**  Det kan ta upp till 20 minuter att hämta data från besökarens första interaktion med Adobe Target. |
| **(Endast Adobe Target)** Kan jag skapa en superpublik genom att kombinera kundattributsdata med delade målgruppsdata? | Nej. Delade målgruppsdata är en komplett målgrupp. |
| **(Endast Adobe Target)** Hur fungerar  [!UICONTROL Customer Attributes] funktionerna jämfört med Adobe Target massprofils-API? | Massprofilens API gör att Adobe Target-profiler kan uppdateras direkt via API:t, antingen för en enskild profil eller gruppvis. Funktionen liknar kundattribut, med följande viktiga skillnader:<ul><li>Profil-API är ett REST API-anrop och kundattribut använder FTP.</li><li>Adobe Target profil-API skickar bara data till Adobe Target i stället för till hela Experience Cloud.</li><li>Kundattribut är ett enkelt gränssnitt för att skapa och hantera externa data.</li></ul> |
| **(Endast Adobe Target)** förlänger överföringen av data från kundattribut till Adobe Target Adobe Target-besökarens profillivslängd? | Ja. Se [Livstid för besöksprofil](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=en) i hjälpen för Adobe Target. |
| **(Endast Adobe Target)** Kan jag rikta in mig på de data som överförs i kundattribut omedelbart efter det att besökaren har identifierats av kund-ID:t? | Ja. På serveranropet till Adobe Target, som innehåller mbox-ID:t, finns alla kundattributsdata tillgängliga. |
| **(Endast Adobe Target)** Vad representerar  **[!UICONTROL Sync Status]** kolumnen för filer som överförs i källan för kundattribut? | Du kan visa antalet poster som publicerats och synkroniserats av Adobe Target genom att klicka på ikonen Synkroniseringsstatus mot en viss attributfil. `Sync %` är ett realtidsmått som anger procentandelen profiler som har synkroniserats i Adobe Target.<br> **Obs!** Det kan ta upp till 24 timmar innan attribut synkroniseras med Adobe Target. |
| Vad representerar mätvärdena för filöverföring i kundattributskällan? | Du kan kontrollera statusen för attribut som överförts till kundattribut med hjälp av följande mått: <ul><li>Poster:  Antal poster i attributfilen.</li><li>**Nya poster:** Antal nya poster i attributfilen.</li> <li>**Uppdaterade poster:** Antal poster i kundattribut med uppdaterade värden i filen.</li><li>**Alla data (poster):** Totalt antal poster som har överförts till kundattribut.</li></ul> |