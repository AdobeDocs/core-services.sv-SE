---
description: Funktioner, versionsinformation och kända fel för Experience Cloud-gränssnittet.
keywords: core services
seo-description: Funktioner, versionsinformation och kända fel för Experience Cloud-gränssnittet.
seo-title: Ackumulerade versionsinformation
solution: Experience Cloud
title: Ackumulerade versionsinformation
uuid: fcff8cc6-e587-4bf2-9a75-261d4eabc7d4
translation-type: tm+mt
source-git-commit: 12c3ac8bfa64b7c8708312576ac6dc4036c1b7d8

---


# Ackumulerade versionsinformation

Funktioner, versionsinformation och kända fel för Experience Cloud-gränssnittet.

En lista över dokumentationsuppdateringar finns i [Experience Cloud](../doc-updates.md#concept_4C8983FCD23848A4B1E4C2D99ED82784).

Versionsinformation om alla lösningar finns i Versionsinformation om [Experience Cloud](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html).

## Januari-2020

* Feed-sidan togs bort i december 2019. Leta efter ett meddelande om borttagning av produkter. (MCUI-10039)

## Augusti-2019

* Ett kritiskt problem med Experience Cloud-inloggning som ledde till sessionsutloggning för vissa användare har korrigerats. (MCUI-6908)
* Experience Cloud-inloggning har uppdaterats för att förbättra prestanda och minska latensen. (MCUI-6854, MCUI-6869, MCUI-6883)
* Uppdaterat gränssnitt kosmetiskt. (MCUI-6861, MCUI-6911, MCUI-6862)
* Korrigerade ett problem med Experience Cloud [!UICONTROL Triggers] som ledde till felaktig tolkning av _Gilla_ -satsen i [!UICONTROL Trigger] definitionen. (MCUI-6611)

## April-2019

* Appväljaren har uppdaterats för att inkludera Marketo i Experience Cloud-lösningssviten och varumärkesuppdateringar i Experience Platform. (MCUI-6529)
* Experience Cloud Home har uppdaterats för att inkludera navigeringslänkar till sidorna Feed och Administration. (MCUI-6682)
* Korrigerade ett fel i [!UICONTROL Trigger] definitionen för korrekt användning av gilla-satsen. (MCUI-6611)
* Förbättringar av kundattribut för bättre inloggning i prenumerationstjänsten. (MCUI-6519)

## Version 19.1.1 - 17 januari 2019

**Obs!** I mars 2019 kommer Experience Cloud-gränssnittet inte att ha stöd för Internet Explorer 11.

* Ett problem som hindrade hjälpsökningen från att returnera resultat har åtgärdats. (MCUI-1670)
* Korrigerad och förbättrad eVar-hantering i utlösare. (MCUI-6400)

## Version 16.5.1 - 26 maj 2016 {#section_3785F182BC13493F84903CA69EB6D0A8}

**Funktioner och förbättringar**

<table id="table_ABBCE1A66F534059BD728BC2B9AEFA80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Förkonfigurerade produktkonfigurationer i Admin Console </p> </td> 
   <td colname="col2"> <p>Experience Cloud-kundadministratörer kan utnyttja produktkonfigurationer som är färdiga och mappade till standardbehörighetsgrupper för Analytics och Dynamic Tag Management. </p> <p>Den här optimeringen är tillgänglig för nyligen etablerade organisationer och minskar den tid som organisationer behöver för att hantera användare på Admin Console. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Förbättrad feed </p> </td> 
   <td colname="col2"> <p> När du skapar ett nytt inlägg i Experience Cloud Feed använder raden Till nu det aktiva ämnet i stället för att använda organisationen som standard.</p> </td> 
  </tr> 
 </tbody> 
</table>

**Korrigeringar**

* Ett problem som förhindrar att miniatyrbilder visas för resurser som delas från Assets on Demand till Experience Cloud Feed har åtgärdats. (MAC-29955)

## Utgåva 16.2 februari 18 2016 {#section_D9610373116C4D77A38F67815C725EA3}

<table id="table_C9B288CF42034F329C3C72D95D22E515"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Förbättringar av Experience Cloud Assets </p> </td> 
   <td colname="col2"> <p>I Experience Cloud Assets kan ni lagra, dela och synkronisera era era digitala resurser från en central plats. Experience Cloud Assets utnyttjar några av funktionerna i <span class="keyword"> Adobe Experience Manager</span> (AEM). </p> <p>Se <a href="../experience-cloud-assets/experience-cloud-assets.md#concept_DDA5224C907D4A4F817D795DA0ED64D0" format="dita" scope="local"> Experience Cloud</a></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Förbättringar av kontolänkning </p> </td> 
   <td colname="col2"> <p>Förbättrat gränssnittsarbetsflöde för länkning av lösningskonton med Experience Cloud (Adobe ID). Det nya arbetsflödet hittar alla användarkonton som är kopplade till en organisation och låter dig välja vilket konto som ska länkas. Vi effektiviserade även kontolänkningen så att du inte längre behöver komma åt sidan Hantera organisationer för att manuellt länka konton. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Korrigeringar**

* Ett problem som förhindrar länkning och enkel inloggning för analys har korrigerats. Det här problemet innehöll meddelandet&quot;Meddelande: Felmeddelandet: FEL: IMS SSO misslyckades: Det gick inte att hitta det länkade företaget.&quot;

**Känt fel**

Om du använder Dynamic Tag Management via **[!UICONTROL Experience Cloud]** >- **[!UICONTROL Activation]** gränssnittet, men ditt Dynamic Tag Management-konto inte är länkat till Experience Cloud (Adobe ID), kan du inte logga in på Dynamic Tag Management. Du undviker det här problemet genom att navigera direkt till [!DNL dtm.adobe.com] på en ny webbläsarflik.

## Version 16.1 - 21 januari 2016 {#section_33B3F7DF6CA347E3AA93801BAC6232CE}

<table id="table_4223658257DA41C999AC710A10D26771"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Målgruppsmeddelanden </td> 
   <td colname="col2"> <p> Vi har förbättrat målgruppsbiblioteket så att det innehåller användbara meddelanden när målgrupper byggs eller när en timeout inträffar. </p> <p>Om du till exempel lägger till fler än fem regler visas ett meddelande som anger att du har överskridit de högsta tillåtna reglerna. (MAC-27376, MAC-27375) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Microsoft [upphör med stödet](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) för Internet Explorer 8, 9 och 10. Därför kommer vi inte att åtgärda problem som rapporteras mot dessa specifika versioner av Internet Explorer.

## Version 15.10 - 14 oktober 2015 {#section_68123833D3634BD3A473C12862BF9606}

**Kända fel**

* Kunderna kan inte logga in i Report Builder om de har enkel inloggning på Analytics via Experience Cloud. Problemet påverkar inte kunder som använder äldre inloggningsuppgifter för Analytics.
* Känt problem med funktionen Länka till rapport i Analytics. Kunder som loggar in på Analytics via Experience Cloud dirigeras till en icke-SSO-inloggningssida för Analytics när de försöker dela en rapport.

## Version 15.9 - 10 september 2015 {#section_BCCE3E7DF62A4FF5A57B9C8FE2A5F37B}

* Korrigerade ett prestandaproblem i Audience Manager API som orsakade intermittenta timeout vid överföring av kundattributdata. (MAC-26305)
* Ett problem som gjorde att användare inte kunde lägga till upp till 200 kundattribut i en prenumeration har åtgärdats. (MAC-26188)
* Korrigerade ett problem med målgruppsbiblioteket som förhindrade målgruppsdelning från Analytics-segmentering. Detta orsakade att&quot;Collecting Data&quot; (0 målgrupper) visades. För att förhindra detta rekommenderar Adobe att segmentstorlekarna hålls under 50 000 publiken per segment. (MAC-25788)
* Korrigerade ett tidigare känt fel på sidan Kundattribut - Redigera schema som orsakade ett innehållsmedvetet fel som utfärdades när ett visningsnamn ändrades. (MAC-25589, AN-103834)

## Version 15.7 - 22 juli 2015 {#section_2683A152176944E48EF6C943892975B7}

* Ett problem har korrigerats som förhindrade att attributbeskrivningar som anges på sidan Visa/redigera schema (i kundattribut) uppdaterades i analysrapporter. (MAC-25985)
* Ett problem som hindrade miniatyrbilderna från att rendera överförda resurser har åtgärdats. (MAC-25863)
* Korrigerade ett problem som förhindrade att nya segment som skapats i rapporter och analyser fanns tillgängliga i Experience Cloud-målgrupper. (MAC-25817)
* Korrigerade ett problem som förhindrade målgruppsdelning från Analytics när besökar-ID-tjänsten användes. (MAC-25788, MAC-25747)
* Stöd för flerbytetecken i kundattribut har lagts till. (MAC-25552)

**Känt fel**

Ett känt fel gör att duplicerade autogenererade konton skapas i Audience Manager och automatiskt länkas till en användares Experience Cloud-identitet. Det här problemet uppstår om du försöker navigera till Audience Manager innan du länkar dina konton. Adobe rekommenderar att du länkar dina Audience Manager-konton till Experience Cloud innan du navigerar till Audience Manager. (MAC-25640)

## Version 15.6.1 - 11 juni 2015 {#section_AD2019F8D2F84C9EB2B0533FAACF7043}

Ingen information finns tillgänglig

## Version 15.5.1 - 13 maj 2015 {#section_EF197410964E40D294D0D8024738CFBA}

<table id="table_14E7B35E06C84A258A21D09691B58354"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>De vänstra navigeringsmenyerna har uppdaterats och ordnats för att ge tillgång till alla bastjänster och lösningar. Viktiga ändringar: </p> 
    <ul id="ul_5BEBAB86B9234A239C4E2DAF8826D8E3"> 
     <li id="li_7FA9F64CE69144B8A8A92746BF40E5A1">Menyvalen <span class="term"> Audience Library</span> och <span class="term"> Customer Attributes</span> finns nu under <span class="term"> Audiences</span>. </li> 
     <li id="li_95D62A43AE6243DBB2A65EDB830D05C4">Menyvalet <span class="term"> Exchange</span> har flyttats från den nedrullningsbara menyn Hjälp till den vänstra navigeringslisten. </li> 
     <li id="li_0443FD50C78446CD8AA27A4F272CAD31"> <span class="term"> Lösningarna</span> har tagits bort. Du kan starta alla lösningar från den nedre halvan av navigeringslisten. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

* Ett problem som förhindrar att kundattribut synkroniseras för vissa kunder har åtgärdats.
* Ett problem som gjorde att [Adobe Target-produktdokumentationssidan](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t.html) inte kunde visas på japanska har korrigerats.
* Ett problem som förhindrade användning av japansk text i kommentarer mellan [!DNL Creative Cloud] och [!DNL Experience Cloud]har korrigerats.

## Version 15.4.1-8 april 2015 {#section_75634120CC934B3381EDEA7F6F976F0A}

<table id="table_3A6FBAE36558425A803B078150862C92"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Administrationsförbättringar: </p> 
    <ul id="ul_7D5FCBEFA262435D865CA1018BFB792E"> 
     <li id="li_6E98974CCB094ABBAB57C51ED56C3F00"> <span class="wintitle"> Admin Console</span> </li> 
     <li id="li_8CDAB6301FD44C3999EE4EEB1A0A2FD6">Stöd för Enterprise ID och Federated ID </li> 
    </ul> </td> 
   <td colname="col2"> <p>Funktionen för användar- och grupphantering har flyttats till Admin Console. Den nya navigeringssökvägen är: </p> <p> <span class="uicontrol"> Experience Cloud</span> &gt; <span class="uicontrol"> Administration</span> &gt; <span class="uicontrol"> Starta Admin Console</span></p> <p> Stöd för Enterprise ID och Federated ID har lagts till. Du kan använda Enterprise ID:n, Federated ID:n och Adobe ID:n i samma företagsdistribution. Använd till exempel Adobe ID:n för användare som kan använda andra Adobe-produkter och -tjänster. Använd Enterprise ID eller Federated ID för användare där du vill hantera deras konton strikt. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Korrigeringar**

* Ett problem som förhindrar enkel inloggning mellan [!DNL Experience Cloud] och [!DNL Media Optimizer]har korrigerats.

**Kända fel**

* Det går inte att länka och bryta länken mellan en dynamisk tagghanteringsorganisation och Experience Cloud för nyligen skapade Experience Cloud-organisationer. Vi arbetar med att åtgärda detta och återställa normal funktionalitet med majversionen. Om du får problem med att logga in på dynamisk tagghantering via Experience Cloud kan du använda den äldre inloggningen på [!DNL dtm.adobe.com].
* Ett känt problem är att förhindra målgruppsdelning från rapportsviter som inte ägs av det länkade Analytics-kontot. Saneringsarbetet pågår

## Version 15.3.2 - 19 mars 2015 {#section_07760FD9CA43497FA8BDCCA990A24BFD}

<table id="table_54025DBE2D094FF1BE837BA60816C6DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Kundattribut </p> </td> 
   <td colname="col2"> <p>Om du samlar in företagsdata i en CRM-databas (customer relationship management) kan du överföra data till en datakälla för kundattribut i Experience Cloud. När data har överförts kan du köra rapporter om <span class="uicontrol"> besöksprofil</span> &gt; <span class="uicontrol"> Kundattribut</span> i Analytics. </p> <p>Du kan också använda de överförda data som ett målgruppssegment i <span class="keyword"> Adobe Target</span>. </p> <p>Se <a href="../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1" format="dita" scope="local"> Kundattribut</a> - produktdokumentation. </p> <p> Mer information om hur du moderniserar dina lösningar för bastjänster finns i <a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local"> Aktivera dina lösningar för bastjänster</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 15.3.1 - 4 mars 2015 {#section_57CB69C044DD47BDBC1A1BEC38957551}

<table id="table_EB3FFBA2DF904546A5185EC9A63BBA98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gruppmappning </p> </td> 
   <td colname="col2"> <p>Sidan Grupphantering har fått en ny design som ett administrativt gränssnitt där du kan skapa grupper, lägga till användare i grupper och tillämpa behörigheter i alla Experience Cloud-lösningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1:N-mappning </p> </td> 
   <td colname="col2"> <p>När du länkar lösningskonton i Experience Cloud kan du, om du har flera lösningar och organisationer, mappa flera produkter och tjänster till en enda organisation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aktivering </p> </td> 
   <td colname="col2"> <p> <a href="../activation/activation.md#concept_EE756B6B0A0643DAB8CA3A00E665406C" format="dita" scope="local"> Aktiveringen</a> visas nu i den vänstra navigeringen i <span class="keyword"> Experience Cloud</span>. <span class="wintitle"> Aktivering</span> är en <span class="keyword"> Experience Cloud</span> -bastjänst som för närvarande består av den dynamiska tagghanteringstekniken och dirigerar dig dit när du klickar på den. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dokumentationsuppdateringar - bastjänster </p> </td> 
   <td colname="col2"> <p>Avsnittet <a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local"> Enable your solutions for core services</a> to help you with implement core services har lagts till. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Version 15.2.1 - 19 februari 2015 {#section_BC694D5AE16A4E16B44B353ED67947F3}

Korrigeringar:

* Förbättrat arbetsflöde för användarens e-postinbjudan för kontoetablering.
* Korrigerade ett problem med resursmappen som förhindrar [!DNL Experience Cloud] och [!DNL Adobe Campaign] att resurser visar identiska mapphierarkier.
* Ett problem som förhindrar att målgrupper som var en del av inaktiverade [!DNL Target] aktiviteter tas bort har åtgärdats.
* Ett problem som gjorde att ikonen Lägg till (plus) inte kunde visas under [!UICONTROL Rules] på [!UICONTROL Create New Audience] sidan har åtgärdats.
* Förbättrat stöd för Experience Cloud-gränssnitt i Internet Explorer 9.

## Version 15.1.1 - 15 januari 2015 {#section_F1A352E928AF432E94CC0A289C345184}

Nya funktioner och korrigeringar i samarbets- och delningsgränssnittet [!DNL Adobe Experience Cloud] .

<table id="table_AD0A8CA760E64227BB04BA6B0E425E80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Skrivskyddad åtkomst. </p> </td> 
   <td colname="col2"> <p>Administratörer kan nu ge icke-administrativa användare skrivskyddad åtkomst. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Korrigeringar**

* Korrigerade ett problem där PNG-filer inte kunde återges på ett kort.
* Ett problem med att överföra filer till Experience Cloud Assets via dra och släpp har korrigerats.

**Kända fel**

* Användare kan inte dela PowerPoint-filer på ritytor.
* Ändringar av grupper och tillstånd som görs i användarhantering börjar gälla först efter en ny inloggning.
* Vissa användare kan ha problem med att överföra stora filtyper till Experience Cloud Assets.
* Användare kanske saknar länkar på sina Experience Cloud-kort från Media Optimizer.
* Vissa administrativa användare kan få problem med att länka sina konton efter att ha accepterat en inbjudan att gå med i Experience Cloud.
* Experience Cloud-gränssnittet kan minska prestandan när flera användare använder det parallellt.
* Vissa användare kan ta bort en inaktuell resurs i stället för att få ett felmeddelande.
* Vissa användare kan få problem med att logga in i två webbläsare med samma Adobe-id samtidigt.
* Vissa användare kanske inte kan lägga till en Creative Cloud-användare på nytt i en delad mapp efter att Creative Cloud-användaren har tagits bort.
* Vissa användare kan få en fördröjning i meddelandet som inträffar när en mapp delas från Experience Cloud till Creative Cloud.
* Vissa användare kan ha problem med att dela en mapp mellan Experience Cloud och Creative Cloud.
* Vissa användare kan ha problem med att skapa en målgrupp i en Analytics-rapportsserie när delade målgrupper har aktiverats.
* Vissa användare kan ha problem med att överföra resurser till en styrelse.

## Version 14.11.1 - 13 november 2014 {#section_A6CF1D4F27B9496892A89C983EB39102}

Kända fel:

* Vissa användare kan ta bort en inaktuell resurs i stället för att få ett felmeddelande.
* Vissa [!DNL .png] filer kan inte återges på ett kort.
* Vissa användare kan ha problem med att överföra resurser till en styrelse.
* Ändringar av grupper och tillstånd som görs i användarhantering börjar gälla först efter en ny inloggning.
* Administratörer måste logga ut och in igen för att se ändringar som gjorts i kontoinställningarna.
* Användaren kan inte dela PowerPoint-filer på ritytor.
* [!DNL Experience Cloud] -gränssnittet kan minska prestandan när det används parallellt av många användare.
* Synkroniseringen mellan Adobe Experience Manager och Creative Cloud fungerar inte.

## Version 14.10.1 - 16 oktober 2014 {#section_E3A0F4423B814707AA3745E083500835}

Nya funktioner och korrigeringar i samarbets- och delningsgränssnittet [!DNL Adobe Experience Cloud] .

<table id="table_7C1ACE8108D54782AE128ACD35069DF5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Redigera användarbehörigheter </p> </td> 
   <td colname="col2"> <p>Styrelsemedlemmar kan nu redigera användarbehörigheter på den aktuella ritytan. </p> <p> 
     <ol id="ol_B12251C510744538AF9BCE60ACB04016"> 
      <li id="li_87B3EDE9542B47CEBE0BE7F2D1DE844D">Klicka på <span class="uicontrol"> Inställningar</span>. </li> 
      <li id="li_0F4786B0E1E743069D082E7DC488A031">Ange <span class="uicontrol"> Ägare</span>, <span class="uicontrol"> Visningsprogram</span>eller <span class="uicontrol"> Redigerare</span>bredvid varje ägare. </li> 
     </ol> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Korrigeringar**

* Ett felmeddelande returnerades när ett kort skapades från en PDF-fil och delades till styrelsen.

**Kända fel**

* Vissa användare kan ha problem med att överföra resurser till en styrelse.
* Vissa [!DNL .png] filer kan inte återges på ett kort.
* Ändringar av grupper och tillstånd som görs i användarhantering börjar gälla först efter en ny inloggning.
* Vissa användare kanske inte kan skapa ett kort från en PDF-fil och dela det med en anslagstavla.
* Vissa användare kan ta bort en inaktuell resurs i stället för att få ett felmeddelande.
* Användaren kan inte dela PowerPoint-filer på ritytor.
* [!DNL Experience Cloud] -gränssnittet kan minska prestandan när det används parallellt av många användare.
* Länkningen [!DNL Search&Promote] är inte tillgänglig från [!UICONTROL Organizations & Product Access] sidan.

## Version 14.9.1 - 18 september 2014 {#section_20F156A9CC2F4FC59C4970075C181D3A}

**Korrigeringar och förbättringar**

* När du navigerar till [!DNL experiencecloud.adobe.com]är inloggningsupplevelsen i linje med Adobe Creative Cloud-inloggningen.
* På sidan Hantera organisationer är länkningen (efter att en inbjudan har tagits emot) nu konsekvent för varje lösning.

**Kända fel**

* Ändringar av grupper och tillstånd som görs i användarhantering börjar gälla först efter en ny inloggning.
* Vissa användare kanske inte kan skapa ett kort från en PDF-fil och dela det med en anslagstavla.
* Vissa användare kan ha problem med att överföra resurser till en styrelse.
* Vissa användare kan ta bort en inaktuell resurs i stället för att få ett felmeddelande.
* Användaren kan inte dela PowerPoint-filer på ritytor.
* Vissa [!DNL .png] filer kan inte återges på ett kort.
* [!DNL Experience Cloud] -gränssnittet kan minska prestandan när det används parallellt av många användare.
* Länkningen [!DNL Search&Promote] är inte tillgänglig från [!UICONTROL Organizations & Product Access] sidan.
* Vissa användare kan uppleva att deras [!DNL Creative Cloud] innehåll tas bort från deras mapp om innehållet inte delas i [!DNL Experience Cloud].

## Version 14.8.1 - 21 augusti 2014 {#section_03BF00F6A95A490C91BCC0A1988FA7AA}

Nya funktioner och korrigeringar i samarbets- och delningsgränssnittet [!DNL Adobe Experience Cloud] .

<table id="table_1E7DBEB5E83B4E4285B6FD1D718CD16D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>Nu kan du komma åt <span class="keyword"> Adobe Mobile Services</span> via den vänstra navigeringen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Kända fel**

* Ändringar av grupper och tillstånd som görs i användarhantering börjar gälla först efter en ny inloggning.
* Vissa användare kanske inte kan skapa ett kort från en PDF-fil och dela det med en anslagstavla.
* Vissa användare kan ha problem med att överföra resurser till en styrelse.
* Vissa användare kanske inte kan logga in från [!DNL Target] till [!DNL Experience Cloud].
* Vissa Audience Manager-användare kan inte logga in i [!DNL Experience Cloud].
* Vissa användare kan ta bort en inaktuell resurs i stället för att få ett felmeddelande.
* Filer som tas bort från [!DNL Experience Cloud] tas inte bort från [!DNL Digital Asset Management].
* Användaren kan inte dela PowerPoint-filer på ritytor.
* Vissa [!DNL .png] filer kan inte återges på ett kort.
* [!DNL Experience Cloud] -gränssnittet kan minska prestandan när det används parallellt av många användare.
* Länkningen [!DNL Search&Promote] är inte tillgänglig från [!UICONTROL Organizations & Product Access] sidan.
* Vissa användare kan uppleva att deras [!DNL Creative Cloud] innehåll tas bort från deras mapp om innehållet inte delas i [!DNL Experience Cloud].

## Version 14.7.1 - 24 juli 2014 {#section_B22D4F830756463DB27BB4D508D9ADD5}

Nya funktioner och korrigeringar i samarbets- och delningsgränssnittet [!DNL Adobe Experience Cloud] .

**Kända fel**

* Filer som tas bort från [!DNL Experience Cloud] tas inte bort från [!DNL Digital Asset Management].
* Vissa [!UICONTROL Exchange] användare kan se sina namn i kommentarerna som ett långt sträng-ID i stället för deras namn
* Vissa [!DNL .png] filer kan inte återges på ett kort
* Att överföra filer ger fler filtyper än att dra och släppa. För bästa resultat ska du överföra med [!UICONTROL Assets].
* Länkningen [!DNL Search&Promote] är inte tillgänglig från [!UICONTROL Organizations & Product Access] sidan.
* [!DNL Exchange] -användare måste rensa sina cookies för att förbättra sin upplevelse.
* [!DNL Experience Cloud] gränssnitt kan göra det långsammare när det används parallellt av många användare.
* Vissa användare kan uppleva att deras [!DNL Creative Cloud] innehåll tas bort från deras mapp om innehållet inte delas i [!DNL Experience Cloud].
* Du loggas ut efter 15 minuters inaktivitet. Om du loggar ut från en plats loggas du ut från [!DNL Experience Cloud].
* Vissa användare kanske inte kan länka sina Audience Manager-konton till [!DNL Experience Cloud].
* [!UICONTROL Exchange] -användare kan bara se engelska i språkväljaren.

**Korrigeringar**

Ingen att rapportera.

## Version 14.6.1 - 19 juni 2014 {#marketing_cloud_interface}

Nya funktioner och korrigeringar i samarbets- och delningsgränssnittet [!DNL Adobe Experience Cloud] .

**Förbättring**

<table id="table_C9BD63436BF0414B97B8D07387D1993B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> Knappen Spara</span> i publiker </p> </td> 
   <td colname="col2"> <p>När du skapar en målgrupp är knappen <span class="wintitle"> Spara</span> på sidan <span class="wintitle"> Skapa ny publik</span> nu inaktiverad tills alla obligatoriska fält har fyllts i. 
     <!--MAC-19712 --></p> </td> 
  </tr> 
 </tbody> 
</table>

**Kända fel**

* Filer som tas bort från [!DNL Experience Cloud] tas inte bort från [!DNL Digital Asset Management].
* Att överföra filer ger fler filtyper än att dra och släppa. För bästa resultat ska du överföra med Assets.
* Länkningen [!DNL Search&Promote] är inte tillgänglig från [!UICONTROL Organizations & Product Access] sidan.
* Filter som används på trendrapporter från [!DNL Analytics] används inte på kort i [!DNL Experience Cloud].
* Vissa användare kan inte länka sina målgruppshanteringskonton till sina [!DNL Experience Cloud] konton.
* Du loggas ut efter 15 minuters inaktivitet. Om du loggar ut från en plats loggas du ut från Experience Cloud.
* Vissa Exchange-användare kan se att deras namn i kommentarerna är ett långt sträng-ID i stället för deras namn

**Korrigeringar**

* Korrigerade ett problem som förhindrade videoöverföring till appar.

## Version 14.5.1 - 22 maj 2014 {#section_7E22B2CB3ABA4D6EAED8CA8EFDE5433E}

<table id="table_4E4B34EEE3D94D78BA1A1FBC62950559"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud Exchange </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Experience Cloud</span> &gt; <span class="uicontrol"> Hjälp</span> &gt; <span class="uicontrol"> Exchange</span></p> <p>Experience Cloud <span class="keyword"> Exchange</span><span class="wintitle"></span> är ett enda mål där du kan söka efter, bläddra bland, välja ut, betala och hämta tillägg för digital marknadsföring via appar. </p> <p>Apparna innehåller dataanslutningar, anpassade konfigurationer av Adobes huvudprodukt, program från tredje part, rapporter och <span class="keyword"> Experience Cloud</span> -kort. </p> <p>Se <a href="../exchange.md#concept_E07F16F070544B82B56527A845C41D59" format="dita" scope="local"> Exchange Marketplace</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud-målgrupper </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Experience Cloud</span> &gt; <span class="uicontrol"> Publiker</span></p> <p> <span class="wintitle"> Målgrupperna</span> är där ni skapar, redigerar och hanterar målgrupper, ungefär som hur ni arbetar med segment. Du kan till exempel skapa ett segment i rapporter och analyser och sedan dela det med <span class="wintitle"> Experience Cloud</span><span class="wintitle"> -målgrupper</span>. När målgruppen har delats är den tillgänglig i <span class="keyword"> Adobe Target</span> för kampanjaktiviteter och i Adobe Audience Manager för segmentering. </p> <p> <p>Obs! Om du vill begära aktivering i Target går du till <a href="https://www.adobe.com/go/audiences" format="http" scope="external"> https://www.adobe.com/go/audiences</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>Användare som nämns på <span class="keyword"> Experience Cloud</span> -kort har nu behörighet för det kortet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>Nya Adobe-användare kan länka sina Scene7-konton till Adobe ID och till sina teammedlemmar. Administratörer kan även bryta länken till användare från Scene7-konton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Resurssynkronisering. </p> </td> 
   <td colname="col2"> <p> Du kan dela resurser i Adobe Experience Manager-resurser (AEM) med Adobe Experience Cloud och Adobe Creative Cloud så att ändringar av dessa resurser återspeglas i de delade kopiorna av resurserna i Adobe Experience Cloud och Adobe Creative Cloud. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Korrigeringar**

* [!DNL Experience Cloud] länkades inte till [!DNL Adobe Target]. Detta problem uppstod om inloggningen [!DNL Adobe Target] kan användas på flera [!DNL Target] servrar.
* [!DNL Adobe Media Optimizer] skapar inte användare automatiskt när användaren har skapats i [!DNL Experience Cloud].
* Alternativ i kombinationsrutor som används för att lägga till nya användare försvinner tillfälligt när du skriver.
* Det gick inte att klicka på kommentarlänken i resurskortvyn.
* När du har lagt till en anpassad tagg i en resurs, bevaras inga andra metadataändringar.
* När du tar bort en bild visas ingen varning om bilden används i Adobe Target Essentials.
* Långsam [!UICONTROL Experience Cloud] gränssnittsprestanda vid parallell användning av många användare.
* När du tog bort en bild i [!UICONTROL Experience Cloud Assets] utlöstes ingen varning om bilden användes i [!DNL Adobe Target Essentials].
* När användaren inte **[!UICONTROL remember me]** valdes under inloggningen loggades användaren ut efter 15 minuter.
* Användarna var tvungna att logga ut och in igen för att alla ändringar i behörighet och tillstånd skulle börja gälla.
* Det [!DNL Experience Cloud] tog längre tid än en sekund att logga in.
* För vissa användare synkroniserades inte filer som togs bort från [!DNL Experience Cloud] med [!DNL Digital Asset Management].
* Användare loggades ut efter endast 15 minuters inaktivitet i webbläsaren.
* Användaren kunde inte dela PowerPoint-filer på ritytor.
* Vissa användare upplevde en dålig visuell layout i Internet Explorer 10 jämfört med andra webbläsare.

## Version 14.4.1 - 22 april 2014 {#section_E2A699764E744D2E8D418E9A3D40AF6B}

<table id="table_D95C0DC64F2A4B47BAC83E504CFD6825"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Skapa kort från hjälpavsnitt </p> </td> 
   <td colname="col2"> <p>När du har aktiverat funktionen Dela till Adobe Experience Cloud i webbläsarens bokmärkesverktygsfält kan du nu dela hjälpsidor från mikrowebbplatsens URL. </p> <p> <b>Dela ett hjälpavsnitt</b> </p> 
    <ol id="ol_F94B816121494B0FA16CC07B0E96AED8"> 
     <li id="li_F47187D4B5FE46D3A51D257DD569B4D6"> <p>Klicka på <span class="keyword"> Administration</span>i <span class="uicontrol"> Experience Cloud</span>. </p> </li> 
     <li id="li_94EF58E7A4974B63951E14F72A710183"> <p>Dra knappen <span class="uicontrol"> Dela till Adobe Experience Cloud</span> till bokmärkets verktygsfält. </p> </li> 
     <li id="li_69EEC4F25D8F4AD7AA106A10B7F50FF6"> <p>Navigera till en hjälpsida (eller stanna kvar på den här) och klicka sedan på <span class="uicontrol"> Dela till Adobe Experience Cloud</span> i webbläsarens bokmärkesverktygsfält. </p> <p>I det här steget skapas ett kort som du kan visa i <span class="wintitle"> Experience Cloud</span>. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

**Korrigeringar**

* När du har lagt till en anpassad tagg i en resurs kan inga andra metadataändringar sparas.
* Användarna måste uppdatera anslagstavlan för att ta bort de raderade korten.
* När **[!UICONTROL Remember me]** inte har valts under inloggningen loggas användaren ut efter 15 minuter
* [!DNL Analytics] på startsidan för lösningen visas formateringsfel.
* Användarna måste logga ut och logga in igen för att alla ändringar i behörighet och tillstånd ska börja gälla.
* När du tar bort en bild visas [!UICONTROL Assets] ingen varning om bilden används i [!DNL Adobe Target Essentials].
* Det går inte att klicka på kommentarlänken i resurskortvyn.
* Alternativ i kombinationsrutor för att lägga till nya användare försvinner tillfälligt när du skriver.
* Inloggning till [!DNL Experience Cloud] tar längre tid än en sekund.
* Data som delas från [!DNL Media Optimizer] är felrepresenterade i [!DNL Experience Cloud].
* Adobe skapar [!DNL Media Optimizer] inte användare automatiskt när användare har skapats i [!DNL Experience Cloud].
* Det [!DNL Experience Cloud] går inte att länka till [!DNL Adobe Target]om [!DNL Adobe Target] inloggningen kan användas på flera [!DNL Target] servrar.
* [!DNL Experience Cloud] gränssnitt kan göra det långsammare när det används parallellt av många användare.
* [!DNL Search&Promote] Det går inte att länka från [!UICONTROL Organizations & Product Access] sidan.
* [!DNL Adobe Media Optimizer] simuleringskort återges inte korrekt.
* Filter som används på trendrapporter från [!DNL Analytics] används inte på kort i [!DNL Experience Cloud].
* Filter som tillämpas på trendrapporter från Analytics tillämpas inte på kort i Experience Cloud.
* Vissa Excel- eller CSV-filer kan inte överföras till en anslagstavla.
* Vissa användare kanske inte kan länka sina målgruppshanteringskonton till sina [!DNL Experience Cloud].
* Vissa användare kan råka ut för fel när de delar [!DNL Analytics] segment i [!DNL Experience Cloud].
* Vissa användare kanske inte kan gå ned i undermappar i [!UICONTROL Asset Selector].
* Vissa användare kan inte dela AdLens-gadgets i [!DNL Experience Cloud].

## Version 14.3.1 - 13 mars 2014 {#section_5D142E3225E3477A84DC01B8197D39BC}

Version 14.3.1 är en underhållsrelease som fokuserar på hastighet, stabilitet och säkerhet. Den innehåller inga viktiga nya funktioner.

**Korrigeringar**

* Lagt till möjlighet att ta bort din avatarbild.
* Ett problem som hindrade dig från att bryta länken till dina [!DNL Adobe Media Optimizer] konton har korrigerats.

**Kända fel**

* Om du tar bort en bild i Experience Cloud Resurser visas ingen varning om bilden används i Adobe Target Essentials.
* Om du uppdaterar ett kort från [!DNL Analytics] kan det ibland leda till att ett tomt diagram visas på det utökade kortet.
* Användarna måste logga ut och logga in igen för att alla ändringar i behörighet och tillstånd ska börja gälla.
* När *`Remember me`* inte har valts under inloggningen loggas användaren ut efter 15 minuter.
* [!DNL Analytics] på startsidan för lösningen visas formateringsfel.
* Länken Kommentarer i resurskortvyn går inte att klicka på.
* Experience Cloud-gränssnittet kan göra det långsammare när många användare använder det parallellt
* Experience Cloud kan inte länkas till [!DNL Adobe Target]om [!DNL Adobe Target] inloggningen kan användas på flera målservrar.
* Det tar längre tid än en sekund att logga in på Experience Cloud.
* När du har lagt till en anpassad tagg i en resurs kan inga andra metadataändringar sparas.
* [!DNL Adobe Media Optimizer] skapar inte användare automatiskt i när användare har skapats i Experience Cloud.
* Alternativ i kombinationsrutor för att lägga till nya användare försvinner tillfälligt när du skriver.
* Data som delas från [!DNL Media Optimizer] är felaktigt representerade i Experience Cloud.
* Det går inte att dela Flickr-bilder.
* Filter som tillämpas på trendrapporter från [!DNL Analytics] tillämpas inte på kort i Experience Cloud.
* Ändringar av grupper och tillstånd som görs i användarhantering börjar gälla först efter en ny inloggning.
* [!DNL Search&Promote] Det går inte att länka från [!UICONTROL Organizations & Product Access].
* Användaren måste uppdatera anslagstavlan för att ta bort de borttagna korten från vyn.
* Vissa Excel- eller CSV-filer kan inte överföras till en anslagstavla.
* [!DNL Adobe Media Optimizer] simuleringskort återges inte korrekt.
* Vissa PNG-filer kan inte återges på ett kort.
* Betafeedback kan inte skickas.

## Version 14.2.1 - 24 februari 2014 {#section_5AD81B0737C843AFB4BE9C4420D70EB3}

<table id="table_DFAB002358C94A17A7F91DAB323A488F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funktion </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>OEmbed </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Uppdatera data </p> </td> 
   <td colname="col2"> <p> 
     <!--MAC-18174-->Ikonen <span class="uicontrol"> Uppdatera data</span> för ett diagram på ett kort är nu dold om lösningen inte tillåter datauppdatering. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Korrigeringar**

* Ett problem som förhindrade delade [!DNL Analytics] rapporter från att tillämpa segmentfilter har korrigerats.
* Ett problem som gjorde att lösningar visades på [!UICONTROL Experience Cloud Solutions] sidan som länkade har korrigerats, även om lösningskontona inte var länkade.
* Korrigerade ett problem som gjorde att [!DNL Adobe Target] kunder i Asien inte kunde klicka på **[!UICONTROL Continue to Experience Cloud]** -knappen på länkningssidan.
* Ett problem som förhindrade delning av YouTube-videor har korrigerats.