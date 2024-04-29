---
title: "[!DNL Customer Attributes] Stöd för den allmänna dataskyddsförordningen"
description: Läs mer om kundattribut Stöd för allmänna dataskyddsregler
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 02417c0c-6780-4699-9470-f1685c3cd25d
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# [!DNL Customer Attributes] stöd för den allmänna dataskyddsförordningen

Den här sidan beskriver hur [!DNL Customer Attributes] stöder allmänna dataskyddsförordningen (GDPR).

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning eller avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om GDPR.

The [Allmän dataskyddsförordning](https://business.adobe.com/privacy/general-data-protection-regulation.html), en lag som gäller den 25 maj 2018, ger alla individer (registrerade) inom EU:s gränser kontroll över sina personuppgifter. Det förenklar också regelmiljön för den internationella verksamheten. Denna lag gäller alla företag (registeransvariga) som erbjuder varor eller tjänster för att övervaka, övervaka eller samla in personuppgifter från enskilda personer inom EU:s gränser vid den tidpunkt då deras personuppgifter behandlas, oavsett var den registeransvarige befinner sig.

Adobe Experience Cloud fungerar som personuppgiftsbiträde för alla personuppgifter som de tar emot och lagrar för sina kunders räkning. Som personuppgiftsansvarig avgör du vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å dina vägnar.

Det här dokumentet beskriver hur [!DNL Customer Attributes] har stöd för de registrerade i GDPR:s dataåtkomst och borttagningsrättigheter med hjälp av Adobe Experience Platform Privacy Service API och Privacy Servicens användargränssnitt.

Mer information om vad GDPR innebär för ditt företag finns i [GDPR och er verksamhet](https://business.adobe.com/privacy/general-data-protection-regulation.html).

## Nödvändig konfiguration för att skicka begäranden [!DNL Customer Attributes]

Gör förfrågningar om åtkomst och borttagning av data för [!DNL Customer Attributes]måste du:

1. Identifiera följande:

   * [Organisations-ID](../../administration/organizations.md)
   * Alias-ID för CRS-datakälla som du vill använda
   * CRM-ID för profilen som du vill använda

   Dina [organisations-ID](../../administration/organizations.md) är en alfanumerisk sträng med 24 tecken som läggs till med @AdobeOrg. Du behöver organisationens ID för att kunna skicka begäranden till sekretess-API:t. Kontakta Adobe kundtjänst på `gdprsupport@adobe.com` om du inte kan hitta ID:t.

1. I [!UICONTROL Privacy Service]kan du skicka in begäranden om åtkomst och borttagning till [!DNL Customer Attributes]och kontrollera status för befintliga förfrågningar.

## Obligatoriska fältvärden i [!DNL Customer Attributes] JSON-begäranden

företagskontext:

* &quot;namespace&quot;: **imsOrgID**
* &quot;value&quot;: &lt;*ditt IMS Org ID-värde*>

användare:

* &quot;key&quot;: &lt;*vanligtvis kundens namn*>
* &quot;action&quot;: antingen **åtkomst** eller **delete**
* användar-ID:
   * &quot;namespace&quot;: &lt;*Alias-ID för CRS-datakälla*>
   * &quot;type&quot;: **integrationCode**
   * &quot;value&quot;: &lt;*CRM-ID*>
* include: **CRS** (som är den Adobe-produkt som är tillämplig på ansökan)
* reglering: **gdpr** (som är den sekretessregel som gäller för begäran)

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
