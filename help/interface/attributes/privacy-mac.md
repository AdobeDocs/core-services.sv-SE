---
description: Överväganden och bästa praxis gällande personligt identifierbar information (PII) som överförts och används i Adobe Experience Cloud.
keywords: customer attributes;core services
seo-description: Överväganden och bästa praxis gällande personligt identifierbar information (PII) som överförts och används i Adobe Experience Cloud.
seo-title: Sekretessfrågor - kundattribut
solution: Experience Cloud
title: Sekretessfrågor - kundattribut
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Sekretessfrågor - kundattribut

Överväganden och bästa praxis gällande personligt identifierbar information (PII) som överförts och används i Adobe Experience Cloud.

* Förnamn och efternamn
* Hemadress eller annan fysisk adress
* E-postadress
* Telefonnummer
* Personnummer
* Annan identifierare som tillåter fysisk eller onlinekontakt av en individ. (Varierar efter plats. Verifiera och följ lokala lagar och regler för sekretess och PII för alla platser där du gör affärer.)

Adobe tillhandahåller verktyg som gör det möjligt för annonsörer att samla in beteendeinformation om konsumenter som besöker deras webbplatser eller använder deras tillämpningar. Adobe tillhandahåller även verktyg som gör det möjligt för annonsörer att förbättra informationen med offline- eller externa kundregister som annonsören kan ha i andra informationshanteringssystem.

Ett vanligt skäl till att annonsörer gör detta är att förbättra den information som finns tillgänglig när de fattar konsumentanpassade beslut om marknadsföring och reklam. Med Adobe Analytics och Target kan annonsörer överföra personligt identifierbar information (PII), till exempel e-postadresser, först efter att de har hashas för att göra det omöjligt att använda för att kontakta personen. Hash-kodad information kan fortfarande användas för analys och marknadsföring. Som en påminnelse förbjuder Adobe annonsörer att skicka känslig personlig information till Adobe, såsom journaler, ekonomisk kontoinformation och information om minderåriga.

Adobe inser att dessa typer av beslut om marknadsföring och reklam kan påverka konsumenternas integritet, och det är därför Adobe har byggt in integritetskontroller för att hjälpa annonsörer att uppfylla kundernas förväntningar. Adobe rekommenderar sina annonsörer att noga överväga vilken information som är lämplig att använda i marknadsföringssyfte och i vilka fall annonsören har tillstånd att använda sådan information.

## God praxis

När du överför PII till Adobe Analytics eller Adobe Target rekommenderar Adobe att kunden kraschar PII innan den överförs till Adobe. Hash-kodad information kan fortfarande användas för analys och marknadsföring. Som en påminnelse förbjuder Adobe annonsörer att skicka känslig personlig information till Adobe Analytics och Adobe Target, som medicinska journaler, ekonomisk kontoinformation och information om minderåriga.

Adobe rekommenderar sina annonsörer att noga överväga vilken information som är lämplig att använda i marknadsföringssyfte och i vilka fall annonsören har tillstånd att använda sådan information.

I takt med att konsumentens sekretesslagstiftning fortsätter att vara flödande rekommenderar Adobe att annonsörer respekterar tre gemensamma hållanden:

1. Gör som du säger (i din integritetspolicy).
1. Säg vad du gör (i din integritetspolicy).
1. Förvåna inte era kunder.

Med dessa förväntningar i åtanke rekommenderar Adobe att när en annonsörer kopplar webbläsaraktiviteter till PII, annonserar eller personaliserar annonsören att konsumenten är autentiserad. Ett exempel på detta är att ta med en hälsning i webbplatsens sidhuvud. Adobe rekommenderar också att annonsörer i sin integritetspolicy beskriver vilken typ av surfinformation som är kopplad till PII och under vilka omständigheter surfinformation är kopplad till PII. Slutligen rekommenderar Adobe varmt att annonsörer granskar de avanmälningsalternativ de ger sina kunder för att förstå om och hur de kan använda oautentiserad profilinformation efter avanmälan.
