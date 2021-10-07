---
description: Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 7.0 of hoger) in kaart te brengen.
title: Het Portaal van het Rapport van de toewijzing aan een Virtuele Folder (IIS 7.0 of hoger)
uuid: 9d18fb85-f9d7-48b6-a19b-1e7b68a5adca
exl-id: 2fa3439a-1fe5-4a20-83db-d233ae8b5263
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# Het Portaal van het Rapport van de toewijzing aan een Virtuele Folder (IIS 7.0 of hoger){#mapping-report-portal-to-a-virtual-directory-iis-or-higher}

Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 7.0 of hoger) in kaart te brengen.

Momenteel, hebben de meeste Beheerde cliënten van de Dienst servers met het werkende systeem van de Server 2008 van Vensters en IIS 7.0 of hogere Webserver.

## Vereisten {#section-7b1cff24fc4f4c8591540b78de686f2f}

* Zorg ervoor dat de componenten ASP en [!DNL ASP.Net] voor IIS 7.0 of hoger geïnstalleerd zijn.
* Zorg ervoor de gebruiker van het Web IIS [!DNL Modify] toegang tot het [!DNL E:\Portal\data\users.mdb] dossier heeft. U kunt dat wijzigen door met de rechtermuisknop op het **[!UICONTROL users.mdb]**-bestand te klikken en onder [!DNL Properties] naar het tabblad [!DNL Security] te gaan. Als u niet de vermelde Gebruiker ziet van het Web IIS of niet de capaciteit hebt om de Gebruiker van het Web IIS aan de lijst toe te voegen, geef eenvoudig [!DNL Users] groep [!DNL Modify] toegang.

* Zorg ervoor welk gebruikersaccount wordt gebruikt om [!DNL Application Pools] in werking te stellen ook [!DNL Modify] toegang tot [!DNL E:\Portal\data\users.mdb] en  [!DNL C:\Windows\Temp\] omslagen heeft.

## Installatiestappen {#section-2a6476a221fa43dfa91866c0d41f82e5}

1. Start [!DNL IIS Manager] op de computer waarop [!DNL Report Portal] is geïnstalleerd:

   **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services (IIS) Manager]**.

1. Selecteer **[!UICONTROL Local Machine]** > **[!UICONTROL Sites]** > **[!UICONTROL Default Web Site]**.

1. Klik met de rechtermuisknop **[!UICONTROL Default Web Site]** en selecteer **[!UICONTROL Add Virtual Directory]**.

1. Voer voor een alias de waarde Portal in.
1. Voer [!DNL E:\Portal\PortalASP] in voor het fysieke pad.
1. Klik op **[!UICONTROL OK]**.

   De virtuele folder die u creeerde verschijnt onder [!DNL Default Web Site].

1. Voeg de volgende virtuele folders onder de virtuele folder toe die u enkel creeerde.

   | Deze alias maken... | Voor deze fysieke bron |
   |---|---|
   | Kern | [!DNL E:\Portal\PortalFiles\Core] |
   | CSS | [!DNL E:\Portal\PortalFiles\CSS] |
   | Afbeeldingen | [!DNL E:\Portal\PortalFiles\Images] |
   | Uitvoer | Fysieke plaats van de folder waarin [!DNL Report Server] de output voor uw rapportreeksen bewaart. De uitvoermap kan overal worden gevonden en een naam krijgen. Het bevat een subfolder voor elke rapportreeks. U kunt [!DNL E:\Portal\PortalFiles\Output] schrappen, maar [!DNL profiles.xml] verplaatsen naar de fysieke plaats van het dossier van de Output. |

1. Wanneer gebeëindigd, verifieer dat IIS vier nieuwe virtuele folders toont. Zorg ervoor dat de mappenstructuur één bovenliggende map (met dezelfde naam als de portal) en vier submappen heeft.
1. Klik op **[!UICONTROL Application Pools]**, dan **[!UICONTROL DefaultAppPool]** (veronderstellend dat is die u opstelling met uw portaal).

1. Klik op **[!UICONTROL Advanced Settings]** en selecteer Waar voor Enable 32-bits Toepassingen.
1. Als u de [!DNL Portal] wilt laten werken, moet u deze converteren naar een toepassing. Nadat u de virtuele mappen hebt ingesteld, klikt u met de rechtermuisknop op de virtuele Portal-map en selecteert u **[!UICONTROL Convert to Application]**.

## Extra tips en trucs {#section-ff84ab3f66c94620a6a11f0e60471d44}

* U kunt [!DNL Portal] van Softdocs onder **[!UICONTROL Softdocs]** > **[!UICONTROL Report Portal]** downloaden. U kunt [!DNL ReportPortal-Release-1-0-0-7.zip] eenvoudig downloaden.

* U hebt [!DNL ReportPortalSetup.xml] niet meer nodig, zodat kan het worden geschrapt.
* Plaats, met het oog op standaardisering, de inhoud van dit ZIP-bestand in [!DNL E:\Portal].
* Om de server SMTP voor beheerde de dienstencliënten te bepalen, kunt u hier gaan kijken.
* Zet in een verzoek met NetOps om de ingang van de domeinnaam in IIS voor de rapportserver in iets vriendelijker - bijvoorbeeld, [!DNL reports.clientname.insight.omniture.com] te veranderen, zodat uw algemene portaal URL [!DNL https://reports.clientname.insight.omniture.com/Portal] is. Configureer uw [!DNL email.asa]-bestand nadat deze wijziging is aangebracht.
