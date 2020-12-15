---
description: Adobe Experience Cloud använder cookies för att lagra ett besökar-ID som används mellan Experience Cloud Solutions.
keywords: cookies;privacy
solution: Experience Cloud,Analytics,Target
title: 'Experience Cloud Cookies '
uuid: a4788c1c-0402-4fc8-b894-cd24fa794f4f
translation-type: tm+mt
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---


# Experience Cloud Cookies{#experience-cloud-cookies}

Adobe Experience Cloud använder cookies för att lagra ett besökar-ID som används mellan Experience Cloud Solutions.

**Cookie-namn: s_ecid**

<table id="table_FF4C70D3D4CC425BA65162D5A9504F7D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Information lagrad </p> </td> 
   <td colname="col2"> <p> Innehåller en kopia av Experience Cloud ID (ECID) eller MID. MID lagras i ett nyckelvärdepar som följer syntaxen s_ecid=MCMID|&lt;ECID&gt; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Förfaller </p> </td> 
   <td colname="col2"> <p>2 år </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Användning </p> </td> 
   <td colname="col2"> <p>Denna cookie anges av kundens domän efter att AMCV-cookien har angetts av klienten. Syftet med denna cookie är att tillåta beständig ID-spårning i det första partsläget och används som referens-ID om AMCV-cookien har upphört att gälla. Mer information finns i AMCV-cookie här. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Plats </p> </td> 
   <td colname="col2"> <p>Endast CNAME-kunder. Gäller inte för tredjepartsscenarier. Cookie lagras på din domän, samma domän som används av CNAME och din bildförfrågan från Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Storlek </p> </td> 
   <td colname="col2"> <p>45 byte </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> SameSite=Lax </p> </td> 
   <td colname="col2"> <p>Cookies med den här inställningen skickas bara när domänen som visas i webbläsarens URL matchar cookie-domänen. Det här är det nya standardvärdet för cookies i Chrome.</p> </td> 
  </tr> 
 </tbody> 
</table>

**Cookie-namn: AMCV_###@AdobeOrg**

I [Experience Platform ID-tjänsten](https://docs.adobe.com/content/help/sv-SE/id-service/using/home.html) används JavaScript för att lagra ett unikt besökar-ID i en `AMCV_###@AdobeOrg` cookie på den aktuella webbplatsens domän, där `###` representerar en slumpmässig teckensträng, till exempel `AMCV_1FD6776A524453CC0A490D44%40AdobeOrg.`

Se även [cookies och ID-tjänsten](https://docs.adobe.com/content/help/sv-SE/id-service/using/intro/cookies.html).

<table id="table_1883C0836C1E4AF5A262FBF5000C1B11"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Information lagrad </p> </td> 
   <td colname="col2"> <p> Unika besökar-ID som används av Experience Cloud Solutions. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Förfaller </p> </td> 
   <td colname="col2"> <p> 2 år </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Användning </p> </td> 
   <td colname="col2"> <p> Denna cookie används för att identifiera en unik besökare </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Plats </p> </td> 
   <td colname="col2"> <p> Denna cookie lagras på webbplatsens domän (inte domänen för bildbegäran). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Storlek </p> </td> 
   <td colname="col2"> <p> De flesta kunder kan förvänta sig att den här cookien ska vara ca 200 byte lång. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inget värde har lagts till. Chrome får standardvärdet Lax. </p> </td> 
   <td colname="col2"> <p> Cookies med den här inställningen skickas bara när domänen som visas i webbläsarens URL matchar cookie-domänen. Det här är det nya standardvärdet för cookies i Chrome. </p> </td> 
  </tr> 
 </tbody> 
</table>
