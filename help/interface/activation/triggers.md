---
description: Så här konfigurerar du Experience Cloud-utlösare.
keywords: integrations;Triggers
seo-description: Så här konfigurerar du Experience Cloud-utlösare.
seo-title: Utlösare
solution: Marketing Cloud
title: Utlösare
uuid: dab536e3-1969-4661-919e-5b15f423fecd
translation-type: tm+mt
source-git-commit: ae97db27349940a8df7ee2ba6678683f57585678

---


# Utlösare

## Översikt över utlösare {#topic_4F21FCE9A64E46E8B6D51F494FA652A7}

*Med triggers* kan ni identifiera, definiera och övervaka viktiga konsumentbeteenden och sedan generera kommunikation mellan olika lösningar för att engagera besökarna på nytt. Ni kan använda triggers i realtidsbeslut och personalisering.

* Konfigurera snabb ommarknadsföring för övergivna varukorgar eller övergivna varukorgar med borttagna produkter
* Ofullständiga formulär och ansökningar
* Åtgärder eller sekvenser av åtgärder på platsen

![](assets/trigger-abandonment-2.png)

**Typer av utlösare**

I allmänhet kan en utlösare ta 15-90 minuter att starta en marknadsföringskampanj. Detta varierar beroende på implementering av datainsamling, inläsning på pipeline, anpassad konfiguration av den definierade utlösaren och arbetsflödet i Adobe Campaign.

* **Övergiven:** Du kan skapa en utlösare som aktiveras när en besökare tittar på en produkt men inte lägger till något i kundvagnen. Konfigurera [poängberäkning](../activation/triggers.md#concept_A506150674AD45DB98D3CC07E560D334) för att förstå kundernas tendens att inte göra det efter att ha övergett en kundvagn.
* **Åtgärd:** Du kan skapa utlösare, till exempel, som aktiveras efter anmälan till nyhetsbrev, e-postprenumerationer eller program för kreditkort (bekräftelser). Om du är återförsäljare kan du skapa en utlösare för en besökare som registrerar sig för ett lojalitetsprogram. I media och underhållning skapar du triggers för besökare som tittar på en viss show och kanske vill svara med en enkät.
* **Sessionsstart och sessionsslut:** Skapa en utlösare för händelser för sessionsstart och sessionsslut.

## Skapa en Experience Cloud-utlösare {#task_821F37183AC045E5AC8EED20317598FE}

Skapa en utlösare för att överge och konfigurera villkoren för utlösaren och poängsättningen för benägenhet. Du kan till exempel ange villkor för en utlösares regler under ett besök, till exempel mått som Cart Abandon eller dimensioner som produktnamnet. När reglerna är uppfyllda körs utlösaren.

<!-- t_create-trigger.xml -->

>[!NOTE]
>
>Det finns för närvarande en teknisk gräns på 100 utlösare.

1. Klicka på i Experience Cloud ![](assets/menu-icon.png)och sedan på **[!UICONTROL Activation]**.
1. Leta reda på [!UICONTROL Triggers] kortet och klicka sedan på **[!UICONTROL Launch]**.

   ![Stegresultat](assets/activation-triggers.png)

1. Klicka **[!UICONTROL New Trigger]** och ange sedan typ av utlösare:

   ![Stegresultat](assets/add-trigger.png)

1. Konfigurera utlösaren genom att fylla i följande fält och dra mått och dimensionsobjekt till regelns behållare:

   | Element | Beskrivning |
   |--- |--- |
   | Namn | Det egna namnet för den här utlösaren. |
   | Beskrivning | Beskrivningen av den här utlösaren, hur du kommer att använda den och så vidare. |
   | Report Suite | Analytics- [rapportsviten](https://docs.adobe.com/content/help/en/analytics/implementation/analytics-basics/ref-reports-report-suites.html) som används för den här utlösaren. Den här inställningen identifierar de rapportdata som ska användas. |
   | Besök måste<br>inkluderaVisit får inte<br>innehållaTrigger efter inga<br>actionInclude-metadata | Du kan definiera villkor eller besökarbeteenden som du vill ska inträffa och beteenden som du inte vill ska inträffa.  Regler för en enkel utlösare för övergivna varukorgar kan till exempel vara:<ul><li>Besök måste omfatta följande:  Cart Addition (metric) och Exists. (Du kan förfina regeln ytterligare med en viss produktvy eller med dimensioner som webbläsartyper.)</li><li>Besök får inte omfatta  Checka ut.</li><li>Utlös efter ingen åtgärd för:  10 minuter.</li><li>Inkludera metadata: Gör att du kan lägga till en viss Campaign-dimension eller variabler som är relevanta för en besökares beteende. Det här fältet kan vara användbart för Adobe Campaign att skapa rätt e-postmeddelande för återmarknadsföring.</li></ul><br>Du kan ange Any (Alla) och eller Or (Logik) i eller mellan behållare, beroende på vilka kriterier du anger är viktiga för regeln. |
   | Behållare | Behållare är där du anger och lagrar regler, villkor eller filter som definierar en utlösare. Om du vill att händelser ska inträffa samtidigt placerar du dem i samma behållare. Det innebär att varje behållare bearbetas oberoende på träffnivå.  Om du till exempel har två behållare som förenas med operatorn And kan du förvänta dig att reglerna kvalificeras när två träffar uppfyller kraven. |
   | Starta ny session efter | Skapa en utlösare för händelser för sessionsstart och sessionsslut. |

1. (Valfritt) I övergivningsutlösare kan du använda [Propensitetsbedömning](../activation/triggers.md#concept_A506150674AD45DB98D3CC07E560D334).

   ![Stegresultat](assets/propensity-scoring.png)

1. Klicka på **[!UICONTROL Save]**.
1. Använd triggers för återmarknadsföring [i](https://docs.campaign.adobe.com/doc/standard/en/EMA_Transactional_messaging_Marketing_Cloud_Triggers.html) realtid i [!DNL Adobe Campaign].

### Exempelutlösare

**Cart Abandonment Trigger**

På följande sida visas regler som du kan använda för en Cart Abandonment-utlösare, baserat på vilka produkter som visas under ett besök.

![](assets/abandonment-trigger.png)

**Utlösare för referent**

Följande utlösare utlöses när en träff kommer in med produkten av Men&#39;s Boots och Facebooks hänvisningsprogram. För att de två kriterierna ( *produkter* och *referent*) ska utvärderas i samma träff bör de läggas till i samma behållare.

![](assets/fb-boots-promo.png)

## Propensitetsbedömning {#concept_A506150674AD45DB98D3CC07E560D334}

<!-- propensity-scoring.xml -->

Förstå kundernas tendens att återvända efter att ha övergett en kundvagn. Propensitetsbedömning är inbyggd i Experience Cloud Triggers och finns för övergivningsutlösare.

![Stegresultat](assets/propensity-scoring.png)

Vissa kunder överger till exempel kundvagnar för att dra nytta av e-postbonusar för att återvända till kundvagnen. För att minska intäktsförlusten hjälper algoritmen för beräkning av sannolikhet till att identifiera de berörda kundöverhoppare som troligen inte skulle returnera utan incitament.

Du kan:

* Undvik att överexponera kunderna för återmarknadsföring.
* Identifiera rätt kunder som överger kundvagnen och mappa deras aktivitet till rätt budskap.
* Öka intäkterna genom att veta vilka kunder som kommer att returnera och inte.

## Värdet för känslighetsskalförändring {#section_CA99874A25434CC0BF01D0DA61608889}

Du kan identifiera dolda beteenden eller mönster som finns i alla dina data genom att utföra dataidentifiering. I synnerhet hjälper benägenhetsbedömningen er att identifiera kluster med liknande kunder med mer fokuserade och objektiva metoder i stället för enkel segmentering eller filtrering. Dessutom kan ni med benägenhetsbedömning lägga upp prediktiva funktioner för att identifiera beteende för företagets värdefulla kunder.

När ni har identifierat den värdefulla målgruppen kan ni sedan engagera dem för maximal effekt. Om du till exempel är ett företag som går mellan företag kan du ha säljsamtalsleads som gör att du kan poängsätta leads och identifiera deras sannolikhet för att konvertera offline. Eftersom varje lead ökar kostnaderna är det mest effektiva och billigaste sättet att fokusera på era resurser att skapa ett incitament för att identifiera potentiella kunder med störst sannolikhet för att omvandla en försäljning.

Med poängberäkning av sannolikhet kan du identifiera de faktorer som är mest prediktiva för en viss poäng eller öka sannolikheten för att en händelse ska äga rum, men den kan även användas för att besvara specifika frågor:

* Kommer kunden att konvertera?
* Kommer kunden att svara på ett e-postmeddelande?
* Kommer kunden att köpa tillbaka?

Med benägenhetsbedömning kan ni besvara dessa frågor och identifiera besökare med en vilja till åtgärd som sedan kan ställas in och poängsättas.
