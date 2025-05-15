---
title: IP-adresser som används av Experience Cloud
description: Om brandväggen blockerar IP-adresser som kommer från Adobe använder du den här listan för att uppdatera brandväggsinställningarna.
exl-id: 1fca8d3b-ae8b-4095-96ef-d165f912b4c6
source-git-commit: 92f041f11cfa33c2e08e90c45e6fa46729447ac5
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 1%

---

# IP-adresser som används av Experience Cloud

Vissa brandväggskonfigurationer blockerar IP-adresser som kommer från Adobe datainsamlingsservrar eller servrar som är ansvariga för dataåtkomst. Du kan använda den här listan med intervall för att ändra organisationens brandväggsinställningar så att åtkomst tillåts och data skickas inifrån organisationen. Den här sidan innehåller både inkommande och utgående system (till exempel datainsamling) (till exempel dataflöden i Adobe Analytics) som används i Adobe.

>[!IMPORTANT]
>
>Även om Adobe gör sitt bästa för att hålla det här dokumentet aktuellt kan det inte garantera att listan med IP-intervall är densamma. Möjliga förändringar är bland annat tillväxt och expansion av verksamheten, ett Internetregister kräver ändringar av Adobe IP-adressutrymme eller att en Internetleverantör slutar fungera.

Förutom de IP-adressblock som anges nedan har enskilda Adobe Experience Cloud-produkter sina egna IP-adresser som de använder:

* [Adobe Analytics](https://experienceleague.adobe.com/sv/docs/analytics/technotes/ip-addresses)
* [Customer Journey Analytics](https://experienceleague.adobe.com/sv/docs/analytics-platform/using/technotes/ip-addresses)
* [Marketo Engage](https://experienceleague.adobe.com/sv/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo#step-allowlist-marketo-ips)

## Alla Adobe IP-adressblock

Följande tabell omfattar alla IP-adresser som ägs av Adobe. Tabellen innehåller alla Adobe personalkontor och datacenter som Adobe driver globalt. Det omfattar inte tjänster som lagras på offentliga moln.

| IP-block (CIDR-notering) |
| --- |
| `63.140.32.0/19` |
| `66.117.16.0/20` |
| `66.235.128.0/19` |
| `130.248.0.0/16` |
| `172.82.192.0/18` |
| `185.34.188.0/22` |
| `192.243.240.0/22` |

{style="table-layout:auto"}

## Adobe Experience Cloud datainsamling och IP-adressblock för FTP

Om din organisation föredrar att tillåta specifika IP-adressintervall kan du referera till följande tabell. Den innehåller följande uppgifter:

* Datainsamlingsservrar för alla Experience Cloud-produkter
* FTP-servrar för alla Experience Cloud-produkter

Alla IP-intervall i det här avsnittet ingår i tabellen ovan.

| Plats | IP-intervall (CIDR-notation) |
| --- | --- |
| Australien | `63.140.55.0/24` |
| Australien | `63.140.56.0/23` |
| Kalifornien | `63.140.32.0/23` |
| Kalifornien | `63.140.34.0/24` |
| Frankrike | `63.140.62.0/23` |
| Indien | `66.117.22.0/23` |
| Japan | `130.248.169.0/23` |
| Japan | `63.140.50.0/23` |
| Japan | `66.117.31.0/24` |
| London | `66.235.156.0/24` |
| London | `185.34.188.0/22` |
| London | `130.248.152.0/22` |
| London | `130.248.244.0/23` |
| Ohio | `66.117.20.0/24` |
| Oregon | `66.235.132.0/22` |
| Oregon | `130.248.130.0/23` |
| Oregon | `130.248.150.0/24` |
| Oregon | `130.248.160.0/21` |
| Oregon | `192.243.242.0/24` |
| Singapore | `130.248.170.0/23` |
| Singapore | `130.248.240.0/24` |
| Singapore | `63.140.44.0/22` |
| Singapore | `63.140.48.0/23` |
| Singapore | `66.117.30.0/24` |
| Singapore | `172.82.240.8/29` |
| Singapore | `172.82.240.88/29` |
| Virginia | `63.140.38.0/23` |
| Virginia | `63.140.54.0/24` |
| Virginia | `67.202.5.244` |

{style="table-layout:auto"}

Adobe Experience Cloud har också stöd för IPv6 med begränsad kapacitet. Dessa IP-block har liknande datainsamlingssyften som IPv4-motsvarigheter ovan, men inte FTP.

| Plats | Värd |
| --- | --- |
| Australien | `2406:da1c:406:1a00::/56` |
| Australien | `2406:da1c:ce5:b400::/56` |
| Kalifornien | `2600:1f1c:366:d900::/56` |
| Frankrike | `2a05:d012:706:d000::/56` |
| Indien | `2406:da1a:f34:6a00::/56` |
| Irland | `2a05:d018:309:600::/56` |
| Japan | `2406:da14:b07:ab00::/56` |
| Ohio | `2600:1f16:130f:7d00::/56` |
| Oregon | `2600:1f14:1eb:7d00::/56` |
| Oregon | `2600:1f14:9d3:2b00::/56` |
| Singapore | `2406:da18:6e8:1e00::/56` |
| Virginia | `2600:1f18:1a20:e800::/56` |
| Virginia | `2600:1f18:4fd:6000::/56` |
| Virginia | `2600:1f18:b00:e100::/56` |
| Virginia | `2600:1f18:d1f:bd00::/56` |

>[!TIP]
>
>FTP-anslutningar för Adobe Analytics exportfunktioner (inklusive Data Warehouse och dataflöden) kommer endast från IPv4-adresser i London, Oregon och Singapore.
