---
description: Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 6.0) in kaart te brengen.
solution: Analytics
title: Het Portaal van het Rapport van de afbeelding aan een Virtuele Folder (IIS 6.0)
topic: Data workbench
uuid: e09d23d7-09de-4180-8260-60527f47aa98
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het Portaal van het Rapport van de afbeelding aan een Virtuele Folder (IIS 6.0){#mapping-report-portal-to-a-virtual-directory-iis}

Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 6.0) in kaart te brengen.

Het in kaart brengen van [!DNL Report Portal] aan een virtuele folder op IIS 6.0 impliceert drie afzonderlijke taken:

1. [Geef het configuratiedossier uit](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-6.md#section-eaf1c58935074cfa840dac33e1286520)
1. [De invoer van het configuratiedossier in IIS](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-6.md#section-9d61f6bfa93846dcb96973fec5573b19)
1. [Laat de Actieve Pagina&#39;s van de Server (ASPs) op IIS toe](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-6.md#section-a7725ec2afc64ffc854c5bd8c5c31802)

U moet alle drie taken voltooien.

## Om het Dossier van de Configuratie uit te geven {#section-eaf1c58935074cfa840dac33e1286520}

1. Op de machine waar geïnstalleerd [!DNL Report Portal] is, open \*PortalName* \ ReportPortalSetup.xml in een tekstredacteur zoals Blocnote.

1. Gebruik de vondst-en-vervangen eigenschap van de redacteur om globally te vervangen (vervang allen) het koord &quot;VSVirtualPortalName&quot;met de naam van uw portaal. Bijvoorbeeld, als u &quot;VisualReportPortal&quot;als naam van uw wilt gebruiken, zou u naar &quot;VSVirtualPortalName&quot;zoeken en het vervangen met &quot;VisualReportPortal.&quot; [!DNL Report Portal]
1. Bepaal de plaats van het volgende element in dit dossier:

   ```
   <IIsWebVirtualDir Location= "/LM/W3SVC/1/Root/PortalName/Output" AccessFlags="AccessRead | AccessScript” AppFriendlyName="Output" . . . >
   ```

1. Plaats de [!DNL Path] attributen van dit element aan de fysieke plaats van de folder waarin de output voor uw rapportreeksen [!DNL Report Server] opslaat.

   De outputomslag kan overal worden gevestigd, kan om het even wat worden genoemd, en bevat een subfolder voor elke rapportreeks.

   >[!NOTE]
   >
   >Dit moet de zelfde folder zijn die u in de parameter van de Wortel van de Output in het [!DNL Report.cfg] dossier voor een rapportreeks specificeert. Voor meer informatie, zie het [Vormen Dossiers](../../../../home/c-rpt-oview/c-admin-rpt/c-config-rpt-files.md#concept-cf4b95344fcb4c8c877db91e5f1d345d)Report.cfg.

   De volgende codesteekproef toont hoe u de [!DNL Path] attributen zou plaatsen als uw rapporten aan werden bewaard [!DNL E:\VSReport\ReportOutput]:

   ```
   < . . . 
   AppIsolated="2" 
       AppRoot="/LM/W3SVC/1/Root/PortalName/OutputFolder" 
       DirBrowseFlags="DirBrowseShowDate | DirBrowseShowTime |...  
       Path="E:\VSReport\ReportOutput"
   ```

   >[!NOTE]
   >
   >Het is kritiek dat het [!DNL Path] attribuut behoorlijk wordt geplaatst.

1. Als u het gebrek [!DNL Path] van het [!DNL Output] element veranderde, beweeg het [!DNL profiles.xml] dossier van *\PortalName*\PortalFiles\Output folder to the output directory that you specified in Step 4. In het voorbeeld hierboven, zou u zich [!DNL profiles.xml] aan bewegen [!DNL E:\VSReport\ReportOutput].

1. Verifieer dat de [!DNL Path] attributen voor alle andere [!DNL IIsWebVirtualDir] [!DNL C:\Inetpub\wwwroot] elementen aan de correcte plaats door naar alle instanties van te zoeken en elk te vervangen met de correcte weg in kaart worden gebracht.

1. Sla het bestand op. Als u het oorspronkelijke dossier wilt bewaren, kunt u het configuratiedossier bewaren gebruikend een nieuwe naam.

## Om het Dossier van de Configuratie in IIS in te voeren {#section-9d61f6bfa93846dcb96973fec5573b19}

1. Op de machine waar [!DNL Report Portal] wordt geïnstalleerd, begin Manager IIS gebruikend **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Systems (IIS) Manager]**.

1. Selecteer **[!UICONTROL (local computer)]** > **[!UICONTROL Web Sites]** > **[!UICONTROL Default Web Site]**.

1. Klik met de rechtermuisknop **[!UICONTROL Default Web Site]** en selecteer **[!UICONTROL New]** > **[!UICONTROL Virtual Directory]** (van bestand).

1. Select the **[!UICONTROL ReportPortalSetup.xml]** file and click **[!UICONTROL Read File]**.

1. Verifieer dat zes virtuele folders voor uw [!DNL Report Portal] zoals aangetoond in het volgende voorbeeld vermeld zijn.

   ![](assets/rptPort_dia_VirDirs.png)

   Als u zes virtuele folders niet ziet of als u een foutenmelding ontvangt, klik **[!UICONTROL Cancel]** en onderzoek het configuratiedossier voor fouten.

1. Selecteer de eerste virtuele folder in de lijst (die de ouder van de andere vijf is) en klik **[!UICONTROL OK]**. IIS voert de afbeeldingen in en voegt de virtuele folders aan de StandaardWebsite toe.

   Zorg ervoor dat de resulterende folderstructuur één ouderomslag (met de zelfde naam zoals uw portaal) en vijf subdirectories zoals aangetoond in het volgende voorbeeld heeft.

   ![](assets/rptPort_scrn_VirDirs_Installed.png)

1. Klik elke virtuele folder om ervoor te zorgen dat IIS van de fysieke folder de plaats kan bepalen het vertegenwoordigt. Als IIS een fout toont, klik de virtuele foldernaam met de rechtermuisknop aan en verifieer dat het [!DNL Local Path] gebied aan de correcte fysieke folder richt.

## Om de Actieve Pagina&#39;s van de Server (ASPs) op IIS toe te laten {#section-a7725ec2afc64ffc854c5bd8c5c31802}

Om te gebruiken [!DNL Report Portal], moet ASPs op IIS worden toegelaten. (Door gebrek, is ASPs gehandicapt wanneer IIS 6.0 geïnstalleerd is.) Gebruik de volgende procedure om te verifiëren dat ASPs op uw IIS wordt toegelaten.

1. In het venster van de Manager IIS, selecteer **[!UICONTROL (local computer)]** > **[!UICONTROL Web Service Extensions]**.
1. Verifieer dat de [!DNL Active Server Pages] uitbreiding aan wordt geplaatst [!DNL Allowed].

   ![](assets/report_aspenable.png)

1. Als hun Status Verboden is, selecteer **[!UICONTROL Active Server Pages]** en klik **[!UICONTROL Allow]**.
1. Sluit IIS Manager.

