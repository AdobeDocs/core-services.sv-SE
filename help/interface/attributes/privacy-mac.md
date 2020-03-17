---
description: Överväganden och bästa praxis gällande personligt identifierbar information (PII) som överförts och används i Adobe Experience Cloud.
keywords: customer attributes;core services
seo-description: Överväganden och bästa praxis gällande personligt identifierbar information (PII) som överförts och används i Adobe Experience Cloud.
seo-title: Sekretessfrågor - kundattribut
solution: Experience Cloud
title: Sekretessfrågor - kundattribut
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
translation-type: tm+mt
source-git-commit: ae97db27349940a8df7ee2ba6678683f57585678

---


# Sekretessfrågor - kundattribut

Överväganden och bästa praxis gällande personligt identifierbar information (PII) som överförts och används i Adobe Experience Cloud.


<!-- <p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> -->


* Förnamn och efternamn
* Hemadress eller annan fysisk adress
* E-postadress
* Telefonnummer
* Personnummer
* Annan identifierare som tillåter fysisk eller onlinekontakt av en individ. (Varierar efter plats. Verifiera och följ lokala lagar och regler för sekretess och PII för alla platser där du gör affärer.)


Adobe tillhandahåller verktyg som gör det möjligt för annonsörer att samla in beteendeinformation om konsumenter som besöker deras webbplatser eller använder deras tillämpningar. Adobe tillhandahåller även verktyg som gör det möjligt för annonsörer att förbättra informationen med offline- eller externa kundregister som annonsören kan ha i andra informationshanteringssystem.

Ett vanligt skäl till att annonsörer gör detta är att förbättra den information som finns tillgänglig när de fattar konsumentanpassade beslut om marknadsföring och reklam. Med Adobe Analytics och Target kan annonsörer överföra personligt identifierbar information (PII), till exempel e-postadresser, först efter att de har hashas för att göra det omöjligt att använda för att kontakta personen. Hash-kodad information kan fortfarande användas för analys och marknadsföring. Som en påminnelse förbjuder Adobe annonsörer att skicka känslig personlig information till Adobe, såsom journaler, ekonomisk kontoinformation och information om minderåriga.

Adobe inser att dessa typer av beslut om marknadsföring och reklam kan påverka konsumenternas integritet, och det är därför Adobe har byggt in integritetskontroller för att hjälpa annonsörer att uppfylla kundernas förväntningar. Adobe rekommenderar sina annonsörer att noga överväga vilken information som är lämplig att använda i marknadsföringssyfte och i vilka fall annonsören har tillstånd att använda sådan information.

**God praxis**

När du överför PII till Adobe Analytics eller Target rekommenderar Adobe att kunden kraschar PII innan den överförs till Adobe. Hash-kodad information kan fortfarande användas för analys och marknadsföring. Som en påminnelse förbjuder Adobe annonsörer att skicka känslig personlig information till Adobe Analytics och Target, som medicinska journaler, ekonomisk kontoinformation och information om minderåriga.

Adobe rekommenderar sina annonsörer att noga överväga vilken information som är lämplig att använda i marknadsföringssyfte och i vilka fall annonsören har tillstånd att använda sådan information.

I takt med att konsumentens sekretesslagstiftning fortsätter att vara flödande rekommenderar Adobe att annonsörer respekterar tre gemensamma hållanden:

1. Gör som du säger (i din integritetspolicy).
1. Säg vad du gör (i din integritetspolicy).
1. Förvåna inte era kunder.

Med dessa förväntningar i åtanke rekommenderar Adobe att när en annonsörer kopplar webbläsaraktiviteter till PII, annonserar eller personaliserar annonsören att konsumenten är autentiserad. Ett exempel på detta är att ta med en hälsning i webbplatsens sidhuvud. Adobe rekommenderar också att annonsörer i sin integritetspolicy beskriver vilken typ av surfinformation som är kopplad till PII och under vilka omständigheter surfinformation är kopplad till PII. Slutligen rekommenderar Adobe varmt att annonsörer granskar de avanmälningsalternativ de ger sina kunder för att förstå om och hur de kan använda oautentiserad profilinformation efter avanmälan.

<!-- <p> <b>Vinay Geol</b> should help craft privacy regarding how all MAC uses privacy/cookies. Privacy implications around each part of the workflow. Moving from CRM to MAC. Can it include PII? What is PII? What isn't PII? </p> 
<p>CRM data is Known Data or Info. Going to combine with activity that occurs when visitor was not authenticated. PII wiki: </p> 
<p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> 
<p>Refactoring of implementation docs as it relates to privacy and cookies. </p> 
<p>Add content to t-publish-audience-segment, as follows: </p> 
<p> Audiences are not filtered based on the authentication state of a visitor. If a visitor can browse your site in un-authenticated and authenticated states, actions that occur when a visitor is un-authenticated can still cause a visitor to be included in an audience. Please review <link> to understand the full privacy implications of audience sharing. </p> 
<p>That "link" goes to a topic dedicated to PII, with this text: </p> 
<p> - Adobe Analytics allows its advertisers to upload personally identifiable information (PII) such as email addresses. When uploading PII to Adobe Analytics, Adobe recommends that the customer should hash PII prior to uploading it to Adobe. Hashed information can still be used for analysis and for marketing purposes. As a reminder, Adobe prohibits advertisers from sending sensitive personal information to Adobe Analytics, such as medical records, financial account information, and information about minors. </p> 
<p> - Adobe recommends its advertisers carefully consider which information is appropriate to use for marketing purposes and in which circumstances the advertiser has permission to use such information. </p> 
<p> - As consumer privacy law remains in flux, Adobe recommends that advertisers respect three common tenets: 1) Do what you say (in your privacy policy); 2) Say what you do (in your privacy policy); and 3) Don't surprise your consumers. </p> 
<p> - With these expectations in mind, Adobe recommends that when an advertiser associates browsing activities to PII, the advertiser provide notices/personalization indicating that the consumer is authenticated. An example of this is including a 'Hello, Jane' greeting within the header of the website. Adobe also recommends that advertisers describe in its privacy policy what type of browsing information it associates with PII and under what circumstances browsing information is associated with PII. Lastly, Adobe strongly recommends advertisers review the opt out choices they provide their consumers to understand whether and how they can use unauthenticated profile information post opt out. </p> 
<p>Possibly revamp the cookies to include privacy, with best practices: https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-privacy.html </p> -->
