---
title: Customer Attributes Support for California Consumer Privacy Act
description: Customer Attributes Support for California Consumer Privacy Act
translation-type: tm+mt
source-git-commit: 2e8c8aee39546a345e72cda2dad08ad866cd90f9
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---


# Customer Attributes Support for California Consumer Privacy Act


>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning och är inte avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om Kaliforniens konsumentsekretesslag.

California Consumer Privacy Act (CCPA) är Kaliforniens nya integritetslag, som träder i kraft den 1 januari 2020. CCPA ger invånare i Kalifornien nya rättigheter när det gäller personuppgifter och ålägger dataskyddsansvar för vissa enheter som bedriver verksamhet i Kalifornien. CCPA ger konsumenterna rätt att få tillgång till och radera sina personuppgifter samt rätt att avanmäla vissa aktiviteter som kvalificerar som &quot;sälja&quot; personuppgifter till tredje part.

Som företag avgör ni vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å era vägnar.

Som tjänsteleverantör tillhandahåller Adobe Experience Cloud support så att ert företag kan uppfylla sina skyldigheter enligt CCPA som är tillämpliga på användningen av Experience Cloud-produkter och -tjänster, inklusive hantering av begäranden om åtkomst och radering av personuppgifter.

I det här dokumentet beskrivs hur kundattribut stöder de registrerade personernas CCPA-dataåtkomst och borttagningsrättigheter med hjälp av API:t för Adobe Experience Platform Privacy Service och gränssnittet för Integritetstjänst.

Mer information om Adobes sekretessavtal för CCPA finns i [Adobes sekretesscenter](https://www.adobe.com/privacy/ccpa.html).

## Nödvändig inställning för att skicka begäranden om kundattribut

Om du vill begära åtkomst till och ta bort data för kundattribut måste du:

1. Identifiera följande:

* IMS-organisations-ID
* Alias-ID för CRS-datakälla som du vill använda
* CRM-ID för profilen som du vill använda

Ett IMS-organisations-ID är en 24 tecken lång alfanumerisk sträng som läggs till med @AdobeOrg. Om marknadsföringsteamet eller den interna Adobe-systemadministratören inte känner till din organisations IMS-organisation kan du kontakta Adobes kundtjänst på gdprsupport@adobe.com. Du måste ha IMS-organisations-ID för att kunna skicka begäranden till sekretess-API:t.

2. Använd användargränssnittet för sekretesstjänsten för att skicka in begäranden om åtkomst och borttagning till kundattribut och för att kontrollera status för befintliga begäranden.

## Obligatoriska fältvärden i kundattribut JSON-begäranden

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
