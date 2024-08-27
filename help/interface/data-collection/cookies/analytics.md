---
description: Läs mer om Adobe Analytics cookies i Adobe Experience Cloud.
solution: Experience Cloud,Analytics,Target
title: Adobe Analytics Cookies
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bc8ce894-f98c-4475-8a07-d74ae76f7451
source-git-commit: 2a80851c0a7d4ef7dbcc2565177b239f3e063164
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Adobe Analytics cookies

Adobe Analytics använder cookies för att skilja på begäranden från olika webbläsare och för att lagra användbar information som ett program kan använda senare. De kan även användas för att koppla webbinformation till kundposter.

Analytics använder cookies för att definiera nya besökare anonymt, hjälpa till att analysera klickströmsdata och spåra historik på webbplatsen, som svar på särskilda kampanjer eller säljcykelns längd.

| Kaknamn | Förfallotid | Storlek | Plats | Beskrivning |
| --- | --- | --- | --- | --- |
| **`s_ecid`** | 2 år | 45 byte | Förste part | Lagrar Experience Cloud-ID (ECID) eller MID. Ange med HTTP-svar. MID lagras i formatet `s_ecid=MCMID`. Ange efter att klienten har angett AMCV-cookien. Den tillåter beständig första parts-ID-spårning och används som referens-ID om AMCV-cookien upphör att gälla. Denna cookie gäller inte för cookie-implementeringar från tredje part. `SameSite` är inställt på&quot;Lax&quot;. |
| **`s_cc`** | Session | 4 byte | Förste part | Anger om cookies är aktiverade. Uppsatt av JavaScript. |
| **`s_sq`** | Session | 100-200 byte | Förste part | Används av Activity Map. Den innehåller information om den föregående länken som besökaren klickade på. Uppsatt av JavaScript. |
| **`s_vi`** | 2 år | 44 byte | Första part eller `*.omtrdc.net` (tredje part) | Lagrar ett unikt besökar-ID och tidsstämpel. Ange med HTTP-svar. Varje besökar-ID är associerat med en besökarprofil på Adobe-servrar. Besökarprofiler tas bort efter 1 års inaktivitet, oavsett om en cookie-fil för besöks-ID har gått ut eller inte. Flaggan `Secure` anges när `SameSite` är Ingen och anslutningen är HTTPS. `SameSite` är Lax som standard för cookies från första part. `SameSite` är ingen när cookies från tredje part används, till exempel på `omtrdc.net` eller `2o7.net`. Ange `SameSite` som Ingen när du använder en enda CNAME för att spåra flera domäner eller egenskaper. |
| **`s_fid`** | 2 år | 33 byte | Förste part | Lagrar unikt besökar-ID och tidsstämpel för reserv. Anges av JavaScript om standardcookien `s_vi` inte kan anges på grund av begränsningar för cookies från tredje part. Används inte för cookie-implementeringar från första part. |
| **`s_ac`** | Omedelbar | 1 byte | Förste part | Hjälper till att fastställa rätt domän att ange AppMeasurementets cookies. Innehåller det statiska värdet `"1"`. När denna cookie är inställd tas den bort omedelbart. |

{style="table-layout:auto"}

## Cookies angivna av plugin-program

Vissa implementeringar använder plugin-program, som är kodfragment som ger ytterligare funktioner för Analytics. Dessa plugin-program kan ange cookies som inte finns med i listan ovan. Se [Översikt över plugin-program för analys](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/plugins/impl-plugins) för en lista över tillgängliga plugin-program och vilka cookies de anger.
