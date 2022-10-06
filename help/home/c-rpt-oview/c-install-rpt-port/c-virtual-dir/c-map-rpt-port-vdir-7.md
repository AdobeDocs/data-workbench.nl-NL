---
description: Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 7.0 of hoger) in kaart te brengen.
title: Het Portaal van het Rapport van de toewijzing aan een Virtuele Folder (IIS 7.0 of hoger)
uuid: 9d18fb85-f9d7-48b6-a19b-1e7b68a5adca
exl-id: 2fa3439a-1fe5-4a20-83db-d233ae8b5263
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Het Portaal van het Rapport van de toewijzing aan een Virtuele Folder (IIS 7.0 of hoger){#mapping-report-portal-to-a-virtual-directory-iis-or-higher}

{{eol}}

Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 7.0 of hoger) in kaart te brengen.

Momenteel, hebben de meeste Beheerde cliënten van de Dienst servers met het werkende systeem van de Server 2008 van Vensters en IIS 7.0 of hogere Webserver.

## Vereisten {#section-7b1cff24fc4f4c8591540b78de686f2f}

* Zorg ervoor dat ASP en [!DNL ASP.Net] componenten worden geïnstalleerd voor IIS 7.0 of hoger.
* Zorg ervoor de gebruiker van het Web IIS heeft [!DNL Modify] toegang tot de [!DNL E:\Portal\data\users.mdb] bestand. U kunt dat wijzigen door met de rechtermuisknop op de knop **[!UICONTROL users.mdb]** bestand en onder [!DNL Properties], ga naar de [!DNL Security] tab. Als u niet de vermelde Gebruiker ziet van het Web IIS of niet de capaciteit hebt om de Gebruiker van het Web IIS aan de lijst toe te voegen, geef eenvoudig [!DNL Users] de groep [!DNL Modify] toegang.

* Controleer of een gebruikersaccount wordt gebruikt voor het uitvoeren van de [!DNL Application Pools] ook [!DNL Modify] toegang tot de [!DNL E:\Portal\data\users.mdb] en de [!DNL C:\Windows\Temp\] mappen.

## Installatiestappen {#section-2a6476a221fa43dfa91866c0d41f82e5}

1. Op de computer [!DNL Report Portal] is geïnstalleerd, start de [!DNL IIS Manager]:

   **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services (IIS) Manager]**.

1. Selecteren **[!UICONTROL Local Machine]** > **[!UICONTROL Sites]** > **[!UICONTROL Default Web Site]**.

1. Klikken met rechtermuisknop **[!UICONTROL Default Web Site]** en selecteert u **[!UICONTROL Add Virtual Directory]**.

1. Voer voor een alias de waarde Portal in.
1. Voor het fysieke pad voert u [!DNL E:\Portal\PortalASP].
1. Klik op **[!UICONTROL OK]**.

   De virtuele map die u hebt gemaakt, verschijnt onder de [!DNL Default Web Site].

1. Voeg de volgende virtuele folders onder de virtuele folder toe die u enkel creeerde.

   | Deze alias maken... | Voor deze fysieke bron |
   |---|---|
   | Kern | [!DNL E:\Portal\PortalFiles\Core] |
   | CSS | [!DNL E:\Portal\PortalFiles\CSS] |
   | Afbeeldingen | [!DNL E:\Portal\PortalFiles\Images] |
   | Uitvoer | Fysieke locatie van de map waarin [!DNL Report Server] Slaat de output voor uw rapportreeksen op. De uitvoermap kan overal worden gevonden en een naam krijgen. Het bevat een subfolder voor elke rapportreeks. U kunt de [!DNL E:\Portal\PortalFiles\Output], maar de [!DNL profiles.xml] naar de fysieke locatie van het uitvoerbestand. |

1. Wanneer gebeëindigd, verifieer dat IIS vier nieuwe virtuele folders toont. Zorg ervoor dat de mappenstructuur één bovenliggende map (met dezelfde naam als de portal) en vier submappen heeft.
1. Klikken op **[!UICONTROL Application Pools]** vervolgens **[!UICONTROL DefaultAppPool]** (ervan uitgaande dat dit het portaal is dat u hebt ingesteld).

1. Klikken op **[!UICONTROL Advanced Settings]** en selecteer Waar voor Enable 32-bits Toepassingen.
1. Om de [!DNL Portal] als u wilt werken, moet u de toepassing converteren naar een toepassing. Nadat u de virtuele mappen hebt ingesteld, klikt u met de rechtermuisknop op de virtuele Portal-map en selecteert u **[!UICONTROL Convert to Application]**.

## Extra tips en trucs {#section-ff84ab3f66c94620a6a11f0e60471d44}

* U kunt de [!DNL Portal] van Softdocs onder **[!UICONTROL Softdocs]** > **[!UICONTROL Report Portal]**. U kunt de opdracht [!DNL ReportPortal-Release-1-0-0-7.zip].

* U hebt de opdracht [!DNL ReportPortalSetup.xml]en kan dus worden verwijderd.
* Plaats, met het oog op standaardisering, de inhoud van dit ZIP-bestand in [!DNL E:\Portal].
* Om de server SMTP voor beheerde de dienstencliënten te bepalen, kunt u hier gaan kijken.
* Zet in een verzoek met NetOps om de ingang van de domeinnaam in IIS voor de rapportserver in iets vriendelijker - bijvoorbeeld te veranderen, [!DNL reports.clientname.insight.omniture.com], zodat de URL van uw algemene portaal [!DNL https://reports.clientname.insight.omniture.com/Portal]. Configureer uw [!DNL email.asa] bestand nadat deze wijziging is aangebracht.
