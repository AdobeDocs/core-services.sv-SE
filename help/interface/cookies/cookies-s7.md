---
description: Scene7 använder cookies för att lagra användbar information som kan användas för att leverera dynamiska medier till webbläsaren.
keywords: cookies;privacy
seo-description: Scene7 använder cookies för att lagra användbar information som kan användas för att leverera dynamiska medier till webbläsaren.
seo-title: Scene7 Cookies
solution: Experience Cloud,Analytics,Target
title: Scene7 Cookies
uuid: f9b9d13a-17e5-4139-8c84-6fe5d22c4196
translation-type: tm+mt
source-git-commit: 11ce83401a12c25853cd6412413b8abf98dd6612
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---


# Scene7 Cookies{#scene-cookies}

Scene7 använder cookies för att lagra användbar information som kan användas för att leverera dynamiska medier till webbläsaren.

Scene7 lagrar information lokalt för vissa äldre AS2 Flash-baserade visningsprogram.

För AS2-visningsprogram, cookies:

* Spåra en användares sessionstillstånd, t.ex. aktuell sida och bild som visas, aktuell zoomnivå osv.
* Bestäm hur länge det har varit sedan användarens föregående session. Visningsprogrammet använder den här informationen för att avgöra om en tidigare session ska fortsätta eller om en ny ska startas. Den här informationen skickas också till Scene7-servrarna, men den används inte.

Cookies för visningsprogrammet för AS2 Flash eCatalog:

* Lagra användargenererat innehåll (mest märkbart innehåll som användaren matar in i funktionen &quot;notislappar&quot; i visningsprogrammet för e-kataloger). Innehållet återställs när användaren återupptar en session.
* När användaren initierar ett e-postmeddelande för att dela katalogen med en annan användare, kopieras anteckningsinnehållet från den andra AS2-visningsprogrampunkten till våra servrar för att ge mottagaren det. När mottagaren initierar visningsprogramsessionen hämtas anteckningsinnehållet från servern och kopieras till en cookie. Den här funktionen används sällan, så den upphör inte att gälla och inaktuellt innehåll tas inte bort. För närvarande finns den kvar på servrarna på obestämd tid.

De nyare AS3-visningsprogrammen implementerar inte sessionens beständighet.

**Cookie-namn: VatLogin.jsp**

| Attribut | Beskrivning |
|---|---|
| Information lagrad | Anger sessionscookie. Det AuthFilter som är inbäddat i IPS ImageServer (IS, IR och även SWF-filer/skal och videokontexter) använder cookien för åtkomstauktorisering. Om det finns tillåter det att HTTP-begäranden skickas igenom. Annars returneras obehörig. |
| Förfaller | Denna cookie är en sessionscookie. Den aktuella sessionens förfallotid är inställd på 45 minuter i Scene7 IPS [!DNL web.xml]. |

**Cookie-namn: s7js.flyout.InfoMessage.displayed `assetId`.state**

<table id="table_6835D64C5D464A049F576621F2BE3FAD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Information lagrad </td> 
   <td colname="col2"> <p>&lt;assetId&gt; är namnet på resursen som visningsprogrammet arbetar med. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Förfaller </td> 
   <td colname="col2"> Denna cookie är en sessionscookie som upphör när webbläsaren stängs. </td> 
  </tr> 
 </tbody> 
</table>

**Cookie-namn: s7js.flyout.InfoMessage.displayed`assetId`_idx`id`.ant**

Webbläsarcookies används av äldre DHTML-visningsprogram för att lagra statusinformation och anteckningsdata. De används också av den utfällbara DHTML-koden för flera skärmar för att göra meddelandeindikatorn sessionsspecifika.

<table id="table_8F6CC83D32D54BEE99884318AD126C98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Information lagrad </td> 
   <td colname="col2"> <p> </p> <p> &lt;assetId&gt; är namnet på resursen som visningsprogrammet arbetar med och &lt;id&gt; är det 0-baserade anteckningsindexet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Förfaller </td> 
   <td colname="col2"> Denna cookie är en sessionscookie som upphör när webbläsaren stängs. </td> 
  </tr> 
 </tbody> 
</table>

