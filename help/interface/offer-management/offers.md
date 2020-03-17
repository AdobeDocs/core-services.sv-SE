---
description: Skapa och hantera erbjudanden som ska användas i Adobe Campaign.
seo-description: Skapa och hantera erbjudanden som ska användas i Adobe Campaign.
seo-title: Erbjudandehantering
title: Erbjudandehantering
uuid: 83e1d4cd-c5fa-4df0-9603-2914eb4648f8
index: y
translation-type: tm+mt
source-git-commit: a0e0b51d731343d5cd4226ab29d917aca63317c2

---


# Erbjudanden

Skapa och hantera erbjudanden som ska användas i Adobe Campaign.

Det finns två typer av erbjudanden [!UICONTROL Offer Management]:

| Typ | Beskrivning |
|---|---|
| Allmänt erbjudande | Gör det möjligt för er att fylla i den kompletta datamodellen för erbjudanden (regler för behörighet, start- och slutdatum samt innehåll). |
| Reserverbjudande | Det sista erbjudandet om en kund inte är berättigad till något av de andra erbjudanden som valts. Du kan inte associera några regler för behörighet eller start- och slutdatum med reserverbjudanden. |

>[!NOTE]
>
>I en erbjudandeaktivitet uppmanas du alltid att välja ett reserverbjudande. Därför måste du ha minst ett reserverbjudande i erbjudandelagret innan du kan skapa en erbjudandeaktivitet.

## Skapa ett erbjudande

Skapa ett erbjudande att lägga till i ert erbjudandelager.

1. Klicka på fliken [!UICONTROL Inventory] i [!UICONTROL Offer Management]och **[!UICONTROL Create New Offer]** välj sedan **[!UICONTROL Create Offer]**.

   ![](assets/create-offerx.png)

1. Fyll i följande fält:

   | Fält | Beskrivning |
   |--- |--- |
   | Namn på erbjudande | Namnet som är associerat med erbjudandet. Du kan inte ha två erbjudanden i lagret med dubblettnamn. |
   | Startdatum | Det datum då erbjudandet kan visas. Om du väljer startdatum 15/17 kan erbjudandet visas från kl. 12.00 15/17.  Erbjudandehanteringen följer UTC:s tidsstandard. Detta innebär att <ul><li> Erbjudandena gäller till kl. 00.00 UTC den dag då erbjudandet ska börja.</li><li> Erbjudandet gäller till kl. 00:00 UTC dagen efter slutdatumet. Om ett erbjudande t.ex. har slutdatumet 5/14 går erbjudandet ut kl. 00:00 UTC den 15 maj. Erbjudandet arkiveras sedan.</li><li>När e-postmeddelanden förbereds i Adobe Campaign visas endast erbjudanden som är giltiga vid den tidpunkten.</li></ul> |
   | Slutdatum | Det datum då erbjudandet upphör. Om ett slutdatum på 1/20/17 väljs visas erbjudandet inte längre efter 11:59 på 20/17-11. När ett erbjudande har gått ut arkiveras det automatiskt. Erbjudandehanteringen följer UTC:s tidsstandard. Se raden ovan för mer information. |
   | Villkor | Du kan skapa regler för kvalificering av erbjudanden baserat på tillgängliga data i Campaign-databasen. Vilka som har rätt att delta avgör vilka och när ett erbjudande kan visas.  Du kan till exempel ange att du bara vill att ett &quot;Kloderbjudande för kvinnor&quot; ska visas när (Kön = &#39;kvinna&#39;) och (Region = &#39;Nordost&#39;). De attribut som används för att skapa dessa regler kommer från Campaign Standard-profilen.  Obs!  När du först får tillgång till Erbjudandehantering finns det inga tillgängliga attribut i regelbyggaren. Du måste dela attribut från Campaign-gränssnittet. När attributen har delats är de tillgängliga. |
   | Max ändpunkt | Maximalt antal erbjudanden.  Obs!  Det antal gånger ett erbjudande föreslås beräknas vid e-postförberedelsen. Om du t.ex. förbereder ett e-postmeddelande med ett antal erbjudanden räknas dessa siffror mot det högsta antalet oavsett om e-postmeddelandet skickas eller inte. |
   | Max tak per användare | Det maximala antal gånger som ett erbjudande kan erbjudas en viss användare.  Obs!  Det antal gånger ett erbjudande föreslås för en viss användare beräknas vid e-postförberedelsen. Om du till exempel förbereder ett e-postmeddelande med ett antal erbjudanden räknas dessa siffror mot det högsta antalet per användare oavsett om e-postmeddelandet skickas eller inte. |
   | Etiketter | Lägg till etiketter i ett erbjudande för att gruppera dem. Du kan skriva och trycka på Retur för att skapa en ny etikett eller börja skriva och välja ett befintligt erbjudande i listrutan. |

1. Fyll i representationsinformationen.

   | Fält | Beskrivning |
   |---|---|
   | Kanal | Den kanal som den här innehållsrepresentationen kan levereras i. Campaign Standard-e-postmeddelanden är den enda kanal som är tillgänglig för närvarande. |
   | Placement | Välj den plats där den här innehållsrepresentationen kan levereras. Placeringar fylls i automatiskt från fliken Placeringar. Du måste associera varje innehållsrepresentation med en placering i listrutan. Du kan inte skapa flera innehållsrepresentationer med samma placering i samma erbjudande. |
   | Innehållstyp | Välj en innehållstyp för en bild, bild-URL, text eller HTML. |
   | Omdirigeringslänk | Det här fältet visas om du väljer en innehållstyp för bild- eller bild-URL. Det här är länken som användaren omdirigeras till om han/hon klickar på erbjudandet i ett e-postmeddelande. |

1. Klicka **[!UICONTROL Save & Preview]** för att se informationen om erbjudandet innan du skickar in det.
1. Klicka **[!UICONTROL Approve]** för att godkänna erbjudandet. När erbjudandet är godkänt kan det användas i en erbjudandeaktivitet.

   Om du inte har behörighet att godkänna ett erbjudande klickar du i stället **[!UICONTROL Submit]**. Erbjudandet visas i erbjudandebiblioteket med en väntande status. När en användare med godkännandebehörighet har godkänt den kan den användas i en erbjudandeaktivitet.
