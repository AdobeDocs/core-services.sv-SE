---
title: 'Customer Attributes Support for California Consumer Privacy Act '
description: Läs mer om stöd för Kundattribut i Kaliforniens konsumentintegritetslag
feature: Kundattribut
topic: Administrering
role: Administratör
level: Erfaren
translation-type: tm+mt
source-git-commit: 61d60273e933c637dfe4400da78257e1c80015b3
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 5%

---


# Customer Attributes support for California Consumer Privacy Act

Den här sidan beskriver [!UICONTROL Customer Attributes']-stödet för California Consumer Privacy Act (CCPA).

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning och är inte avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om (CCPA).

CCPA är Kaliforniens nya integritetslagstiftning som träder i kraft den 1 januari 2020. CCPA ger invånare i Kalifornien nya rättigheter när det gäller personuppgifter och ålägger dataskyddsansvar för vissa enheter som bedriver verksamhet i Kalifornien. CCPA ger konsumenterna rätt att få tillgång till och radera sina personuppgifter samt rätt att avanmäla vissa aktiviteter som kvalificerar som &quot;sälja&quot; personuppgifter till tredje part.

Som företag avgör du vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å dina vägnar.

Som tjänsteleverantör tillhandahåller Adobe Experience Cloud support för ditt företag så att det kan uppfylla sina skyldigheter enligt CCPA som är tillämpliga på användningen av produkter och tjänster från Experience Cloud, inklusive hantering av förfrågningar om åtkomst och radering av personuppgifter.

Det här dokumentet beskriver hur [!UICONTROL Customer Attributes] stöder de registrerade personernas CCPA-dataåtkomst och borttagningsrättigheter med hjälp av Adobe Experience Platform Privacy Service API och Privacy Servicens användargränssnitt.

Mer information om sekretessavtal för CCPA för Adobe finns i [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

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

* reglering: **ccpa** (som är den sekretessregel som gäller för begäran)

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
