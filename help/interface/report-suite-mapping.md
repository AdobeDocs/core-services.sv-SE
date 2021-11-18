---
description: Lär dig hur du mappar en eller flera rapportsviter till en organisation i Experience Cloud.
title: 'Mappa rapportsviter till en organisation '
uuid: b983d5a6-b3d0-4137-ac53-bc5681d3e58b
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 4e9f0f7a-8e16-4473-af4a-3e74ad50c044
source-git-commit: c073b3bacf5505c01017d4ba2507621df8ef877e
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Mappa rapportsviter till en organisation {#topic_7C4740559EAC4E0FA5F8DEF886B580DA}

>[!NOTE]
>
>Rapportsvitens mappningsfunktion togs bort i november 2020. Kontakta kundsupporten om du har några frågor.

Experience Cloud (t.ex. Experience Cloud ID-tjänsten och [!UICONTROL People]) är kopplade till en organisation i stället för till en enskild rapportserie. För att dessa tjänster ska fungera på rätt sätt måste varje analysrapportsserie mappas till en organisation. Mappningsprocessen:

* Anger en Experience Cloud-organisation som primär organisation för rapportsviten.
* Ändrar inte vem som har åtkomst till en rapportserie (åtkomsten bestäms fortfarande av Adobe Analytics inloggningskonto för varje användare)

## Krav

Du måste vara Analytics-administratör för ett inloggningsföretag som har tillgång till den rapportserie som du vill mappa. Dessutom måste det här kontot [länkad till en Experience Cloud-organisation](organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1) för att kartlägga rapporteringsprogram för den organisationen.

Organisationer är nedtonade om du inte har administratörsbehörighet för Analytics för ett inloggningsföretag inom den organisationen som har åtkomst till den angivna rapportsviten.

## Avbilda en rapportsvit till en organisation {#task_23993FE78DF6455FA8D7BE60686EA16C}

1. Navigera till Report Suites for Data Governance på [!DNL Analytics] > **[!UICONTROL Admin]** > **[!UICONTROL Data Governance]** (se [Visa/hantera inställningen för datastyrning i Report Suite](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-view-settings.html?lang=en)

1. Om du vill se vilka inloggningsföretag som har åtkomst till varje rapportsvit väljer du **[!UICONTROL Visible to Login Companies]**.

   Den här vyn är avsedd att hjälpa dig att fatta ett välgrundat beslut om mappningen.

1. Välj listrutan i dialogrutan **[!UICONTROL Mapped Organization]** -kolumnen intill en rapportserie och välj den organisation som du vill mappa till.

   Tips om hur du väljer en Experience Cloud-organisation finns i nästa avsnitt.

## Mappa flera rapportsviter till en organisation {#task_94955B0D8ABA4CB1A38746ECF8E32711}

1. Välj **[!UICONTROL Experience Cloud]** > **[!UICONTROL Administration]** > **[!UICONTROL Report Suite Mapping]**.

1. Välj de rapportsviter som du vill mappa.

   ![Välj de rapportsviter som du vill mappa](assets/rs-mapping-multiple.png)

1. Välj organisation (Outdoor Inc, i det här exemplet) och klicka sedan på **[!UICONTROL Select]**.

   Tips om hur du väljer en Experience Cloud-organisation finns i nästa avsnitt.

1. Välj **[!UICONTROL Save Mapping]**.

## Tips för att välja en Experience Cloud-organisation {#mapping-tips}

Det här avsnittet innehåller tips som hjälper dig att välja den Experience Cloud-organisation som du ska mappa en rapportserie till.

### Vilken organisation ska jag välja?

Om Experience Cloud ID-tjänsten distribueras till rapportsviten kontrollerar du att den organisation du valt i verktyget för mappning av rapportsviten är densamma som anges i [!DNL visitorAPI.js] på din plats. Du kan använda instruktionerna i [Testa och verifiera tjänsten Experience Cloud ID](https://experienceleague.corp.adobe.com/docs/id-service/using/implementation/test-verify.html) för att hitta det organisations-ID som används av besökar-ID-tjänsten.

Se till att distributionen matchar den organisation du valde i verktyget för mappning av rapportsviten.

### Varför är vissa organisationer nedtonade?

Om du tar bort en organisation betyder det att du inte har tillräcklig behörighet för att mappa till den nedtonade rapportsviten. Titta på följande exempel:

![Varför är vissa organisationer nedtonade?](assets/rs-mapping.png)

I det här diagrammet anger den blå tangenten administratörsbehörighet. De grå linjerna visar synlighet.

Den här användaren har åtkomst till två Experience Cloud-organisationer. De har utfört följande:

* Länkade deras administratörskonto i [!UICONTROL chapek] Analytics loggar in företag på deras [!UICONTROL Chapek] Företagskonto för Experience Cloud.
* Länkade deras icke-administratörskonto i [!UICONTROL doohan] Analytics loggar in företag på deras [!UICONTROL Chapek] Företagskonto för Experience Cloud.
* Länkade sitt icke-administratörskonto i inloggningsföretaget nigel Analytics till deras Nigel Inc Experience Cloud org-konto.

I följande punkter visas mappningsåtgärder som den här användaren kan och inte kan utföra för dessa rapportsviter:

* [!UICONTROL Chapek-prod] kan mappas till [!UICONTROL Chapek] Corp org eftersom den här användaren är administratör för ett länkat inloggningsföretag för Analytics ([!UICONTROL chapek]) och hans konto är kopplat till den här organisationen.
* [!UICONTROL Nigel-prod] rapportsviten kan inte länkas av den här användaren eftersom han/hon inte är administratör i något inloggningsföretag som den här rapportsviten är synlig för.
* [!UICONTROL Doohan-prod] kan mappas till [!UICONTROL Chapek Corp] eftersom användaren är administratör för ett inloggningsföretag ([!UICONTROL chapek]) som är länkad till Experience Cloud org (observera att han inte är administratör för inloggningsföretaget för Adobe Analytics). Det är viktigt att veta att [!UICONTROL doohan-prod] kan också mappas till Nigel Inc Experience Cloud org, även om den här användaren inte kan utföra mappningen. I det här fallet visas båda Experience Cloud-organisationerna i listan, men [!UICONTROL Nigel Inc] är nedtonad. Före mappningen bör den här användaren rådfråga en administratör för nollinloggningsföretaget för att avgöra vilken organisation som är bäst lämpad för mappning. Gränssnittet visar en varning om möjlig konflikt om du väljer en organisation som skiljer sig från den organisation som rapportsviten ursprungligen skapades i.

## Vanliga frågor {#section_099E485805994C929FF9C9F75219BEE1}

### Varför ser jag inte alla rapporteringsprogram?

Vissa av dina rapportsviter kan vara synliga under ett annat inloggningsföretag. Du kan ändra det aktuella inloggningsföretaget med hjälp av listrutan högst upp på skärmen.

### Vad händer om jag inte känner igen vissa av de organisationer som listas i listrutan för en av mina rapportsviter?

Listan innehåller alla *möjligt* organisationer som din rapportsvit kan mappas till, även om du inte har behörighet att mappa till alla dessa rapportsviter. Om du är osäker på om rapportsviten ska mappas till någon av de nedtonade rapportsviterna i listan kan du kontakta en Experience Cloud-administratör i din organisation för att avgöra vilket alternativ som är bäst.

### Vad händer om jag inte känner igen några av de inloggningsföretag som anges för en rapportserie i kolumnen&quot;Synligt för inloggningsföretag&quot;?

Vid något tillfälle delades denna rapportserie med ett annat inloggningsföretag som kan vara en del av en annan Experience Cloud-organisation.

### Vad är det här felet &quot;Möjlig konflikt&quot; om rapportsviten genereras av en annan organisation? Varför spelar det någon roll?

Det här meddelandet hjälper dig att fatta ett välgrundat beslut om mappningen av rapportsviten. Vi vill informera dig om att rapportsviten ursprungligen skapades under en annan organisation om den organisationen skulle vara lämpligare för den här rapportsviten.

### Hur vet jag om en rapportsserie är mappad?

Mappade rapportsviter visas i ett format som inte kan redigeras. Kontakta kundtjänst om du måste ändra mappningen.

### Vad händer om jag bara känner till organisationsnumret för min Experience Cloud-organisation? Hur söker jag efter namnet på mitt Org ID?

Du hittar ditt organisationsnamn i [Organisationer och kontoinställningar](organizations.md).

### Jag ser ett datum i kolumnen &quot;Datummappning&quot;. Vem mappade det där?

Du kan läsa ändringsloggen för Report Suite i analysgränssnittet för att kontrollera det användar-ID som gjorde ändringen. Leta efter händelsen &quot;Suite associerad med IMS-organisationen&quot;.
