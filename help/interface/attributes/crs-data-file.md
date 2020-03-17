---
description: Datafilskrav och flera datakällor för överföring av kundattribut till Experience Cloud.
keywords: customer attributes;core services
seo-description: Datafilskrav och flera datakällor för överföring av kundattribut till Experience Cloud.
seo-title: Om datafiler och datakällor för kundattribut
solution: Experience Cloud
title: Om datafiler och datakällor för kundattribut
uuid: 9dd0e364-889b-45db-b190-85c0930a101e
translation-type: tm+mt
source-git-commit: 73cb227d2b44024706ce24a9ae6aa06c57a8ce85

---


# Om datafiler och datakällor för kundattribut

Datafilskrav och flera datakällor för överföring av kundattribut till Experience Cloud.

Du behöver åtkomst till CRM eller liknande data från ditt företag. De data du överför till Experience Cloud måste vara en `.csv` fil. Om du överför via FTP eller sFTP överför du även en `.fin` fil.

Kundattribut är utformat för att hantera några filer per dag. För att minska problemet med att ha ett stort antal små filer som försenar bearbetningen dirigeras filer som skickas inom 30 minuter från en tidigare batch från samma organisation till en kö med lägre prioritet.

<!-- <p>Articulate difference between this and SAINT. </p> -->

## Tillåtna filtyper och namnkrav {#section_6F64FA02ACCC4215B0862CB6A1821FBF}


<table id="table_C27955F6B52A45B28BEEAAF14FFC86D8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Filtyp </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .csv </span> </p> </td> 
   <td colname="col2"> <p>En fil med kommaavgränsade värden (t.ex. en som skapats i Excel). Det här är filen som innehåller kundattributdata. </p> <p> <b>Namngivningskrav:</b> Kontrollera att filnamnstilläggen inte innehåller blanksteg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .fin </span> </p> </td> 
   <td colname="col2"> <p>(Obligatoriskt) <span class="filepath"> .fin- </span> filen talar om för systemet att du är klar med överföringen av data. Namnet på <span class="filepath"> .fin- </span> filen måste matcha namnet på <span class="filepath"> .csv- </span> filen. </p> <p>Adobe rekommenderar att du skapar en tom textfil med <span class="filepath"> filtillägget </span> .fin. En tom fil sparar utrymme och laddningstid. </p> <p> <p>Obs!  Det går inte att ändra namn på en <span class="filepath"> .fin- </span> fil efter att den har överförts. FIN- <span class="filepath"></span> filen måste överföras separat och kan inte ha bytt namn, tidigare överförd fil. </p> </p> <p>När du har överfört <span class="filepath"> .fin- </span> filen i kundattributen FTP hämtar systemet data snabbt (inom en minut). Detta skiljer sig från andra Adobe FTP-baserade system, som hämtar in data mindre ofta (ungefär en gång per timme). </p> <p>FIN- <span class="filepath"></span> filen behövs inte när du använder metoden för att dra och släppa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .gz </span> eller <span class="filepath"> .zip </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> .gz </span> (gzip) eller <span class="filepath"> .zip </span> - för komprimerade filer. En <span class="filepath"> .zip- </span> fil får inte innehålla mer än en fil i arkivet. </p> <p> <b>Namngivningskrav:</b> Namnet på <span class="filepath"> .zip </span> eller <span class="filepath"> .gz </span> måste matcha namnet på <span class="filepath"> .csv </span>. Om <span class="filepath"> .csv- </span> filen till exempel är <span class="filepath"> crm_small.csv </span>, ska <span class="filepath"> .zip- </span> filen vara <span class="filepath"> crm_small.csv.zip </span>. </p> <p>FIN-filen måste matcha CSV-filen. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Krav för attributdatafiler {#section_169FBF5B7BBA47CE825B7A330CF3FE98}



**Exempel på CSV**

CSV-filen måste ha följande format:

Exempel på CSV:

![](assets/cvs.png)

Samma fil som visas i en textredigerare:

![](assets/csv_txt.png)

**Riktlinjer**

<table id="table_A9849CC9AA784763921DE057F0F61515"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Objekt </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Dra och släppa </p> </td> 
   <td colname="col2"> <p>Dra och släpp-filen bör vara mindre än 100 megabyte. </p> <p>FIN- <span class="filepath"></span> filen behövs inte när du använder metoden för att dra och släppa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kund-ID, kolumn </p> </td> 
   <td colname="col2"> <p> Den första kolumnen måste vara ett unikt kund-ID. Det ID som används ska motsvara det ID som skickas till Experience Cloud ID-tjänsten. </p> <p>För Analytics lagras ID:t i en prop eller eVar. </p> <p>För Target anger du värdet setCustomerID. (Se <a href="../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437" format="dita" scope="local"> Analytics &amp; Target - synching the customer ID </a>) </p> <p> Detta kund-ID är den unika identifierare som CRM använder för varje person i din databas. De återstående kolumnerna är attribut som kommer från CRM. Du väljer hur många attribut du vill överföra. </p> <p>Ett läsbart namn rekommenderas för kolumnrubrikerna, men det behövs inte. När du validerar schemat efter överföring kan du mappa egna namn till överförda rader och kolumner. </p> <p> <b>Om Kund-ID</b> </p> <p>Ett företag använder vanligtvis ett kund-ID från ett CRM-system. Detta ID anges med <span class="codeph"> anropet setCustomerIDs </span> när en person loggar in. Detta ID används också som nyckel i CRM-filen som överförs till Experience Cloud. Ett <a href="../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8" format="dita" scope="local"> alias-ID </a> är ett eget namn för ett datalager i Audience Manager, där aliasdata lagras. Systemet skickar alias till detta datalager (via setCustomerID:n). CRM-filen används på data i det datalagret. </p> <p>Mer information om <span class="codeph"> setCustomerID: </span> finns i <a href="https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html" format="https" scope="external"> Kund-ID:n och autentiseringstillstånd </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Efterföljande rubriker och kolumner </p> </td> 
   <td colname="col2"> <p>Efterföljande rubriker ska representera namnet på varje attribut. </p> <p> Dessa kolumner ska innehålla kundattribut som kommer från CRM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attributgränser </p> </td> 
   <td colname="col2"> <p>Du kan överföra hundratals <span class="filepath"> .csv- </span> kolumner till kundattributtjänsten i Experience Cloud. När du konfigurerar prenumerationer och väljer attribut gäller dock följande begränsningar beroende på vilka lösningar du har: </p> <p> 
     <ul id="ul_2BB85067918D4BB3B59394F3E3E37A6D"> 
      <li id="li_93703988B9934384B4B94A839D028380"> <b>Analysstandard</b>: 3 totalt </li> 
      <li id="li_D1E5E7BD24C54591B14D15DE97447835"> <b>Analytics Premium</b>: 200 per rapportserie </li> 
      <li id="li_8C891FE3D1EF49FA9F81E2E32CD0B9CA"> <b>Målstandard:</b> 5 </li> 
      <li id="li_2B66D43023F34EA685CE2C38A9250CEA"> <b>Target Premium:</b> 200 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Radbegränsningar </p> </td> 
   <td colname="col2"> <p>Det finns ingen känd gräns för antalet rader. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kolumngränser </p> </td> 
   <td colname="col2"> <p>Av praktiska skäl bör du begränsa antalet kolumner till ca 200. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Teckengränser </p> </td> 
   <td colname="col2"> <p>När du skapar en Analytics-prenumeration trunkeras fältlängderna för de överförda filerna till 255. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FTP-riktlinjer och storleksbegränsningar </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_E157EE6F98914EADA0C103D1D1E705D3"> 
      <li id="li_84FBD455DD164A28AC16F4A5AB19E4B3">Maximal filstorlek för FTP är 4 GB för varje överföring. </li> 
      <li>Minsta filstorleksgräns för 10 MB för varje överföring. </li>
      <li>Du kan överföra en fil var halvtimme. </li>
      <li id="li_B69A20C51D824727AA99C1F6F78537A4"> Du bör släppa <span class="filepath"> .csv-filen </span> (och <span class="filepath"> .fin-filen </span>) i FTP-platsens rotmapp. </li> 
     </ul> </p> <p> <p>Viktigt:  Det totala tillåtna utrymmet för FTP-kontot är 40 GB. Det är ditt ansvar att ta bort bearbetade filer. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Filkrav </p> </td> 
   <td colname="col2"> <p> Varje attributkälla ska innehålla samma antal kommaavgränsade fält. </p> <p> Fält som innehåller en radbrytning, dubbla citattecken eller kommatecken måste citeras. </p> <p> Dubbelcitattecken i ett fält måste föregås av ett omvänt snedstreck (\). </p> <p> Tomma kolumner lagras som <span class="term"> null </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Flera filer </p> </td> 
   <td colname="col2"> <p>När du överför kundattributdata, om du har flera filer som du vill överföra i snabb följd, och särskilt om filerna är stora, bör du kontrollera att den föregående filen har bearbetats innan du överför nästa fil. Du kan övervaka detta genom att kontrollera när den tidigare filen har flyttats till den bearbetade eller misslyckade mappen i ditt kundattribut via FTP-kontot. </p> <p> Att dela upp en stor fil i mindre filer och skicka in dem i snabb följd kan i själva verket göra bearbetningen långsammare, såvida du inte kan säkerställa att varje fil bearbetas fullständigt innan du skickar in nästa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Teckenkodning </p> </td> 
   <td colname="col2"> <p>För Japan är UTF-8 obligatoriskt. </p> </td> 
  </tr> 
   <tr> 
   <td colname="col1"> <p>Historiska data </p> </td> 
   <td colname="col2"> <p> Kundattribut är knutna till den underliggande besökarprofilen i Analytics. Därför kopplas kundattribut till besökaren under hela besökarprofilens livstid i Analytics. Detta inkluderar beteenden som inträffade innan kunden loggade in för första gången. </p> <p> Om du använder metoden för bakåtfyllnad av datalager är data knutna till en post_visid_high/low som är baserad på analys-ID (AID). Om du använder Experience Cloud ID Service är data knutna till en post_visid_high/low som baseras på Experience Cloud ID (MID). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dataflöden </p> </td> 
   <td colname="col2"> <p>Kundattribut är inte tillgängliga i dataflöden. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Utnyttja flera datakällor {#section_76DEB6001C614F4DB8BCC3E5D05088CB}

När du skapar, ändrar eller tar bort kundattributskällor är det en fördröjning på ungefär en timme innan ID:n börjar synkronisera med den nya datakällan.

Alias-ID för varje kundattributkälla måste vara unikt. Om du har flera datakällor som använder samma ID bör de konfigureras enligt följande:

**I VisitorAPI.js eller Experience Cloud ID-verktyget i dynamisk tagghantering:**

Ange två kund-ID som ska motsvara rätt datakällor:

```
Visitor.setCustomerIDs({ 
     "ds_id1”:"123456", 
     "ds_id2":"123456" 
});
```

(Mer information finns i [Kund-ID och Autentiseringstillstånd](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) .)

I **[!UICONTROL Experience Cloud]** > **[!UICONTROL People]** > **[!UICONTROL Customer Attributes]**:

Skapa två kundattributskällor med unika alias-ID:n som motsvarar kundens ID:n ovan. Med den här metoden kan samma referens-ID skickas till flera källor för kundattribut
