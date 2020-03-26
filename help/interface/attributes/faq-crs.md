---
description: Vanliga frågor och bästa praxis för kundattribut i Analytics och Target.
keywords: customer attributes
seo-description: Vanliga frågor och bästa praxis för kundattribut i Analytics och Target.
seo-title: Vanliga frågor, begränsningar och bästa praxis
solution: Experience Cloud
title: Vanliga frågor, begränsningar och bästa praxis
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Vanliga frågor, begränsningar och bästa praxis

Vanliga frågor och bästa praxis för kundattribut i Analytics och Target.

## God praxis och begränsningar {#section_7F5189B3DAA84EE6865B91D2026EE05A}

Vägledning och begränsningar när kundattribut används.

| Problem | Beskrivning |
|--- |--- |
| Prenumerationsbegränsningar för kundattribut | När du uppgraderar till Analytics Premium tar det 24 timmar innan ytterligare attribut finns tillgängliga. Ett Max-fel för attributprenumeration kan visas under den här fördröjningen. |
| Flera inloggningar på samma enhet | När du använder kundattribut för att överföra kundprofiler till en datakälla, rekommenderar Adobe mot användare som delar samma enhet (det vill säga samma Experience Cloud-ID). Om du gör det kan ECID-tjänsten, som finns kvar på enheten, länka flera användare under samma Experience Cloud ID, vilket kan ge oväntade resultat [!DNL Target]. **Obs!** För mobiler är ECID permanent efter att mobilappen har installerats, och du måste installera om appen för att generera ett nytt ECID. För webben genereras ett nytt ECID när webbläsarens cookie har rensats. |
| Begränsning av överföring av frekvens per dag | Adobe rekommenderar att du bara uppdaterar kundattribut en gång om dagen. Du måste vänta minst 24 timmar för att överföra ytterligare en kundprofildatafil för samma uppsättning profiler. |
| ID för anpassad analys (`s.visitorID`) | Att ange ett kund-ID med `s.visitorID` är ett sätt att identifiera användare i Analytics. Integrationer där Analytics-data exporteras eller importeras med ID-tjänsten kommer dock inte att fungera när en besökare identifieras med `s.visitorID.`<br>Detta inkluderar, men är inte begränsat till, delade målgrupper, Analytics för Adobe Target (A4T) och kundattribut.<br>För dessa integreringar stöds inte inställning av ett anpassat analys-ID. |
| Begränsningar av teckenlängd i Analytics | När du skapar en Analytics-prenumeration trunkeras fältlängderna för de överförda filerna till 255. |

## Frågor och svar om kundattribut {#section_E47866EEA83348E09FE43CEC5E44C461}

| Fråga | Svar |
|--- |--- |
| Kan jag få meddelanden om överföringsstatus för kundattribut? | Ja. Se [Hantera meddelanden](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/organizations.html#concept_0105453AD71847B8BFCAF4A40915F157). |
| Vad bör jag göra för att komma igång med kundattribut? | <ol><li>Få etablerat. Om du är Analytics-kund etablerar Adobe dig för kundattribut. Om du bara använder Adobe Target och inte har Analytics måste du begära att få tillgång till bastjänster genom att kontakta kundtjänst.</li> <li>Diskutera med CRM-teamet. Ta reda på vilken typ av kunddata som är tillgängliga och som skulle vara intressant att använda i Analytics och i hela Experience Cloud.</li><li>Implementera bastjänster. Se [Aktivera lösningar för bastjänster](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html) för steg om hur du kan modernisera implementeringen. (Se avsnittet om synkronisering av kund-ID:n för viktig information.)</li></ol> **Obs!** Administratörens Frågor och svar för implementering av bastjänster finns [här](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/faq.html#concept_13219B4E51784577B6FF78AAA203DE91). |
| Hur många kundattribut får jag använda? | Du kan överföra hundratals `.csv` kolumner till kundattributtjänsten. När du konfigurerar prenumerationer och väljer attribut gäller dock följande begränsningar (per rapportsvit), beroende på vilka lösningar du äger:  <ul><li>Foundation: 0</li><li>Välj: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 totalt</li><li>Premium: 200</li><li>Adobe Target Standard: 5</li><li>Adobe Target Premium: 200</li></ul> |
| Krävs migrering till Experience Cloud ID Service? | Migreringen beror på vilka lösningar du använder. <ul><li>Adobe Analytics:  Rekommenderas starkt </li><li>Adobe Target: Obligatoriskt. </li></ul><br> Genom att använda ID-tjänsten förbättras möjligheterna att använda de senaste funktionerna i Experience Cloud, inklusive målgrupper i realtid, Adobe Target-modernisering, Analytics-integrering och loggning av pulsslag. <br> Mer information finns i [Aktivera lösningar för bastjänster](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html). <br>** Obs!** [Experience Cloud ID-tjänsten](https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html) är en moderniserad implementering av det som tidigare kallades _Analytics besökar ID-tjänst._ |
| Hur hänger kundattributets funktionalitet ihop med Adobe Audience Manager? | Audience Manager kan ta emot data för att identifiera målgrupper, men kan inte utföra analysfunktioner som knyter attribut till historiska beteendedata eller tillhandahåller de rapporterings-, analys- och segmenteringsfunktioner som finns i Adobe Analytics. Bastjänsten People gör att omfattande data från olika lösningar kan kopplas samman och kopplas till ett enda ID för användning i hela Experience Cloud. <br>I Adobe Target visas kundattribut som enskilda attribut som kan kombineras med andra regler för att skapa målgrupper. Målgrupper som delas i personbastjänsten är fullmålgrupper som inte kan ändras. |
| **(Endast Analytics)** Hur skiljer sig den här funktionen från vad som ingår i Analytics Premium? | Tidigare har kunder som är intresserade av att kombinera kundattributdata med analysdata i stor utsträckning förlitat sig på verktyget data workbench för den här funktionen. Kundattribut exponerar denna funktionalitet för en större publik genom att tillhandahålla kundattribut som mått och mätvärden i rapporter och analyser, ad hoc-analyser och rapportverktyg. Analytics Standard-kunder får tillgång till kundattribut, men med begränsade funktioner. Den fullständiga funktionaliteten är tillgänglig för kunder som har Analytics Premium. |
| **(Endast Adobe Target)** Kan jag ladda upp data i förväg för kunder som Adobe Target aldrig har sett? | Ja. När besökaren gör sin första förfrågan till Adobe Target hämtar systemet den befintliga informationen om dem från kundattribut och använder dessa data för målinriktning. **Obs!**  Det kan ta upp till 20 minuter att hämta data från besökarens första interaktion med Adobe Target. |
| **(Endast Adobe Target)** Kan jag skapa en supermålgrupp genom att kombinera kundattributdata med delade målgruppsdata? | Nej. Delade målgruppsdata är en komplett målgrupp. |
| **(Endast Adobe Target)** Hur fungerar kundattributsfunktionen jämfört med Adobe Target-API:t för gruppprofiler? | Massprofilens API gör att Adobe Target-profiler kan uppdateras direkt via API:t, antingen för en enskild profil eller i grupp. Funktionen liknar kundattribut, med följande viktiga skillnader:<ul><li>Profil-API är ett REST API-anrop och kundattribut använder FTP.</li><li>Adobe Target profil-API skickar bara data till Adobe Target i stället för till hela Experience Cloud.</li><li>Kundattribut är ett enkelt gränssnitt för att skapa och hantera externa data.</li></ul> |
| **(Endast Adobe Target)** förlänger Adobe Target-besökarens livslängd genom att överföra data från kundattribut till Adobe Target? | Ja. Mer information finns i [Livstid](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html) för besökarprofiler i hjälpen för Adobe Target. |
| **(Endast Adobe Target)** Kan jag rikta in mig på de data som överförs i kundattribut omedelbart efter det att besökaren har identifierats av kund-ID:t? | Ja. På serveranropet till Adobe Target, som innehåller mbox-ID:t, kommer alla kundattributsdata att vara tillgängliga. |
| **(Endast Adobe Target)** Vad representerar kolumnen **[!UICONTROL Synkroniseringsstatus]** för filer som överförs i Kundattributkälla? | Du kan visa antalet poster som publiceras och synkroniseras av Adobe Target genom att klicka på ikonen Synkronisera status mot en viss attributfil. `Sync %` är ett realtidsmått som anger procentandelen profiler som har synkroniserats i Adobe Target.<br> **Obs!** Det kan ta upp till 24 timmar för attribut att synkronisera med Adobe Target. |
| Vad representerar mätvärdena för filöverföring i kundattributskällan? | Du kan kontrollera statusen för attribut som överförts till kundattribut med hjälp av följande mått: <ul><li>Poster:  Antal poster i attributfilen.</li><li>**Nya poster:** Antal nya poster i attributfilen.</li> <li>**Uppdaterade poster:** Antal poster i som redan finns i kundattribut med uppdaterade värden i filen.</li><li>**Alla data (poster):** Totalt antal poster som har överförts till kundattribut.</li></ul> |
