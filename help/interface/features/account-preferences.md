---
title: Kontoinställningar och meddelanden
description: Läs om användarprofiler och kontoinställningar i Experience Cloud. Prenumerera på produktmeddelanden för e-post och  [!DNL Slack] och konfigurera produktaviseringar.
solution: Experience Cloud
feature: Account Preferences, Notifications, Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 1e34c6b2-a792-41c4-adb7-583de596237f
source-git-commit: b42a942deb91f3fb68ff1195b94df248763f5122
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# Kontoinställningar och meddelanden {#preferences}

Experience Cloud [inställningar](https://experience.adobe.com/preferences) innehåller meddelanden (i programmet, e-post och [!DNL Slack]), prenumerationer och aviseringar.

I inställningarna kan du:

* Sök efter [organisationer](../administration/organizations.md)
* Ange ett mörkt tema (alla program stöder inte det här temat).
* Konfigurera användarinställningar, meddelanden och prenumerationer.
* Logga ut från Experience Cloud.

## Hantera inställningar

Om du vill hantera inställningar väljer du **[!UICONTROL Preferences]** på din kontomeny ![inställningar](../assets/preferences-icon-sm.png).

På [!UICONTROL Experience Cloud preferences] kan du konfigurera följande funktioner:

| Funktion | Beskrivning |
|--- |--- |
| [Standardorganisation](../administration/organizations.md) | Välj den organisation som du vill se när du startar Experience Cloud. |
| [!UICONTROL Product data collection] | Välj vilka tekniker Adobe kan använda för att samla in data om hur du använder dina Adobe-produkter. |
| [Meddelanden](#notifications-and-announcements) | Aktivera [!UICONTROL in-app]-, [!UICONTROL email]- eller [Slack](#slack-notifications)-meddelanden. |
| [!UICONTROL Personalized learning recommendations and promotions] | Välj var du vill få [personlig hjälp](personalized-learning.md) för dina Adobe-produkter. Den här hjälpen finns tillgänglig via e-post, i programmet och i Experience League Communities. |
| [!UICONTROL Subscriptions] | Välj de produkter och kategorier som du vill prenumerera på. Meddelanden i [!UICONTROL Notifications]-porten och i ditt e-postmeddelande. |
| [!UICONTROL Priority] | Välj de kategorier som du vill ska ha hög prioritet. Dessa kategorier är markerade med en [!UICONTROL High]-tagg och kan konfigureras för leverans som varningar. |
| [!UICONTROL Alerts] | Välj de meddelanden som du vill visa aviseringar för i webbläsaren. Varningar visas i fönstrets övre högra hörn under några sekunder. |
| E-post | Ange hur ofta du vill få e-postmeddelanden. (Inte skickat, direkt, dagligen eller veckovis.) |

## Prenumerera på meddelanden i Experience Cloud {#notifications}

Du kan välja de produkter och kategorier som du vill prenumerera på. Meddelanden visas i [!UICONTROL Notifications]-porten (i appen), i ditt e-postmeddelande eller i [Slack](#slack-notifications) (beroende på dina prenumerationer).

E-post och Slack är användbara i situationer när du inte är inloggad på Experience Cloud.

### Prenumerera på meddelanden i appen och e-postmeddelanden

1. Navigera till Experience Cloud [inställningar](https://experience.adobe.com/preferences).

1. Aktivera **[!UICONTROL In-app]** eller **[!UICONTROL Email]** under **[!UICONTROL Notifications]**.

   Ändringar i meddelanden sparas automatiskt.

### Prenumerera på [!DNL Slack] meddelanden {#slack}

>[!NOTE]
>
>Meddelanden från Slack kommer att släppas: **11 september 2024**


Du kan konfigurera dina kontoinställningar så att Experience Cloud-meddelanden skickas till en [!DNL Slack]-kanal.

**Förhandskrav**

* Du måste ha ett Experience Cloud-konto.
* Du måste ha ett [!DNL Slack]-konto. Din Slack-administratör aktiverar integreringen mellan Experience Cloud och Slack.
* Du måste vara en del av minst en [!DNL Slack]-arbetsyta.

**Om du vill prenumerera på Slack-meddelanden**

1. Navigera till Experience Cloud [inställningar](https://experience.adobe.com/preferences)

1. Leta reda på [!DNL Slack] och klicka sedan på **[!UICONTROL Add to Slack]**.

   ![Lägg till i Slack](../assets/add-to-slack.png)

   Om [!DNL Slack] är installerat öppnas programmet och ett meddelande om behörighetsbegäran visas.

   * Klicka på **[!UICONTROL Allow]**.

   Om [!DNL Slack] inte är installerat visas ett _Request to install_ -meddelande:

   ![Begär integrering med Slack](../assets/slack-request.png)

   * I Slack väljer du arbetsytan i det övre högra hörnet av programmet.

   * Klicka på **[!UICONTROL Submit]** om du vill begära programgodkännande för arbetsytehanteraren i Slack.

   * Du får ett meddelande om det i [!DNL Slack] när programbegäran har godkänts.

   * När du har fått [!DNL Slack] godkännande går du tillbaka till Experience Cloud **[!UICONTROL Notifications]** och klickar sedan på **[!UICONTROL Add to Slack]**.

1. Aktivera [!DNL Slack]-meddelanden för önskade produkter och kategorier under **[!UICONTROL Notifications]**.

   ![Slack-meddelanden](../assets/slack.png)

   Uppdateringar sparas automatiskt.

### Vad du ser i [!DNL Slack]

Meddelanden från Slack visar följande information:

* Det personliga meddelandet tas emot från programnamnet _Adobe Experience Cloud_.
* Meddelandet innehåller produktlogotypen för det aktuella programmet, t.ex. Adobe Experience Platform, Adobe Experience Manager osv.
* En länk för att visa alla meddelanden på Experience Cloud.
* En länk för att hantera meddelandeinställningar på Experience Cloud.

## Visa [!UICONTROL notifications] och meddelanden i Experience Cloud {#view-notifications}

I sidhuvudet på Experience Cloud kan du visa meddelanden som du [prenumererar](#notifications) på samt visa meddelanden.

1. Klicka på klockikonen i sidhuvudet. ![Meddelanden och meddelanden](../assets/bell-icon.png)

1. Klicka på **[!UICONTROL Notifications]** eller **[!UICONTROL Announcements]**.

   På den här platsen får du viktig information om produkter, ditt samarbete med andra användare och andra relevanta uppdateringar. Uppdateringarna innehåller produktreleaser, underhållsmeddelanden, delade artiklar och godkännandebegäranden.