---
description: Het Portaal van het rapport wordt samengesteld uit een reeks pagina's van de toepassingsserver (ASPs) en ondersteunende dossiers.
solution: Analytics
title: Installeer de Poorttoepassingsbestanden van het Rapport
uuid: 483a7401-1bb4-4a71-b8c7-e70ff1b129e7
translation-type: tm+mt
source-git-commit: 7521fe7f5fabe8e1be26e140ffff577a42fce88b

---


# Installeer de Poorttoepassingsbestanden van het Rapport{#install-the-report-portal-application-files}

Het Portaal van het rapport wordt samengesteld uit een reeks pagina&#39;s van de toepassingsserver (ASPs) en ondersteunende dossiers.

Als u de toepassing wilt installeren [!DNL Report Portal], moet u deze bestanden uitpakken uit het distributiebestand dat u van Adobe hebt ontvangen en deze installeren op de computer waarop Microsoft IIS wordt uitgevoerd.

**De[!DNL Report Portal]toepassingsbestanden installeren**

1. Als u dit nog niet hebt gedaan, downloadt u het installatiepakket (.zip-bestand) voor het bestand [!DNL Report Portal] van de Adobe FTP-site.
1. Extraheer de bestanden in het installatiepakket naar een willekeurige locatie op de computer waarop IIS wordt uitgevoerd. Deze stap installeert de volgende subfolders en de dossiers in de omslag VSVirtualPortalName.

   | Map of bestand | Beschrijving |
   |---|---|
   | [!DNL \data\users.mdb] | Database met de lijst met geautoriseerde [!DNL Report Portal] gebruikers. |
   | [!DNL \PortalASP\] | Map met de ASP-bestanden waaruit de bestanden bestaan [!DNL Report Portal]. |
   | [!DNL \PortalFiles\] | Map met vijf submappen (Core, CSS, HTC, Images en Output) die ondersteunende bestanden bevatten die worden gebruikt door [!DNL Report Portal]. |
   | [!DNL ReportPortalSetup.xml] | Het dossier van de configuratie u gebruikt om de virtuele folders te bepalen verbonden aan [!DNL Report Portal] (die met IIS 6.0 slechts wordt gebruikt). |

   De map ziet er als volgt uit:

   ![](assets/rptPort_scrn_installDir.png)

   >[!NOTE]
   >
   >De naam van de map kan afwijken van de naam in het voorbeeld.

1. Wijzig de naam van de map VSVirtualPortalName (of een andere naam) in de virtuele hoofdmap van uw [!DNL Report Portal] (hierna *PortalName* genoemd). Zie de volgende sectie voor meer informatie over virtuele mappen.
