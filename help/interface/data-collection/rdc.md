---
title: Regional datainsamling
description: Information om regional datainsamling
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
source-git-commit: 2691f0dc91e48a8f817467e334d9028f2e506e70
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Regional datainsamling

Adobe Experience Cloud använder regional datainsamling (RDC) så att interaktionen mellan besökarna och Adobe sker så nära besökarna som möjligt. Data som samlas in lokalt på en edge-plats vidarebefordras på ett säkert sätt till en central plats för bearbetning. När uppgifterna har bearbetats är de tillgängliga för Adobe Experience Cloud produkter och tjänster.

Arbetsflödet för regional datainsamling ger flera fördelar:

* **Prestanda**: Med RDC ansluter besökarna till den närmaste edge-webbplatsen. Denna optimering ger den snabbaste svarstiden, vilket ger mer exakt spårning och snabbare laddningstider.
* **Redundans**: Om kommunikationen mellan en edge-plats och en central plats störs sparar Adobe infrastruktur data lokalt och vidarebefordrar den sedan till kärnplatsen när kommunikationen återställs. Adobe kan även dirigera trafik till andra edge-sajter om en viss plats får avbrott.

Följande platser (kan ändras) ingår för närvarande i RDC:

## Insamling av data från första part

| Typ av domänkontrollant | Datainsamlingscentral |
| --- | --- |
| Global (standard) | Oregon, Virginia, Irland, Paris, Mumbai, Singapore, Tokyo, Sydney |
| Global + Kina* | Kina*, Oregon, Virginia, Irland, Paris, Mumbai, Singapore, Tokyo, Sydney |
| Endast Amerika | Oregon, Virginia |
| Endast Europa | Irland, Paris |
| Endast Asien och Stillahavsområdet | Mumbai, Singapore, Tokyo, Sydney |
| Endast Kina* | Peking |

{style="table-layout:auto"}

_*China RDC kräver tilläggspaketet för Kina-prestandaoptimering och gäller endast Adobe Analytics som använder datainsamling från AppMeasurement. Andra Experience Cloud-tjänster och Web SDK-datainsamling stöds inte. Kontakta kontoteamet på Adobe om du vill veta mer om tillägget Prestandaoptimering för Kina._

## Datainsamling från tredje part

Insamling av data från tredje part inkluderar cookie-domäner som inte matchar webbplatsens domän. Exempel: `adobedc.net`, `omtrdc.net`och `2o7.net`.

| Typ av domänkontrollant | Datainsamlingscentral |
| --- | --- |
| Standard | Oregon, Virginia, Irland, Paris, Mumbai, Singapore, Tokyo, Sydney, Kina* |

{style="table-layout:auto"}
