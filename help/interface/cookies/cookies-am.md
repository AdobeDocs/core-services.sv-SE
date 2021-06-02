---
description: Läs mer om Audience Manager cookies i Adobe Experience Cloud.
keywords: cookies
solution: Experience Cloud, Audience Manager
title: 'Audience Manager Cookies '
uuid: 8b384c38-b85a-4e93-b00e-41a9d3ae2b21
feature: Cookies
topic: Administrering
role: Administrator
level: Experienced
exl-id: ab6de845-99ea-4cd8-b7cd-012fb641403f
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 2%

---

# Audience Manager Cookies{#audience-manager-cookies}

Audience Manager förlitar sig på några enkla cookies för att utföra olika funktioner. Det kan vara till exempel att tilldela ID:n, spela in datainanrop, felspårning och testa om cookies kan anges. I det här avsnittet listas och beskrivs de olika cookies som har angetts av Audience Manager.

**demdex Cookie**

<table id="table_1CCF7EA2BC9E421F8DEECA5F611E33F6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Syfte</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager  </span> ställer in den här cookien så att den tilldelar ett unikt ID till en besökare. Cookien <span class="wintitle"> demdex </span> hjälper <span class="keyword"> Audience Manger </span> att utföra grundläggande funktioner som besökaridentifiering, ID-synkronisering, segmentering, modellering, rapportering och så vidare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Innehåll</b> </p> </td> 
   <td colname="col2"> <p>Cookien <span class="wintitle"> demonstrationen </span> innehåller ett unikt användar-ID (UUID) enligt exemplet nedan: </p> <p> <span class="codeph"> 061513042277697204303923517820449977  </span> </p> <p>Se även <a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en" format="https" scope="external"> ID-index i Audience Manager </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Andra attribut</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_11291DA87C5045E880034E06C863BCDA"> 
      <li id="li_40C30A06A12449A4A8748621223CA71B">Livstid: Cookien <span class="wintitle"> demdex </span> har ett TTL-intervall på 180 dagar. TTL återställs till 180 dagar efter varje användarinteraktion med en partnerwebbplats. Cookien upphör att gälla om en användare inte kommer tillbaka till webbplatsen inom TTL-intervallet. </li> 
      <li id="li_A589EDA2198249829207A183872EF1FF">Avanmäl dig: <span class="keyword"> Audience Manager </span> återställer cookien med en <span class="codeph"> Do Not Adobe Target </span>-sträng om en användare väljer bort från datainsamlingen. I det här fallet anges TTL-värdet för cookie till 10 år. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**dextp Cookie**

<table id="table_7343C9C9ADD24D3FA693ECC76E4A4045"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Syfte</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager  </span> ställer in den här cookien så att den registreras senast den gjorde ett datasynkroniseringsanrop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Innehåll</b> </p> </td> 
   <td colname="col2"> <p>Cookien <span class="wintitle"> dextp </span> innehåller ett dataleverantörsnamn eller ett ID och en UNIX UTC-tidsstämpel formaterad som pipe-avgränsade strängar. I exemplen representerar <i>kursiv</i> en variabelplatshållare. </p> <p> 
     <ul id="ul_80D0BC3FCF06470991E12712401D784A"> 
      <li id="li_03747A433CEB4756A26CD866E716B89D">Gammalt format: <span class="codeph"> <span class="varname"> dataleverantörsnamn här </span>-1490307822097| <span class="varname"> dataleverantörsnamn här </span>-1490307822038 </span> </li> 
      <li id="li_79E7000E82DB4ADA9E9887B017343B2D">Nytt format: <span class="codeph"> 21-1-1490307821616|544-1-1490307821793|3-1-1490307821852|420-1-1490307822038| </span> </li> 
     </ul> </p> <p>Se även avsnittet om syntax för dextp-data nedan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Andra attribut</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_4922AC2CD55D4C888A6FBEB22F8B889B"> 
      <li id="li_91A68C44E53840379C2ACDED25468735">Livstid: Cookien <span class="wintitle"> dextp </span> har ett TTL-intervall på 180 dagar. </li> 
      <li id="li_6B8C674EFAAC4DABA0A640CF29247F99">Avanmäl dig: <span class="keyword"> Audience Manager </span> återställer cookien med en <span class="codeph"> Do Not Adobe Target </span>-sträng om en användare väljer bort från datainsamlingen. I det här fallet anges TTL-värdet för cookie till 10 år. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

dextp Cookie-datasyntax:

I följande tabell visas och definieras elementen i en `dextp`-cookie efter plats i datasträngen.

<table id="table_BE00604B97F24F5A94AA4F566063D785"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variabelposition </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Första eller andra</b> </p> </td> 
   <td colname="col2"> <p>Placeringen av dataleverantörens namn eller ID varierar beroende på om cookien använder den nya eller gamla formateringen. </p> <p> <b>Gammal formatering:</b> </p> <p> 
     <ul id="ul_5BFBF40E3FE849CA859030F2D070FDF6"> 
      <li id="li_E8F4DC0CB15B472ABE9892B3A61D7F77">Syntax: <span class="codeph"> <span class="varname"> dataleverantörsnamn </span> - <span class="varname"> UNIX UTC-tidsstämpel </span> </span> </li> 
      <li id="li_7CD8B101156140F49EA97B18E9591402">Exempel: <span class="codeph"> dataProvider1 - 1490307822038 </span> </li> 
     </ul> </p> <p>Den gamla stilcookien identifierar DataProvider med ett läsbart namn. </p> <p> <b>Ny formatering:</b> </p> <p> 
     <ul id="ul_AC6225CA781746148C125F21DFED1ED9"> 
      <li id="li_29C4B52E398B4EA28944980A15B05A57">Syntax: <span class="codeph"> <span class="varname"> Data provider ID </span> - 1|2 - <span class="varname"> UNIX UTC-tidsstämpel </span> </span> </li> 
      <li id="li_3BF30CA5FED242DF96E0B54AFC64B06F">Exempel: <span class="codeph"> 123345 - 1 - 1490307822038 </span> </li> 
     </ul> </p> <p>Den nya stilcookien: </p> <p> 
     <ul id="ul_F05A91A455FA44C7A71186C0C9E31630"> 
      <li id="li_A8C9638173684359BABC4207845A4F48">Ersätter det läsbara dataleverantörsnamnet med ett numeriskt ID. </li> 
      <li id="li_28F1E2DB24904E53BE9718AD788CE61E">Identifierar samtalstypen med ID 1 eller ID 2. ID 1 representerar ett ID-synkroniseringsanrop. ID 2 representerar ett inaktuellt anrop som inte längre används. Du ska inte se många (eller några) dextp-cookies med ID 2. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Sista</b> </p> </td> 
   <td colname="col2"> <p>Den sista positionen innehåller en UNIX UTC-tidsstämpel. </p> </td> 
  </tr> 
 </tbody> 
</table>

**dst Cookie**

<table id="table_83AE9B6350C6408BAECD9FCF33022B98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribut </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Syfte</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager  </span> ställer in denna cookie när ett fel uppstår när data skickas till ett  <a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html?lang=en" format="https" scope="external"> mål  </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Innehåll</b> </p> </td> 
   <td colname="col2"> <p> Cookien <span class="wintitle"> DST </span> innehåller uppsättningar mål-ID:n och UNIX-tidsstämplar formaterade som pipe-avgränsade strängar. I exemplen representerar <i>kursiv</i> en variabelplatshållare. </p> <p> 
     <ul id="ul_CE98076A02DA413486C1D341E9806889"> 
      <li id="li_850209D956644749B98C7A208C825C15">Syntax: <span class="codeph"> <span class="varname"> mål-ID </span> - <span class="varname"> UNIX UTC-tidsstämpel </span> </span> </li> 
      <li id="li_4A22152C70844733982230EBF7B9EB78">Exempel: <span class="codeph"> 067797-1490349684|1010788-1490349692|1067797-14903496 92 </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Andra attribut</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_5D13DD701B484B51BF2808A69A919106"> 
      <li id="li_4E665114C63246FBA32A4E19984D2693">Livstid: Cookien <span class="wintitle"> dst </span> har ett TTL-intervall på 180 dagar. </li> 
      <li id="li_A682B566704F43D2AB72487EFF212474">Avanmäl dig: <span class="keyword"> Audience Manager </span> återställer cookien med en <span class="codeph"> Do Not Adobe Target </span>-sträng om en användare väljer bort från datainsamlingen. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**_dp Cookie**

Den här kakan är tillfällig. [!DNL Audience Manager] försöker att ställa in  `_dp` cookien för att avgöra om den kan ställa in andra cookies i domänen demdex.net i en tredjepartskontext. När `_dp` är inställt innehåller det värdet 1. [!DNL Audience Manager] läser det här värdet och tar omedelbart bort cookien. Om cookien `_dp` inte finns vet [!DNL Audience Manager] att den inte kan ange cookies.
