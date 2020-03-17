---
description: Administratörer kan lära sig mer om kraven och vad de kan förvänta sig när de uppgraderar till Analytics Premium, och var de kan få hjälp som Experience Cloud-administratör.
keywords: upgrading
seo-description: Administratörer kan lära sig mer om kraven och vad de kan förvänta sig när de uppgraderar till Analytics Premium, och var de kan få hjälp som Experience Cloud-administratör.
seo-title: Uppgradera till Analytics Premium och Experience Cloud
solution: Experience Cloud
title: Uppgradera till Analytics Premium och Experience Cloud
topic: Premium
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
translation-type: tm+mt
source-git-commit: ae97db27349940a8df7ee2ba6678683f57585678

---


# Uppgradera till Analytics Premium och Experience Cloud

Administratörer kan lära sig mer om kraven och vad de kan förvänta sig när de uppgraderar till Analytics Premium, och var de kan få hjälp som Experience Cloud-administratör.

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

Uppgradera till Adobe Analytics Premium och få alla funktioner och produkter som finns i Analytics Standard, inklusive Data Warehouse, Ad Hoc Analysis, Report Builder och Data Connectors. (Dessa produkter såldes separat till kunder med punktlösningen SiteCatalyst.)

Med Analytics Premium får ni:

* Tillgång till 250 konverteringsvariabler (eVars)
* [Mobilappsanalys](https://docs.adobe.com/content/help/en/mobile-services/using/home.html)
* Data Workbench (visuell datafråga); regelbaserad attribuering, flerkanalsanalys)

>[!NOTE]
>
>Ingen migrering är nödvändig vid uppgradering, men det finns några saker att tänka på:
>
>* Variablerna 76-250 (SiteCatalyst) och 100-250 (Standard) visas i Admin Tools, men är inte aktiverade.>
>* Contribute Analysis aktiveras av Adobe. Platsen ändras inte (den är fortfarande tillgänglig på sidan Anomalidentifiering), men nu börjar analysen av alla datapunkter automatiskt.>


## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

I Analytics Premium Complete får du alla funktioner i [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), plus följande uppgraderingar:

| Produkt | Uppgraderingar |
|--- |--- |
| Rapporter och analyser | <ul><li>[Bidragsanalys](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html)</li><li>[Kundattribut](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (upp till 200)</li></ul> |
| Data Workbench | <ul><li>Algoritmisk attribuering</li><li>Fördefinierade arbetsytor</li></ul> |
| Analytics Platform | [Live-ström](https://helpx.adobe.com/analytics/kb/getting-started-with-livestream-api.html) (rådata, instrumentpaneler, utlösare) |

## Prediktiv intelligens {#section_B407932C07A7476F83FB0275C3FB63DC}

Uppgradera till Predictive Intelligence så får du [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) plus:

| Produkt | Uppgraderingar |
|---|---|
| Rapporter och analyser | [Bidragsanalys](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Data Workbench | Färdiga arbetsytor för målgruppskvalifikationer och prediktiv marknadsföring. |
| Analytics Platform | Live Stream (instrumentpaneler och utlösare) |

## Kund 360 {#section_3B2AC245388248688067DC9A48957AFB}

Uppgradera till Customer 360 med [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) plus:

| Produkt | Uppgraderingar |
|--- |--- |
| [Kundattribut](../attributes/attributes.md) | Kundattribut (analys och segmentdelning) |
| Data Workbench | <ul><li>Härledda kundattribut</li><li>Färdiga arbetsytor för målgruppsidentifiering</li></ul> |
| Analytics Platform | [Kundattribut](../attributes/attributes.md) |

## Avancerad attribuering {#section_9E4986A8389946CCAA7D003268343296}

Avancerad attribuering ger tillgång till [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), plus algoritmisk attribuering i Data Workbench (25 % serveranropsvolym).

## Krav för Data Workbench {#section_D959CA68D6DB42C38707F8E0CA3654CC}

De användare som stöds kan begära att alla klientlicenser uppdateras för att återspegla Premium genom att skicka ett e-postmeddelande `dwb@adobe.com`. Detta aktiverar funktioner som algoritmisk attribuering.

TechOps granskar ditt avtalsåtagande och fastställer rätt hanterad infrastruktur, ökar eller minskar kapaciteten, och sedan koordinerar de med dig via kontohanteraren eller konsulten för att driftsätta eventuella ändringar.

Alla program som körs lokalt måste inaktiveras. Detta inkluderar sensorer, vilket innebär att ni måste säkerställa korrekt spårning med Analytics-taggar.

## Experience Cloud - administrera användare och produkter {#section_6471C54454024301B2E0B687F79F6738}

Användare av Analytics Standard och Premium kan få tillgång till tjänsterna i Experience Cloud och Core, förutsatt att du har följt den modernisering av implementeringen som beskrivs i [Komma igång - aktivera lösningar för bastjänsterna](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C). (Denna process hjälper er att modernisera implementeringen och gör att ni kan bli administratör i Experience Cloud.)

När du har gått med i Experience Cloud kan du logga in via Experience Cloud på [!DNL experiencecloud.adobe.com] och börja använda bastjänsterna (inklusive kundattribut, målgrupper och mobilappsanalyser).

### Administrera användare och grupper

Användarhantering utförs i [Adobe Admin Console](https://helpx.adobe.com/enterprise/help/aedash.html) (produktlänk).

Du kan skapa en 1:1-karta mellan en grupp som skapats i Adobe Admin Console och en lösningsgrupp (till exempel Adobe Analytics). Därefter kommer en ny användare som läggs till i den mappade Admin Console-gruppen att automatiskt skapa ett Analytics-lösningskonto som länkas till användarens Adobe ID. (Befintliga användare måste manuellt länka sina autentiseringsuppgifter för lösningskonton för att få tillgång till lösningar via Experience Cloud-inloggningen.)

>[!NOTE]
>
>Du kan mappa flera lösningsgrupper till en Admin Console-grupp. Adobe rekommenderar dock 1:1-mappning. Genom att mappa grupperna i förväg kan du bjuda in, skapa, ge behörighet och lägga till flera användare genom att överföra en CSV-fil.
