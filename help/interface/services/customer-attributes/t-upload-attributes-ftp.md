---
description: Lär dig överföra kundattributdata via FTP till Experience Cloud.
solution: Experience Cloud
title: Överför kundattributdatafilen via FTP
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Valfritt - Överför datafilen via FTP

Om du inte överför med dra och släpp kan du överföra kundattributdata via FTP till Experience Cloud.

Du kan överföra data när du har skapat en kundattributskälla och ett FTP-konto i Experience Cloud. Du skapar ett FTP-konto per attributkälla. De överförda filerna lagras i kontots rotmapp. Data måste vara i formatet `.csv`, med en andra `.fin`-fil för att indikera att överföringen är slutförd.

>[!IMPORTANT]
>
>Granska [datafilskraven för överföring av kundattribut](crs-data-file.md) innan du överför filen.

Filöverföring till kundattributen FTP-plats kan göras via FTP eller SFTP:

* Du behöver en klient som stöder SFTP-anslutningar.
* Du kan ansluta med SFTP med antingen användarnamn/lösenord eller utan lösenord, vilket beskrivs [här](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html?lang=sv-SE).

**Så här överför du datafilen via FTP**

1. [Skapa en kundattributkälla och överför datafilen..](t-crs-usecase.md).

   Kontrollera att du är inloggad på FTP-platsen på `ftp.adobe.com/<sftpname>`.

1. Klicka på **[!UICONTROL Actions]** > **[!UICONTROL File Upload]**.

1. Överför en `.fin`-fil så att filen kan hämtas.

   Filtypen `.fin` har skapats av användaren och signalerar att överföringen är klar. Det kan vara en tom anteckningsblock. Om du till exempel överför `crs123.csv`, överför du även `crs123.fin`.

   Om överföringen lyckas flyttas båda filerna till en mapp med namnet **bearbetad**.

   Se [Datafilskrav för överföring av kundattribut](crs-data-file.md) för viktig information om filnamn och struktur.
