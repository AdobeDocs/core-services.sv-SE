---
description: Lär dig mer om centrala gränssnittskomponenter för Experience Cloud. Få hjälp med användar- och produktadministration i Admin Console, aktivera program för Experience Cloud tjänster. Få hjälp om Audience Library, kundattribut, Experience Cloud Assets med mera.
title: Experience Cloud gränssnittsdokumentation
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: 361175f290d73f1637673420700874a2415e3fca
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 8%

---

# Experience Cloud Central Interface - översikt

[Experience Cloud](https://experience.adobe.com) är en integrerad Adobe-familj med program, produkter och tjänster för digital marknadsföring. Från det intuitiva gränssnittet får du snabbt tillgång till dina molnprogram, produktfunktioner och tjänster.

![Experience Cloud](assets/landing.png)

Från Experience Cloud sidhuvud kan du:

* Få tillgång till alla program och tjänster i Experience Cloud
* På Hjälp-menyn söker du efter produktdokumentation, självstudiekurser och communityinlägg. Visa resultat i Experience League.
* Sök efter affärsobjekt globalt med en global sökning (endast Experience Platform-användare) i sökfältet.
* Hantera ditt konto [inställningar](features/account-preferences.md) (aviseringar, aviseringar och prenumerationer)


Borttaget från GSPM:

## Utforska funktioner

<table style="table-layout:fixed">
<tr style="border: 0;">
   <td valign="top">
      <a href="../user-guide/effective-prompts.md">
      <img alt="Höger vinklad" src="../assets/icons/icon-chevronRight.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/effective-prompts.md">
         <strong> Skriv effektiva frågor </strong>
         </a>
      </div>
      <p>
         <em>Skapa beskrivande uppmaningar som genererar digitala upplevelser under varumärket.</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/create/overview.md">
      <img alt="Pensel" src="../assets/icons/icon-create.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/create/overview.md">
         <strong> Skapa upplevelser </strong>
         </a>
      </div>
      <p>
         <em>Skapa prestanda, e-post under varumärket och Meta-annonser.</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/approvals/overview.md">
      <img alt="Markering" src="../assets/icons/icon-checkmarkCircle.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/approvals/overview.md">
         <strong> Granska och godkänn </strong>
         </a>
      </div>
      <p>
         <em>Samordna den effektiva granskningen och godkännandet av marknadsföringsresurser.</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/content/overview.md">
      <img alt="Stödraster" src="../assets/icons/icon-images.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/content/overview.md">
         <strong> Hantera innehåll </strong>
         </a>
      </div>
      <p>
         <em>Sök, hantera och återanvänd innehåll samtidigt som varumärkesriktlinjerna behålls.</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/insights/overview.md">
      <img alt="Diagram" src="../assets/icons/icon-dataAnalytics.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/insights/overview.md">
         <strong> Visa insikter </strong>
         </a>
      </div>
      <p>
         <em>Analysera innehållseffektiviteten för betalda mediekanaler.</em>
      </p>
   </td>
</tr>
</table>

## Lär dig hur

<table style="table-layout:fixed">
<td valign="top">
   <div>
      <a href="/help/user-guide/guidelines/add-guidelines.md">
      <img alt="Lägg till riktlinjer" src="../assets/card-guidelines.png">
      <strong>Lägg till riktlinjer</strong>
      </a>
   </div>
   <p>
      <em>Lär dig hur du lägger till riktlinjer - varumärken, produkter och egenskaper - i GenStudio for Performance Marketing.</em>
   </p>
</td>
<td valign="top">
   <div>
      <a href="/help/user-guide/create/create-email-experience.md">
      <img alt="Idéer, böcker, penna, dator" src="../assets/card-create-assets.png">
      <strong>Skapa en e-postupplevelse</strong>
      </a>
   </div>
   <p>
      <em>Lär dig hur du skapar en e-postupplevelse på ett varumärke.</em>
   </p>
</td>
<td valign="top">
   <div>
      <a href="/help/user-guide/create/create-meta-ad.md">
      <img alt="Personer som flyttar filer till en mapp" src="../assets/card-manage-content.png">
      <strong>Skapa en annonsupplevelse i Meta </strong>
      </a>
   </div>
   <p>
      <em>Lär dig hur du skapar en varumärkesanpassad annonsupplevelse i Meta.</em>
   </p>
</td>
</table>


(Slut på GSPM)







## Logga in på Experience Cloud {#signin}

Logga in och verifiera att du är i rätt [organisation](administration/organizations.md).

1. Navigera till [Adobe Experience Cloud](https://experience.adobe.com).
1. Skriv din e-postadress för Adobe och klicka sedan på **[!UICONTROL Continue]**.
1. Välj ett konto.
1. Skriv ditt lösenord.
1. Kontrollera att du är i rätt organisation.

   ![Verifiera att du är i rätt organisation](assets/organizations-menu.png)

   **Verifiera din organisation**

   [organisationen](administration/organizations.md) visas i gränssnittshuvudet.

   Om din organisation använder Federated ID:n kan du med Experience Cloud logga in med din organisations enkla inloggning utan att behöva ange din e-postadress och ditt lösenord. Lägg till `#/sso:@domain` i Experience Cloud-URL:en (`https://experience.adobe.com`) för att utföra den här åtgärden.

   För en organisation med Federated ID och domänen `adobecustomer.com` anger du URL-länken till `https://experience.adobe.com/#/sso:@adobecustomer.com`. Du kan också gå direkt till ett specifikt program genom att skapa ett bokmärke för den här URL:en, som bifogas med programsökvägen. (För Adobe Analytics, till exempel, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`.)

## Öppna Experience Cloud-program {#navigation}

När du har loggat in på Experience Cloud kan du snabbt komma åt alla program, tjänster och organisationer från det enhetliga huvudet.

Gå till programväljaren ![menu](assets/menu-icon.png) om du vill få åtkomst till Experience Cloud-program och -tjänster som har etablerats för dig inom din organisation.

![Öppna Experience Cloud-program](assets/platform-core-services.png)

## Få hjälp och support {#support}

Lär dig mer och hjälp med **[!UICONTROL Help center]** (![asset](assets/help-icon.png)) i sidhuvudet, inklusive hjälpinnehåll (dokumentation, självstudiekurser och kurser) på [Experience League](https://experienceleague.adobe.com/sv#home), samt ytterligare resurser för enskilda program. Du kan även skicka in öppen feedback och skapa prioriterade supportärenden.

![Få hjälp och support](assets/search-menu.png)

Menyn [!UICONTROL Help] ger dig även åtkomst till:

* **[!UICONTROL Support]:** Skapa en supportanmälan eller kontakta [!UICONTROL Support] med Twitter.
* **[!UICONTROL Feedback]:** Dela feedback om Experience Cloud. Dina synpunkter används för att förbättra Adobe produkter och tjänster.
* **[!UICONTROL Status]:** Navigera till `https://status.adobe.com/experience_cloud` och kontrollera produktdriftsstatus och [!UICONTROL Manage Subscriptions].
* **[!UICONTROL Developer Connection]:** Navigering till `adobe.io` och hitta dokumentation för utvecklare.

## Hantera din användarprofil

På menyn [!UICONTROL Profile] kan du:

* Ange ett mörkt tema (alla program stöder inte det här temat)
* [Hantera Experience Cloud-inställningar](features/account-preferences.md)
* Välj eller sök efter en [organisation](administration/organizations.md)
* Visa [!UICONTROL Legal Notices]
* Logga ut
* Konfigurera kontoinställningar, meddelanden och prenumerationer

## Visa meddelanden och meddelanden i produkten {#notifications}

Klicka på klockikonen för att visa meddelanden och meddelanden. Meddelanden kan vara relevanta och användbara uppdateringar, inklusive produktreleaser, underhållsmeddelanden, delade artiklar och godkännandeförfrågningar.

![Meddelanden och meddelanden](assets/notifications-menu-small.png)

Mer information om hur du hanterar meddelanden och aviseringar finns i [Kontoinställningar och meddelanden](features/account-preferences.md)


## Nyheter

Läs om de senaste förbättringarna av Experience Cloud centrala gränssnittskomponenter.

>[!BEGINTABS]

>[!TAB Slack-integrering med Experience Cloud]

Du kan konfigurera dina kontoinställningar så att Experience Cloud-meddelanden skickas till en [!DNL Slack]-kanal.

[!BADGE Beta]{type=Informative url="https://experienceleague.adobe.com/sv/docs/core-services/interface/features/account-preferences#notifications" tooltip="Läs om Slack"}


>[!TAB Nytt webbanvändargränssnitt för kampanj]

Upplev nya Adobe Campaign användargränssnitt. Modern, intuitiv och dynamisk!

[![bild](assets/do-not-localize/learn-more-button.svg)](start/campaign-ui.md#ac-web-ui)


>[!TAB Push channel upcoming changes]

Vissa viktiga ändringar av tjänsten Android Firebase Cloud Messaging (FCM) kommer att släppas 2024 och kan komma att påverka din Adobe Campaign-implementering. Konfigurationen för prenumerationstjänster för push-meddelanden för Android kan behöva uppdateras för att den här ändringen ska fungera. Du kan redan kontrollera och vidta åtgärder.

[![bild](assets/do-not-localize/learn-more-button.svg)](../technotes/upgrades/push-technote.md)



>[!ENDTABS]

## Börja med grunderna

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
    <a href="start/whats-new.md"><img src="assets/do-not-localize/start-capabilities.png"></a>
    <div><strong>Viktiga funktioner</strong><br/>Utforska nyckelfunktionerna i Adobe Campaign v8 för kanalövergripande kampanjhantering.</div>
    </td>
    <td>
    <a href="start/connect.md"><img src="assets/do-not-localize/start-connect.jpeg"></a>
    <div><strong>Anslut till Campaign v8</strong><br/>Lär dig hur du ansluter till Adobe Campaign v8 och startar kampanjhanteringsresan genom att installera och konfigurera klientkonsolen.</div><br/>
    </td>
    <td>
    <a href="start/create-message.md"><img src="assets/do-not-localize/start-send.jpeg"></a>
    <div><strong>Skicka meddelanden</strong><br/>Lär dig hur du skickar meddelanden över olika kanaler, till exempel e-post, SMS och push-meddelanden.
    </div></td>
    <td>
    <a href="audiences/create-profiles.md"><img src="assets/do-not-localize/start-profiles.png"></a>
    <div><strong>Importera profiler</strong><br/>Utforska enkelt skapandet av profiler i Adobe Campaign v8-databasen. Lägg till profiler manuellt eller via importer, förfina kunddata och anpassa kampanjer enkelt.</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="start/whats-new.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="start/connect.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="start/create-message.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="audiences/create-profiles.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    </tr>
</table>

## Utforska dokumentationen

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="assets/do-not-localize/icon-start.svg" width="35px">
    <br/>
      <strong>Kom igång</strong><br/><a href="start/campaign-ui.md">Användargränssnitt</a> - <a href="start/ac-components.md">Komponenter och processer</a> - <a href="start/v7-to-v8.md">Från Classic v7 till v8</a> - <a href="start/campaign-faq.md">Vanliga frågor</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-experience.svg" width="35px">
    <br/>
      <strong>Kundens upplevelse</strong><br/><a href="../automation/workflow/about-workflows.md" target="_blank">Automatisera med arbetsflöden</a> - <a href="../automation/campaigns/set-up-campaigns.md" target="_blank">Kampanjsamordning</a> - <a href="interaction/interaction.md">Beslutshantering</a> - <a href="send/personalize.md">Personalization</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-send.svg" width="35px">
    <br/>
      <strong>Skicka meddelanden</strong><br/><a href="start/create-message.md">Kom igång</a> - <a href="send/preview-and-proof.md">Förhandsgranska och korrektur</a> - <a href="send/predictive.md">Tidsoptimering för sändning</a> - <a href="reporting/gs-reporting.md">Rapportering och analys</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="assets/do-not-localize/icon_profile-audience.svg" width="35px">
    <br/>
      <strong>Profiler och målgrupper</strong><br/><a href="audiences/create-profiles.md">Lägg till profiler</a> - <a href="audiences/create-audiences.md">Skapa målgrupper</a> - <a href="start/subscriptions.md">Hantera prenumerationer</a> - <a href="start/privacy.md">Sekretess</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-configure.svg" width="35px">
    <br/>
      <strong>Arkitektur och konfiguration</strong><br/><a href="architecture/architecture.md">Arkitektur</a> - <a href="start/implement.md">Kampanjimplementering v8</a> - <a href="connect/integration.md">Anslut till andra lösningar</a> - <a href="start/gs-permissions.md">Användare och behörigheter</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-dev.svg" width="35px">
    <br/>
      <strong>Utvecklarresurser</strong><br/><a href="dev/datamodel.md">Datamodell för kampanj v8</a> - <a href="dev/schemas.md">Scheman</a> - <a href="dev/api.md">API:er</a>
    </td>
  </tr>
</table>

## Ytterligare resurser

[Produktbeskrivning för Adobe Campaign v8](https://helpx.adobe.com/se/legal/product-descriptions/adobe-campaign-managed-cloud-services.html){target="_blank"} - [Dokumentation för Adobe Campaign webbgränssnitt](https://experienceleague.adobe.com/docs/campaign-web/v8/campaign-web-home.html?lang=sv-SE){target="_blank"} - [Självstudiekurser](https://experienceleague.adobe.com/docs/campaign-learn/tutorials/overview.html?lang=sv-SE){target="_blank"} - [[!DNL Adobe Campaign] automatiseringsguide](https://experienceleague.adobe.com/docs/campaign/automation/home.html?lang=sv-SE){target="_blank"} - [Kontrollpanelen för Campaign v8](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/key-features.html?lang=sv){target="_blank"}

