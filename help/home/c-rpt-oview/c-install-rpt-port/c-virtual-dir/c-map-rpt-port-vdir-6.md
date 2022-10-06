---
description: Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 6.0) in kaart te brengen.
title: Het Portaal van het Rapport van de toewijzing aan een Virtuele Folder (IIS 6.0)
uuid: e09d23d7-09de-4180-8260-60527f47aa98
exl-id: 39335705-7391-49af-a63d-c0fe4ca3f8f0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# Het Portaal van het Rapport van de toewijzing aan een Virtuele Folder (IIS 6.0){#mapping-report-portal-to-a-virtual-directory-iis}

{{eol}}

Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 6.0) in kaart te brengen.

De toewijzing van [!DNL Report Portal] aan een virtuele folder op IIS 6.0 impliceert drie afzonderlijke taken:

1. [Het configuratiebestand bewerken](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-6.md#section-eaf1c58935074cfa840dac33e1286520)
1. [Importeer het configuratiebestand in IIS](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-6.md#section-9d61f6bfa93846dcb96973fec5573b19)
1. [Active Server Pages (ASP&#39;s) inschakelen in IIS](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-6.md#section-a7725ec2afc64ffc854c5bd8c5c31802)

U moet alle drie de taken voltooien.

## Het configuratiebestand bewerken {#section-eaf1c58935074cfa840dac33e1286520}

1. Op de computer [!DNL Report Portal] is geïnstalleerd, open \*PortalName* \ ReportPortalSetup.xml in een tekstredacteur zoals Blocnote.

1. Gebruik de vondst-en-vervangeigenschap van de redacteur om (allen vervangen) globaal het koord &quot;VSVirtualPortalName&quot;met de naam van uw portaal te vervangen. Bijvoorbeeld, als u &quot;VisualReportPortal&quot;als naam van uw wilt gebruiken [!DNL Report Portal], zou u &quot;VSVirtualPortalName&quot;zoeken en het vervangen met &quot;VisualReportPortal.&quot;
1. Zoek het volgende element in dit bestand:

   ```
   <IIsWebVirtualDir Location= "/LM/W3SVC/1/Root/PortalName/Output" AccessFlags="AccessRead | AccessScript” AppFriendlyName="Output" . . . >
   ```

1. Stel de [!DNL Path] attribuut aan de fysieke plaats van de folder waarin [!DNL Report Server] Slaat de output voor uw rapportreeksen op.

   De outputomslag kan overal worden gevestigd, kan om het even wat worden genoemd, en bevat een subfolder voor elke rapportreeks.

   >[!NOTE]
   >
   >Dit moet dezelfde map zijn als die u opgeeft in de parameter Uitvoer in het dialoogvenster [!DNL Report.cfg] bestand voor een rapportset. Zie voor meer informatie [Report.cfg-bestanden configureren](../../../../home/c-rpt-oview/c-admin-rpt/c-config-rpt-files.md#concept-cf4b95344fcb4c8c877db91e5f1d345d).

   Het volgende codevoorbeeld laat zien hoe u het [!DNL Path] kenmerk als uw rapporten zijn opgeslagen naar [!DNL E:\VSReport\ReportOutput]:

   ```
   < . . . 
   AppIsolated="2" 
       AppRoot="/LM/W3SVC/1/Root/PortalName/OutputFolder" 
       DirBrowseFlags="DirBrowseShowDate | DirBrowseShowTime |...  
       Path="E:\VSReport\ReportOutput"
   ```

   >[!NOTE]
   >
   >Het is van essentieel belang dat de [!DNL Path] wordt ingesteld.

1. Als u de standaardinstelling hebt gewijzigd [!DNL Path] van de [!DNL Output] element, verplaatsen [!DNL profiles.xml] bestand van de *\PortalName*\PortalFiles\Output map naar de uitvoermap die u hebt opgegeven in stap 4. In het bovenstaande voorbeeld verplaatst u [!DNL profiles.xml] tot [!DNL E:\VSReport\ReportOutput].

1. Controleer of de [!DNL Path] kenmerken voor alle andere [!DNL IIsWebVirtualDir] elementen worden toegewezen aan de juiste locatie door te zoeken naar alle instanties van [!DNL C:\Inetpub\wwwroot] en elke koppeling vervangen door het juiste pad.

1. Sla het bestand op. Als u het oorspronkelijke bestand wilt behouden, kunt u het configuratiebestand onder een andere naam opslaan.

## Om het Dossier van de Configuratie in IIS in te voeren {#section-9d61f6bfa93846dcb96973fec5573b19}

1. Op de computer [!DNL Report Portal] is geïnstalleerd, begin de Manager IIS gebruikend **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Systems (IIS) Manager]**.

1. Selecteren **[!UICONTROL (local computer)]** > **[!UICONTROL Web Sites]** > **[!UICONTROL Default Web Site]**.

1. Klikken met rechtermuisknop **[!UICONTROL Default Web Site]** en selecteert u **[!UICONTROL New]** > **[!UICONTROL Virtual Directory]** (van bestand).

1. Selecteer **[!UICONTROL ReportPortalSetup.xml]** bestand en klik op **[!UICONTROL Read File]**.

1. Controleer of er zes virtuele mappen worden vermeld voor uw [!DNL Report Portal] zoals getoond in het volgende voorbeeld.

   ![](assets/rptPort_dia_VirDirs.png)

   Als er geen zes virtuele mappen worden weergegeven of als u een foutbericht ontvangt, klikt u op **[!UICONTROL Cancel]** en controleer het configuratiebestand op fouten.

1. Selecteer de eerste virtuele map in de lijst (de map die het bovenliggende item van de andere vijf is) en klik op **[!UICONTROL OK]**. IIS voert de afbeeldingen in en voegt de virtuele folders aan de StandaardWebsite toe.

   Zorg ervoor dat de resulterende mapstructuur één bovenliggende map (met dezelfde naam als uw portal) en vijf submappen heeft, zoals in het volgende voorbeeld wordt getoond.

   ![](assets/rptPort_scrn_VirDirs_Installed.png)

1. Klik elke virtuele folder om ervoor te zorgen dat IIS van de fysieke folder kan de plaats bepalen het vertegenwoordigt. Als in IIS een fout wordt weergegeven, klikt u met de rechtermuisknop op de naam van de virtuele map en controleert u of de [!DNL Local Path] veld verwijst naar de juiste fysieke map.

## Om de Actieve Pagina&#39;s van de Server (ASPISs) op IIS toe te laten {#section-a7725ec2afc64ffc854c5bd8c5c31802}

Te gebruiken [!DNL Report Portal], ASPs moet op IIS worden toegelaten. (Standaard zijn ASP&#39;s uitgeschakeld wanneer IIS 6.0 is geïnstalleerd.) Gebruik de volgende procedure om te verifiëren dat ASPs op uw IIS wordt toegelaten.

1. Selecteer in het venster IIS Manager de optie **[!UICONTROL (local computer)]** > **[!UICONTROL Web Service Extensions]**.
1. Controleer of de [!DNL Active Server Pages] extensie is ingesteld op [!DNL Allowed].

   ![](assets/report_aspenable.png)

1. Als hun status is verboden, selecteert u **[!UICONTROL Active Server Pages]** en klik op **[!UICONTROL Allow]**.
1. Sluit IIS Manager.
