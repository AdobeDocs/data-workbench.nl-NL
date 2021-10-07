---
description: Voor sommige eigenschappen van de Server van het Rapport om te werken, moet u hardware of software verstrekken en vormen alvorens te installeren.
title: Voordat u begint
uuid: cb464fb6-3109-4eff-9c95-f0cf1f8a8c66
exl-id: 5c8bb4c3-fe76-4b4e-960d-113a9927ad59
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# Voordat u begint{#before-you-begin}

Voor sommige eigenschappen van de Server van het Rapport om te werken, moet u hardware of software verstrekken en vormen alvorens te installeren.

## Vereisten voor basisrapportserver {#section-e891eaee79fe4fa98e658426dc3b2777}

De uitvoerrapporten kunnen de vorm hebben van .PNG-afbeeldingen of .XLS-spreadsheets die in een bestandssysteem zijn geplaatst, of als e-mailberichten. De hardwarevereisten zijn identiek aan [gegevens werkbench cliënt](https://experienceleague.adobe.com/docs/data-workbench/using/install/c-data-workbench-client-install.html#Data_Workbench_Client_Minimum_System_Requirements).

De volgende vereisten bestaan voor de Server van het Rapport:

* Toegang tot het bestandssysteem voor de uitvoer van gegevens (delen van netwerk of lokaal station).
* Toegang tot de geconfigureerde SMTP-server.
* Microsoft Excel 2010 64-bits of hoger geïnstalleerd op [!DNL Report] Server. Zie [Overwegingen voor server-zijAutomatisering van Bureau](https://support.microsoft.com/kb/257757) voor extra informatie.

## Aanvullende vereisten {#section-f53d4388656a4dfc90aefe29dfabef89}

* **Installeer een geschikte grafische adapter.** Om rapporten correct terug te geven, moet de machine waarop u  [!DNL Report] Server installeert een aangewezen grafische adapter hebben geïnstalleerd.

* **Installeer Microsoft Excel om rapporten te genereren als Excel-bestanden.** Als u rapporten wilt genereren en distribueren als Microsoft Excel-bestanden ( [!DNL .xls] of  [!DNL .xlsx]), moet op de computer waarop u Rapportserver installeert, de juiste versie van 64-bits Microsoft Excel zijn geïnstalleerd en geregistreerd. Als Excel niet is geregistreerd en de Server van het Rapport probeert om tot het voor het eerst toegang te hebben, zal Excel een registratiedialoogdoos tonen. Als u niet zeker weet of de kopie is geregistreerd, start u Excel handmatig en voltooit u het registratieproces als er een registratiedialoogvenster verschijnt.

   >[!NOTE]
   >
   >Wanneer u rapporten als dossiers van Excel produceert, opent u een nieuw geval van Excel. Zie [https://support.microsoft.com/kb/257757](https://support.microsoft.com/kb/257757) voor meer informatie over dit proces.

* **Toegang bieden tot een SMTP-server om rapporten via e-mail te verspreiden.** Als u rapporten in e-mail zou willen verspreiden, moet de Server van het Rapport met een server kunnen verbinden SMTP, en de aangewezen havens aan de e-mail door:sturen dienst moeten worden geopend.
