---
description: Läs om Adobe Analytics cookies i Adobe Experience Cloud.
keywords: cookies;sekretess
solution: Experience Cloud,Analytics,Target
title: 'Analytics-cookies '
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookies
topic: Administrering
role: Administratör
level: Erfaren
translation-type: tm+mt
source-git-commit: 61d60273e933c637dfe4400da78257e1c80015b3
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 3%

---


# Analytiska cookies{#analytics-cookies}

Adobe Analytics använder cookies för att skilja på begäranden från olika webbläsare och för att lagra användbar information som ett program kan använda senare. De kan också användas för att koppla webbinformation till kundposter.

Analytics använder i synnerhet cookies för att anonymt definiera nya besökare, hjälpa till att analysera klickströmsdata och spåra historik på webbplatsen, som respons på särskilda kampanjer eller säljcykelns längd.

* [Cookie-namn: s_ecid](../cookies/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Cookie-namn: AMCV_###@AdobeOrg](../cookies/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [Cookie-namn: s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie-namn: s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie-namn: s_sq](../cookies/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [Cookie-namn: s_vi](../cookies/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Cookie-namn: s_fd](../cookies/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [Cookies angivna av plugin-program](../cookies/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

Mer information finns i Analytics-hjälpen om [cookies från första part](/help/interface/cookies/cookies-first-party.md).

## Cookie-namn: s_ecid {#section-32fd753c3fa54452acd62b021434919a}

| Attribut | Beskrivning |
|--- |--- |
| Information lagrad | Innehåller en kopia av Experience Cloud ID (ECID) eller MID. MID lagras i ett nyckelvärdepar som följer syntaxen s_ecid=MCMID | `<ECID>` |
| Förfaller | 2 år |
| Användning | Denna cookie anges av kundens domän efter att AMCV-cookien har angetts av klienten. Syftet med denna cookie är att tillåta beständig ID-spårning i parttillståndet 1^st^ och används som referens-ID om AMCV-cookien har upphört att gälla. Mer information finns i AMCV-cookie här. |
| Plats | Endast CNAME-kunder. Gäller inte för tredjepartsscenarier. Cookie lagras på din domän, samma domän som används av CNAME och din bildförfrågan från Analytics. |
| Storlek | 45 byte |

## Cookie-namn: s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| Attribut | Beskrivning |
|--- |--- |
| Information lagrad | Denna cookie ställs in och läses av JavaScript-koden för att avgöra om cookies är aktiverade (anges helt enkelt till &quot;Sant&quot;) |
| Förfaller | Denna cookie är en sessionscookie som upphör när webbläsaren stängs |
| Användning | Endast en cookie för alla konton |
| Plats | Denna cookie lagras i sidans domän |
| Storlek | 4 byte |

## Cookie-namn: s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| Attribut | Beskrivning |
|--- |--- |
| Information lagrad | Denna cookie ställs in och läses av JavaScript-koden när funktionaliteten ClickMap eller Activity Map är aktiverad. den innehåller information om den föregående länken som användaren klickade på |
| Förfaller | Denna cookie är en sessionscookie som upphör när webbläsaren stängs |
| Användning | Endast en cookie för alla konton |
| Plats | Denna cookie lagras i sidans domän |
| Storlek | Varierar beroende på sidans URL-storlek, men vanligtvis 100-200 byte |

## Cookie-namn: s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

| Attribut | Beskrivning |
|--- |--- |
| Information lagrad | Unik stämpel för besökares ID-tid/datum |
| Förfaller | 2 år |
| Användning | Denna cookie används för att identifiera en unik besökare |
| Plats | Denna cookie lagras i domänen för bildbegäran - vanligtvis en kundspecifik underdomän i 2o7.net eller omtrdc.net om du använder cookies från tredje part eller om din domän använder cookies från första part. |
| Storlek | 44 byte |

>[!NOTE]
>
>Varje besökar-ID för Analytics är kopplat till en besökarprofil på Adobe-servrar. Besökarprofiler tas bort efter 1 års inaktivitet, oavsett om en cookie-fil för besöks-ID har gått ut eller inte.

## Cookie-namn: s_fd {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| Attribut | Beskrivning |
|--- |--- |
| Information lagrad | ID-tidsstämpel för reservens unika besökares ID |
| Förfaller | 2 år |
| Användning | Den här cookien används för att identifiera en unik besökare om standardcookien `s_vi` inte är tillgänglig på grund av cookie-begränsningar från tredje part. Används inte för implementeringar som använder cookies från första part. |
| Plats | Denna cookie lagras på din domän som en cookie från en annan leverantör. |
| Storlek | 33 byte |

## Cookie-flaggor

I följande tabell beskrivs flaggorna för Analytics-cookies:

| Cookie (anges av) | httpOnly | Säker | SameSite |
|--- |--- |--- |--- |
| s_vi   (http-svar) | Nej | Ja när SameSite är None och HTTPS används för anslutningen | &quot;Lax&quot; som standard när CNAME används. &quot;Ingen&quot; när du använder 2o7.net eller omtrdc.net. |
| s_ecid   (http-svar) | Nej | Nej | &quot;Lax&quot; |
| s_fid (Javascript) | Nej | Nej | Ta bort |
| s_cc (JavaScript) | Nej | Nej | Ta bort |
| s_sq (Javascript) | Nej | Nej | Ta bort |

>[!NOTE]
>
>Om du använder en enda CNAME för att spåra över flera domäner eller egenskaper, ska SameSite anges till None för `s_vi`. Kontakta kundtjänst om du behöver hjälp med att ändra inställningarna för Analytics-cookies.

## Cookies angivna av plugin-program {#section-a6b1cae8454945fab9eea5c7884c40fc}

Ytterligare cookies kan anges beroende på hur Analytics-plugin-program används. Dessa cookies är kodfragment som är tillgängliga för klienten för användning i en rad olika situationer. Dessa omständigheter omfattar följande: hämta värden från webbadressen, sammanfogning av värden som ska överföras till Analytics, hämta in formuläravhopp och så vidare. Om du vill ha mer information om cookies som anges av varje plugin-program kontaktar du ClientCare. Ett exempel är den [!DNL s_vh]-cookie som används med plugin-programmen *Set Once Per* och *Set och Get Last Value*.

Konverteringsvariabler (eVarX) som skickas på en bildbegäran utan JavaScript, till exempel kod som placeras i ett e-postmeddelande, tilldelas bara korrekt om e-postklienten och webbläsaren delar samma cookie-utrymme.
