---
description: Lär dig överföra kundattributdata via FTP till Experience Cloud.
solution: Experience Cloud
title: Överför kundattributdatafil via FTP
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: 21120abb5ab0fcc8d556012851548f39f3875038
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Överför datafilen via FTP (valfritt)

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

## Konfigurera ett FTP-konto

Ställ in ett FTP-konto per attributkälla.

Klicka på [!UICONTROL File Upload and Schema Validation] på sidan **[!UICONTROL FTP Setup]**.

![Redigera ett schema](assets/ftp-account.png)

De överförda filerna lagras i kontots rotmapp. Data måste vara i formatet `.csv`, med en andra `.fin`-fil för att indikera att överföringen är slutförd.

De namn du anger för strängar, heltal och tal används för att skapa [!DNL Analytics]-mått.

* **[!UICONTROL attribute:]** attributdata lästes från den överförda `.csv`-filen.

* **[!UICONTROL Type:]** Datatypen, till exempel:

   * **Sträng:** En teckensekvens.

   * **Heltal:** Hela tal.

   * **Nummer:** Kan innehålla upp till två decimaler.

* **[!UICONTROL Display Name:]** Ett eget namn för attributet. Du kan till exempel ändra attributet *kundens ålder* till *kund sedan*.

* **[!UICONTROL Description:]** En användarvänlig beskrivning av attributet.