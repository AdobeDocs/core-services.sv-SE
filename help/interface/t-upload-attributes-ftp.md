---
description: Lär dig hur du överför kundattributdata via FTP till Experience Cloud.
solution: Experience Cloud
title: Överför kundattributdatafilen via FTP
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: eb2ad8a8255915be47b6002a78cc810b522170d2
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Valfritt - Överför datafilen via FTP

Om du inte överför via dra och släpp kan du överföra kundattributdata via FTP till Experience Cloud.

Du kan överföra data när du har skapat en kundattributskälla och ett FTP-konto i Experience Cloud. Du skapar ett FTP-konto per attributkälla. De överförda filerna lagras i kontots rotmapp. Data måste finnas i `.csv` format, med en andra `.fin` för att ange att överföringen är klar.

>[!IMPORTANT]
>
>Granska [Datafilskrav för överföring av kundattribut](crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) innan du överför filen.

Filöverföring till FTP-webbplatsen för kundattribut kan göras via FTP eller SFTP:

* Du behöver en klient som stöder SFTP-anslutningar.
* Du kan ansluta till SFTP med antingen användarnamn/lösenord eller utan lösenord enligt beskrivningen [här](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html?lang=en).

**Så här överför du datafilen via FTP**

1. [Skapa en kundattributskälla och överför datafilen..](t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   Se till att du är inloggad på FTP-platsen på `ftp.adobe.com/<sftpname>`.

1. Välj **[!UICONTROL Actions]** > **[!UICONTROL File Upload]**.

1. Överför en `.fin` så att filen kan hämtas.

   Filtypen `.fin` är användarskapat och signalerar att överföringen är klar. Det kan vara en tom anteckningsblock-fil. Om du till exempel överför [!DNL crs123.csv], du också överföra [!DNL crs123.fin].

   Om överföringen lyckas flyttas båda filerna till en mapp med namnet **bearbetade**.

   Se [Datafilskrav för överföring av kundattribut](crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) om du vill ha viktig information om filnamn och struktur.
