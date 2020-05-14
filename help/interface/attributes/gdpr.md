---
title: Kundattribut Stöd för allmänna dataskyddsregler
description: Kundattribut Stöd för allmänna dataskyddsregler
translation-type: tm+mt
source-git-commit: 4223f9260865756842ad43b99d2509908f4d6572
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 0%

---


# Kundattribut stöd för den allmänna dataskyddsförordningen

Den här sidan beskriver hur kundattribut stöder allmänna dataskyddsförordningen (GDPR).

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning eller avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om GDPR.

Den [allmänna dataskyddsförordningen](https://www.adobe.com/privacy/general-data-protection-regulation/what-is-gdpr.html), som är en lag som gäller den 25 maj 2018, ger alla individer (registrerade) inom EU:s gränser kontroll över sina personuppgifter. Det förenklar också regelmiljön för internationell verksamhet. Denna lag gäller alla företag (registeransvariga) som erbjuder varor eller tjänster för att övervaka, övervaka eller samla in personuppgifter från enskilda personer inom EU:s gränser vid den tidpunkt då deras personuppgifter behandlas, oavsett var den registeransvarige befinner sig.

Adobe Experience Cloud fungerar som databehandlare för alla personuppgifter som de tar emot och lagrar för sina kunders räkning. Som personuppgiftsansvariga fastställer ni de personuppgifter som Adobe Experience Cloud bearbetar och lagrar åt er.

I det här dokumentet beskrivs hur de registrerade [!UICONTROL Customer Attributes] stöder dataåtkomst och borttagningsrättigheter för GDPR-data med hjälp av API:t för Adobe Experience Platform Privacy Service och gränssnittet för integritetstjänsten.

Mer information om vad GDPR innebär för ditt företag finns i [GDPR och Ditt företag](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Nödvändiga inställningar för att skicka begäranden [!UICONTROL Customer Attributes]

Om du vill begära åtkomst till och ta bort data för [!UICONTROL Customer Attributes]måste du:

1. Identifiera följande:

   * IMS-organisations-ID
   * Alias-ID för CRS-datakälla som du vill använda
   * CRM-ID för profilen som du vill använda
   Ett IMS-organisations-ID är en 24 tecken lång alfanumerisk sträng som läggs till med @AdobeOrg. Om marknadsföringsteamet eller den interna Adobe-systemadministratören inte känner till din organisations IMS-organisation kan du kontakta Adobes kundtjänst på gdprsupport@adobe.com. Du måste ha IMS-organisations-ID för att kunna skicka begäranden till sekretess-API:t.

1. I [!UICONTROL Privacy Service]kan du skicka in begäran om åtkomst och borttagning till kundattribut och kontrollera status för befintliga begäranden.

## Obligatoriska fältvärden i [!UICONTROL Customer Attributes] JSON-begäranden

företagskontext:

* &quot;namespace&quot;: **imsOrgID**
* &quot;value&quot;: &lt;*ditt IMS-organisations-ID-värde*>

&quot;användare&quot;:

* &quot;key&quot;: &lt;*vanligtvis kundens* namn>

* &quot;action&quot;: antingen **åtkomst** eller **radering**

* användar-ID:

   * &quot;namespace&quot;: &lt;*Alias-ID för CRS-datakälla*>

   * &quot;type&quot;: **integrationCode**

   * &quot;value&quot;: &lt;*CRM-ID*>

* &quot;include&quot;: **CRS** (som är den Adobe-produkt som gäller för begäran)

* reglering: **gdpr** (som är den sekretessregel som gäller för begäran)

## Exempel på JSON-begäran

```
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

```
attributes:
{
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
