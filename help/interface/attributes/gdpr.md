---
title: 'Kundattribut Stöd för allmänna dataskyddsregler '
description: Läs mer om stöd för kundattribut i den allmänna dataskyddsförordningen
feature: Kundattribut
topic: Administrering
role: Administrator
level: Experienced
exl-id: 02417c0c-6780-4699-9470-f1685c3cd25d
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 1%

---

# Kundattribut stöd för den allmänna dataskyddsförordningen

Den här sidan beskriver hur [!UICONTROL Customer Attributes] stöder allmänna dataskyddsförordningen (GDPR).

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning eller avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om GDPR.

Den [allmänna dataskyddsförordningen](https://business.adobe.com/privacy/general-data-protection-regulation.html), en lag som gäller den 25 maj 2018, ger alla individer (registrerade) inom EU:s gränser kontroll över sina personuppgifter. Det förenklar också regelmiljön för internationell verksamhet. Denna lag gäller alla företag (registeransvariga) som erbjuder varor eller tjänster för att övervaka, övervaka eller samla in personuppgifter från enskilda personer inom EU:s gränser vid den tidpunkt då deras personuppgifter behandlas, oavsett var den registeransvarige befinner sig.

Adobe Experience Cloud fungerar som personuppgiftsbiträde för alla personuppgifter som de tar emot och lagrar för sina kunders räkning. Som personuppgiftsansvarig avgör du vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å dina vägnar.

I det här dokumentet beskrivs hur [!UICONTROL Customer Attributes] stöder de registrerade personernas GDPR-dataåtkomst och borttagningsrättigheter med hjälp av Adobe Experience Platform Privacy Service API och Privacy Servicens användargränssnitt.

Mer information om vad GDPR innebär för ditt företag finns i [GDPR och Ditt företag](https://business.adobe.com/privacy/general-data-protection-regulation.html).

## Nödvändig konfiguration för att skicka begäranden för [!UICONTROL Customer Attributes]

Om du vill begära åtkomst till och ta bort data för [!UICONTROL Customer Attributes] måste du:

1. Identifiera följande:

   * IMS-organisations-ID
   * Alias-ID för CRS-datakälla som du vill använda
   * CRM-ID för profilen som du vill använda

   Ett IMS-organisations-ID är en 24 tecken lång alfanumerisk sträng som läggs till med @AdobeOrg. Om ditt marknadsföringsteam eller den interna systemadministratören i Adobe inte känner till din organisations IMS-organisation kan du kontakta Adobe kundtjänst på gdprsupport@adobe.com. Du måste ha IMS-organisations-ID för att kunna skicka begäranden till sekretess-API:t.

1. I [!UICONTROL Privacy Service] kan du skicka in begäranden om åtkomst och borttagning till kundattribut och kontrollera status för befintliga begäranden.

## Obligatoriska fältvärden i [!UICONTROL Customer Attributes] JSON-begäranden

företagskontext:

* &quot;namespace&quot;: **imsOrgID**
* &quot;value&quot;: &lt;*ditt IMS-organisations-ID-värde*>

&quot;användare&quot;:

* &quot;key&quot;: &lt;*vanligtvis kundens namn*>

* &quot;action&quot;: antingen **åtkomst** eller **ta bort**

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
