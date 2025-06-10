---
description: Lär dig hur ID-tjänsten lagras och används i olika Experience Cloud-program.
solution: Experience Cloud,Analytics,Target
title: Experience Cloud Cookies
uuid: a4788c1c-0402-4fc8-b894-cd24fa794f4f
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bd9bea58-9987-40d6-84e0-da185388bbbb
source-git-commit: 2073400a04933226bd036c1fcd729df70f101df3
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 1%

---

# Experience Cloud cookies

Adobe Experience Cloud använder cookies för att lagra ett besökar-ID som används mellan olika Experience Cloud-program. Dessa cookies gäller specifikt för åtkomst till Adobe Experience Cloud-program på [experience.adobe.com](https://experience.adobe.com).

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
   <td colname="col1"> <p> Förfallotid </p> </td> 
   <td colname="col2"> <p>2 år, men de flesta moderna webbläsare trunkerar till 13 månader</p> </td> 
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
   <td colname="col2"> <p>Cookies med den här inställningen skickas bara när domänen som visas i webbläsarens URL matchar cookie-domänen. Den här inställningen är ny som standard för cookies i Chrome.</p> </td> 
  </tr> 
 </tbody> 
</table>

**Cookie-namn: AMCV_###@AdobeOrg**

[Experience Platform ID-tjänsten](https://experienceleague.adobe.com/docs/id-service/using/home.html) använder JavaScript för att lagra ett unikt besökar-ID i en `AMCV_###@AdobeOrg`-cookie på den aktuella webbplatsens domän, där `###` representerar en slumpmässig teckensträng, till exempel `AMCV_1FD6776A524453CC0A490D44%40AdobeOrg.`

Se även [Cookies och ID-tjänsten](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html).

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
   <td colname="col1"> <p> Förfallotid </p> </td> 
   <td colname="col2"> <p> 13 månader </p> </td> 
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
   <td colname="col1"> <p>Inget värde har lagts till. Chrome är som standard Lax. </p> </td> 
   <td colname="col2"> <p> Cookies med den här inställningen skickas bara när domänen som visas i webbläsarens URL matchar cookie-domänen. Den här inställningen är ny som standard för cookies i Chrome. </p> </td> 
  </tr> 
 </tbody> 
</table>
