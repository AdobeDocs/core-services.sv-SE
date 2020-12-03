---
description: En översikt över nya funktioner och uppdateringar i Experience Cloud.
keywords: core services
seo-description: En översikt över nya funktioner och uppdateringar i Experience Cloud.
seo-title: Nyheter i Experience Cloud
solution: Experience Cloud
title: Nyheter i Experience Cloud
uuid: bc1b1542-1a37-4da1-bcfd-fc86af881642
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 6%

---


# Nyheter i Experience Cloud

En översikt över nya funktioner och uppdateringar i Experience Cloud.

## Augusti 2018 {#section_7388CDAB723B49809AABEFEE85CF6378}

Korrigeringar och förbättringar för augusti 2018.

* Förbättrade kommentarer för att synkronisera resurser över Creative Cloud och Experience Cloud. (CORE-15971)
* Funktionsflagga har lagts till för att styra resurssynkroniseringen mellan Experience Cloud och Creative Cloud. (CORE-15938)
* Förbättrade målgruppssegment, bland annat bättre sök- och listupplevelser. (CORE-5833, CORE-14278)
* Ett problem med hög prioritet som blockerade mappdelning från MAC till Creative Cloud har åtgärdats. (CORE-16677)

## July 19, 2018 {#section_EBB549EBABB7480884A180237ADCCD02}

Korrigeringar och förbättringar för juli 2018.

* Använde en backend-funktion för att styra resursdelning mellan Marketing Cloud-till-AEM och Marketing Cloud-till-Creative Cloud. (CORE-14386)
* Korrigerade ett problem som blockerade etablering av nya innehavare i vissa miljöer. (CORE-15509)
* Korrigerade ett problem som omdirigerade användare till [!DNL experiencecloud.adobe.com] vid åtkomst till [!DNL experiencecloud.adobe.com] via [!DNL http] i stället för [!DNL https] (skyddat). (CORE-15587)
* Korrigerade ett problem som blockerade meddelanden för vissa nya innehavare. (CORE-15240)

## June 14, 2018 {#section_7ABC327992CB46B0B8E4A631B8B68899}

Korrigeringar och förbättringar för juni 2018.

* Aktiverade en länk till GDPR-åtkomst för administratörer. (CORE-11731)
* Funktionen Betafeedback har uppdaterats för att begränsa vilka filtyper som kan bifogas till feedback. (CORE-10474)
* Korrigerade ett problem med att ta bort målgrupper från målgruppsbiblioteket. (CORE-12792)
* Ett problem som resulterade i en tom skärm vid åtkomst av arbetsytans länkar med Federated ID har korrigerats. (CORE-11620)

## May 10, 2018 {#section_498AF78DA17C4720AA0F32B51493E550}

New features and fixes in the [!DNL Adobe Experience Cloud] interface.

| Funktion | Beskrivning |
|--- |--- |
| Ny startsida för administration | När du loggar in på Experience Cloud och navigerar till administrationssidan finns det ett nytt intuitivt gränssnitt som hjälper dig att snabbt komma åt dina Experience Cloud-lösningar och bastjänster. |

**Korrigeringar**

* Ett problem där bildöverföringen misslyckades på grund av en Scene7-uppdatering har åtgärdats. (CORE-12746)
* Utför uppdateringar av stöd för TLS 1.0-protokoll, enligt PCI:s anvisningar för att eliminera säkerhetsluckor. (CORE-7695)

## October 26, 2017 {#section_11195859B4094177A939C0561428B525}

**Känt fel**

Många av underhållsmeddelandena runt schemalagt underhåll/produktuppdateringar saknas i meddelandets e-postmeddelande. Vi arbetar för att se till att alla underhållsmeddelanden inkluderas i e-postmeddelandet.

## August 8, 2017 {#section_2313A875454044F490B418506DD24593}

| Funktion | Beskrivning |
|--- |--- |
| Meddelanden - Detaljerade inställningar | Du kan aktivera meddelanden för produkthändelser och lösningsaktiviteter, inklusive meddelanden om överföringsaktivitet för [kundattribut](../attributes/attributes.md). |
| Meddelanden - Underhållsmeddelanden | I Meddelandeinställningarna kan du aktivera underhållsmeddelanden för produkter och lösningar. |
| Admin Console för Experience Cloud Solutions | Nya Experience Cloud-kunder kan börja använda Admin Console, en central plats för hantering av Adobe i hela organisationen.<br>Migreringen till Admin Console för användarhantering fortsätter i vågor. Adobe kommer att kontakta dig (systemadministratörer) när det är dags att migrera.<br>Analysadministratörer, se [Analysmigrering](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html). |

## May 22, 2017 {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| Funktion | Beskrivning |
|--- |--- |
| Massrapportsvitmappning | I Administration > Rapportsvitsmappning kan du nu välja flera rapportsviter och sedan mappa dem till en organisation. (Tidigare var du tvungen att mappa dem individuellt.)  <br>[Genom att mappa rapportsviter](../core-services/core-services.md) till en enda organisation blir det enklare att aktivera funktioner och tjänster för olika lösningar i Experience Cloud. |
| Uppdateringar till Experience Cloud-målgrupper | **Använda**<br> rapportsviterNu kan du använda en rapportsvit för alla [målgruppsregler](../audience-library/t-audience-create.md). (Tidigare var du tvungen att ange en rapportserie i varje regeldefinition.) <br>**Props och**<br> VariablesNu kan du inkludera utkast från analyser och standardvariabler (utöver eVars och händelser) i målgrupper i realtid. |

## 8 november 2016-16.11.1 {#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| Funktion | Beskrivning |
|--- |--- |
| Uppdatera till profil och lösenord | Användare kan inte längre redigera information om IMS-användarprofiler under Personlig information i Redigera profil > Profil och lösenord. I stället omdirigeras användare till `accounts.adobe.com`. Detta gäller alla identitetstyper (Adobe ID, Enterprise och Federated). |

**Korrigeringar**

* Ett problem med tekniska lösenord som orsakade ett fel vid mappdelning mellan Creative Cloud och Experience Cloud har korrigerats. (MAC-31067, MAC-32014)
* Korrigerade ett problem med överföringen av vissa filtyper, inklusive PDF, som hittades efter oktoberversionen i tjänsten Assets Core. (MAC-32517)
