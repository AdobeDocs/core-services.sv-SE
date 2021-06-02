---
description: Läs mer om krav på datafiler och flera datakällor för överföring av kundattribut till Experience Cloud.
keywords: Kundattribut;bastjänster
solution: Experience Cloud
title: 'Läs mer om datafiler och datakällor för kundattribut '
uuid: 9dd0e364-889b-45db-b190-85c0930a101e
feature: Kundattribut
topic: Administrering
role: Administrator
level: Experienced
exl-id: e2dfe10d-7003-4afa-a5e6-57703d74efd4
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '1193'
ht-degree: 0%

---

# Om datafiler och datakällor för kundattribut

Datafilskrav och flera datakällor för överföring av kundattribut till Experience Cloud.

Du behöver åtkomst till CRM eller liknande data från ditt företag. De data som du överför till Experience Cloud måste vara en `.csv`-fil. Om du överför via FTP eller sFTP överför du även en `.fin`-fil.

Kundattribut är utformat för att hantera några filer per dag. För att minska problemet med att ha många små filer som försenar bearbetningen dirigeras filer som skickas inom 30 minuter från en tidigare batch från samma organisation till en kö med lägre prioritet.

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
   <td colname="col1"> <p> <span class="filepath"> .csv  </span> </p> </td> 
   <td colname="col2"> <p>En fil med kommaavgränsade värden (t.ex. en som skapats i Excel). Den här filen innehåller kundattributsdata. </p> <p> <b>Namngivningskrav:</b> Kontrollera att filnamnstillägg inte innehåller blanksteg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .fin  </span> </p> </td> 
   <td colname="col2"> <p>(Obligatoriskt) Filen <span class="filepath"> .fin </span> talar om för systemet att du är klar med överföringen av data. Namnet på filen <span class="filepath">.fin </span> måste matcha namnet på filen <span class="filepath"> .csv </span>. </p> <p>Adobe rekommenderar att du skapar en tom textfil med filnamnstillägget <span class="filepath"> .fin </span>. En tom fil sparar utrymme och laddningstid. </p> <p> <p>Obs!  Det går inte att ändra namn på en <span class="filepath"> .fin </span>-fil efter att den har överförts. Filen <span class="filepath">.fin </span> måste överföras separat och kan inte ha bytt namn, tidigare överförd fil. </p> </p> <p>När du har överfört filen <span class="filepath"> .fin </span> i kundattributens FTP hämtar systemet data snabbt (inom en minut). Detta skiljer sig från andra Adobe FTP-baserade system, som hämtar in data mindre ofta (ungefär en gång i timmen). </p> <p>Filen <span class="filepath"> .fin </span> krävs inte när du använder metoden för att dra och släppa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .gz  </span> eller  <span class="filepath"> .zip  </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> .gz  </span> (gzip) eller  <span class="filepath"> .zip  </span> - för komprimerade filer. En <span class="filepath">.zip </span>-fil får inte innehålla mer än en fil i arkivet. </p> <p> <b>Namngivningskrav:</b> Namnet på  <span class="filepath"> .zip  </span> eller  <span class="filepath"> .gz  </span> ska matcha namnet på  <span class="filepath"> .csv  </span>. Om till exempel din <span class="filepath"> .csv </span>-fil är <span class="filepath"> crm_small.csv </span> ska .zip <span class="filepath">-filen vara <span class="filepath"> crm_small.csv.zip </span>.</span> </p> <p>FIN-filen måste matcha CSV-filen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Krav för attributdatafiler {#section_169FBF5B7BBA47CE825B7A330CF3FE98}

**Exempel på CSV**

CSV-filen måste ha följande format:

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
   <td colname="col2"> <p>Dra och släpp-filen bör vara mindre än 100 MB. </p> <p>Filen <span class="filepath"> .fin </span> krävs inte när du använder metoden för att dra och släppa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kund-ID, kolumn </p> </td> 
   <td colname="col2"> <p> Den första kolumnen måste vara ett unikt kund-ID. Det ID som används ska motsvara det ID som skickas till Experience Cloud ID-tjänsten. </p> <p>För Analytics lagras ID:t i en propp eller eVar. </p> <p>För Target anger du värdet setCustomerID. (Se <a href="../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437" format="dita" scope="local"> Analytics &amp; Adobe Target - synching the customer ID </a>) </p> <p> Detta kund-ID är den unika identifierare som CRM använder för varje person i din databas. De återstående kolumnerna är attribut som kommer från CRM. Du väljer hur många attribut du vill överföra. </p> <p>Ett läsbart namn rekommenderas för kolumnrubrikerna, men det behövs inte. När du validerar schemat efter överföring kan du mappa egna namn till överförda rader och kolumner. </p> <p> <b>Om Kund-ID</b> </p> <p>Ett företag använder vanligtvis ett kund-ID från ett CRM-system. Detta ID anges med <span class="codeph"> setCustomerIDs </span>-anropet när en person loggar in. Detta ID används också som nyckel i CRM-filen som överförs till Experience Cloud. Ett <a href="../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8" format="dita" scope="local"> alias-ID </a> är ett eget namn för ett datalager i Audience Manager, där aliasdata lagras. Systemet skickar alias till detta datalager (via setCustomerID:n). CRM-filen används på data i det datalagret. </p> <p>Mer information om <span class="codeph"> setCustomerIDs </span> finns i <a href="https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=en" format="https" scope="external"> Customer IDs and Authentication states </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Efterföljande rubriker och kolumner </p> </td> 
   <td colname="col2"> <p>Efterföljande rubriker ska representera namnet på varje attribut. </p> <p> Dessa kolumner ska innehålla kundattribut som kommer från CRM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attributgränser </p> </td> 
   <td colname="col2"> <p>Du kan överföra hundratals <span class="filepath"> .csv </span>-kolumner till kundattributstjänsten i Experience Cloud. När du konfigurerar prenumerationer och väljer attribut gäller dock följande begränsningar beroende på vilka lösningar du har: </p> <p> 
     <ul id="ul_2BB85067918D4BB3B59394F3E3E37A6D"> 
      <li id="li_93703988B9934384B4B94A839D028380"> <b>Analysstandard</b>: 3 totalt </li> 
      <li id="li_D1E5E7BD24C54591B14D15DE97447835"> <b>Analytics Premium</b>: 200 per rapportserie </li> 
      <li id="li_8C891FE3D1EF49FA9F81E2E32CD0B9CA"> <b>Adobe Target Standard:</b> 5 </li> 
      <li id="li_2B66D43023F34EA685CE2C38A9250CEA"> <b>Adobe Target Premium:</b> 200 </li> 
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
      <li id="li_B69A20C51D824727AA99C1F6F78537A4"> Du bör släppa filen <span class="filepath"> .csv </span> (och <span class="filepath"> .fin </span>) i FTP-platsens rotmapp. </li> 
     </ul> </p> <p> <p>Viktigt:  Det totala tillåtna utrymmet för FTP-kontot är 40 GB. Det är ditt ansvar att ta bort bearbetade filer. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Filkrav </p> </td> 
   <td colname="col2"> <p> Varje attributkälla ska innehålla samma antal kommaavgränsade fält. </p> <p> Fält som innehåller en radbrytning, dubbla citattecken eller kommatecken måste citeras. </p> <p> Dubbelcitattecken i ett fält måste föregås av ett omvänt snedstreck (\). </p> <p> Tomma kolumner lagras som <span class="term"> null </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Flera filer </p> </td> 
   <td colname="col2"> <p>När du överför kundattributdata, om du har flera filer som du vill överföra i snabb följd, och särskilt om filerna är stora, bör du kontrollera att den föregående filen har bearbetats innan du överför nästa fil. Du kan övervaka detta genom att kontrollera när den tidigare filen har flyttats till den bearbetade eller misslyckade mappen i FTP-kontot för [!UICONTROL Customer Attributes]. </p> <p> Att dela upp en stor fil i mindre filer och skicka in dem i snabb följd kan i själva verket göra bearbetningen långsammare, såvida du inte kan säkerställa att varje fil bearbetas innan du skickar in nästa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Teckenkodning </p> </td> 
   <td colname="col2"> <p>För Japan är UTF-8 obligatoriskt. </p> </td> 
  </tr> 
   <tr> 
   <td colname="col1"> <p>Historiska data </p> </td> 
   <td colname="col2"> <p> Kundattribut är knutna till den underliggande besökarprofilen i [!DNL Analytics]. Därför är [!UICONTROL-kundattribut] associerade med besökaren under hela besökarprofilens livstid i [!DNL Analytics]. Den här profilen innehåller beteenden som inträffade innan kunden loggade in för första gången. </p> <p> Om du använder metoden för bakåtfyllnad i Data warehouse är data knutna till en post_visid_high/low som är baserad på analys-ID (AID). Om du använder Experience Cloud ID-tjänsten är data knutna till en post_visid_high/low som är baserad på Experience Cloud ID (MID). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dataflöden </p> </td> 
   <td colname="col2"> <p>Kundattribut är inte tillgängliga i dataflöden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Använda flera datakällor {#section_76DEB6001C614F4DB8BCC3E5D05088CB}

När du skapar, ändrar eller tar bort kundattributskällor är det en fördröjning på ungefär en timme innan ID:n börjar synkronisera med den nya datakällan.

Alias-ID för varje kundattributkälla måste vara unikt. Om du har flera datakällor som använder samma ID kan de konfigureras på följande sätt:

**I VisitorAPI.js eller verktyget Experience Cloud ID i dynamisk tagghantering:**

Ange två kund-ID som motsvarar rätt datakällor:

```
Visitor.setCustomerIDs({ 
     "ds_id1”:"123456", 
     "ds_id2":"123456" 
});
```

(Mer information finns i [Kund-ID och autentiseringstillstånd](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=en).)

I **[!UICONTROL Experience Cloud]** > **[!UICONTROL People]** > **[!UICONTROL Customer Attributes]**:

Skapa två kundattribut med unika alias-ID:n som motsvarar kundens ID:n ovan. Med den här metoden kan samma referens-ID skickas till flera källor för kundattribut.
