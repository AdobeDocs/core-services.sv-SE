---
description: Läs mer om datafilskrav och flera datakällor för överföring av [!DNL customer attributes] till Experience Cloud.
solution: Experience Cloud
title: Datafil och datakällor
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: e2dfe10d-7003-4afa-a5e6-57703d74efd4
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '1144'
ht-degree: 0%

---

# Om datafil och datakällor för [!DNL customer attributes]

Datafilskrav och flera datakällor för överföring av [!DNL customer attributes] till Experience Cloud.

Du behöver åtkomst till CRM eller liknande data från ditt företag. De data som du överför till Experience Cloud måste vara en `.csv`-fil. Om du överför via FTP eller sFTP överför du även en `.fin`-fil.

[!DNL customer attributes] är utformat för att hantera några filer per dag. För att minimera problemet med att ha många små filer som försenar bearbetningen dirigeras filer som skickas inom 30 minuter från en tidigare batch från samma organisation till en kö med lägre prioritet.

## Tillåtna filtyper och namnkrav {#section_6F64FA02ACCC4215B0862CB6A1821FBF}

| Filtyp | Beskrivning |
|--- |--- |
| `.csv` | En fil med kommaavgränsade värden (till exempel en som skapats i Excel). Den här filen innehåller kundattributsdata.   Namngivningskrav: Kontrollera att filnamnstillägg inte innehåller blanksteg. |
| `.fin` | (Obligatoriskt) Filen `.fin` talar om för systemet att du är klar med överföringen av data. Namnet på filen `.fin` måste matcha namnet på filen `.csv`.  Adobe rekommenderar att du skapar en tom textfil med tillägget `.fin`. En tom fil sparar utrymme och laddningstid. **Obs!** Det går inte att ändra namn på en `.fin`-fil efter att den har överförts. `.fin`-filen måste överföras separat och kan inte ha bytt namn, tidigare överförd fil. När du har överfört filen `.fin` i kundattributen FTP hämtar systemet data snabbt (inom en minut). Detta skiljer sig från andra FTP-baserade Adobe-system, som hämtar in data mindre ofta (cirka en gång per timme). Filen `.fin` behövs inte när du använder överföringsmetoden dra och släpp. |
| `.gz` eller `.zip` | `.gz` (gzip) eller `.zip` - för komprimerade filer. En `.zip`-fil får inte innehålla mer än en fil i arkivet. Namngivningskrav: Namnet på `.zip` eller `.gz` ska matcha namnet på filen `.csv` . Om din `.csv`-fil till exempel är `crm_small.csv` ska `.zip`-filen vara `crm_small.csv.zip` . Filen `.fin` måste matcha filen `.csv`. |


## Krav för attributdatafiler {#section_169FBF5B7BBA47CE825B7A330CF3FE98}

**Exempel-CSV**

CSV-filen måste ha följande format:

![Krav för attributdatafilerna](assets/cvs.png)

Samma fil som visas i en textredigerare:

![Krav för attributdatafilerna](assets/csv_txt.png)

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
   <td colname="col2"> <p>Dra och släpp-filen bör vara mindre än 100 MB. </p> <p>Filen <span class="filepath"> .fin </span> behövs inte när du använder metoden för att dra och släppa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>kundens ID-kolumn </p> </td> 
   <td colname="col2"> <p> Den första kolumnen måste vara ett unikt kund-ID. Det ID som används ska motsvara det ID som skickas till Experience Cloud ID-tjänsten. </p> <p>För Analytics lagras ID:t i en propp eller eVar. </p> <p>Ange värdet för setCustomerID för Target. </p> <p> Detta kund-ID är den unika identifierare som CRM använder för varje person i din databas. De återstående kolumnerna är attribut som kommer från CRM. Du väljer hur många attribut du vill överföra. </p> <p>Ett läsbart namn rekommenderas för kolumnrubrikerna, men det behövs inte. När du validerar schemat efter överföring kan du mappa egna namn till överförda rader och kolumner. </p> <p> <b>Om kund-ID</b> </p> <p>Ett företag använder vanligtvis ett kund-ID från ett CRM-system. Detta ID anges med <span class="codeph"> setCustomerID:n </span> när en person loggar in. Detta ID används också som nyckel i CRM-filen som överförs till Experience Cloud. Ett <a href="t-crs-usecase.md" format="dita" scope="local"> alias-ID </a> är ett eget namn för ett datalager i Audience Manager, där aliasdata lagras. Systemet skickar alias till det här datalagret (via setCustomerID). CRM-filen används på data i det datalagret. </p> <p>Mer information om <span class="codeph"> setCustomerID:n </span> finns i <a href="https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html" format="https" scope="external"> Customer IDs and Authentication State (Kund-ID:n och autentiseringstillstånd) </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Efterföljande rubriker och kolumner </p> </td> 
   <td colname="col2"> <p>Efterföljande rubriker ska representera namnet på varje attribut. </p> <p> De här kolumnerna ska innehålla kundattribut som kommer från CRM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>attributgränser </p> </td> 
   <td colname="col2"> <p>Du kan överföra hundratals <span class="filepath"> .csv </span> -kolumner till kundattributtjänsten i Experience Cloud. När du konfigurerar prenumerationer och väljer attribut gäller dock följande begränsningar beroende på vilka program du äger: </p> <p> 
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
     </ul> </p> <p> <p>Viktigt: Det totala tillåtna utrymmet för FTP-kontot är 40 GB. Det är ditt ansvar att ta bort bearbetade filer. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Filkrav </p> </td> 
   <td colname="col2"> <p> Varje attributkälla ska innehålla samma antal kommaavgränsade fält. </p> <p> Fält som innehåller en radbrytning, dubbla citattecken eller kommatecken måste citeras. </p> <p> Dubbelcitattecken i ett fält måste föregås av ett omvänt snedstreck (\). </p> <p> Tomma kolumner lagras som <span class="term"> null </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Flera filer </p> </td> 
   <td colname="col2"> <p>När du överför kundattributdata, om du har flera filer som du vill överföra i snabb följd, och särskilt om filerna är stora, bör du kontrollera att den föregående filen har bearbetats innan du överför nästa fil. Du kan övervaka detta genom att kontrollera när den föregående filen har flyttats till den bearbetade eller misslyckade mappen i ditt [!UICONTROL customer attributes] FTP-konto. </p> <p> Att dela upp en stor fil i mindre filer och skicka in dem i snabb följd kan i själva verket göra bearbetningen långsammare, såvida du inte kan säkerställa att varje fil bearbetas innan du skickar in nästa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Teckenkodning </p> </td> 
   <td colname="col2"> <p>För Japan är UTF-8 obligatoriskt. </p> </td> 
  </tr> 
   <tr> 
   <td colname="col1"> <p>Historiska data </p> </td> 
   <td colname="col2"> <p> kundattribut är knutna till den underliggande besökarprofilen i [!DNL Analytics]. Därför är [!UICONTROL customer attributes] associerad med besökaren under hela besökarprofilens livstid i [!DNL Analytics]. Den här profilen innehåller beteenden som inträffade innan kunden loggade in för första gången. </p> <p> Om du använder Data Warehouse bakåtfyllningsmetod är data knutna till en post_visid_high/low som är baserad på analys-ID (AID). Om du använder Experience Cloud ID-tjänsten är data knutna till en post_visid_high/low som är baserad på Experience Cloud ID (MID). </p> <p> Observera att Data Warehouse bakåtfyllnadsmetod inte längre är tillgänglig från och med oktober 2022. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dataflöden </p> </td> 
   <td colname="col2"> <p>kundattribut är inte tillgängliga i dataflöden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Använda flera datakällor {#multiple}

När du skapar, ändrar eller tar bort kundattributskällor är det en fördröjning på ungefär en timme innan ID:n börjar synkronisera med den nya datakällan.

Alias-ID för varje kundattributkälla måste vara unikt. Om du har flera datakällor som använder samma ID kan de konfigureras på följande sätt:

**I VisitorAPI.js eller Experience Cloud ID-verktyget i dynamisk tagghantering:**

Ange två kund-ID som motsvarar rätt datakällor:

```
Visitor.setcustomerIDs({ 
     "ds_id1":"123456", 
     "ds_id2":"123456" 
});
```

(Mer information finns i [Kund-ID:n och autentiseringstillstånd](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html).)

I **[!UICONTROL Experience Cloud]** > **[!UICONTROL Customer Attributes]**:

Skapa två kundattributskällor med unika alias-ID:n som motsvarar kundens ID:n ovan. Med den här metoden kan samma referens-ID skickas till flera källor för kundattribut.
