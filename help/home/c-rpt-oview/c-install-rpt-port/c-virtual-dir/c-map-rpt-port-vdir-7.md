---
description: Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 7.0 of hoger) in kaart te brengen.
solution: Analytics
title: Het Portaal van het Rapport van de afbeelding aan een Virtuele Folder (IIS 7.0 of hoger)
topic: Data workbench
uuid: 9d18fb85-f9d7-48b6-a19b-1e7b68a5adca
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het Portaal van het Rapport van de afbeelding aan een Virtuele Folder (IIS 7.0 of hoger){#mapping-report-portal-to-a-virtual-directory-iis-or-higher}

Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 7.0 of hoger) in kaart te brengen.

Momenteel, hebben de meeste Beheerde cliënten van de Dienst servers met het werkende systeem van de Server 2008 van Vensters en IIS 7.0 of hogere Webserver.

## Voorwaarden {#section-7b1cff24fc4f4c8591540b78de686f2f}

* Zorg ervoor dat het ASPIS en de [!DNL ASP.Net] componenten voor IIS 7.0 of hoger geïnstalleerd zijn.
* Zorg ervoor de gebruiker van het Web IIS [!DNL Modify] toegang tot het [!DNL E:\Portal\data\users.mdb] dossier heeft. U kunt dat veranderen door op het **[!UICONTROL users.mdb]** dossier en onder met de rechtermuisknop te klikken [!DNL Properties], ga naar de [!DNL Security] tabel. Als u niet de vermelde Gebruiker ziet van het Web IIS of niet de capaciteit hebt om de Gebruiker van het Web IIS aan de lijst toe te voegen, geef eenvoudig de [!DNL Users] groep de [!DNL Modify] toegang.

* Zorg ervoor welke gebruikersrekening wordt gebruikt om in werking te stellen [!DNL Application Pools] ook heeft [!DNL Modify] toegang tot de [!DNL E:\Portal\data\users.mdb] en [!DNL C:\Windows\Temp\] omslagen.

## Installatiestappen {#section-2a6476a221fa43dfa91866c0d41f82e5}

1. Op de machine waar [!DNL Report Portal] wordt geïnstalleerd, begin de [!DNL IIS Manager]:

   **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services (IIS) Manager]**.

1. Selecteer **[!UICONTROL Local Machine]** > **[!UICONTROL Sites]** > **[!UICONTROL Default Web Site]**.

1. Klik met de rechtermuisknop **[!UICONTROL Default Web Site]** en selecteer **[!UICONTROL Add Virtual Directory]**.

1. Voor een alias, ga Portaal in.
1. Voor de fysieke weg, ga binnen [!DNL E:\Portal\PortalASP].
1. Klik op **[!UICONTROL OK]**.

   De virtuele folder die u creeerde verschijnt onder de [!DNL Default Web Site].

1. Voeg de volgende virtuele folders onder de virtuele folder toe die u enkel creeerde.

   | Maak dit alias... | Voor dit fysieke middel |
   |---|---|
   | Kern | [!DNL E:\Portal\PortalFiles\Core] |
   | CSS | [!DNL E:\Portal\PortalFiles\CSS] |
   | Afbeeldingen | [!DNL E:\Portal\PortalFiles\Images] |
   | Uitvoer | Fysieke plaats van de folder waarin de output voor uw rapportreeksen [!DNL Report Server] bewaart. De outputomslag kan overal worden gevestigd en kan om het even wat worden genoemd. Het bevat een subfolder voor elke rapportreeks. U kunt het verwijderen [!DNL E:\Portal\PortalFiles\Output], maar het [!DNL profiles.xml] naar de fysieke locatie van het uitvoerbestand verplaatsen. |

1. Wanneer gebeëindigd, verifieer dat IIS vier nieuwe virtuele folders toont. Zorg ervoor dat de folderstructuur één ouderomslag (met de zelfde naam zoals uw portaal) en vier subfolders heeft.
1. Klik op **[!UICONTROL Application Pools]**, dan **[!UICONTROL DefaultAppPool]** (veronderstellend dat is diegene u opstelling met uw portaal).

1. Klik op **[!UICONTROL Advanced Settings]** en selecteer Waar voor de Enable Toepassingen met 32 bits.
1. Om het te krijgen [!DNL Portal] aan het werk, moet u het in een toepassing omzetten. Na vestiging klikken de virtuele folders, op de Portaalvirtuele folder met de rechtermuisknop aan en selecteren **[!UICONTROL Convert to Application]**.

## Extra tips en trucs {#section-ff84ab3f66c94620a6a11f0e60471d44}

* U kunt het downloaden [!DNL Portal] van Softdocs onder **[!UICONTROL Softdocs]** > **[!UICONTROL Report Portal]**. U kunt eenvoudig downloaden [!DNL ReportPortal-Release-1-0-0-7.zip].

* Je hebt het niet meer nodig [!DNL ReportPortalSetup.xml], dus het kan worden verwijderd.
* Met het oog op standaardisering, plaats de inhoud van dit zip-bestand in [!DNL E:\Portal].
* Om de server SMTP voor beheerde de dienstencliënten te bepalen, kunt u hier gaan kijken.
* Zet in een verzoek met NetOps om de ingang van de domeinnaam in IIS voor de rapportserver in iets vriendelijker te veranderen - bijvoorbeeld, [!DNL reports.clientname.insight.omniture.com], zodat uw algemeen portaal URL is [!DNL http://reports.clientname.insight.omniture.com/Portal]. Vorm uw [!DNL email.asa] dossier zodra deze verandering in plaats is gezet.

