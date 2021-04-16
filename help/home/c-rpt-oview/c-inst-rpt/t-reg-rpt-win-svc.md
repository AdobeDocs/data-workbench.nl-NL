---
description: Stappen om de Server van het Rapport te registreren en in werking te stellen.
title: Rapportserver registreren als Windows-service
uuid: 01fc0bbf-9f4a-487e-b1cb-16bf6974a541
exl-id: 46ea5dd4-7041-451e-91e5-f927873fc7d7
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Rapportserver registreren als een Windows-service{#registering-report-server-as-a-windows-service}

Stappen om de Server van het Rapport te registreren en in werking te stellen.

Alvorens u deze procedure uitvoert, identificeer de rekening van Vensters waaronder de [!DNL Report Server] dienst zal lopen. Zorg ervoor dat dit account de juiste machtigingen heeft om toegang te krijgen tot de locatie waar gegenereerde rapporten zijn opgeslagen (gebruik dus niet [!DNL Local System Account]).

Gebruik de onderstaande procedure om [!DNL Report Server] te starten. Wanneer u [!DNL Report Server] voor het eerst begint, registreert het automatisch als dienst van Vensters.

Wanneer u [!DNL Report Server] voor het eerst start, wordt er automatisch verbinding gemaakt met de Adobe-licentieserver om uw digitale certificaat te registreren. Om het registratieproces met succes te voltooien, moet uw computer met Internet worden verbonden wanneer u de volgende stappen uitvoert.

1. Navigeer in Windows naar de map waarin u [!DNL Report Server] hebt geïnstalleerd.

   Voorbeeld: D:\Adobe\Report

1. Dubbelklik op **[!UICONTROL ReportServer.exe]**.
1. Om te bevestigen dat [!DNL Report Server] correct loopt, klik **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Services]**. Deze opdrachtvolgorde kan variëren, afhankelijk van de versie van Windows die u gebruikt.
1. Zoek in de servicelijst de vermelding voor [!DNL Report Server] en bevestig dat de status is gestart en dat het opstarttype Automatisch is.
1. Ga als volgt te werk om de gebruikersaccount op te geven waaronder [!DNL Report Server] wordt uitgevoerd:

   1. Dubbelklik op **[!UICONTROL Report Server]** om het venster [!DNL Properties] te openen.

   1. Selecteer het tabblad **[!UICONTROL Log On]**.
   1. Selecteer het keuzerondje **[!UICONTROL This account]**.
   1. Typ of blader naar de accountnaam. Dit account moet toestemming hebben om toegang te krijgen tot de locatie waar gegenereerde rapporten worden opgeslagen.

      >[!NOTE]
      >
      >Als [!DNL Report Server] rapporten als dossiers van Microsoft Excel ( [!DNL .xls] of [!DNL .xlsx]) verspreidt, zorg ervoor dat de rekening ook toestemming heeft om Microsoft Excel in werking te stellen.

   1. Voer het wachtwoord voor de account in en bevestig dit.
   1. Klik op **[!UICONTROL OK]**.

1. Klik met de rechtermuisknop op de [!DNL Report Server]-service en selecteer **[!UICONTROL Restart]** om de service opnieuw te starten onder de account die u hebt opgegeven.
1. Om te controleren of [!DNL Report Server] fouten ondervond tijdens het opstarten, klikt u op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**. Deze opdrachtvolgorde kan variëren, afhankelijk van de versie van Windows die u gebruikt.

   1. Selecteer in het linkerdeelvenster van het venster [!DNL Event Viewer] het logboek Toepassingen.
   1. Zoek in het rechterdeelvenster naar gebeurtenissen met Adobe in de kolom [!DNL Source].
   1. Als u een fout van Adobe vindt, klik de fout tweemaal om het [!DNL Event Properties] venster te tonen. Dit venster bevat gedetailleerde informatie over de fout.

      >[!NOTE]
      >
      >Nadat de service [!DNL Report Server] is gestart, wordt het bestand [!DNL ReportServer.log] gemaakt in de map Report Server [!DNL Trace]. Dit bestand is ook handig voor het oplossen van problemen met [!DNL Report Server].

U hebt de installatie van [!DNL Report Server] voltooid. [!DNL Report Server] is ontworpen om continu te worden uitgevoerd. Als u de computer opnieuw opstart, wordt [!DNL Report Server] automatisch opnieuw opgestart. Als u [!DNL Report Server] manueel moet beginnen en ophouden, kunt u dit doen gebruikend [!DNL Services] controlepaneel in Vensters.
