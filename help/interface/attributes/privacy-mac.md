---
description: Överväganden och bästa praxis när det gäller personligt identifierbar information (PII) som överförts och används i Experience Cloud.
keywords: Kundattribut;bastjänster
solution: Experience Cloud
title: 'Sekretessöverväganden för kundattribut '
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
feature: Kundattribut
topic: Administrering
role: Administrator
level: Experienced
exl-id: 27c026ff-198b-4f49-9718-f25f77a9e716
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 1%

---

# Sekretessöverväganden för kundattribut

Överväganden och bästa praxis gällande personligt identifierbar information (PII) som överförts och används i Adobe Experience Cloud.

* Förnamn och efternamn
* Hemadress eller annan fysisk adress
* E-postadress
* Telefonnummer
* Personnummer
* Annan identifierare som tillåter fysisk eller onlinekontakt av en individ. (Varierar efter plats. Verifiera och följ lokala lagar och regler för sekretess och PII för alla platser där du gör affärer.)

Adobe tillhandahåller verktyg som gör det möjligt för annonsörer att samla in beteendeinformation om konsumenter som besöker deras webbplatser eller använder deras tillämpningar. Adobe tillhandahåller också verktyg som gör det möjligt för annonsörer att förbättra informationen med offline-baserade eller externa kundregister som annonsören kan ha i andra informationshanteringssystem.

Ett vanligt skäl till att annonsörer gör detta är att förbättra den information som finns tillgänglig när de fattar konsumentanpassade beslut om marknadsföring och reklam. Adobe Analytics och Target tillåter annonsörer att överföra personligt identifierbar information (PII), t.ex. e-postadresser, först efter att det har hashas gjorts för att göra det omöjligt att använda för att kontakta personen. Hash-kodad information kan fortfarande användas för analys och marknadsföring. Som påminnelse förbjuder Adobe annonsörer att skicka känslig personlig information till Adobe, såsom journaler, ekonomisk kontoinformation och information om minderåriga.

Adobe inser att dessa typer av beslut om marknadsföring och reklam kan påverka konsumenternas integritet, och det är därför Adobe har byggt in integritetskontroller för att hjälpa annonsörerna att uppfylla kundernas förväntningar. Adobe rekommenderar sina annonsörer att noga överväga vilken information som är lämplig att använda i marknadsföringssyfte och i vilka fall annonsören har tillstånd att använda sådan information.

## God praxis

När du överför PII till Adobe Analytics eller Adobe Target rekommenderar Adobe att kunden kraschar PII innan den överförs till Adobe. Hash-kodad information kan fortfarande användas för analys och marknadsföring. Som påminnelse förbjuder Adobe annonsörer att skicka känslig personlig information till Adobe Analytics och Adobe Target, såsom journaler, ekonomisk kontoinformation och information om minderåriga.

Adobe rekommenderar sina annonsörer att noga överväga vilken information som är lämplig att använda i marknadsföringssyfte och i vilka fall annonsören har tillstånd att använda sådan information.

I takt med att konsumentsekretesslagstiftningen fortsätter att vara i full gång rekommenderar Adobe att annonsörer respekterar tre gemensamma hållpunkter:

1. Gör som du säger (i din integritetspolicy).
1. Säg vad du gör (i din integritetspolicy).
1. Förvåna inte era kunder.

Med dessa förväntningar i åtanke rekommenderar Adobe att annonsören, när en annonsörer associerar surfningsaktiviteter med PII, tillhandahåller meddelanden eller personalisering som anger att konsumenten är autentiserad. Ett exempel på detta är att ta med en hälsning i webbplatsens sidhuvud. Adobe rekommenderar också att annonsörer i sin integritetspolicy beskriver vilken typ av surfinformation som är kopplad till PII och under vilka omständigheter surfinformation är kopplad till PII. Slutligen rekommenderar Adobe varmt att annonsörer granskar de avanmälningsalternativ de ger sina kunder för att förstå om och hur de kan använda oautentiserad profilinformation efter avanmälan.
