---
title: '[!DNL Customer attributes] Stöd för den allmänna dataskyddsförordningen'
description: Läs mer om stöd för kundattribut i den allmänna dataskyddsförordningen
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 02417c0c-6780-4699-9470-f1685c3cd25d
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# [!DNL Customer attributes]-stöd för den allmänna dataskyddsförordningen

Den här sidan beskriver hur [!DNL customer attributes] stöder allmänna dataskyddsförordningen (GDPR).

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning eller avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om GDPR.

Den [allmänna dataskyddsförordningen](https://business.adobe.com/privacy/general-data-protection-regulation.html), en lag som gäller den 25 maj 2018, ger alla individer (registrerade) inom EU:s gränser kontroll över sina personuppgifter. Det förenklar också regelmiljön för den internationella verksamheten. Denna lag gäller alla företag (registeransvariga) som erbjuder varor eller tjänster för att övervaka, övervaka eller samla in personuppgifter från enskilda personer inom EU:s gränser vid den tidpunkt då deras personuppgifter behandlas, oavsett var den registeransvarige befinner sig.

Adobe Experience Cloud fungerar som personuppgiftsbiträde för alla personuppgifter som de tar emot och lagrar för sina kunders räkning. Som personuppgiftsansvarig avgör du vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å dina vägnar.

I det här dokumentet beskrivs hur [!DNL customer attributes] stöder de registrerades GDPR-dataåtkomst och borttagningsrättigheter med hjälp av Adobe Experience Platform Privacy Service API och Privacy Service UI.

Mer information om vad GDPR innebär för ditt företag finns i [GDPR och ditt företag](https://business.adobe.com/privacy/general-data-protection-regulation.html).

## Nödvändig konfiguration för att skicka begäranden för [!DNL customer attributes]

Om du vill göra förfrågningar om åtkomst och borttagning av data för [!DNL customer attributes] måste du:

1. Identifiera följande:

   * [Organisations-ID](../../administration/organizations.md)
   * Alias-ID för CRS-data Source du vill använda
   * CRM-ID för profilen som du vill använda

   Ditt [organisations-ID](../../administration/organizations.md) är en 24 tecken lång alfanumerisk sträng som läggs till i @AdobeOrg. Du behöver organisationens ID för att kunna skicka begäranden till sekretess-API:t. Kontakta Adobe kundtjänst på `gdprsupport@adobe.com` om du inte kan hitta ID:t.

1. I [!UICONTROL Privacy Service] kan du skicka begäranden om åtkomst och borttagning till [!DNL customer attributes] och kontrollera status för befintliga begäranden.

## Obligatoriska fältvärden i [!DNL customer attributes] JSON-begäranden

företagskontext:

* &quot;namespace&quot;: **imsOrgID**
* &quot;value&quot;: &lt;*ditt IMS Org ID-värde*>

användare:

* &quot;key&quot;: &lt;*vanligtvis kundens namn*>
* &quot;action&quot;: antingen **access** eller **delete**
* användar-ID:
   * &quot;namespace&quot;: &lt;*Alias ID för CRS Data Source*>
   * &quot;type&quot;: **integrationCode**
   * &quot;value&quot;: &lt;*CRM ID*>
* &quot;include&quot;: **CRS** (som är den Adobe-produkt som gäller för begäran)
* &quot;regler&quot;: **gdpr** (som är den sekretessregel som gäller för begäran)

## Exempel på JSON-begäran

```json
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "<IMS_ORG_ID>"
    }
  ],
  "users": [
    {
      "key": "<KEY>",
      "action": [
        "<access/delete>"
      ],
      "userIDs": [
        {
          "namespace": "<Alias ID of CRS Data Source>",
          "type": "integrationCode",
          "value": "<CRM ID>"
        }
      ]
    }
  ],
  "regulation": "<gdpr/ccpa/pdpa>",
  "include": [
    "CRS"
  ]
}
```

## Datafält som returnerats för åtkomstbegäranden

```json
attributes:
{
"value": "<*value*>",
"key": "<*key*>",
"displayName": "<*displayName*>"
}
```
