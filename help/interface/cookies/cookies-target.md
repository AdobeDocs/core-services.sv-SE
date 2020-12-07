---
description: Läs om hur Adobe Target använder cookies för att ge webbplatsoperatörer möjlighet att testa vilket onlineinnehåll och vilka erbjudanden som är mer relevanta för besökarna.
keywords: cookies;privacy
solution: Experience Cloud,Analytics,Target,Social
title: Så här använder du Adobe Target Cookies | Adobe Experience Cloud
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
translation-type: tm+mt
source-git-commit: 4bea0c29afa580dc63b21535ce5c275cd649c9a5
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 1%

---


# Adobe Target Cookies{#target-cookies}

Adobe Target använder cookies för att ge webbplatsoperatörerna möjlighet att testa vilket onlineinnehåll och vilka erbjudanden som är mer relevanta för besökarna.

Du kan ändra de här inställningarna om det behövs, med undantag för cookie-varaktighet. Kontakta din kontorepresentant när du ändrar cookie-inställningarna.

>[!NOTE]
>
>Adobe Target-användare kan också skapa anpassade cookies från tredje part.

<table id="table_54B402C6E19C4A70B1E27BC9DFF776EB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Inställning </th> 
   <th colname="col2" class="entry"> Information </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie-namn </p> </td> 
   <td colname="col2"> <p>mbox. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie-domän </p> </td> 
   <td colname="col2"> <p>Den andra och övre nivån i de domäner som du använder mbox från. Eftersom cookie används av ditt företags domän är den en cookie från första part. Exempel: <span class="filepath"> mycompany.com</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serverdomän </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> clientcode.tt.omtrdc.net</span>, använda klientkoden för ditt Adobe Target-konto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie-varaktighet </p> </td> 
   <td colname="col2"> <p>Cookien finns kvar i besökarens webbläsare två år efter hans eller hennes senaste inloggning. Du kan inte ändra varaktighet för cookie-filen. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Om något av dina domännamn innehåller en landskod, t.ex. [!DNL mycompany.co.uk], kan du samarbeta med dina klienttjänster för att konfigurera dina domäner [!DNL mbox.js] så att de stöder detta.

Denna cookie har ett antal värden för att hantera hur besökarna upplever Adobe Target kampanjer:

<table id="table_5245F72A2D5A4322B40ABB10B7DFB338"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Värde </th> 
   <th colname="col2" class="entry"> Definition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sessions-ID</span> </p> </td> 
   <td colname="col2"> <p>Ett unikt ID för en användarsession. Som standard varar detta 30 minuter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pc-ID</span> </p> </td> 
   <td colname="col2"> <p>Ett halvpermanent ID för en besökares webbläsare. Varar tills cookies tas bort manuellt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> check</span> </p> </td> 
   <td colname="col2"> <p>Ett enkelt testvärde som används för att avgöra om en besökare stöder cookies. Ange varje gång en besökare begär en sida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> disable</span> </p> </td> 
   <td colname="col2"> <p>Ange om besökarens inläsningstid överskrider den timeout som har konfigurerats i filen <span class="filepath"> mbox.js</span> . Som standard varar detta 1 timme. </p> </td> 
  </tr> 
 </tbody> 
</table>

