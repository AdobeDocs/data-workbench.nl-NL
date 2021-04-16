---
description: Het Portaal van het rapport wordt samengesteld uit een reeks pagina's van de toepassingsserver (ASPs) en ondersteunende dossiers.
title: Installeer de Poorttoepassingsbestanden van het Rapport
uuid: 483a7401-1bb4-4a71-b8c7-e70ff1b129e7
exl-id: 0eb7805c-d8f6-4cfd-834e-babc1818ebc0
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Installeer de Poorttoepassingsdossiers van het Rapport{#install-the-report-portal-application-files}

Het Portaal van het rapport wordt samengesteld uit een reeks pagina&#39;s van de toepassingsserver (ASPs) en ondersteunende dossiers.

Om [!DNL Report Portal] te installeren, moet u deze dossiers uit het distributiedossier halen dat u van Adobe ontving en hen installeren op de machine waar Microsoft IIS loopt.

**De  [!DNL Report Portal] toepassingsbestanden installeren**

1. Als u dit nog niet hebt gedaan, downloadt u het installatiepakket (.zip-bestand) voor [!DNL Report Portal] van de FTP-site Adobe.
1. Extraheer de bestanden in het installatiepakket naar een willekeurige locatie op de computer waarop IIS wordt uitgevoerd. Deze stap installeert de volgende subfolders en de dossiers in de omslag VSVirtualPortalName.

   | Map of bestand | Beschrijving |
   |---|---|
   | [!DNL \data\users.mdb] | Database met de lijst van geautoriseerde [!DNL Report Portal] gebruikers. |
   | [!DNL \PortalASP\] | Map met de ASP-bestanden waaruit [!DNL Report Portal] bestaat. |
   | [!DNL \PortalFiles\] | Map met vijf submappen (Core, CSS, HTC, Images en Output) die ondersteunende bestanden bevatten die worden gebruikt door [!DNL Report Portal]. |
   | [!DNL ReportPortalSetup.xml] | Het dossier van de configuratie u gebruikt om de virtuele folders te bepalen verbonden aan [!DNL Report Portal] (slechts gebruikt met IIS 6.0). |

   De map ziet er als volgt uit:

   ![](assets/rptPort_scrn_installDir.png)

   >[!NOTE]
   >
   >De naam van de map kan afwijken van de naam in het voorbeeld.

1. Wijzig de naam van de map VSVirtualPortalName (of een andere naam) in de hoofdmap van de virtuele map [!DNL Report Portal] (hierna *PortalName* genoemd). Zie de volgende sectie voor meer informatie over virtuele mappen.
