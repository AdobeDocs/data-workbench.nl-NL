---
description: Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 5.0) in kaart te brengen.
title: Het Portaal van het Rapport van de toewijzing aan een Virtuele Folder (IIS 5.0)
uuid: 9514c33e-c139-4cc2-97c2-8b241522c44d
exl-id: 20d8e9ea-c5b6-4a1b-9b15-557cc71ad5d9
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Het Portaal van het Rapport van de toewijzing aan een Virtuele Folder (IIS 5.0){#mapping-report-portal-to-a-virtual-directory-iis}

{{eol}}

Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 5.0) in kaart te brengen.

1. Op de computer [!DNL Report Portal] is geïnstalleerd, begin de Manager IIS gebruikend of **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services]** of **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services]**.

1. Selecteren **[!UICONTROL Local Machine]** > **[!UICONTROL Web Sites]** > **[!UICONTROL Default Web Site]**.

1. Klikken met rechtermuisknop **[!UICONTROL Default Web Site]** en selecteert u **[!UICONTROL New]** > **[!UICONTROL Virtual Directory]**.

1. Wanneer de [!DNL Virtual Directory Wizard] opent, klikt u op **[!UICONTROL Next]**.

1. Voer de volgende stappen uit om de virtuele hoofdmap te definiëren voor [!DNL Report Portal]:

   1. Typ de naam van het dialoogvenster [!DNL Report Portal]en klik vervolgens op **[!UICONTROL Next]**. Als u bijvoorbeeld &quot;Portal&quot; wilt gebruiken als naam voor uw [!DNL Report Portal], wijst u de alias &#39;Portal&#39; toe aan de virtuele map. Klikken **[!UICONTROL Next]** wanneer gereed.

   1. Blader naar het fysieke pad en selecteer het *&lt;**[!UICONTROL PortalName]**>* **[!UICONTROL \PortalASP]** map, klik vervolgens op **[!UICONTROL Next]**.

      Voorbeeld: [!DNL C:\Inetpub\wwwroot\Portal\PortalASP]

   1. Controleer wanneer u om machtigingen wordt gevraagd of de volgende opties zijn ingeschakeld:

      * **[!UICONTROL Read]**
      * **[!UICONTROL Run scripts (such as ASP)]**
   1. Klikken **[!UICONTROL Next]** en klik vervolgens op **[!UICONTROL Finish]**. De virtuele folder die u creeerde verschijnt onder de StandaardWebsite zoals aangetoond in het volgende voorbeeld.

   ![](assets/RptPort_scrn_VirDirManual.png)

1. Klik met de rechtermuisknop op de virtuele map die u net hebt gemaakt en selecteer **[!UICONTROL New]** > **[!UICONTROL Virtual Directory]**.

1. Gebruik de [!DNL Virtual Directory] gebruiken om een alias voor elk van de volgende fysieke mappen te maken. Als u dit doet, wordt een correct benoemde virtuele map gemaakt voor elk van deze fysieke bronnen.

<table id="table_B2E04423C20F40CAA8EDA3FCBA210AA2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Deze alias maken. . . </th> 
   <th colname="col2" class="entry"> Voor deze fysieke bron. . . </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Kern </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalBestanden\Core </p> <p>Voorbeeld: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\Core</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CSS </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\CSS </p> <p>Voorbeeld: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\CSS</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> HTC </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\HTC </p> <p>Voorbeeld: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\HTC</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afbeeldingen </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\Images </p> <p>Voorbeeld: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\Images</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> <p>Fysieke locatie van de map waarin <span class="keyword"> Rapportserver</span> Slaat de output voor uw rapportreeksen op. De outputomslag kan overal worden gevestigd, kan om het even wat worden genoemd, en bevat een subfolder voor elke rapportreeks. </p> <p>Dit moet dezelfde map zijn als die u opgeeft in de parameter Uitvoer in het dialoogvenster <span class="filepath"> Report.cfg</span> bestand voor een rapportset. Zie voor meer informatie <a href="../../../../home/c-rpt-oview/c-admin-rpt/c-config-rpt-files.md#concept-cf4b95344fcb4c8c877db91e5f1d345d"> Report.cfg-bestanden configureren</a>. </p> <p>De standaardlocatie is \<i>PortalName</i>\PortalFiles\Output. </p> <p>Voorbeeld: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\Output</span> </p> <p>De <i>PortalName</i>\PortalFiles\Output directory bevat de map <span class="filepath"> profiles.xml</span> bestand, dat moet worden verplaatst naar de uitvoermap die u voor deze alias opgeeft. </p> <p>Het is van essentieel belang dat de <span class="wintitle"> Pad</span> wordt ingesteld. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Wanneer u wordt gebeëindigd, verifieer dat IIS zes nieuwe virtuele folders toont. Zorg ervoor dat de mappenstructuur één bovenliggende map (met dezelfde naam als uw portal) en vijf submappen heeft, zoals hieronder wordt weergegeven.

   ![](assets/rptPort_scrn_VirDirs_Installed.png)

1. Ga als u klaar bent naar [Het sessieconfiguratiebestand bewerken](../../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7) om het installatieproces voort te zetten.
