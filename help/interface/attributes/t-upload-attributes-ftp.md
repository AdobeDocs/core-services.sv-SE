---
description: Lär dig hur du överför kundattributdata via FTP till Experience Cloud.
keywords: Kundattribut;bastjänster
solution: Experience Cloud
title: 'Överför kundattributdatafilen via FTP '
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
feature: Kundattribut
topic: Administrering
role: Administrator
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---

# Valfritt - Överför datafilen via FTP

Om du inte överför med dra och släpp kan du överföra kundattributdata via FTP till Experience Cloud.

Du kan överföra data när du har skapat en kundattributskälla och ett FTP-konto i Experience Cloud. Du skapar ett FTP-konto per attributkälla. De överförda filerna lagras i kontots rotmapp. Data måste vara i formatet `.csv`, med en andra `.fin`-fil för att indikera att överföringen är slutförd.

>[!IMPORTANT]
>
>Granska [datafilskraven för överföring av kundattribut](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) innan du överför filen.

Filöverföring till FTP-webbplatsen för kundattribut kan göras via FTP eller SFTP:

* Du behöver en klient som stöder SFTP-anslutningar.
* Du kan ansluta till SFTP med antingen användarnamn/lösenord eller utan lösenord, vilket beskrivs [här](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html?lang=en).

**Så här överför du datafilen via FTP**

1. [Skapa en kundattributskälla och överför datafilen..](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   Kontrollera att du är inloggad på FTP-platsen på `ftp.adobe.com/<sftpname>`.

1. Klicka på **[!UICONTROL Actions]** > **[!UICONTROL File Upload]**.

1. Överför en `.fin`-fil så att filen kan hämtas.

   Filtypen `.fin` skapas av användaren och signalerar att överföringen är klar. Det kan vara en tom anteckningsblock-fil. Om du till exempel överför [!DNL crs123.csv], överför du även [!DNL crs123.fin].

   Om överföringen lyckas flyttas båda filerna till mappen **bearbetad**.

   Se [Datafilskrav för överföring av kundattribut](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) för viktig information om filnamn och struktur.
