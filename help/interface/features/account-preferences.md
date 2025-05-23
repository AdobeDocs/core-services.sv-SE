---
title: Kontoinställningar och meddelanden
description: Läs om användarprofiler, kontoinställningar och produktanvändningsdata i Experience Cloud. Prenumerera på produktmeddelanden för e-post och  [!DNL Slack] och konfigurera produktaviseringar.
solution: Experience Cloud
feature: Account Preferences, Notifications, Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 1e34c6b2-a792-41c4-adb7-583de596237f
source-git-commit: eddbda54bc3f1cbbc98d7a993d0b477e05c5b01c
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 0%

---

# Kontoinställningar och meddelanden {#preferences}

Om du vill hitta inställningarna för Experience Cloud klickar du på **[!UICONTROL Profile]** ![inställningar](../assets/preferences-icon-sm.png) i sidhuvudet och sedan på **[!UICONTROL Preferences]**.

![inställningar](../assets/preferences-navigation.png){width="100" zoomable="yes"}

På sidan [!UICONTROL Experience Cloud preferences] kan du hantera följande kontofunktioner:

| Funktion | Beskrivning |
|--- |--- |
| [!UICONTROL Profile] | Uppdatera din [Adobe-kontoprofil](https://account.adobe.com/profile). <p>Ditt profilfoto och namn visas när du loggar in på Adobe.com, Adobe-produkter och -tjänster och på offentliga webbplatser som [!DNL Behance]. |
| [!UICONTROL General] | Välj en [organisation](../administration/organizations.md).<p>Den här organisationen används som standard när du loggar in på Experience Cloud. |
| [!UICONTROL Product usage data] | Du kan styra vilka produktanvändningsdata som delas med Adobe när du använder Experience Cloud-program. Detta handlar om hur du använder våra produkter, inte om innehållet eller informationen i din organisation. Adobe använder den här informationen för att förbättra våra produkter, ge dig bättre produktsupport och för att anpassa din upplevelse och kommunikation från oss. <p>Mer information finns i [Produktanvändningsdata](#product-usage-data) (på den här sidan). |
| [!UICONTROL Notifications] | Konfigurera hur och när du vill att [meddelanden](#subscribe-to-notifications-in-experience-cloud) och varningar för produkten ska visas: <ul><li>Välj de produkter du vill prenumerera på för aviseringar</li><li>Konfigurera meddelandetypen ([!UICONTROL in-app], [!UICONTROL email] eller [Slack](#slack-notifications))</li><li>Ange hur ofta du vill få e-postmeddelanden. (Inte skickat, direkt, dagligen eller veckovis.)</li><li>Ange aviseringsprioriteten. Aviseringar i appen visas i fönstrets övre högra hörn under några sekunder. Du kan också ange om aviseringar ska visas tills du stänger dem.</li></ul> |

## [!UICONTROL Product usage data] {#product-usage-data}

Produktanvändningsdata som du väljer att dela med Adobe omfattar följande typer av information om hur du använder och interagerar med Adobe-program:

* Information om webbläsare och enheter, t.ex. enhetsmodell och operativsystem, program- och maskinvaruinformation, inställningar för webbläsare och enheter, unika identifierare (t.ex. IP-adress, cookie-ID eller enhets-ID), installerat minne, språkinställningar och skärmupplösning.
* Hur du interagerar med Adobe Experience Cloud-appar, inklusive de funktioner du använder och de alternativ du väljer;
* Produktinformation om Adobe, t.ex. versionsnummer.
* Information om ert innehåll och era dokument, t.ex. antal sidor och unika identifierare, men inte själva innehållet.
* Information om innehållsanvändning, t.ex. hur många gånger du får tillgång till innehåll och hur du interagerar med innehållet i appen.
* Krasch- och felloggar.

Adobe använder den här informationen för att förbättra våra produkter, ge dig support både i produkten och via kundtjänst samt för att personalisera din upplevelse och kommunikation från oss. Läs mer om [personaliserade upplevelser](personalized-learning.md).

## Prenumerera på meddelanden i Experience Cloud {#notifications}

Du kan välja de produkter och kategorier som du vill prenumerera på. Meddelanden visas i [!UICONTROL Notifications]-porten (i appen), i ditt e-postmeddelande eller i [Slack](#slack-notifications) (beroende på dina prenumerationer).

E-post och Slack är användbara i situationer när du inte är inloggad på Experience Cloud.

### Prenumerera på meddelanden i appen och e-postmeddelanden

1. Navigera till Experience Cloud [inställningar](https://experience.adobe.com/preferences).

1. Aktivera **[!UICONTROL In-app]** eller **[!UICONTROL Email]** under **[!UICONTROL Notifications]**.

   Ändringar i meddelanden sparas automatiskt.

### Prenumerera på [!DNL Slack] meddelanden {#slack}

Du kan konfigurera dina kontoinställningar så att Experience Cloud-meddelanden skickas till en [!DNL Slack]-kanal.

**Förhandskrav**

* Du måste ha ett Experience Cloud-konto.
* Du måste ha ett [!DNL Slack]-konto. Din [!DNL Slack]-administratör aktiverar integreringen av Experience Cloud med [!DNL Slack].
* Du måste vara en del av minst en [!DNL Slack]-arbetsyta.

**Om du vill prenumerera på [!DNL Slack] meddelanden**

1. Navigera till [Inställningar](https://experience.adobe.com/preferences) för Experience Cloud.

1. Leta reda på [!DNL Slack] och klicka sedan på **[!UICONTROL Add to Slack]**.

   ![Lägg till i Slack](../assets/add-to-slack.png)

   Om [!DNL Slack] är installerat öppnas programmet och ett meddelande om behörighetsbegäran visas. Om Slack inte är installerat måste du [begära behörighet](#slack-troubleshoot).

1. Klicka på **[!UICONTROL Allow]**.

1. Aktivera [!DNL Slack]-meddelanden för önskade produkter och kategorier under **[!UICONTROL Notifications]**.

   ![Slack-meddelanden](../assets/slack.png)

   Uppdateringar sparas automatiskt.

### Begär behörighet i [!DNL Slack] (felsökning) {#slack-troubleshoot}

Om [!DNL Slack] inte är installerat visas ett _[!UICONTROL Request to install]_-meddelande när Slack öppnas när du klickar på&#x200B;**[!UICONTROL Add to Slack]**. Exempel:

![Begär integrering med Slack](../assets/slack-workspace.png)

**Om du vill begära behörigheter i Slack**

1. I [!DNL Slack] väljer du arbetsytan på menyn **[!UICONTROL Workspace]** (övre högra hörnet).

1. Om du vill begära programgodkännande för arbetsytehanteraren [!DNL Slack] klickar du på **[!UICONTROL Submit]**.

1. Du får ett meddelande om det i [!DNL Slack] när programbegäran har godkänts.

1. När du har fått [!DNL Slack] godkännande går du tillbaka till Experience Cloud **[!UICONTROL Notifications]** och följer stegen för att [prenumerera på Slack](#slack-notifications) (se ovan).

### Vad du ser i [!DNL Slack]

När [!DNL Slack] har integrerats visas följande information i [!DNL Slack]-meddelandena:

* Det personliga meddelandet kommer att tas emot från programnamnet _Adobe[!DNL Experience Cloud]_.
* Meddelandet innehåller produktlogotypen för det aktuella programmet, till exempel Adobe [!DNL Experience Platform], Adobe [!DNL Experience Manager] och så vidare.
* En länk för att visa alla meddelanden på Experience Cloud.
* En länk för att hantera meddelandeinställningar på Experience Cloud.

## Visa [!UICONTROL notifications] och meddelanden i Experience Cloud {#view-notifications}

I rubriken [!DNL Experience Cloud] kan du visa meddelanden som du [prenumererar](#notifications) på samt visa meddelanden.

1. Klicka på klockikonen i sidhuvudet. ![Meddelanden och meddelanden](../assets/bell-icon.png)

1. Klicka på **[!UICONTROL Notifications]** eller **[!UICONTROL Announcements]**.

   På den här platsen får du viktig information om produkter, ditt samarbete med andra användare och andra relevanta uppdateringar. Uppdateringarna innehåller produktreleaser, underhållsmeddelanden, delade artiklar och godkännandebegäranden.
