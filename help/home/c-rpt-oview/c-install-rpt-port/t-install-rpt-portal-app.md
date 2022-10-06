---
description: Het Portaal van het rapport wordt samengesteld uit een reeks pagina's van de toepassingsserver (ASPs) en ondersteunende dossiers.
title: Installeer de Poorttoepassingsbestanden van het Rapport
uuid: 483a7401-1bb4-4a71-b8c7-e70ff1b129e7
exl-id: 0eb7805c-d8f6-4cfd-834e-babc1818ebc0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Installeer de Poorttoepassingsbestanden van het Rapport{#install-the-report-portal-application-files}

{{eol}}

Het Portaal van het rapport wordt samengesteld uit een reeks pagina&#39;s van de toepassingsserver (ASPs) en ondersteunende dossiers.

Als u het dialoogvenster [!DNL Report Portal], moet u deze dossiers uit het distributiedossier halen dat u van Adobe ontving en hen installeren op de machine waar Microsoft IIS loopt.

**Als u het dialoogvenster [!DNL Report Portal] toepassingsbestanden**

1. Als u dit nog niet hebt gedaan, downloadt u het installatiepakket (.zip-bestand) voor het [!DNL Report Portal] op de FTP-site Adobe.
1. Extraheer de bestanden in het installatiepakket naar een willekeurige locatie op de computer waarop IIS wordt uitgevoerd. Deze stap installeert de volgende subfolders en de dossiers in de omslag VSVirtualPortalName.

   | Map of bestand | Beschrijving |
   |---|---|
   | [!DNL \data\users.mdb] | Database met de lijst van geautoriseerde [!DNL Report Portal] gebruikers. |
   | [!DNL \PortalASP\] | Map met ASP-bestanden waaruit de bestanden bestaan [!DNL Report Portal]. |
   | [!DNL \PortalFiles\] | Map met vijf submappen (Core, CSS, HTC, Images en Output) die ondersteunende bestanden bevatten die worden gebruikt door [!DNL Report Portal]. |
   | [!DNL ReportPortalSetup.xml] | Het dossier van de configuratie u gebruikt om de virtuele folders te bepalen verbonden aan [!DNL Report Portal] (alleen voor IIS 6.0). |

   De map ziet er als volgt uit:

   ![](assets/rptPort_scrn_installDir.png)

   >[!NOTE]
   >
   >De naam van de map kan afwijken van de naam in het voorbeeld.

1. Wijzig de naam van de map VSVirtualPortalName (of een andere naam) in de hoofdmap die u als virtuele map van uw [!DNL Report Portal] (hierna *PortalName*). Zie de volgende sectie voor meer informatie over virtuele mappen.
