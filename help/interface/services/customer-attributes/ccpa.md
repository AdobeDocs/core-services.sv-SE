---
title: Customer Attributes Support for California Consumer Privacy Act
description: Läs mer om stöd för Kundattribut i Kaliforniens konsumentintegritetslag
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# Customer Attributes support for California Consumer Privacy Act

Den här sidan beskriver [!UICONTROL Customer Attributes]-stödet för California Consumer Privacy Act (CCPA).

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning och är inte avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om (CCPA).

CCPA är Kaliforniens nya integritetslagstiftning som träder i kraft den 1 januari 2020. CCPA ger invånare i Kalifornien nya rättigheter när det gäller personuppgifter och ålägger dataskyddsansvar för vissa enheter som bedriver verksamhet i Kalifornien. CCPA ger konsumenterna rätt att få tillgång till och radera sina personuppgifter och rätt att avanmäla vissa aktiviteter som kvalificerar som &quot;sälja&quot; personuppgifter till tredje part.

Som företag avgör du vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å dina vägnar.

Som tjänsteleverantör tillhandahåller Adobe Experience Cloud support för ert företag för att uppfylla de skyldigheter enligt CCPA som gäller för användning av Experience Cloud produkter och tjänster. Supporten omfattar hantering av förfrågningar om åtkomst och radering av personlig information.

I det här dokumentet beskrivs hur [!UICONTROL Customer Attributes] stöder de registrerade personernas CCPA-dataåtkomst och borttagningsrättigheter med hjälp av Adobe Experience Platform Privacy Service API och Privacy Servicens användargränssnitt.

Mer information om sekretessavtal för CCPA för Adobe finns i [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Nödvändig konfiguration för att skicka begäranden för [!UICONTROL Customer Attributes]

Om du vill göra förfrågningar om åtkomst och borttagning av data för [!UICONTROL Customer Attributes] måste du:

1. Identifiera följande:

   * [Organisations-ID](../../administration/organizations.md)
   * Alias-ID för CRS-data Source du vill använda
   * CRM-ID för profilen som du vill använda

   Ditt organisations-ID är en 24-siffrig alfanumerisk sträng som läggs till med @AdobeOrg. Du behöver organisationens ID för att kunna skicka begäranden till sekretess-API:t. Kontakta Adobe kundtjänst på `gdprsupport@adobe.com` om du inte kan hitta ID:t.

1. I [!UICONTROL Privacy Service] kan du skicka in begäran om åtkomst och borttagning till kundattribut och kontrollera status för befintliga begäranden.

## Obligatoriska fältvärden i [!UICONTROL Customer Attributes] JSON-begäranden

företagskontext:

* &quot;namespace&quot;: **imsOrgID**
* &quot;value&quot;: &lt;*ditt företags-ID-värde*>

användare:

* &quot;key&quot;: &lt;*vanligtvis kundens namn*>
* &quot;action&quot;: antingen **access** eller **delete**
* användar-ID:
   * &quot;namespace&quot;: &lt;*Alias ID för CRS Data Source*>
   * &quot;type&quot;: **integrationCode**
   * &quot;value&quot;: &lt;*CRM ID*>
* &quot;include&quot;: **CRS** (som är Adobe-produkten som gäller för begäran)
* &quot;regler&quot;: **ccpa** (som är sekretessregeln som gäller för begäran)

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
