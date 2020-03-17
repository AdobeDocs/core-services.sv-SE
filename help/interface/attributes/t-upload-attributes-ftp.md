---
description: Om du inte överför via dra och släpp kan du överföra kundattributdata via FTP till Experience Cloud.
keywords: customer attributes;core services
seo-description: Om du inte överför via dra och släpp kan du överföra kundattributdata via FTP till Experience Cloud.
seo-title: Valfritt - Överför datafilen via FTP
solution: Experience Cloud
title: Valfritt - Överför datafilen via FTP
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
translation-type: tm+mt
source-git-commit: d304e625bd2125854d9ed932674522284995e030

---


# Valfritt - Överför datafilen via FTP

Om du inte överför via dra och släpp kan du överföra kundattributdata via FTP till Experience Cloud.

Du kan överföra data när du har skapat en kundattributskälla och ett FTP-konto i Experience Cloud. Du skapar ett FTP-konto per attributkälla. De överförda filerna lagras i kontots rotmapp. Data måste vara i `.csv` format, med en andra `.fin` fil för att indikera att överföringen är slutförd.

>[!IMPORTANT]
>
>Granska [datafilskraven för överföring av kundattribut](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) innan du överför filen.

Filöverföring till kundattributens FTP-plats kan göras via FTP eller SFTP.

* Du behöver en klient som stöder SFTP-anslutningar.
* Du kan ansluta med SFTP med antingen användarnamn/lösenord eller utan lösenord, vilket beskrivs [här](https://docs.adobe.com/help/en/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html).

**Så här överför du datafilen via FTP**

1. [Skapa en kundattributskälla och överför datafilen..](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   Se till att du är inloggad på FTP-webbplatsen på [!DNL ftp.adobe.com/<sftpname>].

1. Klicka på **[!UICONTROL Actions]** > **[!UICONTROL File Upload]**.

1. Överför en `.fin` fil så att filen kan hämtas.

   Filtypen `.fin` skapas av användaren och signalerar att överföringen är klar. Det kan vara en tom anteckningsblock-fil. Om du till exempel överför [!DNL crs123.csv]kan du även överföra [!DNL crs123.fin].

   Om överföringen lyckas flyttas båda filerna till en mapp som kallas **bearbetad**.

   Se [Datafilskrav för överföring av kundattribut](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) för viktig information om filnamn och struktur.
