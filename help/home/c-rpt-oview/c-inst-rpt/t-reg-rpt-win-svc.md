---
description: Stappen om de Server van het Rapport te registreren en in werking te stellen.
solution: Analytics
title: Rapportserver registreren als Windows-service
topic: Data workbench
uuid: 01fc0bbf-9f4a-487e-b1cb-16bf6974a541
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Rapportserver registreren als Windows-service{#registering-report-server-as-a-windows-service}

Stappen om de Server van het Rapport te registreren en in werking te stellen.

Alvorens u deze procedure uitvoert, identificeer de rekening van Vensters waaronder de [!DNL Report Server] dienst zal lopen. Zorg ervoor dat deze rekening de juiste toestemmingen heeft om tot de plaats toegang te hebben waar de geproduceerde rapporten worden opgeslagen (namelijk gebruik niet [!DNL Local System Account]).

Gebruik onderstaande procedure om te starten [!DNL Report Server]. Wanneer u [!DNL Report Server] voor het eerst begint, registreert het zich automatisch als dienst van Vensters.

Wanneer u [!DNL Report Server] voor het eerst begint, verbindt het automatisch met de Server van de Vergunning van Adobe om uw digitaal certificaat te registreren. Als u het registratieproces wilt voltooien, moet uw computer zijn verbonden met internet wanneer u de volgende stappen uitvoert.

1. In Vensters, navigeer aan de folder waar u installeerde [!DNL Report Server].

   Voorbeeld: D:\Adobe\Report

1. Dubbelklik **[!UICONTROL ReportServer.exe]**.
1. Om te bevestigen dat [!DNL Report Server] correct loopt, klik **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Services]**. Deze bevelopeenvolging kan variëren afhankelijk van welke versie van Vensters u gebruikt.
1. In de de dienstlijst, bepaal de plaats van de ingang voor [!DNL Report Server] en bevestig dat zijn status Begonnen is en zijn starttype Automatisch is.
1. Voer de volgende handelingen uit om de gebruikersaccount op te geven waaronder deze [!DNL Report Server] wordt uitgevoerd:

   1. Dubbelklik **[!UICONTROL Report Server]** om het [!DNL Properties] venster te openen.

   1. Selecteer het **[!UICONTROL Log On]** tabblad.
   1. Selecteer de **[!UICONTROL This account]** keuzerondje.
   1. Het type of doorbladert voor de rekeningsnaam. Deze rekening moet toestemming hebben om tot de plaats toegang te hebben waar de geproduceerde rapporten worden opgeslagen.

      >[!NOTE]
      >
      >Als [!DNL Report Server] rapporten als dossiers van Microsoft Excel ( [!DNL .xls] of [!DNL .xlsx]) verspreidt, zorg ervoor dat de rekening ook toestemming heeft om Microsoft Excel in werking te stellen.

   1. Ga en bevestig het wachtwoord voor de rekening in.
   1. Klik op **[!UICONTROL OK]**.

1. Klik de [!DNL Report Server] dienst met de rechtermuisknop aan en selecteer **[!UICONTROL Restart]** om de dienst onder de rekening opnieuw te beginnen u specificeerde.
1. Om te controleren of er tijdens het opstarten fouten zijn [!DNL Report Server] opgetreden, klikt u op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**. Deze bevelopeenvolging kan variëren afhankelijk van welke versie van Vensters u gebruikt.

   1. In de linkerruit van het [!DNL Event Viewer] venster, selecteer het logboek van Toepassingen.
   1. In de juiste ruit, zoek gebeurtenissen met Adobe in de [!DNL Source] kolom.
   1. Als u een fout van Adobe vindt, klik de fout tweemaal om het [!DNL Event Properties] venster te tonen. Dit venster verstrekt gedetailleerde informatie over de fout.

      >[!NOTE]
      >
      >Nadat de [!DNL Report Server] dienst begint, [!DNL ReportServer.log] wordt het dossier gecreeerd in de [!DNL Trace] folder van de Server van het Rapport. Dit dossier is ook nuttig voor het oplossen van problemenkwesties met [!DNL Report Server].

U hebt de installatie van voltooid [!DNL Report Server]. [!DNL Report Server] is ontworpen om ononderbroken te lopen. Als u het systeem opnieuw opstart, wordt het automatisch opnieuw [!DNL Report Server] opgestart. Als u moet beginnen en [!DNL Report Server] manueel ophouden, kunt u dit doen gebruikend het [!DNL Services] controlepaneel in Vensters.
