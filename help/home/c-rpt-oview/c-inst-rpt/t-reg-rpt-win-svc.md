---
description: Stappen om de Server van het Rapport te registreren en in werking te stellen.
title: Rapportserver registreren als Windows-service
uuid: 01fc0bbf-9f4a-487e-b1cb-16bf6974a541
exl-id: 46ea5dd4-7041-451e-91e5-f927873fc7d7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Rapportserver registreren als Windows-service{#registering-report-server-as-a-windows-service}

{{eol}}

Stappen om de Server van het Rapport te registreren en in werking te stellen.

Voordat u deze procedure uitvoert, identificeert u de Windows-account waaronder de [!DNL Report Server] service wordt uitgevoerd. Zorg ervoor dat dit account de juiste machtigingen heeft om toegang te krijgen tot de locatie waar gegenereerde rapporten zijn opgeslagen (gebruik dus niet de [!DNL Local System Account]).

Gebruik de onderstaande procedure om te beginnen [!DNL Report Server]. Wanneer u begint [!DNL Report Server] voor het eerst, registreert het zich automatisch als dienst van Vensters.

Wanneer u begint [!DNL Report Server] voor het eerst wordt automatisch verbinding gemaakt met de Adobe-licentieserver om uw digitale certificaat te registreren. Om het registratieproces met succes te voltooien, moet uw computer met Internet worden verbonden wanneer u de volgende stappen uitvoert.

1. Navigeer in Windows naar de map waarin u hebt geïnstalleerd [!DNL Report Server].

   Voorbeeld: D:\Adobe\Report

1. Dubbelklikken **[!UICONTROL ReportServer.exe]**.
1. Bevestig dat [!DNL Report Server] correct wordt uitgevoerd, klikt u op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Services]**. Deze opdrachtvolgorde kan variëren, afhankelijk van de versie van Windows die u gebruikt.
1. Zoek in de lijst met services de vermelding voor [!DNL Report Server] en bevestig dat zijn status Begonnen is en zijn starttype Automatisch is.
1. Ga als volgt te werk om de gebruikersaccount op te geven waaronder [!DNL Report Server] wordt uitgevoerd:

   1. Dubbelklikken **[!UICONTROL Report Server]** om de [!DNL Properties] venster.

   1. Selecteer **[!UICONTROL Log On]** tab.
   1. Selecteer **[!UICONTROL This account]** keuzerondje.
   1. Typ of blader naar de accountnaam. Dit account moet toestemming hebben om toegang te krijgen tot de locatie waar gegenereerde rapporten worden opgeslagen.

      >[!NOTE]
      >
      >Indien [!DNL Report Server] verspreidt rapporten als Microsoft Excel ( [!DNL .xls] of [!DNL .xlsx]), moet u ervoor zorgen dat de account ook gemachtigd is om Microsoft Excel uit te voeren.

   1. Voer het wachtwoord voor de account in en bevestig dit.
   1. Klik op **[!UICONTROL OK]**.

1. Klik met de rechtermuisknop op de knop [!DNL Report Server] service en selecteer **[!UICONTROL Restart]** om de service opnieuw te starten onder de account die u hebt opgegeven.
1. Controleren of [!DNL Report Server] heeft bij het opstarten fouten opgelopen en klikt u op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**. Deze opdrachtvolgorde kan variëren, afhankelijk van de versie van Windows die u gebruikt.

   1. In het linkerdeelvenster van het dialoogvenster [!DNL Event Viewer] selecteert u het logbestand van toepassingen.
   1. Zoek in het rechterdeelvenster naar gebeurtenissen met Adobe in het dialoogvenster [!DNL Source] kolom.
   1. Als u een fout van Adobe vindt, dubbelklikt u op de fout om de fout weer te geven [!DNL Event Properties] venster. Dit venster bevat gedetailleerde informatie over de fout.

      >[!NOTE]
      >
      >Na de [!DNL Report Server] service start, het bestand [!DNL ReportServer.log] wordt gecreeerd in de Server van het Rapport [!DNL Trace] directory. Dit bestand is ook handig voor het oplossen van problemen met [!DNL Report Server].

U hebt de installatie van [!DNL Report Server]. [!DNL Report Server] is ontworpen om continu te worden uitgevoerd. Als u de computer opnieuw opstart, [!DNL Report Server] wordt automatisch opnieuw gestart. Als u moet starten en stoppen [!DNL Report Server] kunt u dit handmatig doen met de [!DNL Services] bedieningspaneel in Windows.
