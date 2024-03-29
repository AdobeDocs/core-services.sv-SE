---
description: Läs mer om Adobe Advertising cookies för att mappa annonsevenemang till konverteringshändelser och, eventuellt, använda informationen för att optimera annonsanbud.
title: Adobe Advertising Cookies
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
source-git-commit: 5d0e02713ec4b233e06ecd3ac0234d1526b947f1
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 4%

---

# Adobe Advertising Cookies{#advertising-cloud-cookies}

Adobe Advertising (tidigare Adobe Advertising Cloud) använder cookies för att mappa annonsengagemangshändelser till konverteringshändelser och, eventuellt, för att använda informationen för att optimera annonserbjudanden.

>[!NOTE]
>
>Taggen Adobe Advertising Javascript som använder [Tjänsten Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) skapar [cookies från första part i Experience Cloud s_ecid](cookies-first-party.md), inte Adobe Advertising cookies.

## Cookie-namn: _lcc

<table id="table_821F8EBE91F244CBA72B0975B961B908"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Information lagrad </p> </td> 
   <td colname="col2"> <p>ID:n och tidsstämplar (i formatet yyyymd) för visningsklickningar</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Förfallotid </p> </td> 
   <td colname="col2"> <p>15 minuter</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Användning </p> </td> 
   <td colname="col2"> <p>En cookie från tredje part som används för att avgöra om en klickhändelse på en displayannons gäller för en Adobe Analytics-träff </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Plats </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Storlek </p> </td> 
   <td colname="col2"> <p>52 byte </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie-namn: _namn

<table id="table_28C2B62595E240D5A3C3E0BE147748C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Information lagrad </p> </td> 
   <td colname="col2"> <p>Kodade ID:n och tidsstämplar för annonsinsatser med hjälp av spårning i Adobe Advertising DSP </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Förfallotid </p> </td> 
   <td colname="col2"> <p>1 år </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Användning </p> </td> 
   <td colname="col2"> <p>En cookie från tredje part som lagrar användarinteraktioner med annonser, t.ex."last see ad xyz123 on June 30, 2016" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Plats </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Storlek </p> </td> 
   <td colname="col2"> <p>Variabel; data är kodade och vanligtvis mindre än 1 kB </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie-namn: adcloud

<table id="table_D7CD238736BC4571883F92F47673F57C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Information lagrad </p> </td> 
   <td colname="col2"> <p>Tidsstämplar för surfens senaste besök på annonsörens webbplats och surfens senaste sökklick samt det ef_id som skapades när användaren klickade på en annons</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Förfallotid </p> </td> 
   <td colname="col2"> <p>1 år</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Användning </p> </td> 
   <td colname="col2"> <p>En cookie från första part som kopplar surfer-ID till relevanta målgruppssegment och konverteringar </p> <p> Information om det senaste besöket används för att optimera sidladdningstiden genom att man undviker onödiga förfrågningar om att [!DNL Adobe] servrar. </p> <p>Information om den senaste klickningen hjälper till att avgöra om en konverteringshändelse är resultatet av en klickning eller en genomgång (konvertering som är ett resultat av visningar men inga klick). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Plats </p> </td> 
   <td colname="col2"> <p>Annonsörens toppnivådomän (till exempel example.com) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Storlek </p> </td> 
   <td colname="col2"> <p>Variabel, men vanligtvis 50-150 byte </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie-namn: ev_sync_&#42;

(ev_sync_ax, ev_sync_bk, ev_sync_dd, ev_sync_fs, ev_sync_ix, ev_sync_nx, ev_sync_ox, ev_sync_pm, ev_sync_rc, ev_sync_tm, ev_sync_yh)

<table id="table_A05C02AB261946E0AABAD78259392D81"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Information lagrad </p> </td> 
   <td colname="col2"> <p>Det datum då synkronisering utförs, i formatet åååmmdd </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Förfallotid </p> </td> 
   <td colname="col2"> <p>Det datum då synkronisering utförs, i formatet åååmmdd </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Användning </p> </td> 
   <td colname="col2"> <p>En tredjeparts-annonsspecifik cookie som synkroniserar Adobe Advertising surfer-ID med partnerannonsutbytet. Den skapas för nya surferingar och skickar en synkroniseringsbegäran när den har gått ut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Plats </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Storlek </p> </td> 
   <td colname="col2"> <p>8 tecken </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie-namn: serverest_g_v2

<table id="table_04043292A43B41B69EAF17AF4E217C69"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Information lagrad </p> </td> 
   <td colname="col2"> <p>Webbläsar- och surfares-ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Förfallotid </p> </td> 
   <td colname="col2"> <p>1 år </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Användning </p> </td> 
   <td colname="col2"> <p>Skapas efter att en användare först klickat på en klientannons och används för att mappa aktuella och efterföljande klickningar med andra händelser på klientens webbplats </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Plats </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Storlek </p> </td> 
   <td colname="col2"> <p>~27 tecken </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie-namn: serverest_session_v2

<table id="table_1A3AE4CA71304ADB943CB1F64BE695F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Information lagrad </p> </td> 
   <td colname="col2"> <p>Sessions-ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Förfallotid </p> </td> 
   <td colname="col2"> <p>När webbläsaren stängs </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Användning </p> </td> 
   <td colname="col2"> <p>En cookie för webbläsarsession från tredje part; en cookie används för alla konton </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Plats </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Storlek </p> </td> 
   <td colname="col2"> <p>~16 tecken </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie-namn: ev_tm

<table id="table_6C4D9DCFA4BF4FB2BD445E027550955F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Information lagrad </p> </td> 
   <td colname="col2"> <p>Adobe Advertising DSP (Demand Side Platform)-ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Förfallotid </p> </td> 
   <td colname="col2"> <p>2 år </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Användning </p> </td> 
   <td colname="col2"> <p>En cookie från tredje part som lagrar det DSP-ID som motsvarar surfer-ID:t i cookie-filen everest_g_v2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Plats </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Storlek </p> </td> 
   <td colname="col2"> <p>~20 byte </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie-namn: id_adcloud

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Information lagrad </p> </td> 
   <td colname="col2"> <p>surfer-ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Förfallotid </p> </td> 
   <td colname="col2"> <p>91 dagar </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Användning </p> </td> 
   <td colname="col2"> <p>Cookien har angetts i förstahandsdomänen men används inte än </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Plats </p> </td> 
   <td colname="col2"> <p>Annonsörens toppnivådomän (till exempel example.com) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Storlek </p> </td> 
   <td colname="col2"> <p>16 byte </p> </td> 
  </tr> 
 </tbody> 
</table>
