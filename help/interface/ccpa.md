---
title: 'Customer Attributes Support for California Consumer Privacy Act '
description: Läs mer om stöd för Kundattribut i Kaliforniens konsumentintegritetslag
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
source-git-commit: 55c81003b94b7e033cddb6854b5c1f1c1ffa199c
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 4%

---

# Customer Attributes support for California Consumer Privacy Act

Den här sidan beskriver [!UICONTROL Customer Attributes'] stöd för California Consumer Privacy Act (CCPA).

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning och är inte avsett att ersätta juridisk rådgivning. Consult with your legal counsel for advice concerning the (CCPA).

The CCPA is California’s new privacy law, which is effective January 1, 2020. CCPA provides California residents new rights regarding their personal information and imposes data protection responsibilities on certain entities who conduct business in California. CCPA provides consumers with the right to access and delete their personal information and the right to opt out of certain activities that qualify as “selling” personal information to a third party.

Som företag avgör du vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å dina vägnar.

Som tjänsteleverantör tillhandahåller Adobe Experience Cloud support för ert företag för att uppfylla de skyldigheter enligt CCPA som gäller för användning av Experience Cloud produkter och tjänster. This support includes managing requests to access and delete personal information.

Det här dokumentet beskriver hur [!UICONTROL Customer Attributes] har stöd för åtkomst och borttagning av data från era registrerade med hjälp av Adobe Experience Platform Privacy Service API och användargränssnittet för Privacy Service.

For more information about the Adobe Privacy services for CCPA, see the [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Nödvändig konfiguration för att skicka begäranden [!UICONTROL Customer Attributes]

Gör förfrågningar om åtkomst och borttagning av data för [!UICONTROL Customer Attributes]måste du:

1. Identifiera följande:

   * [Organization ID](#organizations.md)
   * Alias ID of CRS Data Source you want to act on
   * CRM ID of the profile you want to act on

   Your [organization ID](#organizations.md) is a 24-character alphanumeric string appended with @AdobeOrg. Du behöver organisationens ID för att kunna skicka begäranden till sekretess-API:t. Kontakta Adobe kundtjänst på `gdprsupport@adobe.com` om du inte kan hitta ID:t.

1. In [!UICONTROL Privacy Service], you can submit Access and Delete requests to Customer Attributes, and check the status of existing requests.

## Required field values in [!UICONTROL Customer Attributes] JSON Requests

företagskontext:

* &quot;namespace&quot;: **imsOrgID**
* &quot;value&quot;: &lt;*ditt organisations-ID-värde*>

&quot;användare&quot;:

* &quot;key&quot;: &lt;*vanligtvis kundens namn*>

* &quot;action&quot;: antingen **åtkomst** eller **delete**

* &quot;user IDs&quot;:

   * &quot;namespace&quot;: &lt;*Alias ID of CRS Data Source*>

   * &quot;type&quot;: **integrationCode**

   * &quot;value&quot;: &lt;*CRM-ID*>

* &quot;include&quot;: **CRS** (which is the Adobe product that applies to the request)

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
