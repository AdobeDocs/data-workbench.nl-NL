---
description: Het Portaal van het rapport wordt samengesteld uit een reeks pagina's van de toepassingsserver (ASPs) en ondersteunende dossiers.
solution: Analytics
title: Installeer de Poort van het Rapport Dossiers van de Toepassing
topic: Data workbench
uuid: 483a7401-1bb4-4a71-b8c7-e70ff1b129e7
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Installeer de Poort van het Rapport Dossiers van de Toepassing{#install-the-report-portal-application-files}

Het Portaal van het rapport wordt samengesteld uit een reeks pagina&#39;s van de toepassingsserver (ASPs) en ondersteunende dossiers.

Om te installeren [!DNL Report Portal], moet u deze dossiers uit het distributiedossier halen dat u van Adobe ontving en hen installeren op de machine waar Microsoft IIS loopt.

**Om de[!DNL Report Portal]toepassingsdossiers te installeren**

1. Als u niet reeds dit hebt gedaan, download het installatiepakket (.zip dossier) voor [!DNL Report Portal] van de plaats van FTP van Adobe.
1. Op de machine waar IIS loopt, haal de dossiers in het installatiepakket aan om het even welke plaats. Deze stap installeert volgende subfolders en dossiers in de omslag VSVirtualPortalName.

   | Map of bestand | Beschrijving |
   |---|---|
   | [!DNL \data\users.mdb] | Gegevensbestand met de lijst van gemachtigde [!DNL Report Portal] gebruikers. |
   | [!DNL \PortalASP\] | Omslag die de dossiers bevat van het ASPIS die omhoog maken [!DNL Report Portal]. |
   | [!DNL \PortalFiles\] | Omslag die vijf subfolders (Kern, CSS, HTC, Beelden, en Output) bevat die ondersteunende die dossiers bevatten door worden gebruikt [!DNL Report Portal]. |
   | [!DNL ReportPortalSetup.xml] | Het dossier van de configuratie u gebruikt om de virtuele folders te bepalen verbonden aan [!DNL Report Portal] (gebruikt met IIS 6.0 slechts). |

   De folder kijkt als het volgende voorbeeld:

   ![](assets/rptPort_scrn_installDir.png)

   >[!NOTE]
   >
   >De naam van de folder kan van de naam verschillen die in het voorbeeld wordt getoond.

1. Noem de omslag VSVirtualPortalName (of andere naam) aan wat anders u als wortel virtuele folder van uw wilt gebruiken [!DNL Report Portal] (hierna genoemd *PortalName*). Voor meer informatie over virtuele folders, zie de volgende sectie.
