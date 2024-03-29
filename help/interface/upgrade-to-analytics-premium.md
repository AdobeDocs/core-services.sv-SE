---
description: Läs mer om kraven och vad du kan förvänta dig när du uppgraderar till Analytics Premium.
solution: Experience Cloud
title: Uppgradera till Analytics Premium och Experience Cloud
topic: Administration
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
feature: Admin Console
role: Admin
level: Experienced
exl-id: 746d396d-9629-42db-8c55-07d2d24e4611
source-git-commit: eb2ad8a8255915be47b6002a78cc810b522170d2
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 3%

---

# Uppgradera till Analytics Premium och Experience Cloud

Administratörer kan lära sig mer om kraven och vad de kan förvänta sig när de uppgraderar till Analytics Premium, och var de kan få hjälp som Experience Cloud-administratör.

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

Uppgradera till Adobe Analytics Premium och få alla funktioner och produkter som finns i Analytics Standard, inklusive Data warehouse, Ad Hoc Analysis, Report Builder och Data Connectors.

Med Analytics Premium får ni:

* Tillgång till 250 konverteringsvariabler (eVars)
* [Mobilappsanalys](https://experienceleague.adobe.com/docs/mobile-services/using/home.html?lang=en)
* Data Workbench (Visual data query; regelbaserad attribuering, flerkanalsanalys)

>[!NOTE]
>
>Ingen migrering är nödvändig vid uppgradering, men det finns några saker att tänka på:
>
>* Variablerna 76-250 och 100-250 (Standard) visas i Admin Tools, men är inte aktiverade.
>* Bidragsanalys aktiveras av Adobe. Platsen ändras inte (den är fortfarande tillgänglig på Anomaly Detection-sidan), men den börjar automatiskt analysera alla datapunkter.


## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

I Analytics Premium Complete får du alla funktionerna i [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), plus följande uppgraderingar:

| Produkt | Uppgraderingar |
|--- |--- |
| Rapporter och analyser | <ul><li>[Bidragsanalys](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=en)</li><li>[Kundattribut](attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (Upp till 200)</li></ul> |
| Data Workbench | <ul><li>Algoritmisk attribuering</li><li>Fördefinierade arbetsytor</li></ul> |
| Analytics Platform | [Live Stream](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/index.md) (rådata, instrumentpaneler, utlösare) |

{style=&quot;table-layout:auto&quot;}

## Prediktiv intelligens {#section_B407932C07A7476F83FB0275C3FB63DC}

Uppgradera till Predictive Intelligence [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) plus:

| Produkt | Uppgraderingar |
|---|---|
| Rapporter och analyser | [Bidragsanalys](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=en) |
| Data Workbench | Färdiga arbetsytor för målgruppskvalifikationer och prediktiv marknadsföring. |
| Analytics Platform | Live Stream (instrumentpaneler och utlösare) |

{style=&quot;table-layout:auto&quot;}

## Kund 360 {#section_3B2AC245388248688067DC9A48957AFB}

Uppgradera till Customer 360-erbjudanden [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) plus:

| Produkt | Uppgraderingar |
|--- |--- |
| [Kundattribut](attributes.md) | Kundattribut (analys och segmentdelning) |
| Data Workbench | <ul><li>Härledda kundattribut</li><li>Färdiga arbetsytor för målgruppsidentifiering</li></ul> |
| Analytics Platform | [Kundattribut](attributes.md) |

{style=&quot;table-layout:auto&quot;}

## Avancerad attribuering {#section_9E4986A8389946CCAA7D003268343296}

Avancerad attribuering ger åtkomst till [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), plus algoritmisk attribuering i Data Workbench (25 % serveranropsvolym).

## Krav på Data Workbench {#section_D959CA68D6DB42C38707F8E0CA3654CC}

De användare som stöds kan begära att alla klientlicenser uppdateras för att återspegla Premium genom att skicka e-post `dwb@adobe.com`. Den här uppdateringen aktiverar funktioner som algoritmisk attribuering.

TechOps granskar ditt avtalsåtagande och fastställer rätt hanterad infrastruktur, ökar eller minskar kapaciteten, och koordinerar sedan med dig, via kontohanteraren eller konsulten, för att driftsätta eventuella ändringar.

Alla program som körs lokalt måste inaktiveras. Programvaran innehåller sensorer, vilket innebär att du måste säkerställa korrekt spårning genom [!DNL Analytics] -taggar.

## Experience Cloud - Administrera användare och produkter {#section_6471C54454024301B2E0B687F79F6738}

Experience Cloud och bastjänster är tillgängliga för användare av Analytics Standard och Premium om du har följt den implementeringsmodernisering som beskrivs i [Komma igång - aktivera dina program för bastjänster](core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C). (Denna process hjälper dig att modernisera implementeringen och gör att du kan bli administratör i Experience Cloud.)

När du har gått med i Experience Cloud kan du logga in via Experience Cloud på [!DNL experience.adobe.com] och börja använda bastjänster (inklusive kundattribut, målgrupper och mobilappsanalyser).

### Administrera användare och grupper

Användarhantering utförs i [Adobe Admin Console](https://helpx.adobe.com/se/enterprise/using/admin-console.html) (produktlänk).

Du kan skapa en 1:1-karta mellan en grupp som skapats i Adobe Admin Console och en lösningsgrupp (till exempel Adobe Analytics). Därefter har en ny användare som läggs till i den mappade Admin Console-gruppen ett Analytics-programkonto som automatiskt skapas och länkas till användarens Adobe ID. (Befintliga användare måste manuellt länka sina inloggningsuppgifter för programkonton för att få tillgång till program via inloggningen till Experience Cloud.)

>[!NOTE]
>
>Du kan mappa flera programgrupper till en Admin Console-grupp. Adobe rekommenderar dock 1:1-mappning. Genom att mappa grupperna i förväg kan du bjuda in, skapa, ge behörighet och lägga till flera användare genom att överföra en CSV-fil.
